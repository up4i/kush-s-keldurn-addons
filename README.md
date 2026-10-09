<div align="center">

<h1>Kush's Keldurn Addons</h1>
<p>Addons rewritten and adapted for the Keldurn vanilla 1.12 client.</p>

</div>

[Available addons](#available-addons) · [Installation](#installation-windows) · [Damage! commands](#damage-commands) · [More addons](#more-keldurn-addons)

---

## Available addons

This repository is home to a growing collection of addons for Keldurn. Our first addon is **Damage!**.

| Addon | What it does | Commands |
| --- | --- | --- |
| **Damage!** | Tracks damage and DPS, with spell breakdowns, pet attribution, recent fights, and session totals. | `/damage` or `/dam` |

## Installation (Windows)

Download the ZIP for each addon you want from this repository, then follow these steps:

1. Press **Win + R** to open **Run**, paste the following path, and press **Enter**:

   ```text
   %LOCALAPPDATA%\Keldurn\settings\AddOns
   ```

2. **Unzip your chosen addons into that folder.** Each addon should have its own folder directly inside `AddOns`.

3. **Launch Keldurn** and open **AddOns** on the character selection screen. Make sure your installed addons are enabled before entering the world.

You can also install from the character selection screen: open **AddOns**, click **Install ZIP**, and select the downloaded addon archive. Then enable the addon.

> **Folder tip:** The addon's `.toc` file should be directly inside its addon folder. For Damage!, the path ends in `AddOns\KeldurnMeter\KeldurnMeter.toc`. Keep the included folder name when extracting.

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

## More Keldurn addons

For more addons, I recommend **[ne0x86/keldurn-addons](https://github.com/ne0x86/keldurn-addons)**. ne0x86 has already rewritten and shared additional addons for Keldurn, so check out their collection too.

## Feedback and addon requests

Found a bug or have an addon you'd like to see adapted? Open an issue in this repository with the addon name and a description of the problem or request.

For bug reports, include your addon version, steps to reproduce the issue, and any Lua error message. For Damage!, include the output of `/dam diag` when possible.
