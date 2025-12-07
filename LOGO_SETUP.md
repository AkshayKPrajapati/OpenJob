# Logo Placeholder Instructions

## 📌 Current Logo Setup

The app currently uses a **dummy icon** (work_outline_rounded) as the logo.

### Where the Logo Appears:
1. **Splash Screen** - Large centered logo with animation
2. **Sidebar Drawer Header** - Circular avatar logo

---

## 🎨 How to Add Your Custom Logo

### Step 1: Prepare Your Logo
- **Format**: PNG with transparent background
- **Size**: 512x512 pixels (recommended)
- **Name**: `app_logo.png`

### Step 2: Add Logo to Assets
```
Copy your logo to:
c:\flutter\flutter_project\open_job\assets\images\app_logo.png
```

### Step 3: Update Splash Screen

Open: `lib/screens/splash_screen.dart`

Find this code (around line 76):
```dart
Container(
  width: 150,
  height: 150,
  decoration: BoxDecoration(
    color: Colors.white,
    borderRadius: BorderRadius.circular(30),
    boxShadow: [
      BoxShadow(
        color: Colors.black.withOpacity(0.2),
        blurRadius: 20,
        offset: Offset(0, 10),
      ),
    ],
  ),
  child: Icon(
    Icons.work_outline_rounded,
    size: 80,
    color: Color(0xFF1877F2),
  ),
),
```

Replace with:
```dart
Container(
  width: 150,
  height: 150,
  decoration: BoxDecoration(
    color: Colors.white,
    borderRadius: BorderRadius.circular(30),
    boxShadow: [
      BoxShadow(
        color: Colors.black.withOpacity(0.2),
        blurRadius: 20,
        offset: Offset(0, 10),
      ),
    ],
  ),
  child: ClipRRect(
    borderRadius: BorderRadius.circular(30),
    child: Image.asset(
      'assets/images/app_logo.png',
      width: 120,
      height: 120,
      fit: BoxFit.contain,
    ),
  ),
),
```

### Step 4: Update Drawer Header

Open: `lib/widgets/app_drawer.dart`

Find this code (around line 29):
```dart
CircleAvatar(
  radius: 35,
  backgroundColor: Colors.white,
  child: Icon(
    Icons.work_outline_rounded,
    size: 40,
    color: Color(0xFF1877F2),
  ),
),
```

Replace with:
```dart
CircleAvatar(
  radius: 35,
  backgroundColor: Colors.white,
  child: ClipOval(
    child: Image.asset(
      'assets/images/app_logo.png',
      width: 60,
      height: 60,
      fit: BoxFit.cover,
    ),
  ),
),
```

### Step 5: Hot Reload
```powershell
# If app is running, press 'R' for hot restart
# Or restart the app
flutter run
```

---

## 🎯 Alternative: Use Network Image

If your logo is online, use:
```dart
Image.network(
  'https://your-domain.com/logo.png',
  width: 120,
  height: 120,
  fit: BoxFit.contain,
)
```

---

## 📱 App Icon (Launcher Icon)

To change the app icon on device home screen:

### Android
Replace: `android/app/src/main/res/mipmap-*/ic_launcher.png`

### iOS
Replace: `ios/Runner/Assets.xcassets/AppIcon.appiconset/`

### Or Use flutter_launcher_icons Package
```yaml
# Add to pubspec.yaml
dev_dependencies:
  flutter_launcher_icons: ^0.13.1

flutter_launcher_icons:
  android: true
  ios: true
  image_path: "assets/images/app_logo.png"
```

Run:
```powershell
flutter pub get
flutter pub run flutter_launcher_icons
```

---

## ✅ Checklist

- [ ] Logo image prepared (512x512 PNG)
- [ ] Logo added to `assets/images/`
- [ ] Splash screen updated
- [ ] Drawer header updated
- [ ] App restarted/hot reloaded
- [ ] Logo displays correctly
- [ ] Optional: App icon updated

---

## 🎨 Current Dummy Icon

The current icon (`Icons.work_outline_rounded`) is:
- Professional briefcase icon
- Matches the job search theme
- Works well as placeholder
- Can be kept if you prefer

---

**Ready to add your custom logo!** 🎨
