# Hotel Punta Galería — Design System Context
> Fuente de verdad para todos los proyectos digitales de la marca. Aplica a: web apps, menús HTML, PDFs, emails, tablas, presentaciones y cualquier pieza digital de Hotel Punta Galería.
> Este archivo **extiende** (no reemplaza) el sistema base de Grupo Ortiz definido en `context_design.md`.

---

## 1. IDENTIDAD DE MARCA

**Marca:** Hotel Punta Galería  
**Abreviatura oficial:** HPG  
**Anatomía del logo:** "hotel" en script caligráfico (La Bohemienne) + "puntaGalería" en sans-serif bold (Brisbane) — siempre en minúsculas, sin espacio entre "punta" y "Galería" salvo en la variante con submarca  
**Color primario:** Azul Marino HPG `#323F48`  
**Color secundario:** Verde Galería `#838C2F` (en piezas del hotel) / `#236D00` (en piezas de naturaleza/jardín)  
**Colores de ambiente:** Arena `#C7B7A4` y Lino `#E5E0D8`  
**Sector:** Hospitalidad / Hotel boutique  
**Tono de marca:** Sereno, cercano, natural — habla con calidez a viajeros que valoran la tranquilidad y el entorno verde

---

## 2. PALETA DE COLORES OFICIAL

### Primarios
| Nombre | Hex | Pantone (aprox.) | CMYK | Uso |
|--------|-----|-----------------|------|-----|
| Azul Marino HPG | `#323F48` | 7546 C | 31% 13% 0% 72% | Color de marca principal, fondos oscuros, texto sobre claro, headers, nav, footer |
| Verde Galería | `#838C2F` | 5777 C | 6% 0% 66% 45% | Acento natural, títulos alternativos, variante color del logo "Galería" |
| Verde Bosque | `#626C1F` | 582 C | 9% 0% 71% 58% | Verde profundo, hover del verde galería, detalles de naturaleza |
| Verde Frondoso | `#236D00` | 364 C | 68% 0% 100% 57% | Alto impacto natural, piezas de jardín/exterior, submarca Cafetería |

### Neutros cálidos
| Nombre | Hex | Pantone (aprox.) | CMYK | Uso |
|--------|-----|-----------------|------|-----|
| Arena HPG | `#C7B7A4` | 7527 C | 0% 8% 18% 22% | Fondo cálido secundario, separadores, cards sobre blanco |
| Lino HPG | `#E5E0D8` | 7527 U | 0% 2% 6% 10% | Fondo principal cálido, secciones de contenido, fondo de reportes |
| Blanco | `#FFFFFF` | — | — | Fondo limpio, texto sobre oscuro |
| Negro suave | `#1C1C1C` | — | — | Texto principal (evitar negro puro) |

### Paleta ordenada (oscuro → claro)
```
#323F48  →  #626C1F  →  #838C2F  →  #236D00  →  #C7B7A4  →  #E5E0D8  →  #FFFFFF
```

### Tokens CSS recomendados
```css
:root {
  /* Primarios */
  --hpg-navy:          #323F48;
  --hpg-navy-deep:     #242F38;        /* hover / pressed */
  --hpg-navy-tint:     rgba(50,63,72,0.10);

  --hpg-green:         #838C2F;
  --hpg-green-hover:   #626C1F;
  --hpg-green-deep:    #4F571A;
  --hpg-green-tint:    rgba(131,140,47,0.10);

  --hpg-forest:        #236D00;
  --hpg-forest-hover:  #1A5200;
  --hpg-forest-tint:   rgba(35,109,0,0.10);

  /* Neutros cálidos */
  --hpg-sand:    #C7B7A4;
  --hpg-linen:   #E5E0D8;
  --hpg-white:   #FFFFFF;
  --hpg-black:   #1C1C1C;

  /* Semánticos */
  --hpg-bg:        var(--hpg-linen);
  --hpg-bg-warm:   var(--hpg-sand);
  --hpg-bg-dark:   var(--hpg-navy);
  --hpg-text:      var(--hpg-black);
  --hpg-text-2:    var(--hpg-navy);
  --hpg-accent:    var(--hpg-green);
  --hpg-accent-2:  var(--hpg-navy);
  --hpg-border:    rgba(199,183,164,0.50);
}
```

