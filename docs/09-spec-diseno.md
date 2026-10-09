# Spec de diseño — Elysa

> Guía: [Spec de diseño](../evaluacion/guias/fase-2-specs/06-spec-de-diseno.md)

La spec de diseño tiene dos partes:

1. **[`DESIGN.md`](../DESIGN.md)** (en la raíz): tu design system, en el formato que Stitch importa.
2. **Este documento:** tus pantallas, escritas como prompts listos para pegar en Stitch.

**Wireframes en Whimsical:** https://whimsical.com/gabriela83/pagina-elysa-6SnDMzHbE2vbDd7AAZhiQv

> Guía de wireframes: [Wireframes](../evaluacion/guias/fase-2-specs/04-wireframes.md)

<!-- Captura de los wireframes: ![Wireframes](img/wireframes.png) -->

## Pantallas

A continuación se detallan los prompts de las 6 pantallas para Google Stitch, alineados con el design system (`DESIGN.md`), las necesidades de **Valentina Morales** y la arquitectura de la información de Elysa.

---

### 1. Landing

```text
Pantalla: Landing page de Elysa, versión desktop. Usa el design system del proyecto.
Objetivo: Que Valentina Morales comprenda en segundos la propuesta de valor de Elysa (bienestar integral y sanación energética), conecte con la calidez del espacio y encuentre un camino directo y transparente para agendar una sesión o descargar una guía orientativa.
Componentes, de arriba hacia abajo:
1. navbar: Logo "Elysa — Terapias Holísticas", enlaces de navegación "Inicio", "Terapias", "Blog", "Sobre Mí", botón button-secondary "WhatsApp directo" y botón de carrito con contador numérico.
2. hero: Título en headline-display "Reconecta con tu equilibrio natural y vuelve a habitar tu paz", bajada en body-md explicando las terapias holísticas personalizadas para aliviar la sobrecarga laboral, botón button-primary "Explorar terapias", botón button-secondary "Agendar por WhatsApp" e imagen cálida con texturas de cuarzo y luz suave.
3. Sección de diferenciales: Fila de 3 contenedores con íconos orgánicos: "Atención cercana y personalizada", "Modalidades presencial y a distancia" y "Valores transparentes sin cotizaciones ocultas".
4. Sección de catálogo destacado: Título en headline-lg "Terapias para restaurar tu vitalidad", bajada y grilla de 3 card-product:
   - "Tameana: Sanación Vibracional con Cuarzos" ($30.000 CLP / 60 min, tag-offer "Presencial en Providencia", botón button-primary "Ver detalles").
   - "Péndulo Hebreo y Armonización" ($28.000 CLP / 60 min, tag-offer "Presencial u Online", botón button-primary "Ver detalles").
   - "Sesión de Reiki Tradicional Usui" ($25.000 CLP / 50 min, tag-offer "Presencial u Online", botón button-primary "Ver detalles").
5. lead-form: Bloque destacado en fondo secondary con título en headline-md "¿No sabes qué terapia necesitas? Descarga nuestra Guía de Bienestar", campos input-field para Nombre y Correo/WhatsApp, botón button-primary "Descargar guía gratuita + 10% dcto" y texto de privacidad.
6. Sección de testimonios: Grilla de 3 tarjetas con testimonios reales de consultantes, nombre, profesión y terapia recibida destacando la disminución del estrés y la sensación de paz.
7. footer: Enlaces a políticas, preguntas frecuentes, redes sociales (@elysa.bienestar) y derechos reservados.
```

---

### 2. Tienda

