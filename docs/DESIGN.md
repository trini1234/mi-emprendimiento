---
version: alpha
name: "[Lash Beauty]"
description: "[Lash Beauty es un emprendimiento de belleza especializado en extensiones de pestañas personalizadas, ofreciendo servicios de calidad para realzar la mirada de sus clientas.]"
# Guía: evaluacion/guias/fase-2-specs/06-spec-de-diseno.md
# Reemplaza TODOS los valores de ejemplo por los de tu paleta y tipografía
# (docs/08-color-tipografia.md). Los HEX van siempre entre comillas.
# Valida con: npx @google/design.md lint DESIGN.md

colors:
  primary: "#C2185B"
  primary-hover: "#A0134A"
  on-primary: "#FFFFFF"
  secondary: "#E8D5CC"
  on-secondary: "#1A1A1A"
  tertiary: "#F2B8C6"
  on-tertiary: "#1A1A1A"
  neutral: "#FFF7F8"
  surface: "#FFFFFF"
  on-surface: "#1A1A1A"
  on-surface-variant: "#5C5C5C"
  disabled: "#D6D6D6"
  on-disabled: "#4A4A4A"
  error: "#C62828"
  success: "#2E7D32"
typography:
  headline-display:
    fontFamily: "Playfair Display"
    fontSize: 48px
    fontWeight: 700
    lineHeight: 1.1
  headline-lg:
    fontFamily: "Playfair Display"
    fontSize: 36px
    fontWeight: 600
    lineHeight: 1.2
  headline-md:
    fontFamily: "Playfair Display"
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
  body-md:
    fontFamily: "Poppins"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label-md:
    fontFamily: "Poppins"
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1
rounded:
  md: 12px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-primary-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  card-product:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  tag-offer:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    rounded: "{rounded.full}"
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 12px 14px
  message-error:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.error}"
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
  text-secondary:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface-variant}"
---

# Lash Beauty – Design system

## Overview

Lash Beauty es una marca de pestañas y belleza para mujeres jóvenes como Sofía, que quieren verse bien, aprender a cuidar sus pestañas y comprar de forma rápida y segura. La interfaz debe transmitir **confianza, calma, feminidad, elegancia y cercanía**, las mismas sensaciones del moodboard: rosa pastel, beige, negro suave, detalles con brillo y una tipografía elegante. El diseño es limpio, ordenado y luminoso, con mucho espacio en blanco, para que el producto y las fotos de pestañas sean los protagonistas.

## Colors

