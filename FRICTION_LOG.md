# Fire TV Development Friction Log

## Task attempted

Implement reliable Back-button pause and resume behavior for Sky Rings Phú Yên – Fire TV Edition using a television remote.

## Steps taken

1. Added Construct 3 Browser events for the mobile/remote Back button.
2. Tested the game in the Android TV Emulator.
3. Observed that the remote Back input reached Android but the Construct event did not reliably trigger.
4. Used Android Studio Logcat to inspect remote key events.
5. Confirmed that Android was receiving `KEYCODE_BACK`.
6. Added native Java handling in `MainActivity.java`.
7. Forwarded the Back event directly from Android to the Cordova/JavaScript layer.
8. Updated the Construct game-state logic so Back pauses when gameplay is active and resumes when the pause menu is open.
9. Rebuilt and tested the signed release APK on the Android TV Emulator.

## Expected result

Pressing Back once during gameplay should pause the game and display the TV pause menu. Pressing Back again should resume gameplay.

## Actual result

Initially, Android received the Back key but the Construct Browser event did not reliably react to it. The game therefore continued running even though the remote input had been detected at the native Android level.

## Severity

High — reliable Back-button behavior is essential for a television application because it is a primary remote-control action.

## Workaround used

I implemented a native Java handler in `MainActivity.java` that detects `KEYCODE_BACK` and forwards a Cordova `backbutton` event directly to JavaScript. Construct 3 then handles the pause/resume logic using the current game state.

## Actionable suggestion

Provide an official Fire TV sample for Cordova/HTML5 applications demonstrating D-pad, Center/OK, Back-button handling, focus navigation, and Android-to-JavaScript event forwarding.

A dedicated troubleshooting guide showing how to confirm remote key events in Logcat and how they should propagate through Cordova would also save developers significant debugging time.
