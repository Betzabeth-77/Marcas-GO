# Ichigo — Design System Context
> Fuente de verdad para todos los proyectos digitales de la marca. Aplica a: web apps, propuestas HTML, PDFs, emails, tablas, presentaciones y cualquier pieza digital de Ichigo Agencia Creativa.
> Este archivo **extiende** (no reemplaza) el sistema base de Grupo Ortiz definido en `context_design.md`.

---

## 1. IDENTIDAD DE MARCA

**Marca:** Ichigo Agencia Creativa  
**Abreviatura oficial:** ICH  
**Significado:** "Ichigo" (いちご) = fresa en japonés — el isotipo es una fresa estilizada con una gráfica de barras ascendente y una flecha hacia arriba, representando crecimiento y resultados  
**Anatomía del logo:** Isotipo (fresa + gráfica) + wordmark "ichigo" (ITC Avant Garde Book/Bold) + descriptor "AGENCIA CREATIVA" (ITC Avant Garde Bold Condensed, uppercase, tracking amplio)  
**Color primario:** Carbón Ichigo `#2B2A28`  
**Color secundario:** Rojo Fresa `#EF3238`  
**Color neutro claro:** Crema Ichigo `#DDD9D0`  
**Color de acento:** Verde Hoja `#236D2D`  
**Color de energía:** Amarillo Ichigo `#FFD72E`  
**Sector:** Agencia creativa / Marketing digital / Branding  
**Tono de marca:** Audaz, directo, creativo — habla con confianza a marcas que quieren crecer

---

## 2. PALETA DE COLORES OFICIAL

### Colores corporativos (fuente: imagen de variantes del isotipo)
| Nombre | Hex | RGB | CMYK | Uso |
|--------|-----|-----|------|-----|
| Rojo Fresa | `#EF3238` | 239, 50, 56 | 0% 89% 74% 0% | Cuerpo de la fresa — acento principal de la marca, botón primario, borde de tabla, línea de header, palabra clave en título |
| Carbón Ichigo | `#2B2A28` | 43, 42, 40 | 70% 61% 60% 73% | Color de fondo base, texto principal, nav, footer, fondo de presentaciones |
| Crema Ichigo | `#DDD9D0` | 221, 217, 208 | 16% 13% 19% 0% | Neutro claro oficial — wordmark sobre fondo oscuro, fondo de reportes PDF, texto secundario sobre carbón |
| Verde Hoja | `#236D2D` | 35, 109, 45 | 85% 32% 100% 22% | Hojas del isotipo, badges positivos, highlights de crecimiento |
| Amarillo Ichigo | `#FFD72E` | 255, 215, 46 | 1% 14% 86% 0% | Acento de energía, eyebrows/labels, banda de acento bajo header |

### Neutros
| Nombre | Hex | Uso |
|--------|-----|-----|
| Negro absoluto | `#1A1918` | Fondos de máximo contraste, piezas oscuras premium |
| Carbón medio | `#3D3C3A` | Variante de fondo oscuro, hover sobre carbón |
| Gris medio | `#6E6C69` | Texto secundario sobre fondo claro |
| Crema Ichigo | `#DDD9D0` | Fondo claro cálido (equivalente al lino GO) — texto corrido sobre blanco |
| Blanco | `#FFFFFF` | Fondos claros, texto sobre carbón/rojo/verde |

### Paleta ordenada (oscuro → claro)
```
#1A1918  →  #2B2A28  →  #3D3C3A  →  #236D2D  →  #EF3238  →  #FFD72E  →  #DDD9D0  →  #FFFFFF
```

