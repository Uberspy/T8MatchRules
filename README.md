# T8MatchRules

[Download 0.1.0 beta 1](https://github.com/Uberspy/T8MatchRules/releases/download/v0.1.0-beta.1/T8MatchRules-0.1.0-beta.1.zip)

Configure matchmaking filters to choose specific region, language, wired/Wi-Fi and connection strength to match with, and auto-accept/decline opponents.

## Install UE4SS (skip if already installed)

1. In Steam, right-click TEKKEN 8 → Manage → Browse local files, then open `Polaris/Binaries/Win64`.
2. Download [UE4SS v3.0.1](https://github.com/UE4SS-RE/RE-UE4SS/releases/tag/v3.0.1) (`UE4SS_v3.0.1.zip`) and extract it into Win64, beside `Polaris-Win64-Shipping.exe`.
3. **Only if UE4SS crashes on startup:** try setting `bUseUObjectArrayCache = false` in `UE4SS-settings.ini`, as suggested by the UE4SS release notes.

## Install T8MatchRules

1. Close the game and extract the mod ZIP.
2. Copy the included `Polaris` folder into your TEKKEN 8 game folder, merging folders.
3. Launch the game and press **F11**.

If updating, back up the old T8MatchRules folder outside Mods, install the new copy, then restore only `profile.ini` to keep your settings.

## Using the menu

- Enable any of the four filters and select the values you allow. **Ctrl+click** selects multiple values; **Select all** and **Clear** change the selection.
- All enabled filters must pass. Any selected value within a filter is allowed. Unchecked filters allow anything; an enabled empty filter allows nobody.
- **Observe** previews decisions without acting. **Automatic** accepts allowed opponents and declines others. **Off** stops automatic input.
- **Autofocus** brings Tekken forward for decisions. The menu shortcut can also be changed.
- Click **Save and close** to apply changes to the next opponent prompt. **Cancel** discards changes.
- **F12** turns automation Off while Tekken or its settings window has focus.

Fresh installs start in Observe. Automatic input uses the default **Down/J** keyboard bindings. Use windowed or borderless mode.

**Compatibility:** Windows x64, Steam build 26651490, UE4SS 3.0.1 and the Microsoft Visual C++ x64 runtime. This is a beta; other builds/loaders are not verified.

**Uninstall:** close the game and move `Mods/T8MatchRules` out of Mods.
