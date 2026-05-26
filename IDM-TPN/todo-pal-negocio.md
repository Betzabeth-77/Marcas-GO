# Todo Pal Negocio® — Design System Context
> Fuente de verdad para todos los proyectos digitales de la marca. Aplica a: web apps, catálogos HTML, PDFs, emails, tablas, presentaciones y cualquier pieza digital de Todo Pal Negocio®.
> Este archivo **extiende** (no reemplaza) el sistema base de Grupo Ortiz definido en `context_design.md`.

---

## 1. IDENTIDAD DE MARCA

**Marca:** Todo Pal Negocio®  
**Abreviatura oficial:** TPN  
**Símbolo:** Puesto de comida emergiendo de una caja de cartón abierta — representa el negocio emprendedor accesible, listo para arrancar  
**Tipografía del logo:** Eigerdals (bold redondeada) — "todo pal negocio®" siempre en minúsculas  
**Color primario:** Rojo TPN `#E30F2C`  
**Color secundario:** Amarillo TPN `#FDD823`  
**Color de apoyo:** Azul pizarra TPN `#56717B`  
**Sector:** Comercio / insumos para emprendedores y negocios de calle  
**Tono de marca:** Cercano, directo, popular, energético — habla de tú al emprendedor

---

## 2. PALETA DE COLORES OFICIAL

### Primarios
| Nombre | Hex | Uso |
|--------|-----|-----|
| Rojo TPN | `#E30F2C` | Color de marca principal, fondos de logo, CTAs, acentos, botones primarios, headers |
| Amarillo TPN | `#FDD823` | Color secundario, highlights, precios, etiquetas de oferta, fondos de acento cálido |
| Azul Pizarra TPN | `#56717B` | Color de apoyo, fondos neutros con personalidad, texto sobre claro, encabezados sobrios |

### Neutros
| Nombre | Hex | Uso |
|--------|-----|-----|
| Negro TPN | `#1A1A1A` | Texto principal, fondos oscuros extremos |
| Café contorno | `#3D1F00` | Contorno del isotipo / ilustración (líneas del puesto y caja) |
| Cartón / Kraft | `#E8B87A` | Color de la caja del isotipo — fondo cálido alternativo para secciones de contenido |
| Blanco | `#FFFFFF` | Fondo principal, texto sobre rojo/oscuro |

### Paleta completa ordenada (oscuro → claro)
```
#1A1A1A  →  #56717B  →  #E30F2C  →  #E8B87A  →  #FDD823  →  #FFFFFF
```
Con acento frio: `#56717B` (azul pizarra)

### Tokens CSS recomendados
```css
:root {
  /* Primarios */
  --tpn-red:         #E30F2C;
  --tpn-red-hot:     #FF1F3A;        /* hover */
  --tpn-red-deep:    #BF0A24;        /* pressed */
  --tpn-red-tint:    rgba(227,15,44,0.10); /* fondos suaves */

  --tpn-yellow:      #FDD823;
  --tpn-yellow-hot:  #FFE033;        /* hover */
  --tpn-yellow-deep: #D9B800;        /* pressed */
  --tpn-yellow-tint: rgba(253,216,35,0.15);

  --tpn-slate:       #56717B;
  --tpn-slate-dark:  #3F5560;        /* hover / pressed */
  --tpn-slate-tint:  rgba(86,113,123,0.10);

  /* Neutros */
  --tpn-black:   #1A1A1A;
  --tpn-outline: #3D1F00;
  --tpn-kraft:   #E8B87A;
  --tpn-white:   #FFFFFF;

  /* Semánticos */
  --tpn-bg:        var(--tpn-white);
  --tpn-bg-warm:   var(--tpn-kraft);
  --tpn-bg-cool:   var(--tpn-slate-tint);
  --tpn-text:      var(--tpn-black);
  --tpn-text-2:    var(--tpn-slate);
  --tpn-accent:    var(--tpn-red);
  --tpn-accent-2:  var(--tpn-yellow);
  --tpn-border:    rgba(86,113,123,0.25);
}
```

