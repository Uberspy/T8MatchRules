# T8MatchRules

[Download 0.2.1 beta 1](https://github.com/Uberspy/T8MatchRules/releases/download/v0.2.1-beta.1/T8MatchRules-0.2.1-beta.1.zip)

Configure matchmaking filters to choose specific region, language, wired/Wi-Fi and connection strength to match with, and auto-accept/decline opponents.

Version 0.2.1 beta 1 adds a maximum disconnection-rate filter, named rule presets, a connection card and an optional maximum RTT filter.

## Install UE4SS (skip if already installed)

1. In Steam, right-click TEKKEN 8 → Manage → Browse local files, then open `Polaris/Binaries/Win64`.
2. Download [UE4SS v3.0.1](https://github.com/UE4SS-RE/RE-UE4SS/releases/tag/v3.0.1) (`UE4SS_v3.0.1.zip`) and extract it into Win64, beside `Polaris-Win64-Shipping.exe`.
3. **Only if UE4SS crashes on startup:** try setting `bUseUObjectArrayCache = false` in `UE4SS-settings.ini`, as suggested by the UE4SS release notes.

## Install T8MatchRules

1. Close the game and extract the mod ZIP.
2. Copy the included `Polaris` folder into your TEKKEN 8 game folder, merging folders.
3. Check that `Polaris/Binaries/Win64/Mods/T8MatchRules` contains `enabled.txt`, `Scripts/main.lua` and `dlls/main.dll`.
4. Launch the game and press **F11**.

If updating, back up the old T8MatchRules folder outside Mods, install the new copy, then restore `profile.ini` and any `preset-1.ini` through `preset-16.ini` files to keep your settings and presets. Disable other matchmaking automation mods to avoid conflicting inputs.

## Using the menu

- Enable any of the four filters and select the values you allow. **Ctrl+click** selects multiple values; **Select all** and **Clear** change the selection.
- **Maximum disconnection rate** optionally limits the game's displayed percentage, inclusively from 0 to 100%.
- **Maximum RTT (rolling mean)** optionally limits the game's mean RTT to your chosen value, inclusively from 1 to 2000 ms. The saved default is disabled with an 80 ms limit. Missing, stale, capped or unrefreshed RTT data waits for fresh samples or the normal game timeout.
- **Show connection card** displays mean RTT in the prompt and full range, spread and sample count in F11. The RTT filter works even with the card hidden.
- All enabled filters must pass. Any selected value within a filter is allowed. Unchecked filters allow anything; an enabled empty filter allows nobody.
- **Observe** previews decisions without acting. **Automatic** accepts allowed opponents and declines others. **Off** stops automatic input.
- Automation pauses once a match starts and resumes on the next search. An opponent declining does not switch it off. Your saved mode is preserved.
- **Autofocus** brings Tekken forward for decisions. The menu shortcut can also be changed.
- Click **Save and close** to apply changes to the next opponent prompt. **Cancel** discards changes.
- **F12** turns automation Off while Tekken or its settings window has focus.

Fresh installs start in Observe. Automatic input uses the default **Down/J** keyboard bindings. Use windowed or borderless mode.

## Rule presets

Choose a preset to load its rules into the menu draft, then **Save and close** to apply them to the next opponent. Enter a name and click **Save preset** to store the current draft; up to 16 named presets are supported. Saving a preset writes it immediately; Cancel leaves active rules unchanged. **Delete preset** removes the selected snapshot.

With Tekken focused and settings closed, **Ctrl+F9** cycles saved presets. Presets retain filter selections, percentage/RTT limits and card visibility, while preserving the current automation mode, autofocus and menu shortcut. Loading a preset does not undo F12.

## RTT measurement

RTT uses the game's rolling sample manager, following the [TekkenRTTDisplay](https://tekkenmods.com/mod/7344/) approach. The filter requires an observed sample-list reset and refresh in the current opponent context. It clears that evidence on source replacement or capture discontinuity, and waits when observations are stale or capped.

These checks do not independently establish the samples' account identity or network measurement timestamp. Range/spread is not statistical jitter, packet loss or remote PC performance. Check the new RTT rule in Observe before using Automatic. This remains a beta; the RTT rule's automatic behavior has not been independently live-verified.

**Compatibility:** Windows x64, Steam build 26651490, UE4SS 3.0.1 and the Microsoft Visual C++ x64 runtime. This is a beta; other builds/loaders are not verified.

**Uninstall:** close the game and move `Mods/T8MatchRules` out of Mods.
