# FIRMA_ARQ

Sitio web de una ficticia empresa de arquitectura, realizado con HTML y CSS puros.
El diseño sigue una estética **brutalista**: bordes gruesos, sombras duras, tipografía
en mayúsculas, paleta blanco/negro/rojo y fotografía en blanco y negro.

## Páginas

| Archivo | Descripción |
| --- | --- |
| `html/index.html` | Portada: hero a pantalla completa, marquesina de datos, índice de obras en rejilla y pie. |
| `html/proyectoFirma_Arq.html` | Ficha del proyecto *Sede Central*: portada con metadatos, panorámica, manifiesto, galería técnica y navegación entre proyectos. |

## Estructura

```
ivansanchez-amandajaneiro-p1/
├── css/
│   ├── index.css               # estilos de la portada
│   └── proyectoFirma_Arq.css   # estilos de la ficha de proyecto
├── guia_wireframes/            # wireframes y guía de estilos del proyecto
│   ├── archivografico_1.jpeg
│   ├── archivografico_2.jpeg
│   ├── guia-de-estilos.png
│   └── home.jpeg
├── html/
│   ├── index.html
│   └── proyectoFirma_Arq.html
└── img/
    ├── Cafe.png                # stickers
    ├── Constructor.png
    ├── Edificio.png
    ├── SelloCalidad.png
    ├── favicon.svg
    ├── fig1.PNG                # figuras de la galería
    ├── fig2.PNG
    ├── fig3.PNG
    └── sede.PNG                # imagen panorámica del proyecto
```

## Pruébalo tú mismo

No hay dependencias ni build: es HTML y CSS estáticos. Clona el repositorio y ábrelo
directamente en el navegador.

```bash
git clone https://github.com/corraal15/FIRMA_ARQ
cd FIRMA_ARQ
xdg-open ivansanchez-amandajaneiro-p1/html/index.html
```

> Las rutas de las hojas de estilo son relativas (`../css/...`), así que conviene abrir
> siempre desde el navegador en lugar de arrastrar el `.html` a otra ubicación.

## Detalles técnicos

- **HTML5 semántico**: `header`, `nav`, `main`, `section`, `figure`, `article`, `footer`.
- **CSS con variables** en `:root` (`--black`, `--red`, `--borde`, `--sombra`, `--espacio`)
  para mantener los bordes, sombras y separaciones consistentes.
- **Fotografía en blanco y negro** con `filter: grayscale(100%) contrast(120%)` sobre `img`.
- **Stickers** posicionados con `position: absolute` en cuatro variantes
  (`.sticker--constructor`, `--edificio`, `--sello`, `--cafe`).
- **Tipografías** de Google Fonts: *Inter* para titulares y *JetBrains Mono* para etiquetas.
- **Responsive** mediante media queries: `1100px` y `700px` en la portada;
  `1280px`, `1024px`, `768px` y `640px` en la ficha de proyecto (mallas con
  `grid-template-columns: repeat(n, minmax(0, 1fr))` y `aspect-ratio`).
- **Animaciones** de la marquesina y los stickers, desactivadas con
  `@media (prefers-reduced-motion: reduce)`.
- Las imágenes de la portada vienen de **Unsplash** por URL; las de la ficha de proyecto
  son locales.