### Texturas / fondos de marca
TPN cuenta con 3 texturas de rayos (starburst) para fondos de piezas promocionales:

| Archivo | Color base | Uso |
|---------|-----------|-----|
| `Textura_tpn.png` | Amarillo `#FDD823` | Fondo de piezas de oferta, catálogos cálidos |
| `Textura_tpn_2.png` | Azul Pizarra `#56717B` | Fondo de piezas institucionales, encabezados sobrios |
| `Textura_tpn_3.png` | Rojo `#E30F2C` | Fondo de piezas de alto impacto, portadas, banners principales |

**Regla:** Las texturas son opcionales — se usan en piezas impresas y digitales de alto impacto. Nunca como fondo de UI funcional (formularios, tablas, reportes).

---

## 3. TIPOGRAFÍA

### Fuentes oficiales TPN

| Fuente | Rol | Características |
|--------|-----|-----------------|
| **Eigerdals** | **PRINCIPAL** — logo, display, títulos, UI | Bold redondeada, alto impacto, amigable y directa. Usada en "todo pal negocio®" |
| **Como** | Cuerpo / apoyo / texto corrido | Geométrica sans, legible en tamaños pequeños — tablas, descripciones, reportes |

### Fallbacks seguros (cuando fuentes TPN no estén instaladas)
```css
--tpn-font-display: 'Eigerdals', 'Nunito', 'Poppins', 'Rounded Mplus 1c', sans-serif;
--tpn-font-body:    'Como', 'Inter', 'DM Sans', 'Segoe UI', system-ui, sans-serif;
--tpn-font-mono:    'JetBrains Mono', 'Fira Code', Consolas, monospace;
```

### Escala tipográfica
| Nivel | Fuente | Tamaño | Peso | Uso |
|-------|--------|--------|------|-----|
| Display XL | Eigerdals | 72–96px | 900 | Portadas, hero, banners de oferta |
| H1 | Eigerdals | 48–64px | 800 | Títulos principales de página |
| H2 | Eigerdals | 32–40px | 700 | Secciones, títulos de tarjeta |
| H3 | Eigerdals | 24–28px | 700 | Subtítulos |
| H4 | Eigerdals | 18–20px | 700 | Encabezados de tabla, labels fuertes |
| Body | Como | 14–16px | 400 | Texto corrido, descripciones de producto |
| Body Small | Como | 12–13px | 400 | Notas, pie de página, metadatos |
| Label | Eigerdals | 10–11px | 700 | Etiquetas, eyebrows (uppercase + letter-spacing) |
| Precio / Oferta | Eigerdals | 20–32px | 900 | Precios destacados, porcentajes de descuento |
| Mono | JetBrains Mono | 12–13px | 400 | Códigos de producto, SKUs, fechas, cifras técnicas |

### Reglas tipográficas
- **Eyebrow / label:** `font-family: var(--tpn-font-display); font-size: 11px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.14em; color: var(--tpn-red)`
- **Precio destacado:** `font-family: var(--tpn-font-display); font-weight: 900; color: var(--tpn-red)` — nunca en azul pizarra
- **Etiqueta de oferta / badge:** fondo `#FDD823`, texto `#1A1A1A`, Eigerdals bold
- **Título de sección:** `font-family: var(--tpn-font-display); font-weight: 800; text-transform: uppercase`
- Nunca mezclar más de 2 fuentes en una misma pieza
- El nombre de marca "todo pal negocio®" **siempre en minúsculas** — nunca en mayúsculas ni capitalizado

---

## 4. LOGO — VARIANTES Y USO

### Anatomía del sistema de logo

```
ISOTIPO      = La caja con el puesto de comida (ilustración sola, sin texto)
IMAGOTIPO    = Isotipo + "todo pal negocio®" (ícono + texto)
LOGOTIPO     = "todo pal negocio®" (texto solo, Eigerdals)
```

