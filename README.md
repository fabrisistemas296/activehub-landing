# ActiveHub — Landing page

Landing estática de ActiveHub: **HTML + CSS puro**, sin build, sin dependencias y sin JavaScript.

```
activehub-landing/
├── index.html      # la página
├── styles.css      # estilos (colores y tipografías de la marca)
├── vercel.json     # config de Vercel (URLs limpias, caché, headers)
└── assets/         # favicon e imágenes (WebP)
```

## Verla en local

Abrí `index.html` en el navegador (las rutas son relativas), o levantá un servidor:

```bash
python3 -m http.server 8000   # http://localhost:8000
```

## Desplegar en Vercel

**Desde la web:** New Project → importar el repo → *Root Directory*: `activehub-landing` →
*Framework Preset*: **Other** → sin Build Command ni Output Directory → Deploy.

**Desde la CLI:**

```bash
npm i -g vercel
cd activehub-landing
vercel          # preview
vercel --prod   # producción
```

## Antes de publicar

Los botones que llevan a la aplicación (Iniciar sesión, Registrarse, Manual, Ayuda) tienen el
atributo `data-app-link` y apuntan a `https://activehub-app.vercel.app`, que es un valor
provisorio. Reemplazalo por la URL real del frontend:

```bash
sed -i 's#https://activehub-app.vercel.app#https://TU-URL-REAL#g' index.html
```
