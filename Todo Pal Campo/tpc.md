# Todo Pal Campo® — Design System Context
> Fuente de verdad para todos los proyectos digitales e impresos de la marca. Aplica a: web apps, redes sociales, catálogos, reportes HTML, PDFs, emails, señalética, publicidad y cualquier pieza de comunicación de Todo Pal Campo®.

---

## 1. IDENTIDAD DE MARCA

**Marca:** Todo Pal Campo®  
**Abreviatura oficial:** TPC  
**Registro:** Marca registrada (símbolo ® aparece siempre junto al nombre en el logotipo)  
**Slogan:** *Donde el campo encuentra soluciones*  
**Símbolo / Isotipo:** Tractor agrícola de perfil — icono flat, sin outline, con detalles interiores de línea (ventana, parrilla, ejes de rueda)  
**Sector:** Agro / Campo / Insumos agropecuarios / Soluciones rurales  
**Tipografía del nombre:** Fuse Black (display, encabezados)  
**Tipografía de cuerpo:** Outfit Regular / Variable  
**Color primario:** Verde Campo `#236D2D`  
**Color de acento:** Amarillo TPC `#FFD72E`  
**Color de soporte:** Carbón `#282828`

---

## 2. PALETA DE COLORES OFICIAL

### Colores corporativos (del manual oficial)
| Nombre | Hex | RGB | CMYK | Uso |
|--------|-----|-----|------|-----|
| Amarillo TPC | `#FFD72E` | 255, 215, 46 | 1, 14, 86, 0 | Acento principal — tractor sobre verde, CTAs, highlights, bandas de comunicación |
| Verde Campo | `#236D2D` | 35, 109, 45 | 85, 32, 100, 22 | Color de fondo primario, fondos de sección, fondo del isotipo en redes |
| Carbón TPC | `#282828` | 40, 40, 40 | 72, 63, 58, 73 | Texto principal en fondos claros, versión monocromática del logo, fondos de contraste |

### Neutros complementarios
| Nombre | Hex | Uso |
|--------|-----|-----|
| Blanco | `#FFFFFF` | Texto sobre verde/carbón, fondos de documentos, logo versión negativa |
| Off-white / Crema | `#F8F7F2` | Fondo cálido de reportes y documentos, fondo de email |
| Verde oscuro | `#1A5222` | Hover/pressed del verde, fondos de secciones más oscuras |
| Verde claro | `#2D8A39` | Gradientes, hover |
| Amarillo suave | `#FFF0A0` | Tint del amarillo para fondos muy claros |

### Tokens CSS recomendados
```css
:root {
  /* Colores de marca */
  --tpc-yellow:       #FFD72E;
  --tpc-yellow-hot:   #FFE55A;       /* hover */
  --tpc-yellow-deep:  #E0BB00;       /* pressed / texto sobre fondo claro */
  --tpc-yellow-tint:  rgba(255,215,46,0.15);

  --tpc-green:        #236D2D;
  --tpc-green-dark:   #1A5222;       /* hover, pressed */
  --tpc-green-light:  #2D8A39;       /* gradiente, variante */
  --tpc-green-tint:   rgba(35,109,45,0.10);

  --tpc-charcoal:     #282828;
  --tpc-charcoal-2:   #3D3D3D;       /* texto secundario oscuro */

  /* Neutros */
  --tpc-white:        #FFFFFF;
  --tpc-off-white:    #F8F7F2;
  --tpc-gray-1:       #888888;       /* texto secundario, bordes */
  --tpc-gray-2:       #D0D0D0;       /* separadores, fondos de tabla */

  /* Semánticos */
  --tpc-bg:           var(--tpc-green);
  --tpc-bg-light:     var(--tpc-off-white);
  --tpc-text:         var(--tpc-white);          /* sobre verde */
  --tpc-text-dark:    var(--tpc-charcoal);       /* sobre claro */
  --tpc-text-2:       var(--tpc-gray-1);
  --tpc-accent:       var(--tpc-yellow);
  --tpc-border:       rgba(255,255,255,0.15);
}
```

