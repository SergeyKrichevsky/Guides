# Отчёт об установленной конфигурации BG3

Основная установка и тест: **2 августа 2026 года**.

Консоль Script Extender включена: **3 августа 2026 года**.

Игра: **Baldur's Gate 3, GOG, Patch 8 / Hotfix #36, `4.1.1.7209685`**.

Это отчёт о фактическом состоянии конкретной установки. Инструкция по воспроизведению конфигурации находится в [руководстве по модам для 144-го уровня](level-144-mod-installation.md).

## Итог

Целевая конфигурация предназначена для новой кампании. Активны два `.pak`:

```text
1. Level 144 - No XP Modifier Required 1.3.1
2. Choose Your Stats 2.53
```

Дополнительно установлен BG3 Script Extender v32. Старый Level 144, старый XP modifier, старый Choose Your Stats и ModFixer выведены из активной папки и сохранены в архиве.

## Пути этой установки

| Назначение | Путь |
|---|---|
| Корень игры | `C:\GOG Games\Baldurs Gate 3` |
| DX11 | `C:\GOG Games\Baldurs Gate 3\bin\bg3_dx11.exe` |
| Активные `.pak` | `C:\Users\User\AppData\Local\Larian Studios\Baldur's Gate 3\Mods` |
| Порядок загрузки | `C:\Users\User\AppData\Local\Larian Studios\Baldur's Gate 3\PlayerProfiles\Public\modsettings.lsx` |
| Сохранения | `C:\Users\User\AppData\Local\Larian Studios\Baldur's Gate 3\PlayerProfiles\Public\Savegames\Story` |
| Кэш BG3SE | `C:\Users\User\AppData\Local\BG3ScriptExtender` |
| BG3MM | `C:\GOG Games\BG3 Mod Manager` |
| Архив старых модов | `C:\GOG Games\BG3 Modding Staging 2026-08-02\Disabled Legacy` |
| Проверенные загрузки | `C:\GOG Games\BG3 Modding Staging 2026-08-02\Verified Downloads` |

## Проверенная резервная копия

```text
C:\GOG Games\Baldurs Gate 3 - Modding Backup 2026-08-02 (2)
```

- 183 файла;
- 775 313 963 байта;
- сверены размеры и SHA-256 последних сейвов, профилей, `.pak` и `modsettings.lsx`.

Неполная первая попытка осталась в `C:\GOG Games\Baldurs Gate 3 - Modding Backup 2026-08-02`; её не считать основной копией.

## BG3 Mod Manager

- Версия: `1.0.12.9`.
- Официальный релиз: <https://github.com/LaughingLeader/BG3ModManager/releases/tag/1.0.12.9>.
- ZIP SHA-256: `D28670A6B4ABEE65C0818C67A90540DF141971193EAFF53D47A8AF2743DD22D3`.
- `BG3ModManager.exe` SHA-256: `13F44D647D781580992BDCAC8B792AE7DAB2898B4CCC85CBB0D9939B4B073294`.
- Именованный активный порядок: `C:\GOG Games\BG3 Mod Manager\Orders\BG3MM-Patch8-NewGame-Level144.json`.

Во время контрольного запуска процесс BG3MM стартовал, но видимого окна не показал. Он был закрыт; игровые файлы и активный порядок не изменились. Текущая игра не зависит от работающего BG3MM.

## BG3 Script Extender

- Updater/runtime: v32 / `32.0.0.0`.
- Официальный релиз: <https://github.com/Norbyte/bg3se/releases/tag/v32>.
- Загрузчик: `C:\GOG Games\Baldurs Gate 3\bin\DWrite.dll`.
- `DWrite.dll` SHA-256: `8F3C0782461CC280CAB4ADFC270979549211F6CAC91AD851BAA2B2716118ECB0`.
- Официальный ZIP SHA-256: `2B451D044FEB9D50BC0CED4A64ABF9C076D613436644945BDB2FBA31DC9AC25A`.
- Runtime-пакет SHA-256: `F1FC36CA3143B2591F2DF1F565F525CB76A561E0D3D916D2F007592BF9FDE461`.

Консоль включена в `C:\GOG Games\Baldurs Gate 3\bin\ScriptExtenderSettings.json`:

```json
{
  "CreateConsole": true,
  "LogRuntime": true,
  "LogDirectory": "C:\\Users\\User\\AppData\\Local\\Larian Studios\\Baldur's Gate 3\\Script Extender Logs"
}
```

SHA-256 текущего файла настроек: `DB51FBD49739EBB96ED61CE2777CB8318EA80DAE557C5967BE2016FDB6E543FF`.

После сетевого тайм-аута проверки манифеста создан `ScriptExtenderUpdaterConfig.json` с `DisableUpdates=true`. Локальный v32 при этом загружается. После обновления игры нужно временно вернуть автообновление BG3SE и повторить тест.

## Level 144

