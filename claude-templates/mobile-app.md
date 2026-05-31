# CLAUDE.md - Mobile App Project

## Project Overview
[App name] is a mobile app for [purpose] targeting [platforms].

## Tech Stack
- Framework: React Native / Flutter
- Language: TypeScript / Dart
- State: Zustand / Riverpod
- Navigation: React Navigation / GoRouter
- API: REST + GraphQL
- Auth: OAuth2 + Biometric

## Architecture
- Feature-first directory structure
- Clean Architecture layers
- Repository pattern for data
- BLoC / ViewModel for screen logic

## UI/UX Rules
- Follow platform conventions (Material/iOS)
- Responsive design for all screen sizes
- Dark mode support
- Accessibility labels
- Smooth animations (60fps target)
- Offline-first where possible

## Testing
- Unit tests for business logic
- Widget/component tests for UI
- Integration tests for flows
- Golden/image tests for critical screens
- Test on real devices before release

## Build & Deploy
- EAS Build / Fastlane
- Staged rollout (1% → 10% → 100%)
- Code signing via CI
- Sentry for crash reporting
- Analytics for user behavior
