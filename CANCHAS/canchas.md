# Club Atlético de Morelia — Design System Context
> Fuente de verdad para todos los proyectos digitales e impresos del club. Aplica a: web apps, reportes HTML, PDFs, emails, uniformes, merchandising, señalética y cualquier pieza de comunicación visual del Club Atlético de Morelia.

---

## 1. IDENTIDAD DE MARCA

**Club:** Club Atlético de Morelia  
**Abreviatura oficial:** CAM  
**Sector:** Deporte / Fútbol / Academia  
**Sede:** Morelia, Michoacán, México  
**Símbolo:** Escudo heráldico con balón en llamas — representa pasión, fuego competitivo y arraigo local  
**Tipografía del nombre en escudo:** Anton (condensada, bold, impacto)  
**Tipografía de apoyo principal:** Bebas Neue Cyrillic (display, títulos)  
**Tipografía de cuerpo:** Open Sauce One / Open Sans  
**Color primario:** Azul Oscuro `#0E1D31`  
**Color de acento:** Rojo `#EE0E2F`  
**Color de detalle:** Amarillo / Dorado `#F4D722`

---

## 2. PALETA DE COLORES OFICIAL

### Colores primarios
| Nombre | Hex | Pantone | CMYK | RGB | Uso |
|--------|-----|---------|------|-----|-----|
| Azul Oscuro | `#0E1D31` | 296 C | 71, 41, 0, 81 | 14, 29, 49 | Color de fondo principal, escudo, uniformes navy, fondos de reporte |
| Rojo | `#EE0E2F` | 185 C | 0, 94, 80, 7 | 238, 14, 47 | Banda central del escudo, CTAs, acentos energéticos, botones primarios |
| Amarillo / Dorado | `#F4D722` | 109 C | 0, 12, 86, 4 | 244, 215, 34 | Texto "CLUB" y "MORELIA" en escudo, estrella, detalles premium, eyebrows |

### Neutros
| Nombre | Hex | Pantone | CMYK | RGB | Uso |
|--------|-----|---------|------|-----|-----|
| Blanco | `#FFFFFF` | White | 0, 0, 0, 0 | 255, 255, 255 | Texto sobre fondo oscuro/rojo, fondo de documentos, logo versión negativa |
| Negro | `#000000` | Black C | 0, 0, 0, 100 | 0, 0, 0 | Contorno del escudo, texto de alto contraste, sombras |

### Paleta ordenada (oscuro → claro)
```
#0E1D31  →  #EE0E2F  →  #F4D722  →  #FFFFFF
```
Con neutro de anclaje: `#000000` (contornos y sombras del escudo)

### Transparencias del Azul Oscuro
El manual establece el uso de `#0E1D31` en diferentes opacidades como recurso gráfico para overlays fotográficos.

| Uso | Valor |
|-----|-------|
| Overlay máximo (fondos de sección) | `rgba(14,29,49,0.90)` |
| Overlay medio (sobre fotografía) | `rgba(14,29,49,0.65)` |
| Overlay suave (textura de fondo) | `rgba(14,29,49,0.40)` |
| Tint muy suave (áreas de contenido) | `rgba(14,29,49,0.12)` |

### Tokens CSS recomendados
```css
:root {
  /* Colores de marca */
  --cam-navy:        #0E1D31;
  --cam-red:         #EE0E2F;
  --cam-red-hot:     #FF2040;         /* hover */
  --cam-red-deep:    #CC0A27;         /* pressed */
  --cam-red-tint:    rgba(238,14,47,0.12);  /* fondos suaves */
  --cam-yellow:      #F4D722;
  --cam-yellow-hot:  #FFE033;         /* hover */
  --cam-yellow-tint: rgba(244,215,34,0.15);

  /* Neutros */
  --cam-black:   #000000;
  --cam-white:   #FFFFFF;
  --cam-gray-1:  #2A3A4A;             /* texto secundario sobre oscuro */
  --cam-gray-2:  #8A9AAA;             /* bordes, separadores */
  --cam-gray-3:  #D0D8E0;             /* fondos de tabla alternos claros */
  --cam-off-white: #F2F4F6;           /* fondo cálido de documentos */

  /* Overlays Navy */
  --cam-navy-90: rgba(14,29,49,0.90);
  --cam-navy-65: rgba(14,29,49,0.65);
  --cam-navy-40: rgba(14,29,49,0.40);
  --cam-navy-12: rgba(14,29,49,0.12);

  /* Semánticos */
  --cam-bg:        var(--cam-navy);
  --cam-bg-light:  var(--cam-off-white);
  --cam-text:      var(--cam-white);
  --cam-text-dark: var(--cam-navy);
  --cam-text-2:    var(--cam-gray-2);
  --cam-accent:    var(--cam-red);
  --cam-accent-2:  var(--cam-yellow);
  --cam-border:    rgba(255,255,255,0.12);
}
```

