# Spec de desarrollo — Elysa

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente

Este prompt se utilizará para iniciar la etapa de código con el asistente de IA (Antigravity o Claude Code):

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.
En la carpeta stitch/ está el código exportado de Stitch de cada pantalla como referencia visual.
Construye el sitio de Elysa siguiendo exactamente docs/10-spec-desarrollo.md:
utiliza exclusivamente HTML5 semántico y CSS3 puro (sin frameworks externos ni Tailwind), respetando
la estructura de archivos, la navegación entre páginas y los tokens de diseño definidos en :root
a partir de DESIGN.md. Al terminar la implementación, valida cada uno de los criterios de aceptación
indicando cuáles se cumplen exitosamente y cuáles requieren ajustes.
```

---

## 1. Estructura de archivos y carpetas

```text
elysa-bienestar/
├── index.html                  ← Landing page principal
├── tienda.html                 ← Catálogo general de terapias y productos
├── producto.html               ← Ficha de detalle de servicio o producto (Péndulo Hebreo)
├── carrito.html                ← Carrito de compras, cálculo de despacho y reserva
├── blog.html                   ← Catálogo de artículos y reflexiones holísticas
├── articulo.html               ← Artículo individual ("Flores de Bach para el insomnio...")
├── sobre-mi.html               ← Historia, enfoque y certificaciones de la terapeuta
├── contacto.html               ← Formulario de contacto y canal directo a WhatsApp
├── faq.html                    ← Preguntas frecuentes sobre sesiones y modalidades
├── terminos.html               ← Términos, condiciones y políticas de reprogramación
├── privacidad.html             ← Política de privacidad y tratamiento de datos
├── 404.html                    ← Página de error amigable con retorno al inicio
├── DESIGN.md                   ← Design system oficial del proyecto
├── css/
│   └── styles.css              ← Estilos globales, variables :root y componentes
├── img/
│   ├── servicios/              ← Fotografías de terapias (Reiki, Tameana, Péndulo, Tarot)
│   ├── productos/              ← Fotografías de esencias florales, brumas y cuarzos
│   ├── blog/                   ← Imágenes de cabecera de artículos
│   └── ui/                     ← Logotipo, íconos SVG y avatar de la terapeuta
├── stitch/                     ← Código exportado desde Google Stitch (solo referencia visual)
└── docs/                       ← Documentación y especificaciones del proyecto
```

---

## 2. Páginas y navegación

### Elementos transversales

* **Navbar global (en todas las páginas):**
  * Logotipo de Elysa con enlace a `index.html`.
  * Enlaces de navegación: Inicio (`index.html`), Terapias y Tienda (`tienda.html`), Blog (`blog.html`), Sobre Elysa (`sobre-mi.html`), Contacto (`contacto.html`).
  * Botón secundario `button-secondary`: "WhatsApp directo" con enlace a chat `https://wa.me/56912345678`.
  * Ícono de carrito con contador badge numérico con enlace a `carrito.html`.
* **Footer global (en todas las páginas):**
  * Resumen de la propuesta de valor y ubicación (Providencia, Santiago y atención Online).
  * Enlaces a páginas secundarias: Preguntas Frecuentes (`faq.html`), Términos y Condiciones (`terminos.html`), Política de Privacidad (`privacidad.html`).
  * Enlaces a redes sociales de Elysa (`https://instagram.com/elysa.bienestar`).
  * Copyright y nota de consentimiento terapéutico informado.

### Tabla de navegación entre pantallas

