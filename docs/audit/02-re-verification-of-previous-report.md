# Повторная проверка прежнего отчёта и ростеров

**Дата и время проверки: 2026-11-08 19:10 UTC** — получено собственной командой `date -u`, а не скопировано из прежнего отчёта.

**Принцип проверки:** прежние ответы ИИ и журнал итераций проекта **не считаются доказательством**. Каждое утверждение перепроверено через GitHub API, `gh`, реальный `git clone` и загрузку исходных страниц вики.

---

## 1. Ветка по умолчанию и существование `master`

| Проверка | Команда | Результат |
|---|---|---|
| Ветка по умолчанию | `git clone` + вывод | `origin/HEAD -> origin/main` |
| HEAD ветки main | `git rev-parse HEAD` в свежем клоне | `20035e0` |
| Существует ли `master` | `git ls-remote origin refs/heads/master` | **пусто** |
| Все ветки | `git ls-remote --heads origin` | `main` + 3 ветки `arena/*` |

**Вывод: ветки `master` НЕ существует.** Утверждение прежнего отчёта «существует две ветки — `main` и `master`» **опровергнуто**. Редирект GitHub на ветку по умолчанию действительно не является доказательством существования `master`, и прямой запрос refs это подтвердил: ветки нет, все файлы находятся на `main`.

Ветки на момент проверки:

| Ветка | SHA | Защита |
|---|---|---|
| `main` | `20035e0` | нет |
| `arena/31f2dd7a-retro-time` | `1acd5fa` | нет |
| `arena/d3cf9574-retro-time` | `90a5c731` | нет |
| `arena/fd27dbba-retro-time` | `9f3b80c` | нет |

---

## 2. Файлы на `main` @ `20035e0` — фактическая проверка

Свежий клон, `git ls-files -s` и `wc -l`. **Все 16 файлов реально присутствуют, размеры ненулевые.**

| Файл | Строк | blob | Статус |
|---|---:|---|---|
| `README.md` | 54 | `cf0b68ed` | есть |
| `docs/audit/01-github-audit.md` | 126 | `2fcda137` | есть |
| `docs/decisions/01-status.md` | 268 | `8fcaa361` | есть |
| `docs/design/01-core-loop-and-modes.md` | 537 | `418266d7` | есть |
| `docs/design/02-obraz-implementation.md` | 335 | `90a76ef1` | есть |
| `docs/design/03-one-bounce.md` | 267 | `6b53450f` | есть |
| `docs/iterations/01-iteration-log.md` | 289 | `daa2310c` | есть |
| `docs/research/00-research-report.md` | 575 | `4e3940b0` | есть |
| `docs/research/01-voice-chat-matchmaking.md` | 251 | `e360ae87` | есть |
| `docs/research/02-core-loop-references.md` | 422 | `5001f75a` | есть |
| `docs/research/rosters/00-index.md` | 96 | `5b562b13` | есть |
| `docs/research/rosters/01-forsaken.md` | 163 | `d6562ca8` | есть |
| `docs/research/rosters/02-bite-by-night.md` | 123 | `3cbda2fd` | есть |
| `docs/research/rosters/03-die-of-death.md` | 114 | `10a1a660` | есть |
| `docs/research/rosters/04-violence-district.md` | 125 | `29f96a57` | есть |
| `docs/research/rosters/05-dead-by-daylight.md` | 220 | `ea9ffc01` | есть |

**7 файлов, которые прежний отчёт заявлял как созданные** (`docs/audit/01-github-audit.md` и 6 файлов `docs/research/rosters/*`), **все присутствуют**. Заявление подтверждено.

---

## 3. CI — точная формулировка

| Проверка | Результат |
|---|---|
| `gh api repos/GoShadowS/retro-time/contents/.github/workflows` | **HTTP 404** |
| `git ls-files \| grep -i github` | путь `.github` в дереве **отсутствует** |
| `gh pr checks` по PR #1–#6 | «no checks reported» |

**Формулировка: в репозитории отсутствуют файлы workflow и каталог `.github` целиком, то есть CI не настроен.** Это сильнее, чем «проверок не было» Я **не** делаю вывод «CI отключён» — его просто нет.

---

## 4. PR #1–#6 — head commit и merge commit раздельно

