---
name: tnp-devices
description: Help the user watch TnP on a TV, phone, computer or other device (Samsung, LG, Hisense, Sony/Philips, Android TV, Fire TV, Chromecast, iPhone, Windows, macOS, Linux, Steam Deck, Raspberry Pi, VR). Use when the user asks how to watch on the TV, install the app, or set up a device.
---

# Watch TnP on any device

Tools come from the `tnp` MCP server.

1. Ask which device if unclear (brand + TV or set-top box; for TVs the year matters: Samsung 2019+, LG 2020+).
2. `device_guide` with the device id (`device_guide(device="list")` shows ids). Walk the user through `steps`
   one or two at a time, give `links` and the `video` if present; use `faq` for their specific trouble.
3. Stremio login and password are personal: point to `stremio_login.url` (TnP cabinet → «Плеєр»), never ask the
   user to paste them into the chat.
4. If something did not work as the guide says, call `report_feedback(kind="playback" or "wrong_info", ...)`.

Answer in the user's language.
