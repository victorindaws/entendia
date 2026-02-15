---
name: entendia-brand-v2
description: Identidad visual EntendIA v2.1 - Estilo / con fondo negro, teal brillante (#14B8A6) y logo con "IA" cursiva. Tech-forward, minimalista, ambicioso. Usar para branding corporativo moderno.
---

# EntendIA Brand v2.1 — / Style

## Overview

Nueva versión de la identidad EntendIA inspirada en  y . Fondo negro profundo (#191C1F), tipografía Inter + Caveat para "IA" cursiva, estilo tech-forward y ambicioso.

**Keywords**: branding, identidad visual, EntendIA, , , minimalista, tech, startup, moderno

---

## Diferencias con v2.0

| Aspecto | v2.0 | v2.1 |
|---------|------|------|
| Teal | #0D5C4E (oscuro) | #14B8A6 (brillante, Tailwind 400) |
| Logo "IA" | Inter Bold (mismo que "Entend") | **Caveat cursiva** (firma personal) |
| Contraste | Bajo vs fondo negro | **Alto contraste** |
| Estilo | Corporativo tech | Firma personal + tech |

---

## Logo

### Concepto: Portal + Firma Personal

El isotipo es un portal simplificado. El wordmark combina:
- **"Entend"**: Inter Bold — profesional, tech, sólido
- **"IA"**: Caveat cursiva — firma personal, humano, memorable

Este contraste transmite: **IA con personalidad, no IA genérica**.

### Construcción del Logo

```
[Portal]  EntendIA
          ^^^^^^
          "Entend" Inter Bold
                ^^
                "IA" Caveat cursiva, teal
```

- **"Entend"**: White #FFFFFF (dark mode) o #191C1F (light mode)
- **"IA"**: Teal #14B8A6 (Caveat cursiva)
- **Font "Entend"**: Inter Bold (700)
- **Font "IA"**: Caveat SemiBold (600)
- **Letter spacing**: 0.5px (Inter), 1px (Caveat)

### Versiones del Logo

| Versión | Uso | Archivo |
|---------|-----|---------|
| Horizontal Dark | Headers sobre negro | `logo-horizontal-dark.svg` |
| Horizontal Light | Headers sobre blanco | `logo-horizontal-light.svg` |
| Stacked Dark | Formato cuadrado (fondo oscuro) | `logo-stacked-dark.svg` |
| Stacked Light | Formato cuadrado (fondo claro) | `logo-stacked-light.svg` |
| Isotipo | Avatar, favicon, iconos | `isotipo.svg` |

### Logo CSS

```css
/* Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Caveat:wght@500;600;700&family=Inter:wght@400;500;600;700&display=swap');

.logo-wordmark {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    font-weight: 700;
    font-size: 32px;
    letter-spacing: 0.5px;
}

.logo-ia {
    font-family: 'Caveat', cursive;
    font-weight: 600;
    font-size: 38px; /* ~1.2x tamaño del Inter */
    letter-spacing: 1px;
    color: #14B8A6;
}

/* Dark mode (sobre fondo negro) */
.logo-base-dark { color: #FFFFFF; }

/* Light mode (sobre fondo blanco) */
.logo-base-light { color: #191C1F; }
```

### Zona de Seguridad

Margen mínimo: **altura del isotipo × 0.5** en todos los lados.

### Tamaño Mínimo

- **Logo completo**: 100px ancho mínimo
- **Isotipo solo**: 16px (favicon), 24px (avatar), 32px (recomendado)

---

## Brand Colors

### Primary Palette

| Name | Hex | RGB | Use |
|------|-----|-----|-----|
|  | `#191C1F` | 25, 28, 31 | Fondo principal |
| Teal 400 | `#14B8A6` | 20, 184, 166 | Accent principal, "IA" del logo |
| Amber | `#E5B92B` | 229, 185, 43 | CTAs, centro del isotipo |

### Extended Palette

| Name | Hex | Use |
|------|-----|-----|
| Teal Dark | `#0F9488` | Gradiente, hover states |
| Teal Light | `#2DD4BF` | Alternativa si necesita más brillo |
| White | `#FFFFFF` | Texto principal dark mode |
| Muted | `rgba(255,255,255,0.7)` | Texto secundario |
| Muted Light | `rgba(255,255,255,0.5)` | Texto terciario |
| Border | `rgba(255,255,255,0.1)` | Bordes de cards |
| Surface | `#1E2225` | Cards, surfaces elevadas |

### Gradientes

```css
/* Teal gradient (para accents) */
.gradient-teal {
    background: linear-gradient(135deg, #14B8A6 0%, #0F9488 100%);
}

/* Subtle surface gradient */
.gradient-surface {
    background: linear-gradient(180deg, #1E2225 0%, #191C1F 100%);
}

/* Amber gradient (para CTAs destacados) */
.gradient-amber {
    background: linear-gradient(135deg, #E5B92B 0%, #D4A826 100%);
}
```

### Color Usage Rules

1. ** #191C1F** es el fondo base — SIEMPRE
2. **Teal #14B8A6** para accents, links, "IA" del logo, elementos destacados
3. **Amber #E5B92B** SOLO para CTAs principales y centro del isotipo
4. **White** para texto principal, **Muted** para secundario
5. **Nunca** usar colores saturados adicionales

---

## Typography

### Font Families

**Inter** — Sans-serif geométrica moderna (cuerpo, headlines)
**Caveat** — Script/handwriting (solo para "IA" del logo)

```css
@import url('https://fonts.googleapis.com/css2?family=Caveat:wght@500;600;700&family=Inter:wght@400;500;600;700&display=swap');

:root {
    --font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --font-cursive: 'Caveat', cursive;
}
```

### Type Scale

| Element | Size | Weight | Line Height | Use |
|---------|------|--------|-------------|-----|
| Display | 64px | 700 | 1.1 | Hero headlines |
| H1 | 48px | 700 | 1.2 | Page titles |
| H2 | 36px | 700 | 1.25 | Section heads |
| H3 | 24px | 600 | 1.3 | Card titles |
| H4 | 20px | 600 | 1.35 | Subtitles |
| Body | 16px | 400 | 1.6 | Paragraphs |
| Body Large | 18px | 400 | 1.6 | Lead text |
| Small | 14px | 400 | 1.5 | Captions |
| Micro | 12px | 500 | 1.4 | Labels, tags |

### Typography CSS

```css
h1 { font-size: 48px; font-weight: 700; line-height: 1.2; letter-spacing: -0.02em; }
h2 { font-size: 36px; font-weight: 700; line-height: 1.25; letter-spacing: -0.01em; }
h3 { font-size: 24px; font-weight: 600; line-height: 1.3; }
h4 { font-size: 20px; font-weight: 600; line-height: 1.35; }
p  { font-size: 16px; font-weight: 400; line-height: 1.6; color: rgba(255,255,255,0.7); }

/* Negative letter-spacing para headings grandes */
.display { font-size: 64px; font-weight: 700; line-height: 1.1; letter-spacing: -0.03em; }
```

---

## Visual Style

### Cards — Estilo 

```css
.card {
    background: #1E2225;
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 12px;
    padding: 24px;
    transition: all 0.2s ease;
}

.card:hover {
    border-color: rgba(255, 255, 255, 0.15);
    transform: translateY(-2px);
}

/* Card con accent teal */
.card-accent {
    background: linear-gradient(135deg, rgba(20, 184, 166, 0.15) 0%, rgba(20, 184, 166, 0.05) 100%);
    border: 1px solid rgba(20, 184, 166, 0.3);
}

/* Card destacada */
.card-featured {
    background: linear-gradient(135deg, #1E2225 0%, #191C1F 100%);
    border: 1px solid rgba(20, 184, 166, 0.4);
    box-shadow: 0 0 40px rgba(20, 184, 166, 0.15);
}
```

### Buttons

```css
/* Primary — Amber (CTAs principales) */
.btn-primary {
    background: #E5B92B;
    color: #191C1F;
    border: none;
    border-radius: 8px;
    padding: 12px 24px;
    font-weight: 600;
    font-size: 14px;
    cursor: pointer;
    transition: all 0.2s ease;
}

.btn-primary:hover {
    background: #D4A826;
    transform: translateY(-1px);
}

/* Secondary — Teal */
.btn-secondary {
    background: #14B8A6;
    color: #FFFFFF;
    border: none;
    border-radius: 8px;
    padding: 12px 24px;
    font-weight: 600;
    font-size: 14px;
}

.btn-secondary:hover {
    background: #0F9488;
}

/* Ghost */
.btn-ghost {
    background: transparent;
    color: #FFFFFF;
    border: 1px solid rgba(255, 255, 255, 0.2);
    border-radius: 8px;
    padding: 12px 24px;
    font-weight: 500;
}

.btn-ghost:hover {
    background: rgba(255, 255, 255, 0.05);
    border-color: rgba(255, 255, 255, 0.3);
}
```

### Tags/Badges

```css
.tag {
    display: inline-block;
    background: rgba(20, 184, 166, 0.2);
    color: #14B8A6;
    border: 1px solid rgba(20, 184, 166, 0.3);
    border-radius: 6px;
    padding: 4px 12px;
    font-size: 12px;
    font-weight: 500;
}

/* Versión light (sobre fondo oscuro) */
.tag-light {
    background: rgba(255, 255, 255, 0.1);
    color: rgba(255, 255, 255, 0.8);
    border: 1px solid rgba(255, 255, 255, 0.15);
}
```

---

## Spacing Scale

```css
:root {
    --space-1: 4px;
    --space-2: 8px;
    --space-3: 12px;
    --space-4: 16px;
    --space-5: 20px;
    --space-6: 24px;
    --space-8: 32px;
    --space-10: 40px;
    --space-12: 48px;
    --space-16: 64px;
    --space-20: 80px;
    --space-24: 96px;
}
```

---

## Border Radius

```css
:root {
    --radius-sm: 4px;   /* Tags, pequeños elementos */
    --radius-md: 8px;   /* Buttons, inputs */
    --radius-lg: 12px;  /* Cards */
    --radius-xl: 16px;  /* Modals, containers grandes */
}
```

---

## Shadows

Minimalistas, casi imperceptibles:

```css
:root {
    --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.1);
    --shadow-md: 0 4px 12px rgba(0, 0, 0, 0.15);
    --shadow-lg: 0 8px 24px rgba(0, 0, 0, 0.2);
    --shadow-glow-teal: 0 0 40px rgba(20, 184, 166, 0.15);
    --shadow-glow-amber: 0 0 30px rgba(229, 185, 43, 0.2);
}
```

---

## Tone of Voice

### Brand Personality —  Style

EntendIA v2.1 es **ambicioso, directo, sin rodeos**. No pedimos permiso, construimos el futuro.

| Somos | No somos |
|-------|----------|
| Ambiciosos | Arrogantes |
| Directos | Agresivos |
| Técnicos | Incomprensibles |
| Confiados | Prepotentes |
| Orientados a resultados | Vendedores |
| Modernos | Trendy sin sustancia |

### Taglines

**Principal:**
> "No esperamos al futuro de tu empresa. Lo construimos."

**Alternativas:**
- "IA que entiende tu negocio."
- "Del concepto a producción en semanas."
- "Tu empresa, potenciada por IA."

### Writing Guidelines

**En lugar de:**
> "Ofrecemos soluciones de inteligencia artificial personalizadas para empresas que buscan mejorar sus procesos."

**Escribe:**
> "Implementamos IA en tu empresa. En 5 semanas, no en meses. Con resultados medibles."

**En lugar de:**
> "Nuestro equipo de expertos te acompañará en cada paso del camino hacia la transformación digital."

**Escribe:**
> "Trabajamos con tus datos reales desde el día uno. Sin PowerPoints infinitos."

### Key Messages

1. **Velocidad**: "5 semanas. 2-3 Skills funcionando. Resultados medibles."

2. **Sin excusas**: "Tu competencia ya usa IA. ¿A qué esperas?"

3. **Garantía**: "Funciona o te devolvemos el dinero."

---

## CSS Variables (Complete)

```css
:root {
    /* Colors */
    --color-bg: #191C1F;
    --color-surface: #1E2225;
    --color-teal: #14B8A6;
    --color-teal-dark: #0F9488;
    --color-amber: #E5B92B;
    --color-amber-dark: #D4A826;
    --color-white: #FFFFFF;
    --color-muted: rgba(255, 255, 255, 0.7);
    --color-muted-light: rgba(255, 255, 255, 0.5);
    --color-border: rgba(255, 255, 255, 0.1);
    --color-border-hover: rgba(255, 255, 255, 0.15);
    
    /* Typography */
    --font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    --font-cursive: 'Caveat', cursive;
    --font-weight-regular: 400;
    --font-weight-medium: 500;
    --font-weight-semibold: 600;
    --font-weight-bold: 700;
    
    /* Spacing */
    --space-1: 4px;
    --space-2: 8px;
    --space-3: 12px;
    --space-4: 16px;
    --space-6: 24px;
    --space-8: 32px;
    --space-12: 48px;
    --space-16: 64px;
    
    /* Radius */
    --radius-sm: 4px;
    --radius-md: 8px;
    --radius-lg: 12px;
    --radius-xl: 16px;
    
    /* Shadows */
    --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.1);
    --shadow-md: 0 4px 12px rgba(0, 0, 0, 0.15);
    --shadow-lg: 0 8px 24px rgba(0, 0, 0, 0.2);
    --shadow-glow-teal: 0 0 40px rgba(20, 184, 166, 0.15);
}
```

---

## Do's and Don'ts

### Do ✓

- Usar fondo #191C1F siempre
- Inter para cuerpo, Caveat para "IA"
- Teal #14B8A6 para accents (alto contraste)
- Amber solo para CTAs principales
- Border radius 8-12px
- Bordes sutiles (1px, 10% opacity)
- Escribir directo, sin rodeos
- Espaciado generoso
- Diseño limpio, mucho espacio negativo

### Don't ✗

- Usar más de 3 colores
- Usar Caveat para algo que no sea "IA"
- Gradientes llamativos o coloridos
- Sombras pronunciadas
- Border radius >16px
- Glassmorphism pesado
- Lenguaje corporativo aburrido
- Fotos de stock con gente sonriendo
- Emojis en materiales profesionales
- Bordes gruesos de colores

---

## Assets Directory

```
assets/
├── isotipo.svg                 # Isotipo universal
├── isotipo-dark.svg            # Isotipo para fondos oscuros
├── isotipo-light.svg           # Isotipo para fondos claros
├── logo-horizontal-dark.svg    # Logo horizontal (fondo oscuro)
├── logo-horizontal-light.svg   # Logo horizontal (fondo claro)
├── logo-stacked-dark.svg       # Logo apilado (fondo oscuro)
└── logo-stacked-light.svg      # Logo apilado (fondo claro)
```
