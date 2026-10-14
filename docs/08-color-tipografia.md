# Color y tipografía — Studio Milano

> Guía: [Color y tipografía](../evaluacion/guias/fase-2-specs/05-color-y-tipografia.md)

## Paleta

| Rol | Color | HEX | Uso |
|---|---|---|---|
| **Principal** | Rosado | `#D98CA7` | Botones principales, enlaces y elementos destacados |
| **Secundario** | Rosado claro | `#F5DCE5` | Fondos de secciones, tarjetas y detalles decorativos |
| **Acento** | Dorado | `#C5A253` | Bordes, pequeños detalles, íconos y adornos |
| **Fondo** | Blanco | `#FFFFFF` | Fondo general del sitio para mantenerlo limpio y luminoso |
| **Texto** | Café oscuro | `#49343D` | Títulos y textos principales para facilitar la lectura |
| **Éxito** | Verde | `#2E7D32` | Mensajes de confirmación y alertas positivas |
| **Error** | Rojo | `#B3261E` | Mensajes de error en formularios y validaciones |

> **Regla 60-30-10:** Aproximadamente 60 % de blanco y tonos neutros (fondos y espacios limpios), 30 % de rosado claro (fondos de tarjetas y secciones) y 10 % de rosado principal y dorado (botones, llamados a la acción y detalles).

## Contraste

Verificado según las pautas de accesibilidad WCAG en el [verificador de contraste WebAIM](https://webaim.org/resources/contrastchecker/):

| Combinación | Ratio | Resultado | Uso recomendado |
|---|---|---|---|
| Café oscuro (`#49343D`) sobre Blanco (`#FFFFFF`) | 11.4:1 | AA / AAA ✅ | Textos principales de párrafos y títulos |
| Café oscuro (`#49343D`) sobre Rosado claro (`#F5DCE5`) | 8.8:1 | AA / AAA ✅ | Textos sobre tarjetas y fondos de sección |
| Café oscuro (`#49343D`) sobre Dorado (`#C5A253`) | 4.7:1 | AA ✅ | Botones secundarios y badges con texto |
| Café oscuro (`#49343D`) sobre Rosado (`#D98CA7`) | 4.5:1 | AA ✅ | Botones principales y elementos interactivos |
| Blanco (`#FFFFFF`) sobre Verde éxito (`#2E7D32`) | 5.1:1 | AA ✅ | Mensajes de confirmación y alertas de éxito |
| Blanco (`#FFFFFF`) sobre Rojo error (`#B3261E`) | 6.5:1 | AA ✅ | Alertas de error en formularios |
| Blanco (`#FFFFFF`) sobre Rosado principal (`#D98CA7`) | 2.5:1 | No alcanza AA ❌ | Evitar: usar texto café oscuro sobre rosado |
| Blanco (`#FFFFFF`) sobre Dorado (`#C5A253`) | 2.4:1 | No alcanza AA ❌ | Evitar: usar texto café oscuro sobre dorado |

## Tipografía

- **Títulos:** [Playfair Display](https://fonts.google.com/specimen/Playfair+Display) — Letra serif elegante y sofisticada que ayuda a destacar la marca Studio Milano y los encabezados.
- **Textos:** [Montserrat](https://fonts.google.com/specimen/Montserrat) — Letra sans-serif moderna, limpia y de excelente legibilidad en descripciones, precios, menús y celulares.

### Escala de tamaños de texto

| Elemento | Desktop | Mobile | Peso |
|---|---|---|---|
| **h1** | 3rem (48px) | 2rem (32px) | 700 (Bold) |
| **h2** | 2.25rem (36px) | 1.75rem (28px) | 700 (Bold) |
| **h3** | 1.5rem (24px) | 1.25rem (20px) | 600 (SemiBold) |
| **Párrafo** | 1rem (16px) | 1rem (16px) | 400 (Regular) |
| **Botón** | 1rem (16px) | 1rem (16px) | 600 (SemiBold) |

## Justificación

Elegí el rosado porque representa la feminidad, la belleza y la delicadeza, características que identifican la propuesta de Studio Milano. El dorado aporta un toque elegante y sofisticado que evoca exclusividad, mientras que el blanco permite que el sitio se vea ordenado, luminoso y moderno, dando protagonismo a las fotos de las uñas.

La combinación tipográfica de Playfair Display en títulos y Montserrat en textos logra el equilibrio perfecto entre estilo y funcionalidad: proyecta una imagen profesional y cuidada, garantizando a la vez que clientas como Antonella revisen servicios, comparen precios y reserven sin ninguna dificultad visual desde sus dispositivos móviles.
