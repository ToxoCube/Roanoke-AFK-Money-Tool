# Toxicity

Desktop toolkit for Roblox automation. It drives the OS mouse and keyboard like a human would, nothing is injected into Roblox!

## Features

| Tab | Description |
|-----|-------------|
| **Macro** | Auto-redeems a list of codes: click input box → type/paste code (with optional extra spaces) → redeem → repeat with looping and growing spaces. |
| **Anti-AFK** | Periodic keep-alive actions (jump, key press, etc.) so Roblox won't idle-kick you. Pauses automatically while the macro is running. |
| **Crosshair** | Transparent, click-through, always-on-top aim reference overlay. Draws a static crosshair only  it does not read the game or move the mouse. |

## INSTALL
Install Toxicity.exe PC and double-click to run.

- Works from a USB drive or any folder

**Limitations:**
- Windows only (built for x64)
- First launch may be slightly slow (PyInstaller extracts to a temp folder)
- Some antivirus tools flag PyInstaller exes; allowlist if needed
- Run **as Administrator** if OS-level clicks don't register on top of Roblox


> **Tip:** Run the terminal or exe as **Administrator** so mouse/keyboard automation works reliably on top of Roblox.

## Usage  Macro tab

1. Open your Roblox game and go to the codes screen.
2. Paste your codes in the text box  **one per line**.
3. Click **Set Input Box**, then hover over the in-game code box. A 3-second countdown captures that position.
4. Click **Set Redeem Button**, then hover over the in-game Redeem button. (Or enable **Press Enter instead of clicking Redeem** if the game submits on Enter.)
5. Choose where to add the extra space: **Before / After / Both**.
6. Adjust delay, type speed, loop options, and input method (type vs paste) as needed.
7. Click **START**. You get a 3-second countdown  click back into the Roblox window during it.
8. Click **STOP** anytime to abort. Move the mouse to the **top-left corner** of the screen for PyAutoGUI's emergency failsafe stop.

## Usage  Anti-AFK tab

1. Enable the toggle.
2. Set the interval (seconds between actions).
3. Pick an action (jump, key press, etc.) and configure the key if needed.

The keep-alive loop runs in the background and pauses while the Macro tab is actively running.

## Usage  Crosshair tab

1. Toggle visibility with the on-screen button (or configure shape, size, gap, color, opacity).
2. The overlay is click-through and always on top  use it as a visual aim reference only.

## Hotkeys

Button labels reference F6 / F7 / F8, but **global hotkeys are currently disabled** on Python 3.13. The `keyboard` library's low-level Windows hook can corrupt the process heap and crash the app. Use the on-screen buttons instead.


## Notes

- Keep the Roblox window in the foreground while automation runs.
- If clicks land in the wrong spot, re-capture positions (the game window must stay in the same place and size).
- Panels that fail to import (missing module or dependency) are skipped with a warning  the rest of the app still loads.