---

## 3. TIPOGRAFÍA

### Fuentes oficiales HPG

| Fuente | Archivo | Rol | Características |
|--------|---------|-----|-----------------|
| **La Bohemienne Deluxe** | `la-bohemienne-deluxe.otf` | **CALIGRÁFICA / logo "hotel"** | Script manuscrito elegante — solo para el wordmark "hotel" en el logo y contadas aplicaciones de display |
| **Brisbane** | `Brisbane-Bold_Trial-BF660e1a392b91c.otf` | **DISPLAY / encabezados** | Sans-serif geométrica semibold, kerning −20 — toda la tipografía visible de marca, encabezados, títulos |
| **Salford Sans VF Family** | (variable font, Google/sistema) | **CUERPO / texto corrido** | Variable sans, legible, moderna — descripciones, párrafos, tablas, body de reportes |

### Fallbacks seguros
```css
--hpg-font-script:  'La Bohemienne Deluxe', 'Pinyon Script', cursive;
--hpg-font-display: 'Brisbane', 'Outfit', 'DM Sans', 'Inter', sans-serif;
--hpg-font-body:    'Salford Sans VF', 'Inter', 'DM Sans', system-ui, sans-serif;
--hpg-font-mono:    'JetBrains Mono', 'Fira Code', Consolas, monospace;
```

### Regla de kerning para Brisbane
Brisbane en encabezados siempre con `letter-spacing: -0.02em` (equivalente a −20 de kerning en diseño).

### Escala tipográfica
| Nivel | Fuente | Tamaño | Peso | Letra-spacing | Uso |
|-------|--------|--------|------|---------------|-----|
| Display XL | Brisbane | 64–96px | 600 | −0.03em | Portadas, hero, banners principales |
| H1 | Brisbane | 48–56px | 600 | −0.02em | Títulos principales de sección |
| H2 | Brisbane | 32–40px | 600 | −0.02em | Subtítulos, nombres de sección |
| H3 | Brisbane | 22–26px | 600 | −0.015em | Encabezados de tarjeta, nombres de habitación |
| H4 | Brisbane | 16–18px | 600 | −0.01em | Encabezados de tabla, labels de formulario |
| Body | Salford Sans VF | 14–16px | 400 | 0 | Texto corrido, descripciones |
| Body Small | Salford Sans VF | 12–13px | 400 | 0 | Pie de página, notas, metadata |
| Eyebrow / label | Brisbane | 10–11px | 600 | 0.14em | Supratítulo en UPPERCASE antes de H1/H2 |
| Caption script | La Bohemienne | 14–16px | 400 | 0 | Solo en piezas especiales (tarjetas, menú impreso, amenidades) |
| Mono | JetBrains Mono | 12–13px | 400 | 0.04em | Teléfonos, fechas, códigos de reserva |

### Reglas tipográficas
- **Eyebrow:** `font-family: var(--hpg-font-display); font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.14em; color: var(--hpg-green)`
- **Script (La Bohemienne):** reservada al logo + aplicaciones editoriales de lujo. NUNCA en UI funcional (formularios, botones, tablas).
- **Brisbane en web:** incluir como @font-face con el archivo .otf provisto
- Nunca mezclar Brisbane + La Bohemienne en el mismo elemento — son niveles distintos de jerarquía

---

## 4. LOGO — VARIANTES Y USO

### Anatomía del sistema de logo

```
WORDMARK PRINCIPAL  =  "hotel" (La Bohemienne script) + "puntaGalería" (Brisbane bold)
VARIANTE SUBMARCA   =  Logo principal + línea separadora + "CAFETERÍA · RESTAURANT · BAR"
NEGATIVO            =  Todo blanco sobre cualquier fondo oscuro
```

### Archivos disponibles
| Archivo | Descripción | Texto principal | Acento | Sobre qué fondo |
|---------|-------------|-----------------|--------|-----------------|
| `Hotel_PuntaGalería_Azul.png` | Logo principal — versión azul marina | `#323F48` | — (monocromo) | Fondo blanco, lino `#E5E0D8`, arena `#C7B7A4` |
| `Hotel_PuntaGalería_Caféteria-Restaurant-Bar.png` | Logo con submarca F&B | `#323F48` + `#838C2F` en "Galería" | Verde en wordmark | Fondo blanco o lino |
| `Hotel_PuntaGalería_negativo.png` | Logo negativo completo | Blanco | — | Fondos oscuros: `#323F48`, `#323F48`, negro, verde bosque |

