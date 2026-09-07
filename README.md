# City-Escape Room: Madrid — landing page

Landing bilingüe (ES/EN) para **City-Escape Room: Madrid**, optimizada para SEO,
lista para publicarse en GitHub Pages con dominio propio
`city-escape-room-madrid.devcodelight.com`.

## Estructura

```
/
├── index.html          → versión en español (raíz, idioma por defecto)
├── en/
│   └── index.html      → versión en inglés
├── assets/
│   ├── style.css
│   └── script.js
├── sitemap.xml
├── robots.txt
└── CNAME
```

## Publicar en GitHub Pages

1. Crea un repositorio nuevo (público), p. ej. `city-escape-room-madrid-landing`.
2. Sube todo el contenido de esta carpeta a la raíz del repo (rama `main`).
   El archivo `CNAME` ya incluye `city-escape-room-madrid.devcodelight.com`,
   no lo borres.
3. En GitHub → **Settings → Pages**: Source = `Deploy from a branch`,
   branch `main`, carpeta `/ (root)`.
4. En el DNS de `devcodelight.com`, añade un registro **CNAME**:
   - Host: `city-escape-room-madrid`
   - Valor: `usuario.github.io` (tu usuario/organización de GitHub)
5. En **Settings → Pages**, confirma el dominio personalizado y activa
   **Enforce HTTPS** cuando esté disponible (puede tardar unos minutos tras
   la propagación DNS).

## Notas de contenido

- Textos, capturas, tráiler y valoración (4,8★ / 54 reseñas) tomados de la ficha
  actual de Google Play. El tráiler se sirve directo desde el CDN de Google
  (`play-games.googleusercontent.com`) vía `<video>` con controles nativos.
- La sección de FAQ evita afirmar cosas que la ficha de Play Store no confirma
  (p. ej. si el juego usa geolocalización real): se queda en lo que la propia
  descripción dice.
- Si prefieres no depender del CDN de Google a largo plazo, descarga
  capturas/tráiler/icono y sírvelos desde `/assets/`, actualizando las rutas
  en ambos HTML.

## Notas técnicas

- Sin frameworks ni build step.
- Tipografías: Bebas Neue (titulares, tono "expediente de misión") + Work Sans
  (cuerpo), vía Google Fonts.
- Identidad visual distinta a la landing de Fuentes de Agua a propósito: aquí
  el motivo es un "tablero de investigación" (hilo rojo conectando los 5
  monumentos de la ruta) en vez de líneas topográficas.
- Accesible: foco visible, `prefers-reduced-motion` respetado, skip-link, alt
  text descriptivo.
