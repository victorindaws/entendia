# EntendIA Discovery Skill

Auditoria AI-First para empresas. Mapea oportunidades de automatizacion e incremento de ingresos en una organizacion.

## Uso

Este skill guia el proceso de discovery en 4 fases para identificar y priorizar oportunidades de transformacion AI.

### Cuando usar este skill

- Sesiones de discovery con equipos directivos
- Auditorias de procesos empresariales
- Identificacion de Quick Wins para automatizacion
- Preparacion de propuestas de transformacion AI

## Proceso (4 Fases)

1. **Fase 0: Investigacion previa** - Usar Brave Search para contexto
2. **Fase 1: Mapa de organizacion** - Estructura, departamentos, cuello de botella
3. **Fase 2: Deep Dive** - Tareas concretas con potencial de automatizacion
4. **Fase 3: Priorizacion** - Calcular valor y ordenar por impacto
5. **Fase 4: Presentacion** - Generar CSV + presentacion ejecutiva

## Assets disponibles

| Archivo | Descripcion |
|---------|-------------|
| `assets/template-presentacion.html` | Template HTML para resultados |
| `assets/plantilla-discovery.csv` | Estructura CSV de oportunidades |
| `brand/EntendIA-BrandBook-v1.md` | Guia de marca EntendIA |
| `brand/color-preview.html` | Preview visual de colores |
| `references/departamentos.md` | Preguntas por departamento |

## Placeholders del template

### Portada
| Variable | Descripcion | Ejemplo |
|----------|-------------|---------|
| `{{EMPRESA}}` | Nombre empresa | "Distribuciones Peris" |
| `{{FECHA}}` | Fecha sesion | "14 Febrero 2026" |

### Metricas
| Variable | Descripcion | Ejemplo |
|----------|-------------|---------|
| `{{NUM_OPORTUNIDADES}}` | Total oportunidades | "8" |
| `{{VALOR_EFICIENCIA}}` | Ahorro anual | "152.000 EUR" |
| `{{VALOR_CRECIMIENTO}}` | Ingresos potenciales | "80.000 EUR" |
| `{{VALOR_TOTAL}}` | Suma total | "232.000 EUR" |

### Quick Wins
| Variable | Descripcion |
|----------|-------------|
| `{{QW1_TITULO}}` | Titulo del Quick Win 1 |
| `{{QW1_DESCRIPCION}}` | Descripcion del Quick Win 1 |
| `{{QW1_VALOR}}` | Valor estimado del Quick Win 1 |
| `{{QW2_*}}`, `{{QW3_*}}` | Igual para QW 2 y 3 |

### Tabla de oportunidades
| Variable | Descripcion |
|----------|-------------|
| `{{TABLA_OPORTUNIDADES}}` | Filas HTML de la tabla |
| `{{NUM_SKILLS}}` | Skills a entregar |

### Formato fila tabla
```html
<tr>
    <td>Comercial</td>
    <td>Gestion de pedidos</td>
    <td>25h</td>
    <td class="highlight">72.000 EUR</td>
    <td class="priority-quick">Quick Win</td>
</tr>
```

## Estructura CSV

```csv
Departamento,Tarea,Responsable,Personas,Horas/Semana,Automatizable,Valor Eficiencia EUR,Valor Crecimiento EUR,Prioridad,Notas
Comercial,Gestion pedidos,Luis,3,25,Alto,72000,80000,Quick Win,WhatsApp+email
```

## Paleta de colores (Indaws)

| Nombre | Hex | Uso |
|--------|-----|-----|
| Warm Yellow | `#E5B92B` | Highlights, metricas |
| Blue Lilac | `#6B68FA` | Acentos |
| Blue Space | `#1C265D` | Fondos |
| Light Sky | `#8AC2DB` | Elementos secundarios |

## Requisitos

- Google Fonts: Montserrat
- Bootstrap 5 (opcional)
- Navegadores modernos con backdrop-filter
