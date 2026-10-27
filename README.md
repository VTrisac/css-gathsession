# GathSession · CSS Proyecto 2

Maquetación del diseño 2 de la relación de proyectos de CSS: la landing de *GathSession*, comunidad para organizar proyectos y eventos. Fiel al Figma en escritorio (1920px) y adaptada a pantallas más pequeñas.

## Qué incluye
- Cabecera con logo bicolor y menú con indicador de página activa.
- Titular, texto, botón principal y enlace "Learn More" con flecha animada.
- Tres características con iconos SVG propios.
- Rejilla de cinco fotos en "píldora" con CSS Grid (alturas distintas y desplazamiento de la tercera columna), cada una con su color de fondo y efecto `:hover`.
- Anillos decorativos de fondo hechos solo con CSS.
- Responsive: en tablet las fotos pasan debajo del texto y en móvil se muestran en dos columnas, sin scroll horizontal.

## Estructura
```
index.html
scss/   _fonts, _variables, _base, _components, _layout, _responsive, styles.scss
css/styles.css   (compilado)
assets/img (fotos recortadas en webp), assets/fonts
```

## Sass
Los estilos se escriben en `scss/` (parciales para variables, base, componentes, layout y responsive) y se compilan a `css/styles.css`, que es el que enlaza el HTML. El CSS compilado ya va incluido, así que la web funciona tal cual. Para recompilar:
```bash
npx sass scss/styles.scss css/styles.css          # una vez
npx sass --watch scss/styles.scss css/styles.css  # mientras editas
```
(o la extensión *Live Sass Compiler* de VS Code).

## Fuentes
Alojadas en `assets/fonts/` (woff2, subconjunto latino) y cargadas con `@font-face`, sin depender de Google Fonts.

## Ver en local
Basta con abrir `index.html` en el navegador o usar Live Server.

## Publicar en GitHub Pages
1. Crea un repositorio público y sube el contenido de esta carpeta a la rama `main`.
2. Settings → Pages → *Deploy from a branch* → `main` / `(root)` → Save.
3. En un minuto estará en `https://<tu-usuario>.github.io/<repositorio>/`. Ese enlace es el que se entrega.
