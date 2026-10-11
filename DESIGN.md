---
version: alpha
name: Elysa
description: Design system para Elysa, terapias holísticas y bienestar integral
# Guía: evaluacion/guias/fase-2-specs/06-spec-de-diseno.md
# Valida con: npx @google/design.md lint DESIGN.md
colors:
  primary: "#445B3C"
  primary-hover: "#35472F"
  primary-soft: "#A5B19A"
  on-primary: "#FFFFFF"
  secondary: "#E6D7C3"
  on-secondary: "#2C3E35"
  tertiary: "#C88A65"
  tertiary-soft: "#D5A587"
  tertiary-strong: "#9E5732"
  on-tertiary: "#FFFFFF"
  neutral: "#FAF8F5"
  surface: "#FFFFFF"
  on-surface: "#2C3E35"
  on-surface-variant: "#637367"
  disabled: "#D9D4CC"
  on-disabled: "#7D7871"
  success: "#3D7A54"
  error: "#B33A2B"
typography:
  headline-display:
    fontFamily: Cormorant Garamond
    fontSize: 48px
    fontWeight: 600
    lineHeight: 1.1
  headline-lg:
    fontFamily: Cormorant Garamond
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.2
  headline-md:
    fontFamily: Cormorant Garamond
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1
rounded:
  md: 8px
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
  button-cta:
    backgroundColor: "{colors.tertiary-strong}"
    textColor: "{colors.on-tertiary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  card-product:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  badge:
    backgroundColor: "{colors.primary-soft}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.full}"
  tag-offer:
    backgroundColor: "{colors.tertiary-soft}"
    textColor: "{colors.on-surface}"
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

# Elysa — Design system

## Overview

Elysa es un espacio de bienestar integral y terapias holísticas (Reiki, Tameana, Tarot terapéutico, Péndulo Hebreo y Flores de Bach). Su usuaria principal es Valentina Morales (32 años), profesional que busca equilibrar su energía y aliviar el estrés laboral, navegando habitualmente desde su smartphone por las noches. La interfaz transmite calma, calidez botánica, serenidad, transparencia y contención, evitando la frialdad clínica o estéticas esotéricas estridentes.

## Colors

- **Primary (`#445B3C`):** Verde oliva profundo. Se utiliza para botones de acción principal, enlaces destacados, íconos principales y estados activos. Garantiza accesibilidad WCAG AA con texto blanco encima (ratio 6.8:1).
- **Primary-hover (`#35472F`):** Verde oliva oscuro para feedback visual interactivo al pasar el cursor o presionar botones primarios.
- **Primary-soft (`#A5B19A`):** Salvia clara. Fondo para insignias y chips de modalidad informativa (ej. "Presencial") con texto carbón (`#2C3E35`), asegurando contraste WCAG AA (ratio 5.1:1).
- **Secondary (`#E6D7C3`):** Arena suave / lino. Fondo cálido y contenedor para tarjetas de servicios (`card-product`), bloques destacados y banners suaves.
- **Tertiary (`#C88A65`):** Terracota suave. Reservado exclusivamente para iconos cálidos, bordes y detalles decorativos, sin texto encima.
- **Tertiary-soft (`#D5A587`):** Terracota clara. Fondo para etiquetas e insignias de oferta o sesión destacada (ej. "Sesión destacada") con texto carbón (`#2C3E35`), asegurando contraste WCAG AA (ratio 5.2:1).
- **Tertiary-strong (`#9E5732`):** Terracota profundo. Fondo exclusivo para botones CTA directos o conversiones que requieran texto blanco legible (ratio 5.2:1).
- **Neutral (`#FAF8F5`):** Crema suave / lino claro. Fondo principal general de todas las páginas para evitar la fatiga visual del blanco puro.
- **Surface (`#FFFFFF`):** Blanco puro cálido para fondos de campos de formulario (`input-field`), tarjetas elevadas y modales.
- **On-surface (`#2C3E35`):** Carbón bosque. Color por defecto para títulos y cuerpo de texto general, asegurando un contraste superior a 10:1 sobre el fondo neutral.
- **On-surface-variant (`#637367`):** Gris salvia oscuro para textos complementarios, metadatos, duración de terapias y subtítulos.
- **Disabled (`#D9D4CC`):** Fondo para elementos interactivos deshabilitados.
- **Success (`#3D7A54`):** Verde sanación para mensajes de confirmación de agendamiento y estados exitosos.
- **Error (`#B33A2B`):** Terracota rojizo para alertas de validación y errores en formularios.

## Typography

- **Títulos:** Cormorant Garamond (Google Fonts). Fuente serif clásica con aire meditativo, místico y orgánico. Se emplea en `headline-display` (48px), `headline-lg` (32px) y `headline-md` (24px).
- **Textos:** Plus Jakarta Sans (Google Fonts). Fuente sans-serif de trazado geométrico, legible y versátil para pantallas móviles. Se emplea en `body-md` (16px, regular) para descripciones y `label-md` (16px, semibold) para botones y etiquetas interactivas.

## Layout