Все данные получены через `gh api repos/GoShadowS/retro-time/pulls/N`. **Все шесть пар SHA, заявленных прежним отчётом, подтверждены.**

| PR | state | base ← head | **head commit** | **merge commit** | создан → слит (UTC) | файлов | ± |
|---:|---|---|---|---|---|---:|---:|
| #1 | MERGED | `main` ← `arena/31f2dd7a-retro-time` | `549efa5` | `d2d52dd` | 17:45:53 → 17:46:01 | 9 | +2625 / −1 |
| #2 | MERGED | `main` ← `arena/31f2dd7a-retro-time` | `1acd5fa` | `419f70b` | 17:46:44 → 17:46:52 | 1 | +13 / −1 |
| #3 | MERGED | `main` ← `arena/d3cf9574-retro-time` | `9aad502` | `fa7e3b3` | 18:36:28 → 18:37:05 | 4 | +469 / −249 |
| #4 | MERGED | `main` ← `arena/d3cf9574-retro-time` | `90a5c73` | `a3fa96b` | 18:37:34 → 18:37:40 | 1 | +15 / −1 |
| #5 | MERGED | `main` ← `arena/fd27dbba-retro-time` | `5d587d4` | `58f1e8f` | 19:05:28 → 19:05:36 | **9** | **+1073 / −4** |
| #6 | MERGED | `main` ← `arena/fd27dbba-retro-time` | `9f3b80c` | `20035e0` | 19:06:11 → 19:06:13 | 1 | +26 / −1 |

В каждом PR ровно **1 коммит** (проверено через `/pulls/N/commits`).

### PR #5 — проверка пофайлово (было отдельное требование)

`gh api .../pulls/5/files` — **ровно 9 файлов**, цифры сходятся:

| Файл | Статус | ± |
|---|---|---:|
| `README.md` | M | +41 / −4 |
| `docs/audit/01-github-audit.md` | A | +126 |
| `docs/iterations/01-iteration-log.md` | M | +65 |
| `docs/research/rosters/00-index.md` | A | +96 |
| `docs/research/rosters/01-forsaken.md` | A | +163 |
| `docs/research/rosters/02-bite-by-night.md` | A | +123 |
| `docs/research/rosters/03-die-of-death.md` | A | +114 |
| `docs/research/rosters/04-violence-district.md` | A | +125 |
| `docs/research/rosters/05-dead-by-daylight.md` | A | +220 |

**Итого +1073 / −4 — совпадает с заявленным.**

### Кто что менял

| Что | PR |
|---|---|
| `README.md` | **PR #5** (и только он) |
| `docs/iterations/01-iteration-log.md` | создан в PR #3, дополнен в **PR #5** (+65), ещё раз в **PR #6** (+26) |

### Итоговая точка `main`

`git rev-parse HEAD` в свежем клоне = **`20035e0`** = merge commit PR #6 = заявленный прежним отчётом SHA. **Совпадает.**

---

## 5. `README.md` — проверено по содержимому

Файл переписан в PR #5 и содержит: описание проекта, фиксированные ростеры (Default 1v8; Double Trouble 2v12; One Bounce — событие 8×1 на Default; Two Bounce — 12×2 на Double Trouble), основной цикл, перечень документации, статус персонажей. **Факт обновления подтверждён и пофайловым diff PR #5, и чтением файла.**

---

## 6. Ссылки внутри документов

`grep -rhoE https?://` по всем 16 файлам — 200 уникальных внешних URL. Распределение по доменам (топ):

| Домен | URL | Принадлежность |
|---|---:|---|
| `deadbydaylight.wiki.gg` | 111 | Dead by Daylight, официальная вики |
| `die-of-death.fandom.com` | 51 | Die of Death |
| `forsaken.wiki` | 29 | Forsaken, официальная вики |
| `bite-by-night.fandom.com` | 20 | Bite By Night |
| `forsaken2024.fandom.com` | 18 | Forsaken, **неофициальная** вики |
| `create.roblox.com` | 14 | Roblox |
| `forsakenhub.com` | 12 | Forsaken, сторонний сайт |
| `violencedistrictroblox.wiki` | 12 | Violence District |

