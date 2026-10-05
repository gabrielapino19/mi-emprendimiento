# Arquitectura de la información — Elysa

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

```text
Inicio (Landing page)
├── Servicios y Tienda (Catálogo general)
│   ├── Categoría: Terapias Energéticas
│   ├── Categoría: Autoconocimiento y Guía
│   ├── Categoría: Bienestar Natural y Esencias
│   ├── Ficha de Servicio o Producto (Detalle, modalidades, duración y valores)
│   └── Carrito de compra y reserva (Resumen de orden y cálculo de despacho)
├── Blog de Bienestar
│   ├── Categoría: Sanación Energética
│   ├── Categoría: Autocuidado y Gestión Emocional
│   ├── Categoría: Guía y Reflexión Personal
│   └── Artículo de lectura (Contenido educativo, comentarios y recomendación de servicios)
├── Sobre Elysa (Historia, trayectoria, certificaciones y enfoque de la terapeuta)
├── Contacto (Formulario de mensaje directo y botón a WhatsApp)
├── Preguntas Frecuentes (FAQ sobre sesiones presenciales, a distancia, preparación y cancelaciones)
├── Términos y Condiciones (Políticas de reserva, reprogramación, pagos y entregas)
├── Política de Privacidad (Tratamiento seguro de datos de contacto y leads)
└── 404 (Página de error amigable con botón de retorno al inicio)
```

---

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: Compra y reserva de terapia

Representa el viaje de **Valentina Morales** al descubrir el sitio desde redes sociales durante la noche, buscando aliviar su agotamiento laboral.

```text
Instagram (Reel nocturno sobre sobrecarga laboral y equilibrio de energía)
→ Inicio (Landing page)
→ [Hace clic en "Explorar terapias y sesiones"]
→ Servicios y Tienda
→ [Aplica filtros: Modalidad "A distancia" y Enfoque "Alivio del estrés"]
→ Ficha de servicio: "Péndulo Hebreo y Armonización Energética"
→ [Revisa descripción en lenguaje claro, duración (60 min), requisitos previos y precio]
→ [Selecciona la variante: "Modalidad a distancia (Online)"]
◇ ¿Tiene dudas puntuales antes de confirmar?
   ├── Sí → [Hace clic en "Consultar por WhatsApp"] → Chat de WhatsApp con la terapeuta
   └── No → [Hace clic en "Agregar al carrito"]
→ Carrito de compra y reserva
→ [Revisa el resumen de la sesión, valor transparente y condiciones]
→ Fin: Carrito listo para confirmar y pagar
```

### Flujo 2: Contenido educativo y conversión

Representa a Valentina buscando soluciones naturales para sus dificultades de descanso e integrando el contenido del blog con la tienda o captación de leads.

```text
Google ("Flores de Bach para el insomnio y sobrecarga laboral")
→ Artículo del blog: "Flores de Bach para el insomnio: 4 esencias para calmar la mente de noche"
→ [Lee el artículo y recomendaciones de autocuidado]
→ [Hace clic en la tarjeta del producto recomendado en el texto: "Fórmula Flores de Bach - Calma y Sueño"]
→ Ficha de producto: "Fórmula Personalizada Flores de Bach (30 ml)"
◇ ¿Desea adquirir el producto en este momento?
   ├── Sí → [Selecciona formato de 30 ml y hace clic en "Agregar al carrito"]
          → Carrito de compra
          → [Calcula costo de despacho ingresando su comuna: Providencia]
          → Fin: Compra lista para coordinar envío a domicilio
   └── No → [Regresa al final del artículo y completa nombre y correo en el formulario para recibir la "Guía de Bienestar + 10 % de dcto."]
          → Pantalla de confirmación con descarga directa de la guía en PDF
          → Fin: Lead captado exitosamente
```

---

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de productos y servicios

| Categoría | Servicios y Productos incluidos |
|---|---|
| **Terapias Energéticas** | • Sesión de Reiki Tradicional (Presencial y A distancia)<br>• Sesión de Tameana - Sanación vibracional con cuarzos (Presencial)<br>• Sesión de Péndulo Hebreo - Limpieza y armonización energética (Presencial y A distancia) |
| **Autoconocimiento y Guía** | • Lectura de Tarot Terapéutico (Presencial y Online)<br>• Sesión integral de Tarot Terapéutico + Alineación de chakras (Online) |
| **Bienestar Natural y Esencias** | • Fórmula personalizada Flores de Bach (Gotario 30 ml y 50 ml)<br>• Fórmula SOS Rescate Emocional (Gotario 30 ml)<br>• Bruma áurica de descarga con aceites esenciales y cuarzo blanco (100 ml)<br>• Kit de cuarzos para armonización personal |

*Filtros complementarios en la tienda:* Modalidad (Presencial / A distancia) y Enfoque terapéutico (Alivio del estrés, Armonización energética, Claridad mental).

### Categorías del blog

| Categoría | Idea de artículo | Necesidad o motivación de Valentina | Producto o servicio relacionado |
|---|---|---|---|
| **Sanación Energética** | *"¿Reiki o Péndulo Hebreo? Cómo elegir la terapia adecuada según tu nivel de cansancio"* | Le frustra no entender la diferencia entre terapias y necesita una guía clara sin tecnicismos para saber cuál le devolverá la vitalidad | Sesión de Péndulo Hebreo / Sesión de Reiki |
| **Autocuidado y Gestión Emocional** | *"Flores de Bach para el insomnio: 4 esencias para calmar la mente de noche"* | Siente que el estrés laboral le genera fatiga mental y no le permite conciliar un sueño reparador | Fórmula personalizada Flores de Bach (Calma y Sueño) |
| **Guía y Reflexión Personal** | *"Tarot terapéutico vs. Tarot predictivo: por qué esta herramienta te ayuda a tomar decisiones difíciles"* | Busca herramientas de introspección para encontrar claridad mental en momentos de cambio personal o laboral | Lectura de Tarot Terapéutico |