| Desde | Elemento interactivo | Lleva a | Propósito en el flujo del usuario |
|---|---|---|---|
| `index.html` | Botón `button-primary` "Explorar terapias" en Hero | `tienda.html` | Permite a Valentina descubrir el catálogo completo de terapias |
| `index.html` | Botón `button-secondary` "Agendar por WhatsApp" en Hero | `https://wa.me/56912345678` | Canal directo para resolver dudas inmediatas |
| `index.html` | Botón `button-primary` "Ver detalles" en cada `card-product` | `producto.html` | Ingreso a la ficha individual de la terapia destacada |
| `index.html` | Formulario de leads "Descargar Guía de Bienestar" | Confirmación modal / descarga directa de PDF | Captación de correo y entrega de 10% de descuento |
| `tienda.html` | Chips de categoría ("Terapias Energéticas", "Esencias", etc.) | Filtro dinámico en `tienda.html` | Filtra los productos sin recargar la página |
| `tienda.html` | Botón `button-primary` "Ver detalles / Reservar" | `producto.html` | Acceso a la ficha específica de la terapia o producto seleccionado |
| `tienda.html` | Botón `button-secondary` "¿Dudas? Escríbenos por WhatsApp" | `https://wa.me/56912345678` | Asistencia personalizada para consultantes indecisos |
| `producto.html` | Botón `button-primary` "Reservar y agregar al carrito" | `carrito.html` | Incorpora la terapia con la modalidad elegida al carrito |
| `producto.html` | Botón `button-secondary` "Consultar dudas por WhatsApp" | `https://wa.me/56912345678` | Coordinación de horarios específicos con la terapeuta |
| `producto.html` | Fila de terapias afines (`card-product`) | `producto.html` | Recomendación cruzada de terapias complementarias |
| `carrito.html` | Botón `button-secondary` "Explorar más servicios" | `tienda.html` | Permite volver al catálogo para sumar productos adicionales |
| `carrito.html` | Botón `button-primary` "Continuar con el pago y confirmación" | Pasarela segura / WhatsApp | Cierre de orden de compra o agendamiento |
| `blog.html` | Tarjeta destacada `card-article` y artículos de grilla | `articulo.html` | Lectura completa del artículo informativo |
| `articulo.html` | Tarjeta banner `card-product` ("Fórmula Flores de Bach") | `producto.html` | Conversión contextual desde el contenido hacia la tienda |
| `articulo.html` | Botón para compartir por WhatsApp | `https://api.whatsapp.com/send?text=...` | Viralización de contenido útil para la salud mental |
| `404.html` | Botón `button-primary` "Volver al inicio" | `index.html` | Recuperación fluida frente a URLs incorrectas |

---

## 3. Estructura semántica

Cada página HTML5 utiliza elementos semánticos estándar para asegurar óptima accesibilidad, navegación por teclado y posicionamiento en buscadores:

### `index.html` (Landing page)
```html
<header>
  <!-- Barra de navegación global con logo, menú y acceso al carrito -->
  <nav class="navbar"> ... </nav>
</header>
<main>
  <!-- Hero con propuesta de valor, llamado a la acción e imagen cálida -->
  <section class="hero"> ... </section>
  <!-- Diferenciales de atención (cercanía, modalidades, transparencia) -->
  <section class="features"> ... </section>
  <!-- Servicios y terapias destacadas -->
  <section class="featured-services">
    <h2>Terapias para restaurar tu vitalidad</h2>
    <div class="services-grid">
      <article class="card-product"> ... </article>
    </div>
  </section>
  <!-- Captación de leads con guía gratuita descargable -->
  <section class="lead-capture">
    <form class="lead-form"> ... </form>
  </section>
  <!-- Testimonios de consultantes -->
  <section class="testimonials"> ... </section>
</main>
<footer class="footer"> ... </footer>
```

### `tienda.html` (Catálogo general)
```html
<header>
  <nav class="navbar"> ... </nav>
</header>
<main>
  <section class="catalog-header">
    <h1>Terapias y Bienestar Natural</h1>
    <div class="search-bar">
      <input type="search" class="input-field" placeholder="Buscar por síntoma...">
    </div>
  </section>
  <div class="catalog-layout">
    <aside class="filters-sidebar">
      <fieldset class="filter-group"> ... </fieldset>
    </aside>
    <section class="products-grid">
      <article class="card-product"> ... </article>
    </section>
  </div>
  <aside class="help-banner"> ... </aside>
</main>
<footer class="footer"> ... </footer>
```

