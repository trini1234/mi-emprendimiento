# Spec de diseño —Lash Beauty

> Guía: [Spec de diseño](../evaluacion/guias/fase-2-specs/06-spec-de-diseno.md)

La spec de diseño tiene dos partes:

1. **[`DESIGN.md`](../DESIGN.md)** (en la raíz): tu design system, en el formato que Stitch importa.
2. **Este documento:** tus pantallas, escritas como prompts listos para pegar en Stitch.

**Wireframes en Whimsical:** https://whimsical.com/duocuc91/Nv9J6dfGZdDFiaVf6qMvhW

> Guía de wireframes: [Wireframes](../evaluacion/guias/fase-2-specs/04-wireframes.md)

![Wireframes](img/moodboard.jpg.png)

## Pantallas

<!-- Un prompt por pantalla. Cada uno con: pantalla y dispositivo, objetivo
de tu proto-persona, componentes de arriba hacia abajo (con los nombres de
tu DESIGN.md) y textos y datos reales. -->

### 1. Landing

```text
Pantalla: Landing de Lash Beauty, versión desktop. Usa el design system del proyecto.
Objetivo: Que Sofía entienda en segundos qué ofrece la marca, sienta confianza, llegue rápido a las pestañas que le interesan y deje su correo para recibir un descuento de bienvenida.
Componentes, de arriba hacia abajo:
1. Navbar: logo "Lash Beauty" en cursiva a la izquierda; enlaces "Inicio", "Tienda", "Blog" y "Contacto" al centro; buscador e ícono de carrito a la derecha.
2. Hero: imagen grande de una mirada con pestañas en tonos rosa pastel; título "Tu mirada, siempre impecable"; subtítulo "Pestañas de calidad para que te veas y te sientas increíble"; botón principal "Ver pestañas".
3. Categorías: cuatro círculos con las categorías "Clásicas", "Volumen", "De tira" y "Accesorios".
4. Productos destacados: título "Los favoritos de nuestras clientas" y cuatro tarjetas de producto, cada una con foto, nombre (por ejemplo "Pestañas Natural Glam"), precio ($12.990) y botón "Agregar al carrito".
5. Beneficios: tres íconos con texto: "Calidad profesional", "Envíos a todo Chile" y "Te asesoramos por WhatsApp".
6. Galería de resultados: título "Resultados reales" y cuadrícula de seis fotos de pestañas puestas, con enlace "Síguenos en Instagram".
7. Suscripción: título "Recibe novedades y un 10% de descuento en tu primera compra", campo de correo con placeholder "Tu correo" y botón "Quiero mi descuento".
8. Footer: logo, enlaces "Preguntas frecuentes", "Términos y condiciones", "Política de privacidad", íconos de Instagram y WhatsApp.
```

### 2. Tienda

```text
Pantalla: Tienda de Lash Beauty, versión desktop. Usa el design system del proyecto.
Objetivo: Que Sofía encuentre rápido el producto que busca, compare opciones según su estilo, largo y presupuesto, y las agregue al carrito con facilidad.
Componentes, de arriba hacia abajo:
1. Navbar: logo "Lash Beauty", enlaces "Inicio", "Tienda", "Blog" y "Contacto", buscador e ícono de carrito con contador.
2. Encabezado de página: título "Tienda" y subtítulo "Encuentra las pestañas perfectas para tu mirada".
3. Buscador: campo con placeholder "Buscar por nombre o tipo de pestaña".
4. Filtros laterales: columna a la izquierda con "Categoría" (Clásicas, Volumen, De tira, Accesorios), "Estilo" (Natural, Gato, Dramático), "Largo" (8 mm, 10 mm, 12 mm) y "Precio" (control deslizante), más el botón "Limpiar filtros".
5. Cuadrícula de productos: seis tarjetas en tres columnas, cada una con foto, nombre (por ejemplo "Pestañas Volumen Ruso"), estilo y largo, precio ($14.990) y botón "Agregar al carrito".
6. Paginación: botón "Ver más productos".
7. Footer: logo, enlaces "Preguntas frecuentes", "Términos y condiciones", "Política de privacidad", íconos de Instagram y WhatsApp.
```

### 3. Ficha de producto

```text
Pantalla: Ficha de producto de Lash Beauty, versión desktop. Usa el design system del proyecto.
Objetivo: Que Sofía vea cómo se ven realmente las pestañas, elija el modelo y el largo con seguridad, lea la opinión de otras clientas y agregue el producto al carrito.
Componentes, de arriba hacia abajo:
1. Navbar: logo "Lash Beauty", enlaces "Inicio", "Tienda", "Blog" y "Contacto", buscador e ícono de carrito.
2. Ruta de navegación: "Tienda / Pestañas volumen / Volumen Ruso".
3. Galería de producto: a la izquierda, imagen grande de las pestañas puestas y cuatro miniaturas (una de ellas es un video corto).
4. Información de compra: a la derecha, título "Pestañas Volumen Ruso", precio "$14.990", selector de modelo (Natural, Gato, Dramático), selector de largo (8, 10 y 12 mm), selector de cantidad y botón principal "Agregar al carrito".
5. Detalles desplegables: tres secciones "Descripción", "Cuidados" y "Modo de uso".
6. Reseñas: título "Lo que dicen nuestras clientas", calificación de 4,8 estrellas y tres reseñas cortas con nombre.
7. Productos relacionados: título "También te puede gustar" y cuatro tarjetas de producto.
8. Botón flotante de WhatsApp: "¿Dudas? Escríbenos".
9. Footer: logo, enlaces "Preguntas frecuentes", "Términos y condiciones", "Política de privacidad", íconos de Instagram y WhatsApp.
```

