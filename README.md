# Sky Rings Phú Yên – Fire TV Edition

Sky Rings Phú Yên – Fire TV Edition is a television-focused version of the Sky Rings Phú Yên flying game, adapted for remote-control gameplay and a 10-foot TV experience.

Players fly through rings, build their score, and explore scenery inspired by Phú Yên, Vietnam. The Fire TV Edition adds remote-friendly controls, television navigation, and dedicated pause/resume behavior.

## Hackathon Track

**Primary Track:** Fire TV

This project is being submitted to the Build, Ship, Shape: Amazon Developer Hackathon.

## What Was Added During the Hackathon

Sky Rings Phú Yên existed before the hackathon. During the hackathon period, I significantly updated it for television use by adding:

- D-pad navigation for TV remotes
- Center/OK button confirmation
- Back-button pause and resume behavior
- Pause-menu navigation designed for a TV remote
- TV-focused on-screen control instructions
- Landscape 16:9 television presentation
- Music pause/resume synchronized with game pause
- Android/Fire TV compatibility work
- Native Android Back-key handling through Cordova/Android Studio
- A signed release APK for TV distribution

The Back-button implementation required additional native Android handling so remote Back events could be reliably delivered to the Construct game logic.

## Controls

- **D-pad:** Navigate/select movement options
- **Center / OK:** Confirm selections
- **Back:** Pause gameplay
- **Back while paused:** Resume gameplay

## Technology

The project uses:

- Construct 3
- HTML5 / JavaScript game runtime
- Apache Cordova Android export
- Java
- Android Studio
- Android/Fire OS-compatible APK packaging

## Project Structure

The repository contains:

- Construct 3 project source
- Android Studio / Cordova project
- Game assets required to build and run the project
- Fire TV-specific Android changes
- Setup and testing instructions

## Build Instructions

### Requirements

- Construct 3
- Android Studio
- Android SDK
- Java/Gradle dependencies supplied by the Android project

### Construct 3

1. Open the included Construct 3 project.
2. Export using the Android/Cordova Android Studio project option.
3. Use landscape orientation and television-compatible settings.

### Android Studio

1. Open the exported Android Studio project.
2. Ensure the local Android SDK is configured.
3. In `AndroidManifest.xml`, the application uses the required Back-button compatibility configuration.
4. `MainActivity.java` contains the native Back-key bridge used by the TV version.
5. Build or generate a signed APK from Android Studio.

## Testing

The release build should be tested for:

- Game launch
- D-pad input
- Center/OK confirmation
- Gameplay
- Back-button pause
- Back-button resume
- Music pause/resume
- Game Over
- Restart

For the hackathon demonstration, the project should be shown on an actual Fire TV device or the official Fire TV/Vega simulation environment.

## Security

The repository intentionally does **not** contain:

- Signing keystore files (`.jks`)
- Keystore passwords
- Key passwords
- `local.properties`
- Private credentials

## Distribution

The Android package identifier for the TV version is:

`com.tnkgames.skyringsphuyen.firetv`

The same package identifier and signing identity should be retained for future releases.

## Author

TNK Games

## License

Add an appropriate open-source license here if this repository is submitted publicly.

If the repository is kept private for the hackathon, provide reviewer access according to the competition submission requirements instead.
