# Whether App

Whether App is a Flutter weather application that detects the user's current city, fetches live weather data from OpenWeatherMap, and renders a condition-specific Lottie animation. It is designed to be a lightweight, visual-first weather experience for Flutter mobile and desktop targets.

## What It Does

- Detects the user's current location and resolves it to a city name.
- Fetches live temperature and condition data from OpenWeatherMap.
- Displays weather state with animated Lottie assets for clear, cloudy, rainy, and stormy conditions.
- Uses a simple, focused UI so the current weather is visible immediately on launch.

## Why It Is Useful

- Removes manual city search by using the device's current location.
- Provides a quick at-a-glance weather view with animated feedback.
- Keeps the app small and easy to modify because the weather model and service are simple.
- Ships with Flutter's standard platform scaffolding, so it can be extended to other targets later.

## Tech Stack

- Flutter
- Dart
- `http` for API requests
- `geolocator` and `geocoding` for location lookup
- `lottie` for weather animations

## Getting Started

### Prerequisites

- Flutter SDK `>=3.2.5`
- A working Android, iOS, macOS, Windows, or Linux development setup for Flutter
- An OpenWeatherMap API key

### Install

```bash
flutter pub get
```

### Run

```bash
flutter run
```

If you have multiple devices connected, specify a target:

```bash
flutter devices
flutter run -d <device_id>
```

### Configuration

The weather request is configured in [lib/services/weather_service.dart](lib/services/weather_service.dart). Replace the current OpenWeatherMap API key with your own key before distributing the app.

Android location permissions are already declared in [android/app/src/main/AndroidManifest.xml](android/app/src/main/AndroidManifest.xml).

For iOS, make sure your app has a location usage description in [ios/Runner/Info.plist](ios/Runner/Info.plist) before shipping to devices or TestFlight.

## Project Structure

- [lib/main.dart](lib/main.dart) bootstraps the app.
- [lib/pages/weather_page.dart](lib/pages/weather_page.dart) contains the main weather UI.
- [lib/services/weather_service.dart](lib/services/weather_service.dart) handles location lookup and API calls.
- [lib/models/weather_model.dart](lib/models/weather_model.dart) defines the weather data model.
- [assets/](assets/) contains the weather animations used by the UI.

## Help and Documentation

If you need help working with the app or the dependencies, these resources are the best starting points:

- [Flutter documentation](https://docs.flutter.dev/)
- [OpenWeatherMap API docs](https://openweathermap.org/current)
- [geolocator package](https://pub.dev/packages/geolocator)
- [geocoding package](https://pub.dev/packages/geocoding)
- [lottie package](https://pub.dev/packages/lottie)

## Maintainers and Contributions

This project is maintained by the repository owner. Contributions are welcome through pull requests. Keep changes focused, follow the existing Flutter style, and update this README if setup or runtime behavior changes.

If you want to formalize contribution rules, add a dedicated `CONTRIBUTING.md` file and link it here.

## License

Add a `LICENSE` file if you plan to publish or share the project publicly.
