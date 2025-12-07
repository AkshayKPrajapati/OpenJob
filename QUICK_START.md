# 🚀 Quick Start Guide - Open Job

## Run the Application

### Option 1: Using VS Code
1. Open the project in VS Code
2. Press `F5` or click "Run and Debug"
3. Select your device (emulator or physical device)

### Option 2: Using Command Line
```powershell
# Navigate to project
cd c:\flutter\flutter_project\open_job

# Run on default device
flutter run

# Or select specific device
flutter devices
flutter run -d <device-id>
```

---

## 📱 Testing the App

### 1. Splash Screen (3 seconds)
- Animated logo with fade and scale effects
- Gradient background
- Automatically navigates to Home

### 2. Home Screen
- View featured jobs
- Check statistics
- Bookmark jobs
- Access search and notifications

### 3. Learner Screen
- View learning progress
- Browse recommended courses
- Check course details (duration, ratings, students)

### 4. Profile Screen
- View profile information
- Check application statistics
- Access account settings
- Manage preferences

### 5. Bottom Navigation
- Tap icons to switch between: Home, Learner, Profile
- Active tab is highlighted in blue

### 6. Hamburger Menu (Sidebar)
- Tap menu icon (☰) in top-left
- **Try the Dark Mode toggle** 🌓
- Browse all menu options
- Theme preference is saved automatically!

---

## 🌓 Dark Mode Testing

**How to Test:**
1. Open app
2. Tap hamburger menu (☰)
3. Toggle "Dark Mode" switch
4. Watch the entire app theme change instantly!
5. Close and reopen app → theme is remembered ✓

---

## 🎨 Color Scheme

### Light Mode
- Primary: Blue (#1877F2)
- Background: White
- Cards: White with shadow

### Dark Mode
- Primary: Light Blue (#409CFF)
- Background: Dark (#18191A)
- Cards: Dark Gray (#242526)

---

## 📝 Current Features (v1.0.0)

✅ Splash Screen with animations
✅ Home screen with job listings
✅ Learner screen with courses
✅ Profile screen with settings
✅ Bottom Navigation Bar
✅ Sidebar Drawer with menu
✅ Dark/Light theme toggle
✅ Persistent theme storage
✅ Professional UI design
✅ Responsive layouts

---

## 🔜 Coming Soon

🔄 Real API integration
🔄 User authentication
🔄 Job search and filters
🔄 Application submission
🔄 Resume upload
🔄 Push notifications

---

## 🛠️ Troubleshooting

**App not running?**
```powershell
flutter doctor
flutter clean
flutter pub get
flutter run
```

**Theme not saving?**
- Clear app data
- Reinstall app
- Check permissions

**Build errors?**
```powershell
flutter clean
flutter pub cache repair
flutter pub get
```

---

## 📞 Need Help?

Refer to:
- `SETUP_GUIDE.md` - Comprehensive setup instructions
- `README.md` - Project overview
- Flutter documentation: https://flutter.dev/docs

---

Happy Testing! 🎉
