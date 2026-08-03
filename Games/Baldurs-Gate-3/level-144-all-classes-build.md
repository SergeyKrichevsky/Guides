# Персонаж 144-го уровня: все 12 классов и максимум проверок

Пошаговая сборка для **Baldur's Gate 3 Patch 8 / Hotfix #36**, PC, GOG, версия `4.1.1.7209685`. Цель — не просто собрать как можно больше надписей `Expertise`, а практически проходить максимум проверок: получить 12 компетентностей, владеть всеми 18 навыками, довести все шесть характеристик до 20, собрать постоянные и расходуемые бонусы к проверкам, пять постоянных владений спасбросками и максимально широкий набор разных заклинаний.

> **Статус модификации.** Сам расчёт выборов закончен, но мод уровня 144 нельзя считать гарантированно стабильным на Hotfix #36 без контрольной новой игры. У `Custom Level Cap` есть свежие сообщения о пропадающих экранах выбора при мультиклассе. Перед настоящим прохождением обязателен smoke test из раздела установки.

## Итог сборки

| Параметр | Результат |
|---|---|
| Происхождение | **Dark Urge / Тёмный Соблазн** |
| Предыстория | `Haunted One` — зафиксирована происхождением |
| Раса | Свободная, гном не требуется |
| Первый класс | **Ranger / Следопыт** |
| Уровни | Все 12 официальных классов по 12 уровней = 144 |
| Характеристики | **20 / 20 / 20 / 20 / 20 / 20** без сюжетных бонусов и экипировки |
| Навыки | Владение всеми **18 из 18** |
| Expertise | **12 из 18** на старте игры |
| Постоянные владения спасбросками | **5 из 6**: STR, DEX, CON, INT, WIS |
| Без proficiency | Только CHA; при CHA 20 и паладинской ауре итог всё равно высокий |
| Снаряжение и инструменты | Простое и воинское оружие, лёгкая/средняя/тяжёлая броня, щиты и выбранный музыкальный инструмент |
| Обычные черты | 38 экранов: 24 на характеристики и 14 на иные возможности |
| Поздние сюжетные усиления | В основной расчёт не входят |
| Экипировка | В основной расчёт не входит |

Основные подклассы:

| Класс | Подкласс | Причина выбора |
|---|---|---|
| Barbarian | **Wildheart** | Постоянное преимущество Вниманию и всем проверкам STR |
| Bard | **College of Lore** | Три владения навыками и четыре `Magical Secrets` |
| Cleric | **Knowledge Domain** | Две обязательные компетентности |
| Druid | **Circle of the Stars** | Уникальные звёздные формы и дополнительные бесплатные применения |
| Fighter | **Arcane Archer** | `Beguiling Arrow` может дать преимущество харизматическим проверкам |
| Monk | **Way of the Drunken Master** | `Drunkard's Luck` убирает помеху у проверки, атаки или спасброска |
| Paladin | **Oath of the Ancients** | `Aura of Warding` вдвое уменьшает урон заклинаний; полезные ритуал и oath spells |
| Ranger | **Gloom Stalker** | `Iron Mind`: сразу INT и WIS saving throw proficiency |
| Rogue | **Swashbuckler** | `Panache`: проверка Убеждения и преимущество харизматическим проверкам |
| Sorcerer | **Wild Magic** | `Tides of Chaos` и `Bend Luck` непосредственно усиливают проверки |
| Warlock | **The Fiend** | `Dark One's Own Luck`: `+1d10` к проверке |
| Wizard | **Transmutation School** | двойная алхимия через Medicine и свободный выбор полезного камня |

## Почему характеристики на создании выглядят низкими

### Точный point buy

Сначала выставить значения **до** свободных бонусов:

| STR | DEX | CON | INT | WIS | CHA | Стоимость |
|---:|---:|---:|---:|---:|---:|---:|
| 13 | 13 | 12 | 12 | 12 | 13 | 27/27 |

Затем назначить `+1` в DEX и `+2` в CHA. Итог на наутилоиде:

| STR | DEX | CON | INT | WIS | CHA |
|---:|---:|---:|---:|---:|---:|
| **13** | **14** | **12** | **12** | **12** | **15** |

Point buy делает значения 14 и 15 дороже: каждое следующее очко уже стоит два пункта. Поэтому обычный старт `17/16` уменьшил бы суммарное число характеристик и заставил бы потратить больше будущих черт. Равномерный старт здесь — способ одновременно получить шесть двадцаток и сохранить 14 самостоятельных черт.

### Шесть полу-черт

Их надо взять **до** доведения соответствующей характеристики до 20:

| Черта | Прирост | После всех шести |
|---|---:|---:|
| `Athlete` | STR +1 | STR 14 |
| `Heavy Armour Master` | STR +1 | STR 15 |
| `Tavern Brawler` | STR +1 | STR 16 |
| `Durable` | CON +1 | CON 13 |
| `Resilient: Constitution` | CON +1 | CON 14 |
| `Actor` | CHA +1 | CHA 16 |

После них массив равен `16 / 14 / 14 / 12 / 12 / 16`. Оставшиеся 18 `Ability Improvement` распределяются так:

| Характеристика | Число ASI | Прирост | Итог |
|---|---:|---:|---:|
| STR | 2 | +4 | 20 |
| DEX | 3 | +6 | 20 |
| CON | 3 | +6 | 20 |
| INT | 4 | +8 | 20 |
| WIS | 4 | +8 | 20 |
| CHA | 2 | +4 | 20 |

Всего: 6 полу-черт + 18 ASI = 24 окна. У всех двенадцати классов есть черты на уровнях 4, 8 и 12; Fighter получает дополнительную на 6-м, Rogue — на 10-м. Поэтому всего доступно 38 окон и остаётся ещё 14.

## Навыки и 12 Expertise

### Владение всеми 18 навыками

Схема не зависит от известного бага: в актуальном интерфейсе добавленный мультиклассом Cleric предлагает два навыка, хотя по обычным правилам мультикласса не должен давать ни одного. Для расчёта достаточно одного нового навыка; второй намеренно станет дублем.

| Источник | Выбрать |
|---|---|
| `Haunted One` | Medicine, Intimidation |
| Ranger 1 — классовые навыки | Insight, Animal Handling, Survival |
| Ranger 1 — `Bounty Hunter` | Investigation |
| Ranger 1 — `Urban Tracker` | Sleight of Hand |
| Ranger 6 — `Ranger Knight` | History и владение тяжёлой бронёй |
| Ranger 10 — `Keeper of the Veil` | Arcana; здесь допустим будущий дубль; также `Protection from Evil and Good` 1/ДО |
| Cleric 1 — мультикласс | Persuasion; если есть второй слот — Religion как будущий дубль |
| Knowledge Domain | Arcana, Religion; одновременно Expertise |
| Rogue 1 — мультикласс | Perception |
| Bard 1 — мультикласс | Acrobatics |
| College of Lore | Athletics, Stealth, Nature |
| Arcane Archer | Arcana и Nature автоматически |
| `Actor` | Deception, Performance |