- **Primary (#C2185B, rosa frambuesa):** botones principales, enlaces, íconos activos y llamados a la acción como "Agregar al carrito" y "Finalizar compra". No se usa como fondo de secciones grandes.
- **Primary-hover (#A0134A):** estado hover y active de los botones principales.
- **Secondary (#E8D5CC, beige rosado):** fondos de tarjetas de producto y secciones alternas como colecciones y productos destacados.
- **Tertiary (#F2B8C6, rosa pastel):** etiquetas de oferta, detalles decorativos y bloques destacados como el hero y la suscripción.
- **Neutral (#FFF7F8):** fondo general de todas las páginas.
- **Surface (#FFFFFF):** campos de formulario, tarjetas de reseñas y botones secundarios.
- **On-surface (#1A1A1A):** títulos, párrafos y footer.
- **On-surface-variant (#5C5C5C):** textos secundarios como fechas, descripciones cortas y placeholders.
- **Disabled / On-disabled (#D6D6D6 / #4A4A4A):** botones o campos no disponibles, por ejemplo un producto sin stock.
- **Error (#C62828):** mensajes de error en formularios y carrito.
- **Success (#2E7D32):** confirmaciones como suscripción lista o compra realizada.

**Dónde NO se usa:** el rosa frambuesa no va en párrafos largos ni en fondos grandes, el rosa pastel nunca lleva texto blanco, y el rojo y el verde se reservan solo para mensajes de estado.

## Typography

- **Títulos:** Playfair Display (serif elegante), en línea con la cursiva del logo "Lash Beauty".
- **Textos y botones:** Poppins (sans-serif limpia, fácil de leer en celular).
- **Escala desktop:** h1 48 px (700), h2 36 px (600), h3 24 px (600), párrafo 16 px (400) y botón 16 px (600).
- **Escala mobile:** h1 32 px, h2 26 px, h3 20 px, párrafo 16 px y botón 15 px.
- El texto de párrafo nunca baja de 16 px, para que Sofía lea cómoda desde el celular.

## Layout

- **Ancho máximo:** 1200 px, centrado. Márgenes laterales de 16 px en mobile, 24 px en tablet y 40 px en desktop.
- **Espaciado:** escala basada en 4 px (xs 4, sm 8, md 16, lg 24, xl 32, 2xl 48, 3xl 64). Entre secciones se usa 2xl o 3xl.
- **Mobile (hasta 767 px):** una columna. La navbar se reduce al logo, el carrito y un menú de hamburguesa. Los productos van en 2 columnas y los artículos del blog en 1. Los filtros de la tienda se abren con un botón "Filtrar". Los botones principales ocupan todo el ancho y el footer se apila en vertical.
- **Tablet (768 a 1023 px):** los productos y artículos van en 3 columnas, el menú se muestra completo y los filtros se despliegan sobre la cuadrícula.
- **Desktop (desde 1024 px):** menú completo en una fila, productos en 3 o 4 columnas, filtros en una columna lateral a la izquierda y, en la ficha de producto, galería a la izquierda y datos de compra a la derecha.
- **Imágenes:** siempre con proporción fija (4:5 en productos, 16:9 en banners y artículos) y con texto alternativo.

## Elevation & Depth

La jerarquía se marca con **sombras suaves y bordes finos**, nunca con sombras duras.

- **Tarjetas de producto y artículo:** sombra ligera (0 2px 8px con 8 % de negro) y, al pasar el cursor, una sombra un poco mayor (0 6px 16px).
- **Navbar:** borde inferior de 1 px en beige y sombra muy sutil al hacer scroll.
- **Botón flotante de WhatsApp:** sombra más marcada para que siempre se vea por encima del contenido.
- **Campos de formulario:** borde de 1 px que pasa a rosa frambuesa al enfocarse.
- Los bloques de color (beige y rosa pastel) también crean profundidad sin necesidad de sombras.

## Shapes

- **Botones y etiquetas:** totalmente redondeados (pill, 9999 px), para transmitir dulzura.
- **Tarjetas, campos de formulario e imágenes:** esquinas redondeadas de 12 px.
- **Círculos de categorías:** forma circular completa, como en las colecciones del moodboard.
- Se evitan las esquinas rectas y los ángulos agudos.

## Components

### Navbar
Logo "Lash Beauty" a la izquierda, enlaces Inicio, Tienda, Blog y Contacto al centro, y buscador y carrito a la derecha. Fondo `surface`, texto `on-surface`. El enlace de la página actual se marca en `primary`. El carrito muestra un contador con la cantidad de productos. En mobile se convierte en menú de hamburguesa.

### Hero
Imagen grande de una mirada con pestañas, título en `headline-display`, subtítulo en `body-md` y un único botón `button-primary`. Fondo en `tertiary`. El texto siempre debe leerse sobre la imagen o sobre un bloque de color.

### button-primary
Fondo `primary`, texto `on-primary`, forma pill y padding 12px 24px. Hay un solo botón principal por bloque.
- **Hover / active:** cambia a `primary-hover` (`button-primary-hover`).
- **Disabled:** usa `disabled` y `on-disabled` (`button-primary-disabled`) y no responde al clic.
- **Focus:** anillo visible de 2 px en `primary`.

### button-secondary
Fondo `surface`, texto y borde `primary`, forma pill. Se usa para acciones secundarias como "Seguir comprando" o "Leer más". Nunca compite con el botón principal en la misma vista.

### card-product
Fondo `secondary`, esquinas de 12 px y padding de 16 px. Contiene, en este orden: foto, nombre, estilo y largo, precio y botón "Agregar al carrito".
- El precio siempre es visible.
- El nombre ocupa máximo 2 líneas y se corta con puntos suspensivos.
- La foto mantiene proporción 4:5.
- Al pasar el cursor, la tarjeta sube levemente y aumenta la sombra.
- Si hay oferta, se muestra un `tag-offer` en la esquina superior de la foto.

### tag-offer
Etiqueta en forma de pill con fondo `tertiary` y texto `on-tertiary`. Texto corto, como "-10%" o "Nuevo". Máximo una etiqueta por tarjeta.

### input-field
Fondo `surface`, texto `on-surface`, `body-md`, esquinas de 12 px y padding 12px 14px. Siempre lleva una etiqueta o placeholder claro, como "Tu correo". Al enfocarse, el borde pasa a `primary`. Si hay un error, el borde y el mensaje cambian a `error`.

### message-error
Texto en `error` sobre `surface`, debajo del campo afectado, con un mensaje claro y amable como "Revisa tu correo, parece incompleto". Nunca se usa solo el color: siempre va acompañado de texto.

### Filtros de la tienda
Columna lateral en desktop y botón "Filtrar" en mobile. Contiene Categoría, Estilo, Largo y Precio, más el botón "Limpiar filtros". Los filtros activos se resaltan en `primary`.

### Tarjeta de artículo
Imagen, categoría, título en máximo 2 líneas y enlace "Leer más". Fondo `surface` y esquinas de 12 px.

### Formulario de suscripción
Título, campo `input-field` con el placeholder "Tu correo" y `button-primary` con el texto "Quiero mi descuento". Al enviarse, muestra un mensaje de confirmación en `success`.

### Botón flotante de WhatsApp
Visible en las páginas de tienda y ficha de producto, abajo a la derecha, con el texto "¿Dudas? Escríbenos".

### Footer
Fondo `on-surface` con texto blanco. Logo, enlaces a Preguntas frecuentes, Términos y condiciones y Política de privacidad, e íconos de Instagram y WhatsApp. En mobile se apila en vertical.

## Do's and Don'ts

**Do**
- Usar `button-primary` solo para la acción más importante de cada vista.
- Mantener el contraste mínimo de 4,5:1 entre texto y fondo.
- Mostrar siempre el precio de forma visible y clara.
- Usar fotos reales de pestañas puestas para dar confianza.
- Dejar mucho espacio en blanco y mantener el diseño ordenado.
- Usar un tono amable y cercano en todos los textos.
- Probar cada pantalla primero en mobile.

**Don't**
- No usar texto blanco sobre rosa pastel ni sobre beige.
- No poner más de un botón principal en el mismo bloque.
- No usar rojo o verde fuera de los mensajes de error y éxito.
- No usar más de dos familias tipográficas.
- No usar sombras duras ni esquinas rectas.
- No bajar el tamaño del párrafo de 16 px.
- No comunicar errores o estados solo con color.