### Modo de uso por contexto
| Contexto | Fondo | Texto | Isotipo / Acento |
|----------|-------|-------|-----------------|
| Social media (default) | Verde `#236D2D` | Blanco / `#FFD72E` | Amarillo `#FFD72E` |
| Web / digital | Verde `#236D2D` o Carbón `#282828` | Blanco | Amarillo `#FFD72E` |
| Catálogos / publicidad impresa | Verde `#236D2D` | Blanco / amarillo | Amarillo sobre verde |
| Documentos / reportes claros | Blanco / `#F8F7F2` | Carbón `#282828` | Verde `#236D2D` |
| Email corporativo | Blanco `#FFFFFF` | Carbón `#282828` | Verde `#236D2D` / Amarillo |
| Variante negra (merch, impresión) | Negro / `#282828` | Blanco o amarillo | Amarillo `#FFD72E` |

### Nota sobre el uso del amarillo
El amarillo `#FFD72E` es el acento de energía — sobre verde genera el contraste identitario de la marca. Sobre fondos blancos/claros el amarillo puro tiene poco contraste para texto: en esos casos usar el verde `#236D2D` como color tipográfico o el amarillo oscurecido `#E0BB00` para acentos pequeños.

---

## 3. TIPOGRAFÍA

### Fuentes oficiales TPC
Ambas fuentes están disponibles como archivos subidos a los assets de la marca.

| Fuente | Archivo | Rol | Características |
|--------|---------|-----|-----------------|
| **Fuse Black** | `fonnts_com-fuse-black.otf` | **ENCABEZADOS, display, nombre de marca** | Sans-serif ultra-bold, geométrica, condensada. Alta presencia visual. Usada en "TODO PAL CAMPO" en la portada y piezas de impacto |
| **Fuse Bold** | `fonnts_com-fuse-bold.otf` | **Subtítulos de impacto, CTAs, labels** | Versión bold de Fuse — peso intermedio entre Black y Regular |
| **Outfit Regular** | `Outfit-Regular.ttf` | **Cuerpo de texto, descripciones, UI** | Sans-serif geométrica, moderna, altamente legible en tamaños pequeños |
| **Outfit Variable** | `Outfit-VariableFont_wght.ttf` | **Fuente variable — todos los pesos** | Permite usar cualquier peso (100–900) con un solo archivo. Recomendada para web |

### Fallbacks seguros
```css
--tpc-font-display:  'Fuse', 'Impact', 'Arial Black', 'Helvetica Neue', sans-serif;
--tpc-font-headline: 'Fuse Bold', 'Outfit', 'Inter', sans-serif;
--tpc-font-body:     'Outfit', 'Inter', 'DM Sans', 'Helvetica Neue', system-ui, sans-serif;
--tpc-font-mono:     'JetBrains Mono', 'Fira Code', Consolas, monospace;
```

### Carga de fuentes en web (variable preferida)
```css
@font-face {
  font-family: 'Fuse';
  src: url('/fonts/fonnts_com-fuse-black.otf') format('opentype');
  font-weight: 900;
  font-style: normal;
}
@font-face {
  font-family: 'Fuse';
  src: url('/fonts/fonnts_com-fuse-bold.otf') format('opentype');
  font-weight: 700;
  font-style: normal;
}
@font-face {
  font-family: 'Outfit';
  src: url('/fonts/Outfit-VariableFont_wght.ttf') format('truetype');
  font-weight: 100 900;
  font-style: normal;
}
```

### Escala tipográfica
| Nivel | Fuente | Tamaño | Peso | Uso |
|-------|--------|--------|------|-----|
| Display XL | Fuse Black | 72–96px | 900 | Portadas, hero sections, nombre en grande |
| H1 | Fuse Black | 48–64px | 900 | Títulos principales de página |
| H2 | Fuse Bold | 32–40px | 700 | Títulos de sección |
| H3 | Outfit | 22–28px | 700 | Subtítulos, encabezados de módulo |
| H4 | Outfit | 18–20px | 600 | Encabezados de tarjeta, labels fuertes |
| Slogan | Outfit | 14–18px | 400 | "Donde el campo encuentra soluciones" — siempre Regular |
| Body | Outfit | 14–16px | 400 | Texto corrido, descripciones, párrafos |
| Body Small | Outfit | 12–13px | 400 | Notas, pies de página, metadatos |
| Label / Eyebrow | Fuse Bold | 10–12px | 700 | Etiquetas uppercase + letter-spacing |
| Mono | JetBrains Mono | 12–13px | 400 | Precios, códigos, cifras clave |

