# Установка модов для персонажа 144-го уровня

Пошаговая инструкция для **Baldur's Gate 3 на Windows 11, GOG, Patch 8 / Hotfix #36**, версия игры `4.1.1.7209685`.

Руководство обновлено **3 августа 2026 года** после фактической установки и smoke test. Новая кампания дошла до редактора персонажа, в меню появилась строка `Script Extender v32 loaded`, а после начала игры появилось зелье и меню Choose Your Stats. Полный проход нового персонажа от 1-го до 144-го уровня пока не выполнялся.

Фактически установленная конфигурация, версии, UUID и контрольные суммы вынесены в [отдельный отчёт](installed-mods-report-2026-08-02.md).

## Короткий ответ: что требуется

| Статус | Компонент | Проверенный вариант | Назначение |
|---|---|---|---|
| Обязательно | Игра | Patch 8 / Hotfix #36, `4.1.1.7209685` | Целевая версия сборки |
| Для BG3MM | .NET | .NET 8 Desktop Runtime x64 | Требование менеджера |
| Для BG3MM | Visual C++ | Microsoft Visual C++ Redistributable x64 | Требование менеджера |
| Рекомендуется | BG3 Mod Manager | `1.0.12.9` | Импорт `.pak` и экспорт порядка |
| Обязательно | Level 144 | `Level 144 - No XP Modifier Required` v1.3.1 | Общий предел 144 и собственная таблица XP |
| Обязательно для CYS и консоли | BG3 Script Extender | updater/runtime v32 | Lua, Choose Your Stats и консоль |
| Для ручной коррекции ОЗ | Choose Your Stats | v2.53 | Постоянная поправка Max HP и другие параметры |

`Level 144 - No XP Modifier Required` — standalone-вариант. Он уже содержит `XPData.txt`; отдельный XP Modifier ему не нужен.

## Что не нужно добавлять

| Компонент | Решение | Причина |
|---|---|---|
| Другой level-cap (`UnlockLevelCurve` и подобные) | Не ставить одновременно | Конфликт таблиц прогрессии |
| Старый `XP modifier instant max level` | Не ставить | Текущий Level 144 содержит собственную таблицу XP |
| `ModFixer.pak` / `ForceRecompile.txt` | Не ставить | Устарел после Patch 7/8 |
| Старые ImprovedUI Assets для Patch 6/7 | Не ставить | Компоненты другой версии интерфейса |
| `Community Library`, Compatibility Framework, Native Mod Loader | Не ставить без явной зависимости | Для этой сборки не нужны |
| Achievement Enabler | Не требуется | BG3SE включает достижения для модифицированной игры по умолчанию |
| Второй менеджер, управляющий теми же `.pak` | Не использовать параллельно | Может вернуть старые файлы и порядок |

`Scaling Difficulty` + MCM не рекомендуется использовать как большую плоскую отрицательную поправку ОЗ: её Player HP может затрагивать Wild Shape. Текущее решение — ручная поправка Choose Your Stats; её поведение во всех формах друида также следует отдельно проверить на тестовом сохранении.

## Где находятся нужные папки

В инструкции `<BG3_GOG>` означает корень установленной игры.

| Назначение | Путь |
|---|---|
| Корень игры | `<BG3_GOG>` |
| Game Data Path | `<BG3_GOG>\Data` |
| Vulkan executable | `<BG3_GOG>\bin\bg3.exe` |
| DirectX 11 executable | `<BG3_GOG>\bin\bg3_dx11.exe` |
| Загрузчик Script Extender | `<BG3_GOG>\bin\DWrite.dll` |
| Настройки BG3SE | `<BG3_GOG>\bin\ScriptExtenderSettings.json` |
| Пользовательские `.pak` | `%LOCALAPPDATA%\Larian Studios\Baldur's Gate 3\Mods` |
| Порядок загрузки | `%LOCALAPPDATA%\Larian Studios\Baldur's Gate 3\PlayerProfiles\Public\modsettings.lsx` |
| Сохранения | `%LOCALAPPDATA%\Larian Studios\Baldur's Gate 3\PlayerProfiles\Public\Savegames\Story` |
| Кэш runtime BG3SE | `%LOCALAPPDATA%\BG3ScriptExtender` |