### Lectura del logo en uso real (banner publicitario)
En aplicaciones publicitarias (ej. banner exterior `www.hotelpuntagaleria.com.mx`) el logo aparece sobre fondo `#323F48` con wordmark reducido —  siempre en versión negativo blanca en ese caso.

### Color del acento "Galería" en el wordmark
- Sobre fondo blanco/lino → "Galería" en **verde** `#838C2F`, "punta" en azul marino `#323F48`
- Sobre fondo oscuro (navy/negro) → todo el wordmark en **blanco** `#FFFFFF`
- Versión mono → todo en azul marino `#323F48`

### Espacio de respeto
- Mínimo: `= altura de la "p" de "punta" × 0.5` en todos los lados
- Nunca distorsionar proporciones del logo
- Nunca aplicar sombra, glow, stroke extra o efectos al logo
- La parte script "hotel" nunca aparece sola sin el wordmark "puntaGalería"

---

## 5. COMPONENTES UI

### Botón primario (azul marino)
```css
.btn-primary {
  background: var(--hpg-navy);
  color: #fff;
  font-family: var(--hpg-font-display);
  font-weight: 600;
  font-size: 13px;
  letter-spacing: 0.04em;
  border: none;
  border-radius: 6px;
  padding: 12px 28px;
  cursor: pointer;
  transition: background 200ms ease;
}
.btn-primary:hover  { background: #242F38; }
.btn-primary:active { background: #1A2229; }
```

### Botón secundario (verde)
```css
.btn-secondary {
  background: var(--hpg-green);
  color: #fff;
  font-family: var(--hpg-font-display);
  font-weight: 600;
  font-size: 13px;
  letter-spacing: 0.04em;
  border: none;
  border-radius: 6px;
  padding: 12px 28px;
  cursor: pointer;
  transition: background 200ms ease;
}
.btn-secondary:hover  { background: var(--hpg-green-hover); }
.btn-secondary:active { background: var(--hpg-green-deep); }
```

### Botón ghost / outline (sobre fondos claros)
```css
.btn-ghost {
  background: transparent;
  color: var(--hpg-navy);
  border: 1.5px solid var(--hpg-navy);
  border-radius: 6px;
  padding: 10px 24px;
  font-family: var(--hpg-font-display);
  font-weight: 600;
  font-size: 13px;
  letter-spacing: 0.04em;
  transition: all 200ms ease;
  cursor: pointer;
}
.btn-ghost:hover { border-color: var(--hpg-green); color: var(--hpg-green); }
```

### Card / tarjeta de habitación o servicio
```css
.card {
  background: var(--hpg-white);
  border: 1px solid rgba(199,183,164,0.40);
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 2px 12px rgba(50,63,72,0.07);
}
.card-body { padding: 20px 24px; }
.card-eyebrow {
  font-family: var(--hpg-font-display);
  font-size: 10px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.14em;
  color: var(--hpg-green);
  margin-bottom: 8px;
}
.card-title {
  font-family: var(--hpg-font-display);
  font-size: 20px;
  font-weight: 600;
  letter-spacing: -0.02em;
  color: var(--hpg-navy);
  margin-bottom: 10px;
}
.card-body p {
  font-family: var(--hpg-font-body);
  font-size: 14px;
  color: #4A5A62;
  line-height: 1.6;
}
```

### Input / campo de formulario (reservas, contacto)
```css
.input {
  width: 100%;
  padding: 11px 16px;
  border: 1.5px solid rgba(199,183,164,0.60);
  border-radius: 6px;
  font-family: var(--hpg-font-body);
  font-size: 14px;
  color: var(--hpg-black);
  background: var(--hpg-white);
  transition: border-color 200ms;
}
.input:focus {
  outline: none;
  border-color: var(--hpg-navy);
  box-shadow: 0 0 0 3px rgba(50,63,72,0.10);
}
.input::placeholder { color: #A09585; }
```