### Tokens CSS recomendados
```css
:root {
  /* Primarios */
  --ich-carbon:        #2B2A28;
  --ich-carbon-dark:   #1A1918;        /* fondos premium */
  --ich-carbon-mid:    #3D3C3A;        /* hover sobre carbón */
  --ich-carbon-tint:   rgba(43,42,40,0.08);

  --ich-red:           #EF3238;
  --ich-red-hover:     #CC1E23;        /* hover */
  --ich-red-deep:      #A81F24;        /* pressed */
  --ich-red-tint:      rgba(239,50,56,0.10);

  --ich-green:         #236D2D;
  --ich-green-hover:   #1A5221;
  --ich-green-tint:    rgba(35,109,45,0.10);

  --ich-yellow:        #FFD72E;
  --ich-yellow-hover:  #E8C100;
  --ich-yellow-tint:   rgba(255,215,46,0.15);

  /* Neutros */
  --ich-cream:   #DDD9D0;              /* neutro claro oficial */
  --ich-gray:    #6E6C69;
  --ich-white:   #FFFFFF;

  /* Semánticos */
  --ich-bg:        var(--ich-carbon);      /* fondo base = oscuro */
  --ich-bg-light:  var(--ich-cream);       /* fondo claro alternativo */
  --ich-text:      var(--ich-white);       /* texto sobre fondo oscuro */
  --ich-text-dark: var(--ich-carbon);      /* texto sobre fondo claro */
  --ich-text-2:    rgba(255,255,255,0.55); /* texto secundario sobre oscuro */
  --ich-accent:    var(--ich-red);
  --ich-accent-2:  var(--ich-yellow);
  --ich-accent-3:  var(--ich-green);
  --ich-border:    rgba(255,255,255,0.10);
  --ich-border-light: rgba(43,42,40,0.12);
}
```

### Modo claro (piezas de propuesta / reporte)
```css
body[data-theme="light"] {
  --ich-bg:      var(--ich-cream);
  --ich-bg-card: var(--ich-white);
  --ich-text:    var(--ich-carbon);
  --ich-text-2:  var(--ich-gray);
  --ich-border:  rgba(43,42,40,0.10);
}
```

---

## 3. TIPOGRAFÍA

### Fuentes oficiales Ichigo (fuente: Manual de Identidad)

| Fuente | Archivo | Rol | Uso |
|--------|---------|-----|-----|
| **ITC Avant Garde Gothic Bold** | `ITC_Avant_Garde_Gothic_Bold.otf` | **DISPLAY / encabezados** | Títulos principales, H1–H3, wordmark "ichigo" principal, CTAs en bold |
| **ITC Avant Garde Gothic CE Book** | `ITC_Avant_Garde_Gothic_CE_Book.otf` | **CUERPO / subtítulos** | Cuerpo de texto, párrafos, descripciones, subtítulos de sección |
| **ITC Avant Garde Gothic Bold Condensed** | `ITC_Avant_Garde_Gothic_Bold_Condensed.otf` | **DESCRIPTOR / eyebrow** | "AGENCIA CREATIVA" en el logo, labels uppercase, badges condensados |

### Fallbacks seguros
```css
--ich-font-display:    'ITC Avant Garde Gothic Bold', 'Futura', 'Century Gothic', 'Trebuchet MS', sans-serif;
--ich-font-body:       'ITC Avant Garde Gothic CE Book', 'Futura', 'Century Gothic', 'DM Sans', sans-serif;
--ich-font-condensed:  'ITC Avant Garde Gothic Bold Condensed', 'Futura Condensed', 'Arial Narrow', sans-serif;
--ich-font-mono:       'JetBrains Mono', 'Fira Code', Consolas, monospace;
```

### Escala tipográfica
| Nivel | Fuente | Tamaño | Peso | Letra-spacing | Uso |
|-------|--------|--------|------|---------------|-----|
| Display XL | Avant Garde Bold | 72–96px | Bold | −0.02em | Portadas, hero de propuesta, banners de campaña |
| H1 | Avant Garde Bold | 48–64px | Bold | −0.015em | Título principal de sección |
| H2 | Avant Garde Bold | 32–40px | Bold | −0.01em | Subtítulos de sección |
| H3 | Avant Garde Bold | 22–28px | Bold | 0 | Encabezados de tarjeta, nombres de servicio |
| H4 | Avant Garde Bold | 16–18px | Bold | 0.02em | Encabezados de tabla, labels fuertes |
| Body | Avant Garde Book | 14–16px | Book | 0 | Texto corrido, descripciones de servicio |
| Body Small | Avant Garde Book | 12–13px | Book | 0 | Pie de página, notas, metadata |
| Eyebrow / descriptor | Avant Garde Bold Condensed | 10–12px | Bold | 0.18em | Labels UPPERCASE, "AGENCIA CREATIVA", supratítulos |
| Mono | JetBrains Mono | 12–13px | Regular | 0.04em | Fechas, presupuestos, IDs de proyecto |

