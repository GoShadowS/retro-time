# Независимый аудит и проверка ответа ИИ от 19:23 UTC — 2026-11-08

**Дата и время проверки: 2026-11-08 19:39:59 UTC** (собственная команда `date -u`, epoch 1794166799).

**Метод:** `gh api` (REST), `git ls-remote`, свежий `git clone`, `git log --all --name-only`, `fetch_page` с `?action=raw`, веб-поиск. Ни журнал итераций, ни предыдущие ответы ИИ, ни уже созданные документы не использовались как доказательство.

**О временных метках.** Предыдущий ответ сообщал период 19:10–19:23 UTC и merge PR #7 в 19:23:46 UTC. Момент проверки — **19:39:59 UTC**, то есть заявленное событие находится **в прошлом** и может быть проверено. Все семь временных меток подтверждены API.

---

## 1. Сводка: утверждение / вердикт

| № | Утверждение предыдущего ответа | Вердикт | Доказательство |
|---:|---|---|---|
| 1 | Основная ветка — `main` | **подтверждено** | `git ls-remote --heads origin` → `main`; `symbolic-ref refs/remotes/origin/HEAD` → `origin/main` |
| 2 | HEAD `main` = `e31ff0e` | **подтверждено** | `git ls-remote` и свежий клон: `e31ff0e21b3283da33fbe8c3b361e34ee3f11f6f` |
| 3 | Ветки `master` не существует | **подтверждено** | `git ls-remote origin refs/heads/master` → пусто |
| 4 | После PR #7 на `main` — `e31ff0e`, новых коммитов нет | **подтверждено** | `gh api .../commits` — последний коммит `e31ff0e`, 19:23:46Z |
| 5 | В репозитории 17 файлов | **подтверждено** | свежий клон: `git ls-files \| wc -l` = 17 |
| 6 | Workflow-файлов и `.github` нет | **подтверждено, усилено** | см. раздел 3 |
| 7 | PR #1–#6: head/merge SHA и.diff верны | **подтверждено** | все шесть пар совпали |
| 8 | PR #5 — 9 файлов, +1073/−4 | **подтверждено** | `/pulls/5/files`, пофайлово |
| 9 | PR #5 меняет README; PR #6 — журнал итераций | **подтверждено** | `/pulls/5/files` и `/pulls/6/files` |
| 10 | PR #7 слит, head `3160be8`, merge `e31ff0e`, 7 файлов, +636/−288 | **подтверждено** | `/pulls/7`, `/pulls/7/files` |
| 11 | **«В каждом PR ровно 1 коммит»** | **ОПРОВЕРГНУТО** | PR #1 содержит **7 коммитов** |
| 12 | DoD: 15 способностей и 4 Synergies | **подтверждено** (цитата со страницы) | раздел 5 |
| 13 | DbD: 45 сил с псевдонимами получены | **подтверждено** | предыдущая итерация, страница Powers |
| 14 | DbD: 55 Survivors, но есть расхождение со счётчиком 54 | **подтверждено как расхождение** | не разрешено, вариант не выбран |
| 15 | VD: 9 убийц, The Butcher добавлен 24.10.2026 | **подтверждено** | патчноут на странице The Butcher |
| 16 | VD: Jason / Michael Myers / Jeff the Killer / Jacket — скины | **подтверждено** | таблицы образов и патчноуты |
| 17 | `The Slasher = Jason Voorhees = Omnipresent Evil` (DbD) | **подтверждено, уточнено** | независимые источники; зафиксировано совпадение имён с VD |
| 18 | Forsaken: Shatterpoint HP у **Guest 1337** | **ОПРОВЕРГНУТО** | Shatterpoint HP и 40% сопротивления — у **Jane Doe** |
| 19 | Forsaken: overheal у Noob и Dusekkar | **не подтверждено** | в выгруженных данных overheal есть только у Guest 1337 |
| 20 | Helperbot добавлен в «New Beginnings», игра в Beta | **не подтверждено** | на странице Helperbot указана **версия 5.3.0**; названия и статуса в данных нет |
| 21 | Forsaken: 13 Survivors, 8 Killers | **подтверждено** | 13 + 8, по персональным страницам |
| 22 | Forsaken: способности только у Shedletsky и Elliot | **ОПРОВЕРГНУТО как ограничение** | выгружены способности всех 13 Survivors и всех 8 Killers (часть — неполно) |
| 23 | Персонажей retro time нет | **подтверждено** | раздел 6 |

