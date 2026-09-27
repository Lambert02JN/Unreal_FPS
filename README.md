# Unreal_FPS

A first-person objective and extraction game prototype built with **Unreal Engine 4.21** and **C++**. The player explores the level, collects an objective, and reaches an extraction zone while avoiding a guard that reacts to sight and sound.

> **Portfolio focus:** Gameplay programming. The character models, animations, and other visual assets used in this project are third-party assets and are **not my original artwork**.

## Gameplay

- Move through a first-person environment and collect the objective by touching it.
- Avoid detection: the AI guard reacts when it sees the player and turns toward sounds it hears.
- Reach the extraction zone while carrying the objective to complete the mission. Being spotted by the guard ends the mission in failure.
- Fire a projectile, jump, and interact with a launcher pickup and environmental gameplay actors such as a launch pad and black hole.

## Controls

| Input | Action |
| --- | --- |
| `W` / `S` | Move forward / backward |
| `A` / `D` | Move left / right |
| Mouse | Look around |
| `Space` | Jump |
| Left mouse button | Fire |
| Arrow keys | Alternative movement and turning controls |

The project's input configuration also contains gamepad and motion-controller bindings. `R` is mapped to **Reset VR orientation**, rather than reload.

## Technical Work

The gameplay code in [`Source/FPS`](Source/FPS) demonstrates:

- First-person character movement, camera control, jumping, and projectile firing (`FPSCharacter`, `FPSProjectile`).
- Guard perception and state changes between idle, suspicious, and alerted (`FPSAIGuard`).
- Objective pickup, extraction overlap, and mission completion (`FPSObjectiveActor`, `FPSExtractionZone`, `FPSGameMode`).
- Interactions with a launcher pickup, launch pad, and black-hole actor (`FPSLauncher`, `FPSLaunchPad`, `FPSBlackHole`).

## My Contribution and Asset Credits

**My contribution:** C++ gameplay programming and implementation of the interactive systems represented in the project source code. This is submitted as a **technical programming piece** in my portfolio.

**Third-party materials:** The characters, animations, and other visual art assets came from asset packs. I did not create those models or animations, and they should not be assessed as my original artwork. Unreal Engine template material may also be present in the project; the portfolio emphasis is on the gameplay systems rather than ownership of template or marketplace content.


## Open the Project

1. Install **Unreal Engine 4.21** and a compatible C++ development environment.
2. Clone or download this repository.
3. Open `FPS.uproject`, generate or build the C++ project when prompted, and launch the project in Unreal Editor.
4. Open the playable level and select **Play**.

Some third-party assets may require separate access or import if they are not included in the repository. This repository does not provide a packaged game build.

## Repository Structure

| Path | Contents |
| --- | --- |
| `Source/FPS/` | C++ gameplay classes |
| `Config/DefaultInput.ini` | Keyboard, mouse, and controller input mappings |
| `Content/` | Unreal project content and assets |
| `FPS.uproject` | Unreal Engine project file |
