# Dead by Daylight — ростер персонажей

**Дата проверки: 2026-11-08.**

## Идентификация игры и источника

| Параметр | Значение | Метка |
|---|---|---|
| Разработчик | **Behaviour Interactive** (BHVR) | [Ф] |
| Релиз | 14 июня 2016 (PC, Steam) | [Ф] |
| Состав | **4 выживших против 1 убийцы** | [Ф] |
| Мир | Процедурно генерируемый | [Ф] |
| Вики | `deadbydaylight.wiki.gg` | **[Ф] — ОФИЦИАЛЬНАЯ** («Official Dead by Daylight Wiki») |

**Источник ростера:** категории `Category:Killers` и `Category:Survivors` на официальной вики.
**Почему категории, а не страница:** страницы Killers и Survivors формируют списки через Lua-модуль `{{#Invoke:Various|resolveCharactersTable}}`, поэтому в викитексте страниц имён нет. Категории же содержат полный перечень страниц.

---

## Стороны и терминология

| Термин | Значение |
|---|---|
| **Killers** | Сторона убийцы. Задача — найти, сбить и повесить Survivors на Hook для принесения в жертву The Entity |
| **Survivors** | Сторона выживших. Задача — починить генераторы, открыть Exit Gate и покинуть Trial Grounds (или уйти через Hatch) |
| **Power** | Уникальная сила каждого Killer |
| **Items** | Предметы Survivors (вместо сил): Firecrackers, Fog Vials, Flashlights, Keys, Maps, Med-Kits, Toolboxes |
| **Perks** | Перки, общие для роли, но у каждого персонажа есть **три персональных** |

Формулировка вики: «Whereas Killers have their **Powers**, Survivors have their **Items**».

---

## Численность: подтверждено

| Сторона | Всего | Оригинальных (BHVR) | Лицензионных | Источник |
|---|---:|---:|---:|---|
| **Killers** | **45** | 25 | 20 | `Module:Killers` → `getCountOfKillers()` **[Ф]** |
| **Survivors** | **54** | 32 | 22 | `Module:Survivors` → `getCountOfSurvivors()` **[Ф]** |

Подтверждено дословно из викитекстраниц: «There are currently 45 Killers featured in *Dead by Daylight*, of which 25 are **Original Characters** (created by BHVR) and 20 are **Licensed Characters** (licensed from other IP holders)».

### Расхождение по Survivors

| Источник | Число |
|---|---:|
| Модуль счётчика (`Module:Survivors`) | **54** |
| `Category:Survivors` (число страниц) | **55** |

**Расхождение в 1 не разрешено.** Возможные причины **[П]**: одна страница в категории не является играбельным персонажем, или счётчик отстаёт. **В список ниже включены все 55 страниц из категории.**

---

## Killers — 45

Имена приведены по **настоящим именам**, как они указаны в категории официальной вики. **Игровые псевдонимы (The Trapper, The Wraith и т. д.) в категории отсутствуют** и отдельно не выгружались.