### Reglas tipográficas
- **Descriptor/eyebrow:** siempre en `ITC Avant Garde Gothic Bold Condensed`, `text-transform: uppercase`, `letter-spacing: 0.16em` — igual que "AGENCIA CREATIVA" en el logo
- **Nunca** usar Italic — la familia Avant Garde no tiene uso cursivo en la identidad Ichigo
- **Fondo base es oscuro** — la mayoría del texto va en blanco `#FFFFFF` sobre carbón `#2B2A28`
- En piezas light (propuestas, reportes PDF), el texto va en carbón `#2B2A28` sobre crema `#DDD9D0`

---

## 4. LOGO — VARIANTES Y USO

### Anatomía del sistema de logo

```
ISOTIPO    = Fresa estilizada con gráfica de barras + flecha ascendente (crecimiento)
IMAGOTIPO  = Isotipo + "ichigo" (wordmark) + "AGENCIA CREATIVA" (descriptor)
LOGOTIPO   = "ichigo" + "AGENCIA CREATIVA" (sin isotipo)
```

### Archivos disponibles
| Archivo | Descripción | Colores | Sobre qué fondo |
|---------|-------------|---------|-----------------|
| `Logo_Ichigo_1.png` | Imagotipo completo — versión crema/oscuro | "ichigo" en crema `#DDD9D0`, descriptor en crema, isotipo a color | Fondo oscuro `#2B2A28` o negro |
| `Logo_Ichigo_2.png` | Imagotipo completo — versión oscura sobre claro | "ichigo" en carbón `#2B2A28`, isotipo a color | Fondo blanco o crema |
| `Logo_Ichigo_blanco.png` | Imagotipo negativo completo | Todo blanco | Cualquier fondo oscuro (carbón, rojo, verde) |
| `Logo_Ichigo_negro.png` | Imagotipo monocromo oscuro | Todo carbón `#2B2A28` | Fondo blanco o crema |
| `Icono_Ichigo.png` | Isotipo solo — a color | Rojo fresa + verde hoja + negro | Fondo oscuro preferido |
| `Icono_Ichigo_blanco.png` | Isotipo negativo | Blanco | Fondos oscuros |
| `Icono_Ichigo_negro.png` | Isotipo monocromo | Carbón `#2B2A28` | Fondo blanco o crema |

### Colores del isotipo
- **Cuerpo de la fresa:** Rojo `#EF3238` · RGB: 239, 50, 56 · CMYK: 0% 89% 74% 0%
- **Hojas:** Verde `#236D2D`
- **Gráfica de barras + flecha:** Carbón `#2B2A28` / blanco según versión
- **Contorno:** Carbón `#2B2A28`
- **Versión crema:** Neutro `#DDD9D0` (tercer isotipo de la imagen de referencia)

### Reglas de uso del logo (según Manual de Identidad)
- ✅ Usar el logo completo (isotipo + wordmark + descriptor)
- ✅ Usar solo el isotipo en aplicaciones donde el espacio sea reducido
- ✅ Versión vertical (isotipo arriba + wordmark abajo)
- ❌ **Nunca** aplicar opacidad al logo
- ❌ **Nunca** rotar el logo
- ❌ **Nunca** deformar o cambiar proporciones
- ❌ **Nunca** aplicar sombras
- ❌ **Nunca** omitir el isotipo del imagotipo completo
- ❌ **Nunca** cambiar los colores fuera del sistema oficial

### Espacio de respeto
- Mínimo: `= altura de la fresa × 0.30` en todos los lados
- El descriptor "AGENCIA CREATIVA" es parte integral del logo — no omitir en aplicaciones formales

---

## 5. COMPONENTES UI

> **Nota de contexto:** Ichigo es una agencia creativa — sus piezas digitales son principalmente propuestas de cliente, reportes de campaña, landing pages y presentaciones. El fondo base es **oscuro** (`#2B2A28`). Los componentes se definen en modo oscuro por defecto.

