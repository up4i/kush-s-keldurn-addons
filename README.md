<div align="center">

<h1>Kush's Keldurn Addons</h1>
<p>Addons for the Keldurn vanilla 1.12 client, with addons built or rewritten for Keldurn.</p>

</div>

[Available addons](#available-addons) · [Installation](#installation-windows) · [Damage! commands](#damage-commands) · [Bartender2 commands](#bartender2-commands) · [Bagnon](#bagnon-rewritten) · [pfQuest](#pfquest-rewritten) · [Gatherer](#gatherer-rewritten) · [OmniCC](#omnicc-rewritten) · [More addons](#more-keldurn-addons)

---

## Available addons

This repository is home to a growing collection of addons for Keldurn. The collection currently includes **Damage!**, **Bartender2 (Rewritten)**, **Bagnon (Rewritten)**, **pfQuest (Rewritten)**, **Gatherer (Rewritten)**, and **OmniCC (Rewritten)**.

| Addon | What it does | Commands |
| --- | --- | --- |
| **Damage!** | Tracks damage and DPS, with spell breakdowns, pet attribution, recent fights, and session totals. | `/damage` or `/dam` |
| **Bartender2 (Rewritten)** | Move and arrange your hotbars, lock their positions, and bind keys by hovering over buttons. Rewritten for Keldurn. | `/bar` or `/bartender` |
| **Bagnon (Rewritten)** | Combines all your bags into one window, with inventory refresh fixes for Keldurn. | Open your bags normally |
| **pfQuest (Rewritten)** | Quest locations, map markers, a searchable database, and route guidance, with movement-performance optimizations for Keldurn. | `/pfquest` or `/db` |
| **Gatherer (Rewritten)** | Records gathered herbs, ore, and treasure locations and displays map markers, with a loading-error fix for Keldurn. | `/gather` or `/gatherer` |
| **OmniCC (Rewritten)** | Displays remaining cooldown time on action, pet, stance, and item buttons, with cooldown and command compatibility fixes for Keldurn. | `/omnicc`, `/omni`, or `/cc` |

## Installation (Windows)

Download the ZIP for each addon you want from this repository, then follow these steps:

1. Press **Win + R** to open **Run**, paste the following path, and press **Enter**:

   ```text
   %LOCALAPPDATA%\Keldurn\settings\AddOns
   ```

2. **Unzip your chosen addons into that folder.** Each addon should have its own folder directly inside `AddOns`.

3. **Launch Keldurn** and open **AddOns** on the character selection screen. Make sure your installed addons are enabled before entering the world.

You can also install from the character selection screen: open **AddOns**, click **Install ZIP**, and select the downloaded addon archive. Then enable the addon.

> **Folder tip:** The addon's `.toc` file should be directly inside its addon folder. For Damage!, the path ends in `AddOns\KeldurnMeter\KeldurnMeter.toc`. For Bartender2, it ends in `AddOns\Bartender2\Bartender2.toc`. For pfQuest, it ends in `AddOns\pfQuest\pfQuest.toc`. For Gatherer, it ends in `AddOns\Gatherer\Gatherer.toc`. For OmniCC, it ends in `AddOns\!OmniCC\!OmniCC.toc`. Keep the included folder name when extracting.

When updating an addon, replace its existing files and restart Keldurn. Avoid leaving a second copy of the same addon installed.

## Damage!

A damage meter inspired by Details!, built around the vanilla combat events available in Keldurn.

- **Damage and DPS rankings** for you and your group.
- **Spell breakdowns:** click a player to inspect their abilities and pet attacks.
- **Fight history:** view the ten most recent completed fights or your session's overall totals.
- **Resizable window:** drag the bottom-right corner to resize; bars and visible rows adjust automatically.
- **Hamburger menu:** access Current, Fights, Overall, Reset, and page controls from the top-right icon.
- **Saved preferences:** window position, size, visibility, and metric selection persist between sessions.

Damage! tracks combat reported by your client. It currently does not synchronize data between group members. Combat totals and fight history reset when the UI reloads or the client restarts.

### Damage! commands

Both `/damage` and `/dam` support the same subcommands.

| Command | Action |
| --- | --- |
| `/damage` or `/dam` | Show or hide the window |
| `/dam show` / `/dam hide` | Set window visibility |
| `/dam damage` / `/dam dps` | Switch the displayed metric |
| `/dam current` / `/dam last` | Show the current or most recent completed fight |
| `/dam history 3` | Show the third most recent completed fight; accepts 1–10 |
| `/dam overall` | Show session totals |
| `/dam reset` | Clear combat totals and fight history |
| `/dam position` | Restore the default window position |
| `/dam diag` | Print diagnostic information |
| `/dam help` | List available commands |

## Bartender2 (Rewritten)

Mikma's Bartender2, rewritten to work with Keldurn's vanilla 1.12 interface.

- **Custom hotbar positions:** unlock the bars, drag them into place, then lock them again.
- **Configurable layouts:** adjust action-bar rows, button spacing, and scale.
- **Hover keybinding:** enter bind mode, hover over an action, stance, or pet button, and press the desired key. Shift, Ctrl, and Alt combinations are supported.
- **Save or cancel:** press Escape or click Save to keep binding changes; Cancel restores previous bindings.
- **Saved layouts:** bar positions and existing profiles are preserved.

### Bartender2 commands

Both `/bar` and `/bartender` support the same subcommands.

| Command | Action |
| --- | --- |
| `/bar lock` | Unlock or lock bars for dragging |
| `/bar bind` | Enter hover-binding mode, or save and exit it |
| `/bar repair` | Reapply button alignment without resetting positions |
| `/bar bar1 rows 3` | Arrange the main bar into three rows of four buttons |
| `/bar bar2 scale 1.2` | Change bar 2's scale |
| `/bar bar2 padding 4` | Change bar 2's button spacing |
| `/bar diag` | Print layout and binding diagnostics |
| `/bar` | List available options |

In bind mode, **Backspace** or **Delete** clears the hovered button's bindings. Left and right click are reserved; middle click, mouse buttons 4/5, and the mouse wheel are supported. Bag and micro-menu bars can be moved but are not included in hover binding.

## Bagnon (Rewritten)

Tuller's Bagnon, rewritten to work with Keldurn's inventory updates. Combines all your bags into a single window.

- **Item refresh fixes:** clears stale icons and stack counts when moving items.
- **Live inventory checks:** catches missing or delayed bag updates while the window is open.
- **Bag layout updates:** adjusts the layout when bag capacities change.
- **Saved settings:** preserves existing preferences and cached inventory.

Install and enable **both `Bagnon` and `Bagnon_Core`**, then open your bags normally. When updating, close Keldurn and replace both folders. Keep your saved variables.

## pfQuest (Rewritten)

Based on Shagu's pfQuest, with the minimap and route update paths rewritten for Keldurn.

- **Quest markers:** find quest locations and objectives on the world map and minimap.
- **Searchable database:** look up quests, items, creatures, and objects.
- **Route guidance:** use route lines and the direction arrow to reach objectives.
- **Movement-performance optimizations:** scan nearby minimap markers, reduce repeated updates, and avoid redrawing player route lines on a closed world map.

Route previews show up to **32 stops** to limit expensive route planning. All quest markers, databases, and translations are retained.

### pfQuest commands

| Command | Action |
| --- | --- |
| `/pfquest` or `/db` | List available commands |
| `/pfquest config` | Open settings |
| `/pfquest show` | Open the database browser |
| `/pfquest perf` | Print FPS, zone marker counts, and nearby marker candidates |

## Gatherer (Rewritten)

Gatherer 2.99.1, with a small compatibility fix for Keldurn.

- **Gathering history:** records the locations of herbs, ore, and treasure you collect.
- **Map markers:** shows recorded gathering locations on the minimap and world map.
- **Loading-error fix:** removes a duplicated semicolon in the **Hide Icon** checkbox handler that prevented it from compiling.
- **Saved data:** preserves recorded nodes and existing settings.

Use `/gather` or `/gatherer` for Gatherer's commands. Install the included `Gatherer` folder using the steps above. When updating, close Keldurn and replace that folder while keeping your saved variables.

## OmniCC (Rewritten)

Tuller's Omni Cooldown Count 1.1.0, adapted for Keldurn.

- **Cooldown numbers:** displays remaining time over action, pet, stance, and item buttons.
- **Readable countdowns:** changes text size and color as cooldowns approach completion.
- **Native cooldown checks:** updates supported visible buttons even when Keldurn bypasses the old timer hook.
- **Command aliases:** use `/omnicc`, `/omni`, or `/cc` to change settings.

Install the included **`!OmniCC`** folder and keep the exclamation mark. Enable **Omni Cooldown Count** at character selection.

### OmniCC commands

All three aliases support the same subcommands. Settings use chat commands; entering `/cc` prints help.

| Command | Action |
| --- | --- |
| `/cc` | Print available commands |
| `/cc size 24` | Set text size; default is 20 |
| `/cc min 3` | Show text for cooldowns longer than three seconds; default is 3 |
| `/cc color short 1 0 0` | Set short-duration text color; also accepts `medium` or `long`, with RGB values from 0 to 1 |
| `/cc font Fonts\FRIZQT__.TTF` | Select a font |
| `/cc reset` | Restore default settings |

By default, cooldowns of three seconds or less are excluded, including ordinary global cooldowns.

## More Keldurn addons

For more addons, I recommend **[ne0x86/keldurn-addons](https://github.com/ne0x86/keldurn-addons)**. ne0x86 has already rewritten and shared additional addons for Keldurn, so check out their collection too.

## Feedback and addon requests

Found a bug or have an addon you'd like to see adapted? Open an issue in this repository with the addon name and a description of the problem or request.

For bug reports, include your addon version, steps to reproduce the issue, and any Lua error message. For Damage!, include the output of `/dam diag` when possible. For Bartender2, include `/bar diag` output and a screenshot if the bars are misplaced. For pfQuest performance issues, include `/pfquest perf` output while moving and say whether the world map, arrow, or minimap route lines are visible.