Повторы Arcana и Religion намеренны: каждый источник дополнительно даёт самостоятельную способность, а `Blessings of Knowledge` умеет выдать Expertise даже без предварительного владения. Схема работает и при одном, и при двух предложенных Cleric навыках; `Skilled` не требуется. На smoke test уровня 13 обязательно проверить, что после Persuasion + Religion экран домена позволяет выбрать Arcana + Religion и в листе появились обе Expertise.

### Точное распределение Expertise

| Источник | Навыки |
|---|---|
| Knowledge Domain | Arcana, Religion |
| Rogue 1 | Perception, Investigation |
| Bard 3 | Insight, Persuasion |
| Rogue 6 | Sleight of Hand, Stealth |
| Bard 10 | Intimidation, History |
| `Actor` | Deception, Performance |

Без Expertise остаются Athletics, Acrobatics, Nature, Animal Handling, Medicine и Survival. Они всё равно имеют proficiency, характеристику 20 и `Reliable Talent`: на любой освоенной проверке Rogue 11 превращает результат d20 ниже 10 в 10. В BG3 это также убирает автоматический провал на натуральной единице для освоенного навыка.

## Спасброски: почему постоянными выбраны именно эти пять

Только самый первый класс выдаёт свои два классовых владения saving throws. Поэтому порядок принципиален:

| Источник | Владения |
|---|---|
| Первый класс Ranger | STR, DEX |
| Gloom Stalker 7 — `Iron Mind` | WIS, INT |
| `Resilient: Constitution` | CON |
| **Итого без предметов** | **STR, DEX, CON, INT, WIS** |

Это объясняет, почему первым нельзя брать Wizard, Cleric или иной класс с WIS/INT: его владение перекрылось бы с `Iron Mind`. Gloom Stalker взаимоисключается с Hunter, Beast Master и Swarmkeeper, но ни один из этих подклассов не даёт сразу два новых владения спасбросками. `Ranger Knight` не конфликтует с Gloom Stalker: это Favoured Enemy, а не подкласс.

Категории актуальной wiki содержат 158 эффектов с CON save, 153 с DEX, 149 с WIS, 84 с STR, 28 с INT и только 9 с CHA. Это не статистика реального прохождения — в категориях есть варианты одного эффекта, — но разница хорошо показывает порядок величин. Практически:

- **CON, WIS и DEX — верхний приоритет.** CON дополнительно используется каждый раз, когда урон проверяет концентрацию; WIS защищает от `Hold`, `Fear`, `Charm`, `Command` и другого отключающего контроля; DEX постоянно встречается у площадного урона и ловушек.
- **STR — средний приоритет:** толчки, сбивание, связывание и принудительное перемещение встречаются регулярно.
- **INT встречается реже, но провалы против mind flayer-эффектов часто означают Stunned или тяжёлый психический урон.** Оно достаётся вместе с WIS от `Iron Mind`, без отдельной цены.
- **CHA — наименее болезненная жертва:** среди заметных примеров остаются `Banishment`, Possession и несколько уникальных эффектов.

Поэтому `Resilient` берётся именно для CON, а не CHA. У непрофильного CHA save всё равно будет `+5` от характеристики 20 и ещё `+5` от собственной `Aura of Protection` Paladin 6, прежде чем будут учтены иные общие бонусы.

Transmutation Wizard 6 всё ещё может создать `Transmuter's Stone: Constitution`, но теперь этот вариант дублирует постоянное владение и не нужен. Камень остаётся свободен для `Speed`, Darkvision или требуемого в конкретной области сопротивления стихии. Это лучше, чем делать жизненно важный CON save зависимым от предмета в инвентаре.

Помимо пяти владений сборка получает несколько независимых страховок:

| Источник | Помощь спасброскам |
|---|---|
| `Aura of Protection` | Постоянно добавляет CHA modifier, то есть +5, ко всем шести saves героя и ближайших союзников |
| `Danger Sense` | Advantage на DEX saves против ловушек, заклинаний и поверхностей, пока герой не Blinded/Incapacitated |
| `Lucky` | Можно дать Advantage важному saving throw, 3 заряда за долгий отдых |
| `Indomitable` | Fighter 9 позволяет перебросить проваленный save |
| `Shield Master` | +2 к DEX saves при надетом щите; отдельная защитная реакция |
| `War Caster` | Advantage на CON saves для удержания концентрации |
| `Mage Slayer` | Advantage на saves против заклинаний, применённых рядом с героем |
| `Bless` или `Resistance` | +1d4 к saves; оба требуют концентрации и одновременно не работают |
| Rogue/Monk `Evasion` | Не повышает бросок, но превращает успешный DEX save в нулевой урон, а провал — в половинный |
| Паладинские ауры | Иммунитет к Frightened и половина урона от заклинаний не повышают число на кубике, но уменьшают цену провала |

Именно поэтому отсутствие CHA proficiency остаётся наиболее безопасной жертвой: даже этот единственный save получает базовые `+5 CHA +5 Aura = +10`, а общие Advantage/перебросы остаются доступны.

## Все постоянные и расходуемые усилители проверок

Обозначим показанный игрой proficiency bonus буквой `B`. Мод уровня выше 12 может изменить его нетипично, поэтому после прокачки надо смотреть фактическое значение в листе персонажа, а не подставлять предположение.

| Эффект | Что даёт | Ограничение |
|---|---|---|
| Характеристика 20 | +5 ко всем связанным проверкам | Постоянно |
| Proficiency / Expertise | `+B` / `+2B` | Все 18 / выбранные 12 навыков |
| `Reliable Talent` | d20 не ниже 10 | Только освоенные навыки |
| `Jack of All Trades` | +половина B | Только редкие ability checks без proficiency; к Initiative в BG3 не применяется |
| `Guidance` | +1d4 | Concentration |
| `Dark One's Own Luck` | +1d10 | Одна проверка за короткий отдых |
| `Bend Luck` | +1d4 | 2 Sorcery Points; заранее вручную применить к себе |
| `Tides of Chaos` | Advantage следующей проверке | Повышает риск Wild Magic Surge |
| `Lucky` | Advantage / переброс | 3 Luck Points за долгий отдых |
| `Enhance Ability` | Advantage проверкам одной характеристики | Concentration |
| `Thaumaturgy` | Advantage Intimidation и Performance | Не требует concentration |
| Wildheart: Eagle | Advantage Perception | Постоянно |
| Wildheart: Bear | Advantage всем STR checks, включая Athletics | Постоянно |
| `Pass Without Trace` | +10 Stealth | Concentration |
| `Dungeon Delver` | Advantage на Perception для скрытых объектов и на проверки/спасы ловушек | Ситуативно |
| `Panache` | Advantage CHA checks в диалоге с очарованной целью | Сначала выиграть Persuasion contest; возможна реакция NPC |
| `Beguiling Arrow` | Advantage CHA checks против очарованной цели | Вредящая атака, поэтому не обычный мирный способ |
| `Drunkard's Luck` | Убирает Disadvantage | 2 Ki, когда помеха уже есть |

Гарантированный результат освоенного навыка до временных бонусов:

- с Expertise: `10 + 5 + 2B`;
- без Expertise: `10 + 5 + B`;
- Athletics и любые иные STR checks можно бросать с постоянным Advantage от Bear Aspect.

