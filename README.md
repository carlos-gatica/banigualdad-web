# banigualdad-web

Sitio de Francisco Villarreal (Asesor de Emprendimiento), migrado desde
Systeme.io a un proyecto Node/Express + EJS, listo para desplegar en Vercel
(mismo flujo que `sitio-particulares`).

## Correr en local

```bash
npm install
npm start
```

Abre http://localhost:3000

## Estructura

```
banigualdad-web/
├── server.js        # Servidor Express
├── views/
│   └── index.ejs    # Tu HTML actual, migrado tal cual (Tailwind vía CDN)
├── public/           # Para futuros assets estáticos (imágenes, etc.)
├── package.json
└── .gitignore
```

## Subir a GitHub y desplegar en Vercel

1. Crea un repo nuevo en GitHub (ej. `banigualdad-web`).
2. Desde esta carpeta:
   ```bash
   git init
   git add .
   git commit -m "Primera versión: migración desde Systeme.io"
   git branch -M main
   git remote add origin https://github.com/<tu-usuario>/banigualdad-web.git
   git push -u origin main
   ```
3. Entra a vercel.com, "Add New Project", importa el repo `banigualdad-web`.
4. Vercel detecta Node automáticamente. No necesitas variables de entorno
   (no hay base de datos ni Resend/CallMeBot en esta versión).
5. Deploy. Cada `git push` a `main` vuelve a desplegar solo, igual que en
   `sitio-particulares`.

## Editar contenido

Todo el contenido (textos, links de WhatsApp, FAQ, colores de marca) está en
`views/index.ejs`. Ábrelo en WebStorm y edita directo — es el mismo HTML de
siempre, solo que ahora vive en un proyecto propio versionado con Git en vez
de estar pegado en Systeme.io.
