# 2D Survivors

`2D Survivors` is a Godot 2D survival prototype developed as a university game development course project. Start from the `The Arena` main menu, move around the arena, survive enemy waves, collect experience vials, and choose upgrades as you level up.

## Game Overview

- The player starts with an automatically triggered sword ability.
- Experience vials fill the experience bar and trigger an upgrade choice when the player levels up.
- Upgrade choices include the axe ability, sword quickness, sword damage, axe damage, and movement speed.
- The axe can be unlocked as an additional periodic ability.
- Basic enemies spawn around the player. A wizard enemy is added to the spawn pool as arena difficulty increases.
- Arena difficulty increases every 5 seconds and reduces the enemy spawn interval.
- The run ends in defeat when the player's health reaches zero.
- The run reaches the victory screen after the 300-second arena timer completes.

## Godot Version

The project is configured for the Godot 4.1 feature set with the Forward Plus renderer (`project.godot`). The repository does not record the exact Godot patch version, so use a compatible Godot 4.1 installation when possible.

## Clone, Open, and Run

Clone the repository:

```bash
git clone https://github.com/xfelipealves/2dsurvivorsgame.git
cd 2dsurvivorsgame
```

Open the project in the Godot editor:

```bash
godot --editor --path .
```

Run the project from the editor, or launch it directly from the project directory:

```bash
godot --path .
```

The configured entry scene is `scenes/ui/main_menu.tscn`.

## Controls

| Action | Input |
| --- | --- |
| Move up | `W` or Up Arrow |
| Move down | `S` or Down Arrow |
| Move left | `A` or Left Arrow |
| Move right | `D` or Right Arrow |
| Select menu or upgrade card | Left mouse button |

Combat abilities activate automatically. There is no player attack button in the current input map.

## Project Structure

```text
project.godot                  Godot project settings, entry scene, renderer, and inputs
scenes/main/                   Main arena scene and defeat handling
scenes/ui/                     Main menu, HUD, upgrade cards, and end screens
scenes/game_object/            Player, enemies, camera, and experience pickups
scenes/ability/                Sword and axe abilities and controllers
scenes/manager/                Enemy spawning, arena time, experience, and upgrades
resources/upgrades/            Upgrade resource definitions
resources/theme/               Shared UI theme
resources/tileset.tres         Arena and menu tileset
assets/                        Art and audio assets
scripts/                       Shared GDScript utilities
build/                         Windows desktop export artifacts
```

## Status

This is a playable work-in-progress prototype, not a finished commercial release. The core arena loop, progression, enemy spawning, automatic abilities, upgrade selection, victory, and defeat flows are present in the repository.

## Limitations

- The `Options` button is present in the main menu, but its handler is currently a stub.
- The exact Godot patch version is not documented in the repository.
- The export configuration contains a Windows Desktop preset only; no macOS or Linux preset is recorded.
- The repository does not include an automated test suite or release/version metadata.
- No screenshots are included in this README.

## Contributing

Fork the repository, create a focused branch, and open a pull request with a clear description of the change. Keep Godot code, scenes, and assets organized under their existing directories. Please include reproduction or verification steps for gameplay changes.

## License

No `LICENSE` file or license declaration is currently included. Until the project adds one, the repository does not grant permission to reuse or redistribute its code or assets.