- **Ancho máximo de contenedor:** 1200px centrado con `margin: 0 auto`.
- **Escala de espaciado:** basamento modular de múltiplos de 8px (`xs: 4px`, `sm: 8px`, `md: 16px`, `lg: 24px`, `xl: 32px`, `2xl: 48px`, `3xl: 64px`).
- **Breakpoints:**
  - **Mobile (hasta 767px):** 1 columna fluida, márgenes laterales de 16px, navegación con menú hamburguesa, botones en ancho completo (full-width) para fácil toque táctil.
  - **Tablet (768px a 1023px):** 2 columnas para grilla de terapias y artículos, márgenes laterales de 24px.
  - **Desktop (1024px o más):** 3 columnas para el catálogo de terapias/productos, 2 columnas asimétricas para fichas de detalle, menú de navegación horizontal visible y márgenes laterales de 32px.

## Elevation & Depth

- La jerarquía visual se establece primordialmente a través de capas sutiles de color (fondo neutral `#FAF8F5`, tarjetas de servicios en secundario `#E6D7C3`, y modales o inputs en surface `#FFFFFF`).
- **Sombras suaves:** para elementos interactivos en elevación se utiliza una sombra difusa y cálida: `0 4px 16px rgba(44, 62, 53, 0.06)`. En estado hover se intensifica levemente a `0 8px 24px rgba(44, 62, 53, 0.10)`.

## Shapes

- **Botones y chips:** esquinas redondeadas completas (`rounded.full: 9999px`) de estilo píldora orgánica para acentuar la sensación de armonía y suavidad.
- **Tarjetas y campos de entrada:** esquinas suavemente redondeadas (`rounded.md: 8px`).

## Components

### Botón Primario (`button-primary`)
Botón de llamada a la acción estándar (ej. "Agendar sesión", "Conocer más").
- Fondo `{colors.primary}`, texto `{colors.on-primary}`, tipografía `{typography.label-md}`, esquinas redondeadas `{rounded.full}` y padding de 12px 24px.
- **Hover (`button-primary-hover`):** Fondo cambia a `{colors.primary-hover}`.
- **Disabled (`button-primary-disabled`):** Fondo `{colors.disabled}` y texto `{colors.on-disabled}`. Cursor `not-allowed`.

### Botón Secundario (`button-secondary`)
Botón secundario para acciones alternativas o de menor jerarquía (ej. "Ver detalles", "Volver al catálogo").
- Fondo `{colors.surface}` con borde sutil en `{colors.primary}`, texto `{colors.primary}`, esquinas `{rounded.full}`.

### Botón CTA (`button-cta`)
Botón de conversión directa para agendamiento inmediato o compra por WhatsApp.
- Fondo `{colors.tertiary-strong}`, texto `{colors.on-tertiary}`, tipografía `{typography.label-md}`, esquinas `{rounded.full}` y padding de 12px 24px.

### Tarjeta de Servicio o Producto (`card-product`)
Contenedor modular para exhibir cada terapia holística (Reiki, Tameana, Tarot, etc.).
- Fondo `{colors.secondary}`, texto `{colors.on-secondary}`, esquinas `{rounded.md}`, padding `{spacing.md}`.
- Contiene: imagen de la terapia, título del servicio en `headline-md`, descripción breve en `body-md`, etiqueta de modalidad (Presencial / A distancia), valor en pesos chilenos y botón de acción.
- El precio y la modalidad siempre son visibles de forma transparente para evitar la frustración de precios ocultos.
- Hover: elevación sutil y transición suave de escala del 102% en la imagen.

### Insignia de Modalidad (`badge`)
Chip compacto para comunicar modalidad de atención (ej. "Presencial", "Online").
- Fondo `{colors.primary-soft}`, texto `{colors.on-surface}`, tipografía compacta y esquinas `{rounded.full}`. Cumple con ratio WCAG AA (5.1:1).

### Etiqueta de Destacado / Oferta (`tag-offer`)
Chip compacto para comunicar sesiones destacadas, ofertas o recomendaciones.
- Fondo `{colors.tertiary-soft}`, texto `{colors.on-surface}`, tipografía compacta y esquinas `{rounded.full}`. Cumple con ratio WCAG AA (5.2:1).

### Campo de Texto (`input-field`)
Campo de entrada para formularios de contacto o reservas.
- Fondo `{colors.surface}`, texto `{colors.on-surface}`, padding de 12px 14px, esquinas `{rounded.md}` y borde en `{colors.secondary}`.
- Focus: borde activo en `{colors.primary}` sin contornos invasivos.

## Do's and Don'ts

- **Do:** Usar el fondo crema suave (`#FAF8F5`) para mantener la calidez y el descanso visual en pantallas.
- **Do:** Indicar siempre la modalidad (presencial u online) y la duración de cada terapia de forma transparente.
- **Do:** Mantener bordes redondeados orgánicos para conservar el tono receptivo y empático del espacio.
- **Don't:** No colocar texto directamente sobre verde salvia decorativo (`#7A8B6E`) o terracota suave (`#C88A65`) ya que no cumplen ratio mínimo AA (4.5:1); usar siempre `primary-soft` (`#A5B19A`) y `tertiary-soft` (`#D5A587`) con texto carbón (`#2C3E35`) para insignias y etiquetas.
- **Don't:** No usar fondos negros puros o blancos puros deslumbrantes que rompan la armonía natural.
- **Don't:** No saturar la interfaz con animaciones ruidosas o textos esotéricos confusos; priorizar claridad, cercanía y serenidad.
