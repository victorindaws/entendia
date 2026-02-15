# Templates Reference

Guía para usar los templates reveal.js de EntendIA.

---

## Archivos de Template

| Archivo | Uso |
|---------|-----|
| `assets/base-dark.html` | Presentaciones sobre fondo negro (#191C1F) |
| `assets/base-light.html` | Presentaciones sobre fondo claro (#FAFAFA) |

---

## Estructura del Template

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="utf-8">
    <title>Título de la Presentación</title>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=..." rel="stylesheet">
    
    <!-- Reveal.js CDN -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4/dist/reveal.css">
    
    <!-- Custom EntendIA Styles -->
    <style>
        /* Variables de marca */
        /* Estilos base */
        /* Tipos de slides */
    </style>
</head>
<body>
    <div class="reveal">
        <div class="slides">
            <!-- Slides aquí -->
        </div>
    </div>
    
    <!-- Reveal.js Scripts -->
    <script src="https://cdn.jsdelivr.net/npm/reveal.js@4/dist/reveal.js"></script>
    <script>
        Reveal.initialize({
            // Configuración
        });
    </script>
</body>
</html>
```

---

## Configuración de Reveal.js

### Opciones Recomendadas

```javascript
Reveal.initialize({
    // Dimensiones
    width: 1280,
    height: 720,
    
    // Márgenes
    margin: 0.05,
    
    // Escalado
    minScale: 0.2,
    maxScale: 2.0,
    
    // Navegación
    controls: true,
    controlsTutorial: false,
    progress: true,
    hash: true,
    
    // Transiciones (solo fade o none)
    transition: 'fade',
    transitionSpeed: 'default',
    backgroundTransition: 'fade',
    
    // Comportamiento
    center: true,
    touch: true,
    loop: false,
    shuffle: false,
    
    // Autoplay
    autoSlide: 0,
    autoSlideStoppable: true,
    
    // Plugins
    plugins: []
});
```

---

## Cómo Usar los Templates

### 1. Copiar el Template

```bash
cp assets/base-dark.html mi-presentacion.html
```

### 2. Editar Metadatos

```html
<title>Mi Título de Presentación</title>
<meta name="description" content="Descripción breve">
<meta name="author" content="EntendIA">
```

### 3. Agregar Slides

Cada `<section>` es un slide:

```html
<div class="slides">
    <!-- Title Slide -->
    <section class="title-slide">
        <div class="logo">
            <span class="logo-entend">Entend</span><span class="logo-ia">IA</span>
        </div>
        <h1>TÍTULO PRINCIPAL</h1>
        <p class="subtitle">Subtítulo descriptivo</p>
    </section>
    
    <!-- Content Slide -->
    <section class="content-slide">
        <h3>TÍTULO DEL CONTENIDO</h3>
        <ul>
            <li>Punto uno</li>
            <li>Punto dos</li>
            <li>Punto tres</li>
        </ul>
    </section>
    
    <!-- Más slides... -->
</div>
```

### 4. Personalizar si Necesario

Editar variables CSS en el `<style>`:

```css
:root {
    --color-bg: #191C1F;
    --color-teal: #14B8A6;
    --color-amber: #E5B92B;
    /* etc. */
}
```

---

## Clases de Slide

| Clase | Tipo de Slide |
|-------|---------------|
| `.title-slide` | Slide de título/portada |
| `.section-divider` | Divisor de sección |
| `.content-slide` | Contenido con bullets |
| `.image-text-slide` | Imagen + texto split |
| `.data-slide` | Gráficos y datos |
| `.quote-slide` | Citas/testimonios |
| `.diagram-slide` | Diagramas Excalidraw |
| `.closing-slide` | Slide de cierre |

---

## Elementos Comunes

### Logo en Esquina

```html
<div class="logo-corner">
    <span class="logo-entend">Entend</span><span class="logo-ia">IA</span>
</div>
```

### Línea Accent

```html
<div class="accent-line"></div>
```

### Fragmentos (Animación Appear)

```html
<ul>
    <li class="fragment">Aparece primero</li>
    <li class="fragment">Aparece segundo</li>
    <li class="fragment">Aparece tercero</li>
</ul>
```

### Dos Columnas

```html
<div class="columns">
    <div class="column">
        <h4>Columna 1</h4>
        <ul>
            <li>Item A</li>
            <li>Item B</li>
        </ul>
    </div>
    <div class="column">
        <h4>Columna 2</h4>
        <ul>
            <li>Item X</li>
            <li>Item Y</li>
        </ul>
    </div>
</div>
```

### Background Override por Slide

```html
<section data-background-color="#14B8A6">
    <!-- Section divider con fondo teal -->
</section>
```

---

## Añadir Imágenes

### Imagen Inline

```html
<img src="imagen.jpg" alt="Descripción" style="max-width: 80%;">
```

### Imagen de Fondo

```html
<section data-background-image="fondo.jpg" data-background-opacity="0.3">
    <h1>Título sobre imagen</h1>
</section>
```

### Diagrama SVG

```html
<div class="diagram">
    <img src="assets/excalidraw/diagrama.svg" alt="Diagrama">
</div>
```

---

## Añadir Charts

### Con Chart.js

```html
<canvas id="myChart" width="800" height="400"></canvas>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script>
new Chart(document.getElementById('myChart'), {
    type: 'bar',
    data: {
        labels: ['Q1', 'Q2', 'Q3', 'Q4'],
        datasets: [{
            label: 'Revenue',
            data: [12, 19, 3, 5],
            backgroundColor: ['#14B8A6', '#0F9488', '#E5B92B', '#2DD4BF']
        }]
    },
    options: {
        plugins: {
            legend: { labels: { color: '#FFFFFF' } }
        },
        scales: {
            x: { ticks: { color: 'rgba(255,255,255,0.7)' } },
            y: { ticks: { color: 'rgba(255,255,255,0.7)' } }
        }
    }
});
</script>
```

---

## Speaker Notes

```html
<section>
    <h3>Slide con Notas</h3>
    <p>Contenido visible</p>
    
    <aside class="notes">
        Notas solo visibles para el presentador (presionar 's' para ver).
        - Recordar mencionar X
        - Ejemplo: caso de cliente Y
    </aside>
</section>
```

---

## Export a PDF

1. Abrir en navegador con `?print-pdf` al final:
   ```
   file:///path/to/presentacion.html?print-pdf
   ```

2. Imprimir a PDF (Ctrl+P / Cmd+P)

3. Configurar:
   - Layout: Landscape
   - Márgenes: None
   - Background graphics: ✓

---

## Checklist Pre-Presentación

- [ ] Título y metadatos actualizados
- [ ] Todas las imágenes cargan correctamente
- [ ] Diagrams SVG visibles
- [ ] Fonts cargando (Google Fonts)
- [ ] Transiciones solo fade/none
- [ ] Contraste verificado
- [ ] Speaker notes añadidas (si aplica)
- [ ] Probado en modo presentación (F11)
- [ ] PDF exportado como backup

---

## Troubleshooting

### Fonts no cargan

Verificar conexión a internet o añadir fonts localmente:
```html
<style>
@font-face {
    font-family: 'Inter';
    src: url('fonts/Inter.woff2') format('woff2');
}
</style>
```

### Slides no escalan bien

Verificar configuración de `width`, `height`, y `margin` en Reveal.initialize().

### Imágenes no aparecen

- Verificar paths relativos
- Usar paths absolutos para testing
- Verificar que el archivo existe

### Transiciones lentas

Cambiar `transitionSpeed: 'fast'` en la configuración.