| # | Имя (по категории) | Страница |
|---:|---|---|
| 1 | Adiris | https://deadbydaylight.wiki.gg/wiki/Adiris |
| 2 | Adriana Imai | https://deadbydaylight.wiki.gg/wiki/Adriana_Imai |
| 3 | Albert Wesker | https://deadbydaylight.wiki.gg/wiki/Albert_Wesker |
| 4 | Amanda Young | https://deadbydaylight.wiki.gg/wiki/Amanda_Young |
| 5 | Anna | https://deadbydaylight.wiki.gg/wiki/Anna |
| 6 | Art The Clown | https://deadbydaylight.wiki.gg/wiki/Art_The_Clown |
| 7 | Bubba Sawyer | https://deadbydaylight.wiki.gg/wiki/Bubba_Sawyer |
| 8 | Burong Sukapat | https://deadbydaylight.wiki.gg/wiki/Burong_Sukapat |
| 9 | Caleb Quinn | https://deadbydaylight.wiki.gg/wiki/Caleb_Quinn |
| 10 | Carmina Mora | https://deadbydaylight.wiki.gg/wiki/Carmina_Mora |
| 11 | Charles Lee Ray | https://deadbydaylight.wiki.gg/wiki/Charles_Lee_Ray |
| 12 | Charlotte & Victor Deshayes | https://deadbydaylight.wiki.gg/wiki/Charlotte_%26_Victor_Deshayes |
| 13 | Danny Johnson alias Jed Olsen | https://deadbydaylight.wiki.gg/wiki/Danny_Johnson_alias_Jed_Olsen |
| 14 | Dracula | https://deadbydaylight.wiki.gg/wiki/Dracula |
| 15 | Evan MacMillan | https://deadbydaylight.wiki.gg/wiki/Evan_MacMillan |
| 16 | Frank Stone | https://deadbydaylight.wiki.gg/wiki/Frank_Stone |
| 17 | Frank, Julie, Susie, Joey | https://deadbydaylight.wiki.gg/wiki/Frank,_Julie,_Susie,_Joey |
| 18 | Freddy Krueger | https://deadbydaylight.wiki.gg/wiki/Freddy_Krueger |
| 19 | Hak Ji-woon | https://deadbydaylight.wiki.gg/wiki/Hak_Ji-woon |
| 20 | Henry Creel | https://deadbydaylight.wiki.gg/wiki/Henry_Creel |
| 21 | Herman Carter | https://deadbydaylight.wiki.gg/wiki/Herman_Carter |
| 22 | HUX-A7-13 | https://deadbydaylight.wiki.gg/wiki/HUX-A7-13 |
| 23 | Jason Voorhees | https://deadbydaylight.wiki.gg/wiki/Jason_Voorhees |
| 24 | Kazan Yamaoka | https://deadbydaylight.wiki.gg/wiki/Kazan_Yamaoka |
| 25 | Ken Kaneki | https://deadbydaylight.wiki.gg/wiki/Ken_Kaneki |
| 26 | Kenneth Chase alias Jeffrey Hawk | https://deadbydaylight.wiki.gg/wiki/Kenneth_Chase_alias_Jeffrey_Hawk |
| 27 | Lisa Sherwood | https://deadbydaylight.wiki.gg/wiki/Lisa_Sherwood |
| 28 | Max Thompson Jr. | https://deadbydaylight.wiki.gg/wiki/Max_Thompson_Jr. |
| 29 | Michael Myers | https://deadbydaylight.wiki.gg/wiki/Michael_Myers |
| 30 | Nemesis T-Type | https://deadbydaylight.wiki.gg/wiki/Nemesis_T-Type |
| 31 | Philip Ojomo | https://deadbydaylight.wiki.gg/wiki/Philip_Ojomo |
| 32 | Portia Maye | https://deadbydaylight.wiki.gg/wiki/Portia_Maye |
| 33 | Pyramid Head | https://deadbydaylight.wiki.gg/wiki/Pyramid_Head |
| 34 | Rin Yamaoka | https://deadbydaylight.wiki.gg/wiki/Rin_Yamaoka |
| 35 | Sadako Yamamura | https://deadbydaylight.wiki.gg/wiki/Sadako_Yamamura |
| 36 | Sally Smithson | https://deadbydaylight.wiki.gg/wiki/Sally_Smithson |
| 37 | Talbot Grimes | https://deadbydaylight.wiki.gg/wiki/Talbot_Grimes |
| 38 | Tarhos Kovács | https://deadbydaylight.wiki.gg/wiki/Tarhos_Kov%C3%A1cs |
| 39 | The Demogorgon | https://deadbydaylight.wiki.gg/wiki/The_Demogorgon |
| 40 | The Dredge | https://deadbydaylight.wiki.gg/wiki/The_Dredge |
| 41 | The Judgment | https://deadbydaylight.wiki.gg/wiki/The_Judgment |
| 42 | The Unknown | https://deadbydaylight.wiki.gg/wiki/The_Unknown |
| 43 | The Xenomorph | https://deadbydaylight.wiki.gg/wiki/The_Xenomorph |
| 44 | Vecna | https://deadbydaylight.wiki.gg/wiki/Vecna |
| 45 | William Afton | https://deadbydaylight.wiki.gg/wiki/William_Afton |

**Уверенность в списке имён: высокая** — категория официальной вики, revision `oldid=107701`, 45 из 45 страниц.

**Powers (силы): НЕ ПОДТВЕРЖДЕНЫ.** Страница Killers формирует список сил через шаблон `{{Powers}}`, содержимое которого не выгружалось.

**Примечание о составных персонажах:** **Charlotte & Victor Deshayes** и **Frank, Julie, Susie, Joey** — это один игровой персонаж каждый (дуэт и группа). Они не являются скинами и не разделяются на отдельных персонажей.

---

## Survivors — 54 (55 страниц в категории)

Имена приведены по категории официальной вики.

