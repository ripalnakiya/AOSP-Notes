# ADB

Android Debug Bridge (ADB) is a versatile command line tool that lets you communicate with an emulator instance.

Used for various purposes, including:

- Installing apps
- Debugging apps
- Accessing Unix shell of the device

## adb Commands

- `adb devices`: Lists all connected Android devices or emulators.
- `adb install <path-to-apk>`: Installs an APK on the connected device.
- `adb uninstall <package-name>`: Uninstalls an app from the connected device.
- `adb logcat`: Displays real-time logs from the device, useful for debugging.
- `adb shell`: Opens a shell on the device for executing commands directly.
- `adb pull <remote-path> <local-path>`: Copies a file from the device to the local machine.
- `su` : Used to switch to the superuser (root) account