---

## 2. Аудит GitHub

### Ветки

| Ветка | SHA | Назначение |
|---|---|---|
| `main` | `e31ff0e` | основная |
| `arena/31f2dd7a-retro-time` | `1acd5fa` | PR #1, #2 |
| `arena/d3cf9574-retro-time` | `90a5c73` | PR #3, #4 |
| `arena/fd27dbba-retro-time` | `9f3b80c` | PR #5, #6 |
| `arena/13309d0b-retro-time` | `3160be8` | PR #7 |
| `master` | — | **не существует** |

### Таблица PR #1–#7 (все данные из `gh api repos/GoShadowS/retro-time/pulls/N`)

| PR | state | base ← head | **head commit** | **merge commit** | created → merged (UTC) | файлов | ± | коммитов |
|---:|---|---|---|---|---|---:|---:|---:|
| #1 | MERGED | `main` ← `arena/31f2dd7a-retro-time` | `549efa5` | `d2d52dd` | 17:45:53 → 17:46:01 | 9 | +2625/−1 | **7** |
| #2 | MERGED | `main` ← `arena/31f2dd7a-retro-time` | `1acd5fa` | `419f70b` | 17:46:44 → 17:46:52 | 1 | +13/−1 | 1 |
| #3 | MERGED | `main` ← `arena/d3cf9574-retro-time` | `9aad502` | `fa7e3b3` | 18:36:28 → 18:37:05 | 4 | +469/−249 | 1 |
| #4 | MERGED | `main` ← `arena/d3cf9574-retro-time` | `90a5c73` | `a3fa96b` | 18:37:34 → 18:37:40 | 1 | +15/−1 | 1 |
| #5 | MERGED | `main` ← `arena/fd27dbba-retro-time` | `5d587d4` | `58f1e8f` | 19:05:28 → 19:05:36 | 9 | +1073/−4 | 1 |
| #6 | MERGED | `main` ← `arena/fd27dbba-retro-time` | `9f3b80c` | `20035e0` | 19:06:11 → 19:06:13 | 1 | +26/−1 | 1 |
| #7 | MERGED | `main` ← `arena/13309d0b-retro-time` | `3160be8` | `e31ff0e` | 19:23:39 → 19:23:46 | 7 | +636/−288 | 1 |

**Все семь заявленных пар head/merge SHA подтверждены.** Даты создания и merge совпадают.

**Найденная ошибка предыдущего отчёта:** в аудите PR #2 утверждалось «В каждом PR ровно 1 коммит». **PR #1 содержит 7 коммитов**:

| SHA | Сообщение |
|---|---|
| `abe1ec5` | docs: add research report on references and project status decisions |
| `cfa6b7d` | docs: record retro-slop/platform/BBN decisions and voice chat matchmaking analysis |
| `93e352a` | docs: add core loop and three-mode balance proposals |
| `e1b5983` | docs: Obraz implementation variants, A2 risk analysis, One Bounce concept choice |
| `d07f47e` | docs: withdraw decoy concept, record V3 Nakoplenie, add One Bounce Attrition concept |
| `78b5166` | Merge: reconcile local final state with previously pushed history |
| `549efa5` | docs: align project docs with full requirements (modes, copied core loop, Bounce rules) |

Именно поэтому PR #1 дал +2625/−1 в 9 файлах при одном «логическом» изменении — это восстановление истории.

### PR #5 — пофайлово

| Файл | Статус | ± |
|---|---|---:|
| `README.md` | modified | +41/−4 |
| `docs/audit/01-github-audit.md` | added | +126 |
| `docs/iterations/01-iteration-log.md` | modified | +65 |
| `docs/research/rosters/00-index.md` | added | +96 |
| `docs/research/rosters/01-forsaken.md` | added | +163 |
| `docs/research/rosters/02-bite-by-night.md` | added | +123 |
| `docs/research/rosters/03-die-of-death.md` | added | +114 |
| `docs/research/rosters/04-violence-district.md` | added | +125 |
| `docs/research/rosters/05-dead-by-daylight.md` | added | +220 |

Итого +1073/−4 — совпадает. **PR #5 создал 7 файлов ростеров и аудита, изменил README и журнал итераций.**

### PR #7 — пофайлово