### Archivos disponibles
| Archivo | Descripción | Contenedor | Usar sobre |
|---------|-------------|------------|------------|
| `Logo_Todo_pal_negocio-01.png` | Imagotipo vertical — fondo círculo rojo | Círculo rojo `#E30F2C` | Fondo blanco, claro, kraft |
| `Logo_Todo_pal_negocio-02.png` | Logotipo horizontal — fondo píldora rojo | Píldora roja `#E30F2C`, texto blanco | Fondo blanco o claro |
| `Logo_Todo_pal_negocio-03.png` | Logotipo horizontal — fondo píldora blanco | Píldora blanca, texto rojo | Fondo blanco o muy claro |
| `Logo_Todo_pal_negocio-04.png` | Imagotipo vertical — fondo círculo blanco | Círculo blanco, texto rojo | Fondo blanco o muy claro |
| `Logo_Todo_pal_negocio-05.png` | Imagotipo vertical — fondo negro | Sin contenedor, texto blanco | Fondo negro u oscuro |

### Fondo del ícono en UI
Cuando el logo se use en contenedor pequeño (nav, favicon, avatar):
- Fondo: `#E30F2C` (rojo) — **siempre, sin importar modo claro u oscuro**
- Border-radius: `8px` (nav small), `14px` (login/card), `50%` (avatar redondo)
- Logo PNG: versión blanca sobre ese fondo (equivalente al -05 sin fondo negro)

### Color del texto de marca en UI
- Sobre fondo rojo → texto **blanco** `#FFFFFF`
- Sobre fondo blanco/claro → texto **rojo** `#E30F2C`
- Sobre fondo negro/oscuro → texto **blanco** `#FFFFFF`
- **Nunca** texto amarillo para el nombre de marca

### Espacio de respeto
- Mínimo: `= altura de la caja del isotipo × 0.25` alrededor del logo completo
- Nunca distorsionar proporciones
- Nunca aplicar efectos (sombra extra, gradiente, stroke adicional)
- Nunca cambiar colores fuera del sistema (rojo, amarillo, azul pizarra, blanco, negro)

---

## 5. COMPONENTES UI

### Botón primario
```css
.btn-primary {
  background: var(--tpn-red);
  color: #fff;
  font-family: var(--tpn-font-display);
  font-weight: 700;
  font-size: 14px;
  letter-spacing: 0.04em;
  border: none;
  border-radius: 8px;
  padding: 12px 24px;
  cursor: pointer;
  transition: background 200ms ease;
}
.btn-primary:hover  { background: #FF1F3A; }
.btn-primary:active { background: #BF0A24; }
```

### Botón secundario / amarillo (oferta)
```css
.btn-offer {
  background: var(--tpn-yellow);
  color: var(--tpn-black);
  font-family: var(--tpn-font-display);
  font-weight: 800;
  font-size: 14px;
  border: none;
  border-radius: 8px;
  padding: 12px 24px;
  cursor: pointer;
  transition: background 200ms ease;
}
.btn-offer:hover  { background: #FFE033; }
.btn-offer:active { background: #D9B800; }
```

### Botón ghost / slate
```css
.btn-ghost {
  background: transparent;
  color: var(--tpn-slate);
  border: 1.5px solid var(--tpn-slate);
  border-radius: 8px;
  padding: 10px 20px;
  font-family: var(--tpn-font-display);
  font-weight: 600;
  transition: all 200ms ease;
}
.btn-ghost:hover { border-color: var(--tpn-red); color: var(--tpn-red); }
```

### Card / tarjeta de producto
```css
.card {
  background: var(--tpn-white);
  border: 1px solid rgba(86,113,123,0.20);
  border-radius: 12px;
  padding: 20px;
  box-shadow: 0 2px 8px rgba(26,26,26,0.06);
}
.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 14px;
  padding-bottom: 10px;
  border-bottom: 2px solid var(--tpn-red);
}
.card-title {
  font-family: var(--tpn-font-display);
  font-weight: 700;
  font-size: 13px;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--tpn-black);
}
```

