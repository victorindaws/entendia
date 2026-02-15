# Typography Reference

Sistema tipográfico para presentaciones EntendIA.

---

## Font Families

### Inter (Principal)

Fuente sans-serif geométrica moderna. Usar para todo el contenido.

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
```

**Pesos disponibles:**
- 400 (Regular) — Body text, subtítulos
- 500 (Medium) — Captions importantes
- 600 (SemiBold) — Énfasis
- 700 (Bold) — Títulos, headlines

### Caveat (Firma)

Fuente cursiva/handwriting. **Solo** para "IA" del logo y atribuciones de citas.

```css
@import url('https://fonts.googleapis.com/css2?family=Caveat:wght@500;600;700&display=swap');

font-family: 'Caveat', cursive;
```

**Pesos disponibles:**
- 500 (Medium) — Firmas
- 600 (SemiBold) — "IA" del logo
- 700 (Bold) — Énfasis decorativo

---

## Type Scale for Slides

Los tamaños son mayores que en documentos debido a la distancia de visualización en proyección.

| Elemento | Fuente | Peso | Tamaño | Line Height | Letter Spacing |
|----------|--------|------|--------|-------------|----------------|
| Display | Inter | 700 | 64pt | 1.1 | -0.03em |
| H1 (Title) | Inter | 700 | 48pt | 1.2 | -0.02em |
| H2 (Section) | Inter | 700 | 40pt | 1.2 | -0.01em |
| H3 (Slide Title) | Inter | 700 | 32pt | 1.25 | -0.01em |
| H4 (Subtitle) | Inter | 600 | 24pt | 1.3 | 0 |
| Body Large | Inter | 400 | 20pt | 1.5 | 0 |
| Body | Inter | 400 | 18pt | 1.6 | 0 |
| Caption | Inter | 400 | 14pt | 1.4 | 0 |
| Micro | Inter | 500 | 12pt | 1.4 | 0.02em |
| Quote | Inter | 400 Italic | 24pt | 1.5 | 0 |
| Attribution | Caveat | 600 | 20pt | 1.3 | 0.02em |

---

## Color by Element

### Dark Mode (#191C1F background)

| Elemento | Color | Hex/RGBA |
|----------|-------|----------|
| Display/H1 | White | #FFFFFF |
| H2/H3 Title | Teal | #14B8A6 |
| Subtitle | Muted | rgba(255,255,255,0.7) |
| Body | Muted | rgba(255,255,255,0.7) |
| Caption | Light Muted | rgba(255,255,255,0.5) |
| Quote | White | #FFFFFF |
| Attribution | Teal | #14B8A6 |
| Links | Teal | #14B8A6 |
| Emphasis | Amber | #E5B92B |

### Light Mode (#FAFAFA background)

| Elemento | Color | Hex |
|----------|-------|-----|
| Display/H1 | Dark | #191C1F |
| H2/H3 Title | Dark | #191C1F |
| Subtitle | Gray | #6B7280 |
| Body | Dark Gray | #374151 |
| Caption | Gray | #9CA3AF |
| Links | Teal | #0F9488 |
| Emphasis | Amber Dark | #D4A826 |

---

## CSS Implementation

```css
/* Import fonts */
@import url('https://fonts.googleapis.com/css2?family=Caveat:wght@500;600;700&family=Inter:wght@400;500;600;700&display=swap');

/* Base typography */
.reveal {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    font-size: 18px;
    line-height: 1.6;
    color: rgba(255, 255, 255, 0.7);
}

/* Headings */
.reveal h1 {
    font-size: 48px;
    font-weight: 700;
    line-height: 1.2;
    letter-spacing: -0.02em;
    color: #FFFFFF;
}

.reveal h2 {
    font-size: 40px;
    font-weight: 700;
    line-height: 1.2;
    letter-spacing: -0.01em;
    color: #14B8A6;
}

.reveal h3 {
    font-size: 32px;
    font-weight: 700;
    line-height: 1.25;
    letter-spacing: -0.01em;
    color: #14B8A6;
}

.reveal h4 {
    font-size: 24px;
    font-weight: 600;
    line-height: 1.3;
    color: rgba(255, 255, 255, 0.7);
}

/* Body text */
.reveal p {
    font-size: 18px;
    font-weight: 400;
    line-height: 1.6;
    color: rgba(255, 255, 255, 0.7);
}

.reveal .lead {
    font-size: 20px;
}

/* Lists */
.reveal ul, .reveal ol {
    font-size: 18px;
    line-height: 1.6;
}

.reveal li {
    margin-bottom: 12px;
}

/* Quotes */
.reveal blockquote {
    font-size: 24px;
    font-style: italic;
    font-weight: 400;
    line-height: 1.5;
    color: #FFFFFF;
}

.reveal .attribution {
    font-family: 'Caveat', cursive;
    font-size: 20px;
    font-weight: 600;
    color: #14B8A6;
}

/* Captions */
.reveal .caption,
.reveal .source {
    font-size: 14px;
    font-weight: 400;
    line-height: 1.4;
    color: rgba(255, 255, 255, 0.5);
}

/* Logo wordmark */
.logo-entend {
    font-family: 'Inter', sans-serif;
    font-weight: 700;
    letter-spacing: 0.5px;
    color: #FFFFFF;
}

.logo-ia {
    font-family: 'Caveat', cursive;
    font-weight: 600;
    font-size: 1.2em;
    letter-spacing: 1px;
    color: #14B8A6;
}

/* Emphasis */
.reveal strong {
    font-weight: 700;
    color: #FFFFFF;
}

.reveal em {
    font-style: italic;
}

.reveal .highlight {
    color: #E5B92B;
    font-weight: 600;
}

.reveal a {
    color: #14B8A6;
    text-decoration: none;
}

.reveal a:hover {
    color: #2DD4BF;
}
```

---

## Text Transforms

| Uso | Transform | Ejemplo |
|-----|-----------|---------|
| Section Dividers | UPPERCASE | NUESTRA SOLUCIÓN |
| Title Slides | Normal o UPPERCASE | EntendIA para Retail |
| Slide Titles | Normal | Beneficios del Sistema |
| Body Text | Normal | Nunca uppercase |

---

## Alignment Rules

| Tipo de Slide | Título | Body |
|---------------|--------|------|
| Title | Center | Center |
| Section Divider | Center | — |
| Content | Left | Left |
| Image + Text | Left | Left |
| Data/Chart | Center | Center |
| Quote | Center | Center |
| Closing | Center | Center |

---

## Spacing Guidelines

### Vertical Spacing

| Entre... | Espacio |
|----------|---------|
| Título y subtítulo | 16px |
| Título y body | 32px |
| Párrafos | 24px |
| List items | 12px |
| Secciones | 48px |

### Márgenes de Slide

- **Safe zone**: 5% desde todos los bordes
- **Contenido principal**: centrado en el 90% interior
- **Logo corner**: 32px desde esquina

---

## Best Practices

1. **Máximo 3 niveles de jerarquía** por slide (título, subtítulo, body)
2. **6-8 palabras máximo** por bullet point
3. **No más de 6 bullets** por slide
4. **Una idea = un slide** — si necesitas más, divide
5. **Contraste mínimo** 4.5:1 para accesibilidad
6. **Nunca** texto menor a 14pt en slides
7. **Caveat solo** para "IA" y firmas — nunca para body text