**Проверка «той ли игре принадлежит ссылка»**: распределение по доменам согласовано с разделами документов — каждая вики цитируется только в файле своей игры. Перекрёстного цитирования не обнаружено.

**Предупреждение, которое следует сохранить:** `forsaken2024.fandom.com` — **неофициальная** вики Forsaken; официальная — `forsaken.wiki`. Ссылки на неё в `docs/research/00-research-report.md` оставлены как исторические, но置信度 у них ниже.

**Внутренние markdown-ссылки**: в документах есть ссылки только на файлы ростеров `01`–`05` из `00-index.md`. На момент PR #5 все пять файлов существовали, **битых внутренних ссылок нет**.

---

## 7. Сводка по утверждениям прежнего отчёта

| Утверждение | Вердикт |
|---|---|
| Существуют две ветки, `main` и `master` | **ОПРОВЕРГНУТО** — `master` не существует |
| Ветка по умолчанию — `main` | подтверждено |
| HEAD `main` = `20035e0` | подтверждено |
| PR #1–#4 слиты, SHA верны | подтверждено |
| PR #5 и #6 существуют и слиты | подтверждено |
| PR #5 меняет 9 файлов, +1073/−4 | подтверждено пофайлово |
| PR #5 меняет README, PR #6 — журнал итераций | подтверждено |
| 16 файлов на `main` | подтверждено |
| «Проверок CI нет» | подтверждено, но **уточнено**: workflow-файлов и каталога `.github` нет вообще |
| 7 новых файлов созданы | подтверждено |

---

## 8. Что изменено в этой проверке

| Файл | Изменение |
|---|---|
| `docs/research/rosters/05-dead-by-daylight.md` | Переписан: добавлены **все 45 сил убийц с игровыми псевдонимами и настоящими именами** (по `Powers` и `Module:Datatable`); добавлены все **55 выживших**; зафиксировано расхождение 55 против 54 |
| `docs/research/rosters/04-violence-district.md` | Переписан полностью: **все 9 убийц со способностями и перками**; конфликт 8/9 **разрешён**; Jason / Michael Myers / Jeff the Killer / Jacket **разрешены как скины** |
| `docs/research/rosters/03-die-of-death.md` | **Расхождение 11 vs 15 разрешено в пользу 15** (прямая цитата страницы Abilities + косвенное подтверждение 105 = C(15,2)); добавлен полный перечень из 15 способностей; отдельно вынесены Panel-Exclusive и Upcoming |
| `docs/research/rosters/01-forsaken.md` | Добавлены постранично подтверждённые данные по **Shedletsky** и **Elliot** (категория, HP, скорости, полный текст способностей); явно зафиксировано, что способности остальных 19 персонажей **не подтверждены** и почему |
| `docs/audit/02-re-verification-of-previous-report.md` | Этот файл |
| `docs/research/rosters/00-index.md` | Обновлён: снята пометка «не подтверждено» с DbD, зафиксирован статус проверки |
| `docs/iterations/01-iteration-log.md` | Добавлена Итерация 4 |

---

## 9. Что осталось непроверенным — честно

| Пункт | Причина |
|---|---|
| Способности 11 выживших и 8 убийц Forsaken | Персональные страницы `forsaken.wiki` — по 9 фрагментов каждая; `api.php` и `rest.php/v1` на хосте недоступны (ответ «File not found») |
| Описания 45 сил DbD (есть только названия) | Описания формируются отдельным модулем `Loadout.getPowerByOwner`, напрямую не выгружаются |
| Персональные перки 55 выживших DbD | Раздел формируется модулем `Loadout.getPerksByCategory`; 165 отдельных перков не выгружены |
| Способности убийц Bite By Night, Die of Death, Violence District | Не выгружены в этой итерации |
| ~~Конфликт 8 против 9 убийц Violence District~~ | **Снят:** патчноут The Butcher — «October 24, 2026 — The Butcher was added to the game». Гипотеза из прошлой итерации **подтверждена документально** |
| Список выживших Violence District | Страница Survivors отдаёт пустой HTML-скелет при `?action=raw`. Получены только предметы и отдельные перки |
| Статусы DbD-персонажей после изъятия лицензий | Известны даты `retracted` для глав HALLOWEEN (19.01.2026) и Hellraiser (04.04.2025), но **влияние на доступность персонажей не проверялось** |