Для единичной самой трудной проверки обычно использовать `Guidance` + `Dark One's Own Luck` + заранее вручную применённый к себе `Bend Luck` и один источник Advantage. Реакцией `Bend Luck` собственный бросок Sorcerer поддержать нельзя. Advantage не складывается само с собой. `Guidance`, `Enhance Ability`, `Friends` и `Pass Without Trace` требуют концентрацию, поэтому в одиночку одновременно работает только один из них. `Thaumaturgy` концентрации не требует и потому хорошо складывается с `Guidance` для Intimidation/Performance.

`Friends` следует применять осторожно: на Tactician/Honour после окончания эффекта NPC способен обвинить героя в чарах. `Panache` имеет похожий риск на высокой сложности. `Cosmic Omen` Circle of Stars может повышать проверки союзников, но описание не гарантирует применение к самому друиду; в соло-бонусом героя его не считать.

## Ранние внешние усиления в I акте

Они не входят в показатели «сразу после наутилоида», но удовлетворяют ограничению получить всё не позднее I акта:

| Эффект | Решение |
|---|---|
| `Forbidden Knowledge` | **Брать обязательно:** пролистать три страницы Necromancy of Thay. Постоянно даёт +1 ко всем WIS ability checks и WIS saves независимо от успеха трёх бросков при чтении |
| `Favourable Beginnings` | **Брать, если разрешены личинки:** ранняя иллитидская способность. По описанию добавляет `+B` к первой атаке или проверке против цели, но в текущей игре из ability checks фактически срабатывает только на Deception и Persuasion |
| `Auntie Ethel's Hair: Constitution` | Опциональная более сильная ветка черт: на Ranger 8 взять `Dual Wielder` вместо `Durable`, до встречи с каргой иметь CON 19, затем волосом довести CON до 20. Это освобождает одну полноценную черту, но сделка нарушит Oath of the Ancients — клятву придётся восстановить |
| `Bliss Spores` | Временные `+1d6` к атакам, ability checks и saves до следующего долгого отдыха. Получить у Sovereign Spaw и сохранить единственный эффект для заранее выбранной сложной цепочки |
| `Loviatar's Love` | Можно взять для +2 к WIS saves при 30% ОЗ или ниже; к проверкам не добавляет и навсегда теряется после смерти |
| `Paid the Price` | **Не брать:** +1 Intimidation не компенсирует постоянную Disadvantage на критически важный Perception и атаки против карг |

Базовая таблица уровней ниже остаётся самодостаточной веткой без волоса: Ranger 8 берёт `Durable`, и все шесть характеристик становятся 20 ещё до любых сюжетных наград.

## Раса

Сборка не требует конкретной расы и не использует скального гнома. Механическая рекомендация для проверок — **lightfoot halfling**: `Naturally Stealthy` даёт постоянное преимущество Stealth, а `Halfling Luck` перебрасывает единицу на атаках, проверках и спасбросках. После получения `Reliable Talent` расовый переброс уже почти не нужен для 18 освоенных навыков, но продолжает помогать атакам, спасброскам и редким необработанным d20.

Githyanki — хороший резерв для тестовой сборки: `Astral Knowledge` временно закрывает все навыки выбранной характеристики, если какой-либо экран proficiency сломался. В штатном финале со всеми 18 навыками эта способность становится избыточной. Поэтому внешность и расовый контент можно выбирать свободно.

Буквальные навыки в таблице уровней ниже рассчитаны на lightfoot halfling и любую расу без постоянного Perception/Stealth. Если раса уже даёт навык, использовать замену, чтобы интерфейс не заблокировал повтор:

| Расовая особенность | Изменить уровневый выбор |
|---|---|
| Уже есть Perception | На Rogue 1 взять Deception вместо Perception; Expertise всё равно выбрать Perception + Investigation |
| Уже есть Stealth | В College of Lore вместо Stealth взять Deception |
| Уже есть одновременно Perception и Stealth | Rogue 1: Deception; College of Lore: Athletics, Nature, Performance |
| Human с одним свободным навыком | На создании взять Nature; College of Lore: Athletics, Stealth, Deception |

`Actor` позднее всё равно превращает Deception и Performance в Expertise, поэтому эти перестановки не меняют итоговые 18 владений и 12 Expertise. Выбор божества тоже зависит от расы: Selûne — рекомендация для дополнительного контента, но у расово зафиксированного божества, например Lolth-sworn drow, надо оставить доступный вариант.

## Все 38 черт

### Точная раскладка

| Класс и уровень | Черта |
|---|---|
| Ranger 4 / 8 / 12 | `Athlete: STR` / `Durable: CON` / `Heavy Armour Master: STR` |
| Rogue 4 / 8 / 10 / 12 | `Actor: CHA` / `Resilient: Constitution` / `Lucky` / `Dungeon Delver` |
| Barbarian 4 / 8 / 12 | `Tavern Brawler: STR` / STR +2 / STR +2 |
| Bard 4 / 8 / 12 | DEX +2 / DEX +2 / DEX +2 |
| Cleric 4 / 8 / 12 | CON +2 / CON +2 / CON +2 |
| Druid 4 / 8 / 12 | INT +2 / INT +2 / INT +2 |
| Fighter 4 / 6 / 8 / 12 | INT +2 / WIS +2 / WIS +2 / WIS +2 |
| Monk 4 / 8 / 12 | WIS +2 / CHA +2 / CHA +2 |
| Paladin 4 / 8 / 12 | `War Caster` / `Mage Slayer` / `Shield Master` |
| Sorcerer 4 / 8 / 12 | `Spell Sniper: Eldritch Blast` / `Elemental Adept: Fire` / `Defensive Duellist` |
| Warlock 4 / 8 / 12 | `Charger` / `Sentinel` / `Polearm Master` |
| Wizard 4 / 8 / 12 | `Martial Adept: Rally, Riposte` / `Great Weapon Master` / `Sharpshooter` |

Первые 24 выбора математически доводят все характеристики до 20. Остальные 14 идут в порядке приоритетов:

- `Lucky` и `Dungeon Delver` непосредственно усиливают проверки и нормально складываются с `Reliable Talent`;
- `War Caster`, `Mage Slayer` и `Shield Master` усиливают важные спасброски или концентрацию;
- оставшиеся черты добавляют отдельные реакции, режимы атак, действия и манёвры; `Spell Sniper` сознательно повторяет будущий `Eldritch Blast`, потому что главная ценность черты — снижение порога критического попадания для всех атакующих заклинаний.

Шесть `Magic Initiate` сознательно исключены: объединённые книги уже закрывают все 25 названий заговоров и все доступные заклинания 1-го круга; каждая такая черта дала бы только ещё одно повторное применение за долгий отдых. `Mobile` почти полностью перекрывается `Fancy Footwork` Swashbuckler и `Land's Stride` Ranger, а `Alert` — `Feral Instinct` Barbarian и `Dread Ambusher` Gloom Stalker. `Tough` не берётся из-за отдельной цели ограничить ОЗ.

