---
title: Backlight Schedule
description:
  How the Espcontrol panel automatically adjusts screen brightness during the day and night based on sunrise and sunset.
---

# Backlight Schedule

Your panel can automatically adjust its screen brightness based on the time of day — brighter during daylight hours and dimmer at night. This is especially useful for panels in bedrooms or hallways where a bright screen at night would be distracting.

## How it works

The panel calculates sunrise and sunset times based on your timezone. During the day (between sunrise and sunset), it uses your **daytime brightness** setting. At night, it switches to your **nighttime brightness** setting. The transition happens automatically — you don't need to do anything once it's set up.

## Settings

These are configured from the **Settings** tab in the [Web UI](/web-ui), under the **Brightness** section.

- **Daytime brightness** — how bright the screen should be during the day. Range: 10%–100%, default: 100%.
- **Nighttime brightness** — how bright the screen should be at night. Range: 10%–100%, default: 75%.
- **Sunrise / Sunset** — these are shown for reference so you can see when the brightness will change. They update automatically each day.

## Screensaver and brightness

When the screensaver is active, the backlight turns off regardless of the brightness schedule. When the panel wakes up (by touch or presence sensor), it returns to the correct brightness for the current time of day.

## If sunrise and sunset aren't available

If the panel can't determine sunrise and sunset times (for example, during initial setup), it defaults to using the **daytime brightness** setting at all times.

## Related

- [Display & Screensaver](/display-screensaver) — screensaver timeout and presence sensor
- [Web UI](/web-ui) — full guide to the Settings tab