### Botón primario (rojo)
```css
.btn-primary {
  background: var(--ich-red);
  color: #fff;
  font-family: var(--ich-font-display);
  font-weight: 700;
  font-size: 13px;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  border: none;
  border-radius: 4px;
  padding: 12px 28px;
  cursor: pointer;
  transition: background 200ms ease;
}
.btn-primary:hover  { background: var(--ich-red-hover); }
.btn-primary:active { background: var(--ich-red-deep); }
```

### Botón secundario (amarillo)
```css
.btn-secondary {
  background: var(--ich-yellow);
  color: var(--ich-carbon);
  font-family: var(--ich-font-display);
  font-weight: 700;
  font-size: 13px;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  border: none;
  border-radius: 4px;
  padding: 12px 28px;
  cursor: pointer;
  transition: background 200ms ease;
}
.btn-secondary:hover  { background: var(--ich-yellow-hover); }
```

### Botón ghost / outline (sobre fondo oscuro)
```css
.btn-ghost {
  background: transparent;
  color: var(--ich-white);
  border: 1.5px solid rgba(255,255,255,0.35);
  border-radius: 4px;
  padding: 10px 24px;
  font-family: var(--ich-font-display);
  font-weight: 700;
  font-size: 13px;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  transition: all 200ms ease;
  cursor: pointer;
}
.btn-ghost:hover { border-color: var(--ich-red); color: var(--ich-red); }
```

### Card / tarjeta de servicio (modo oscuro)
```css
.card {
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 8px;
  padding: 24px;
  transition: border-color 200ms;
}
.card:hover { border-color: var(--ich-red); }
.card-eyebrow {
  font-family: var(--ich-font-condensed);
  font-size: 10px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.18em;
  color: var(--ich-yellow);
  margin-bottom: 10px;
}
.card-title {
  font-family: var(--ich-font-display);
  font-size: 20px;
  font-weight: 700;
  color: var(--ich-white);
  margin-bottom: 10px;
  letter-spacing: -0.01em;
}
.card p {
  font-family: var(--ich-font-body);
  font-size: 14px;
  color: rgba(255,255,255,0.55);
  line-height: 1.65;
}
/* Acento lateral rojo */
.card.accent-left {
  border-left: 3px solid var(--ich-red);
}
```

### Input / campo de formulario (modo oscuro)
```css
.input {
  width: 100%;
  padding: 11px 16px;
  border: 1.5px solid rgba(255,255,255,0.15);
  border-radius: 4px;
  font-family: var(--ich-font-body);
  font-size: 14px;
  color: var(--ich-white);
  background: rgba(255,255,255,0.05);
  transition: border-color 200ms;
}
.input:focus {
  outline: none;
  border-color: var(--ich-red);
  box-shadow: 0 0 0 3px rgba(239,50,56,0.15);
}
.input::placeholder { color: rgba(255,255,255,0.30); }
```

### Badge / etiqueta
```css
/* Servicio activo / entregado */
.badge-active {
  display: inline-block;
  background: rgba(35,109,45,0.18);
  color: #5AC46A;
  font-family: var(--ich-font-condensed);
  font-size: 10px; font-weight: 700;
  padding: 3px 10px; border-radius: 3px;
  text-transform: uppercase; letter-spacing: 0.12em;
}
/* En proceso */
.badge-progress {
  background: rgba(255,215,46,0.15);
  color: var(--ich-yellow);
  font-family: var(--ich-font-condensed);
  font-size: 10px; font-weight: 700;
  padding: 3px 10px; border-radius: 3px;
  text-transform: uppercase; letter-spacing: 0.12em;
}
/* Pendiente / urgente */
.badge-urgent {
  background: rgba(239,50,56,0.18);
  color: #FF4D6A;
  font-size: 10px; font-weight: 700;
  padding: 3px 10px; border-radius: 3px;
  text-transform: uppercase; letter-spacing: 0.12em;
}
```

---

## 6. TABLAS