### Reglas tipográficas
- **Fuse Black** — SOLO para titulares y display. Nunca en cuerpo de texto largo.
- **Nombre de marca** en comunicación impacto: "TODO PAL CAMPO" en Fuse Black uppercase, con "PAL" en amarillo y el resto en blanco o verde según el fondo (ver banner de portada).
- **Slogan** — "Donde el campo encuentra soluciones" siempre en Outfit Regular, nunca en Fuse.
- **Símbolo ®** — siempre presente junto al nombre en el logotipo, en superíndice.
- **Eyebrow / label:** `font-family: 'Fuse', ...; font-weight: 700; font-size: 11px; text-transform: uppercase; letter-spacing: 0.14em; color: var(--tpc-yellow)`
- Nunca mezclar más de 2 familias en una misma pieza.
- Outfit Variable permite ajustar el peso fluidamente en web — preferir sobre archivos estáticos.

---

## 4. LOGO — VARIANTES Y USO

### Anatomía del logo
```
ISOTIPO       = Tractor agrícola de perfil (flat, sin stroke exterior, detalles internos de línea)
LOGOTIPO      = "Todo Pal Campo®" (Fuse Black, Title Case)
LOGO COMPLETO = ISOTIPO centrado arriba + LOGOTIPO debajo
```

### Descripción del isotipo
Tractor agrícola visto desde el costado izquierdo. Estilo flat (sin sombras ni gradientes), con detalles internos representados por líneas finas: marco de ventana con limpiaparabrisas, parrilla lateral, línea de carrocería, ejes y pernos de las ruedas. Las ruedas tienen perfil dentado (neumático de campo). El tractor mira hacia la derecha.

### Variantes de logo disponibles
| Archivo | Isotipo | Texto | Fondo | Usar sobre |
|---------|---------|-------|-------|------------|
| `Todo_Pal_Campo.png` | Amarillo `#FFD72E` | Amarillo `#FFD72E` | Verde `#236D2D` | Fondo verde (uso principal en redes) |
| `IMG_3373.png` | Verde `#236D2D` | Blanco | Negro | Fondos oscuros / negros |
| `IMG_3377.png` | Blanco | Blanco | Negro | Fondos oscuros — versión negativa blanca |
| `IMG_3406.png` | Verde `#236D2D` | Verde `#236D2D` | Negro | Monocromático verde sobre oscuro |
| `IMG_3407.png` | Carbón `#282828` | Carbón `#282828` | Negro | Monocromático gris oscuro (versión neutra) |
| `IMG_3657.png` | Amarillo `#FFD72E` | Blanco | Negro | Fondos oscuros — isotipo amarillo + texto blanco |
| `IMG_3658.png` | Amarillo `#FFD72E` | Amarillo `#FFD72E` | Negro | Fondos oscuros — versión todo amarillo |
| `Portada__TPC.png` | — | Fuse Black, "PAL" en amarillo | — | Banner redes / portada |

### Variantes de color del isotipo según contexto
| Contexto | Isotipo | Texto | Fondo |
|----------|---------|-------|-------|
| Social media / digital (default) | Amarillo `#FFD72E` | Amarillo `#FFD72E` | Verde `#236D2D` |
| Sobre fondo negro / oscuro | Amarillo o Verde o Blanco | Blanco o Amarillo | Negro / Carbón |
| Sobre fondo blanco / claro | Verde `#236D2D` | Verde `#236D2D` o Carbón | Blanco |
| Monocromático para impresión | Carbón `#282828` | Carbón `#282828` | Blanco |
| Bordado / grabado | Blanco o Amarillo | Blanco | Tela verde o carbón |

### Espacio de respeto
- Mínimo: `= altura de la letra "T" de "Todo"` alrededor del logo completo
- El símbolo ® nunca se omite cuando aparece el nombre de la marca
- El logo siempre en posición vertical (isotipo arriba, texto abajo) — salvo versiones horizontales específicas de aplicación

---

## 5. ESTILO GRÁFICO

El manual define el estilo gráfico de TPC como **publicidad agro de alto impacto**, caracterizado por:

