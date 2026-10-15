# PeriSafio-Updates

Repositorio para distribuir el manifiesto de actualizaciones del launcher PeriSafio.

## Publicación
1. Sube `manifest.json` y activa GitHub Pages en Settings → Pages, rama `main`, carpeta `/(root)`.
2. Aloja los archivos grandes (mods y paquetes) en GitHub Releases.
3. Añade al array `files` del manifiesto la URL HTTPS de cada archivo, su SHA-256 real y su ruta de destino.

**Importante:** el launcher debe implementar el lector del manifiesto, descarga HTTPS, verificación SHA-256 y actualización segura. Este repositorio por sí solo no añade un botón al launcher. El manifiesto inicial tiene `files: []` hasta que se añadan URLs y hashes reales.