### Badge / etiqueta
```css
/* Disponibilidad */
.badge-available {
  display: inline-block;
  background: rgba(131,140,47,0.12);
  color: var(--hpg-green-hover);
  font-family: var(--hpg-font-display);
  font-size: 11px; font-weight: 600;
  padding: 3px 10px; border-radius: 20px;
  text-transform: uppercase; letter-spacing: 0.08em;
}
/* Destaque / promoción */
.badge-promo {
  background: var(--hpg-navy);
  color: #fff;
  font-family: var(--hpg-font-display);
  font-size: 11px; font-weight: 600;
  padding: 3px 10px; border-radius: 20px;
  text-transform: uppercase; letter-spacing: 0.08em;
}
/* Agotado / no disponible */
.badge-full {
  background: rgba(199,183,164,0.30);
  color: #7A6D62;
  font-size: 11px; font-weight: 600;
  padding: 3px 10px; border-radius: 20px;
  text-transform: uppercase;
}
```

---

## 6. TABLAS

```css
.hpg-table {
  width: 100%;
  border-collapse: collapse;
  font-family: var(--hpg-font-body);
  font-size: 13px;
  color: var(--hpg-black);
}
.hpg-table thead tr {
  border-top: 3px solid var(--hpg-navy);
  background: var(--hpg-linen);
}
.hpg-table th {
  font-family: var(--hpg-font-display);
  font-weight: 600;
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  color: var(--hpg-navy);
  padding: 11px 16px;
  text-align: left;
}
.hpg-table td {
  padding: 11px 16px;
  border-bottom: 1px solid rgba(199,183,164,0.40);
}
.hpg-table tbody tr:hover { background: rgba(229,224,216,0.50); }

/* Columna de tarifa */
.hpg-table .col-rate {
  font-family: var(--hpg-font-display);
  font-weight: 600;
  color: var(--hpg-navy);
  letter-spacing: -0.01em;
}
/* Columna de código / folio */
.hpg-table .col-id {
  font-family: var(--hpg-font-mono);
  font-size: 12px;
  color: var(--hpg-green-hover);
  letter-spacing: 0.04em;
}
/* Fila destacada */
.hpg-table tr.featured {
  background: rgba(131,140,47,0.08);
  border-left: 3px solid var(--hpg-green);
}
```

---

## 7. REPORTE HTML / MENÚ DIGITAL

