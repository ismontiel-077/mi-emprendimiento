# Spec de desarrollo — Studio Milano

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## 0. Insumos y prompt para el asistente

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.

En la carpeta stitch/ está el código exportado de Stitch de cada pantalla.

Construye el sitio web siguiendo exactamente las especificaciones del proyecto: solo HTML y CSS, estructura de archivos definida, navegación entre páginas, variables CSS en :root con los valores de DESIGN.md y estructura semántica de cada página.

Usa el código de Stitch solo como referencia visual. No utilices frameworks ni gestores de contenido.

Al terminar, revisa cada criterio de aceptación e indica cuáles se cumplen y cuáles no.
```

## 1. Estructura de archivos

```text
studio-milano/
├── index.html
├── servicios.html
├── detalle-servicio.html
├── blog.html
├── articulo.html
├── nosotros.html
├── contacto.html
├── preguntas-frecuentes.html
├── terminos.html
├── privacidad.html
├── 404.html
├── DESIGN.md
├── css/
│   └── styles.css
├── img/
│   ├── logo/
│   ├── servicios/
│   ├── galeria/
│   └── blog/
├── stitch/
│   ├── inicio/
│   ├── servicios/
│   ├── detalle-servicio/
│   ├── blog/
│   ├── articulo/
│   └── contacto/
└── docs/
    ├── 09-spec-diseno.md
    └── 10-spec-desarrollo.md
```

> **Nota:** La carpeta `stitch/` guardará los archivos exportados de Stitch únicamente como referencia visual. El sitio final utilizará HTML y CSS propios.

## 2. Páginas y navegación

La navegación principal estará disponible en todas las páginas e incluirá Inicio, Servicios, Blog, Nosotros y Contacto. También habrá un botón destacado para reservar una hora.

El pie de página incluirá enlaces a Preguntas frecuentes, Términos y condiciones, Política de privacidad y redes sociales.

### Enlaces entre páginas

| Página de origen | Elemento | Destino |
|---|---|---|
| `index.html` | Logo o enlace Inicio | `index.html` |
| `index.html` | Botón Ver servicios | `servicios.html` |
| `index.html` | Botón Reservar hora | `contacto.html` |
| `index.html` | Enlace Conócenos | `nosotros.html` |
| `servicios.html` | Botón Ver detalles | `detalle-servicio.html` |
| `detalle-servicio.html` | Botón Reservar hora | `contacto.html` |
| `blog.html` | Botón Leer más | `articulo.html` |
| `articulo.html` | Enlace Volver al blog | `blog.html` |
| Cualquier página | Enlace Contacto | `contacto.html` |
| Cualquier página | Enlace Preguntas frecuentes | `preguntas-frecuentes.html` |
| Cualquier página | Enlace Términos y condiciones | `terminos.html` |
| Cualquier página | Enlace Política de privacidad | `privacidad.html` |
| `404.html` | Botón Volver al inicio | `index.html` |

Las categorías de servicios y del blog serán filtros o enlaces dentro de sus respectivas páginas, no páginas HTML independientes.

El formulario de contacto permitirá enviar consultas o solicitudes de reserva. No se mostrará una reserva confirmada si no existe un sistema que la confirme.

## 3. Estructura semántica

Todas las páginas tendrán un `header` con la navegación, un `main` con el contenido principal y un `footer` con información complementaria.

### index.html

```html
<header>
  <nav aria-label="Navegación principal">
    <!-- Logo, enlaces y botón de reserva -->
  </nav>
</header>

<main>
  <section class="hero">
    <!-- Título, descripción e imagen -->
  </section>

  <section class="services">
    <!-- Tarjetas de servicios -->
  </section>

  <section class="gallery">
    <!-- Galería de diseños -->
  </section>

  <section class="benefits">
    <!-- Beneficios del emprendimiento -->
  </section>

  <section class="testimonials">
    <!-- Opiniones reales -->
  </section>
</main>

<footer>
  <!-- Contacto y enlaces legales -->