### 4. Carrito

```text
Pantalla: Carrito de Lash Beauty, versión desktop. Usa el design system del proyecto.
Objetivo: Que Sofía revise lo que va a comprar, pueda cambiar cantidades o eliminar productos, vea el total claro y avance a pagar de forma rápida y segura.
Componentes, de arriba hacia abajo:
1. Navbar: logo "Lash Beauty", enlaces "Inicio", "Tienda", "Blog" y "Contacto", buscador e ícono de carrito con contador.
2. Título de página: "Tu carrito".
3. Lista de productos: a la izquierda, dos filas con foto, nombre ("Pestañas Volumen Ruso"), modelo y largo, selector de cantidad (− 1 +), precio ($14.990) y ícono para eliminar.
4. Código de descuento: campo con placeholder "Código de descuento" y botón "Aplicar".
5. Resumen del pedido: a la derecha, tarjeta con "Subtotal", "Envío", "Total" y botón principal "Finalizar compra".
6. Enlace secundario: "Seguir comprando".
7. Mensaje de confianza: "Compra segura y envíos a todo Chile".
8. Footer: logo, enlaces "Preguntas frecuentes", "Términos y condiciones", "Política de privacidad", íconos de Instagram y WhatsApp.
```

### 5. Blog

```text
Pantalla: Blog de Lash Beauty, versión desktop. Usa el design system del proyecto.
Objetivo: Que Sofía aprenda a aplicar y cuidar sus pestañas con consejos fáciles de seguir, encuentre artículos por tema y se suscriba para recibir novedades.
Componentes, de arriba hacia abajo:
1. Navbar: logo "Lash Beauty", enlaces "Inicio", "Tienda", "Blog" y "Contacto", buscador e ícono de carrito.
2. Encabezado de página: título "Blog" y subtítulo "Consejos, tutoriales y tendencias para tu mirada".
3. Categorías: botones "Todos", "Cuidados", "Tutoriales" y "Tendencias".
4. Artículo destacado: imagen grande a la izquierda y a la derecha categoría "Tutoriales", título "Cómo aplicar pestañas pelo a pelo en casa paso a paso", resumen de dos líneas y botón "Leer más".
5. Cuadrícula de artículos: seis tarjetas en tres columnas, cada una con imagen, categoría, título (por ejemplo "Cómo cuidar tus pestañas para que duren más") y enlace "Leer más".
6. Suscripción: título "Recibe consejos y novedades", campo "Tu correo" y botón "Suscribirme".
7. Footer: logo, enlaces "Preguntas frecuentes", "Términos y condiciones", "Política de privacidad", íconos de Instagram y WhatsApp.
```

### 6. Artículo

```text
Pantalla: Artículo del blog de Lash Beauty, versión desktop. Usa el design system del proyecto.
Objetivo: Que Sofía lea un consejo claro y útil, pueda compartirlo con sus amigas, conozca el producto relacionado y llegue fácilmente a comprarlo.
Componentes, de arriba hacia abajo:
1. Navbar: logo "Lash Beauty", enlaces "Inicio", "Tienda", "Blog" y "Contacto", buscador e ícono de carrito.
2. Encabezado del artículo: categoría "Tutoriales", título "Cómo aplicar pestañas pelo a pelo en casa paso a paso" y fecha de publicación.
3. Imagen principal: foto grande de una mirada con pestañas aplicadas.
4. Contenido: introducción, subtítulos numerados ("1. Prepara tus pestañas", "2. Aplica el pegamento", "3. Coloca cada pestaña") y fotos del paso a paso.
5. Botones para compartir: "Compartir en Instagram" y "Compartir por WhatsApp".
6. Producto relacionado: tarjeta con foto, nombre ("Kit de aplicación pelo a pelo"), precio y botón "Comprar".
7. Comentarios: campo "Escribe tu comentario", botón "Publicar" y lista de comentarios.
8. Artículos relacionados: título "Sigue leyendo" y tres tarjetas de artículo.
9. Footer: logo, enlaces "Preguntas frecuentes", "Términos y condiciones", "Política de privacidad", íconos de Instagram y WhatsApp.
```

### Versión mobile (para cada pantalla)

```text
Genera la versión mobile (375px de ancho) de esta pantalla siguiendo la
sección Layout del design system: una sola columna, la navbar se convierte en un menú de hamburguesa con el logo y el carrito visibles, las cuadrículas de productos y artículos pasan a dos columnas (una columna en el blog), los filtros de la tienda se abren con un botón "Filtrar", los botones principales ocupan todo el ancho y el footer se apila en vertical. Mantén la misma paleta, tipografías y textos.
```
