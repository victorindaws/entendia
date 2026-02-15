# EntendIA Brand v2.1

**No esperamos al futuro de tu empresa. Lo construimos.**

---

## Brand Story

EntendIA nació de una frustración: ver empresas con potencial quedarse atrás porque la IA parecía algo "para otros". Demasiado complejo. Demasiado caro. Demasiado arriesgado.

Nosotros lo vemos diferente.

La IA no es el futuro. Es el presente. Y cada día que pasa sin implementarla es un día que tu competencia te adelanta.

EntendIA existe para cerrar esa brecha. No con consultorías interminables ni PowerPoints de 200 páginas. Con implementación real. Skills funcionando. Resultados medibles.

**5 semanas. 2-3 Skills. O te devolvemos el dinero.**

---

## The Name

**Entend** + **IA**

- **Entender**: Porque la IA debe entender tu negocio, no al revés
- **IA**: Inteligencia Artificial, ahora en **Caveat cursiva** como firma personal

El nombre es un juego de palabras que funciona en español: "Entiende IA" → "EntendIA"

---

## Visual Identity v2.1

Esta versión evoluciona v2.0 con:

1. **Teal más brillante** (#14B8A6 vs #0D5C4E) — mejor contraste contra fondo negro
2. **"IA" en Caveat cursiva** — firma personal, memorable, humano

### Key Visual Elements

1. **Fondo  (#191C1F)**: Negro profundo, no negro puro. Sofisticado.
2. **Teal 400 (#14B8A6)**: Brillante, alto contraste, moderno.
3. **Amber CTAs (#E5B92B)**: El punto focal, reservado para acciones clave.
4. **Inter + Caveat**: Sans-serif profesional + cursiva personal.
5. **Geometría Limpia**: Bordes sutiles, espaciado generoso, sin adornos.

---

## Logo — Portal + Firma

El concepto del "Portal" se mantiene para el isotipo, pero el wordmark ahora tiene personalidad:

```
[Portal]  EntendIA
                ^^
                Caveat cursiva, teal
```

**v2.0**: Todo en Inter Bold — profesional pero genérico
**v2.1**: Inter Bold + Caveat cursiva — profesional con firma personal

El contraste tipográfico transmite: **IA con personalidad, no IA de fábrica**.

Inspirado en marcas como every.to que usan tipografía script para humanizar tech.

---

## Colors

### Primary

| Name | Hex | Uso |
|------|-----|-----|
|  | `#191C1F` | Fondo principal |
| Teal 400 | `#14B8A6` | Accents, "IA" del logo, links |
| Amber | `#E5B92B` | CTAs, centro del isotipo |

### Cambio vs v2.0

| | v2.0 | v2.1 |
|---|------|------|
| Teal | `#0D5C4E` (oscuro) | `#14B8A6` (brillante) |
| Contraste vs fondo | ~3.5:1 | **~8:1** ✓ |

---

## Typography

### Fonts

```html
<link href="https://fonts.googleapis.com/css2?family=Caveat:wght@500;600;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
```

### Usage

- **Inter Bold (700)**: Headlines, "Entend" del logo, cuerpo importante
- **Inter Regular (400)**: Párrafos, texto secundario
- **Caveat SemiBold (600)**: SOLO para "IA" del logo

---

## Files

```
entendia-brand-v2/
├── SKILL.md                        # Guía completa de marca
├── README.md                       # Este archivo
├── assets/
│   ├── isotipo.svg                 # Isotipo universal
│   ├── isotipo-dark.svg            # Para fondos oscuros
│   ├── isotipo-light.svg           # Para fondos claros
│   ├── logo-horizontal-dark.svg    # Logo completo, fondo oscuro
│   ├── logo-horizontal-light.svg   # Logo completo, fondo claro
│   ├── logo-stacked-dark.svg       # Logo apilado, fondo oscuro
│   └── logo-stacked-light.svg      # Logo apilado, fondo claro
└── presentation/
    ├── brand-guidelines.html       # Presentación Reveal.js (dark)
    └── brand-guidelines-light.html # Presentación Reveal.js (light)
```

---

## Quick Start

### Colors
```css
--bg: #191C1F;
--teal: #14B8A6;
--amber: #E5B92B;
--text: #FFFFFF;
--muted: rgba(255,255,255,0.7);
```

### Fonts
```html
<link href="https://fonts.googleapis.com/css2?family=Caveat:wght@500;600;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
```

### Logo Wordmark
```css
.logo-base { font-family: 'Inter', sans-serif; font-weight: 700; }
.logo-ia { font-family: 'Caveat', cursive; font-weight: 600; color: #14B8A6; }
```

### Card
```css
.card {
    background: #1E2225;
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 12px;
    padding: 24px;
}
```

---

## Version History

- **v1.0** (2024): Identidad original — Fondo teal, Poppins+Lora, cálido y cercano
- **v2.0** (2025-01): / style — Fondo negro, Inter, tech-forward
- **v2.1** (2025-02): Teal brillante + IA cursiva — Mejor contraste, firma personal

---

*EntendIA © 2026*
