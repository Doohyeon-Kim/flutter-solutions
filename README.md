# Flutter Solutions

written by Doohyeon Kim, First written on 10/06/2021, last updated date on 10/06/2021

<br>

### json_serializable
Generate json serializable code file.
```
flutter pub run build_runner build
```

Adding watcher to auto-generate the code file.
```
flutter pub run build_runner watch
```

error: pub finished with exit code 78
```
flutter clean
flutter pub get
flutter packages pub run build_runner build --delete-conflicting-outputs
```

<br>

### Keyboard Error(Android)
error message
```
W/IInputConnectionWrapper(24997): beginBatchEdit on inactive InputConnection
W/IInputConnectionWrapper(24997): getTextBeforeCursor on inactive InputConnection
W/IInputConnectionWrapper(24997): getTextAfterCursor on inactive InputConnection
W/IInputConnectionWrapper(24997): getSelectedText on inactive InputConnection
W/IInputConnectionWrapper(24997): endBatchEdit on inactive InputConnection
W/IInputConnectionWrapper(24997): beginBatchEdit on inactive InputConnection
W/IInputConnectionWrapper(24997): endBatchEdit on inactive InputConnection
```
cause: Occurs while rebuilding the parent widget when the keyboard is showing up on the Android device.

Solution 1.
```
resizeToAvoidBottomInset : false, 
```

Solution 2.

check Navigator or context as argument.

<br>

### Podfile Error(iOS)

Automatically assigning platform `iOS` with version `9.0` on target `Runner` because no platform was specified. Please specify a platform for this target in your Podfile.

Solution.

1. Check which iOS versions are compatible with package what you are using.

2. Specify your target iOS bersion

