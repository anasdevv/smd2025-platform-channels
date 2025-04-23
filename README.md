# Battery Level App

A Flutter application that demonstrates platform-specific code integration using platform channels. This app retrieves the device's battery level from the native Android system and displays it in the Flutter UI.

![Battery Level App Screenshot](assets/images/app_screenshot.png)

## Features

- Retrieves real-time battery level from the device
- Clean Material Design UI
- Error handling for battery level retrieval failures
- Platform channel implementation between Flutter and native Android (Kotlin)

## Project Structure

- **Flutter UI**: `lib/main.dart` - Contains the Flutter UI and platform channel client code
- **Native Android Code**: `android/app/src/main/kotlin/com/example/batterylevel/MainActivity.kt` - Contains the Kotlin implementation for battery level retrieval

## Getting Started

### Prerequisites

- Flutter SDK (latest version recommended)
- Android Studio or VS Code with Flutter extensions
- An Android device or emulator for testing

### Installation

1. Clone this repository:

   ```
   git clone https://github.com/yourusername/batterylevel.git
   ```

2. Navigate to the project directory:

   ```
   cd batterylevel
   ```

3. Install dependencies:
   ```
   flutter pub get
   ```

## Running the App

### On an Android Device

1. Connect your Android device to your computer via USB
2. Enable USB debugging on your device (Settings > Developer options > USB debugging)
3. Run the app:
   ```
   flutter run
   ```
   Or specify your device ID:
   ```
   flutter run -d <device-id>
   ```

### On an Android Emulator

1. Start an Android emulator
2. Run the app:
   ```
   flutter run
   ```

## Testing the App

1. Launch the app on your device or emulator
2. The app will initially display "Current battery level: Unknown"
3. Tap the floating action button (battery icon) at the bottom right
4. The app will display your current battery level as a percentage

## Development Commands

While the app is running, you can use these commands:

- Press 'r' for hot reload (to quickly see UI changes)
- Press 'R' for hot restart (to restart the app)
- Press 'q' to quit the app

## How It Works

This app demonstrates the use of platform channels to communicate between Flutter and native code:

1. The Flutter UI sends a method call to the native Android code via a MethodChannel
2. The native Kotlin code retrieves the battery level using Android's BatteryManager
3. The result is sent back to Flutter and displayed in the UI

```markdown
[demo](assets/demo.jpeg)
```

## Resources

- [Flutter Platform Channels Documentation](https://docs.flutter.dev/platform-integration/platform-channels)
- [Flutter Documentation](https://docs.flutter.dev/)
- [Dart Documentation](https://dart.dev/guides)