### Modo de uso por contexto
| Contexto | Fondo | Texto | Acento |
|----------|-------|-------|--------|
| Digital / web (default) | `#0E1D31` | `#FFFFFF` | `#EE0E2F` / `#F4D722` |
| Reportes / documentos claros | `#F2F4F6` | `#0E1D31` | `#EE0E2F` |
| Email corporativo | `#FFFFFF` | `#0E1D31` | `#EE0E2F` |
| Señalética / merchandising | `#0E1D31` | `#FFFFFF` | `#F4D722` |
| Uniformes | `#0E1D31` (principal) | `#F4D722` (número/nombre) | `#EE0E2F` (banda) |

---

## 3. TIPOGRAFÍA

### Fuentes oficiales CAM
Las tres fuentes son de uso libre y están disponibles en Google Fonts.

| Fuente | Rol | Características | Descarga |
|--------|-----|-----------------|----------|
| **Anton** | **PRINCIPAL — nombre del club en escudo, display de alto impacto** | Condensada, negrita, sans-serif de alto impacto. Trazos uniformes, sin serif. Perfecta para titulares deportivos | `fonts.google.com/specimen/Anton` |
| **Bebas Neue Cyrillic** | Titulares, secciones, display secundario | All-caps condensada, geométrica, muy legible en grande. Estilo deportivo premium | `fonts.google.com/specimen/Bebas+Neue` |
| **Open Sauce One** | Cuerpo de texto, párrafos, descripciones | Humanista, legible en tamaños pequeños. Disponible en Regular y Bold | `github.com/marcologous/Open-Sauce-Fonts` |
| **Open Sans** | Apoyo de cuerpo, UI alternativo | Sans-serif neutro de alta legibilidad — usar cuando Open Sauce One no esté disponible | `fonts.google.com/specimen/Open+Sans` |

### Fallbacks seguros (cuando fuentes CAM no estén instaladas)
```css
--cam-font-display:  'Anton', 'Impact', 'Arial Black', sans-serif;
--cam-font-headline: 'Bebas Neue', 'Anton', 'Arial Narrow', sans-serif;
--cam-font-body:     'Open Sauce One', 'Open Sans', 'Inter', 'Helvetica Neue', sans-serif;
--cam-font-mono:     'JetBrains Mono', 'Fira Code', Consolas, monospace;
```

### Escala tipográfica
| Nivel | Fuente | Tamaño | Peso | Uso |
|-------|--------|--------|------|-----|
| Display XL | Anton | 72–96px | 400 (Anton es inherentemente bold) | Portadas, hero sections, nombre del club en grande |
| H1 | Bebas Neue | 48–64px | 400 | Títulos principales de página |
| H2 | Bebas Neue | 32–40px | 400 | Secciones, títulos de tarjeta |
| H3 | Bebas Neue | 24–28px | 400 | Subtítulos, encabezados de módulo |
| H4 | Open Sauce One Bold | 18–20px | 700 | Encabezados de tabla, labels fuertes |
| Body | Open Sauce One Regular | 14–16px | 400 | Texto corrido, párrafos, descripciones |
| Body Small | Open Sans Regular | 12–13px | 400 | Notas, pie de página, metadatos |
| Label / Eyebrow | Bebas Neue | 11–12px | 400 | Etiquetas uppercase + letter-spacing |
| Mono | JetBrains Mono | 12–13px | 400 | Estadísticas, marcadores, fechas, códigos |

