# Control TV Samsung (APK)

## Opción A: compilar en GitHub (sin instalar nada)
1. Crea un repositorio en github.com y sube TODO el contenido de esta carpeta (incluida `.github`).
2. Ve a la pestaña Actions > "Build APK" y espera ~5 min.
3. Entra a la ejecución terminada y descarga el artefacto `control-tv-apk` (contiene app-debug.apk).
4. Pásalo al celular e instálalo (permite "orígenes desconocidos").

## Opción B: compilar en tu PC (Node 20 + Java 17 + Android Studio)
    npm install
    npx cap add android
    bash scripts/patch-android.sh
    npx cap sync android
    cd android && ./gradlew assembleDebug
APK: android/app/build/outputs/apk/debug/app-debug.apk

## Wake-on-LAN en la TV
- MAC: Configuración > General > Red > Estado de red > Config. IP (o Acerca de esta TV).
- Activa "Encender con móvil" (Configuración > General > Red > Configuración experta).
- Funciona mejor con la TV por cable; en Wi-Fi depende del modelo.