- Nexus: <https://www.nexusmods.com/baldursgate3/mods/7101>.
- Установленный файл: `Level 144 - No XP Modifier Required.pak`.
- Версия конкретного файла: `1.3.1`.
- File ID: `90427`.
- Дата файла: 24 апреля 2025 года.
- UUID: `e8dfe4da-8ce7-47d0-9923-2caae5a7a519`.
- Version64: `36451011631513600`.
- `.pak` SHA-256: `675CE1DD685384F624AAF18A2324561A6A1262E7050540DF05362605D93E1309`.
- ZIP SHA-256: `CF23408DEA340FB5B8A82AAD894B1399F1FCE5A936A18DB051FB0FBE9B696257`.

Это standalone-вариант, а не старый `Level 144.pak` и не вариант с фиксированными 250 XP на каждый уровень.

Фактический `XPData.txt`:

```text
Level1 = 10
каждый следующий уровень = предыдущее значение + 15
Level17 = 250
Level100 = 1495
Level143 = 2140
MaxXPLevel = 144
```

Сумма переходов от первого до 144-го уровня: **153 725 XP**.

## Choose Your Stats

- Nexus: <https://www.nexusmods.com/baldursgate3/mods/206>.
- Версия: `2.53`.
- Дата файла: 27 июня 2026 года.
- UUID: `a88d400b-febb-4662-abdd-5d0b5d6e57cc`.
- Version64: `72057707854561280`.
- `.pak` SHA-256: `F1E0A5D9F8B135577ECC8D97AC49B0427C7740D9A5B684DE3E60EF9BF7BE5CA9`.
- ZIP SHA-256: `7A98FCE2AE4DAF78E5581847D0931480D9F182AD156FE420B7FD8F5D00E74CBB`.
- Конфигурация внутри пакета: Script Extender API 9, feature Lua.

Зелье и меню Choose Your Stats подтверждены пользователем в новой игре.

HP меняется постоянными аддитивными статусами `IncreaseMaxHP(±5)`. Класс, уровень и Constitution продолжают рассчитываться отдельно. После применения мод рекомендуется оставить включённым; `End` закрывает меню, а `Remove All` снимает эффекты.

## Активный порядок

```text
cb555efe-2d9e-131f-8195-a89329d218ea  GustavX
e8dfe4da-8ce7-47d0-9923-2caae5a7a519  Level 144 - No XP Modifier Required
a88d400b-febb-4662-abdd-5d0b5d6e57cc  chooseyourstats
```

SHA-256 активного `modsettings.lsx`: `EE368AFA00E5592CF6AEE4930E4A951DD28057B2F6A6D38D810F926748366D80`.

## Отключённые старые файлы

Архив: `C:\GOG Games\BG3 Modding Staging 2026-08-02\Disabled Legacy`.

- `Level 144 v1.1.pak`, UUID `2b1867dc-8254-4316-82b3-e604137926ab`;
- `XP modifier instant max level v1.0.pak`, UUID `97b141ba-7b8e-4eaa-bb58-9c086faa9b8d`;
- `chooseyourstats v1.76.pak`;
- `ModFixer.pak`;
- прежний `vortex.deployment.json`.

Старый и новый Level 144 нельзя активировать одновременно. Старый XP modifier и ModFixer текущей Patch-8-сборке не нужны.

## Проведённые проверки

1. Старая кампания загрузилась с legacy-порядком.
2. Старый главный герой: уровень 144, XP 1 450 000, HP 149/149, временные HP 15/15.
3. Характеристики героя: STR/DEX/CON/INT/WIS 20, CHA 21.
4. В сейве найдено 266 эффектов CYS `−5 Max HP`, суммарно `−1330`; без них расчётный максимум был бы около 1479.
5. Оригинальный QuickSave_600 не менялся; SHA-256 `1884AE819C2315A7DDBA4DDEF8B2348F4BF3C72BD840F1AF1F76498D4DEFA873`.
6. Чистая Patch-8-конфигурация дошла до редактора новой кампании.
7. Главное меню показало `Script Extender v32 loaded`.
8. Игра не сбросила `modsettings.lsx`.
9. Пользователь подтвердил появление зелья и действий Choose Your Stats.

Полный новый проход от уровня 1 до 144 ещё не выполнялся; это остаётся обязательным тестом перед долгой основной кампанией.

## Команда опыта

В серверном контексте консоли BG3SE после загрузки управляемого героя:

```lua
AddExplorationExperience(GetHostCharacter(), 10000)
```

Для свежего персонажа с нулевым XP сумма всей установленной таблицы:

```lua
AddExplorationExperience(GetHostCharacter(), 153725)
```

На практике безопаснее выдавать по 5 000–10 000 XP и сохраняться между блоками повышений.

## Известные замечания

- Консоль появляется отдельным окном при каждом запуске; это ожидаемо.
- Не отключать Choose Your Stats после применения постоянных эффектов.
- Не нажимать `Remove All` без резервного сейва.
- Не возвращать старые Level 144, XP modifier или ModFixer в активный порядок.
- После обновления BG3 повторно проверить BG3SE, оба `.pak` и `modsettings.lsx`.
- Текущая целевая конфигурация рассчитана на новую игру; legacy-файлы сохранены только для возврата.