### Reglas tipográficas
- **Eyebrow / label:** `font-family: var(--cam-font-headline); font-size: 12px; text-transform: uppercase; letter-spacing: 0.18em; color: var(--cam-yellow)`
- **Nombre del equipo en display:** `font-family: var(--cam-font-display); text-transform: uppercase; letter-spacing: -0.01em`
- **Títulos de sección:** `font-family: var(--cam-font-headline); text-transform: uppercase; letter-spacing: 0.06em`
- **Estadísticas / marcador:** `font-family: var(--cam-font-mono); font-variant-numeric: tabular-nums; letter-spacing: -0.02em`
- Anton se usa **solo** en piezas de alto impacto visual — nunca en texto corrido
- Bebas Neue para jerarquías intermedias — secciones, subtítulos, labels
- Open Sauce / Open Sans para toda lectura corrida
- Nunca mezclar más de 2 familias tipográficas en una misma pieza
- Amarillo `#F4D722` solo en acentos tipográficos y eyebrows — nunca en párrafos largos
- Rojo `#EE0E2F` para CTAs tipográficos y elementos de acción

---

## 4. LOGO / ESCUDO — DESCRIPCIÓN Y USO

### Anatomía del escudo
```
ESCUDO HERÁLDICO     = Forma de escudo con borde rojo y fondo azul oscuro
BALÓN + LLAMAS       = Pelota de fútbol en blanco/negro coronada con llamas rojas/naranjas
BANDA ROJA CENTRAL   = Franja horizontal con "ATLETICO" en Anton blanco
TEXTO SUPERIOR       = "CLUB" en Bebas Neue dorado (#F4D722)
TEXTO INFERIOR       = "MORELIA" en Bebas Neue dorado (#F4D722)
ESTRELLA             = Estrella dorada de 5 puntas en la parte inferior del escudo
```

### Descripción del símbolo
El escudo combina elementos del fútbol (balón) con simbolismo de pasión y fuego (llamas). Las llamas en rojo-naranja sobre el balón expresan la intensidad competitiva. La estructura heráldica otorga tradición e identidad institucional. La estrella en la parte inferior puede representar logros o títulos del club.

### Variantes de logo disponibles
| Archivo | Descripción | Usar sobre |
|---------|-------------|------------|
| `ATLETICO_CLUB-MORELIA_LOGO.png` | Escudo completo sobre fondo negro | Fondos claros (el PNG tiene fondo negro — usar versión AI para otros usos) |
| `ATLETICO_CLUB-MORELIA_LOGO.ai` | Archivo fuente Illustrator (editable) | Cualquier aplicación, cualquier escala |

### Variantes de color según contexto
| Contexto | Aplicación |
|----------|-----------|
| Fondo navy `#0E1D31` | Escudo completo en sus colores originales |
| Fondo blanco / claro | Escudo completo — el navy del escudo genera contraste suficiente |
| Fondo rojo `#EE0E2F` | Escudo completo — verificar contraste del borde rojo |
| Merchandising negro | Escudo completo — alta legibilidad |
| Bordado (uniformes) | Versión simplificada — reducir detalle de llamas para bordado |

### Usos NO permitidos (especificados en el manual)
- ❌ **Cambios de color** — el escudo solo existe en su paleta oficial (azul navy + rojo + amarillo + blanco + negro)
- ❌ **Rotación** — el escudo siempre en posición vertical, nunca inclinado
- ❌ **Transparencias sobre el escudo** — aplicar opacidad al escudo completo está prohibido
- ❌ **Modificar la forma** — nunca recortar, deformar, estirar o cambiar la silueta del escudo
- ❌ **Efectos no autorizados** — sin sombras externas, gradientes o filtros sobre el escudo

### Espacio de respeto
- Mínimo: `= ancho de la franja roja "ATLETICO"` alrededor del escudo completo
- Nunca yuxtaponer el escudo contra texto u otros logos sin espacio de separación
- En aplicaciones pequeñas (favicon, avatar): usar escudo completo a mínimo 32×32px

---

## 5. COMPONENTES UI

