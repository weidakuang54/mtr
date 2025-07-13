# mtr-superbwarfare-compat-fix

## Project Goal
A compatibility patch for Minecraft Forge 1.20.1, designed to fix the camera conflict between MTR (Minecraft Transit Railway, version 4.0.0) and superbwarfare (version 8.4.0).  
When both mods are loaded, using the superbwarfare drone in self-destruct mode (yellow-named entity, with or without payload, any trigger method) causes extreme camera flicker between player and drone views.

## Functional Requirements
- Detect when the player is controlling a superbwarfare drone in self-destruct mode.
- While this state is active, temporarily suppress any MTR camera/cameraEntity control or overrides.
- Restore all MTR camera functions as normal when exiting drone control.
- Do **not** affect any other MTR or superbwarfare features, blocks, or events.

## Automation & Code Standards
- Automatically generate a standard Forge 1.20.1 project structure (build.gradle, etc.), using the best available template.
- Include detailed code comments, no known bugs, and support future mod upgrades where possible.
- Optional: support a `/mtrfix` toggle command or log output for debugging.

## Build Instructions
- Must support building with a single `./gradlew build` command to produce a JAR usable in the mods folder.

## Background
MTR is widely used for station, rail, and airport builds on the server, and superbwarfare's drone self-destruct is a core combat mechanic.  
Ensuring full compatibility between these mods is critical for gameplay.

---

**Please automatically initialize a Forge 1.20.1 project, add all required dependencies, and complete the build script and example main class.  
Prefer Mixin or event hooks for implementation.**

## Dependencies
Please note:
- The required mod jars (`MTR-forge-4.0.0-prerelease.1+1.20.1.jar` and `superbwarfare-1.20.1-0.8.4-57df9bc06.jar`) are located in the `libs/` folder of this repository.
- Please add these to the `build.gradle` dependencies as needed.

## Dependencies

- The required MTR jar (`MTR-forge-4.0.0-prerelease.1+1.20.1.jar`) is **NOT included** in this repository due to its large file size (75MB+).
- Please download MTR from the official source:
  [MTR - Minecraft Transit Railway on CurseForge](https://www.curseforge.com/minecraft/mc-mods/minecraft-transit-railway)
- After downloading, place the jar in the `libs/` folder for local building.

- The superbwarfare jar (if needed) can be included in `libs/` or downloaded similarly.

**Do not commit large mod files to this repository. Always use official downloads for dependencies over 25MB.**
