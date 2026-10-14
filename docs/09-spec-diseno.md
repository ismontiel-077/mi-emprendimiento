# Spec de diseño — Studio Milano

> Guía: [Spec de diseño](../evaluacion/guias/fase-2-specs/06-spec-de-diseno.md)

La spec de diseño tiene dos partes:

1. **[`DESIGN.md`](../DESIGN.md)** (en la raíz): tu design system, en el formato que Stitch importa.
2. **Este documento:** tus pantallas, escritas como prompts listos para pegar en Stitch.

**Wireframes en Whimsical:** [pega aquí el link]

> Guía de wireframes: [Wireframes](../evaluacion/guias/fase-2-specs/04-wireframes.md)

![Wireframes](img/componentes.png)

## Pantallas

### 1. Inicio (Landing)

```text
Pantalla: Inicio de Studio Milano, versión desktop. Usa el design system del proyecto.
Objetivo: Presentar el emprendimiento, mostrar su estilo y conseguir que las clientas reserven una hora.
Componentes, de arriba hacia abajo:
1. Navbar con el logo Studio Milano y enlaces Inicio, Servicios, Blog, Nosotros y Contacto. Incluye botón button-primary "Reservar hora".
2. Hero con el título "Belleza y estilo en cada detalle", un texto breve y una fotografía de uñas elegantes.
3. Botón principal button-primary "Reservar hora" y botón secundario button-secondary "Ver servicios".
4. Sección "Nuestros servicios" con una grilla de tres columnas de card-service para Manicure tradicional, Esmaltado permanente y Diseños personalizados.
5. Galería con fotografías reales de trabajos de nail art.
6. Sección de beneficios: atención personalizada, diseños modernos y cuidado de uñas.
7. Testimonios reales con tarjetas card-testimonial.
8. Footer con contacto, dirección y redes sociales.
```

### 2. Servicios

```text
Pantalla: Servicios de Studio Milano, versión desktop. Usa el design system del proyecto.
Objetivo: Ayudar a las clientas a conocer los servicios, comparar opciones y elegir una manicure.
Componentes, de arriba hacia abajo:
1. Navbar.
2. Título h1 "Nuestros servicios" y texto introductorio.
3. Barra de categorías con chips: Todos (activo), Manicure tradicional, Esmaltado permanente y Diseños personalizados.
4. Grilla de tres columnas con tarjetas card-service.
5. Cada tarjeta card-service tendrá una imagen, nombre del servicio, descripción breve, duración aproximada, precio visible y botón button-primary "Reservar hora".
6. Bloque de contacto con botón button-secondary para resolver dudas por WhatsApp.
7. Footer.
```

### 3. Detalle del servicio

```text
Pantalla: Detalle del servicio de Studio Milano, versión desktop. Usa el design system del proyecto.
Objetivo: Explicar en qué consiste un servicio y facilitar la reserva inmediata.
Componentes, de arriba hacia abajo:
1. Navbar.
2. Ruta de navegación (breadcrumbs): Inicio > Servicios > Detalle.
3. Distribución en dos columnas: a la izquierda, imagen grande del diseño de uñas; a la derecha, nombre del servicio en headline-lg, descripción detallada, duración aproximada y precio destacado.
4. Botón principal button-primary "Reservar hora" y botón secundario "Consultar por WhatsApp".
5. Sección con consejos de cuidado posterior del servicio.
6. Sección de diseños relacionados con tarjetas card-service.
7. Footer.
```

### 4. Blog

```text
Pantalla: Blog de Studio Milano, versión desktop. Usa el design system del proyecto.
Objetivo: Ofrecer consejos útiles para el cuidado de uñas y mostrar las últimas tendencias en nail art.
Componentes, de arriba hacia abajo:
1. Navbar.
2. Título h1 "Consejos y tendencias" y texto introductorio.
3. Categorías con chips: Cuidados básicos, Tendencias y Consejos de manicure.
4. Grilla de tres columnas con tarjetas card-blog.
5. Cada tarjeta card-blog tendrá una imagen, tag-accent de categoría, título del artículo, resumen breve y botón "Leer más".
6. Footer.
```

### 5. Artículo del blog

```text
Pantalla: Artículo del blog de Studio Milano, versión desktop. Usa el design system del proyecto.
Objetivo: Permitir que las clientas lean consejos de cuidado de uñas de forma cómoda y descubran servicios relacionados.
Componentes, de arriba hacia abajo:
1. Navbar.
2. Ruta de navegación: Inicio > Blog > Artículo.
3. Categoría en tag-accent, título del artículo en headline-display y fecha de publicación.
4. Imagen principal destacada con proporción consistente.
5. Contenido del artículo en tipografía body-md, organizado en subtítulos (headline-md), párrafos y bloques destacados con tips prácticos.
6. Enlace o botón secundario "Volver al blog".
7. Sección de artículos relacionados con tarjetas card-blog.
8. Footer.
```

### 6. Contacto y reservas

```text
Pantalla: Contacto y reservas de Studio Milano, versión desktop. Usa el design system del proyecto.
Objetivo: Facilitar que las clientas realicen consultas y soliciten una cita fácilmente.
Componentes, de arriba hacia abajo:
1. Navbar.
2. Título headline-lg "Agenda tu próxima manicure" y texto breve que invite a contactar.
3. Formulario con inputs para nombre, correo, teléfono, selector de servicio de interés, fecha preferida y campo de mensaje.
4. Botón principal button-primary "Enviar solicitud".
5. Información de contacto del estudio: dirección, mapa, horarios y enlace directo a WhatsApp.
6. Mensajes de validación y confirmación en estados input-error o alert.
7. Footer.
```

### Versión mobile (para cada pantalla)

```text
Genera la versión mobile (ancho máximo 767px) de esta pantalla siguiendo la sección Layout del design system:
- Mobile 1 (Inicio): Cambia la navegación por un menú desplegable, coloca el contenido en una sola columna, adapta la imagen principal al ancho disponible y mantén visible y accesible el botón "Reservar hora".
- Mobile 2 (Servicios): Coloca las tarjetas card-service en una columna vertical, conserva el nombre, descripción, precio y botón de reserva, y permite recorrer los chips de categoría sin desplazamiento horizontal en la página.
- Mobile 3 (Detalle del servicio): Distribución en una columna vertical con la imagen arriba y la información y precio debajo, manteniendo el botón "Reservar hora" destacado y fácil de pulsar.
- Mobile 4 (Blog): Coloca las tarjetas card-blog en una columna vertical, adaptando las imágenes al ancho y facilitando el acceso a los chips de categoría.
- Mobile 5 (Artículo): Contenido en una sola columna con imagen adaptable y tipografía optimizada para lectura en celular (body-md 16px), conservando subtítulos y tips destacados.
- Mobile 6 (Contacto y reservas): Todos los campos del formulario en una sola columna a ancho completo, con botón "Enviar solicitud" visible y mensajes de validación claros junto a cada campo.
```
