# Publicar los documentos legales con GitHub Pages

Esta carpeta `docs/` contiene las páginas legales listas (`index.html`, `privacy.html`,
`terms.html`, `delete.html`) en español e inglés. Publicarlas es gratis y toma 2 minutos.

## Pasos

1. Sube el proyecto a un repositorio de **GitHub** (si aún no lo tienes):
   ```bash
   cd "/Users/franciscoarriagavelasco/Documents/My coding projects/NFCproject"
   git init && git add . && git commit -m "NFC sticker"
   # crea el repo en github.com (ej. "nfc-sticker") y luego:
   git remote add origin https://github.com/TU_USUARIO/nfc-sticker.git
   git branch -M main && git push -u origin main
   ```
2. En GitHub: **Settings → Pages**.
3. En "Build and deployment" → Source: **Deploy from a branch**.
4. Branch: **main** y carpeta: **/docs** → **Save**.
5. Espera ~1 minuto. Tus páginas quedarán en:

   ```
   https://TU_USUARIO.github.io/nfc-sticker/privacy.html
   https://TU_USUARIO.github.io/nfc-sticker/terms.html
   https://TU_USUARIO.github.io/nfc-sticker/delete.html
   ```

## Después de publicar

1. Pega esas 3 URLs en **`src/legal.ts`** (reemplaza las de `example.com`):
   ```ts
   export const PRIVACY_URL = 'https://TU_USUARIO.github.io/nfc-sticker/privacy.html';
   export const TERMS_URL   = 'https://TU_USUARIO.github.io/nfc-sticker/terms.html';
   export const DELETE_URL  = 'https://TU_USUARIO.github.io/nfc-sticker/delete.html';
   ```
2. Usa esas mismas URLs en las consolas:
   - **Google Play** → Política de privacidad (privacy) y Eliminación de cuenta (delete).
   - **App Store Connect** → Privacy Policy URL (privacy) y, si quieres EULA propia, Terms.

> Nota: si tu repo es privado, GitHub Pages requiere cuenta de pago para servirlo; usa un repo
> **público** (o solo sube la carpeta `docs/` a un repo público aparte) para que las URLs sean
> accesibles, que es lo que exigen las tiendas.