Plantilla base para reportes internos, listas de precios y documentos de servicio:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;600&display=swap');

    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { background: #E5E0D8; font-family: 'Salford Sans VF', 'DM Sans', sans-serif; }
    .wrapper { max-width: 900px; margin: 0 auto; background: #fff; }

    /* Header del reporte */
    .report-header {
      background: #323F48;
      padding: 28px 40px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .report-logo-area img {
      height: 48px;
      object-fit: contain;
      filter: brightness(0) invert(1); /* logo en blanco sobre navy */
    }
    .report-meta {
      text-align: right;
      color: rgba(255,255,255,0.55);
      font-size: 11px;
      font-family: 'Brisbane', 'DM Sans', sans-serif;
      letter-spacing: 0.10em;
      text-transform: uppercase;
    }

    /* Banda de acento verde */
    .report-accent-bar { height: 3px; background: #838C2F; }

    /* Sección de contenido */
    .report-section {
      padding: 32px 40px;
      border-bottom: 1px solid rgba(199,183,164,0.35);
    }
    .report-eyebrow {
      font-family: 'Brisbane', 'DM Sans', sans-serif;
      font-size: 10px; font-weight: 600;
      text-transform: uppercase; letter-spacing: 0.16em;
      color: #838C2F; margin-bottom: 10px;
    }
    .report-title {
      font-family: 'Brisbane', 'DM Sans', sans-serif;
      font-size: 28px; font-weight: 600;
      letter-spacing: -0.02em;
      color: #323F48;
      margin-bottom: 20px;
    }

    /* KPI */
    .kpi-value {
      font-family: 'Brisbane', 'DM Sans', sans-serif;
      font-size: 44px; font-weight: 600;
      color: #323F48; letter-spacing: -0.03em;
    }
    .kpi-label {
      font-size: 12px; color: #838C2F;
      text-transform: uppercase; letter-spacing: 0.10em;
      margin-top: 4px;
    }

    /* Footer */
    .report-footer {
      background: #323F48;
      padding: 18px 40px;
      display: flex;
      justify-content: space-between;
      font-size: 10px; color: rgba(255,255,255,0.35);
      font-family: 'Brisbane', 'DM Sans', sans-serif;
      letter-spacing: 0.08em; text-transform: uppercase;
    }
  </style>
</head>
<body>
  <div class="wrapper">
    <div class="report-header">
      <div class="report-logo-area">
        <img src="cid:logo" alt="Hotel Punta Galería">
      </div>
      <div class="report-meta">
        Reporte Interno<br>Mayo 2026
      </div>
    </div>
    <div class="report-accent-bar"></div>

    <div class="report-section">
      <div class="report-eyebrow">Resumen del período</div>
      <div class="report-title">Ocupación Hotelera</div>
      <!-- contenido -->
    </div>

    <div class="report-footer">
      <span>Hotel Punta Galería · Grupo Ortiz</span>
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
  body { background: #fff; color: #1C1C1C; }
  * { box-shadow: none !important; transition: none !important; }

  .hpg-navy-text  { color: #323F48; }
  .hpg-green-text { color: #838C2F; }

  /* Encabezado de página */
  .pdf-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 2.5px solid #323F48;
    padding-bottom: 14px;
    margin-bottom: 24px;
  }
  /* Línea verde de acento bajo header */
  .pdf-accent { height: 2px; background: #838C2F; margin-bottom: 24px; }

  /* Footer de página */
  .pdf-footer {
    position: fixed;
    bottom: 0; left: 0; right: 0;
    border-top: 1px solid rgba(199,183,164,0.50);
    padding: 8px 40px;
    font-size: 10px; color: #838C2F;
    display: flex; justify-content: space-between;
    font-family: 'Brisbane', sans-serif;
    letter-spacing: 0.08em; text-transform: uppercase;
  }

  .page-break { page-break-before: always; }
  .no-break   { page-break-inside: avoid; }
}
```

### Márgenes de página recomendados
- Carta/A4: `margin: 22mm 28mm`
- Header fijo: logo HPG izquierda (negativo sobre banda navy) + nombre del documento derecha
- Footer fijo: `Hotel Punta Galería · Grupo Ortiz · Página X de Y`
- Color de línea divisoria encabezado: Navy `#323F48` 2.5pt + verde `#838C2F` 1pt debajo

---

## 9. MODO OSCURO (web apps)

```css
body[data-mode="dark"] {
  --hpg-bg:      #1A2229;
  --hpg-bg-warm: #232F37;
  --hpg-text:    #E5E0D8;
  --hpg-text-2:  #A0B0B8;
  --hpg-border:  rgba(229,224,216,0.10);
  /* Navy se aclara para contraste */
  --hpg-navy:    #4A6070;
  /* Verde no cambia */
  --hpg-green:   #838C2F;
  /* Neutros cálidos en modo oscuro */
  --hpg-sand:    #5A4F45;
  --hpg-linen:   #2C2520;
}
```

**Regla:** El verde `#838C2F` es **invariable** — mismo valor en claro y oscuro. El azul marino puede aclararse para mantener contraste sobre fondos muy oscuros.

---

## 10. SUBMARCA — CAFETERÍA · RESTAURANT · BAR

La submarca de alimentos y bebidas comparte la identidad HPG con estas particularidades:

### Logo con submarca
- Archivo: `Hotel_PuntaGalería_Caféteria-Restaurant-Bar.png`
- "Galería" en verde `#838C2F` dentro del wordmark
- Texto "CAFETERÍA · RESTAURANT · BAR" en Brisbane, uppercase, `#323F48`, kerning amplio, separado del wordmark por línea navy

### Tokens adicionales para F&B
```css
:root {
  --hpg-fnb-accent:  #236D00;  /* verde frondoso — mayor vitalidad para el área de alimentos */
  --hpg-fnb-bg:      #E5E0D8;  /* lino como fondo de menú */
  --hpg-fnb-header:  #323F48;  /* navy para encabezado de menú */
}
```

### Regla de uso del verde frondoso `#236D00`
Reservado para la submarca F&B y piezas de comunicación de exteriores / jardín. No usar como acento general de la marca hotel.

---

## 11. REGLAS DE ORO (resumen ejecutivo para IA/agentes)

1. **Azul Marino `#323F48`** — color de identidad absoluto. Va en: encabezados, nav, footer, fondo oscuro, borde de tabla, header de reporte, botón primario.
2. **Verde Galería `#838C2F`** — acento de vida natural. Va en: eyebrows, "Galería" en el logo bicolor, badges, banda de acento bajo header, botón secundario.
3. **Verde Bosque `#626C1F`** — hover/pressed del verde galería. Nunca como color base independiente.
4. **Verde Frondoso `#236D00`** — solo en submarca F&B y comunicación exterior/jardín.
5. **Arena `#C7B7A4`** — separadores, bordes de card, fondo de tabla.
6. **Lino `#E5E0D8`** — fondo principal cálido de toda la identidad (NO blanco puro).
7. **Brisbane** — toda tipografía display visible: títulos, encabezados de tabla, botones, eyebrows. Siempre kerning −0.02em.
8. **La Bohemienne Deluxe** — SOLO en el wordmark "hotel" del logo y piezas editoriales de lujo. Nunca en UI funcional.
9. **Salford Sans VF** — todo el texto corrido, descripciones, párrafos, cuerpo de tablas.
10. **Banda verde** `#838C2F` bajo el header de reporte — 3px, siempre presente.
11. **Logo sobre fondo oscuro** → siempre versión negativo (blanco), nunca coloreado.
12. **Fondo base** → lino `#E5E0D8`, nunca blanco puro para documentos y reportes.

---

## 12. RELACIÓN CON EL SISTEMA GO

| Elemento | Sistema GO (`context_design.md`) | Sub-marca HPG (este archivo) |
|----------|----------------------------------|------------------------------|
| Acento primario | `#FB670B` naranja | `#323F48` azul marino |
| Acento secundario | — | `#838C2F` verde galería |
| Fondo cálido | `#ECEBE0` crema | `#E5E0D8` lino |
| Fondo cálido secundario | — | `#C7B7A4` arena |
| Tipografía display | Blauer Nue | Brisbane (−20 kerning) |
| Tipografía cuerpo | Conthic | Salford Sans VF |
| Tipografía especial | — | La Bohemienne (solo logo) |
| Banda de acento en reporte | Naranja `#FB670B` | Verde `#838C2F` |
| Botón primario | Naranja | Azul Marino `#323F48` |

### Regla de carga para agentes e IA
```
Proyecto HPG solo         → context_design.md  +  hotel-punta-galeria.md
Proyecto multi-marca      → context_design.md  +  brand_system.md  +  hotel-punta-galeria.md
Submarca F&B              → hotel-punta-galeria.md  §10 (tokens --hpg-fnb-*)
Conflicto de color GO/HPG → brand_system.md §4 (Tabla de conflictos)
```

---

## 13. RUTAS DE ASSETS

```
hotel punta galeria/
├── 01_LOGO/
│   ├── Hotel_PuntaGalería_Azul.png                       ← Principal monocromo navy
│   ├── Hotel_PuntaGalería_Caféteria-Restaurant-Bar.png   ← Con submarca F&B, bicolor
│   └── Hotel_PuntaGalería_negativo.png                   ← Blanco sobre fondos oscuros
│
├── 02_TIPOGRAFIA/
│   ├── la-bohemienne-deluxe.otf    ← Script caligráfico — solo logo "hotel"
│   └── Brisbane-Bold_Trial-BF660e1a392b91c.otf  ← Display / encabezados
│   (Salford Sans VF → fuente de sistema / Google Fonts)
│
└── 03_PALETA DE COLORES/
    ├── color_palette.png   ← Referencia visual completa con Pantone/CMYK
    ├── 323f48.png  ← Azul Marino HPG (primario)
    ├── 838c2f.png  ← Verde Galería (no incluido como .png individual, ver color_palette)
    ├── 626c1f.png  ← Verde Bosque
    ├── 236d00.png  ← Verde Frondoso / F&B
    ├── c7b7a4.png  ← Arena HPG
    └── e5e0d8.png  ← Lino HPG
```

---

*Última actualización: 2026-05-19 · Sistema HPG integrado al ecosistema Grupo Ortiz*