### Botón primario (acción principal)
```css
.btn-primary {
  background: var(--cam-red);
  color: var(--cam-white);
  font-family: var(--cam-font-headline);
  font-size: 14px;
  letter-spacing: 0.10em;
  text-transform: uppercase;
  border: none;
  border-radius: 4px;
  padding: 12px 28px;
  cursor: pointer;
  transition: background 200ms ease;
}
.btn-primary:hover  { background: #FF2040; }
.btn-primary:active { background: #CC0A27; }
```

### Botón secundario / dorado
```css
.btn-gold {
  background: var(--cam-yellow);
  color: var(--cam-navy);
  font-family: var(--cam-font-headline);
  font-size: 14px;
  letter-spacing: 0.10em;
  text-transform: uppercase;
  border: none;
  border-radius: 4px;
  padding: 12px 28px;
  cursor: pointer;
  transition: background 200ms ease;
}
.btn-gold:hover { background: #FFE033; }
```

### Botón ghost / contorno
```css
.btn-ghost {
  background: transparent;
  color: var(--cam-white);
  border: 1.5px solid rgba(255,255,255,0.35);
  border-radius: 4px;
  padding: 10px 24px;
  font-family: var(--cam-font-headline);
  letter-spacing: 0.10em;
  text-transform: uppercase;
  transition: all 200ms ease;
}
.btn-ghost:hover {
  border-color: var(--cam-red);
  color: var(--cam-red);
}
/* Versión sobre fondo claro */
.btn-ghost-dark {
  color: var(--cam-navy);
  border-color: rgba(14,29,49,0.35);
}
.btn-ghost-dark:hover {
  border-color: var(--cam-red);
  color: var(--cam-red);
}
```

### Card / tarjeta (sobre fondo navy)
```css
.card {
  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.10);
  border-radius: 8px;
  padding: 24px;
  position: relative;
}
/* Acento superior rojo */
.card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 3px;
  background: var(--cam-red);
  border-radius: 8px 8px 0 0;
}
/* Card sobre fondo claro */
.card-light {
  background: var(--cam-white);
  border: 1px solid var(--cam-gray-3);
  border-radius: 8px;
  padding: 24px;
  box-shadow: 0 2px 10px rgba(14,29,49,0.08);
}
.card-light::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 3px;
  background: var(--cam-red);
  border-radius: 8px 8px 0 0;
}
/* Título de card */
.card-title {
  font-family: var(--cam-font-headline);
  font-size: 13px;
  text-transform: uppercase;
  letter-spacing: 0.14em;
  color: var(--cam-yellow);
  margin-bottom: 16px;
}
```

### Input / campo de formulario
```css
.input {
  width: 100%;
  padding: 10px 14px;
  border: 1.5px solid rgba(255,255,255,0.20);
  border-radius: 4px;
  font-family: var(--cam-font-body);
  font-size: 14px;
  color: var(--cam-white);
  background: rgba(255,255,255,0.06);
  transition: border-color 200ms;
}
.input:focus {
  outline: none;
  border-color: var(--cam-red);
  box-shadow: 0 0 0 3px rgba(238,14,47,0.15);
}
.input::placeholder { color: rgba(255,255,255,0.30); }
```

### Badge / píldora de estado
```css
/* Rojo — activo, urgente, destacado */
.badge-red {
  background: rgba(238,14,47,0.15);
  color: var(--cam-red);
  border: 1px solid rgba(238,14,47,0.30);
  border-radius: 4px;
  padding: 4px 10px;
  font-family: var(--cam-font-headline);
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.12em;
}
/* Amarillo — información, destacado especial */
.badge-yellow {
  background: rgba(244,215,34,0.15);
  color: var(--cam-yellow);
  border: 1px solid rgba(244,215,34,0.30);
  border-radius: 4px;
  padding: 4px 10px;
  font-family: var(--cam-font-headline);
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.12em;
}
/* Neutro — inactivo, secundario */
.badge-neutral {
  background: rgba(255,255,255,0.06);
  color: rgba(255,255,255,0.45);
  border: 1px solid rgba(255,255,255,0.10);
  border-radius: 4px;
  padding: 4px 10px;
  font-family: var(--cam-font-headline);
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.12em;
}
```

