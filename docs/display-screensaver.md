---
title: Display & Screensaver
description:
  How to configure the temperature display, screensaver timeout, and presence sensor wake on your Espcontrol panel.
---

# Display & Screensaver

These settings control what the panel shows on screen and how it behaves when you're not using it. All of these are configured from the **Settings** tab in the [Web UI](/web-ui).

## Temperature display

The top bar of your panel can show indoor and outdoor temperatures, pulled from any temperature sensor in Home Assistant.

- **Indoor temperature** — toggle it on or off, then enter the entity ID of the sensor you want to use (for example, `sensor.living_room_temperature`).
- **Outdoor temperature** — works the same way. Use a weather sensor or outdoor thermometer entity.

When both are enabled, the top bar shows two temperatures side by side. When only one is enabled, it shows a single value.

## Screensaver

To protect the display and save power, the panel activates a screensaver after a period of inactivity.

- **Timeout** — how long the panel waits with no touch before activating the screensaver. You can set this from **30 seconds to 30 minutes**, in 30-second steps. The default is **5 minutes**.

When the screensaver is active, the screen shows a gentle snow animation and the backlight turns off. Touching the screen wakes it back up immediately.

## Presence sensor wake

If you have a motion or presence sensor (such as a mmWave sensor), you can connect it so the panel wakes up when someone walks nearby — no need to touch the screen.

- **Presence sensor** — enter the entity ID of a binary sensor in Home Assistant (for example, `binary_sensor.hallway_presence`). When this sensor detects motion, the panel wakes from the screensaver automatically.

Leave this field blank if you don't have a presence sensor or prefer touch-only wake.

## Related

- [Backlight Schedule](/backlight-schedule) — automatic day and night brightness
- [Web UI](/web-ui) — full guide to the Settings tab
