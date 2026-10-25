# PDF Editor Pro (móvil)

Versión Android (Capacitor) del editor de PDFs. Mismo motor que la versión web
([pdf-editor-pro](https://github.com/melvinfranco99/pdf-editor-pro)) y la de escritorio
([pdf-editor-pro-desktop](https://github.com/melvinfranco99/pdf-editor-pro-desktop)), pero
pensada para el móvil: botones grandes, barra de herramientas con scroll horizontal y
exportación mediante la hoja de compartir de Android (guardar en Drive, Archivos, enviar
por WhatsApp, etc.). Todo tu PDF se procesa en el teléfono; nada se sube a ningún servidor.

**Página de descarga:** https://melvinfranco99.github.io/pdf-editor-pro-mobile/

## Herramientas incluidas

Las mismas que las versiones web y de escritorio: unir/reordenar/eliminar páginas de
varios PDFs, texto (mover, redimensionar, grosor y transparencia), dibujo y resaltado
libres con transparencia ajustable, resaltado recto asistido, goma de borrar con
intensidad progresiva, firmas (dibujadas o generadas con tu nombre), deshacer/rehacer y
exportación a un PDF nuevo.

## Instalación

1. Descarga el `.apk` desde [Releases](https://github.com/melvinfranco99/pdf-editor-pro-mobile/releases)
   o desde la [página de descarga](https://melvinfranco99.github.io/pdf-editor-pro-mobile/).
2. Tu teléfono probablemente avise de "origen desconocido": es normal al instalar un APK
   fuera de Google Play. Acepta para continuar con la instalación.
3. Abre el APK descargado para instalarlo.

Es una compilación de depuración (debug), suficiente para instalación personal; no está
firmada para publicación en Google Play.

## Desarrollo

```
npm install
npx cap sync android
cd android && ./gradlew assembleDebug   # genera android/app/build/outputs/apk/debug/app-debug.apk
```

El contenido web (`www/`) usa pdf.js y pdf-lib empaquetados localmente (sin CDN), por lo
que la app funciona sin conexión salvo las tipografías de firma automática (Google Fonts),
que se degradan a una fuente manuscrita genérica sin red.