```css
.ich-table {
  width: 100%;
  border-collapse: collapse;
  font-family: var(--ich-font-body);
  font-size: 13px;
  color: rgba(255,255,255,0.85);
  background: transparent;
}
.ich-table thead tr {
  border-top: 2px solid var(--ich-red);
  background: rgba(255,255,255,0.04);
}
.ich-table th {
  font-family: var(--ich-font-condensed);
  font-weight: 700;
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 0.16em;
  color: var(--ich-yellow);
  padding: 12px 16px;
  text-align: left;
}
.ich-table td {
  padding: 12px 16px;
  border-bottom: 1px solid rgba(255,255,255,0.06);
}
.ich-table tbody tr:hover { background: rgba(239,50,56,0.05); }

/* Columna de monto / presupuesto */
.ich-table .col-amount {
  font-family: var(--ich-font-display);
  font-weight: 700;
  color: var(--ich-white);
  letter-spacing: -0.01em;
}
/* Columna de código de proyecto / folio */
.ich-table .col-id {
  font-family: var(--ich-font-mono);
  font-size: 11px;
  color: rgba(255,255,255,0.40);
  letter-spacing: 0.06em;
}
/* Fila destacada */
.ich-table tr.featured {
  background: rgba(239,50,56,0.08);
  border-left: 2px solid var(--ich-red);
}
/* Tabla en modo claro (propuestas) */
body[data-theme="light"] .ich-table { color: var(--ich-carbon); }
body[data-theme="light"] .ich-table thead tr { background: #F0EBE3; }
body[data-theme="light"] .ich-table th { color: var(--ich-red); }
body[data-theme="light"] .ich-table td { border-bottom-color: rgba(43,42,40,0.08); }
```

---

## 7. PROPUESTA / REPORTE HTML

