# Color y tipografía — Elysa

> Guía: [Color y tipografía](../evaluacion/guias/fase-2-specs/05-color-y-tipografia.md)

## Paleta

| Rol | Color | HEX | Uso |
|---|---|---|---|
| Principal | Verde oliva suave (Salvia) | `#7A8B6E` | Identidad de marca, detalles botánicos, iconos, bordes e insignias informativas |
| Principal interactivo | Verde oliva profundo | `#445B3C` | Botones de acción primaria (`button-primary`) con texto blanco y enlaces activos para asegurar contraste AA |
| Secundario | Arena suave / Lino | `#E6D7C3` | Fondos de tarjetas de servicios (`card-product`), contenedores y banners secundarios |
| Acento | Terracota suave | `#C88A65` | Elementos de énfasis visual, iconos cálidos, badges decorativos y etiquetas |
| Acento CTA | Terracota profundo | `#9E5732` | Botones de conversión directa (agendar sesión por WhatsApp o comprar) con texto blanco |
| Fondo general | Crema suave | `#FAF8F5` | Fondo principal del sitio (`page`), evitando el resplandor del blanco puro |
| Texto principal | Carbón bosque | `#2C3E35` | Títulos, subtítulos y cuerpo de lectura general |
| Texto secundario | Gris salvia oscuro | `#637367` | Metadatos, duración de sesiones, bajadas y textos complementarios |
| Superficie / Tarjetas | Blanco cálido | `#FFFFFF` | Contenedores de modales, inputs de formulario y tarjetas elevadas |
| Éxito | Verde sanación | `#3D7A54` | Mensajes de confirmación de agenda, pago recibido y estado completado |
| Error | Terracota rojizo | `#B33A2B` | Alertas de validación de campos y mensajes de error en formularios |

## Contraste

| Combinación | Ratio | Resultado |
|---|---|---|
| Texto `#2C3E35` sobre fondo crema `#FAF8F5` | 10.7:1 | AAA ✅ (Lectura principal óptima y sin fatiga) |
| Texto `#2C3E35` sobre fondo secundario arena `#E6D7C3` | 8.0:1 | AAA ✅ (Lectura nítida dentro de tarjetas de servicios) |
| Texto blanco `#FFFFFF` sobre verde interactivo `#445B3C` | 6.8:1 | AA ✅ (Botones primarios con alta visibilidad) |
| Texto blanco `#FFFFFF` sobre terracota CTA `#9E5732` | 5.2:1 | AA ✅ (Llamadas a la acción y reservas) |
| Texto secundario `#637367` sobre fondo crema `#FAF8F5` | 4.6:1 | AA ✅ (Bajadas y textos secundarios legibles) |
| Texto blanco `#FFFFFF` sobre verde salvia `#7A8B6E` | 3.7:1 | ⚠️ Solo para elementos gráficos o insignias con texto oscuro `#2C3E35` (4.6:1 ✅) |
| Texto blanco `#FFFFFF` sobre terracota suave `#C88A65` | 2.9:1 | ⚠️ Solo para detalles decorativos, iconos y bordes |

## Tipografía

- **Títulos:** **Cormorant Garamond** (Google Fonts). Familia serif de proporciones clásicas y trazos elegantes. Transmite serenidad, espiritualidad reflexiva, profundidad holística y la calidez acogedora de un espacio terapéutico.
- **Textos:** **Plus Jakarta Sans** (Google Fonts). Sans-serif moderna, limpia y geométrica con excelente legibilidad en pantallas móviles pequeñas, ideal para la lectura nocturna sin cansancio ocular.

| Elemento | Desktop | Mobile | Peso |
|---|---|---|---|
| h1 | 3rem (48px) | 2.25rem (36px) | 600 (SemiBold) |
| h2 | 2rem (32px) | 1.75rem (28px) | 600 (SemiBold) |
| h3 | 1.5rem (24px) | 1.25rem (20px) | 600 (SemiBold) |
| Párrafo | 1rem (16px) | 1rem (16px) | 400 (Regular) |
| Botón | 1rem (16px) | 1rem (16px) | 600 (SemiBold) |

## Justificación

La identidad visual de **Elysa** se fundamenta en la búsqueda de calma, sanación y equilibrio energético para nuestra proto-persona, **Valentina Morales**. Valentina suele conectarse al sitio tarde en la noche tras una extenuante jornada laboral; por ello, la combinación del fondo crema suave (`#FAF8F5`) con el texto carbón bosque (`#2C3E35`) elimina el deslumbramiento del blanco puro y asegura una lectura relajante, con un ratio de contraste sobresaliente (10.7:1).

El verde salvia (`#7A8B6E`) y el verde oliva interactivo (`#445B3C`) evocan las propiedades de las Flores de Bach, la naturaleza y la renovación energética del Reiki. El tono arena suave (`#E6D7C3`) aporta la estabilidad de la tierra y los cuarzos usados en Tameana, proporcionando una base neutra y cálida para organizar las fichas de servicios. Por su parte, el terracota (`#C88A65` y `#9E5732`) rescata la calidez del contacto humano y canaliza la atención hacia las acciones clave de reserva sin resultar agresivo.

A nivel tipográfico, la majestuosidad orgánica de **Cormorant Garamond** otorga a los títulos un carácter meditativo y místico confiable, mientras que la pureza geométrica de **Plus Jakarta Sans** permite que Valentina comprenda de inmediato las descripciones de las terapias, modalidades y valores en su smartphone sin barreras de legibilidad.