- **Fotografía de campo** como fondo: cultivos, tractores en acción, agricultores, cosechas
- **Overlays de color sólido** (amarillo o verde) en forma de bandas diagonales o franjas geométricas que irrumpen sobre la fotografía
- **Tipografía de impacto** (Fuse Black) para precios y nombres de producto en grande
- **Productos protagonistas** en primer plano recortados sobre fondo verde o fotográfico
- **Composición limpia**: máximo 3 bloques de información — titular, producto, CTA/precio

### Composición del banner de comunicación (referencia Portada_TPC)
```
┌─────────────────────────────────────────────────────┐
│  BANDA AMARILLA DIAGONAL   │  FOTOGRAFÍA DE CAMPO   │
│  (izquierda)               │  con overlay verde     │
│                            │                        │
│                            │  TODO  PAL  CAMPO      │
│                            │  Donde el campo        │
│                            │  encuentra soluciones  │
│                            │  [íconos de sector]    │
└─────────────────────────────────────────────────────┘
```

### Íconos de sector (del banner oficial)
Los 4 íconos que representan los rubros de TPC:
1. 🌱 Plántula / semilla (agronomía, siembra)
2. 📦 Empaque / insumos (productos agro)
3. 🍽 Agro-alimentación / herramientas de campo
4. 🚜 Tractor / maquinaria agrícola

---

## 6. COMPONENTES UI

### Botón primario (CTA amarillo)
```css
.btn-primary {
  background: var(--tpc-yellow);
  color: var(--tpc-charcoal);
  font-family: var(--tpc-font-display);
  font-weight: 900;
  font-size: 14px;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  border: none;
  border-radius: 6px;
  padding: 12px 28px;
  cursor: pointer;
  transition: background 200ms ease;
}
.btn-primary:hover  { background: #FFE55A; }
.btn-primary:active { background: #E0BB00; }
```

### Botón secundario / verde
```css
.btn-green {
  background: var(--tpc-green);
  color: var(--tpc-white);
  font-family: var(--tpc-font-display);
  font-weight: 700;
  font-size: 14px;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  border: none;
  border-radius: 6px;
  padding: 12px 28px;
  cursor: pointer;
  transition: background 200ms ease;
}
.btn-green:hover  { background: #1A5222; }
.btn-green:active { background: #154019; }
```

### Botón ghost / contorno
```css
.btn-ghost {
  background: transparent;
  color: var(--tpc-white);
  border: 2px solid rgba(255,255,255,0.40);
  border-radius: 6px;
  padding: 10px 24px;
  font-family: var(--tpc-font-headline);
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  transition: all 200ms ease;
}
.btn-ghost:hover {
  border-color: var(--tpc-yellow);
  color: var(--tpc-yellow);
}
/* Versión sobre fondo claro */
.btn-ghost-dark {
  color: var(--tpc-green);
  border-color: rgba(35,109,45,0.35);
}
.btn-ghost-dark:hover {
  border-color: var(--tpc-green);
  background: var(--tpc-green-tint);
}
```

### Card / tarjeta (sobre verde)
```css
.card {
  background: rgba(255,255,255,0.06);
  border: 1px solid rgba(255,255,255,0.12);
  border-radius: 10px;
  padding: 24px;
  position: relative;
}
/* Acento superior amarillo */
.card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 3px;
  background: var(--tpc-yellow);
  border-radius: 10px 10px 0 0;
}
/* Card sobre fondo claro */
.card-light {
  background: var(--tpc-white);
  border: 1px solid var(--tpc-gray-2);
  border-radius: 10px;
  padding: 24px;
  box-shadow: 0 2px 8px rgba(35,109,45,0.08);
}
.card-light::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 3px;
  background: var(--tpc-green);
  border-radius: 10px 10px 0 0;
}
/* Título de card */
.card-title {
  font-family: var(--tpc-font-display);
  font-weight: 900;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.14em;
  color: var(--tpc-yellow);
  margin-bottom: 12px;
}
```

