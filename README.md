<div align="center">

<h1>Kush's Keldurn Addons</h1>
<p>Addons for the Keldurn vanilla 1.12 client, including rewrites and addons that work out of the box.</p>

</div>

[Available addons](#available-addons) · [Installation](#installation-windows) · [Damage! commands](#damage-commands) · [Bartender2 commands](#bartender2-commands) · [Bagnon](#bagnon) · [More addons](#more-keldurn-addons)

---

## Available addons

This repository is home to a growing collection of addons for Keldurn. The collection currently includes **Damage!**, **Bartender2 (Rewritten)**, and **Bagnon**.

| Addon | What it does | Commands |
| --- | --- | --- |
| **Damage!** | Tracks damage and DPS, with spell breakdowns, pet attribution, recent fights, and session totals. | `/damage` or `/dam` |
| **Bartender2 (Rewritten)** | Move and arrange your hotbars, lock their positions, and bind keys by hovering over buttons. Rewritten for Keldurn. | `/bar` or `/bartender` |
| **Bagnon** | Combines all your bags into one window. Works out of the box in Keldurn; no rewrite required. | Open your bags normally |

## Installation (Windows)

Download the ZIP for each addon you want from this repository, then follow these steps:

1. Press **Win + R** to open **Run**, paste the following path, and press **Enter**:

   ```text
   %LOCALAPPDATA%\Keldurn\settings\AddOns
   ```

2. **Unzip your chosen addons into that folder.** Each addon should have its own folder directly inside `AddOns`.

3. **Launch Keldurn** and open **AddOns** on the character selection screen. Make sure your installed addons are enabled before entering the world.

You can also install from the character selection screen: open **AddOns**, click **Install ZIP**, and select the downloaded addon archive. Then enable the addon.

> **Folder tip:** The addon's `.toc` file should be directly inside its addon folder. For Damage!, the path ends in `AddOns\KeldurnMeter\KeldurnMeter.toc`. For Bartender2, it ends in `AddOns\Bartender2\Bartender2.toc`. Keep the included folder name when extracting.

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

## Bagnon

Combines all your bags into a single window, making your inventory easier to browse.

**Works out of the box in Keldurn.** Bagnon is included without a rewrite or compatibility changes. Install it using the steps above, enable it, and open your bags normally.

## More Keldurn addons

For more addons, I recommend **[ne0x86/keldurn-addons](https://github.com/ne0x86/keldurn-addons)**. ne0x86 has already rewritten and shared additional addons for Keldurn, so check out their collection too.

## Feedback and addon requests

Found a bug or have an addon you'd like to see adapted? Open an issue in this repository with the addon name and a description of the problem or request.

For bug reports, include your addon version, steps to reproduce the issue, and any Lua error message. For Damage!, include the output of `/dam diag` when possible. For Bartender2, include `/bar diag` output and a screenshot if the bars are misplaced.
