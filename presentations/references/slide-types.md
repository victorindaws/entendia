# Slide Types Reference

Guía detallada de cada tipo de slide para presentaciones EntendIA.

---

## 1. Title Slide

El primer slide de la presentación. Establece el tono y la marca.

### Estructura

```
┌─────────────────────────────────────────────────┐
│                                                 │
│                                                 │
│              [Logo EntendIA]                    │
│              ~35% del ancho                     │
│                                                 │
│           ─────── teal line ───────             │
│                                                 │
│              TÍTULO PRINCIPAL                   │
│              Inter Bold 48pt                    │
│                                                 │
│              Subtítulo descriptivo              │
│              Inter Regular 24pt                 │
│                                                 │
│                                                 │
└─────────────────────────────────────────────────┘
```

### Especificaciones

| Propiedad | Dark Mode | Light Mode |
|-----------|-----------|------------|
| Background | #191C1F | #FAFAFA |
| Título | #FFFFFF | #191C1F |
| Subtítulo | rgba(255,255,255,0.7) | #6B7280 |
| Línea accent | #14B8A6 (3px) | #14B8A6 (3px) |

### HTML Example

```html
<section class="title-slide" data-background-color="#191C1F">
    <div class="logo">
        <span class="logo-entend">Entend</span><span class="logo-ia">IA</span>
    </div>
    <div class="accent-line"></div>
    <h1>TÍTULO DE LA PRESENTACIÓN</h1>
    <p class="subtitle">Subtítulo descriptivo aquí</p>
</section>
```

---

## 2. Section Divider

Separa secciones mayores de la presentación. Fondo teal distintivo.

### Estructura

```
┌─────────────────────────────────────────────────┐
│                                   ░░░░░░░░░░░░░ │
│                                   ░ Isotipo  ░░ │
│                                   ░ 20% opac ░░ │
│         NOMBRE DE SECCIÓN                    ░░ │
│         Inter Bold 48pt                      ░░ │
│         #191C1F (negro)                      ░░ │
│                                   ░░░░░░░░░░░░░ │
│                                   ░░░░░░░░░░░░░ │
└─────────────────────────────────────────────────┘
        Fondo: #14B8A6 (teal)
```

### Especificaciones

| Propiedad | Valor |
|-----------|-------|
| Background | #14B8A6 |
| Título | #191C1F, Inter Bold 48pt |
| Transform | UPPERCASE |
| Isotipo | 20% opacity, derecha, grande |

### HTML Example

```html
<section class="section-divider" data-background-color="#14B8A6">
    <h2>NOMBRE DE SECCIÓN</h2>
    <div class="isotipo-watermark"></div>
</section>
```

---

## 3. Content Slide

El slide más común. Para bullets, texto explicativo, y contenido general.

### Estructura

```
┌─────────────────────────────────────────────────┐
│ [Logo]                                          │
│                                                 │
│ TÍTULO DEL SLIDE                                │
│ Inter Bold 32pt, Teal                           │
│                                                 │
│ ■ Punto número uno con información              │
│   relevante que puede ocupar dos líneas         │
│                                                 │
│ ■ Punto número dos más breve                    │
│                                                 │
│ ■ Punto número tres                             │
│                                                 │
│                                                 │
└─────────────────────────────────────────────────┘
```

### Variantes

**Single Column** (default)
- Máximo 6-8 bullets
- Texto alineado izquierda
- 60% del ancho para contenido

**Two Columns**
- Para comparaciones o listas paralelas
- Máximo 4 bullets por columna
- Gap de 48px entre columnas

### Especificaciones

| Propiedad | Dark Mode | Light Mode |
|-----------|-----------|------------|
| Background | #191C1F | #FAFAFA |
| Título | #14B8A6 | #191C1F |
| Body | rgba(255,255,255,0.7) | #374151 |
| Bullets | #14B8A6 (■) | #14B8A6 (■) |

### HTML Example