### Marcador / Score display
```css
.score-display {
  display: flex;
  align-items: center;
  gap: 12px;
  font-family: var(--cam-font-mono);
  font-size: 48px;
  font-weight: 700;
  color: var(--cam-white);
  letter-spacing: -0.02em;
  font-variant-numeric: tabular-nums;
}
.score-divider {
  color: var(--cam-red);
  font-size: 40px;
}
.score-team {
  font-family: var(--cam-font-headline);
  font-size: 13px;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  color: var(--cam-yellow);
}
```

---

## 6. TABLAS

```css
/* Tabla de estadísticas / reportes Club Atlético de Morelia */
.cam-table {
  width: 100%;
  border-collapse: collapse;
  font-family: var(--cam-font-body);
  font-size: 13px;
}
/* Línea de acento superior roja */
.cam-table-wrap {
  border-top: 3px solid var(--cam-red);
}
/* Encabezados */
.cam-table thead th {
  font-family: var(--cam-font-headline);
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.16em;
  color: var(--cam-yellow);
  padding: 10px 14px;
  border-bottom: 1px solid rgba(244,215,34,0.20);
  text-align: left;
  background: var(--cam-navy);
}
/* Filas */
.cam-table tbody tr {
  border-bottom: 1px solid rgba(255,255,255,0.06);
}
.cam-table tbody tr:nth-child(even) {
  background: rgba(255,255,255,0.02);
}
.cam-table tbody tr:hover {
  background: rgba(238,14,47,0.06);
}
.cam-table tbody td {
  padding: 10px 14px;
  color: var(--cam-white);
  vertical-align: middle;
}
/* Cifras numéricas */
.cam-table .num {
  font-family: var(--cam-font-mono);
  font-variant-numeric: tabular-nums;
  text-align: right;
  letter-spacing: -0.02em;
}
/* Nombre del jugador — destacado */
.cam-table .player-name {
  font-family: var(--cam-font-headline);
  font-size: 13px;
  letter-spacing: 0.04em;
  text-transform: uppercase;
}

/* Versión clara (documentos internos / PDF) */
.cam-table-light thead th {
  color: var(--cam-navy);
  background: var(--cam-off-white);
  border-bottom: 1px solid rgba(14,29,49,0.15);
}
.cam-table-light {
  border-top: 3px solid var(--cam-red);
}
.cam-table-light tbody td { color: var(--cam-navy); }
.cam-table-light tbody tr:nth-child(even) {
  background: rgba(14,29,49,0.04);
}
.cam-table-light tbody tr:hover {
  background: rgba(238,14,47,0.05);
}
```

---

