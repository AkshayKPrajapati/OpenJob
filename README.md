# Open Job

A professional Flutter application for job searching and learning with comprehensive theme management (Dark/Light mode).

## Features

- 🎨 Dark/Light theme support with persistent preferences
- 🏠 Home screen with job listings
- 📚 Learner screen for courses and tutorials
- 👤 Profile management
- 📱 Bottom navigation bar
- 🍔 Hamburger menu with sidebar drawer
- 💫 Professional splash screen

## Project Structure

```
lib/
├── main.dart
├── config/
│   └── theme_config.dart
├── providers/
│   └── theme_provider.dart
├── screens/
│   ├── splash_screen.dart
│   ├── main_navigation.dart
│   ├── home_screen.dart
│   ├── learner_screen.dart
│   └── profile_screen.dart
└── widgets/
    └── app_drawer.dart
```

## Getting Started

1. Run `flutter pub get` to install dependencies
2. Run `flutter run` to start the app

## Theme Management

The app uses Provider for state management and SharedPreferences for persistent theme storage.