### `producto.html` (Ficha de terapia / producto)
```html
<header>
  <nav class="navbar"> ... </nav>
</header>
<main>
  <nav aria-label="Migas de pan" class="breadcrumbs"> ... </nav>
  <article class="product-detail">
    <section class="product-gallery"> ... </section>
    <section class="product-info">
      <span class="badge">Presencial u Online</span>
      <h1>Péndulo Hebreo y Armonización Energética</h1>
      <p class="price">$28.000 CLP</p>
      <form class="purchase-form">
        <fieldset class="variant-selector"> ... </fieldset>
        <button type="submit" class="button-primary">Reservar y agregar al carrito</button>
      </form>
    </section>
    <section class="product-description-accordion"> ... </section>
  </article>
  <aside class="related-products">
    <h2>Terapias complementarias</h2>
    <div class="related-grid"> ... </div>
  </aside>
</main>
<footer class="footer"> ... </footer>
```

### `carrito.html` (Resumen de orden)
```html
<header>
  <nav class="navbar"> ... </nav>
</header>
<main class="cart-layout">
  <h1>Tu Espacio de Bienestar — Resumen de tu orden</h1>
  <section class="cart-items">
    <article class="cart-item"> ... </article>
  </section>
  <aside class="cart-summary">
    <h2>Resumen de pago</h2>
    <div class="shipping-calculator"> ... </div>
    <div class="discount-code"> ... </div>
    <button class="button-primary">Continuar con el pago y confirmación</button>
  </aside>
</main>
<footer class="footer"> ... </footer>
```

### `blog.html` y `articulo.html` (Contenido)
```html
<!-- blog.html -->
<main>
  <section class="blog-header"> ... </section>
  <section class="featured-post">
    <article class="card-article card-article-featured"> ... </article>
  </section>
  <section class="blog-grid">
    <article class="card-article"> ... </article>
  </section>
</main>

<!-- articulo.html -->
<main>
  <article class="article-post">
    <header class="article-header">
      <span class="badge">Autocuidado y Gestión Emocional</span>
      <h1>Flores de Bach para el insomnio: 4 esencias para calmar la mente de noche</h1>
      <time datetime="2026-10-10">10 de octubre de 2026</time>
    </header>
    <div class="article-body">
      <p> ... </p>
      <aside class="banner-product-cta">
        <article class="card-product"> ... </article>
      </aside>
    </div>
    <footer class="article-share"> ... </footer>
  </article>
  <section class="comments-section">
    <h2>Preguntas y comentarios</h2>
    <form class="comment-form"> ... </form>
  </section>
</main>
```

---

## 4. Organización del CSS

Los estilos se centralizan en `css/styles.css`, implementando un enfoque **Mobile-First** con variables CSS vinculadas directamente a los tokens de `DESIGN.md`.

