---
name: entendia-presentations
description: Generación de presentaciones reveal.js con el branding EntendIA v2.1. Estilo tech-forward, minimalista, fondo negro con accents teal y amber. Usa este skill para crear decks profesionales, pitches, y presentaciones de producto.
---

# EntendIA Presentations Skill

Crea presentaciones profesionales usando reveal.js con la identidad visual EntendIA v2.1.

**Keywords**: presentaciones, slides, reveal.js, pitch deck, branding, EntendIA, dark mode, tech

---

## Quick Start

1. Lee `references/slide-types.md` para entender los tipos de slides disponibles
2. Lee `references/typography.md` para las reglas de texto
3. Usa `assets/base-dark.html` o `assets/base-light.html` como plantilla
4. Para diagramas, consulta `references/excalidraw.md`

---

## Slide Dimensions

- **Standard**: 16:9 (1280 × 720 px)
- **Margins/safe zone**: 5% inset desde todos los bordes
- **Logo**: solo en esquinas o centro, nunca más del 10% del ancho del slide

---

## Slide Types

### 1. Title Slide
- **Background**: #191C1F (dark) / #FAFAFA (light)
- **Logo**: centrado, 35% del ancho del slide
- **Título**: Inter Bold 48pt, blanco o #191C1F, centrado
- **Subtítulo**: Inter Regular 24pt, rgba(255,255,255,0.7), centrado
- **Accent**: línea teal (#14B8A6) de 3px entre título y subtítulo (opcional)

### 2. Section Divider
- **Background**: #14B8A6 (teal) — igual en dark y light mode
- **Título sección**: Inter Bold 48pt, #191C1F, UPPERCASE, centrado vertical
- **Isotipo**: watermark opcional al 20% opacity, posicionado a la derecha

### 3. Content Slide
- **Background**: #191C1F (dark) / #FAFAFA (light)
- **Logo**: esquina superior izquierda, pequeño
- **Título**: Inter Bold 32pt, #14B8A6 (dark) o #191C1F (light), alineado izquierda
- **Body**: Inter Regular 18pt, rgba(255,255,255,0.7) (dark) o #374151 (light)
- **Bullets**: cuadrados teal, 18pt
- **Máximo 2 columnas** para contenido denso

### 4. Image + Text Slide
- **Layout**: split 50/50 o 60/40
- **Lado imagen**: full-bleed, con overlay teal sutil si necesario
- **Lado texto**: fondo #191C1F o #FAFAFA
- **Logo**: en el lado del texto, esquina alineada

### 5. Data / Chart Slide
- **Background**: #191C1F (dark) / #FAFAFA (light)
- **Chart area**: centrada, máximo 80% del ancho
- **Colores de datos**: #14B8A6, #0F9488, #E5B92B, #2DD4BF
- **Data labels**: Inter Regular 14pt
- **Fuente**: Inter Regular 10pt, esquina inferior izquierda, rgba(255,255,255,0.5)

### 6. Quote Slide
- **Background**: #191C1F (solo dark mode)
- **Comillas decorativas**: #E5B92B (amber), grande, arriba izquierda
- **Quote**: Inter Italic 24pt, blanco, centrado
- **Atribución**: Caveat 20pt, #14B8A6, debajo de la cita

### 7. Diagram Slide (Excalidraw)
- **Background**: #191C1F (dark) / #FAFAFA (light)
- **Diagrama**: SVG generado con Excalidraw MCP
- **Estilo**: hand-drawn, colores EntendIA
- **Título opcional**: Inter Bold 28pt, arriba centrado

### 8. Closing Slide
- **Background**: #191C1F (dark) / #FAFAFA (light)
- **Logo**: centrado, mismo tamaño que title slide
- **Tagline**: "No esperamos al futuro. Lo construimos." — Inter Bold 24pt, blanco
- **Contacto**: Inter Regular 18pt, #14B8A6
- **Website/email**: rgba(255,255,255,0.7)

---

## Color Usage

### Background Assignment

| Slide Type | Background Dark | Background Light |
|------------|-----------------|------------------|
| Title | #191C1F | #FAFAFA |
| Section | #14B8A6 | #14B8A6 |
| Content | #191C1F | #FAFAFA |
| Image+Text | #191C1F | #FAFAFA |
| Data/Chart | #191C1F | #FAFAFA |
| Quote | #191C1F | — (solo dark) |
| Diagram | #191C1F | #FAFAFA |
| Closing | #191C1F | #FAFAFA |

### Accent Colors

| Color | Hex | Uso |
|-------|-----|-----|
| Teal | #14B8A6 | Accents principales, títulos, links, "IA" del logo |
| Amber | #E5B92B | CTAs, comillas decorativas, highlights importantes |
| Teal Dark | #0F9488 | Hover states, gradientes |
| Teal Light | #2DD4BF | Datos secundarios en charts |

### Reglas de Color

1. **Amber solo para CTAs y decoración** — nunca como fondo completo
2. **Teal es el accent principal** — usar para destacar información clave
3. **Máximo 3 colores por slide** (fondo + 2 accents)
4. **Sin colores saturados adicionales** — la paleta es teal + amber, nada más

---

## Typography

Ver `references/typography.md` para detalles completos.

| Elemento | Fuente | Peso | Tamaño | Color (Dark) |
|----------|--------|------|--------|--------------|
| Slide Title | Inter | 700 | 32-48pt | Blanco o Teal |
| Subtitle | Inter | 400 | 20-24pt | rgba(255,255,255,0.7) |
| Body | Inter | 400 | 18-20pt | rgba(255,255,255,0.7) |
| Caption | Inter | 400 | 12-14pt | rgba(255,255,255,0.5) |
| Quote | Inter | 400 Italic | 24pt | Blanco |
| Attribution | Caveat | 600 | 20pt | Teal |

---

## Diagrams with Excalidraw

Ver `references/excalidraw.md` para la guía completa.

### Quick Reference

```
Paleta Excalidraw EntendIA:
- Background: #191C1F
- Stroke principal: #14B8A6 (teal)
- Fill accent: #14B8A6 (20% opacity)
- Highlight: #E5B92B (amber)
- Text: #FFFFFF
```

Usar Excalidraw MCP para generar diagramas hand-drawn que mantienen el estilo de marca. Exportar como SVG para incrustar en slides.

---

## Transitions & Animation

- **Transiciones de slide**: solo **None** o **Fade** (0.3s)
- **Animaciones de contenido**: solo **Appear** (appear)
- **Charts**: pueden usar **Wipe** desde la izquierda
- **Regla general**: claridad > efectos visuales

---

## Rules (Do's & Don'ts)

### DO ✓

- Usar Inter para todo el texto (excepto firmas/atribuciones = Caveat)
- Fondo #191C1F para presentaciones profesionales
- Espaciado generoso (min 24px entre elementos)
- Máximo 6-8 bullets por slide
- Una idea principal por slide
- Logo solo en esquinas o centro
- Diseño limpio, mucho espacio negativo

### DON'T ✗

- Emojis en slides profesionales
- Más de 2 columnas de contenido
- Texto menor a 14pt
- Gradientes llamativos o multicolor
- Fotos de stock con personas sonriendo
- Animaciones fly-in, bounce, spin
- Mezclar dark mode y light mode en el mismo deck
- Logo flotando en medio del contenido

---

## File Structure

```
presentations/
├── SKILL.md                 # Este archivo
├── references/
│   ├── slide-types.md       # Detalles de cada tipo de slide
│   ├── typography.md        # Sistema tipográfico completo
│   ├── excalidraw.md        # Guía para diagramas Excalidraw
│   └── templates.md         # Instrucciones para usar templates
└── assets/
    ├── base-dark.html       # Template reveal.js dark mode
    ├── base-light.html      # Template reveal.js light mode
    └── excalidraw/          # Ejemplos de diagramas SVG
```

---

## Output Format

Al generar una presentación, crear un archivo HTML completo basado en los templates de `assets/`. El archivo debe:

1. Ser autocontenido (CSS inline, fonts de Google CDN)
2. Funcionar abriendo directamente en navegador
3. Usar reveal.js desde CDN
4. Incluir todas las slides solicitadas
5. Seguir la estructura de nombres: `presentacion-[tema]-[fecha].html`

---

## Related Skills

- `entendia-brand` — Identidad visual completa
- `entendia-discovery` — Proceso de discovery para proyectos