Plantilla base para propuestas de cliente, reportes de campaña y documentos de entrega:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;700&display=swap');

    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { background: #1A1A1A; font-family: 'ITC Avant Garde Gothic CE Book', 'DM Sans', sans-serif; color: #fff; }
    .wrapper { max-width: 920px; margin: 0 auto; background: #2B2A28; }

    /* Header oscuro */
    .report-header {
      background: #1A1918;
      padding: 28px 40px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      border-bottom: 2px solid #EF3238;
    }
    .report-logo-area img { height: 44px; object-fit: contain; }
    .report-meta {
      text-align: right;
      color: rgba(255,255,255,0.35);
      font-family: 'ITC Avant Garde Gothic Bold Condensed', 'DM Sans', sans-serif;
      font-size: 10px;
      letter-spacing: 0.16em;
      text-transform: uppercase;
    }

    /* Banda amarilla */
    .report-accent-bar { height: 3px; background: #FFD72E; }

    /* Sección */
    .report-section {
      padding: 36px 40px;
      border-bottom: 1px solid rgba(255,255,255,0.06);
    }
    .report-eyebrow {
      font-family: 'ITC Avant Garde Gothic Bold Condensed', 'DM Sans', sans-serif;
      font-size: 10px; font-weight: 700;
      text-transform: uppercase; letter-spacing: 0.18em;
      color: #FFD72E; margin-bottom: 12px;
    }
    .report-title {
      font-family: 'ITC Avant Garde Gothic Bold', 'DM Sans', sans-serif;
      font-size: 32px; font-weight: 700;
      letter-spacing: -0.02em;
      color: #FFFFFF;
      margin-bottom: 20px;
    }

    /* KPI */
    .kpi-value {
      font-family: 'ITC Avant Garde Gothic Bold', 'DM Sans', sans-serif;
      font-size: 48px; font-weight: 700;
      color: #FFFFFF; letter-spacing: -0.03em;
    }
    .kpi-label {
      font-size: 10px; color: #FFD72E;
      text-transform: uppercase; letter-spacing: 0.14em;
      margin-top: 4px;
    }

    /* Highlight rojo */
    .highlight { color: #EF3238; }

    /* Footer */
    .report-footer {
      background: #1A1918;
      padding: 18px 40px;
      display: flex;
      justify-content: space-between;
      font-family: 'ITC Avant Garde Gothic Bold Condensed', sans-serif;
      font-size: 10px;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: rgba(255,255,255,0.25);
      border-top: 1px solid rgba(255,255,255,0.06);
    }
  </style>
</head>
<body>
  <div class="wrapper">
    <div class="report-header">
      <div class="report-logo-area">
        <img src="cid:logo_blanco" alt="Ichigo Agencia Creativa">
      </div>
      <div class="report-meta">
        Propuesta de Campaña<br>Mayo 2026
      </div>
    </div>
    <div class="report-accent-bar"></div>

    <div class="report-section">
      <div class="report-eyebrow">Resumen ejecutivo</div>
      <div class="report-title">Estrategia de <span class="highlight">Crecimiento</span></div>
      <!-- contenido -->
    </div>

    <div class="report-footer">
      <span>Ichigo · Agencia Creativa</span>
      <span>Confidencial · Uso interno</span>
    </div>
  </div>
</body>
</html>
```

---

## 8. PDF / PRINT

```css
@media print {
  body { background: #fff; color: #2B2A28; }
  * { box-shadow: none !important; }

  /* En PDF las propuestas pueden ir en modo claro */
  .ich-accent   { color: #EF3238; }
  .ich-yellow   { color: #D4A800; } /* amarillo más oscuro para impresión */

  .pdf-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 3px solid #2B2A28;
    padding-bottom: 16px;
    margin-bottom: 8px;
  }
  .pdf-accent-bar { height: 2px; background: #EF3238; margin-bottom: 24px; }

  .pdf-footer {
    position: fixed;
    bottom: 0; left: 0; right: 0;
    border-top: 1px solid rgba(43,42,40,0.15);
    padding: 8px 40px;
    font-size: 10px; color: #6E6C69;
    display: flex; justify-content: space-between;
    font-family: 'ITC Avant Garde Gothic Bold Condensed', sans-serif;
    letter-spacing: 0.10em; text-transform: uppercase;
  }

  .page-break { page-break-before: always; }
  .no-break   { page-break-inside: avoid; }
}
```

### Márgenes de página recomendados
- Carta/A4: `margin: 20mm 25mm`
- Header: logo Ichigo negro (izquierda) + nombre del documento (derecha)
- Línea divisoria: carbón `#2B2A28` 3pt + rojo `#EF3238` 2pt debajo
- Footer: `Ichigo · Agencia Creativa · Página X de Y`

---

## 9. MODO OSCURO (base por defecto)

Ichigo opera en **modo oscuro como base** — es el estado natural de la marca. El modo claro es la excepción para propuestas y PDF formales.

```css
/* Modo oscuro = estado base, no requiere clase adicional */
body {
  background: var(--ich-carbon);   /* #2B2A28 */
  color: var(--ich-white);
}

/* Modo claro = activado explícitamente */
body[data-theme="light"] {
  background: var(--ich-cream);    /* #DDD9D0 */
  color: var(--ich-carbon);        /* #2B2A28 */
}
```

**Regla:** El rojo `#EF3238`, el amarillo `#FFD72E` y el verde `#236D2D` son **invariables** — mismo valor en oscuro y claro. Solo el fondo y el texto neutro cambian.

---

## 10. REFERENCIAS VISUALES DE MARCA

Las referencias visuales del Manual de Identidad definen el mood:
- Fondos oscuros predominantes (`#2B2A28`, `#1A1918`)
- Tipografía **grande, bold** como elemento compositivo
- Rojo como acento de máximo impacto
- Fotografías high-contrast con renders 3D o personas + tecnología
- Lettering display ocupando gran parte del espacio
- Uso de grids y líneas geométricas como elementos gráficos

**Patrón visual típico de pieza Ichigo:**
```
[Fondo negro/carbón] + [Título bold enorme en blanco] + [Acento rojo en palabra clave] + [Isotipo o logo en esquina] + [Banda amarilla o línea roja de separación]
```

---

## 11. REGLAS DE ORO (resumen ejecutivo para IA/agentes)

1. **Carbón `#2B2A28`** — fondo base de toda la identidad. La marca vive en oscuro.
2. **Rojo Fresa `#EF3238`** — acento de máximo impacto. Va en: borde de tabla, línea de header, botón primario, palabra clave en título, hover de card.
3. **Crema `#DDD9D0`** — neutro claro oficial. Va en: wordmark sobre fondo oscuro, fondos de reportes PDF, texto en piezas oscuras.
4. **Amarillo `#FFD72E`** — energía y atención. Va en: eyebrows/labels, banda de acento bajo header, KPI labels, badges de estado.
5. **Verde `#236D2D`** — acento orgánico/positivo. Va en: badges de completado/crecimiento, detalles positivos, no como color principal de UI.
6. **Avant Garde Bold** — toda tipografía display y encabezados.
7. **Avant Garde Book** — texto corrido, descripciones, cuerpo de tablas.
8. **Avant Garde Bold Condensed** — eyebrows, descriptores UPPERCASE, "AGENCIA CREATIVA".
9. **Nunca Italic** — la familia Avant Garde no se usa en cursiva dentro de Ichigo.
10. **Fondo base es oscuro** — no usar blanco puro como fondo principal de ninguna pieza digital.
11. **Banda amarilla** `#FFD72E` bajo el header de reporte — 3px.
12. **Logo sobre fondo claro** → versión carbón (`Logo_Ichigo_negro.png`). Sobre fondo oscuro → versión crema `#DDD9D0` o blanca.
13. **Prohibiciones de logo:** sin opacidad, sin rotación, sin deformación, sin sombra, sin omitir isotipo, sin cambio de color.

---

## 12. RELACIÓN CON EL SISTEMA GO

| Elemento | Sistema GO (`context_design.md`) | Sub-marca Ichigo (este archivo) |
|----------|----------------------------------|---------------------------------|
| Fondo base | `#ECEBE0` crema (claro) | `#2B2A28` carbón (oscuro) |
| Acento primario | `#FB670B` naranja | `#EF3238` rojo fresa |
| Neutro claro | `#ECEBE0` | `#DDD9D0` crema Ichigo |
| Acento secundario | — | `#FFD72E` amarillo |
| Acento terciario | — | `#236D2D` verde |
| Tipografía display | Blauer Nue | ITC Avant Garde Gothic Bold |
| Tipografía cuerpo | Conthic | ITC Avant Garde Gothic CE Book |
| Tipografía condensada | — | ITC Avant Garde Gothic Bold Condensed |
| Banda de acento en reporte | Naranja `#FB670B` | Amarillo `#FFD72E` |
| Botón primario | Naranja | Rojo `#EF3238` |
| Modo predeterminado | Claro | Oscuro |

### Regla de carga para agentes e IA
```
Proyecto Ichigo solo     → context_design.md  +  ichigo.md
Proyecto multi-marca     → context_design.md  +  brand_system.md  +  ichigo.md
Conflicto GO/Ichigo      → brand_system.md §4 (Tabla de conflictos)
Piezas en modo claro     → ichigo.md §9, activar body[data-theme="light"]
```

---

## 13. RUTAS DE ASSETS

```
ichigo/
├── 01_LOGO/
│   ├── Logo_Ichigo_1.png        ← Imagotipo — wordmark crema sobre oscuro
│   ├── Logo_Ichigo_2.png        ← Imagotipo — wordmark carbón sobre claro
│   ├── Logo_Ichigo_blanco.png   ← Imagotipo negativo blanco
│   ├── Logo_Ichigo_negro.png    ← Imagotipo monocromo carbón
│   ├── Icono_Ichigo.png         ← Isotipo a color (rojo + verde)
│   ├── Icono_Ichigo_blanco.png  ← Isotipo blanco
│   └── Icono_Ichigo_negro.png   ← Isotipo monocromo carbón
│
├── 02_TIPOGRAFIA/
│   ├── ITC_Avant_Garde_Gothic_Bold.otf            ← Display / encabezados
│   ├── ITC_Avant_Garde_Gothic_CE_Book.otf         ← Cuerpo / subtítulos
│   └── ITC_Avant_Garde_Gothic_Bold_Condensed.otf  ← Eyebrows / descriptor
│
└── 03_MANUAL/
    └── Ichigo_-_Manual_de_identidad.pdf  ← Fuente de verdad oficial
```

---

*Última actualización: 2026-06-02 · Colores corregidos desde imagen oficial de variantes del isotipo · Sistema Ichigo integrado al ecosistema Grupo Ortiz*