```text
Pantalla: Tienda y catálogo de Elysa, versión desktop. Usa el design system del proyecto.
Objetivo: Que Valentina explore todas las terapias y productos de bienestar, filtrando según su molestia o disponibilidad de horario sin encontrarse con precios ocultos.
Componentes, de arriba hacia abajo:
1. navbar.
2. Encabezado con título headline-lg "Terapias y Bienestar Natural" y buscador input-field con texto "Buscar por molestia: estrés, insomnio, Reiki, Flores de Bach...".
3. Barra de filtros: Chips interactivos de categoría ("Todas las Terapias", "Terapias Energéticas", "Autoconocimiento y Guía", "Bienestar Natural y Esencias") y selector desplegable de modalidad ("Todas", "Presencial en Providencia", "A distancia / Online").
4. Grilla de 6 card-product organizadas en 3 columnas:
   - "Péndulo Hebreo y Armonización Energética" ($28.000 CLP / 60 min, Presencial / Online).
   - "Tameana: Sanación Vibracional con Cuarzos" ($30.000 CLP / 60 min, Presencial).
   - "Sesión de Reiki Tradicional Usui" ($25.000 CLP / 50 min, Presencial / Online).
   - "Lectura de Tarot Terapéutico" ($22.000 CLP / 60 min, Online / Presencial).
   - "Fórmula personalizada Flores de Bach 30 ml" ($14.990 CLP, Despacho a todo Chile).
   - "Bruma Áurica de Descarga con Cuarzo Blanco 100 ml" ($12.500 CLP, Despacho a todo Chile).
5. Bloque de ayuda: Caja informativa con texto "¿Tienes dudas sobre cuál elegir?" y botón button-secondary "Escríbenos por WhatsApp para asesorarte".
6. footer.
```

---

### 3. Ficha de producto

```text
Pantalla: Ficha de servicio de Elysa ("Péndulo Hebreo y Armonización Energética"), versión desktop. Usa el design system del proyecto.
Objetivo: Que Valentina conozca exactamente qué incluye la sesión, cómo prepararse en modalidad a distancia, su valor transparente y elija su horario con seguridad.
Componentes, de arriba hacia abajo:
1. navbar.
2. Layout principal de 2 columnas asimétricas:
   - Columna izquierda: Imagen destacada de la terapia con péndulo de amatista, seguida de acordeón de información: "En qué consiste la terapia", "Beneficios comprobados", "Cómo prepararte (para modalidad online)" y "Preguntas frecuentes".
   - Columna derecha: Chip tag-offer "Sesión más solicitada", título en headline-lg "Péndulo Hebreo y Armonización Energética", precio visible destacado "$28.000 CLP", duración ("60 minutos"), selector de modalidad en radio buttons ("A distancia por videollamada" seleccionado por defecto, "Presencial en Providencia"), selector de fecha sugerida, botón button-primary "Reservar y agregar al carrito", botón button-secondary "Consultar dudas por WhatsApp" y nota de confidencialidad y contención terapéutica.
3. Sección de recomendaciones: Fila de 3 card-product con terapias o complementos afines ("Fórmula Flores de Bach Calma", "Bruma Áurica", "Reiki Usui").
4. footer.
```

---

### 4. Carrito

```text
Pantalla: Carrito de compras y reserva de Elysa, versión desktop. Usa el design system del proyecto.
Objetivo: Que Valentina revise el detalle claro de sus servicios y preparados seleccionados, verifique el total sin recargos sorpresa y finalice su reserva cómodamente.
Componentes, de arriba hacia abajo:
1. navbar.
2. Título en headline-lg "Tu Espacio de Bienestar — Resumen de tu orden".
3. Layout de 2 columnas:
   - Columna izquierda (Ítems en el carrito): Contenedor en surface con tarjeta de servicio "Péndulo Hebreo (Modalidad a distancia)" por $28.000 CLP con botón de eliminar, y producto físico "Fórmula Flores de Bach (Gotario 30 ml)" con selector de cantidad por $14.990 CLP.
   - Columna derecha (Resumen de pago): Contenedor en secondary con desglose de montos: Subtotal $42.990 CLP, calculador de costo de envío con input-field para comuna ("Providencia: $3.500 CLP"), campo para código de descuento de bienvenida ("BIENVENIDA10: -$4.299 CLP"), y total final destacado en headline-md "$42.191 CLP".
   - Botón button-primary "Continuar con el pago y confirmación", sellos de pago seguro (Webpay / Transferencia bancaria) y garantía de reprogramación sin costo hasta 24 horas antes.
4. footer.
```

---

### 5. Blog

