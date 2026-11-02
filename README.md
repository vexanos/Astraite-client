# Astraite

A client-side **Fabric** mod for **Minecraft 1.21.1** with a Meteor-style click GUI, base/ore finders, an entity ESP and a set of combat and utility modules.

> Client-only. Nothing needs to be installed on the server.

## Requirements

- Minecraft **1.21.1**
- Fabric Loader **0.16.0** or newer
- Fabric API
- Java **21**

## Installation

1. Install Fabric Loader for Minecraft 1.21.1.
2. Put **Fabric API** and the Astraite `.jar` into your `mods` folder.
3. Launch the game.

## Usage

Press **Right Shift** to open the click GUI (the key can be changed in *Options > Controls*). There is also an **Astraite** button on the title screen.

| Action | Result |
| --- | --- |
| Left click a module | Toggle it on or off |
| Right click a module | Open its settings popup |
| Mouse wheel (in a popup) | Scroll the settings |
| Black arrow / `Esc` / click outside | Close the popup |

Settings are saved automatically to `config/chesthl.json`.

## Modules

### Combat
- **Kill Aura**: Meteor-style options: weapon, rotate mode, auto switch, only on click / look, priority, max targets, range and walls range, mob age filter, ignore named / passive / tamed, pause on lag / use / Crystal Aura, TPS sync, custom hit delay, switch delay and shield mode. Includes a scrollable, searchable **entity list** to choose exactly which entity types to attack.
- **Crystal Aura**: automatic end crystal placing and breaking.
- **Auto Anchor**: respawn anchor automation.
- **Auto Totem**, **Auto Armor**, **Auto Eat** (under *Player*): inventory and survival helpers.

### Render
- **ESP**: entity ESP in Meteor style.
  - Modes: **Box**, **2D**, **Glow**
  - Shape mode (lines / sides / both), fill opacity, fade distance
  - Ignore self, highlight target, distance colors
  - Scrollable entity selector and separate colors for players, animals, water animals, monsters, ambient mobs and misc entities
- **Base ESP**: highlights player-made block types such as chests, furnaces, barrels and shulker boxes.
- **Ore ESP**: highlights ores near you.
- **Fullbright**, **Free Look**, **Freecam**.

### Misc
- **Accounts**: account switcher.
- **HUD Status**: small on-screen status lines for Crystal Aura and Auto Anchor.

## Building from source

```bash
gradle build
```

The jar is written to `build/libs/`. The included GitHub Actions workflow (`.github/workflows/build.yml`) builds the mod on every push and uploads the jar as an artifact.

## Disclaimer

This mod contains combat automation and ESP features. Using them on multiplayer servers can violate server rules and may get you banned. Only use these features where they are allowed, for example in singleplayer, on your own server or on servers that explicitly permit them. You are responsible for how you use this mod.

Astraite is an independent project. It is **not** affiliated with Mojang, Microsoft or the Meteor Client developers. Module names and option layouts are inspired by Meteor Client.

## License

MIT