| Файл | Статус | ± |
|---|---|---:|
| `docs/audit/02-re-verification-of-previous-report.md` | added | +186 |
| `docs/iterations/01-iteration-log.md` | modified | +37 |
| `docs/research/rosters/00-index.md` | modified | +18/−16 |
| `docs/research/rosters/01-forsaken.md` | modified | +44/−2 |
| `docs/research/rosters/03-die-of-death.md` | modified | +28/−4 |
| `docs/research/rosters/04-violence-district.md` | modified | +162/−82 |
| `docs/research/rosters/05-dead-by-daylight.md` | modified | +161/−184 |

Итого 7 файлов, +636/−288 — совпадает. **PR #7 изменил аудит, Forsaken, Die of Death, Violence District, Dead by Daylight, индекс и журнал — как и заявлялось. README PR #7 не трогал.**

### Проверка файлов на `main` @ `e31ff0e`

Все 17 файлов присутствуют в свежем клоне, размеры ненулевые. Разделение по PR:

| Файл | Когда появился / последний раз изменён |
|---|---|
| `README.md` | изменён в **PR #5** |
| `docs/audit/01-github-audit.md` | создан в **PR #5** |
| `docs/audit/02-re-verification-of-previous-report.md` | создан в **PR #7** |
| `docs/decisions/01-status.md` | исходный, изменён в **PR #1** |
| `docs/design/01-core-loop-and-modes.md` | исходный |
| `docs/design/02-obraz-implementation.md` | исходный |
| `docs/design/03-one-bounce.md` | исходный |
| `docs/iterations/01-iteration-log.md` | создан **PR #3**, изменён **PR #5** и **PR #7** |
| `docs/research/00-research-report.md` | исходный |
| `docs/research/01-voice-chat-matchmaking.md` | исходный |
| `docs/research/02-core-loop-references.md` | исходный |
| `docs/research/rosters/00-index.md` … `05-dead-by-daylight.md` | созданы **PR #5**, изменены **PR #7** (кроме `02-bite-by-night.md`) |

---

## 3. CI — три разных вопроса, три разных ответа

| Вопрос | Проверка | Результат |
|---|---|---|
| Есть ли **workflow-файлы** в дереве? | `gh api .../actions/workflows --jq .total_count` | **0** |
| Есть ли **checks** у конкретных PR? | `check-runs` для head SHA каждого из PR #1–#7 | **0** для всех семи |
| Есть ли **CI вообще**? | `gh api .../contents/.github/workflows` → HTTP 404; `git ls-tree HEAD` → только `README.md` и `docs`; `git log --all --diff-filter=A --name-only` по паттернам `.github\|workflow\|\.yml\|\.yaml` | **ни одного файла `.github`, workflow, `.yml`, `.yaml` никогда не существовало ни в одном коммите ни на одной ветке** |

**Формулировка:** в репозитории **отсутствуют файлы CI-конфигурации и каталог `.github` целиком**, Actions не настроены (0 workflow), проверки ни у одного PR не запускались. Это подтверждено четырьмя независимыми способами, а не одним 404.

---

## 4. Forsaken — что исправлено

Полный ростер с способностями выгружен по персональным страницам и сохранён в `docs/research/rosters/01-forsaken.md`.

**Главное исправление:** предыдущий отчёт приписал **Shatterpoint HP и врождённое сопротивление 40%** персонажу **Guest 1337**. По странице **Jane Doe** это её механика:

> «**Shatterpoint** — Jane Doe has a unique health type that is unable to be healed by outside means, but has **40% damage reduction**. Jane Doe spawns with 20 Shatterpoints HP…»

У **Guest 1337** пассивные — **Made To Last** (+10 HP) и **Self Sacrifice** (приоритет попадания). Overheal подтверждён только у него: Block даёт «+10 permanent overheal HP».

**Категории выживших подтверждены:** Sentinels — 5, Supports — 5, Survivalists — 3.

**Статусные пометки, найденные на страницах:** 007n7 помечен `{{Revamp}}` (переработка набора в работе); Noli помечен `{{Revamp}}` (замена озвучки, переписывание лора); страница Helperbot помечена `{{Stub}}`.

---

## 5. Die of Death — цитата вместо арифметики

Требование «не использовать только вывод 105 = C(15,2)» принято. **Прямой источник** — страница `die-of-death.fandom.com/wiki/Abilities` (`?action=raw`):

> «There is currently **15 Abilities** and **4 Synergies** in Die of Death»