### Tarjeta de producto (e-commerce / catálogo)
```css
.product-card {
  background: var(--tpc-white);
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 16px rgba(35,109,45,0.12);
  transition: transform 200ms, box-shadow 200ms;
}
.product-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(35,109,45,0.18);
}
.product-card-img {
  background: var(--tpc-off-white);
  aspect-ratio: 1;
  display: flex;
  align-items: center;
  justify-content: center;
}
.product-card-body { padding: 16px; }
.product-card-category {
  font-family: var(--tpc-font-display);
  font-size: 10px; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.14em;
  color: var(--tpc-green);
  margin-bottom: 6px;
}
.product-card-name {
  font-family: var(--tpc-font-body);
  font-size: 15px; font-weight: 600;
  color: var(--tpc-charcoal);
  margin-bottom: 8px;
}
.product-card-price {
  font-family: var(--tpc-font-mono);
  font-size: 22px; font-weight: 700;
  color: var(--tpc-green);
  font-variant-numeric: tabular-nums;
}
```

### Input / campo de formulario
```css
.input {
  width: 100%;
  padding: 10px 14px;
  border: 1.5px solid rgba(255,255,255,0.22);
  border-radius: 6px;
  font-family: var(--tpc-font-body);
  font-size: 14px;
  color: var(--tpc-white);
  background: rgba(255,255,255,0.07);
  transition: border-color 200ms;
}
.input:focus {
  outline: none;
  border-color: var(--tpc-yellow);
  box-shadow: 0 0 0 3px rgba(255,215,46,0.15);
}
.input::placeholder { color: rgba(255,255,255,0.32); }
/* Versión sobre fondo claro */
.input-light {
  color: var(--tpc-charcoal);
  background: var(--tpc-white);
  border-color: var(--tpc-gray-2);
}
.input-light:focus {
  border-color: var(--tpc-green);
  box-shadow: 0 0 0 3px rgba(35,109,45,0.12);
}
```

### Badge / etiqueta de categoría
```css
/* Verde — categoría, activo */
.badge-green {
  background: rgba(35,109,45,0.15);
  color: var(--tpc-green-light);
  border: 1px solid rgba(35,109,45,0.30);
  border-radius: 100px;
  padding: 4px 10px;
  font-family: var(--tpc-font-display);
  font-size: 10px; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.12em;
}
/* Amarillo — oferta, destacado */
.badge-yellow {
  background: rgba(255,215,46,0.15);
  color: var(--tpc-yellow-deep);
  border: 1px solid rgba(255,215,46,0.35);
  border-radius: 100px;
  padding: 4px 10px;
  font-family: var(--tpc-font-display);
  font-size: 10px; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.12em;
}
/* Versión sólida para piezas oscuras */
.badge-yellow-solid {
  background: var(--tpc-yellow);
  color: var(--tpc-charcoal);
  border-radius: 100px;
  padding: 4px 10px;
  font-family: var(--tpc-font-display);
  font-size: 10px; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.10em;
}
```

---

## 7. TABLAS

```css
/* Tabla Todo Pal Campo */
.tpc-table {
  width: 100%;
  border-collapse: collapse;
  font-family: var(--tpc-font-body);
  font-size: 13px;
}
/* Acento superior amarillo */
.tpc-table-wrap {
  border-top: 3px solid var(--tpc-yellow);
}
/* Encabezados */
.tpc-table thead th {
  font-family: var(--tpc-font-display);
  font-weight: 700;
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 0.16em;
  color: var(--tpc-yellow);
  padding: 10px 14px;
  border-bottom: 1px solid rgba(255,215,46,0.20);
  text-align: left;
  background: var(--tpc-green);
}
/* Filas */
.tpc-table tbody tr {
  border-bottom: 1px solid rgba(255,255,255,0.07);
}
.tpc-table tbody tr:nth-child(even) {
  background: rgba(255,255,255,0.03);
}
.tpc-table tbody tr:hover {
  background: rgba(255,215,46,0.05);
}
.tpc-table tbody td {
  padding: 10px 14px;
  color: var(--tpc-white);
  vertical-align: middle;
}
/* Cifras numéricas */
.tpc-table .num {
  font-family: var(--tpc-font-mono);
  font-variant-numeric: tabular-nums;
  text-align: right;
  letter-spacing: -0.02em;
}

/* Versión clara (reportes / PDF) */
.tpc-table-light {
  border-top: 3px solid var(--tpc-green);
}
.tpc-table-light thead th {
  color: var(--tpc-white);
  background: var(--tpc-green);
  border-bottom: 1px solid rgba(35,109,45,0.20);
}
.tpc-table-light tbody td { color: var(--tpc-charcoal); }
.tpc-table-light tbody tr:nth-child(even) {
  background: rgba(35,109,45,0.04);
}
.tpc-table-light tbody tr:hover {
  background: rgba(35,109,45,0.07);
}
```