```css
:root {
  /* ==========================================================================
     Colores (Tokens sincronizados con DESIGN.md)
     ========================================================================== */
  --color-primary: #445B3C;            /* Verde oliva profundo (Acción primaria y contraste AA) */
  --color-primary-hover: #35472F;      /* Hover activo primario */
  --color-primary-soft: #A5B19A;       /* Salvia clara (Fondo de insignias de modalidad con texto carbón) */
  --color-on-primary: #FFFFFF;         /* Texto blanco sobre primary */
  
  --color-secondary: #E6D7C3;          /* Arena suave (Fondo de tarjetas card-product y banners) */
  --color-on-secondary: #2C3E35;       /* Texto carbón sobre fondo arena */
  
  --color-tertiary: #C88A65;           /* Terracota suave (Decorativo, bordes e íconos sin texto encima) */
  --color-tertiary-soft: #D5A587;      /* Terracota clara (Fondo de etiquetas tag-offer con texto carbón) */
  --color-tertiary-strong: #9E5732;    /* Terracota profundo (Botones CTA de conversión y WhatsApp) */
  --color-on-tertiary: #FFFFFF;        /* Texto blanco sobre tertiary-strong */
  
  --color-neutral: #FAF8F5;            /* Crema suave (Fondo base de página contra el deslumbramiento) */
  --color-surface: #FFFFFF;            /* Blanco cálido (Contenedores elevados e inputs) */
  --color-on-surface: #2C3E35;         /* Carbón bosque (Texto principal de lectura, contraste > 10:1) */
  --color-on-surface-variant: #637367; /* Gris salvia oscuro (Metadatos, duración y subtítulos) */
  
  --color-disabled: #D9D4CC;           /* Elementos deshabilitados */
  --color-on-disabled: #7D7871;        /* Texto de elementos deshabilitados */
  --color-success: #3D7A54;            /* Verde sanación (Confirmaciones exitosas) */
  --color-error: #B33A2B;              /* Terracota rojizo (Alertas de formulario) */

  /* ==========================================================================
     Tipografía (Google Fonts)
     ========================================================================== */
  --font-title: 'Cormorant Garamond', Georgia, serif;
  --font-body: 'Plus Jakarta Sans', system-ui, -apple-system, sans-serif;

  /* Escala Desktop */
  --font-size-display: 3rem;       /* 48px */
  --font-size-headline-lg: 2rem;   /* 32px */
  --font-size-headline-md: 1.5rem; /* 24px */
  --font-size-body: 1rem;          /* 16px */
  --font-size-label: 1rem;         /* 16px */

  --font-weight-regular: 400;
  --font-weight-semibold: 600;

  /* ==========================================================================
     Espaciados y Dimensiones
     ========================================================================== */
  --spacing-xs: 4px;
  --spacing-sm: 8px;
  --spacing-md: 16px;
  --spacing-lg: 24px;
  --spacing-xl: 32px;
  --spacing-2xl: 48px;
  --spacing-3xl: 64px;

  --container-max-width: 1200px;

  /* ==========================================================================
     Radios de borde (Shapes)
     ========================================================================== */
  --radius-md: 8px;                    /* Tarjetas card-product e inputs */
  --radius-full: 9999px;               /* Botones pill, insignias y chips */

  /* ==========================================================================
     Elevaciones y Sombras
     ========================================================================== */
  --shadow-sm: 0 4px 16px rgba(44, 62, 53, 0.06);
  --shadow-hover: 0 8px 24px rgba(44, 62, 53, 0.10);
  --transition-smooth: all 0.25s ease-in-out;
}
```

### Convención de clases CSS

Se emplea la nomenclatura kebab-case coherente en inglés/estándar:
* **Layout:** `.container`, `.grid-2-cols`, `.grid-3-cols`, `.stack-vertical`.
* **Componentes:**
  * `.navbar`, `.footer`
  * `.hero`, `.lead-form`
  * `.card-product`, `.card-article`
  * `.button-primary`, `.button-secondary`, `.button-cta`
  * `.badge` (insignia de modalidad con fondo `--color-primary-soft` y texto `--color-on-surface`)
  * `.tag-offer` (etiqueta de destacado con fondo `--color-tertiary-soft` y texto `--color-on-surface`)
  * `.input-field`

### Breakpoints y Responsive
* **Mobile (base hasta 767px):**
  * 1 sola columna fluida con `padding: 0 var(--spacing-md)`.
  * Menú hamburguesa desplegable y botones principales en ancho completo (`width: 100%`).
  * Tamaños tipográficos adaptados: `display: 2.25rem (36px)`, `headline-lg: 1.75rem (28px)`, `headline-md: 1.25rem (20px)`.