```html
<section class="content-slide" data-background-color="#191C1F">
    <div class="logo-corner"></div>
    <h3>TÍTULO DEL CONTENIDO</h3>
    <ul>
        <li>Primer punto importante</li>
        <li>Segundo punto con más detalle que puede extenderse</li>
        <li>Tercer punto conciso</li>
    </ul>
</section>
```

---

## 4. Image + Text Slide

Para combinar visual con explicación.

### Estructura

```
┌────────────────────┬────────────────────────────┐
│                    │ [Logo]                     │
│                    │                            │
│                    │ TÍTULO                     │
│      IMAGEN        │                            │
│      50-60%        │ Texto explicativo que      │
│      full-bleed    │ acompaña la imagen y       │
│                    │ proporciona contexto.      │
│                    │                            │
│                    │ ■ Punto adicional          │
│                    │                            │
└────────────────────┴────────────────────────────┘
```

### Variantes

**50/50 Split** — Balance igual
**60/40 Split** — Imagen dominante
**40/60 Split** — Texto dominante

### Especificaciones

| Propiedad | Valor |
|-----------|-------|
| Layout | CSS Grid o Flexbox |
| Gap | 0px (imagen full-bleed) |
| Image treatment | Opcional: overlay teal 10% |
| Text side bg | #191C1F o #FAFAFA |

### HTML Example

```html
<section class="image-text-slide" data-background-color="#191C1F">
    <div class="image-side">
        <img src="imagen.jpg" alt="Descripción">
    </div>
    <div class="text-side">
        <div class="logo-corner"></div>
        <h3>TÍTULO</h3>
        <p>Texto explicativo...</p>
    </div>
</section>
```

---

## 5. Data / Chart Slide

Para gráficos, métricas, y visualización de datos.

### Estructura

```
┌─────────────────────────────────────────────────┐
│ [Logo]                                          │
│                                                 │
│              TÍTULO DEL GRÁFICO                 │
│                                                 │
│        ┌─────────────────────────────┐          │
│        │                             │          │
│        │       CHART / GRAPH         │          │
│        │         80% width           │          │
│        │                             │          │
│        └─────────────────────────────┘          │
│                                                 │
│ Fuente: Datos internos, 2026                    │
└─────────────────────────────────────────────────┘
```

### Paleta de Datos

Usar en este orden:
1. **#14B8A6** — Teal (primario)
2. **#0F9488** — Teal Dark (secundario)
3. **#E5B92B** — Amber (highlight)
4. **#2DD4BF** — Teal Light (terciario)

### Especificaciones

| Propiedad | Dark Mode | Light Mode |
|-----------|-----------|------------|
| Background | #191C1F | #FAFAFA |
| Chart bg | transparent | transparent |
| Grid lines | rgba(255,255,255,0.1) | rgba(0,0,0,0.1) |
| Labels | rgba(255,255,255,0.7) | #6B7280 |

### HTML Example

```html
<section class="data-slide" data-background-color="#191C1F">
    <div class="logo-corner"></div>
    <h3>MÉTRICAS DE RENDIMIENTO</h3>
    <div class="chart-container">
        <!-- Chart.js, SVG, o imagen -->
    </div>
    <p class="source">Fuente: Datos internos, Q1 2026</p>
</section>
```

---

## 6. Quote Slide

Para testimonios, citas destacadas, o afirmaciones importantes.

### Estructura

```
┌─────────────────────────────────────────────────┐
│                                                 │
│     "                                           │
│                                                 │
│        "Cita importante que queremos            │
│         destacar y que transmite un             │
│         mensaje clave."                         │
│                                                 │
│                          — Nombre Persona       │
│                            Cargo, Empresa       │
│                                                 │
└─────────────────────────────────────────────────┘
        Fondo: #191C1F
        Comillas: #E5B92B (grande, decorativo)
        Cita: Blanco, Inter Italic
        Firma: Caveat, Teal
```

### Especificaciones