</footer>
```

### servicios.html

- `header`: navegación principal.
- `main`: contenido de servicios.
- `section`: título, categorías y grilla de servicios.
- `article`: cada tarjeta de servicio.
- `footer`: contacto y enlaces legales.

### detalle-servicio.html

- `header`: navegación principal.
- `main`: información del servicio.
- `section`: imagen, nombre, descripción y precio.
- `section`: recomendaciones o cuidados.
- `section`: servicios relacionados.
- `footer`: información complementaria.

### blog.html

- `header`: navegación principal.
- `main`: contenido del blog.
- `section`: título y categorías.
- `section`: grilla de artículos.
- `article`: cada tarjeta de artículo.
- `footer`: contacto y enlaces legales.

### articulo.html

- `header`: navegación principal.
- `main`: contenido del artículo.
- `article`: título, imagen, fecha y texto.
- `section`: artículos relacionados.
- `footer`: información complementaria.

### nosotros.html

- `header`: navegación principal.
- `main`: presentación de Studio Milano.
- `section`: historia, objetivos y propuesta de valor.
- `section`: fotografías del emprendimiento, si están disponibles.
- `footer`: enlaces y contacto.

### contacto.html

- `header`: navegación principal.
- `main`: información de contacto.
- `section`: formulario de consultas y reservas.
- `section`: medios de contacto y redes sociales.
- `footer`: enlaces legales.

### preguntas-frecuentes.html

- `header`: navegación principal.
- `main`: título y lista de preguntas.
- `section`: preguntas y respuestas.
- `footer`: enlaces complementarios.

### terminos.html y privacidad.html

- `header`: navegación principal.
- `main`: título y contenido legal.
- `section`: apartados correspondientes a cada documento.
- `footer`: enlaces y contacto.

### 404.html

- `header`: navegación principal.
- `main`: mensaje de página no encontrada y botón para regresar.
- `footer`: enlaces principales.

## 4. Organización del CSS

Todos los estilos se encontrarán en `css/styles.css`. Se utilizarán nombres de clases en inglés, escritos en minúsculas y separados por guiones.

### Variables de diseño

Los valores estarán basados en `DESIGN.md`.

```css
:root {
  /* Colores */
  --color-primary: #A84F70;
  --color-primary-hover: #8E3E5D;
  --color-primary-active: #78314C;
  --color-secondary: #F5DCE5;
  --color-tertiary: #C5A253;
  --color-tertiary-strong: #8A6828;
  --color-bg: #FFFBFC;
  --color-surface: #FFFFFF;
  --color-text: #49343D;
  --color-text-on-primary: #FFFFFF;
  --color-text-on-secondary: #49343D;
  --color-text-on-tertiary: #33261D;
  --color-border: #E6D5DC;
  --color-error: #B3261E;
  --color-success: #2E7D32;

  /* Tipografía */
  --font-title: "Playfair Display", serif;
  --font-body: "Montserrat", sans-serif;

  /* Espaciados */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;

  /* Radios */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --radius-full: 9999px;

  /* Layout */
  --container-width: 1200px;
}
```

Todos los colores del sitio deberán utilizar las variables de `:root`. Si se modifica un valor, primero se actualizará `DESIGN.md` y después el CSS.

### Clases principales

- `.navbar`: barra de navegación.
- `.hero`: presentación inicial.
- `.section-title`: título de sección.
- `.services-grid`: grilla de servicios.
- `.service-card`: tarjeta de servicio.
- `.blog-grid`: grilla de artículos.
- `.article-card`: tarjeta de artículo.
- `.btn-primary`: botón principal.
- `.btn-secondary`: botón secundario.
- `.contact-form`: formulario de contacto.
- `.form-input`: campo de formulario.
- `.footer`: pie de página.

### Responsive

El sitio se diseñará primero para celulares.

```css
/* Mobile: hasta 767 px */
@media (max-width: 767px) {
  .services-grid,
  .blog-grid {
    grid-template-columns: 1fr;
  }
}

/* Tablet: 768 px a 1023 px */
@media (min-width: 768px) and (max-width: 1023px) {
  .services-grid,
  .blog-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

/* Desktop: desde 1024 px */
@media (min-width: 1024px) {
  .services-grid,
  .blog-grid {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }
}
```

El menú será desplegable en celulares y horizontal en pantallas grandes. Las imágenes serán adaptables y los formularios ocuparán el ancho disponible sin generar desplazamiento horizontal.

## 5. Criterios de aceptación

### Navegación

- [ ] La barra de navegación y el pie de página mantienen una estructura consistente en todas las páginas.
- [ ] Los enlaces principales llevan a sus destinos correctos.
- [ ] Se puede recorrer el flujo Inicio → Servicios → Detalle del servicio → Contacto.
- [ ] Se puede recorrer el flujo Blog → Artículo → Blog.
- [ ] La página 404 permite volver al inicio.
- [ ] No existen enlaces internos rotos.

### Funcionalidades

- [ ] La página de inicio presenta Studio Milano y sus principales servicios.
- [ ] Las tarjetas de servicios muestran nombre, descripción, precio y acceso al detalle.
- [ ] La página de detalle presenta la información del servicio.
- [ ] El blog muestra artículos y permite abrirlos.
- [ ] El formulario de contacto valida los campos obligatorios.
- [ ] Los mensajes de error se muestran cuando corresponde.
- [ ] La página de preguntas frecuentes presenta respuestas claras.
- [ ] Los enlaces a redes sociales y medios de contacto funcionan cuando se han configurado.

### Diseño

- [ ] Los colores provienen de las variables de `:root`.
- [ ] Se utilizan Playfair Display para títulos y Montserrat para textos.
- [ ] Los botones principales tienen estados normal, hover, active y disabled.
- [ ] Las tarjetas respetan los radios y espaciados de `DESIGN.md`.
- [ ] Los precios se muestran de forma clara.
- [ ] Las fotografías corresponden a los servicios y tienen texto alternativo.

### Responsive

- [ ] El diseño se adapta a celulares, tablets y computadores.
- [ ] En celular, las tarjetas aparecen en una columna.
- [ ] En tablet, las tarjetas aparecen en dos columnas.
- [ ] En escritorio, las tarjetas aparecen en tres columnas.
- [ ] No existe desplazamiento horizontal a 375 px de ancho.
- [ ] Los botones y campos pueden utilizarse cómodamente desde un celular.

### Accesibilidad y publicación

- [ ] Cada página tiene un solo título principal `h1`.
- [ ] Las imágenes informativas tienen atributos `alt` descriptivos.
- [ ] Los formularios tienen etiquetas asociadas a sus campos.
- [ ] Los enlaces y botones pueden identificarse y utilizarse con teclado.
- [ ] Los textos tienen contraste suficiente.
- [ ] Las páginas utilizan HTML semántico.
- [ ] El sitio funciona sin frameworks ni gestores de contenido.
- [ ] El sitio está publicado y se puede navegar desde GitHub Pages.

## 6. Revisión final

Antes de entregar el proyecto, comprobaré cada criterio de aceptación en el navegador, revisaré la versión móvil y verificaré que las páginas, imágenes, enlaces y formularios funcionen correctamente.
Los criterios se marcarán como cumplidos solo después de probarlos. Si alguna funcionalidad requiere un servicio externo, como el envío real de formularios o la confirmación de reservas, se indicará claramente si está implementada o pendiente.