`Shield Master`, `Defensive Duellist`, `Polearm Master`, `Great Weapon Master` и `Sharpshooter` предназначены для разных комплектов оружия. Они не должны работать одновременно: цель — расширить доступные режимы персонажа, а не объявить один комплект экипировки частью основной сборки.

## Порядок всех 144 уровней

Следовать порядку буквально. Он сначала закрывает зависимости навыков и Expertise, затем проходит каждый класс цельным блоком. В колонке перечислены только экраны выбора и важные контрольные автоматические особенности; всё остальное класс выдаёт автоматически. Все необязательные `Replace Spell`, `Replace Invocation`, `Replace Arcane Shot` и `Replace Bestial Heart` пропускать, если конкретная замена явно не написана в строке.

### 1–12: Ranger

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 1 | Ranger 1 | Первый класс; Insight, Animal Handling, Survival; `Bounty Hunter`; `Urban Tracker` |
| 2 | Ranger 2 | Fighting Style `Archery`; `Hail of Thorns`, `Hunter's Mark` |
| 3 | Ranger 3 | `Gloom Stalker`; временно `Fog Cloud`; фиксированный `Disguise Self` |
| 4 | Ranger 4 | `Athlete: +1 STR` |
| 5 | Ranger 5 | Новый spell `Pass Without Trace`; заменить `Fog Cloud` → `Spike Growth`; фиксированный `Misty Step` |
| 6 | Ranger 6 | `Ranger Knight`; первая ещё не полученная от расы устойчивость `Wasteland Wanderer` — базово Fire |
| 7 | Ranger 7 | `Protection from Poison`; автоматически `Iron Mind` — INT и WIS saves |
| 8 | Ranger 8 | `Durable: +1 CON` |
| 9 | Ranger 9 | `Conjure Barrage`; фиксированный `Fear` |
| 10 | Ranger 10 | `Keeper of the Veil` + бесплатный `Protection from Evil and Good` 1/ДО; вторая отличная от первой и ещё не расовая устойчивость `Wasteland Wanderer` — базово Cold |
| 11 | Ranger 11 | `Lightning Arrow` |
| 12 | Ranger 12 | `Heavy Armour Master: +1 STR` |

### 13–17: открыть зависимости Cleric, Rogue и Bard

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 13 | Cleric 1 | Persuasion; если интерфейс даёт второй слот — Religion; божество Selûne, если доступна; `Knowledge Domain`; Expertise Arcana + Religion; cantrips из матрицы |
| 14 | Rogue 1 | Навык Perception; Expertise Perception + Investigation |
| 15 | Bard 1 | Навык Acrobatics; инструмент Lute; cantrips и четыре spells из матрицы |
| 16 | Bard 2 | `Heroism` |
| 17 | Bard 3 | `College of Lore`; Athletics, Stealth, Nature; Expertise Insight + Persuasion; `Enhance Ability`; Heroism → `Heat Metal` |

### 18–28: закончить Rogue

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 18 | Rogue 2 | — |
| 19 | Rogue 3 | `Swashbuckler` |
| 20 | Rogue 4 | `Actor: +1 CHA` |
| 21 | Rogue 5 | — |
| 22 | Rogue 6 | Expertise Sleight of Hand + Stealth |
| 23 | Rogue 7 | —; Evasion автоматически |
| 24 | Rogue 8 | `Resilient: Constitution` |
| 25 | Rogue 9 | —; `Panache` автоматически |
| 26 | Rogue 10 | `Lucky` |
| 27 | Rogue 11 | —; `Reliable Talent` автоматически |
| 28 | Rogue 12 | `Dungeon Delver` |

### 29–37: закончить Bard

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 29 | Bard 4 | DEX +2; `Dancing Lights`; `Detect Thoughts` |
| 30 | Bard 5 | `Glyph of Warding` |
| 31 | Bard 6 | `Hypnotic Pattern`; Lore Secrets `Spirit Guardians`, `Warden of Vitality` |
| 32 | Bard 7 | `Greater Invisibility` |
| 33 | Bard 8 | DEX +2; `Dimension Door` |
| 34 | Bard 9 | `Hold Monster` |
| 35 | Bard 10 | Expertise Intimidation + History; `Mage Hand`; `Freedom of Movement`; Secrets `Banishing Smite`, `Counterspell` |
| 36 | Bard 11 | `Otto's Irresistible Dance` |
| 37 | Bard 12 | DEX +2; `Enthrall` |

### 38–48: закончить Cleric

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 38 | Cleric 2 | — |
| 39 | Cleric 3 | — |
| 40 | Cleric 4 | CON +2; cantrip `Produce Flame` |
| 41 | Cleric 5 | — |
| 42 | Cleric 6 | —; domain actions `Read Thoughts` и `Speak with Animals` автоматически |
| 43 | Cleric 7 | — |
| 44 | Cleric 8 | CON +2 |
| 45 | Cleric 9 | — |
| 46 | Cleric 10 | Cantrip `Resistance`; `Divine Intervention` выдаётся автоматически, вариант пока не расходовать |
| 47 | Cleric 11 | — |
| 48 | Cleric 12 | CON +2 |

### 49–60: Barbarian

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 49 | Barbarian 1 | — |
| 50 | Barbarian 2 | — |
| 51 | Barbarian 3 | `Wildheart`; `Bear Heart` |
| 52 | Barbarian 4 | `Tavern Brawler: +1 STR` |
| 53 | Barbarian 5 | — |
| 54 | Barbarian 6 | `Aspect of the Beast: Eagle` — Advantage Perception |
| 55 | Barbarian 7 | —; `Feral Instinct` автоматически |
| 56 | Barbarian 8 | STR +2 |
| 57 | Barbarian 9 | — |
| 58 | Barbarian 10 | `Aspect of the Beast: Bear` — Advantage STR checks |
| 59 | Barbarian 11 | — |
| 60 | Barbarian 12 | STR +2 |

### 61–72: Druid

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 61 | Druid 1 | Cantrips `Shillelagh`, `Thorn Whip` |
| 62 | Druid 2 | `Circle of the Stars`; все три Starry Forms; фиксированные `Guidance`, `Guiding Bolt` и 2 заряда `Star Map: Guiding Bolt` |
| 63 | Druid 3 | — |
| 64 | Druid 4 | INT +2; cantrip `Poison Spray` |
| 65 | Druid 5 | —; `Star Map: Guiding Bolt` возрастает до 3 зарядов |
| 66 | Druid 6 | —; `Cosmic Omen` автоматически |
| 67 | Druid 7 | — |
| 68 | Druid 8 | INT +2 |
| 69 | Druid 9 | —; `Star Map: Guiding Bolt` возрастает до 4 зарядов |
| 70 | Druid 10 | Cantrip `Resistance` — вынужденный дубль |
| 71 | Druid 11 | — |
| 72 | Druid 12 | INT +2 |

### 73–84: Fighter

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 73 | Fighter 1 | Fighting Style `Two-Weapon Fighting` |
| 74 | Fighter 2 | — |
| 75 | Fighter 3 | `Arcane Archer`; Nature и Arcana; cantrip `Light`; shots `Beguiling`, `Enfeebling`, `Grasping` |
| 76 | Fighter 4 | INT +2 |
| 77 | Fighter 5 | — |
| 78 | Fighter 6 | WIS +2 |
| 79 | Fighter 7 | `Seeking Arrow`; не заменять старые shots |
| 80 | Fighter 8 | WIS +2 |
| 81 | Fighter 9 | — |
| 82 | Fighter 10 | `Banishing Arrow`; не заменять старые shots |
| 83 | Fighter 11 | — |
| 84 | Fighter 12 | WIS +2 |

