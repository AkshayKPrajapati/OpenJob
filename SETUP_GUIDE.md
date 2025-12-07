# Open Job - Project Setup Guide

## 🎯 Project Overview

**Open Job** is a professional Flutter application designed for job searching and skill development with comprehensive theme management.

### Key Features
- ✨ Beautiful Splash Screen with animations
- 🏠 Home screen with featured jobs
- 📚 Learner screen for courses and skill development
- 👤 Profile management screen
- 📱 Bottom Navigation Bar (Home, Learner, Profile)
- 🍔 Professional Sidebar Drawer with hamburger menu
- 🌓 Dark/Light theme support with persistent storage
- 🎨 Color palette based on professional design standards

---

## 📁 Project Structure

```
open_job/
├── lib/
│   ├── main.dart                      # App entry point with theme integration
│   ├── config/
│   │   └── theme_config.dart          # Light & Dark theme configuration
│   ├── providers/
│   │   └── theme_provider.dart        # Theme state management
│   ├── screens/
│   │   ├── splash_screen.dart         # Animated splash screen
│   │   ├── main_navigation.dart       # Bottom navigation container
│   │   ├── home_screen.dart           # Job listings and featured jobs
│   │   ├── learner_screen.dart        # Learning courses and progress
│   │   └── profile_screen.dart        # User profile and settings
│   └── widgets/
│       └── app_drawer.dart            # Sidebar drawer with theme toggle
├── assets/
│   ├── images/                        # App images and logos
│   └── icons/                         # Custom icons
├── pubspec.yaml                       # Dependencies configuration
├── analysis_options.yaml              # Linting rules
└── README.md                          # Project documentation
```

---

## 🚀 Setup Instructions

### Step 1: Navigate to Project Directory
```powershell
cd c:\flutter\flutter_project\open_job
```

### Step 2: Install Dependencies
```powershell
flutter pub get
```

This will install:
- `provider` - State management for theme
- `shared_preferences` - Persistent theme storage
- `cupertino_icons` - iOS style icons

### Step 3: Run the Application
```powershell
flutter run
```

---

## 🎨 Theme Management

### Color Palette
Based on the provided design, the app uses:
- **Primary Blue**: `#1877F2` - Main brand color
- **Light Blue**: `#409CFF` - Secondary actions
- **Background Light**: `#E7E9ED` - Light mode background
- **Background Grey**: `#B0B3B8` - Neutral elements
- **Text Dark**: `#242526` - Dark text

### Theme Features
1. **Automatic Theme Detection**: App remembers user preference
2. **Persistent Storage**: Theme choice saved across app restarts
3. **Smooth Transitions**: Seamless switching between modes
4. **System-wide**: All screens and components respect theme

### Toggle Theme
Users can switch themes from:
- **Sidebar Drawer**: Dark Mode toggle switch
- Automatically saves preference using SharedPreferences

---

## 📱 Screen Details

### 1. Splash Screen
- **Duration**: 3 seconds
- **Features**:
  - Fade-in animation
  - Scale animation
  - App logo with gradient background
  - Loading indicator
- **Auto-navigation**: Redirects to Main Navigation

### 2. Main Navigation (Bottom Nav Bar)
- **Tabs**: Home, Learner, Profile
- **Features**:
  - App bar with search and notifications
  - Hamburger menu for drawer
  - Active tab highlighting
  - Smooth tab transitions

### 3. Home Screen
- Welcome card
- Quick statistics (Jobs Available, Companies)
- Featured jobs list with:
  - Company name and logo
  - Position and location
  - Salary range
  - Bookmark functionality

### 4. Learner Screen
- Learning progress tracker
- Course recommendations with:
  - Course title and instructor
  - Duration and ratings
  - Student count
  - "Start Learning" button

### 5. Profile Screen
- User profile header
- Application statistics
- Settings sections:
  - Account Settings
  - Preferences
  - Help & Support
- Logout functionality

### 6. Sidebar Drawer
- **Header**: App branding with gradient
- **Menu Items**:
  - Home
  - Browse Jobs
  - Companies
  - My Applications
  - Saved Jobs
  - Learning Center
  - My Certificates
  - **Dark Mode Toggle** ⭐
  - Settings
  - Help & Support
  - About
  - Logout

---

## 🔧 Customization Guide

### Adding Custom Logo
1. Place your logo image in `assets/images/`
2. Update `pubspec.yaml` to ensure assets are included
3. Modify `splash_screen.dart`:
   ```dart
   // Replace the Icon widget with:
   Image.asset(
     'assets/images/your_logo.png',
     width: 100,
     height: 100,
   )
   ```

### Changing Colors
Edit `lib/config/theme_config.dart`:
```dart
static const Color primaryBlue = Color(0xFF1877F2); // Change hex code
```

### Adding New Screens
1. Create screen file in `lib/screens/`
2. Add to bottom navigation in `main_navigation.dart`
3. Add drawer menu item in `app_drawer.dart`

---

## 📦 Dependencies

```yaml
dependencies:
  flutter:
    sdk: flutter
  cupertino_icons: ^1.0.2      # iOS style icons
  shared_preferences: ^2.2.2    # Persistent storage
  provider: ^6.1.1              # State management
```

---

## 🎯 Next Steps & Future Features

### Recommended Additions
1. **Authentication**:
   - Firebase Auth integration
   - Login/Register screens
   - Password recovery

2. **API Integration**:
   - Real job listings API
   - Course content API
   - User profile backend

3. **Features**:
   - Job search and filters
   - Application submission
   - Resume upload
   - Push notifications
   - In-app messaging

4. **Enhancements**:
   - Animations and transitions
   - Skeleton loaders
   - Pull-to-refresh
   - Infinite scroll

5. **Testing**:
   - Unit tests
   - Widget tests
   - Integration tests

---

## 🐛 Troubleshooting

### Common Issues

**1. Dependencies not installing:**
```powershell
flutter clean
flutter pub get
```

**2. Build errors:**
```powershell
flutter clean
flutter pub cache repair
flutter pub get
```

**3. Theme not persisting:**
- Check SharedPreferences permissions
- Clear app data and restart

**4. Hot reload not working:**
```powershell
# Stop the app and run again
flutter run
```

---

## 📝 Development Tips

### Best Practices
1. **State Management**: Use Provider for global state (theme, user data)
2. **Code Organization**: Keep screens, widgets, and logic separated
3. **Theme Consistency**: Always use `Theme.of(context)` for colors and styles
4. **Responsive Design**: Test on different screen sizes
5. **Performance**: Use `const` constructors where possible

### VS Code Extensions Recommended
- Flutter
- Dart
- Flutter Widget Snippets
- Awesome Flutter Snippets

### Useful Commands
```powershell
# Check Flutter doctor
flutter doctor

# Run on specific device
flutter devices
flutter run -d <device-id>

# Build APK
flutter build apk --release

# Build iOS
flutter build ios --release

# Analyze code
flutter analyze
```

---

## 📄 License & Credits

Created with ❤️ using Flutter

**Open Job** - Your Career, Your Future

Version: 1.0.0
© 2025 All rights reserved.

---

## 🤝 Support

For issues or questions:
1. Check the troubleshooting section
2. Review Flutter documentation
3. Check Provider package documentation

Happy Coding! 🚀