* **Tablet (768px a 1023px):**
  * Grillas a 2 columnas para el catálogo y artículos del blog.
  * Márgenes laterales de 24px (`var(--spacing-lg)`).
* **Desktop (1024px en adelante):**
  * Catálogo en grilla de 3 columnas y layout asimétrico de 2 columnas para ficha de servicio y carrito.
  * Menú horizontal visible y contenedor centrado en 1200px.

---

## 5. Criterios de aceptación

### Navegación y flujos de usuario
- [ ] La barra de navegación (`.navbar`) y el pie de página (`.footer`) son coherentes y están presentes en todas las páginas.
- [ ] Se puede completar el **Flujo 1 (Compra y reserva)** sin interrupciones: `index.html` → `tienda.html` → `producto.html` → `carrito.html`.
- [ ] Se puede completar el **Flujo 2 (Contenido y conversión)**: `blog.html` → `articulo.html` → `producto.html` → `carrito.html`.
- [ ] Todos los enlaces internos entre páginas funcionan correctamente sin arrojar errores 404 accidentales.
- [ ] La página `404.html` contiene un enlace visible para regresar a `index.html`.

### Funcionalidades
- [ ] La landing page (`index.html`) cuenta con el formulario de captación de leads funcional para descargar la Guía de Bienestar.
- [ ] La tienda (`tienda.html`) cuenta con campo de búsqueda por síntoma y selector de modalidades (Presencial / A distancia).
- [ ] La ficha de servicio (`producto.html`) muestra de forma transparente el valor en CLP, duración (60 min), modalidad y botón de WhatsApp directo.
- [ ] El carrito (`carrito.html`) detalla los servicios y productos añadidos, calcula costo de envío por comuna y aplica código de descuento.
- [ ] El artículo (`articulo.html`) incluye botones para compartir en redes/WhatsApp y formulario para dejar comentarios.

### Diseño y Design System
- [ ] Todos los colores y estilos aplicados en el CSS provienen exclusivamente de las variables declaradas en `:root`, sincronizadas con `DESIGN.md`.
- [ ] Las insignias de modalidad (`.badge`) usan el fondo Salvia clara (`#A5B19A`) con texto carbón (`#2C3E35`), superando el ratio WCAG AA (5.1:1).
- [ ] Las etiquetas de oferta y destacado (`.tag-offer`) usan el fondo Terracota clara (`#D5A587`) con texto carbón (`#2C3E35`), superando el ratio WCAG AA (5.2:1).
- [ ] Los colores decorativos `#7A8B6E` y `#C88A65` no tienen texto superpuesto directo en ningún componente.
- [ ] Todos los botones (`.button-primary`, `.button-secondary`, `.button-cta`) implementan estados `:hover`, `:active` y `:focus-visible`.
- [ ] La tipografía respeta la combinación de Cormorant Garamond para títulos y Plus Jakarta Sans para cuerpo y botones.

### Responsive y adaptación multidispositivo
- [ ] La visualización en pantallas móviles (375px de ancho) no genera scroll horizontal no deseado.
- [ ] En pantallas móviles, los botones interactivos clave tienen un área táctil mínima de 44px de altura para facilitar el toque táctil.
- [ ] Las grillas de productos y artículos se reorganizan automáticamente: 1 columna en móvil, 2 columnas en tablet y 3 columnas en desktop.

### Semántica, accesibilidad y publicación
- [ ] Cada página HTML cuenta con un único elemento `<h1>` descriptivo.
- [ ] Todas las imágenes incluyen atributos `alt` con descripciones contextuales para lectores de pantalla.
- [ ] Los campos de formulario (`<input>`, `<select>`, `<textarea>`) tienen etiquetas `<label>` asociadas correctamente.
- [ ] El sitio utiliza únicamente HTML5 y CSS3 propios, sin librerías externas pesadas ni estilos incrustados arbitrarios.
- [ ] El repositorio contiene todos los archivos estructurados y listos para su posterior publicación en GitHub Pages.
