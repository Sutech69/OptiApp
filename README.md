# Optik Falkner – Kunden-App (Prototyp)

Web-App (`www/index.html`) + Android-Hülle via [Capacitor](https://capacitorjs.com).

## APK über GitHub bauen (empfohlen)
1. Alle Dateien in ein GitHub-Repository hochladen (Branch `main`).
2. Unter **Actions** startet „Android APK bauen“ automatisch (oder manuell über *Run workflow*).
3. Nach ca. 5 Minuten im Lauf unten bei **Artifacts** → `optik-falkner-apk` herunterladen (ZIP mit der APK).
4. APK aufs Handy kopieren und installieren („Installation aus unbekannten Quellen“ erlauben).

## Lokal bauen (Android Studio / Android SDK + JDK 21 nötig)
```
npm install
npx cap add android
npm run android:icons
npx cap sync android
npm run android:build
```
APK: `android/app/build/outputs/apk/debug/app-debug.apk`

## Web-Version (GitHub Pages)
Pages-Quelle auf den Ordner `/www` geht nicht direkt – entweder `www/index.html` zusätzlich ins Root kopieren oder Pages per Action aus `www` deployen.

## Inhalte ändern
Nur `www/index.html` bearbeiten → pushen → neue APK wird automatisch gebaut.
