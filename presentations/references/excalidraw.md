# Excalidraw Integration Guide

Crear diagramas hand-drawn para slides usando Excalidraw MCP.

---

## Overview

Excalidraw produce diagramas con estilo sketch/hand-drawn que complementan el look tech-forward de EntendIA. Usar para:

- Flujos de proceso
- Arquitecturas de sistema
- Diagramas de concepto
- Timelines
- Mapas mentales

---

## Paleta EntendIA para Excalidraw

### Colores Principales

| Uso | Color | Hex |
|-----|-------|-----|
| Background (dark) | Almost black | #191C1F |
| Background (light) | Off-white | #FAFAFA |
| Stroke principal | Teal | #14B8A6 |
| Stroke secundario | White | #FFFFFF |
| Fill accent | Teal 20% | rgba(20,184,166,0.2) |
| Highlight | Amber | #E5B92B |
| Text | White (dark) | #FFFFFF |
| Text | Dark (light) | #191C1F |

### Colores Adicionales para Datos

Para diagramas con múltiples elementos:

1. #14B8A6 — Teal (primario)
2. #0F9488 — Teal Dark
3. #E5B92B — Amber
4. #2DD4BF — Teal Light
5. #FFFFFF — White (para contraste)

---

## Excalidraw MCP Commands

### Usando mcporter

```bash
# Crear nuevo diagrama
mcporter excalidraw create --name "arquitectura-sistema"

# Añadir elementos
mcporter excalidraw add-shape --type rectangle --x 100 --y 100 --width 200 --height 100 --fill "#14B8A6" --stroke "#14B8A6"

# Añadir texto
mcporter excalidraw add-text --text "API Gateway" --x 150 --y 140 --color "#FFFFFF"

# Añadir flecha
mcporter excalidraw add-arrow --start "100,150" --end "300,150" --stroke "#14B8A6"

# Exportar SVG
mcporter excalidraw export --format svg --output "diagrama.svg"
```

### Parámetros de Estilo

```json
{
  "strokeStyle": "solid",
  "strokeWidth": 2,
  "roughness": 1,
  "opacity": 100,
  "backgroundColor": "transparent",
  "fillStyle": "hachure"
}
```

---

## Configuración por Defecto

### Para Fondos Oscuros (#191C1F)

```json
{
  "appState": {
    "viewBackgroundColor": "#191C1F",
    "currentItemStrokeColor": "#14B8A6",
    "currentItemBackgroundColor": "transparent",
    "currentItemFillStyle": "hachure",
    "currentItemStrokeWidth": 2,
    "currentItemRoughness": 1
  }
}
```

### Para Fondos Claros (#FAFAFA)

```json
{
  "appState": {
    "viewBackgroundColor": "#FAFAFA",
    "currentItemStrokeColor": "#14B8A6",
    "currentItemBackgroundColor": "transparent",
    "currentItemFillStyle": "hachure",
    "currentItemStrokeWidth": 2,
    "currentItemRoughness": 1
  }
}
```

---

## Tipos de Elementos

### Shapes

| Forma | Uso | Fill |
|-------|-----|------|
| Rectangle | Bloques, contenedores | hachure teal o transparent |
| Ellipse | Puntos de inicio/fin | solid teal |
| Diamond | Decisiones | hachure amber |
| Line | Conexiones simples | — |
| Arrow | Flujo direccional | — |

### Text

| Tipo | Tamaño | Peso |
|------|--------|------|
| Label principal | 20px | Bold |
| Label secundario | 16px | Regular |
| Nota/caption | 14px | Regular |

### Connectors

- **Arrow**: para flujo con dirección
- **Line**: para asociaciones sin dirección
- **Stroke width**: 2px para todo
- **Color**: #14B8A6 (primario) o #FFFFFF (secundario)

---

## Estilos de Fill

### Hachure (Recomendado)

Líneas diagonales hand-drawn. Mantiene el estilo sketch.

```json
{
  "fillStyle": "hachure",
  "backgroundColor": "#14B8A6",
  "opacity": 30
}
```

### Solid

Para elementos que necesitan destacar más.

```json
{
  "fillStyle": "solid",
  "backgroundColor": "#14B8A6",
  "opacity": 100
}
```

### Cross-hatch

Para énfasis máximo.

```json
{
  "fillStyle": "cross-hatch",
  "backgroundColor": "#E5B92B",
  "opacity": 50
}
```

---

## Diagrama de Ejemplo: Arquitectura

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│   ┌──────────┐          ┌──────────┐                   │
│   │  Client  │ ──────▶  │   API    │                   │
│   │   App    │          │ Gateway  │                   │
│   └──────────┘          └────┬─────┘                   │
│                              │                          │
│              ┌───────────────┼───────────────┐          │
│              ▼               ▼               ▼          │
│        ┌──────────┐   ┌──────────┐   ┌──────────┐      │
│        │  Auth    │   │  Core    │   │   AI     │      │
│        │ Service  │   │  Logic   │   │ Engine   │      │
│        └──────────┘   └──────────┘   └──────────┘      │
│                              │                          │
│                              ▼                          │
│                       ┌──────────┐                      │
│                       │ Database │                      │
│                       └──────────┘                      │
│                                                         │
└─────────────────────────────────────────────────────────┘

Colores:
- Client App: stroke #FFFFFF, fill none
- API Gateway: stroke #14B8A6, fill hachure #14B8A6 20%
- Services: stroke #14B8A6, fill hachure #14B8A6 20%
- AI Engine: stroke #E5B92B, fill hachure #E5B92B 20%
- Database: stroke #14B8A6, fill solid #0F9488
- Arrows: #14B8A6, 2px
```

---

## Exportación

### SVG (Recomendado)

```bash
mcporter excalidraw export --format svg --transparent --output "diagrama.svg"
```

- Usar fondo transparente
- El slide proporciona el background
- Escalable sin pérdida de calidad

### PNG

```bash
mcporter excalidraw export --format png --scale 2 --output "diagrama.png"
```

- Solo si SVG no es opción
- Exportar a 2x para retina
- Incluir fondo si es necesario

---

## Integración en Slides

### HTML

```html
<section class="diagram-slide" data-background-color="#191C1F">
    <h3>ARQUITECTURA DEL SISTEMA</h3>
    <div class="diagram">
        <img src="assets/excalidraw/arquitectura.svg" 
             alt="Diagrama de arquitectura"
             style="max-width: 80%; max-height: 70vh;">
    </div>
</section>
```

### CSS

```css
.diagram-slide .diagram {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 60vh;
}

.diagram-slide .diagram img {
    max-width: 80%;
    max-height: 100%;
    object-fit: contain;
}
```

---

## Best Practices

1. **Mantener simplicidad** — máximo 10-12 elementos por diagrama
2. **Usar roughness 1** — suficiente hand-drawn sin ser caótico
3. **Stroke width 2px** — visible desde proyección
4. **Labels legibles** — mínimo 16px para texto
5. **Contraste alto** — teal sobre negro funciona bien
6. **Exportar transparent** — el slide controla el fondo
7. **Alineación** — usar grid de Excalidraw para orden
8. **Grouping** — agrupar elementos relacionados

---

## Troubleshooting

### SVG no muestra en slide

- Verificar path relativo correcto
- Asegurar que el SVG tiene viewBox definido
- Probar con PNG como fallback

### Colores no coinciden

- Verificar hex codes exactos
- Excalidraw puede ajustar opacity — revisar export
- Comparar con paleta de referencia

### Texto ilegible

- Aumentar tamaño de fuente
- Usar color #FFFFFF sobre teal
- Evitar texto sobre hachure denso
