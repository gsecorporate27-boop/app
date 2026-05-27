# Corrección Vercel / npm

Esta versión corrige el error de instalación:

`npm error Exit handler never called!`

Cambios aplicados:
- Se eliminó `package-lock.json` porque contenía rutas de registry interno y podía romper `npm install` en Vercel.
- Se fijaron versiones estables de React, Vite, plugin React y lucide-react.
- Se agregó `packageManager: npm@10.9.2` y `engines` para evitar npm 11.
- Se agregó `.npmrc` con `legacy-peer-deps=true`, `audit=false` y `fund=false`.
- Se agregó `vite.config.js`.

En Vercel usa:
- Framework Preset: Vite
- Install Command: `npm install`
- Build Command: `npm run build`
- Output Directory: `dist`

No subas el ZIP como archivo. Descomprímelo y sube los archivos reales a la raíz del repo.