Сохранения находятся в `AppData`, а не в каталоге игры. Поэтому обычная переустановка BG3 их, как правило, не удаляет.

## Шаг 1. Создать резервную копию

Закрыть игру и менеджеры. Скопировать:

1. `%LOCALAPPDATA%\Larian Studios\Baldur's Gate 3` целиком.
2. `%LOCALAPPDATA%\BG3ScriptExtender`, если BG3SE уже использовался.
3. Папку `Orders` или весь переносной каталог прежнего BG3MM.
4. Архивы точных версий используемых модов.

GOG Cloud не заменяет локальную копию `.pak`, `modsettings.lsx` и порядка загрузки.

Если нужна чистая диагностическая игра, одной Verify / Repair недостаточно: она не удаляет пользовательские `.pak` из AppData и вручную добавленный `DWrite.dll`.

## Шаг 2. Установить компоненты BG3 Mod Manager

Официальные загрузки Microsoft:

1. [.NET 8 Desktop Runtime x64](https://dotnet.microsoft.com/en-us/download/dotnet/8.0).
2. [Microsoft Visual C++ Redistributable x64](https://aka.ms/vs/17/release/vc_redist.x64.exe).

Старые инструкции про .NET Framework 4.8 относятся к прежним версиям BG3MM.

## Шаг 3. Установить BG3 Mod Manager

1. Скачать архив с [официальной страницы релизов](https://github.com/LaughingLeader/BG3ModManager/releases/latest).
2. Распаковать целиком в обычную папку с правом записи.
3. Запустить `BG3ModManager.exe`.
4. В Preferences проверить:
   - Game Data Path: `<BG3_GOG>\Data`;
   - основной Game Executable Path: `<BG3_GOG>\bin\bg3.exe`;
   - для DX11 включить соответствующий вариант запуска;
   - профиль `Public`;
   - кампания `Main`.
5. Перезапустить BG3MM и нажать Refresh.

В Patch 8 базовая кампания называется `GustavX`; BG3MM добавляет её автоматически.

BG3MM — удобный инструмент, но не runtime-зависимость. После корректной записи `modsettings.lsx` он не обязан оставаться открытым во время игры.

## Шаг 4. Установить Script Extender и включить консоль

Официальные источники:

- [Norbyte BG3 Script Extender](https://github.com/Norbyte/bg3se)
- [релиз v32](https://github.com/Norbyte/bg3se/releases/tag/v32)
- [документация консоли](https://github.com/Norbyte/bg3se/blob/main/Docs/API.md#se-console)

### Установка

1. В BG3MM выбрать **Tools → Download & Extract the Script Extender**, либо скачать официальный релиз вручную.
2. Убедиться, что `DWrite.dll` находится непосредственно в `<BG3_GOG>\bin`.
3. Запустить игру. Updater загрузит совместимый runtime в `%LOCALAPPDATA%\BG3ScriptExtender`.
4. В главном меню проверить `Script Extender v32 loaded` или более новую совместимую версию.

### Консоль

Создать рядом с `DWrite.dll` файл `ScriptExtenderSettings.json`:

```json
{
  "CreateConsole": true,
  "LogRuntime": true
}
```

Проверить, что Windows не превратила имя в `ScriptExtenderSettings.json.txt`.

Консоль — отдельное чёрное окно Windows; клавиша `~` или `F11` не требуется. После запуска игры переключаться на неё через `Alt+Tab`.

Обычно BG3SE проверяет обновления автоматически. `DisableUpdates=true` допустим как временный обход сетевого тайм-аута только при уже проверенном локальном runtime. После обновления игры автообновление нужно вернуть и повторно проверить совместимость.

## Шаг 5. Скачать точные файлы модов

### Level 144

1. Открыть [Custom Level Cap — Files](https://www.nexusmods.com/baldursgate3/mods/7101?tab=files).
2. Выбрать `Level 144 - No XP Modifier Required`:
   - версия `1.3.1`;
   - file ID `90427`;
   - дата загрузки 24 апреля 2025 года;
   - пометка Patch 8 / standalone.
3. Не брать старый `Level 144 v1.3`, варианты другого максимального уровня или второй level-cap.

Шапка страницы Nexus может показывать общий старый номер версии; ориентироваться нужно на строку конкретного файла.

### Choose Your Stats

1. Открыть [Choose Your Stats](https://www.nexusmods.com/baldursgate3/mods/206?tab=files).
2. Выбрать актуальный Patch-8-файл. В проверенной конфигурации это v2.53 от 27 июня 2026 года.
3. Мод требует Script Extender и Lua.

## Шаг 6. Импортировать `.pak` и экспортировать порядок

1. В BG3MM выбрать **File → Import Mod** для каждого архива.
2. Переместить оба мода из Inactive в Active.
3. Оставить порядок:

   ```text
   GustavX
   Level 144 - No XP Modifier Required
   chooseyourstats
   ```

4. Убедиться, что красных отсутствующих зависимостей нет.
5. Выполнить **Save Order As** и сохранить именованный JSON.
6. Выполнить **Export Order to Game**.
7. Проверить `%LOCALAPPDATA%\Larian Studios\Baldur's Gate 3\PlayerProfiles\Public\modsettings.lsx`.
8. Закрыть BG3MM и запустить игру.

`.pak` должен лежать непосредственно в корне `Mods`, а не в дополнительной подпапке. Встроенный менеджер Larian может показывать его как third-party — это описание происхождения, а не ошибка.

## Шаг 7. Smoke test до настоящего прохождения

1. Создать новую тестовую кампанию.
2. Убедиться, что отображается версия BG3SE.
3. Дойти до управления персонажем.
4. Проверить появление зелья Choose Your Stats.
5. Сделать отдельный ручной сейв до выдачи XP.
6. Выдавать опыт порциями и полностью проходить предложенные повышения.
7. Перезагружать контрольные сейвы после уровней 12, 13, 20/21, 72, 120 и 144.
8. Проверять экраны мультикласса, способности и сохранность действий после перезагрузки.

Сам Level 144 не меняется или не удаляется посреди основной кампании. Переход на другой level-cap выполнять только в новой игре или из сейва до установки.

## Шаг 8. Выдать опыт через консоль

1. Загрузить сохранение и дождаться управления персонажем.
2. Переключиться в окно BG3SE.
3. Нажать `Enter`, чтобы перейти в режим ввода.
4. Ввести `server` и нажать `Enter`.
5. Выполнить команду:

   ```lua
   AddExplorationExperience(GetHostCharacter(), 10000)
   ```

Число — количество **добавляемого** опыта, не итоговый уровень. Команда `exit` возвращает консоль в режим журнала.

Не выполнять команду в главном меню или редакторе персонажа: `GetHostCharacter()` должен указывать на существующего управляемого героя.

### Фактическая таблица XP v1.3.1

Установленный `XPData.txt` не использует фиксированные 250 XP на каждый уровень. Стоимость перехода задаётся последовательностью:

```text
XP перехода = 10 + 15 × (текущий уровень − 1)
```

Примеры:

| Текущий уровень | XP до следующего уровня |
|---:|---:|
| 1 | 10 |
| 17 | 250 |
| 100 | 1 495 |
| 131 | 1 960 |
| 143 | 2 140 |
| 144 | 2 155, но это уже установленный максимум |

Сумма переходов от уровня 1 до уровня 144 — **153 725 XP**.

Контрольные блоки для связанного билда:

| Этап | Добавить XP | Совокупно |
|---|---:|---:|
| 1 → 12 | 935 | 935 |
| 12 → 13 | 175 | 1 110 |
| 13 → 14 | 190 | 1 300 |
| 14 → 17 | 660 | 1 960 |
| 17 → 28 | 3 575 | 5 535 |
| 28 → 37 | 4 275 | 9 810 |
| 37 → 48 | 6 875 | 16 685 |
| 48 → 60 | 9 570 | 26 255 |
| 60 → 72 | 11 730 | 37 985 |
| 72 → 84 | 13 890 | 51 875 |
| 84 → 96 | 16 050 | 67 925 |
| 96 → 108 | 18 210 | 86 135 |
| 108 → 120 | 20 370 | 106 505 |
| 120 → 132 | 22 530 | 129 035 |
| 132 → 144 | 24 690 | 153 725 |

Для первого теста безопаснее выдавать по 5 000–10 000 XP и сохраняться между группами повышений. Технически свежему герою с нулевым XP можно добавить всю сумму одной командой, но это создаст очередь из 143 повышений:

```lua
AddExplorationExperience(GetHostCharacter(), 153725)
```

## Шаг 9. Использовать Choose Your Stats

Choose Your Stats — не внешний редактор сейва. Он применяет постоянные игровые статусы.

1. После начала игры найти в инвентаре `Potion of Lesser Wish (Choose Your Stats Potion)`.
2. Использовать зелье; оно не расходуется.
3. Если действия не появились на панели, нажать `K` и добавить их на hotbar.
4. Выбрать нужную категорию и изменения.
5. Завершить командой `Choose Your Stats: End`.

Если зелье не появилось, вне боя последовательно включить скрытность, `Non-Lethal Attacks` и обычный `Dash`.

`End` закрывает меню, но сохраняет выбранные эффекты. `Remove All Statuses From This Magical Potion` снимает почти все эффекты и не является обычной кнопкой выхода.

После применения эффектов CYS лучше оставить включённым: сохранение содержит статусы, определения которых находятся в `.pak`.

### Как CYS меняет HP

Действия HP используют аддитивный `IncreaseMaxHP(±5)`:

```text
Max HP = обычный расчёт от класса, уровня, Constitution и других эффектов
       + 5 × количество бонусов
       − 5 × количество снижений
```

Constitution и классовые бонусы продолжают рассчитываться отдельно. После level-up или respec базовая часть пересчитывается, а поправка CYS сохраняется.

Увеличение Max HP не обязательно лечит текущий HP; после настройки следует вылечиться или сделать долгий отдых.

На проверенном старом персонаже 144-го уровня было 266 эффектов `−5 Max HP`, всего `−1330`; это давало 149/149 HP вместо примерно 1479. Для новой игры сначала получить уровни, затем корректировать итог шагами по 5. `Remove All` и `Remove HP Reduction` не нажимать без отдельной копии.

## Диагностика

| Симптом | Что проверить |
|---|---|
| BG3MM не запускается | .NET 8 Desktop Runtime x64, VC++ x64, полностью ли распакован архив |
| Моды не видны | Правильны ли Data Path, профиль Public, кампания Main и корень папки Mods |
| Порядок сбрасывается | Дубликаты UUID, подпапки в Mods, повреждённый `.pak`, конфликт менеджеров |
| BG3SE не загружается | `DWrite.dll` должен лежать в `bin` фактически запускаемой копии |
| Консоль не появляется | `CreateConsole=true`, корректный JSON и расширение `.json` |
| Уровень останавливается | Точный ли файл v1.3.1, нет ли второго level-cap или XP-мода |
| Missing Mod при загрузке | Отменить загрузку и вернуть точную прежнюю версию и порядок |
| Красная ошибка BG3SE | Повторить запуск сначала только с BG3SE, затем добавлять `.pak` по одному |

## Обновление и откат

Перед обновлением игры или модов сохранить:

- `PlayerProfiles\Public`;
- папку `Mods`;
- именованный JSON порядка BG3MM;
- исходные ZIP точных версий;
- `DWrite.dll` и настройки BG3SE.

После обновления сначала запускать новую тестовую игру или копию сейва. Не пересохранять единственную основную кампанию до подтверждения совместимости.

Verify / Repair не удаляет автоматически пользовательские `.pak` из AppData.

## Основные источники

- [Larian: Hotfix #36](https://baldursgate3.game/news/hotfix-36-now-live_149)
- [Larian: Playing With Mods](https://baldursgate3.game/news/community-update-29-playing-with-mods_124)
- [BG3 Mod Manager](https://github.com/LaughingLeader/BG3ModManager)
- [BG3 Mod Manager releases](https://github.com/LaughingLeader/BG3ModManager/releases)
- [BG3 Script Extender](https://github.com/Norbyte/bg3se)
- [BG3SE v32](https://github.com/Norbyte/bg3se/releases/tag/v32)
- [BG3SE console](https://github.com/Norbyte/bg3se/blob/main/Docs/API.md#se-console)
- [Custom Level Cap](https://www.nexusmods.com/baldursgate3/mods/7101)
- [Choose Your Stats](https://www.nexusmods.com/baldursgate3/mods/206)
- [Choose Your Stats documentation](https://www.nexusmods.com/baldursgate3/mods/206?tab=docs)
- [.NET 8 Desktop Runtime](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- [Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)