| # | Имя | Страница |
|---:|---|---|
| 1 | Ace Visconti | https://deadbydaylight.wiki.gg/wiki/Ace_Visconti |
| 2 | Ada Wong | https://deadbydaylight.wiki.gg/wiki/Ada_Wong |
| 3 | Adam Francis | https://deadbydaylight.wiki.gg/wiki/Adam_Francis |
| 4 | Aestri Yazar & Baermar Uraz | https://deadbydaylight.wiki.gg/wiki/Aestri_Yazar_%26_Baermar_Uraz |
| 5 | Alan Wake | https://deadbydaylight.wiki.gg/wiki/Alan_Wake |
| 6 | Ashley J. Williams | https://deadbydaylight.wiki.gg/wiki/Ashley_J._Williams |
| 7 | Aurora Stardotter | https://deadbydaylight.wiki.gg/wiki/Aurora_Stardotter |
| 8 | Cheryl Mason | https://deadbydaylight.wiki.gg/wiki/Cheryl_Mason |
| 9 | Claudette Morel | https://deadbydaylight.wiki.gg/wiki/Claudette_Morel |
| 10 | David King | https://deadbydaylight.wiki.gg/wiki/David_King |
| 11 | Detective David Tapp | https://deadbydaylight.wiki.gg/wiki/Detective_David_Tapp |
| 12 | Dustin Henderson | https://deadbydaylight.wiki.gg/wiki/Dustin_Henderson |
| 13 | Dwight Fairfield | https://deadbydaylight.wiki.gg/wiki/Dwight_Fairfield |
| 14 | Eleven | https://deadbydaylight.wiki.gg/wiki/Eleven |
| 15 | Ellen Ripley | https://deadbydaylight.wiki.gg/wiki/Ellen_Ripley |
| 16 | Felix Richter | https://deadbydaylight.wiki.gg/wiki/Felix_Richter |
| 17 | Feng Min | https://deadbydaylight.wiki.gg/wiki/Feng_Min |
| 18 | Gabriel Soma | https://deadbydaylight.wiki.gg/wiki/Gabriel_Soma |
| 19 | Haddie Kaur | https://deadbydaylight.wiki.gg/wiki/Haddie_Kaur |
| 20 | Jake Park | https://deadbydaylight.wiki.gg/wiki/Jake_Park |
| 21 | Jane Romero | https://deadbydaylight.wiki.gg/wiki/Jane_Romero |
| 22 | Jeffrey "Jeff" Johansen | https://deadbydaylight.wiki.gg/wiki/Jeffrey_%22Jeff%22_Johansen |
| 23 | Jill Valentine | https://deadbydaylight.wiki.gg/wiki/Jill_Valentine |
| 24 | Jonah Vasquez | https://deadbydaylight.wiki.gg/wiki/Jonah_Vasquez |
| 25 | Kate Denson | https://deadbydaylight.wiki.gg/wiki/Kate_Denson |
| 26 | Kwon Tae-young | https://deadbydaylight.wiki.gg/wiki/Kwon_Tae-young |
| 27 | Lara Croft | https://deadbydaylight.wiki.gg/wiki/Lara_Croft |
| 28 | Laurie Strode | https://deadbydaylight.wiki.gg/wiki/Laurie_Strode |
| 29 | Lee Yun-jin | https://deadbydaylight.wiki.gg/wiki/Lee_Yun-jin |
| 30 | Leon Scott Kennedy | https://deadbydaylight.wiki.gg/wiki/Leon_Scott_Kennedy |
| 31 | Meg Thomas | https://deadbydaylight.wiki.gg/wiki/Meg_Thomas |
| 32 | Michonne Grimes | https://deadbydaylight.wiki.gg/wiki/Michonne_Grimes |
| 33 | Mikaela Reid | https://deadbydaylight.wiki.gg/wiki/Mikaela_Reid |
| 34 | Nancy Wheeler | https://deadbydaylight.wiki.gg/wiki/Nancy_Wheeler |
| 35 | Nea Karlsson | https://deadbydaylight.wiki.gg/wiki/Nea_Karlsson |
| 36 | Nicolas Cage | https://deadbydaylight.wiki.gg/wiki/Nicolas_Cage |
| 37 | Orela Rose | https://deadbydaylight.wiki.gg/wiki/Orela_Rose |
| 38 | Quentin Smith | https://deadbydaylight.wiki.gg/wiki/Quentin_Smith |
| 39 | Rebecca Chambers | https://deadbydaylight.wiki.gg/wiki/Rebecca_Chambers |
| 40 | Renato Lyra | https://deadbydaylight.wiki.gg/wiki/Renato_Lyra |
| 41 | Rick Grimes | https://deadbydaylight.wiki.gg/wiki/Rick_Grimes |
| 42 | Sable Ward | https://deadbydaylight.wiki.gg/wiki/Sable_Ward |
| 43 | Shane Wiigwaas | https://deadbydaylight.wiki.gg/wiki/Shane_Wiigwaas |
| 44 | Sienna Shaw | https://deadbydaylight.wiki.gg/wiki/Sienna_Shaw |
| 45 | Steve Harrington | https://deadbydaylight.wiki.gg/wiki/Steve_Harrington |
| 46 | Taurie Cain | https://deadbydaylight.wiki.gg/wiki/Taurie_Cain |
| 47 | Thalita Lyra | https://deadbydaylight.wiki.gg/wiki/Thalita_Lyra |
| 48 | Trevor Belmont | https://deadbydaylight.wiki.gg/wiki/Trevor_Belmont |
| 49 | Vee Boonyasak | https://deadbydaylight.wiki.gg/wiki/Vee_Boonyasak |
| 50 | Vittorio Toscano | https://deadbydaylight.wiki.gg/wiki/Vittorio_Toscano |
| 51 | William "Bill" Overbeck | https://deadbydaylight.wiki.gg/wiki/William_%22Bill%22_Overbeck |
| 52 | Yoichi Asakawa | https://deadbydaylight.wiki.gg/wiki/Yoichi_Asakawa |
| 53 | Yui Kimura | https://deadbydaylight.wiki.gg/wiki/Yui_Kimura |
| 54 | Zarina Kassir | https://deadbydaylight.wiki.gg/wiki/Zarina_Kassir |
| 55 | Élodie Rakoto | https://deadbydaylight.wiki.gg/wiki/%C3%89lodie_Rakoto |

