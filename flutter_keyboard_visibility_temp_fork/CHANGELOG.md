## [0.1.8] - October 16, 2026

- iOS: no longer reports the keyboard as visible when a rotation posts `keyboardWillShow`/`keyboardDidShow` for a keyboard that isn't on screen (a zero-height frame at the bottom edge, seen on a foldable's inner display). Nothing hides a keyboard that never appeared, so the state used to stay stuck at visible.
- iOS: measures keyboard frames against the screen the notification belongs to instead of `UIScreen.main`, which is a different display on a device with two screens.

## [0.1.7] - September 4, 2026

- Updates the federated platform dependencies to `flutter_keyboard_visibility_platform_interface` 3.0.0 and `flutter_keyboard_visibility_linux`, `flutter_keyboard_visibility_macos`, `flutter_keyboard_visibility_windows` 2.0.0.
- Raises the minimum supported versions to Dart 3.11 and Flutter 3.41 to match them.
- Uses `flutter.compileSdkVersion` on Android instead of pinning `compileSdkVersion 34` ([#9](https://github.com/EchoEllet/flutter_keyboard_visibility_temp_fork/pull/9)).

## [0.1.6] - February 20, 2025

- Fixes WASM compilation issue when using [`flutter_keyboard_visibility`](https://pub.dev/packages/flutter_keyboard_visibility) with this package by removing the deprecated class `FlutterKeyboardVisibilityPluginWeb` which is not expected to be used by clients.

## [0.1.5] - December 2, 2024

- Updates the threshold for detecting the keyboard state from 85% to 82% of the visible screen height. This improves accuracy in determining whether the keyboard is visible [#5](https://github.com/EchoEllet/flutter_keyboard_visibility_temp_fork/pull/5/).

## [0.1.4] - November 24, 2024

* Supports Swift package manager.
* Migrates the iOS plugin from Objective-C to Swift.
* Updates the minimum supported iOS from `8.0` to `9.0`.

## [0.1.3] - November 7, 2024

* Promoted 0.1.3-alpha to stable.

## [0.1.3-alpha] - November 6, 2024

* Adds iOS notification observer for the floating keyboard (see [PR #2](https://github.com/EchoEllet/flutter_keyboard_visibility_temp_fork/pull/2)).
* Adds keyboard debounce check (see [PR #2](https://github.com/EchoEllet/flutter_keyboard_visibility_temp_fork/pull/2)).

## [0.1.2-alpha] - November 5, 2024

* Fixes plugin class name collisions with [flutter_keyboard_visibility](https://pub.dev/packages/flutter_keyboard_visibility) for Web, Android, and iOS. Which updates the platform plugin name to `FlutterKeyboardVisibilityTempForkPlugin`. The desktop platforms don't have issues.
* Updates the [web](https://pub.dev/packages/web) dependency constraints to `>=0.5.1 <2.0.0`.

## [0.1.1] - September 27, 2024

* Updates `README.md` to reflect the changes.

## [0.1.0] - September 27, 2024

* Initial release for the temporary fork of [flutter_keyboard_visibility](https://pub.dev/packages/flutter_keyboard_visibility).