### 85–96: Monk

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 85 | Monk 1 | — |
| 86 | Monk 2 | — |
| 87 | Monk 3 | `Way of the Drunken Master` |
| 88 | Monk 4 | WIS +2 |
| 89 | Monk 5 | — |
| 90 | Monk 6 | — |
| 91 | Monk 7 | —; Evasion автоматически |
| 92 | Monk 8 | CHA +2 |
| 93 | Monk 9 | — |
| 94 | Monk 10 | — |
| 95 | Monk 11 | —; поздняя особенность `Drunkard's Luck` не требует выбора |
| 96 | Monk 12 | CHA +2 |

### 97–108: Paladin

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 97 | Paladin 1 | `Oath of the Ancients` |
| 98 | Paladin 2 | Fighting Style `Defence` |
| 99 | Paladin 3 | —; oath spells автоматически |
| 100 | Paladin 4 | `War Caster` |
| 101 | Paladin 5 | — |
| 102 | Paladin 6 | —; `Aura of Protection` выдаётся автоматически, затем вручную активировать class action |
| 103 | Paladin 7 | —; `Aura of Warding` выдаётся автоматически, затем вручную активировать |
| 104 | Paladin 8 | `Mage Slayer` |
| 105 | Paladin 9 | —; oath spells автоматически |
| 106 | Paladin 10 | —; вручную активировать автоматическую `Aura of Courage` |
| 107 | Paladin 11 | — |
| 108 | Paladin 12 | `Shield Master` |

Dark Urge способен нарушить Oath of the Ancients сюжетными решениями. Чтобы не потерять oath actions, всегда подготовленные spells и ауры, избегать реплик, прямо одобряющих бессмысленное убийство; после неизбежного события Dark Urge не выбирать вариант восхищения смертью. Если клятва всё же нарушена, восстановить её у Oathbreaker Knight до дальнейшей проверки сборки.

### 109–120: Sorcerer

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 109 | Sorcerer 1 | `Wild Magic`; 4 cantrips; `Magic Missile`, `Thunderwave` |
| 110 | Sorcerer 2 | `Witch Bolt`; `Twinned Spell`, `Extended Spell` |
| 111 | Sorcerer 3 | `Scorching Ray`; `Quickened Spell` |
| 112 | Sorcerer 4 | `Spell Sniper: Eldritch Blast`; class cantrip `Shocking Grasp`; `Invisibility` |
| 113 | Sorcerer 5 | `Fireball` |
| 114 | Sorcerer 6 | `Haste`; `Bend Luck` автоматически |
| 115 | Sorcerer 7 | `Ice Storm` |
| 116 | Sorcerer 8 | `Elemental Adept: Fire`; `Wall of Fire` |
| 117 | Sorcerer 9 | `Cloudkill` |
| 118 | Sorcerer 10 | Cantrip `Booming Blade`; `Wall of Stone`; `Subtle Spell` |
| 119 | Sorcerer 11 | `Chain Lightning`; `Controlled Chaos` автоматически |
| 120 | Sorcerer 12 | `Defensive Duellist`; `Globe of Invulnerability` |

### 121–132: Warlock

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 121 | Warlock 1 | `The Fiend`; cantrips `Eldritch Blast`, `Minor Illusion`; `Armour of Agathys`, `Hex` |
| 122 | Warlock 2 | `Hellish Rebuke`; `Mask of Many Faces`, `Devil's Sight` |
| 123 | Warlock 3 | `Darkness`; `Pact of the Chain` |
| 124 | Warlock 4 | `Charger`; cantrip `True Strike`; `Cloud of Daggers` |
| 125 | Warlock 5 | `Hunger of Hadar`; `One with Shadows` |
| 126 | Warlock 6 | `Arms of Hadar`; `Dark One's Own Luck` автоматически |
| 127 | Warlock 7 | `Banishment`; `Book of Ancient Secrets` |
| 128 | Warlock 8 | `Sentinel`; `Blight` |
| 129 | Warlock 9 | `Cone of Cold`; `Whispers of the Grave` |
| 130 | Warlock 10 | Cantrip `Toll the Dead`; `Flame Strike` |
| 131 | Warlock 11 | `Vampiric Touch`; Mystic Arcanum `Create Undead` |
| 132 | Warlock 12 | `Polearm Master`; `Gaseous Form`; `Repelling Blast` |

### 133–144: Wizard

| Общий | Класс | Выбор на экране |
|---:|---:|---|
| 133 | Wizard 1 | 3 cantrips и 6 spells из матрицы ниже |
| 134 | Wizard 2 | `Transmutation School`; `Feather Fall`, `Colour Spray` |
| 135 | Wizard 3 | `Phantasmal Force`, `Shadow Blade` |
| 136 | Wizard 4 | `Martial Adept: Rally, Riposte`; cantrip `Minor Illusion`; `Knock`, `See Invisibility` |
| 137 | Wizard 5 | `Counterspell`, `Grant Flight` |
| 138 | Wizard 6 | `Lightning Bolt`, `Stinking Cloud`; после экрана создать `Transmuter's Stone: Speed` |
| 139 | Wizard 7 | `Otiluke's Resilient Sphere`, `Evard's Black Tentacles` |
| 140 | Wizard 8 | `Great Weapon Master`; `Conjure Minor Elemental`, `Phantasmal Killer` |
| 141 | Wizard 9 | `Seeming`, `Conjure Elemental` |
| 142 | Wizard 10 | Cantrip `Bursting Sinew`; `Arcane Lock`, `Web` |
| 143 | Wizard 11 | `Arcane Gate`, `Create Undead` |
| 144 | Wizard 12 | `Sharpshooter`; `Wall of Ice`, `Otiluke's Freezing Sphere` |

В конце проверить: каждый класс ровно 12, все характеристики 20, навыки 18/18, Expertise 12, saving throw proficiencies STR/DEX/CON/INT/WIS.

## Матрица магии без потерянных выборов

### Как считаются повторы

Одинаковое название у двух классов не является отдельной «сильной версией». Базовый круг и эффект совпадают; применение более высокой ячейкой — это upcast того же заклинания. Отличаться могут использованная характеристика, книга, подготовка и ресурс: обычные общие ячейки, восстанавливаемые коротким отдыхом pact slots или отдельное бесплатное применение.

Поэтому обычный дубль в двух ограниченных списках `Known Spells` убирается, если вместо него можно закрыть новое название. Повтор считается оправданным, когда он:

- всегда подготовлен и не занимает лимит;
- применяется без ячейки или восстанавливается отдельно;
- нужен, чтобы в конечной книге Wizard присутствовало заклинание без доступного свитка;
- неизбежен из-за обязательного экрана выбора.