```text
Pantalla: Blog de Bienestar de Elysa, versión desktop. Usa el design system del proyecto.
Objetivo: Que Valentina encuentre lecturas breves y relajantes para educarse en terapias holísticas y resolver dudas comunes durante sus noches de descanso.
Componentes, de arriba hacia abajo:
1. navbar.
2. Encabezado con título headline-lg "Blog de Bienestar y Sabiduría Holística" y bajada sobre autocuidado y equilibrio interior.
3. Barra de navegación por categorías con chips: "Todos los artículos", "Sanación Energética", "Autocuidado y Gestión Emocional", "Guía y Reflexión Personal".
4. Artículo destacado (Hero post): Imagen horizontal amplia con chip "Sanación Energética", título headline-md "¿Reiki o Péndulo Hebreo? Cómo elegir la terapia adecuada según tu nivel de cansancio", tiempo de lectura "4 min", bajada y botón button-secondary "Leer artículo completo".
5. Grilla de 4 card-article organizadas en 2 columnas:
   - "Flores de Bach para el insomnio: 4 esencias para calmar la mente de noche" (Autocuidado / 3 min de lectura).
   - "Tarot terapéutico vs. Tarot predictivo: una brújula para tus decisiones" (Guía y Reflexión / 5 min de lectura).
   - "Qué es Tameana y cómo actúan los cuarzos en tu cuerpo sutil" (Sanación Energética / 4 min de lectura).
   - "Rutina nocturna de descarga energética para profesionales con sobrecarga mental" (Autocuidado / 3 min de lectura).
6. Bloque de suscripción: Contenedor con input-field para correo y botón button-primary "Recibir reflexiones y consejos semanales".
7. footer.
```

---

### 6. Artículo

```text
Pantalla: Artículo individual del blog de Elysa ("Flores de Bach para el insomnio..."), versión desktop. Usa el design system del proyecto.
Objetivo: Que Valentina lea una guía cercana y comprensible sobre el insomnio, identifique cómo las esencias florales le ayudan a dormir mejor y acceda fácilmente a la fórmula personalizada.
Componentes, de arriba hacia abajo:
1. navbar.
2. Encabezado del artículo: Chip de categoría "Autocuidado y Gestión Emocional", título en headline-display "Flores de Bach para el insomnio: 4 esencias para calmar la mente de noche", fecha, tiempo estimado "3 min de lectura" y firma de la terapeuta.
3. Imagen horizontal de cabecera con frascos de esencias florales, luz cálida de atardecer y elementos botánicos.
4. Contenedor de lectura centrado (ancho máximo 760px) con tipografía body-md y subtítulos en headline-md explicando las 4 esencias (White Chestnut para pensamientos rumiantes, Vervain para relajación, etc.) en tono empático y sin tecnicismos densos.
5. Banner contextual dentro del texto: Tarjeta destacada card-product recomendando la "Fórmula personalizada Flores de Bach (Calma y Sueño)" con botón button-primary "Ver fórmula en la tienda".
6. Barra de interacción social: Botones para compartir por WhatsApp y redes sociales.
7. Sección de comentarios con input-field para preguntas dirigidas a la terapeuta.
8. footer.
```

---

### Versión mobile (para cada pantalla)

```text
Genera la versión mobile (375px de ancho) de esta pantalla siguiendo la sección Layout de DESIGN.md:
- Contenedor fluido de 1 sola columna con márgenes laterales de 16px.
- La navbar se condensa mostrando únicamente el logotipo de Elysa, el acceso al carrito con contador y un botón de menú hamburguesa desplegable.
- Los botones principales y secundarios se presentan a ancho completo (full-width) con padding táctil de 14px para facilitar el toque con el pulgar.
- Las escalas tipográficas se ajustan a mobile: headline-display en 36px, headline-lg en 28px y headline-md en 20px, manteniendo body-md en 16px para lectura nocturna cómoda.
- Las grillas de card-product y card-article pasan de columnas múltiples a un stack vertical de 1 columna con tarjetas amplias y espaciado de 16px.
- En la ficha de producto y el carrito, la información se apila verticalmente priorizando primero los detalles y dejando los resúmenes y botones de confirmación siempre accesibles al final.
```