## 7. EMAIL HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Club Atlético de Morelia</title>
  <style>
    body {
      margin: 0; padding: 0;
      background: #F2F4F6;
      font-family: 'Open Sans', 'Helvetica Neue', Arial, sans-serif;
    }
    .wrapper { max-width: 600px; margin: 0 auto; background: #FFFFFF; }

    /* Header navy con banda roja */
    .email-header {
      background: #0E1D31;
      padding: 20px 32px;
      display: flex; align-items: center; gap: 16px;
    }
    .email-logo-box {
      width: 48px; height: 48px;
      flex-shrink: 0;
    }
    .email-brand strong {
      display: block;
      font-family: 'Anton', Impact, sans-serif;
      font-size: 20px; font-weight: 400;
      letter-spacing: 0.04em; text-transform: uppercase;
      color: #FFFFFF;
    }
    .email-brand small {
      font-size: 10px; color: #F4D722;
      text-transform: uppercase; letter-spacing: 0.16em;
    }

    /* Banda roja de acento */
    .email-accent-bar { height: 4px; background: #EE0E2F; }

    /* Sección */
    .email-section {
      background: #FFFFFF;
      padding: 32px 40px;
      border-bottom: 1px solid #E0E6EC;
    }
    .email-section-label {
      font-family: 'Anton', Impact, sans-serif;
      font-size: 11px; font-weight: 400;
      text-transform: uppercase; letter-spacing: 0.18em;
      color: #EE0E2F; margin-bottom: 12px;
    }
    .email-body {
      font-size: 14px; color: #0E1D31; line-height: 1.7;
    }

    /* KPI / Estadística grande */
    .kpi-value {
      font-family: 'JetBrains Mono', 'Courier New', monospace;
      font-size: 48px; font-weight: 700;
      color: #0E1D31; letter-spacing: -0.02em;
    }
    .kpi-label {
      font-size: 12px; color: #8A9AAA; margin-top: 4px;
      text-transform: uppercase; letter-spacing: 0.10em;
    }

    /* CTA Rojo */
    .email-cta {
      display: inline-block;
      background: #EE0E2F; color: #FFFFFF;
      font-family: 'Anton', Impact, sans-serif;
      font-weight: 400; font-size: 14px;
      letter-spacing: 0.10em; text-transform: uppercase;
      text-decoration: none;
      padding: 14px 32px; border-radius: 4px;
      margin-top: 20px;
    }

    /* Footer */
    .email-footer {
      background: #0E1D31; padding: 20px 40px;
      text-align: center;
      font-size: 11px; color: rgba(255,255,255,0.35);
      letter-spacing: 0.08em;
    }
    .email-footer a { color: #F4D722; text-decoration: none; }
  </style>
</head>
<body>
  <div class="wrapper">
    <div class="email-header">
      <div class="email-logo-box">
        <img src="cid:escudo" alt="CAM" width="48">
      </div>
      <div class="email-brand">
        <strong>Atlético de Morelia</strong>
        <small>Club · Morelia, Michoacán</small>
      </div>
    </div>
    <div class="email-accent-bar"></div>

    <div class="email-section">
      <div class="email-section-label">Nombre de sección</div>
      <!-- contenido -->
    </div>

    <div class="email-footer">
      Club Atlético de Morelia · atleticomorelia.com.mx · Confidencial
    </div>
  </div>
</body>
</html>
```

---

## 8. USO DE TRANSPARENCIAS Y CONTORNOS

### Transparencias (recurso gráfico oficial)
El manual documenta el uso de `#0E1D31` en diferentes opacidades como técnica de diseño para fotografías, secciones hero y fondos de comunicación.

```css
/* Overlay sobre fotografía — uso estándar */
.photo-overlay {
  background: linear-gradient(
    to bottom,
    rgba(14,29,49,0.40) 0%,
    rgba(14,29,49,0.85) 100%
  );
}

/* Hero section con imagen de fondo */
.hero {
  position: relative;
  min-height: 60vh;
  display: flex;
  align-items: center;
}
.hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background: rgba(14,29,49,0.65);
}

/* Card con fondo fotográfico */
.card-photo {
  background: rgba(14,29,49,0.90);
  backdrop-filter: blur(2px);
}
```

### Contornos (recurso gráfico oficial)
El manual documenta el uso de contornos blancos alrededor de elementos recortados (jugadores, figuras) para destacarlos sobre fondos navy o fotográficos.

```css
/* Contorno blanco para figuras recortadas */
.cutout-figure {
  filter: drop-shadow(0 0 0 3px #FFFFFF)
          drop-shadow(0 0 0 6px rgba(14,29,49,0.50));
}
/* O via outline en SVG/canvas: stroke: #FFFFFF; stroke-width: 6px */

/* Contorno rojo para elementos de acción */
.cutout-accent {
  filter: drop-shadow(0 0 0 3px #EE0E2F);
}
```

---

## 9. PDF / PRINT

### Notas de impresión
Los colores del Club Atlético de Morelia están definidos en Pantone para garantizar consistencia en impresión:
- **Azul Oscuro:** Pantone 296 C — verificar conversión CMYK con imprenta (71, 41, 0, 81)
- **Rojo:** Pantone 185 C — rojo vivo, alta saturación (0, 94, 80, 7)
- **Amarillo:** Pantone 109 C — amarillo cálido, alta luminosidad (0, 12, 86, 4)

### Variables para impresión
```css
@media print {
  body { background: #FFFFFF; color: #0E1D31; }
  * { box-shadow: none !important; transition: none !important; }

  .cam-accent { color: #EE0E2F; }
  .cam-accent-gold { color: #F4D722; }

  /* Encabezado de página PDF */
  .pdf-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 4px solid #EE0E2F;
    padding-bottom: 16px;
    margin-bottom: 24px;
  }
  .pdf-footer {
    position: fixed;
    bottom: 0; left: 0; right: 0;
    border-top: 1px solid #D0D8E0;
    padding: 8px 40px;
    font-size: 10px; color: #8A9AAA;
    display: flex; justify-content: space-between;
    background: #FFFFFF;
  }

  .page-break { page-break-before: always; }
  .no-break   { page-break-inside: avoid; }
}
```

### Márgenes de página recomendados
- Carta/A4: `margin: 20mm 25mm`
- Header fijo: escudo CAM izquierda + nombre del documento / fecha derecha
- Footer fijo: `Club Atlético de Morelia · Confidencial · Página X de Y`
- Línea divisoria encabezado: `#EE0E2F` 3–4pt (rojo)
- Fondo de secciones alternativas: `rgba(14,29,49,0.05)` (navy muy tenue)

---

## 10. MODO OSCURO / CLARO

El **modo oscuro navy es el modo por defecto** de la marca — el fondo `#0E1D31` es la identidad primaria del club en digital.

```css
/* Default: modo oscuro navy */
:root {
  --cam-bg:       #0E1D31;
  --cam-bg-card:  rgba(255,255,255,0.05);
  --cam-text:     #FFFFFF;
  --cam-text-2:   rgba(255,255,255,0.60);
  --cam-text-3:   rgba(255,255,255,0.30);
  --cam-border:   rgba(255,255,255,0.10);
  --cam-accent:   #EE0E2F;
  --cam-accent-2: #F4D722;
}

/* Modo claro (documentos administrativos / reportes) */
body[data-mode="light"] {
  --cam-bg:       #F2F4F6;
  --cam-bg-card:  #FFFFFF;
  --cam-text:     #0E1D31;
  --cam-text-2:   #2A3A4A;
  --cam-text-3:   #8A9AAA;
  --cam-border:   #D0D8E0;
  --cam-accent:   #EE0E2F;
  --cam-accent-2: #C49A00; /* amarillo oscurecido para legibilidad sobre fondo claro */
}
```

**Reglas de color:**
- `#EE0E2F` (rojo) funciona igual en ambos modos — siempre es el acento primario
- `#F4D722` (amarillo) tiene buen contraste sobre navy — en modo claro usar versión oscurecida `#C49A00` para textos
- `#0E1D31` (navy) nunca cambia — es la identidad del club en ambos modos (fondo o texto)

---

## 11. APLICACIONES DE MARCA

### Merchandising y uniformes
Según el manual oficial:
- **Uniformes:** Fondo navy `#0E1D31` como color principal, banda en rojo `#EE0E2F`, número/nombre en amarillo `#F4D722`
- **Gorras:** Disponibles en navy, rojo y blanco — escudo completo bordado en variante apropiada
- **Uniformes negros (alternativa):** Escudo en sus colores completos sobre fondo negro
- **Artículos:** Botellas, llaveros, playeras — escudo completo en navy o rojo

### Fotografía editorial
- Usar overlays de `#0E1D31` en diferentes opacidades sobre fotografías de acción
- Contornos blancos alrededor de jugadores recortados para composiciones dinámicas
- Fotografías de cancha y jugadores en uniforme como backdrop de piezas de comunicación

---

## 12. REGLAS DE ORO (resumen ejecutivo para IA/agentes)

1. **Navy `#0E1D31`** — identidad primaria. Fondo default en digital, fondo de uniformes, headers de reporte.
2. **Rojo `#EE0E2F`** — acento de acción y pasión. Va en: botones primarios, eyebrows, barras de acento, CTAs, línea superior de tablas. Funciona igual en ambos modos.
3. **Amarillo `#F4D722`** — acento de detalle y distinción. Va en: texto "CLUB" y "MORELIA" del escudo, estrellas, eyebrows sobre navy, detalles premium, badges de distinción.
4. **Blanco `#FFFFFF`** — texto principal sobre navy y rojo. Nunca usar blanco sobre amarillo.
5. **Anton** — solo para el nombre del club en display y piezas de alto impacto. Nunca en párrafos.
6. **Bebas Neue** — titulares, secciones, labels. Siempre en uppercase.
7. **Open Sauce One / Open Sans** — todo el texto corrido, descripciones, formularios.
8. **El escudo es SIEMPRE en sus colores oficiales** — nunca monocromático, nunca con opacidad, nunca rotado.
9. **Tablas** — `border-top: 3px solid #EE0E2F`, encabezados en Bebas Neue uppercase dorado.
10. **Estadísticas / marcadores** — siempre en fuente monoespaciada (`JetBrains Mono` o equivalente).
11. **Overlays fotográficos** — usar `#0E1D31` en diferentes opacidades (40%–90%) — nunca opacidad en el escudo.
12. **Amarillo en modo claro** — cambiar a versión oscurecida `#C49A00` cuando el fondo sea claro.
13. **No mezclar** más de 2 familias tipográficas en una misma pieza.
14. **Pantones para print** — siempre especificar 296 C (navy), 185 C (rojo), 109 C (amarillo) en archivos de producción.

---

## 13. RUTAS DE ASSETS

```
club-atletico-morelia/
├── 01_LOGO/
│   ├── ATLETICO_CLUB-MORELIA_LOGO.png   ← escudo completo (PNG, fondo negro)
│   └── ATLETICO_CLUB-MORELIA_LOGO.ai    ← archivo fuente Illustrator (editable, vectorial)
│
├── 02_TIPOGRAFIA/
│   ├── Anton                            ← Google Fonts: fonts.google.com/specimen/Anton
│   ├── Bebas Neue                       ← Google Fonts: fonts.google.com/specimen/Bebas+Neue
│   ├── Open Sauce One                   ← GitHub: github.com/marcologous/Open-Sauce-Fonts
│   └── Open Sans                        ← Google Fonts: fonts.google.com/specimen/Open+Sans
│
├── 03_PALETA DE COLORES/
│   ├── 0E1D31  ← Azul Oscuro / Navy (primario)    Pantone 296 C
│   ├── EE0E2F  ← Rojo (acento)                    Pantone 185 C
│   ├── F4D722  ← Amarillo / Dorado (detalle)       Pantone 109 C
│   ├── FFFFFF  ← Blanco (texto negativo)            Pantone White
│   └── 000000  ← Negro (contornos del escudo)       Pantone Black C
│
└── 04_BRANDBOOK/
    └── MANUAL_DE_IDENTIDAD_-_CLUB_ATLETICO_DE_MORELIA.pdf  ← Manual oficial
```

---

## 14. POSICIÓN DENTRO DEL ECOSISTEMA GO

> Este archivo (`canchas.md`) documenta la identidad visual del **Club Atlético de Morelia** — proyecto Canchas dentro del ecosistema de Grupo Ortiz. El sistema gráfico del club opera de forma **independiente** de la identidad GO, con su propia paleta, tipografía y lenguaje visual deportivo.

| Elemento | Sistema GO | Club Atlético de Morelia |
|----------|-----------|--------------------------|
| Color de acento | Naranja `#FB670B` | Rojo `#EE0E2F` + Amarillo `#F4D722` |
| Fuente principal | Blauer Nue (redondeada) | Anton (condensada, bold) |
| Fuente de display | Morganite Pro | Bebas Neue Cyrillic |
| Fondo default | Blanco / Crema | Navy `#0E1D31` |
| Personalidad | Cálido, orgánico, empresarial | Intenso, deportivo, apasionado |
| Sector | Industrial / Corporativo | Fútbol / Academia deportiva |

### Regla de carga para agentes e IA

```
Proyecto Club Atlético          → context_design.md  +  canchas.md
Duda sobre coherencia con GO    → brand_system.md §2 (Árbol de decisión)
Conflicto de color entre marcas → brand_system.md §4 (Tabla de conflictos)
```

---

*Última actualización: 2026-05-31 · Basado en MANUAL_DE_IDENTIDAD_-_CLUB_ATLETICO_DE_MORELIA.pdf y assets oficiales del club*