Cleric, Druid и Paladin автоматически знают полные классовые списки доступных кругов и вне боя лишь меняют подготовку. Их пересечения ничего не отнимают. При основной характеристике 20 каждый из Cleric 12, Druid 12, Paladin 12 и Wizard 12 может держать 17 обычных подготовленных заклинаний; domain/circle/oath spells идут сверх лимита.

### Все 25 разных заговоров

Несколько классов заставят выбрать повтор, но объединение персонажа закрывает все 25 доступных названий Patch 8:

| Источник | Выбрать |
|---|---|
| Arcane Archer 3 | `Light` |
| Bard 1 / 4 / 10 | `Friends`, `Vicious Mockery` / `Dancing Lights` / `Mage Hand` |
| Cleric 1 / 4 / 10 | `Thaumaturgy`, `Sacred Flame`, `Bursting Sinew` / `Produce Flame` / `Resistance` |
| Circle of Stars Druid 1 / 2 / 4 / 10 | `Shillelagh`, `Thorn Whip` / фиксированный `Guidance` / `Poison Spray` / `Resistance` — вынужденный дубль |
| Wild Magic Sorcerer 1 / 4 / 10 | `Acid Splash`, `Bone Chill`, `Fire Bolt`, `Ray of Frost` / `Shocking Grasp` / `Booming Blade` |
| Fiend Warlock 1 / 4 / 10 | `Eldritch Blast`, `Minor Illusion` / `True Strike` / `Toll the Dead` |
| Transmutation Wizard 1 / 4 / 10 | `Blade Ward`, `Fire Bolt`, `Ray of Frost` / `Minor Illusion` / `Bursting Sinew` — повторы обязательны |

### Bard 1–12

Не выполнять необязательную замену, если она не указана в таблице.

| Уровень Bard | Новый выбор |
|---:|---|
| 1 | Cantrips: `Friends`, `Vicious Mockery`; spells: `Dissonant Whispers`, `Healing Word`, `Tasha's Hideous Laughter`, `Faerie Fire` |
| 2 | `Heroism` |
| 3 | `Enhance Ability`; заменить `Heroism` на `Heat Metal`; College of Lore |
| 4 | Cantrip `Dancing Lights`; spell `Detect Thoughts` |
| 5 | `Glyph of Warding` |
| 6 | `Hypnotic Pattern`; Lore Magical Secrets: `Spirit Guardians`, `Warden of Vitality` |
| 7 | `Greater Invisibility` |
| 8 | `Dimension Door` |
| 9 | `Hold Monster` |
| 10 | Cantrip `Mage Hand`; spell `Freedom of Movement`; Magical Secrets: `Banishing Smite`, `Counterspell` |
| 11 | `Otto's Irresistible Dance` |
| 12 | `Enthrall` |

`Banishing Smite` нужен именно через Magical Secrets: после выбора Fiend вместо Hexblade иначе это название персонажу недоступно. `Counterspell` позднее сознательно повторится в книге Wizard, потому что для него нет приобретаемого свитка.

### Ranger 1–12 — Gloom Stalker

| Уровень Ranger | Новый выбор |
|---:|---|
| 1 | Заклинаний ещё нет |
| 2 | `Hail of Thorns`, `Hunter's Mark` |
| 3 | Временно `Fog Cloud`; Gloom всегда готовит `Disguise Self` |
| 4 | — |
| 5 | Новый spell `Pass Without Trace`; заменить `Fog Cloud` на `Spike Growth`; Gloom всегда готовит `Misty Step` |
| 6 | — |
| 7 | `Protection from Poison`; автоматически `Iron Mind` |
| 8 | — |
| 9 | `Conjure Barrage`; Gloom всегда готовит `Fear` |
| 10 | `Keeper of the Veil`: отдельное бесплатное применение `Protection from Evil and Good` 1/ДО |
| 11 | `Lightning Arrow` |
| 12 | — |

Oath of the Ancients постоянно готовит `Ensnaring Strike`, поэтому пятое уникальное название Ranger не теряется.

### Sorcerer 1–12 — Wild Magic

| Уровень Sorcerer | Новый выбор |
|---:|---|
| 1 | Cantrips: `Acid Splash`, `Bone Chill`, `Fire Bolt`, `Ray of Frost`; spells: `Magic Missile`, `Thunderwave`; подкласс `Wild Magic` |
| 2 | `Witch Bolt`; Metamagic: `Twinned Spell`, `Extended Spell` |
| 3 | `Scorching Ray`; Metamagic: `Quickened Spell` |
| 4 | Cantrip `Shocking Grasp`; spell `Invisibility` |
| 5 | `Fireball` |
| 6 | `Haste`; автоматически `Bend Luck` |
| 7 | `Ice Storm` |
| 8 | `Wall of Fire` |
| 9 | `Cloudkill` |
| 10 | Cantrip `Booming Blade`; spell `Wall of Stone`; Metamagic: `Subtle Spell` |
| 11 | `Chain Lightning`; автоматически `Controlled Chaos` |
| 12 | `Globe of Invulnerability` |

### Warlock 1–12 — Fiend и Pact of the Chain

| Уровень Warlock | Новый выбор |
|---:|---|
| 1 | Cantrips `Eldritch Blast`, `Minor Illusion`; spells `Armour of Agathys`, `Hex`; patron `The Fiend` |
| 2 | `Hellish Rebuke`; invocations `Mask of Many Faces`, `Devil's Sight` |
| 3 | `Darkness`; `Pact of the Chain` — доступны Imp и Quasit |
| 4 | Cantrip `True Strike`; spell `Cloud of Daggers` |
| 5 | `Hunger of Hadar`; invocation `One with Shadows`; фамильяр получает Extra Attack |
| 6 | `Arms of Hadar`; автоматически `Dark One's Own Luck` |
| 7 | `Banishment`; invocation `Book of Ancient Secrets` — `Ray of Sickness`, `Chromatic Orb`, `Silence` по 1/ДО |
| 8 | `Blight` |
| 9 | `Cone of Cold`; invocation `Whispers of the Grave` |
| 10 | Cantrip `Toll the Dead`; spell `Flame Strike`; `Fiendish Resilience` |
| 11 | `Vampiric Touch`; Mystic Arcanum `Create Undead` 1/ДО |
| 12 | `Gaseous Form`; invocation `Repelling Blast` |

Здесь выбран Pact of the Chain: он добавляет действительно новые варианты фамильяра Imp/Quasit и на 5-м уровне их вторую атаку. Это осознанный компромисс, а не безусловное превосходство над Tome: Deepened Pact of the Tome дал бы отдельные бесплатные применения `Animate Dead`, `Haste` и `Call Lightning` по одному разу за долгий отдых, хотя сами названия уже присутствуют в других книгах. `Book of Ancient Secrets` в BG3 не требует Tome.

### Wizard 1–12 — Transmutation

Эти 28 уровневых выборов прежде всего сохраняют все десять wizard spells, для которых нельзя купить или найти обычный свиток. Остальные заклинания списка Wizard после начала игры последовательно переписывать из свитков.

