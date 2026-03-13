# Multi Apps MCK 🏆

> **Luxury app cloner** — clone, secure, and personalise any app with a premium experience.

## ✦ Tech Stack

| Layer | Technology |
|-------|-----------|
| State | Riverpod 2 |
| Navigation | GoRouter 14 |
| Local storage | Hive Flutter |
| Secure storage | Flutter Secure Storage |
| Biometrics | local_auth |
| DI | get_it |
| Animations | Lottie |
| Purchases | in_app_purchase (RevenueCat-ready) |
| Linting | flutter_lints + riverpod_lint |

## ✦ Architecture

Feature-first + Clean Architecture inside each feature:

```
lib/
├── core/           # Shared constants, theme, services, DI, errors
├── features/       # Isolated business features
│   ├── app_cloner/
│   │   ├── data/         # Hive persistence, repository impl
│   │   ├── domain/       # Entities, abstract repos, use-cases (pure Dart)
│   │   └── presentation/ # Screens, widgets, Riverpod providers
│   └── ...
├── router/         # GoRouter config, typed route constants
├── app.dart        # MaterialApp.router
└── main.dart       # Bootstrap: Hive + DI + Logger → ProviderScope
```

## ✦ Getting Started

```bash
# Install dependencies
flutter pub get

# Run on device/emulator
flutter run

# Generate Riverpod code (when @riverpod annotations added)
dart run build_runner build --delete-conflicting-outputs
```

## ✦ Features

| Feature | Status |
|---------|--------|
| Splash + Onboarding | ✅ Shell ready |
| Dashboard – clone list | ✅ Shell ready |
| App Cloner engine | 🔧 Domain done, engine in Part 3 |
| Security (PIN + Biometrics) | ✅ Shell ready |
| Customisation | 📭 Shell placeholder |
| Premium / Elite paywall | ✅ Shell ready |
| Settings | ✅ Shell ready |
| Cloud Sync | 🔮 Future |

## ✦ Parts Roadmap

- **Part 1** ✅ Folder structure + all starter files (this commit)
- **Part 2** — Riverpod providers, clone list, Hive persistence
- **Part 3** — Android cloning engine (Work Profile / MultiDex strategy)
- **Part 4** — Premium (RevenueCat or IAP), gate guards
- **Part 5** — Polish: Lottie animations, onboarding, accessibility

## ✦ Environment

- Flutter ≥ 3.22, Dart ≥ 3.3
- Android minSdk 24 (Work Profile API)
- iOS 16+ (limited cloning via shortcuts/Deep Link)

---
*Built with ❤️ and gold accents.*
