---
title: Install
description:
  Flash Espcontrol firmware to a Guition ESP32-P4 JC1060P470 from the browser, or install via the ESPHome package.
---

# Install

Flash Espcontrol to a Guition ESP32-P4 7" display from your browser — no desktop toolchain or ESPHome required.

## What you need

- **Guition ESP32-P4 JC1060P470** (7" display), **USB-C cable** (data-capable), **[Home Assistant](https://www.home-assistant.io/)** on your network

## Web Installer

Connect the display via USB-C, then click the button below.

<EspInstallButton />

::: info Browser
Requires **Chrome** or **Edge** (desktop) with [WebSerial](https://developer.mozilla.org/en-US/docs/Web/API/Web_Serial_API). Safari and Firefox are not supported.
:::

### Steps

1. **Connect** — Plug in with USB-C; allow drivers if prompted.
2. **Flash** — Click **Install Espcontrol**, choose the device's serial port, confirm. Takes a few minutes.
3. **WiFi** — The device creates a hotspot; connect from phone or laptop for captive-portal WiFi setup.
4. **Home Assistant** — When the device is online, Home Assistant discovers it via the ESPHome integration. Complete pairing so the API, time sync, and entity controls work.
5. **Configure** — Open the device IP in a browser (shown on screen) and configure buttons, display, screensaver, and backlight from the web UI.

## Advanced: ESPHome Package

If you prefer to compile locally with ESPHome (for customisation or development), use the package method instead.

### 1. Create the device config

Copy the template from the repo's [`esphome.yaml`](https://github.com/jtenniswood/espcontrol/blob/main/guition-esp32-p4-jc1060p470/esphome.yaml) and adjust:

- `substitutions.name` — ESPHome hostname (e.g. `my-panel`)
- `substitutions.friendly_name` — human-readable name
- `wifi` — use `!secret wifi_ssid` and `!secret wifi_password` (or inline values)

The **packages** block pulls the full firmware from GitHub:

```yaml
packages:
  setup:
    url: https://github.com/jtenniswood/espcontrol/
    file: guition-esp32-p4-jc1060p470/package.yaml
    refresh: 1sec
```

Use a short `refresh` while developing; you can increase it later.

### 2. Flash the firmware

1. Connect the panel via USB-C.
2. In the ESPHome dashboard, create or import the YAML above, then **Install** to the serial port.
3. On first boot you should see the **loading** LVGL page, then WiFi connection.

If WiFi fails, the device exposes a **fallback hotspot** and **captive portal** so you can enter credentials from a phone or laptop (see on-screen instructions).

### 3. Add to Home Assistant

When the device is online, Home Assistant should discover it via the ESPHome integration. Complete pairing so the **API**, **time sync**, and **entity controls** work.

### 4. Open the web UI

1. Note the device IP (router DHCP list, ESPHome log, or on-screen URL when no buttons are configured).
2. Browse to `http://<device-ip>/`.
3. Configure **buttons**, **appearance**, **temperatures**, **screensaver**, **backlight**, and **firmware** from the tabs.
4. Use **Apply Configuration** (restart) when you need a full config reload from persisted entities.

## Troubleshooting

- **No web UI styling** — the device loads custom JS from GitHub Pages (`js_url` in firmware). Ensure the device can reach the internet, or check [Hardware](/hardware-architecture) for the URL.
- **YAML errors after a repo update** — run **Validate** in ESPHome; breaking changes are rare but `refresh: 1sec` helps you pick up fixes quickly.

Next: [Web UI](/web-ui).
