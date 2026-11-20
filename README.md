# TurnoPro EU - Capacitor (Android e iOS)

## Requisitos
- Node.js 20 o superior.
- Android: Android Studio. iOS: Mac con Xcode y CocoaPods.

## Pasos
1. `npm install`
2. `npm run build:web` (genera `www/`)
3. Agrega las plataformas, una sola vez:
   - `npx cap add android`
   - `npx cap add ios` (solo en Mac)
4. `npm run assets` (genera íconos y pantalla de carga desde `assets/`)
5. `npm run android` o `npm run ios` (compila la web, sincroniza y abre el IDE). Desde ahí ejecutas en el equipo o generas el APK/AAB o el archivo para App Store.

## Notas
- `capacitor.config.json`: cambia `appId` (`cl.turnopro.eu`) por el identificador de tu institución antes de publicar.
- PDF, Word y respaldo se guardan en caché y se abren con el menú de compartir del teléfono (usa los plugins Filesystem y Share).
- Los datos viven en el almacenamiento local de la app. Usa el respaldo si cambias de teléfono.
- Si `npm install` instala una versión mayor de Capacitor distinta de 7, mantén todos los paquetes `@capacitor/*` en la misma versión mayor.
- Sin probar en dispositivos reales: valida el flujo antes de usarlo en turno.
