# Tecnologías del proyecto — Elysa

> Guía: [Tecnologías del proyecto](../evaluacion/guias/fase-1-requerimientos/04-tecnologias.md)

## Stack

| Área | Herramienta | Para qué la uso |
|---|---|---|
| Construcción | HTML + CSS | Maquetación web estática, semántica y responsiva de las páginas (landing, blog y tienda) sin dependencias ni gestores de contenido complejos |
| Versionado | Git y GitHub | Control de versiones local y remoto, respaldo en la nube y registro del avance progresivo del proyecto mediante commits |
| Publicación | GitHub Pages | Alojamiento y despliegue gratuito del sitio web con URL pública accesible para evaluación y demostración |
| Diseño | Whimsical | Elaboración del moodboard conceptual, calco de componentes visuales inspirados en los referentes y wireframes iniciales |
| Diseño | Google Stitch | Generación del prototipo referencial e interactivo en alta fidelidad (versiones desktop y mobile) a partir de las specs de diseño |
| IA | Antigravity IDE (Gemini) | Asistencia en la formulación de requerimientos UX/UI, estructuración de documentación markdown y generación de assets gráficos como el avatar |
| Editor | Antigravity IDE | Entorno de desarrollo integrado para edición ágil de código, documentación técnica y trabajo sincronizado con el repositorio |

## Qué es funcional y qué es prototipo

| Funcionalidad | Estado en esta versión |
|---|---|
| Navegación estructural entre landing page, blog y tienda online | Funcional |
| Visualización del detalle de cada terapia y producto con descripción y valores | Funcional |
| Enlace directo a WhatsApp (wa.me) con mensaje predeterminado para consultas | Funcional |
| Botones para compartir artículos del blog en redes sociales y mensajería | Funcional |
| Formulario de captación de leads (guía de bienestar + 10 % de descuento) | Prototipo visual |
| Buscador de terapias y filtrado por modalidad (presencial/a distancia) | Prototipo visual |
| Carrito de compras y selector de variantes de sesión o formato de producto | Prototipo visual |
| Cálculo de costo de despacho para productos físicos según comuna | Prototipo visual |
| Sistema de comentarios e interacción en los artículos del blog | Prototipo visual |
| Cuestionario interactivo de autodiagnóstico emocional | Prototipo visual |
| Calendario interactivo con reserva de horas en tiempo real | Prototipo visual |

## Integraciones para una versión real

- **Pasarela de pago online:** Integración con Webpay Plus (Transbank), Mercado Pago o Fintoc para procesar pagos seguros con tarjetas de crédito/débito y transferencias.
- **Plataforma de agendamiento y sincronización de citas:** Conexión con servicios como Calendly, Acuity Scheduling o Google Calendar API para reservar horas y sincronizar la disponibilidad de la terapeuta en tiempo real.
- **Automatización de Email Marketing / CRM:** Herramienta como Mailchimp, Brevo o ConvertKit para almacenar los contactos captados, enviar automáticamente la guía de bienestar en PDF y remitir cupones de descuento.
- **Courier y cálculo logístico:** API de envíos (como Shipit, Starken o Chilexpress) para calcular de forma dinámica las tarifas de despacho de Flores de Bach y artículos holísticos según la comuna del destinatario.
- **WhatsApp Business API:** Automatización de mensajes de confirmación de reserva y recordatorios de sesiones presenciales o a distancia.

## Restricciones

- **Plazo:** Proyecto enmarcado en la Evaluación Parcial 02 de DUOC UC (del 29 de septiembre al 14 de octubre de 2026), con entrega final de la Fase 1 fijada para el lunes 5 de octubre a las 23:59 hrs.
- **Alcance técnico:** En esta entrega el alcance contempla la documentación de requerimientos y el prototipo referencial en Stitch. La futura implementación en código se limita estrictamente a HTML y CSS nativo publicado en GitHub Pages, sin backend ni bases de datos dinámicas.
- **Marca:** Elysa es un emprendimiento en etapa inicial sin manual de identidad corporativa previo; la paleta de colores, tipografías y lineamientos estéticos se definen y formalizan en la Fase 2 (DESIGN.md).
- **Dispositivos y enfoque:** Enfoque prioritario *Mobile First* (optimizado para pantallas de celular de 360px a 414px), respondiendo al comportamiento de la proto-persona (Valentina) que navega desde su teléfono móvil por las noches, con adaptación fluida a pantallas de escritorio (Desktop 1440px).