Арифметика (105 = C(15,2)) приводилась только как **дополнительное** согласующееся наблюдение, а не как доказательство. Полный перечень из 15 способностей: Adrenaline, Banana Peel, Block, BonusPad, Bugle, Caretaker, Cloak, Dash, Flashlight, Hotdog, Punch, Pie, Reroll, Revolver, Taunt. Отдельно: Panel-Exclusive (ShotgunShoot, ShotgunKick) и Upcoming (Unknown Hood, Careless).

---

## 6. Персонажи retro time

**Проверено по текущему состоянию репозитория (`main` @ `e31ff0e`, 17 файлов).**

| Критерий | Результат |
|---|---|
| Персонажи, прямо утверждённые пользователем | **Не найдено** |
| Персонажи, реализованные в коде | **Кода игры в репозитории нет** — только документация |
| Файлы с ростером retro time | **Не найдено** |

**Подтверждённых или реализованных персонажей retro time нет.** Все имена в документах относятся к референсным играм и помечены как чужая интеллектуальная собственность, которую **нельзя** копировать (см. `docs/decisions/01-status.md` §4.1 и `docs/research/00-research-report.md`).

Установленные **требования** (не персонажи): R6, а не R15; авторские R6-анимации; классическая одежда Roblox или оригинальные R6-совместимые 3D-детали; читаемость важнее стилистической избыточности.

**[Неутверждённое предложение, не решение пользователя]:** список ролей и способностей в `docs/decisions/01-status.md` §9 по-прежнему имеет статус «Не утверждено». Прежде чем обсуждать персонажей, логично зафиксировать **роли** под уже утверждённые составы 1v8, 2v12, 8v1, 12v2. Это предложение, а не решение.

---

## 7. Что НЕ удалось проверить или завершить

| Пункт | Причина | Статус |
|---|---|---|
| **Способности DbD**: описания всех 45 Powers | Описания формируются модулем `Loadout.getPowerByOwner` и не отдаются через `?action=raw`; прямой обход 45 страниц не поместился в бюджет этой проверки | **Не завершено** |
| **Персональные Perks DbD**: 165 записей | Раздел формируется модулем `Loadout.getPerksByCategory`; компактного источника не найдено | **Не завершено** |
| Способности **The Project** и **The Doppelganger** (BBN) | Персональные страницы не выгружались | **Не завершено** |
| Способности **Badware, Artful, Harken, Killdroid** (DoD) | Персональные страницы не выгружались | **Не завершено** |
| Неполные наборы Forsaken: Dusekkar (Plasma Beam), Veeronica (Sk8, Broadcast), Jane Doe (Hatchet), Noli (Void Rush, Nova, Observant), Guest 666 (Eviscerate, Demonic Pursuit, Infernal Cry, Blood Hunt), Nosferatu (Ascension, Hunter's Feast), Azure (Seeker Bulb, Stigmatize, Perforating, Pummeling, Golem), 1x1x1x1 (Rejuvenate The Rotten), Slasher (окончание Raging Pace) | Страницы обрезаны на границе фрагмента; выгружен только первый фрагмент | **Частично** |
| Версия/дата выхода **Azure** | Поле `released` отсутствует в выгруженном фрагменте | **Не подтверждено** |
| Exclusive-персонажи и NPC Forsaken (заявленные «6+11» и «5») | Персональные страницы не выгружались | **Не проверено** |
| Список выживших Violence District | Страница Survivors отдаёт пустой HTML-скелет при `?action=raw` | **Не подтверждено** |
| Расхождение DbD 55 против 54 выживших | Два источника данных дают 55, счётчик страницы — 54 | **Не разрешено**, вариант не выбран |
| Roblox ID Bite By Night `70845479499574` против `71008479572236` | Идентификация в этой проверке не перепроверялась; приняты данные предыдущей итерации (вики ссылается на `70845479499574` и группу `totally not secret games`) | **Не перепроверено в этом проходе** |
| Roblox Studio, запуск кода, тест игры | Доступа нет | **Не проводилось** |
| **Данные Violence District в этом проходе не перевыгружались** | Персональные страницы VD не загружались заново; принято содержимое `04-violence-district.md` из `main` @ `e31ff0e` (PR #7), которое опирается на патчноуты с вики. Файл проверен на наличие и структуру, но **не перепроверен по первоисточнику в этом проходе** | **Принято из предыдущей итерации** |
| Roblox ID Bite By Night — повторно | см. выше | **Не перепроверено** |