---

## 8. EMAIL HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Todo Pal Campo</title>
  <style>
    body {
      margin: 0; padding: 0;
      background: #F8F7F2;
      font-family: 'Outfit', 'Helvetica Neue', Arial, sans-serif;
    }
    .wrapper { max-width: 600px; margin: 0 auto; background: #FFFFFF; }

    /* Header verde */
    .email-header {
      background: #236D2D;
      padding: 22px 32px;
      display: flex; align-items: center; gap: 16px;
    }
    .email-logo-box { width: 50px; flex-shrink: 0; }
    .email-brand strong {
      display: block;
      font-family: 'Impact', 'Fuse', 'Arial Black', sans-serif;
      font-size: 18px; font-weight: 900;
      text-transform: uppercase; letter-spacing: 0.04em;
      color: #FFD72E;
    }
    .email-brand small {
      font-size: 11px; color: rgba(255,255,255,0.60);
      font-style: italic;
    }

    /* Banda amarilla de acento */
    .email-accent-bar { height: 4px; background: #FFD72E; }

    /* Sección */
    .email-section {
      padding: 32px 40px;
      border-bottom: 1px solid #E8E8E8;
    }
    .email-section-label {
      font-family: 'Impact', 'Arial Black', sans-serif;
      font-size: 10px; font-weight: 900;
      text-transform: uppercase; letter-spacing: 0.18em;
      color: #236D2D; margin-bottom: 10px;
    }
    .email-body {
      font-size: 14px; color: #282828; line-height: 1.7;
    }

    /* Precio / KPI */
    .kpi-value {
      font-family: 'Impact', 'Arial Black', sans-serif;
      font-size: 48px; font-weight: 900;
      color: #236D2D; letter-spacing: -0.02em;
    }
    .kpi-label {
      font-size: 12px; color: #888888; margin-top: 4px;
      text-transform: uppercase; letter-spacing: 0.10em;
    }

    /* CTA Verde */
    .email-cta {
      display: inline-block;
      background: #236D2D; color: #FFFFFF;
      font-family: 'Impact', 'Arial Black', sans-serif;
      font-size: 14px; font-weight: 900;
      letter-spacing: 0.08em; text-transform: uppercase;
      text-decoration: none;
      padding: 13px 30px; border-radius: 6px;
      margin-top: 16px;
    }
    /* CTA Amarillo alternativo */
    .email-cta-yellow {
      background: #FFD72E; color: #282828;
    }

    /* Footer */
    .email-footer {
      background: #236D2D; padding: 20px 40px;
      text-align: center;
      font-size: 11px; color: rgba(255,255,255,0.40);
      letter-spacing: 0.06em;
    }
    .email-footer a { color: #FFD72E; text-decoration: none; }
  </style>
</head>
<body>
  <div class="wrapper">
    <div class="email-header">
      <div class="email-logo-box">
        <img src="cid:logo" alt="TPC" width="50">
      </div>
      <div class="email-brand">
        <strong>Todo Pal Campo®</strong>
        <small>Donde el campo encuentra soluciones</small>
      </div>
    </div>
    <div class="email-accent-bar"></div>

    <div class="email-section">
      <div class="email-section-label">Nombre de sección</div>
      <!-- contenido -->
    </div>

    <div class="email-footer">
      Todo Pal Campo® · todopalcampo.com · Confidencial
    </div>
  </div>
</body>
</html>
```

---

## 9. PDF / PRINT

### Colores para impresión
Los colores de TPC están definidos en CMYK para garantizar consistencia:
- **Amarillo TPC:** CMYK 1, 14, 86, 0 — amarillo vivo, alta luminosidad
- **Verde Campo:** CMYK 85, 32, 100, 22 — verde profundo, orgánico
- **Carbón TPC:** CMYK 72, 63, 58, 73 — casi negro, contraste alto

### Variables CSS para impresión
```css
@media print {
  body { background: #FFFFFF; color: #282828; }
  * { box-shadow: none !important; transition: none !important; }

  .tpc-accent        { color: #236D2D; }
  .tpc-accent-yellow { color: #E0BB00; } /* amarillo oscurecido para print */

  /* Encabezado de página PDF */
  .pdf-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 3px solid #236D2D;
    padding-bottom: 16px;
    margin-bottom: 24px;
  }
  .pdf-footer {
    position: fixed;
    bottom: 0; left: 0; right: 0;
    border-top: 1px solid #D0D0D0;
    padding: 8px 40px;
    font-size: 10px; color: #888888;
    display: flex; justify-content: space-between;
    background: #FFFFFF;
  }

  .page-break { page-break-before: always; }
  .no-break   { page-break-inside: avoid; }
}
```

### Márgenes y estructura de página recomendados
- Carta/A4: `margin: 20mm 25mm`
- Header fijo: logo TPC izquierda (variante verde sobre blanco) + nombre del documento / fecha derecha
- Footer fijo: `Todo Pal Campo® · Donde el campo encuentra soluciones · Página X de Y`
- Línea divisoria encabezado: `#236D2D` (verde) 2–3pt
- Amarillo en print: usar `#E0BB00` para mayor legibilidad en papel blanco

---

## 10. MODO OSCURO / CLARO

El **modo verde es el modo por defecto** de la marca en digital. El modo claro se usa para documentos y catálogos de producto.

```css
/* Default: modo verde (identidad primaria TPC) */
:root {
  --tpc-bg:       #236D2D;
  --tpc-bg-card:  rgba(255,255,255,0.06);
  --tpc-text:     #FFFFFF;
  --tpc-text-2:   rgba(255,255,255,0.60);
  --tpc-text-3:   rgba(255,255,255,0.30);
  --tpc-border:   rgba(255,255,255,0.12);
  --tpc-accent:   #FFD72E;
}

/* Modo claro (documentos, catálogos) */
body[data-mode="light"] {
  --tpc-bg:       #F8F7F2;
  --tpc-bg-card:  #FFFFFF;
  --tpc-text:     #282828;
  --tpc-text-2:   #3D3D3D;
  --tpc-text-3:   #888888;
  --tpc-border:   #D0D0D0;
  --tpc-accent:   #236D2D;  /* verde como acento principal en modo claro */
}

/* Modo oscuro carbón (variante alternativa) */
body[data-mode="dark"] {
  --tpc-bg:       #282828;
  --tpc-bg-card:  rgba(255,255,255,0.05);
  --tpc-text:     #FFFFFF;
  --tpc-border:   rgba(255,255,255,0.10);
  --tpc-accent:   #FFD72E;  /* amarillo sigue siendo acento sobre carbón */
}
```

**Reglas de color:**
- `#FFD72E` (amarillo) es el acento de energía — máximo contraste y visibilidad sobre verde y carbón
- Sobre fondos blancos/claros el amarillo NO se usa como color de texto — cambia a verde `#236D2D`
- `#236D2D` (verde) funciona como acento en modo claro y como fondo en modo verde

---

## 11. REGLAS DE ORO (resumen ejecutivo para IA/agentes)

1. **Verde `#236D2D`** — identidad primaria. Fondo default en digital y redes, color de texto en documentos claros, línea de acento en reportes.
2. **Amarillo `#FFD72E`** — acento de energía. Va en: tractor sobre verde, CTAs principales, eyebrows, banda de acento de tablas. **Solo sobre fondos oscuros/verdes/carbón** — nunca como texto sobre blanco.
3. **Carbón `#282828`** — soporte. Texto sobre fondos claros, variante monocromática del logo, fondos alternativos.
4. **Fuse Black** — solo para titulares, nombre de marca en display y piezas de impacto visual. Nunca en párrafos.
5. **Fuse Bold** — subtítulos de impacto, CTAs, labels en display secundario.
6. **Outfit** — todo el texto corrido, UI, descripciones, formularios. Usar la versión Variable en web.
7. **Nombre en display:** "TODO PAL CAMPO" con "PAL" en amarillo, el resto en blanco (sobre verde) o en verde (sobre claro).
8. **El símbolo ®** siempre aparece junto al nombre "Todo Pal Campo" en el logotipo.
9. **El tractor siempre mira hacia la derecha** — nunca voltear horizontalmente el isotipo.
10. **Tablas digitales** — `border-top: 3px solid #FFD72E`, encabezados en Fuse uppercase amarillo.
11. **Tablas en print** — `border-top: 3px solid #236D2D`, encabezados en Fuse uppercase blanco sobre verde.
12. **Precios / cifras** — siempre en fuente monoespaciada (`JetBrains Mono` o equivalente).
13. **Estilo gráfico** — combinar fotografía de campo con bandas de color sólido (amarillo o verde) en diagonal o franja. Productos recortados en primer plano.
14. **No mezclar** más de 2 familias tipográficas en una misma pieza.
15. **Amarillo en modo claro** — cambiar a `#E0BB00` para acentos tipográficos pequeños; o cambiar a verde `#236D2D`.

---

## 12. RUTAS DE ASSETS

```
todo-pal-campo/
├── 01_LOGO/
│   ├── Todo_Pal_Campo.png        ← isotipo+texto AMARILLO sobre fondo VERDE (default redes)
│   ├── IMG_3373.png              ← isotipo+texto VERDE sobre negro
│   ├── IMG_3377.png              ← isotipo+texto BLANCO sobre negro
│   ├── IMG_3406.png              ← isotipo+texto VERDE sobre negro (sin fondo interno)
│   ├── IMG_3407.png              ← isotipo+texto CARBÓN sobre negro (monocromático neutro)
│   ├── IMG_3657.png              ← isotipo AMARILLO + texto BLANCO sobre negro
│   ├── IMG_3658.png              ← isotipo+texto AMARILLO sobre negro
│   └── Portada__TPC.png          ← banner portada / cover redes (Fuse Black, PAL en amarillo)
│
├── 02_TIPOGRAFIA/
│   ├── fonnts_com-fuse-black.otf         ← DISPLAY / ENCABEZADOS — instalar primero
│   ├── fonnts_com-fuse-bold.otf          ← Subtítulos / CTAs
│   ├── Outfit-Regular.ttf                ← CUERPO DE TEXTO
│   └── Outfit-VariableFont_wght.ttf      ← VARIABLE (recomendada para web, todos los pesos)
│
├── 03_PALETA DE COLORES/
│   ├── FFD72E  ← Amarillo TPC (acento principal)   CMYK: 1, 14, 86, 0
│   ├── 236D2D  ← Verde Campo (identidad primaria)  CMYK: 85, 32, 100, 22
│   └── 282828  ← Carbón TPC (soporte)              CMYK: 72, 63, 58, 73
│
└── 04_BRANDBOOK/
    └── Todo_Pal_Campo_-_Manual_de_identidad.pdf  ← Manual oficial
```

---

## 13. POSICIÓN DENTRO DEL ECOSISTEMA GO

> Este archivo (`tpc.md`) documenta la identidad visual de **Todo Pal Campo®** — marca del sector agropecuario dentro del ecosistema de Grupo Ortiz. Opera con identidad independiente, lenguaje visual propio y valores de campo/ruralidad.

| Elemento | Sistema GO | Todo Pal Campo® |
|----------|-----------|-----------------|
| Color primario | Naranja `#FB670B` | Verde `#236D2D` |
| Color de acento | — | Amarillo `#FFD72E` |
| Fuente principal | Blauer Nue | Fuse Black |
| Fuente de cuerpo | Conthic | Outfit |
| Fondo default | Blanco / Crema | Verde `#236D2D` |
| Personalidad | Corporativo, moderno | Cercano, rural, vibrante |
| Sector | Industrial / Multi | Agro / Campo / Insumos |
| Símbolo | Abstracto geométrico | Tractor flat (figurativo) |

### Regla de carga para agentes e IA

```
Proyecto Todo Pal Campo          → context_design.md  +  tpc.md
Proyecto multi-marca con TPC     → context_design.md  +  brand_system.md  +  tpc.md
Duda de qué marca aplicar        → brand_system.md §2 (Árbol de decisión)
```

---

*Última actualización: 2026-06-02 · Basado en Manual_de_identidad_Todo_Pal_Campo.pdf, logos PNG y archivos de fuentes oficiales*
