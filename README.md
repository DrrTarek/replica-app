# Router app (first slice)

Expo + TypeScript. Screens: S01 connect, home, S03 Wi-Fi (read only), S04 devices (read only).
Runs on a **mock adapter** with fake data. The HG8145V5 adapter is a stub (see `../replica/build-log.md`).

## Run on Windows

1. Install Node.js LTS, Android Studio (with an Android SDK) and Git.
2. In PowerShell:
   ```powershell
   npx create-expo-app@latest router-app --template blank-typescript
   cd router-app
   npx expo install expo-router expo-sqlite expo-secure-store expo-crypto expo-build-properties react-native-safe-area-context react-native-screens
   ```
3. Copy `app/`, `src/` and `app.json` from this folder over the new project (replace the files).
4. In `package.json` set `"main": "expo-router/entry"`.
5. Build and run a development build (Expo Go is not enough: plain HTTP to the router needs a custom build):
   ```powershell
   npx expo run:android
   ```
6. On the first screen pick "تجريبي" (mock), type any host, user and password, and press connect.

This code was written without running it. Expect to fix small errors on the first run.
