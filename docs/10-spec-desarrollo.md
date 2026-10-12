# Spec de desarrollo — Lash Beauty

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.
En la carpeta stitch/ está el código exportado de Stitch de cada pantalla.
Construye el sitio siguiendo exactamente docs/10-spec-desarrollo.md:
solo HTML y CSS, la estructura de archivos y la navegación definidas,
las variables de :root con los valores de DESIGN.md y la estructura
semántica de cada página. Usa el código de Stitch solo como referencia
visual. Al terminar, revisa cada criterio de aceptación y dime cuáles
se cumplen y cuáles no.
```


## 1. Estructura de archivos

```text
mi-emprendimiento/
├── index.html                  (landing)
├── tienda.html
├── producto.html               (ficha de producto)
├── carrito.html
├── blog.html
├── articulo.html
├── contacto.html
├── preguntas-frecuentes.html
├── terminos.html
├── privacidad.html
├── 404.html
├── css/
│   ├── variables.css           (:root con los tokens de DESIGN.md)
│   ├── base.css                (reset, tipografía, layout general)
│   ├── components.css          (navbar, botones, tarjetas, formularios, footer)
│   └── pages.css               (estilos propios de cada página)
├── img/                        (fotos de pestañas, logo, íconos)
├── stitch/                     (código exportado de Stitch, solo referencia)
└── docs/                       (documentación del proyecto)
```

## 2. Páginas y navegación

| Desde | Elemento | Lleva a |
|---|---|---|
| Todas las páginas | Logo "Lash Beauty" | index.html |
| Todas las páginas | Enlace "Inicio" del menú | index.html |
| Todas las páginas | Enlace "Tienda" del menú | tienda.html |
| Todas las páginas | Enlace "Blog" del menú | blog.html |
| Todas las páginas | Enlace "Contacto" del menú | contacto.html |
| Todas las páginas | Ícono de carrito | carrito.html |
| Todas las páginas | Enlace "Preguntas frecuentes" del footer | preguntas-frecuentes.html |
| Todas las páginas | Enlace "Términos y condiciones" del footer | terminos.html |
| Todas las páginas | Enlace "Política de privacidad" del footer | privacidad.html |
| Todas las páginas | Ícono de Instagram del footer | Perfil de Instagram de la marca (enlace externo, abre en pestaña nueva) |
| Todas las páginas | Ícono y botón de WhatsApp | Chat de WhatsApp de la marca (enlace externo, abre en pestaña nueva) |
| index.html | Botón "Ver pestañas" del hero | tienda.html |
| index.html | Círculos de categorías | tienda.html |
| index.html | Botón "Agregar al carrito" de productos destacados | carrito.html |
| index.html | Tarjeta de producto destacado | producto.html |
| index.html | Enlace "Síguenos en Instagram" | Perfil de Instagram de la marca (externo) |
| tienda.html | Tarjeta de producto | producto.html |
| tienda.html | Botón "Agregar al carrito" | carrito.html |
| producto.html | Botón "Agregar al carrito" | carrito.html |
| producto.html | Tarjeta de producto relacionado | producto.html |
| carrito.html | Botón "Finalizar compra" | carrito.html (prototipo visual, sin pago real) |
| carrito.html | Enlace "Seguir comprando" | tienda.html |
| blog.html | Botones de categoría | blog.html (prototipo visual, sin filtrado real) |
| blog.html | Tarjeta de artículo y "Leer más" | articulo.html |
| articulo.html | Botón "Comprar" del producto relacionado | producto.html |
| articulo.html | Tarjetas de artículos relacionados | articulo.html |
| articulo.html | Enlace "Volver al blog" | blog.html |
| 404.html | Botón "Volver al inicio" | index.html |

## 3. Estructura semántica

Todas las páginas comparten esta base:

```text
<body>
  <header>
    <nav> logo + enlaces + buscador + carrito </nav>
  </header>
  <main> ... contenido de la página ... </main>
  <footer> logo + enlaces legales + redes </footer>