| Propiedad | Valor |
|-----------|-------|
| Background | #191C1F (solo dark mode) |
| Comillas | #E5B92B, 120pt, decorativo |
| Quote text | #FFFFFF, Inter Italic 24pt |
| Attribution | #14B8A6, Caveat 20pt |
| Cargo | rgba(255,255,255,0.5), Inter 14pt |

### HTML Example

```html
<section class="quote-slide" data-background-color="#191C1F">
    <div class="quote-mark">"</div>
    <blockquote>
        "La IA de EntendIA transformó nuestra operación en semanas, no meses."
    </blockquote>
    <div class="attribution">
        <span class="name">— María García</span>
        <span class="title">CEO, TechCorp</span>
    </div>
</section>
```

---

## 7. Diagram Slide (Excalidraw)

Para diagramas técnicos, flujos, arquitecturas.

### Estructura

```
┌─────────────────────────────────────────────────┐
│ [Logo]                                          │
│                                                 │
│              TÍTULO (opcional)                  │
│                                                 │
│     ┌─────────────────────────────────────┐     │
│     │                                     │     │
│     │      DIAGRAMA EXCALIDRAW SVG        │     │
│     │      Estilo hand-drawn              │     │
│     │      Paleta EntendIA                │     │
│     │                                     │     │
│     └─────────────────────────────────────┘     │
│                                                 │
└─────────────────────────────────────────────────┘
```

### Especificaciones

Ver `references/excalidraw.md` para guía completa de generación.

| Propiedad | Dark Mode | Light Mode |
|-----------|-----------|------------|
| Background | #191C1F | #FAFAFA |
| SVG bg | transparent | transparent |
| Stroke | #14B8A6 | #14B8A6 |
| Fill | rgba(20,184,166,0.2) | rgba(20,184,166,0.2) |

### HTML Example

```html
<section class="diagram-slide" data-background-color="#191C1F">
    <div class="logo-corner"></div>
    <h3>ARQUITECTURA DEL SISTEMA</h3>
    <div class="diagram">
        <img src="diagrama.svg" alt="Arquitectura">
    </div>
</section>
```

---

## 8. Closing Slide

El slide final. Call-to-action y contacto.

### Estructura

```
┌─────────────────────────────────────────────────┐
│                                                 │
│                                                 │
│              [Logo EntendIA]                    │
│              Grande, centrado                   │
│                                                 │
│    "No esperamos al futuro. Lo construimos."    │
│                                                 │
│           ─────── teal line ───────             │
│                                                 │
│              hello@entendia.ai                  │
│              entendia.ai                        │
│                                                 │
│                                                 │
└─────────────────────────────────────────────────┘
```

### Especificaciones

| Propiedad | Dark Mode | Light Mode |
|-----------|-----------|------------|
| Background | #191C1F | #FAFAFA |
| Logo | Igual que title slide | Igual que title slide |
| Tagline | #FFFFFF, Inter Bold 24pt | #191C1F |
| Línea | #14B8A6, 3px | #14B8A6, 3px |
| Contacto | #14B8A6, Inter Regular 18pt | #14B8A6 |

### HTML Example

```html
<section class="closing-slide" data-background-color="#191C1F">
    <div class="logo">
        <span class="logo-entend">Entend</span><span class="logo-ia">IA</span>
    </div>
    <p class="tagline">No esperamos al futuro. Lo construimos.</p>
    <div class="accent-line"></div>
    <div class="contact">
        <p>hello@entendia.ai</p>
        <p>entendia.ai</p>
    </div>
</section>
```

---

## Slide Selection Guide

| Necesitas... | Usa... |
|--------------|--------|
| Abrir la presentación | Title Slide |
| Separar secciones | Section Divider |
| Explicar con bullets | Content Slide |
| Mostrar producto/visual | Image + Text |
| Presentar datos | Data / Chart |
| Destacar testimonio | Quote Slide |
| Explicar flujo/arquitectura | Diagram Slide |
| Cerrar y CTA | Closing Slide |