| Уровень Wizard | Cantrip / два новых заклинания |
|---:|---|
| 1 | `Blade Ward`, `Fire Bolt`, `Ray of Frost`; `Enhance Leap`, `Find Familiar`, `Longstrider`, `Shield`, `Mage Armour`, `Grease` |
| 2 | `Feather Fall`, `Colour Spray`; Transmutation School |
| 3 | `Phantasmal Force`, `Shadow Blade` |
| 4 | Cantrip `Minor Illusion`; `Knock`, `See Invisibility` |
| 5 | `Counterspell`, `Grant Flight` |
| 6 | `Lightning Bolt`, `Stinking Cloud`; после повышения создать `Transmuter's Stone: Speed` |
| 7 | `Otiluke's Resilient Sphere`, `Evard's Black Tentacles` |
| 8 | `Conjure Minor Elemental`, `Phantasmal Killer` |
| 9 | `Seeming`, `Conjure Elemental` |
| 10 | Cantrip `Bursting Sinew`; `Arcane Lock`, `Web`; автоматически `Shapechanger: Blue Jay` |
| 11 | `Arcane Gate`, `Create Undead` |
| 12 | `Wall of Ice`, `Otiluke's Freezing Sphere` |

Десять названий без приобретаемого свитка: `Enhance Leap`, `Find Familiar`, `Longstrider`, `Shield`, `Phantasmal Force`, `Shadow Blade`, `Counterspell`, `Otiluke's Resilient Sphere`, `Arcane Gate`, `Create Undead`. Повторы `Counterspell` с Magical Secrets и `Otiluke's Resilient Sphere` с Knowledge Domain сознательны: иначе полной именно wizard spellbook не получится.

В Акте I уникальный `Scroll of Summon Quasit` не применять как Wild Magic Sorcerer: этот подкласс блокирует надёжную диалоговую ветку Shovel. Сразу переписать свиток в книгу Wizard; изученная версия сохраняется, пока у героя остаётся хотя бы один уровень Wizard.

### Автоматические книги Cleric, Druid и Paladin

- **Knowledge Domain** всегда готовит `Command`, `Sleep`, `Calm Emotions`, `Hold Person`, `Slow`, `Speak with Dead`, `Confusion`, `Otiluke's Resilient Sphere`, `Dominate Person`, `Telekinesis`; на 6-м также получает `Read Thoughts` и `Speak with Animals` через Channel Divinity.
- **Circle of the Stars** выдаёт `Guidance`, всегда подготовленный `Guiding Bolt`, 2/3/4 бесплатных применения через Star Map на уровнях 2/5/9, три Starry Forms и позднее `Cosmic Omen`. Форму заранее выбирать не нужно: Archer, Chalice и Dragon выдаются вместе.
- **Oath of the Ancients** всегда готовит `Speak with Animals`, `Ensnaring Strike`, `Misty Step`, `Moonbeam`, `Protection from Energy`, `Plant Growth`. На Paladin 7 `Aura of Warding` уменьшает урон от заклинаний для героя и ближайших союзников.

Circle of the Land был бы альтернативой для большего числа надписей `Always Prepared`, но большинство его названий уже находится в полных книгах Wizard/Druid. Stars сохраняет больше уникальных действий и бесплатных применений.

Выбор Wildheart вместо Wild Magic Barbarian тоже осознан. Wild Magic 6 дал бы `Bolstering Magic: Boon` — `+1d4` ко всем ability checks на 10 ходов один раз за долгий отдых. Wildheart уступает в максимальном бонусе одной заранее известной проверки, зато постоянно даёт Advantage частым пассивным Perception и всем STR checks без расхода и подготовки; для цели пройти больше проверок за всё прохождение выбран именно он.

## Установка на GOG и подъём до 144

### Что установить

Установку выполнять по отдельному [руководству для персонажа 144-го уровня](level-144-mod-installation.md). В нём зафиксированы точные версии, ссылки, настройка BG3MM (`bg3.exe` и отдельный запуск DX11), включение консоли и порядок `Level 144 v1.3.1` → `Choose Your Stats 2.53`. Фактические UUID и контрольные суммы находятся в [отчёте от 2 августа 2026 года](installed-mods-report-2026-08-02.md).

Не ставить одновременно `UnlockLevelCurve`, Dummy Levels, другой level-cap, XP table или progression patch: выбранный Level 144 уже standalone и меняет `Progressions.lsx`, `Data.txt` и `XPData.txt`.

### Сначала smoke test

У свежих сообщений на странице мода есть случаи остановки на суммарном уровне 20, старого вылета после 72 и отсутствующих заклинаний/классовых особенностей второго мультикласса. Поэтому до настоящего прохождения:

1. Экспортировать точный итоговый порядок: Level 144, затем Choose Your Stats; Script Extender загружается отдельно через `DWrite.dll`. Других модов в контрольном тесте не оставлять.
2. Создать нового Dark Urge с массивом из этого гайда.
3. На наутилоиде после получения управления сделать отдельное ручное сохранение.
4. Выдавать XP блоками из следующей таблицы и полностью завершать все повышения каждого блока.
5. После общих уровней 12, 17, 28, 48, 72, 96, 120 и 144 сохраняться в новый слот, выходить в меню и снова загружать игру.
6. Проверять не только число уровня, но появление подклассов, Expertise, cantrips, новых кругов, invocations, Arcane Shots и всех четырёх feat screens Fighter/Rogue.
7. Отключить **Karmic Dice**: у `Reliable Talent` есть известная проблема с противоборствующими диалоговыми проверками при включённых кармических кубах.

