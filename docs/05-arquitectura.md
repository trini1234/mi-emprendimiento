# Arquitectura de la información — Lash Beauty

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

<!-- Incluye landing, blog, tienda y las páginas obligatorias:
contacto, preguntas frecuentes, términos, privacidad y 404. -->

```text
Inicio (landing)
├── Tienda
│   ├── Pestañas clásicas
│   ├── Pestañas volumen
│   ├── Pestañas de tira
│   ├── Pegamentos y removedores
│   ├── Accesorios y herramientas
│   ├── Detalle de producto
│   └── Carrito
├── Blog
│   ├── Cuidados
│   ├── Tutoriales
│   ├── Tendencias
│   └── Artículo
├── Contacto
├── Preguntas frecuentes
├── Términos y condiciones
├── Política de privacidad
└── Error 404
```

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: compra

```text
Sofía llega al Inicio
→ Entra a la Tienda
→ Busca o filtra por estilo, largo o precio
→ Abre el detalle de un producto
→ Mira fotos y reseñas
→ Elige el modelo
→ Agrega al carrito
→ Revisa el carrito
→ Ingresa sus datos y dirección de envío
→ Elige el método de pago
→ Ve la confirmación de su compra
```

### Flujo 2: contenido

```text
Sofía llega al Inicio
→ Entra al Blog
→ Elige una categoría (cuidados, tutoriales o tendencias)
→ Lee un artículo
→ Ve el producto relacionado al final del artículo
→ Opción A: va a la Tienda para comprarlo
→ Opción B: comparte el artículo o deja sus datos para recibir novedades
```

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de productos

| Categoría | Productos |
|---|---|
| Pestañas clásicas | Pestañas pelo a pelo, set natural, set efecto rímel |
| Pestañas volumen | Volumen ruso, volumen ligero, pestañas efecto gato |
| Pestañas de tira | Tiras naturales, tiras dramáticas, tiras de media pestaña |
| Pegamentos y removedores | Pegamento para pestañas, removedor, primer |
| Accesorios y herramientas | Pinzas, cepillos, pads de gel, kit de aplicación |

### Categorías del blog

| Categoría | Idea de artículo | Necesidad o motivación de la proto-persona | Producto relacionado |
|---|---|---|---|
| Cuidados | Cómo cuidar tus pestañas para que duren más | Quiere que sus pestañas se mantengan bonitas y no gastar de más | Cepillos y kit de cuidado |
| Tutoriales | Cómo aplicar pestañas pelo a pelo en casa paso a paso | Quiere aprender a aplicarlas sola y ahorrar tiempo y dinero | Kit de aplicación y pegamento |
| Tutoriales | Cómo poner pestañas de tira sin que se despeguen | Busca un resultado rápido y fácil para una ocasión especial | Pestañas de tira |
| Tendencias | Estilos de pestañas de moda: natural, gato o volumen | Quiere encontrar el estilo que mejor se ve con sus ojos | Pestañas clásicas y volumen |
| Cuidados | Cómo retirar tus pestañas sin dañar las naturales | Le preocupa cuidar sus pestañas naturales | Removedor |
