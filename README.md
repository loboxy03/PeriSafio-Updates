# PeriSafio-Updates

Manifiesto HTTPS para el launcher PeriSafio (Minecraft 1.20.1, Forge 47.4.10).

## Activar GitHub Pages
1. Abre Settings → Pages.
2. Selecciona **Deploy from a branch**, rama `main`, carpeta `/(root)`.
3. Guarda y espera a que GitHub publique el sitio.
4. La URL del manifiesto será `https://loboxy03.github.io/PeriSafio-Updates/manifest.json`.

## Publicar contenido para actualizaciones
El launcher lee `files` del manifiesto. Cada archivo debe incluir `path`, `type`, `sha256` y `url` (HTTPS directa al archivo). Ejemplo de estructura:

```json
{
  "content_version": "7",
  "launcher_version": "1.0.3",
  "minecraft_version": "1.20.1",
  "forge_version": "47.4.10",
  "files": [
    {
      "path": "mods/Ejemplo.jar",
      "type": "mod",
      "sha256": "SHA256_REAL_DE_64_CARACTERES",
      "url": "https://URL-HTTPS-DIRECTA-AL-ARCHIVO"
    }
  ]
}
```

No publiques hashes o URLs de ejemplo. El hash SHA-256 debe corresponder exactamente al archivo descargable. Los archivos grandes deben alojarse como assets de GitHub Releases u otro hosting HTTPS; GitHub Pages sirve el manifiesto, no aloja automáticamente los archivos binarios.

El manifiesto actual tiene `files: []` de forma intencional hasta que se publiquen los archivos descargables. El launcher está protegido para que un manifiesto vacío no borre el contenido instalado.
