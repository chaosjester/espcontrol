---
title: Setup
description:
  How to use the built-in web page to configure buttons, display settings, screensaver, and brightness on your Espcontrol panel.
---

# Setup

Your Espcontrol panel has a built-in web page where you can set everything up. Open it by typing the panel's address into any browser on your phone or computer.

::: tip Finding the address
The address is shown on the display screen when no buttons are configured yet. You can also find it in your router's connected devices list, or in Home Assistant under **Settings > Devices & Services > ESPHome**.
:::

### Adding and removing buttons

- **Add a button** — tap any empty space in the grid (shown as a dashed outline with a **+** icon). This opens the button settings where you can choose what it controls.
- **Remove a button** — right-click the button and choose **Delete**.

### Selecting buttons

- **Tap** a button to select it. Its settings appear below the preview.
- **Shift+click** to select a range of buttons at once.
- **Ctrl+click** (or Cmd+click on Mac) to pick and choose individual buttons.

When you've selected more than one button, right-click to cut or delete them all at once.

### Moving buttons

Drag and drop any button to move it to a new position. If you drop it onto a space that's already taken, the existing button shifts to the next available space.

### Right-click menu

Right-click a button to see these options:

| Option | What it does |
| --- | --- |
| **Edit Subpage** | Opens the subpage editor (only appears on Subpage buttons) |
| **Double Height** / **Single Height** | Makes the button tall (spans two rows) or reverts to normal |
| **Duplicate** | Creates a copy of the button in the next available space |
| **Cut** | Removes the button and saves it so you can paste it elsewhere |
| **Delete** | Removes the button permanently |

Right-click an **empty space** to see a **Paste** option if you've previously cut a button.

### Cut and paste

You can move buttons around by cutting and pasting. Right-click a button, choose **Cut**, then right-click an empty space and choose **Paste**. This also works between the home screen and subpages — you can cut a button from one and paste it into the other.

### Button settings

When you tap a button to select it, a settings panel appears below the preview where you can choose its type, icon, label, and which device it controls. See [Buttons & Icons](/features/buttons-and-icons) for a full guide to button types, icons, subpages, and sensor readouts.

## Settings tab

See [Settings](/features/settings) for appearance, brightness, temperature, screensaver, backup, and firmware options.

## Logs tab

A live feed of what the panel is doing. This is mainly useful if something isn't working — the logs may explain why. Messages are colour-coded: red for errors, yellow for warnings, green for normal activity. Press **Clear** to empty the log.

## Apply Configuration

After making changes, tap **Apply Configuration** at the bottom of the page. The panel restarts and loads your new settings — you'll see a message while it reconnects.