### Input / campo de formulario
```css
.input {
  width: 100%;
  padding: 10px 14px;
  border: 1.5px solid rgba(86,113,123,0.35);
  border-radius: 8px;
  font-family: var(--tpn-font-body);
  font-size: 14px;
  color: var(--tpn-black);
  background: var(--tpn-white);
  transition: border-color 200ms;
}
.input:focus {
  outline: none;
  border-color: var(--tpn-red);
  box-shadow: 0 0 0 3px rgba(227,15,44,0.10);
}
```

### Badge / etiqueta de oferta
```css
/* Oferta / promoción */
.badge-offer {
  display: inline-block;
  background: var(--tpn-yellow);
  color: var(--tpn-black);
  font-family: var(--tpn-font-display);
  font-size: 11px; font-weight: 800;
  padding: 3px 10px;
  border-radius: 20px;
  text-transform: uppercase;
  letter-spacing: 0.06em;
}
/* Nuevo producto */
.badge-new {
  background: var(--tpn-red);
  color: #fff;
  font-family: var(--tpn-font-display);
  font-size: 11px; font-weight: 700;
  padding: 3px 10px;
  border-radius: 20px;
  text-transform: uppercase;
}
/* Disponible / activo */
.badge-ok {
  background: rgba(86,113,123,0.12);
  color: var(--tpn-slate-dark);
  font-size: 11px; font-weight: 600;
  padding: 3px 10px;
  border-radius: 20px;
}
```

---

## 6. TABLAS

```css
.tpn-table {
  width: 100%;
  border-collapse: collapse;
  font-family: var(--tpn-font-body);
  font-size: 13px;
  color: var(--tpn-black);
}
.tpn-table thead tr {
  border-top: 3px solid var(--tpn-red);
  background: #F8F8F8;
}
.tpn-table th {
  font-family: var(--tpn-font-display);
  font-weight: 700;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.10em;
  color: var(--tpn-black);
  padding: 10px 14px;
  text-align: left;
}
.tpn-table td {
  padding: 10px 14px;
  border-bottom: 1px solid rgba(86,113,123,0.15);
}
.tpn-table tbody tr:hover { background: rgba(253,216,35,0.08); }

/* Columna de precio */
.tpn-table .col-price {
  font-family: var(--tpn-font-display);
  font-weight: 900;
  color: var(--tpn-red);
  font-size: 14px;
}
/* Columna de SKU / código */
.tpn-table .col-sku {
  font-family: var(--tpn-font-mono);
  font-size: 12px;
  color: var(--tpn-slate);
  letter-spacing: 0.04em;
}
/* Fila destacada (oferta) */
.tpn-table tr.featured {
  background: rgba(253,216,35,0.12);
  border-left: 3px solid var(--tpn-yellow);
}
```

---

## 7. CATÁLOGO / REPORTE HTML

