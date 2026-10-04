# Sky Rings Phú Yên - Fire TV Edition

This is the dedicated Fire TV competition edition of Sky Rings Phú Yên.

## Remote controls

- D-pad Up / Down / Left / Right: move menu focus
- D-pad Center (Enter): confirm selected menu item
- During flight: D-pad Center or Up = flap / fly upward
- Back: pause during gameplay; resume from pause
- Space: desktop-preview equivalent of Center
- Escape / Backspace: desktop-preview equivalents of Back

## Fire TV changes in this project

- Dedicated package ID: `com.tnkgames.skyringsphuyen.firetv`
- Added Construct Keyboard input object
- Remote-first menu navigation and focus feedback
- Remote controls for play, pause/resume, restart, sound, game-over restart, and next-level flow
- Fire TV instructions in the start and pause UI
- AdMob requests disabled for the competition build; rewarded/interstitial/banner gameplay flows do not run
- Rewarded continue disabled (`MaxContinues = 0`)
- Game-over restart button centered for TV
- Landscape 1920x1080 presentation retained

## Android Studio export step

After exporting this project from Construct 3 as an Android Studio project, add the manifest feature in `AndroidManifest.xml` as a direct child of `<manifest>`:

```xml
<uses-feature android:name="android.hardware.touchscreen" android:required="false" />
```

A copy is provided in `AndroidManifest-firetv-snippet.xml` in the project Files folder.

Do not overwrite the existing mobile project/package. This Fire TV edition intentionally uses a separate application ID.

## Test checklist

1. Preview in Construct with keyboard: arrows navigate, Enter/Space confirm, Enter/Up flaps, Escape pauses/resumes.
2. Export Android Studio project.
3. Apply the touchscreen-not-required manifest line.
4. Build an APK.
5. Install on Fire TV, Android TV Emulator, or accepted Fire TV/Vega simulator.
6. Verify D-pad focus, Center, Back, sound, pause/restart, game-over restart, and next-level flow.
7. Record the Devpost demonstration on the accepted target device/simulator.
