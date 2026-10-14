# Arquitectura de la información — Studio Milano

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

Studio Milano ofrece servicios de manicure, diseños personalizados y cuidado de uñas. El mapa de sitio organiza la estructura para que las clientas conozcan los servicios, revisen los trabajos realizados y puedan contactar o reservar una hora fácilmente.

### Estructura del sitio web

```text
Inicio (Landing)
├── Servicios
│   ├── Manicure tradicional
│   ├── Esmaltado permanente
│   ├── Uñas acrílicas o gel
│   ├── Diseños personalizados
│   ├── Galería de trabajos
│   └── Precios
├── Blog
│   ├── Cuidados básicos de uñas
│   ├── Tendencias en diseños
│   ├── Consejos de manicure
│   └── Artículo individual
├── Nosotros
├── Contacto y reservas
├── Preguntas frecuentes
├── Términos y condiciones
├── Política de privacidad
└── Página 404
```

### Objetivo de cada sección

- **Inicio (Landing):** Presentar Studio Milano, mostrar los diseños más destacados y dar una primera impresión profesional y confiable.
- **Servicios:** Informar sobre los tipos de manicure, los diseños disponibles, la duración de cada servicio y sus respectivos precios.
- **Blog:** Compartir consejos de cuidado, tendencias de temporada y recomendaciones para mantener las uñas bonitas y saludables.
- **Nosotros:** Presentar la historia, la identidad, las especialistas y la propuesta de valor cercana de Studio Milano.
- **Contacto y reservas:** Facilitar la comunicación directa con las clientas y permitir que soliciten una hora online o vía WhatsApp.
- **Preguntas frecuentes:** Resolver dudas comunes sobre los servicios, formas de pago, duración, cuidados posteriores y políticas de reserva.
- **Términos y condiciones:** Explicar las condiciones de agendamiento, políticas de cancelación, abonos y prestación de los servicios.
- **Política de privacidad:** Informar de forma transparente cómo se resguardan y utilizan los datos personales entregados por las clientas.
- **Página 404:** Orientar a las visitantes cuando ingresen a un enlace roto o página inexistente, ofreciéndoles un acceso rápido para volver al inicio.

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: Compra / Reserva de servicio

Recorrido de Antonella desde que descubre un diseño hasta que solicita su cita:

```text
Instagram (publicación de un diseño de nail art)
→ Inicio (Landing)
→ [Clic en "Ver servicios y precios"]
→ Servicios
→ [Filtra por "Esmaltado permanente" y revisa opciones]
→ Ficha de servicio: Esmaltado permanente con diseño personalizado
→ [Revisa duración (60 min), fotos de referencia y valor]
◇ ¿Tiene dudas con el diseño o disponibilidad?
   ├── Sí → [Clic en "Consultar por WhatsApp"] → WhatsApp de Studio Milano
   └── No → [Clic en "Reservar cita"]
→ Contacto y reservas
→ [Selecciona día viernes, horario disponible e ingresa sus datos]
→ Fin: Solicitud de reserva enviada con confirmación visual en pantalla
```

### Flujo 2: Contenido a conversión

Recorrido de Antonella desde una búsqueda de información hasta agendar o unirse a la comunidad:

```text
Buscador / Redes sociales ("cómo cuidar las uñas para que no se quiebren")
→ Blog
→ [Selecciona la categoría "Cuidados básicos de uñas"]
→ Artículo: "5 tips para que tu esmaltado permanente dure más de 3 semanas"
→ [Lee el artículo y revisa el servicio recomendado al final]
◇ ¿Desea agendar su atención?
   ├── Sí → [Clic en "Ver servicio de esmaltado permanente"] → Servicios → [Reservar hora]
   └── No → [Deja su correo en el formulario para recibir novedades y un 10 % de descuento]
          → Fin: Lead captado exitosamente
```

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de servicios

| Categoría | Servicios incluidos |
|---|---|
| **Manicure tradicional** | Manicure exprés, limpieza profunda de cutículas, limado y esmaltado tradicional, spa de manos e hidratación |
| **Esmaltado permanente** | Permanente unicolor, degradé / baby boomer, francesita clásica y moderna, efecto ojo de gato |
| **Uñas acrílicas o gel** | Uñas esculpidas en acrílico, sistema Soft Gel (press on), baño de acrílico en uña natural, kapping gel |
| **Diseños personalizados (Nail Art)** | Nail art minimalista (líneas, figuras geométricas), diseño a mano alzada complejo, encapsulados, cristales y apliques 3D |

### Categorías del blog

| Categoría | Idea de artículo | Necesidad o motivación de Antonella | Servicio relacionado |
|---|---|---|---|
| **Cuidados básicos de uñas** | "5 hábitos sencillos para que tu esmaltado permanente dure impecable por semanas" | Le frustra que el esmaltado se despegue o dañe rápido | Esmaltado permanente |
| **Tendencias en diseños** | "Top 6 tendencias de nail art que arrasan esta temporada en Santiago" | Le motiva probar diseños modernos y lucir uñas a la moda | Diseños personalizados |
| **Consejos de manicure** | "Acrílicas vs. Soft Gel: ¿cuál es la mejor opción para tus uñas naturales?" | Necesita conocer qué técnica le conviene según su rutina y presupuesto | Uñas acrílicas o gel |