Если второй класс показывает только варианты первого уровня или пропадают обязательные экраны, этот файл мода для данной сборки не годится. Не продолжать основное сохранение. Более свежий запасной генератор того же автора — [Edit XP Configurator](https://www.nexusmods.com/baldursgate3/mods/23185); он строит собственный high-priority patch и не должен использоваться одновременно с Level 144.

### Консоль и точный опыт

У самой BG3 нет штатной пользовательской консоли. После установки Script Extender откроется отдельное консольное окно. Нажать Enter; если команда попала не в серверный контекст, ввести `server`.

Перед любым начислением сделать отдельное ручное сохранение. Документированная функция начисления:

```lua
AddExplorationExperience(GetHostCharacter(), X)
```

В установленном `XPData.txt` стоимость перехода растёт на 15 XP за уровень: `10 + 15 × (текущий уровень − 1)`. Полный путь свежего героя с уровня 1 до общего уровня 144 требует **153 725 XP**. Не выдавать всё число до smoke test. Следующие порции точны только для нового героя с **0 уже накопленного XP**; если опыт уже получен, нужно вычесть его из очередной порции.

`AddExplorationExperience` начисляет exploration XP всей партии, даже когда аргументом передан host character. Поэтому выполнять процедуру лучше на наутилоиде до присоединения спутников. Это всё равно не гарантирует, что позднее присоединённые спутники не получат catch-up XP.

Безопасные порции совпадают с таблицей сборки:

| Довести общий уровень | Добавить XP | Что закончить |
|---:|---:|---|
| 12 | 935 | Ranger 12 |
| 13 | 175 | Cleric 1 |
| 14 | 190 | Rogue 1 |
| 17 | 660 | Bard 1–3 |
| 28 | 3 575 | Rogue 2–12 |
| 37 | 4 275 | Bard 4–12 |
| 48 | 6 875 | Cleric 2–12 |
| 60 | 9 570 | Barbarian 1–12 |
| 72 | 11 730 | Druid 1–12 |
| 84 | 13 890 | Fighter 1–12 |
| 96 | 16 050 | Monk 1–12 |
| 108 | 18 210 | Paladin 1–12 |
| 120 | 20 370 | Sorcerer 1–12 |
| 132 | 22 530 | Warlock 1–12 |
| 144 | 24 690 | Wizard 1–12 |
| **Итого** | **153 725** | 143 повышения |

Пример первой порции:

```lua
AddExplorationExperience(GetHostCharacter(), 935)
```

Полную структуру текущего опыта без изменения состояния можно вывести так:

```lua
_D(Ext.Entity.Get(GetHostCharacter()).Experience)
```

Точные сведения об установленном файле, его хеше и проверенной таблице приведены в [датированном отчёте](installed-mods-report-2026-08-02.md). После замены файла мода таблицу нужно проверить заново.

## Как не получить тысячи ОЗ

### Проверенный способ: Choose Your Stats

Установленный `Choose Your Stats 2.53` изменяет максимум ОЗ постоянными плоскими шагами по 5. Это не замена формуле здоровья: уровни классов и CON продолжают рассчитывать базовую часть, а CYS добавляет отдельную поправку. Поэтому сначала нужно закончить прокачку, затем уменьшить максимум ОЗ до выбранного значения, вылечиться или сделать долгий отдых и проверить отдельное сохранение после повторной загрузки.

Проверенный старый герой 144-го уровня имеет 149/149 ОЗ: сохранённые эффекты CYS уменьшают расчётный максимум примерно с 1479 до 149. После применения нужно нажать `End`, а не `Remove All`; мод следует оставить включённым. После нового уровня, изменения CON или сброса класса базовая часть ОЗ пересчитывается, поэтому итог нужно проверить и при необходимости скорректировать снова. Полная последовательность действий и предупреждения о **Диком облике** приведены в [руководстве по установке](level-144-mod-installation.md).

## Финальный контрольный список

- [ ] Версия игры `4.1.1.7209685`, GOG, Patch 8 / Hotfix #36.
- [ ] Первый класс именно Ranger.
- [ ] Финальные классы: 12 × 12 = 144.
- [ ] STR/DEX/CON/INT/WIS/CHA = 20/20/20/20/20/20.
- [ ] Proficiency во всех 18 навыках; Expertise в 12 указанных.
- [ ] Saving throw proficiency: STR, DEX, CON, INT, WIS; CHA компенсируется CHA 20 и Aura of Protection.
- [ ] `Aura of Protection`, `Aura of Warding` и `Aura of Courage` вручную активированы после прокачки Paladin.
- [ ] `Transmuter's Stone: Speed`, а не Constitution, пока не требуется иное сопротивление.
- [ ] Karmic Dice выключены.
- [ ] Все 25 уникальных названий cantrips присутствуют; случайные Known Spell replacements не сделаны.
- [ ] После каждой контрольной загрузки классовые действия и spellbooks сохранились.
- [ ] Поправка ОЗ через Choose Your Stats проверена после сохранения и повторной загрузки.

## Источники

- [Larian: Patch 8 и двенадцать новых подклассов](https://baldursgate3.game/news/the-final-patch-new-subclasses-photo-mode-and-cross-play_138)
- [Larian: Hotfix #36 / 4.1.1.7209685](https://forums.larian.com/ubbthreads.php?Number=961054&ubb=showflat)
- [Классы, мультикласс и начальные владения](https://bg3.wiki/wiki/Classes)
- [Характеристики, навыки и Expertise](https://bg3.wiki/wiki/Abilities)
- [Черты и уровни их получения](https://bg3.wiki/wiki/Feats)
- [Список источников proficiency и Expertise](https://bg3.wiki/wiki/Proficiency)
- [Blessings of Knowledge](https://bg3.wiki/wiki/Blessings_of_Knowledge)
- [Gloom Stalker и Iron Mind](https://bg3.wiki/wiki/Gloom_Stalker)
- [Wildheart и Animal Aspects](https://bg3.wiki/wiki/Wildheart)
- [Bolstering Magic: Boon](https://bg3.wiki/wiki/Bolstering_Magic:_Boon)
- [Swashbuckler и Panache](https://bg3.wiki/wiki/Swashbuckler)
- [Jack of All Trades](https://bg3.wiki/wiki/Jack_of_All_Trades)
- [Wild Magic Sorcerer](https://bg3.wiki/wiki/Wild_Magic_(sorcerer_subclass))
- [Bend Luck](https://bg3.wiki/wiki/Bend_Luck)
- [The Fiend и Dark One's Own Luck](https://bg3.wiki/wiki/The_Fiend)
- [Transmutation School и варианты камня](https://bg3.wiki/wiki/Transmutation_School)
- [College of Lore](https://bg3.wiki/wiki/College_of_Lore)
- [Knowledge Domain](https://bg3.wiki/wiki/Knowledge_Domain)
- [Way of the Drunken Master](https://bg3.wiki/wiki/Way_of_the_Drunken_Master)
- [Circle of the Stars](https://bg3.wiki/wiki/Circle_of_the_Stars)
- [Oath of the Ancients](https://bg3.wiki/wiki/Oath_of_the_Ancients)
- [Aura of Protection](https://bg3.wiki/wiki/Aura_of_Protection) и [Danger Sense](https://bg3.wiki/wiki/Danger_Sense)
- [Warlock progression и Eldritch Invocations](https://bg3.wiki/wiki/Warlock)
- [Wizard spells без доступных свитков](https://bg3.wiki/wiki/List_of_Wizard_spells#Wizard_spells_without_scrolls)
- [Forbidden Knowledge](https://bg3.wiki/wiki/Forbidden_Knowledge), [Favourable Beginnings](https://bg3.wiki/wiki/Favourable_Beginnings), [Auntie Ethel's Hair](https://bg3.wiki/wiki/Auntie_Ethel%27s_Hair)
- [Категории STR](https://bg3.wiki/wiki/Category:Strength_saving_throws), [DEX](https://bg3.wiki/wiki/Category:Dexterity_saving_throws), [CON](https://bg3.wiki/wiki/Category:Constitution_saving_throws), [INT](https://bg3.wiki/wiki/Category:Intelligence_saving_throws), [WIS](https://bg3.wiki/wiki/Category:Wisdom_saving_throws), [CHA](https://bg3.wiki/wiki/Category:Charisma_saving_throws) saving throws
- [Custom Level Cap](https://www.nexusmods.com/baldursgate3/mods/7101) и [файлы](https://www.nexusmods.com/baldursgate3/mods/7101?tab=files)
- [BG3 Script Extender](https://github.com/Norbyte/bg3se) и [API](https://github.com/Norbyte/bg3se/blob/main/Docs/API.md)
- [Osiris API: AddExplorationExperience](https://docs.baldursgate3.game/index.php?title=AddExplorationExperience)
- [Osiris API: SetHitpoints](https://docs.baldursgate3.game/index.php?title=SetHitpoints)