Plantilla base para catálogos de producto y reportes internos:

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Nunito:wght@400;700;900&display=swap');

    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { background: #F4F4F4; font-family: 'Como', 'Inter', sans-serif; }
    .wrapper { max-width: 900px; margin: 0 auto; background: #fff; }

    /* Header del reporte */
    .report-header {
      background: #E30F2C;
      padding: 24px 40px;
      display: flex;
      align-items: center;
      gap: 20px;
    }
    .report-logo-box {
      width: 56px; height: 56px;
      background: #fff;
      border-radius: 12px;
      display: flex; align-items: center; justify-content: center;
      overflow: hidden;
    }
    .report-logo-box img { width: 48px; height: 48px; object-fit: contain; }
    .report-brand { color: #fff; }
    .report-brand strong {
      font-family: 'Eigerdals', 'Nunito', sans-serif;
      font-size: 20px; font-weight: 800;
      display: block;
    }
    .report-brand small {
      font-size: 11px; color: rgba(255,255,255,0.65);
      text-transform: uppercase; letter-spacing: 0.14em;
    }

    /* Banda amarilla de acento */
    .report-accent-bar { height: 4px; background: #FDD823; }

    /* Sección */
    .report-section {
      background: #FFFFFF;
      margin: 0; padding: 32px 40px;
      border-bottom: 1px solid rgba(86,113,123,0.15);
    }
    .report-section-label {
      font-family: 'Eigerdals', 'Nunito', sans-serif;
      font-size: 10px; font-weight: 700;
      text-transform: uppercase; letter-spacing: 0.18em;
      color: #E30F2C; margin-bottom: 12px;
    }

    /* KPI grande */
    .kpi-value {
      font-family: 'Eigerdals', 'Nunito', sans-serif;
      font-size: 42px; font-weight: 900;
      color: #1A1A1A; letter-spacing: -0.02em;
    }
    .kpi-label { font-size: 12px; color: #56717B; margin-top: 4px; }

    /* Badge de oferta en catálogo */
    .offer-tag {
      display: inline-block;
      background: #FDD823;
      color: #1A1A1A;
      font-family: 'Eigerdals', 'Nunito', sans-serif;
      font-size: 12px; font-weight: 800;
      padding: 4px 12px; border-radius: 20px;
      text-transform: uppercase; letter-spacing: 0.06em;
    }

    /* Footer */
    .report-footer {
      background: #1A1A1A; padding: 20px 40px;
      text-align: center;
      font-size: 11px; color: rgba(255,255,255,0.4);
    }
  </style>
</head>
<body>
  <div class="wrapper">
    <div class="report-header">
      <div class="report-logo-box">
        <img src="cid:logo" alt="TPN">
      </div>
      <div class="report-brand">
        <strong>todo pal negocio®</strong>
        <small>Catálogo de Productos · 2026</small>
      </div>
    </div>
    <div class="report-accent-bar"></div>

    <div class="report-section">
      <div class="report-section-label">Ofertas del mes</div>
      <!-- contenido -->
    </div>

    <div class="report-footer">
      todo pal negocio® · Grupo Ortiz · Confidencial
    </div>
  </div>
</body>
</html>
```

---

## 8. PDF / PRINT

```css
@media print {
  body { background: #fff; color: #1A1A1A; }
  * { box-shadow: none !important; transition: none !important; }

  /* Rojo y amarillo se imprimen bien en la mayoría de impresoras */
  .tpn-accent   { color: #E30F2C; }
  .tpn-accent-2 { color: #FDD823; }

  /* Encabezado de página PDF */
  .pdf-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 3px solid #E30F2C;
    padding-bottom: 16px;
    margin-bottom: 24px;
  }
  .pdf-footer {
    position: fixed;
    bottom: 0; left: 0; right: 0;
    border-top: 1px solid rgba(86,113,123,0.25);
    padding: 8px 40px;
    font-size: 10px; color: #56717B;
    display: flex; justify-content: space-between;
  }

  .page-break { page-break-before: always; }
  .no-break   { page-break-inside: avoid; }
}
```

### Márgenes de página recomendados
- Carta/A4: `margin: 20mm 25mm`
- Header fijo: logo TPN izquierda + fecha derecha
- Footer fijo: `todo pal negocio® · Confidencial · Página X de Y`
- Color de línea divisoria encabezado: `#E30F2C` 3pt

---

## 9. MODO OSCURO (web apps)

```css
body[data-mode="dark"] {
  --tpn-bg:      #0F0F0F;
  --tpn-bg-warm: #1A1A1A;
  --tpn-text:    #FFFFFF;
  --tpn-text-2:  #8FA8B0;
  --tpn-border:  rgba(255,255,255,0.08);
  /* Rojo y amarillo NO cambian — mismos valores en ambos modos */
  --tpn-red:     #E30F2C;
  --tpn-yellow:  #FDD823;
  /* Azul pizarra se aclara ligeramente para mayor contraste */
  --tpn-slate:   #7A9BA5;
}
```

**Regla de oro:** El rojo `#E30F2C` y el amarillo `#FDD823` son **invariables** — mismo valor en modo claro y oscuro. Solo los neutros se invierten.

---

## 10. REGLAS DE ORO (resumen ejecutivo para IA/agentes)

1. **Rojo `#E30F2C`** — color de acento universal. Va en: botones primarios, encabezados, eyebrows, bordes de tabla, barras de acento, fondo del ícono TPN, precio en negativo.
2. **Amarillo `#FDD823`** — color de oferta y energía. Va en: badges de descuento, botones secundarios, highlights de fila en tabla, banda de acento bajo el header.
3. **Azul Pizarra `#56717B`** — neutro con personalidad. Va en: texto secundario, fondos institucionales, íconos de apoyo. Nunca compite con rojo o amarillo.
4. **Negro `#1A1A1A`** — texto principal, fondos oscuros, headers de reporte dark.
5. **Eigerdals** — toda tipografía visible de marca (títulos, precios, labels, logo text).
6. **Como** — texto corrido, descripciones de producto, tablas, cuerpo de reporte.
7. **Logo texto** — "todo pal negocio®" **siempre en minúsculas**, nunca en mayúsculas ni capitalizado.
8. **Logo ícono en UI** — siempre sobre fondo rojo `#E30F2C` cuando va en contenedor pequeño.
9. **Precios** — Eigerdals weight 900, color rojo `#E30F2C` — nunca en fuente mono (diferencia clave vs. sistema GO).
10. **Texturas de rayos** — solo en piezas de alto impacto (portadas, banners, flyers) — nunca en UI funcional.
11. **Banda de acento** bajo el header de reporte: `#FDD823` (amarillo), no rojo.
12. **No mezclar** más de 2 pesos de fuente en una misma sección.

---

## 11. RELACIÓN CON EL SISTEMA GO

Este archivo define la capa TPN — una extensión del sistema base GO.

| Elemento | Sistema GO (`context_design.md`) | Sub-marca TPN (este archivo) |
|----------|----------------------------------|------------------------------|
| Acento primario | `#FB670B` naranja | `#E30F2C` rojo |
| Acento secundario | — | `#FDD823` amarillo |
| Apoyo neutro | `#262626` negro puro | `#56717B` azul pizarra |
| Fondo cálido | `#ECEBE0` crema | `#E8B87A` kraft |
| Tipografía display | Blauer Nue | Eigerdals |
| Tipografía cuerpo | Conthic | Como |
| Precios | JetBrains Mono | Eigerdals weight 900 |
| Banda de acento en reporte | Naranja `#FB670B` | Amarillo `#FDD823` |

### Regla de carga para agentes e IA
```
Proyecto TPN solo         → context_design.md  +  todo-pal-negocio.md
Proyecto multi-marca      → context_design.md  +  brand_system.md  +  todo-pal-negocio.md
Conflicto de color GO/TPN → brand_system.md §4 (Tabla de conflictos)
```

---

## 12. RUTAS DE ASSETS

```
todo pal negocio/
├── 01_LOGO/
│   ├── Logo_Todo_pal_negocio-01.png  ← Imagotipo circular, fondo rojo
│   ├── Logo_Todo_pal_negocio-02.png  ← Logotipo horizontal, píldora roja
│   ├── Logo_Todo_pal_negocio-03.png  ← Logotipo horizontal, píldora blanca
│   ├── Logo_Todo_pal_negocio-04.png  ← Imagotipo circular, fondo blanco
│   └── Logo_Todo_pal_negocio-05.png  ← Imagotipo vertical, fondo negro
│
├── 02_TIPOGRAFIA/
│   ├── eigerdals/                    ← PRINCIPAL — instalar primero
│   └── como/                         ← Cuerpo / tablas / catálogos
│
├── 03_PALETA DE COLORES/
│   ├── MUESTAS_TPN.aco               ← Muestras Adobe Color
│   ├── e30f2c.png  ← Rojo TPN (primario)
│   ├── fdd823.png  ← Amarillo TPN (secundario)
│   └── 56717b.png  ← Azul Pizarra TPN (apoyo)
│
└── 04_TEXTURAS/
    ├── Textura_tpn.png    ← Rayos amarillos
    ├── Textura_tpn_2.png  ← Rayos azul pizarra
    └── Textura_tpn_3.png  ← Rayos rojos
```

---

*Última actualización: 2026-05-12 · Sistema TPN integrado al ecosistema Grupo Ortiz*