**Уверенность в списке имён: высокая** — категория официальной вики, revision `oldid=5614`, 55 из 55 страниц.

### Чем различаются Survivors

**Выжившие в Dead by Daylight не имеют отдельных способностей.** Это прямое требование точности: у них нет аналога Killer Power.

Различия подтверждены официальной викой:

| Чем различается | Статус |
|---|---|
| **Персональные перки** — у каждого выжившего свой набор из трёх | Подтверждено наличием раздела «List of Survivor Perks» **[Ф]**, но **конкретные перки по персонажам не выгружены** |
| **Предметы (Items)** — экипируются до матча или находятся в сундуках | Подтверждён перечень типов **[Ф]** |
| **Уникальная анимация ожидания у костра** | Подтверждено: «Each Survivor has a unique animation for waiting around The Campfire» **[Ф]** |
| Лицензированная или оригинальная внешность | Подтверждено разделением 32 / 22 **[Ф]** |

**Персональные перки: НЕ ПОДТВЕРЖДЕНЫ по персонажам.** Страница Survivors формирует их через Lua-модуль `{{#Invoke:Loadout|getPerksByCategory}}`; выгрузка не производилась.

**Примечание о составном персонаже:** **Aestri Yazar & Baermar Uraz** — один игровой персонаж (дуэт), а не два.

**Отделение персонажа от косметики:** лицензированные персонажи (Laurie Strode, Rick Grimes, Nicolas Cage и др.) — это **отдельные играбельные персонажи со своими перками**, а не скины. Косметические образы (Costumes) в категориях не перечислены и в этот список не включены.

---

## Итог по полноте

| Категория | Число | Полнота имён | Полнота сил / перков |
|---|---:|---|---|
| Killers | 45 | **Полный** (45/45) | **Нет** |
| Survivors | 54–55 | **Полный** (55/55 страниц) | **Нет** (только подтверждено, что различаются перками) |

Списки **имён полны**. Силы убийц и персональные перки выживших **не выгружены** — это 99 отдельных наборов данных.

---

## Источники

| Источник | Страница | Тип | Дата проверки |
|---|---|---|---|
| Dead by Daylight Wiki | [Category:Killers](https://deadbydaylight.wiki.gg/wiki/Category:Killers) | **Официальная [Ф]**, oldid 107701 | 2026-11-08 |
| Dead by Daylight Wiki | [Category:Survivors](https://deadbydaylight.wiki.gg/wiki/Category:Survivors) | **Официальная [Ф]**, oldid 5614 | 2026-11-08 |
| Dead by Daylight Wiki | [Killers](https://deadbydaylight.wiki.gg/wiki/Killers) — `?action=raw` (численность) | **Официальная [Ф]** | 2026-11-08 |
| Dead by Daylight Wiki | [Survivors](https://deadbydaylight.wiki.gg/wiki/Survivors) — `?action=raw` (численность, предметы) | **Официальная [Ф]** | 2026-11-08 |
| Dead by Daylight Wiki | [Dead by Daylight](https://deadbydaylight.wiki.gg/wiki/Dead_by_Daylight) (разработчик, релиз) | **Официальная [Ф]** | 2026-11-08 |

**Не проверено:** силы всех 45 убийц; персональные перки всех 54 выживших; соответствие «настоящее имя → игровой псевдоним»; статусы отдельных персонажей (отключённые после изъятия лицензий).