</body>
```

Lo que va dentro de `<main>` en cada página:

- **index.html:** `<section>` hero, `<section>` categorías, `<section>` productos destacados, `<section>` beneficios, `<section>` galería de resultados y `<section>` suscripción. Cada sección con su `<h2>` (el `<h1>` es el título del hero).
- **tienda.html:** `<h1>` "Tienda", `<aside>` con los filtros (`<form>` con `<fieldset>` y `<legend>`) y `<section>` con las tarjetas de producto. Cada tarjeta es un `<article>`.
- **producto.html:** `<section>` galería con `<figure>` e `<img>`, `<section>` información de compra con `<h1>`, precio y `<form>`, `<section>` detalles, `<section>` reseñas (cada reseña es un `<article>`) y `<section>` productos relacionados.
- **carrito.html:** `<h1>` "Tu carrito", `<section>` lista de productos (cada uno un `<article>`) y `<aside>` con el resumen del pedido.
- **blog.html:** `<h1>` "Blog", `<nav>` de categorías, `<article>` destacado y `<section>` con las tarjetas de artículos (cada una un `<article>`).
- **articulo.html:** un `<article>` con `<header>` (categoría, `<h1>`, `<time>`), `<figure>` de la imagen principal y secciones con `<h2>`. Después, `<aside>` con el producto relacionado, `<section>` de comentarios y `<section>` de artículos relacionados.
- **contacto.html:** `<h1>`, `<form>` con campos de nombre, correo y mensaje, y datos de contacto.
- **preguntas-frecuentes.html, terminos.html y privacidad.html:** `<h1>` y `<section>` con un `<h2>` por tema.
- **404.html:** `<h1>` "Página no encontrada", un párrafo amable y un botón para volver al inicio.

## 4. Organización del CSS

```css
:root {
  /* Colores (DESIGN.md) */
  --color-primary: #C2185B;
  --color-primary-hover: #A0134A;
  --color-on-primary: #FFFFFF;
  --color-secondary: #E8D5CC;
  --color-on-secondary: #1A1A1A;
  --color-tertiary: #F2B8C6;
  --color-on-tertiary: #1A1A1A;
  --color-neutral: #FFF7F8;
  --color-surface: #FFFFFF;
  --color-on-surface: #1A1A1A;
  --color-on-surface-variant: #5C5C5C;
  --color-disabled: #D6D6D6;
  --color-on-disabled: #4A4A4A;
  --color-error: #C62828;
  --color-success: #2E7D32;

  /* Tipografía */
  --font-heading: "Playfair Display", serif;
  --font-body: "Poppins", sans-serif;
  --fs-h1: 48px;
  --fs-h2: 36px;
  --fs-h3: 24px;
  --fs-body: 16px;
  --fw-heading: 600;
  --fw-body: 400;
  --fw-label: 600;
  --lh-heading: 1.2;
  --lh-body: 1.6;

  /* Radios */
  --radius-md: 12px;
  --radius-full: 9999px;

  /* Espaciado */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;

  /* Layout */
  --max-width: 1200px;
}
```

**Nombres de clases** (en minúsculas y con guiones): `.navbar`, `.hero`, `.btn`, `.btn-primary`, `.btn-secondary`, `.card-product`, `.card-article`, `.tag-offer`, `.input-field`, `.message-error`, `.filters`, `.footer`, `.whatsapp-float`.

**Breakpoints** (mobile first, con `min-width`):

```css
/* Mobile: estilos base, hasta 767px */
@media (min-width: 768px)  { /* Tablet: 3 columnas, menú completo */ }
@media (min-width: 1024px) { /* Desktop: filtros laterales, 3 o 4 columnas */ }
```

Orden de carga en cada página: `variables.css`, `base.css`, `components.css`, `pages.css`. Las fuentes se cargan desde Google Fonts en el `<head>`.

## 5. Criterios de aceptación

**Navegación**
- [ ] El logo y el menú aparecen en todas las páginas y llevan a los destinos de la tabla de la sección 2.
- [ ] Ningún enlace interno lleva a una página que no existe.
- [ ] Los enlaces de Instagram y WhatsApp abren en una pestaña nueva.
- [ ] La página 404 existe y tiene un botón para volver al inicio.
- [ ] La página actual se marca en el menú con el color primario.

**Funcionalidades**
- [ ] La landing muestra hero, categorías, productos destacados, beneficios, galería y formulario de suscripción.
- [ ] La tienda muestra el buscador, los filtros y la cuadrícula de productos.
- [ ] La ficha de producto muestra galería, selector de modelo y largo, y el botón "Agregar al carrito".
- [ ] El carrito muestra la lista de productos y el resumen con subtotal, envío y total.
- [ ] El blog muestra las categorías, el artículo destacado y la cuadrícula de artículos.
- [ ] El artículo muestra botones para compartir, producto relacionado y comentarios.
- [ ] El botón de WhatsApp es visible en la tienda y en la ficha de producto.
- [ ] Las funcionalidades que son prototipo visual están marcadas como tal en `04-tecnologias.md`.

**Diseño**
- [ ] Todos los colores salen de las variables de `:root`, sin colores escritos a mano.
- [ ] Los títulos usan Playfair Display y los textos y botones usan Poppins.
- [ ] Los botones y etiquetas tienen forma de pill y las tarjetas e inputs tienen esquinas de 12 px.
- [ ] Hay un solo botón primario por bloque.
- [ ] El precio siempre es visible en las tarjetas de producto, y el nombre ocupa máximo 2 líneas.
- [ ] Los botones tienen estados hover y disabled definidos.

**Responsive**
- [ ] En mobile (hasta 767 px) hay una sola columna y la navbar se convierte en menú de hamburguesa.
- [ ] En mobile la tienda muestra 2 productos por fila y el blog muestra 1 artículo por fila.
- [ ] En mobile los filtros se abren con un botón "Filtrar".
- [ ] En tablet (768 a 1023 px) los productos y artículos se muestran en 3 columnas.
- [ ] En desktop (desde 1024 px) los filtros van en una columna lateral.
- [ ] No hay scroll horizontal en ningún tamaño de pantalla.

**Accesibilidad y publicación**
- [ ] Todas las imágenes tienen el atributo `alt` con una descripción útil.
- [ ] Cada página tiene un solo `<h1>` y los títulos siguen un orden lógico.
- [ ] Cada página usa `header`, `nav`, `main` y `footer`.
- [ ] Todos los campos de formulario tienen `<label>` o texto asociado.
- [ ] El contraste entre texto y fondo es de al menos 4,5:1.
- [ ] Cada página tiene `<title>` y `<meta name="viewport">`.
- [ ] El sitio está publicado en GitHub Pages y el enlace funciona.
