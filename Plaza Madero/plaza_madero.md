# Plaza Madero — Design System Context
> Fuente de verdad para todos los proyectos internos. Aplica a: web apps, reportes HTML, PDFs, emails, tablas, presentaciones y cualquier pieza digital de Plaza Madero. Este archivo extiende el sistema base de Grupo Ortiz (`context_design.md`).

---

## 1. IDENTIDAD DE MARCA

**Empresa:** Plaza Madero  
**Abreviatura oficial:** PM  
**Tagline / Slogan:** *el epicentro de la tecnología*  
**Símbolo:** Dos flechas convergentes que forman una cruz diagonal — representan el encuentro entre la tecnología y el hombre. Un espacio negativo central simboliza ese punto de encuentro.  
**Tipografía del logo:** Menseal Regular (geométrica, sin serif, moderna)  
**Tipografía del slogan:** Articulat CF (oblique / demi-bold oblique)  
**Color primario:** Negro PM `#222524`  
**Color de acento:** Lima PM `#CCFF50`

---

## 2. PALETA DE COLORES OFICIAL

### Primario
| Nombre | Hex | Pantone | Uso |
|--------|-----|---------|-----|
| Negro PM | `#222524` | Black 7 C | Fondo principal, texto principal, headers, logo versión oscura |
| Lima PM | `#CCFF50` | 375 C | Color de acento y energía — CTAs digitales, isotipo en pantalla, detalles activos |

### Secundarios / Complementarios
| Nombre | Hex | Pantone | Uso |
|--------|-----|---------|-----|
| Arena Claro | `#D6B78D` | 728 C | Acento cálido — fondos de sección, bolsas, piezas de merchandising |
| Arena Oscuro | `#9B8B78` | 7530 C | Isotipo en versión neutra sobre fondos claros, texto secundario cálido |
| Malva / Blue | `#7C90E5` | 2715 C | Acento digital secundario — badges, categorías, elementos de UI específicos |
| Blanco Hueso | `#F5F7F0` | 663 C | Fondo cálido de reportes, fondos de tarjeta, fondos de email |

### Paleta ordenada (oscuro → claro)
```
#222524  →  #9B8B78  →  #D6B78D  →  #F5F7F0
```
Con acentos: `#CCFF50` (lima digital) · `#7C90E5` (blue secundario)

### Tokens CSS recomendados
```css
:root {
  /* Primarios */
  --pm-black:       #222524;
  --pm-lime:        #CCFF50;
  --pm-lime-hot:    #D4FF6A;        /* hover */
  --pm-lime-deep:   #AADD30;        /* pressed */
  --pm-lime-tint:   rgba(204,255,80,0.12); /* fondos suaves */

  /* Secundarios */
  --pm-sand-light:  #D6B78D;
  --pm-sand-dark:   #9B8B78;
  --pm-blue:        #7C90E5;
  --pm-blue-tint:   rgba(124,144,229,0.12);
  --pm-bone:        #F5F7F0;
  --pm-white:       #FFFFFF;

  /* Grises neutros */
  --pm-gray-1:      #3A3C3B;        /* texto secundario oscuro */
  --pm-gray-2:      #888888;        /* bordes, separadores */
  --pm-gray-3:      #C8C8C8;        /* fondos de tabla alternos */

  /* Semánticos */
  --pm-bg:          var(--pm-black);
  --pm-bg-light:    var(--pm-bone);
  --pm-text:        var(--pm-bone);          /* sobre fondo negro */
  --pm-text-dark:   var(--pm-black);         /* sobre fondo claro */
  --pm-text-2:      var(--pm-gray-2);
  --pm-accent:      var(--pm-lime);
  --pm-accent-warm: var(--pm-sand-light);
  --pm-border:      var(--pm-gray-2);
}
```

### Modo de uso por contexto
| Contexto | Fondo | Texto | Acento |
|----------|-------|-------|--------|
| Digital / web oscuro (default) | `#222524` | `#F5F7F0` | `#CCFF50` |
| Reportes / documentos claros | `#F5F7F0` | `#222524` | `#D6B78D` |
| Piezas de merchandising / print | `#D6B78D` (arena) | `#F5F7F0` | `#CCFF50` |
| Email corporativo | `#FFFFFF` | `#222524` | `#D6B78D` |

---

## 3. TIPOGRAFÍA

### Fuentes oficiales PM
Los archivos están disponibles en la carpeta de assets de Plaza Madero.

| Fuente | Archivo | Rol | Características |
|--------|---------|-----|-----------------|
| **Menseal Regular** | `Menseal-Regular.otf` | **PRINCIPAL — logo, UI, display** | Geométrica, sans-serif, trazos uniformes, moderna y tecnológica |
| **Menseal Bold** | `Menseal-Bold.otf` | Titulares, énfasis, KPIs | Versión bold de la fuente principal — para jerarquía fuerte |
| **Articulat CF Bold Oblique** | `Fontspring-DEMO-articulatcf-boldoblique-*.otf` | Slogan, cuerpo de impacto | Oblique, geométrica, energética — usar en el tagline y piezas de comunicación |
| **Articulat CF Demi Bold Oblique** | `Fontspring-DEMO-articulatcf-demiboldoblique-*.otf` | Subtítulos, apoyo al slogan | Peso intermedio oblique — para jerarquías secundarias de comunicación |

### Fallbacks seguros (cuando fuentes PM no estén instaladas)
```css
--pm-font-display:  'Menseal', 'Inter', 'DM Sans', 'Helvetica Neue', sans-serif;
--pm-font-headline: 'Menseal Bold', 'Inter', 'Helvetica Neue', sans-serif;
--pm-font-slogan:   'Articulat CF', 'DM Sans', 'Inter', sans-serif;
--pm-font-body:     'Inter', 'Helvetica Neue', 'Segoe UI', system-ui, sans-serif;
--pm-font-mono:     'JetBrains Mono', 'Fira Code', Consolas, monospace;
```

### Escala tipográfica
| Nivel | Fuente | Tamaño | Peso | Uso |
|-------|--------|--------|------|-----|
| Display XL | Menseal Bold | 72–96px | 700 | Portadas, hero sections, pantallas principales |
| H1 | Menseal Regular | 48–64px | 400–500 | Títulos principales de página |
| H2 | Menseal Regular | 32–40px | 400 | Secciones, títulos de tarjeta |
| H3 | Menseal Regular | 24–28px | 400 | Subtítulos |
| H4 | Menseal Bold | 18–20px | 700 | Encabezados de tabla, labels fuertes |
| Slogan | Articulat CF Bold Oblique | 14–18px | 700 italic | Tagline "el epicentro de la tecnología" |
| Body | Inter / system-ui | 14–16px | 400 | Texto corrido, párrafos |
| Body Small | Inter / system-ui | 12–13px | 400 | Notas, pie de página, metadatos |
| Label | Menseal Regular | 10–11px | 700 | Etiquetas, eyebrows (uppercase + letter-spacing) |
| Mono | JetBrains Mono | 12–13px | 400 | Precios, cifras, código, fechas |

### Reglas tipográficas
- **Eyebrow / label:** `font-size: 11px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.14em; color: var(--pm-lime)`
- **Precio / cifra clave:** `font-family: var(--pm-font-mono); font-variant-numeric: tabular-nums; letter-spacing: -0.02em`
- **Título de sección:** `font-family: var(--pm-font-display); font-weight: 400; text-transform: uppercase; letter-spacing: 0.06em`
- **Slogan:** Siempre en Articulat CF, italic/oblique, en minúsculas — nunca en mayúsculas
- Nunca mezclar más de 2 fuentes en una misma pieza
- Lima `#CCFF50` solo en acentos tipográficos digitales — nunca en texto corrido largo
- Arena `#D6B78D` para acentos tipográficos en piezas cálidas / print

---

## 4. LOGO — VARIANTES Y USO

### Anatomía del sistema de logo

```
ISOTIPO      = Las dos flechas convergentes (símbolo puro, sin texto)
LOGOTIPO     = "PLAZA MADERO" (texto solo, Menseal Regular, mayúsculas)
SLOGAN       = "el epicentro de la tecnología" (Articulat CF, lowercase)
COMPLETO     = ISOTIPO + LOGOTIPO (horizontal) + SLOGAN (esquina superior derecha)
```

### Descripción del isotipo
El símbolo consiste en **dos flechas que convergen** formando una cruz geométrica con una línea diagonal: una flecha apunta hacia arriba-derecha y otra hacia abajo-izquierda, con brazos ortogonales que las atraviesan. En el punto de encuentro existe un **espacio negativo** (cuadrado pequeño) que simboliza el epicentro — el punto donde se encuentran tecnología y usuario.

### Archivos disponibles
| Archivo | Color isotipo | Texto logo | Usar sobre |
|---------|--------------|------------|------------|
| `01.png` | Lima `#CCFF50` | — | Fondo negro, oscuro |
| `02.png` | Arena claro `#D6B78D` | — | Fondo negro, oscuro |
| `03.png` | Blue `#7C90E5` | — | Fondo negro, oscuro |
| `04.png` | Negro `#222524` | — | Fondo blanco o claro |
| `05.png` | Hueso `#F5F7F0` | — | Fondo negro, oscuro |
| `06.png` | Arena oscuro `#9B8B78` | — | Fondo negro, oscuro |
| `Editable_isotipo.ai` | Editable | — | Archivo fuente Illustrator |
| Logo horizontal oscuro | Arena `#D6B78D` | `#222524` | Fondo blanco / hueso |
| Logo horizontal claro | Hueso `#F5F7F0` | `#F5F7F0` | Fondo negro `#222524` |
| Logo horizontal lima | Lima `#CCFF50` | `#F5F7F0` | Fondo negro `#222524` |
| Logo horizontal blue | Blue `#7C90E5` | `#222524` | Fondo blanco / hueso |

### Variantes de color del isotipo según contexto
| Contexto | Isotipo | Fondo |
|----------|---------|-------|
| Web / digital (default) | Lima `#CCFF50` | Negro `#222524` |
| Print / merchandising | Arena `#D6B78D` | Negro `#222524` |
| Sobre fondo blanco/hueso | Arena oscuro `#9B8B78` | Blanco / `#F5F7F0` |
| Monocromático oscuro | Negro `#222524` | Blanco / `#F5F7F0` |
| Monocromático claro | Hueso `#F5F7F0` | Negro `#222524` |

### Fondo del ícono en UI compacto (nav, favicon, avatar)
- Fondo: `#222524` (negro PM) — **siempre**
- Isotipo PNG: versión lima `#CCFF50` sobre ese fondo
- Border-radius: `8px` (nav small), `14px` (login/card)

### Espacio de respeto
- Mínimo: `= ancho de un brazo del isotipo` alrededor del logo completo
- El slogan "el epicentro de la tecnología" va siempre en la esquina superior derecha del logotipo, en Articulat CF, tamaño pequeño (10–12px en uso digital)
- Nunca distorsionar proporciones del isotipo
- Nunca aplicar efectos (sombra, gradiente, stroke extra)
- Nunca rotar el isotipo — su orientación diagonal es parte de su identidad
- Nunca cambiar colores fuera del sistema de 6 colores aprobados

---

## 5. COMPONENTES UI

### Botón primario
```css
.btn-primary {
  background: var(--pm-lime);
  color: var(--pm-black);
  font-family: var(--pm-font-display);
  font-weight: 700;
  font-size: 14px;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  border: none;
  border-radius: 6px;
  padding: 12px 24px;
  cursor: pointer;
  transition: background 200ms ease;
}
.btn-primary:hover  { background: #D4FF6A; }
.btn-primary:active { background: #AADD30; }
```

### Botón secundario / ghost
```css
.btn-ghost {
  background: transparent;
  color: var(--pm-bone);
  border: 1.5px solid rgba(245,247,240,0.30);
  border-radius: 6px;
  padding: 10px 20px;
  font-family: var(--pm-font-display);
  font-weight: 400;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  transition: all 200ms ease;
}
.btn-ghost:hover {
  border-color: var(--pm-lime);
  color: var(--pm-lime);
}
/* Versión sobre fondo claro */
.btn-ghost-dark {
  color: var(--pm-black);
  border-color: rgba(34,37,36,0.30);
}
.btn-ghost-dark:hover {
  border-color: var(--pm-black);
  color: var(--pm-black);
}
```

### Card / tarjeta (sobre fondo oscuro)
```css
.card {
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(245,247,240,0.10);
  border-radius: 12px;
  padding: 24px;
}
/* Card sobre fondo claro */
.card-light {
  background: var(--pm-white);
  border: 1px solid var(--pm-gray-3);
  border-radius: 12px;
  padding: 24px;
  box-shadow: 0 2px 8px rgba(34,37,36,0.06);
}
/* Header de card */
.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 16px;
  padding-bottom: 12px;
  border-bottom: 1px solid rgba(245,247,240,0.10);
}
.card-title {
  font-family: var(--pm-font-display);
  font-weight: 700;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  color: var(--pm-lime);
}
```

### Input / campo de formulario
```css
.input {
  width: 100%;
  padding: 10px 14px;
  border: 1.5px solid rgba(245,247,240,0.20);
  border-radius: 6px;
  font-family: var(--pm-font-body);
  font-size: 14px;
  color: var(--pm-bone);
  background: rgba(255,255,255,0.05);
  transition: border-color 200ms;
}
.input:focus {
  outline: none;
  border-color: var(--pm-lime);
  box-shadow: 0 0 0 3px rgba(204,255,80,0.12);
}
.input::placeholder { color: rgba(245,247,240,0.35); }
```

### Badge / píldora de estado
```css
/* Lima — activo, disponible, destacado */
.badge-lime {
  background: rgba(204,255,80,0.15);
  color: var(--pm-lime);
  border: 1px solid rgba(204,255,80,0.30);
  border-radius: 100px;
  padding: 4px 10px;
  font-size: 11px; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.10em;
}
/* Arena — información, neutro cálido */
.badge-sand {
  background: rgba(214,183,141,0.15);
  color: var(--pm-sand-light);
  border: 1px solid rgba(214,183,141,0.30);
  border-radius: 100px;
  padding: 4px 10px;
  font-size: 11px; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.10em;
}
/* Blue — secundario, categorías */
.badge-blue {
  background: rgba(124,144,229,0.15);
  color: var(--pm-blue);
  border: 1px solid rgba(124,144,229,0.30);
  border-radius: 100px;
  padding: 4px 10px;
  font-size: 11px; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.10em;
}
/* Neutro — inactivo */
.badge-neutral {
  background: rgba(245,247,240,0.06);
  color: rgba(245,247,240,0.50);
  border: 1px solid rgba(245,247,240,0.12);
  border-radius: 100px;
  padding: 4px 10px;
  font-size: 11px; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.10em;
}
```

### Tag / categoría de producto
```css
.tag {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 6px 12px;
  background: rgba(245,247,240,0.06);
  border: 1px solid rgba(245,247,240,0.10);
  border-radius: 6px;
  font-size: 12px;
  color: rgba(245,247,240,0.70);
  font-family: var(--pm-font-display);
  letter-spacing: 0.04em;
}
.tag:hover {
  border-color: var(--pm-lime);
  color: var(--pm-lime);
  background: var(--pm-lime-tint);
}
```

---

## 6. TABLAS

```css
/* Tabla de reportes Plaza Madero */
.pm-table {
  width: 100%;
  border-collapse: collapse;
  font-family: var(--pm-font-body);
  font-size: 13px;
}
/* Línea de acento superior */
.pm-table-wrap {
  border-top: 2px solid var(--pm-lime);
  border-radius: 0;
}
/* Encabezados */
.pm-table thead th {
  font-family: var(--pm-font-display);
  font-weight: 700;
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 0.14em;
  color: var(--pm-lime);
  padding: 10px 14px;
  border-bottom: 1px solid rgba(204,255,80,0.20);
  text-align: left;
  background: var(--pm-black);
}
/* Filas */
.pm-table tbody tr { border-bottom: 1px solid rgba(245,247,240,0.06); }
.pm-table tbody tr:nth-child(even) { background: rgba(255,255,255,0.02); }
.pm-table tbody tr:hover           { background: rgba(204,255,80,0.04); }
.pm-table tbody td {
  padding: 10px 14px;
  color: var(--pm-bone);
  vertical-align: middle;
}
/* Cifras numéricas */
.pm-table .num {
  font-family: var(--pm-font-mono);
  font-variant-numeric: tabular-nums;
  text-align: right;
  letter-spacing: -0.02em;
}

/* Versión para fondos claros (reportes PDF) */
.pm-table-light thead th {
  color: var(--pm-black);
  background: var(--pm-bone);
  border-bottom: 1px solid rgba(34,37,36,0.15);
}
.pm-table-light {
  border-top: 2px solid var(--pm-sand-dark);
}
.pm-table-light tbody td { color: var(--pm-black); }
.pm-table-light tbody tr:nth-child(even) { background: rgba(34,37,36,0.03); }
```

---

## 7. EMAIL HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Plaza Madero</title>
  <style>
    body {
      margin: 0; padding: 0;
      background: #F5F7F0;
      font-family: 'Inter', 'Helvetica Neue', Arial, sans-serif;
    }
    .wrapper {
      max-width: 600px; margin: 0 auto;
      background: #FFFFFF;
    }

    /* Header negro con lima */
    .email-header {
      background: #222524;
      padding: 24px 32px;
      display: flex; align-items: center; gap: 16px;
    }
    .email-logo-box {
      width: 40px; height: 40px;
      display: flex; align-items: center; justify-content: center;
    }
    .email-brand strong {
      display: block;
      font-size: 16px; font-weight: 700;
      letter-spacing: 0.08em; text-transform: uppercase;
      color: #F5F7F0;
    }
    .email-brand small {
      font-size: 10px; color: rgba(245,247,240,0.45);
      text-transform: lowercase; letter-spacing: 0.08em;
      font-style: italic;
    }

    /* Banda lima de acento */
    .email-accent-bar { height: 3px; background: #CCFF50; }

    /* Sección */
    .email-section {
      background: #FFFFFF;
      padding: 32px 40px;
      border-bottom: 1px solid #E8E8E8;
    }
    .email-section-label {
      font-size: 10px; font-weight: 700;
      text-transform: uppercase; letter-spacing: 0.18em;
      color: #9B8B78; margin-bottom: 12px;
    }
    .email-body { font-size: 14px; color: #222524; line-height: 1.7; }

    /* KPI grande */
    .kpi-value {
      font-family: 'JetBrains Mono', 'Courier New', monospace;
      font-size: 42px; font-weight: 700;
      color: #222524; letter-spacing: -0.02em;
    }
    .kpi-label { font-size: 12px; color: #888888; margin-top: 4px; }

    /* CTA */
    .email-cta {
      display: inline-block;
      background: #CCFF50; color: #222524;
      font-weight: 700; font-size: 13px;
      letter-spacing: 0.06em; text-transform: uppercase;
      text-decoration: none;
      padding: 12px 28px; border-radius: 6px;
      margin-top: 16px;
    }

    /* Footer */
    .email-footer {
      background: #222524; padding: 20px 40px;
      text-align: center;
      font-size: 11px; color: rgba(245,247,240,0.35);
      letter-spacing: 0.06em;
    }
  </style>
</head>
<body>
  <div class="wrapper">
    <div class="email-header">
      <div class="email-logo-box">
        <img src="cid:logo" alt="PM" width="36">
      </div>
      <div class="email-brand">
        <strong>Plaza Madero</strong>
        <small>el epicentro de la tecnología</small>
      </div>
    </div>
    <div class="email-accent-bar"></div>

    <div class="email-section">
      <div class="email-section-label">Nombre de sección</div>
      <!-- contenido -->
    </div>

    <div class="email-footer">
      Plaza Madero · plazamadero.com · Confidencial
    </div>
  </div>
</body>
</html>
```

---

## 8. PDF / PRINT

### Contexto de impresión PM
Plaza Madero opera en dos modos de impresión: **modo oscuro premium** (fondos negros con acento arena/lima, para materiales de alto impacto) y **modo claro corporativo** (fondos hueso/blanco, para documentos internos y reportes).

### Variables para impresión
```css
@media print {
  /* Modo claro (documentos internos) */
  body { background: #F5F7F0; color: #222524; }

  * { box-shadow: none !important; transition: none !important; }

  /* Lima se imprime bien — verificar en impresora antes de usar */
  /* En caso de dudas de impresión, usar arena #D6B78D como acento */
  .pm-accent { color: #D6B78D; }

  /* Encabezado de página PDF */
  .pdf-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 3px solid #9B8B78;
    padding-bottom: 16px;
    margin-bottom: 24px;
  }
  .pdf-footer {
    position: fixed;
    bottom: 0; left: 0; right: 0;
    border-top: 1px solid #C8C8C8;
    padding: 8px 40px;
    font-size: 10px; color: #888888;
    display: flex; justify-content: space-between;
  }

  .page-break { page-break-before: always; }
  .no-break   { page-break-inside: avoid; }
}
```

### Márgenes de página recomendados
- Carta/A4: `margin: 20mm 25mm` (Word/PDF)
- Header fijo: isotipo PM izquierda (versión arena `#D6B78D`) + fecha derecha
- Footer fijo: `Plaza Madero · el epicentro de la tecnología · Página X de Y`
- Color de línea divisoria encabezado: `#9B8B78` (arena oscuro) 2–3pt en documentos claros; `#CCFF50` 2pt en documentos oscuros premium

---

## 9. MODO OSCURO / CLARO (web apps)

Plaza Madero tiene **modo oscuro como modo por defecto** (fondo negro). El modo claro es una variante alternativa para reportes y contextos administrativos.

```css
/* Default: modo oscuro (identidad primaria de PM) */
:root {
  --pm-bg:      #222524;
  --pm-bg-card: rgba(255,255,255,0.04);
  --pm-text:    #F5F7F0;
  --pm-text-2:  rgba(245,247,240,0.55);
  --pm-text-3:  rgba(245,247,240,0.30);
  --pm-border:  rgba(245,247,240,0.10);
  --pm-accent:  #CCFF50;
}

/* Modo claro alternativo */
body[data-mode="light"] {
  --pm-bg:      #F5F7F0;
  --pm-bg-card: #FFFFFF;
  --pm-text:    #222524;
  --pm-text-2:  #3A3C3B;
  --pm-text-3:  #888888;
  --pm-border:  #C8C8C8;
  --pm-accent:  #9B8B78;  /* lima da poco contraste sobre fondo claro → cambiar a arena oscuro */
}
```

**Reglas de oro del color:**
- `#CCFF50` (lima) es el acento digital — solo sobre fondos oscuros `#222524` donde da máximo contraste
- Sobre fondos claros, el acento cambia a `#9B8B78` (arena oscuro) — lima no tiene contraste suficiente sobre hueso/blanco
- `#D6B78D` (arena claro) es el acento de calidez — para print, merchandising y piezas físicas
- El negro `#222524` nunca cambia — es el ADN de la marca en ambos modos

---

## 10. REGLAS DE ORO (resumen ejecutivo para IA/agentes)

1. **Negro `#222524`** — identidad primaria. Fondo default en digital, texto principal en documentos claros.
2. **Lima `#CCFF50`** — acento de energía digital. Va en: botones primarios, eyebrows, barras de acento, isotipo en pantalla, links activos. **Solo sobre fondo oscuro.**
3. **Arena `#D6B78D` / `#9B8B78`** — acentos de calidez. Usar en: isotipo sobre fondos claros, print, merchandising, acento alternativo en modo claro.
4. **Blue `#7C90E5`** — acento secundario digital. Usar en: categorías, badges secundarios, elementos de UI específicos.
5. **Menseal Regular** — toda tipografía visible de marca (logo, display, UI). Siempre en mayúsculas en el logotipo.
6. **Articulat CF** — tipografía del slogan y comunicación de impacto. Siempre en minúsculas, siempre oblique.
7. **Logo texto** — "PLAZA MADERO" siempre en MAYÚSCULAS, Menseal Regular.
8. **Slogan** — "el epicentro de la tecnología" siempre en minúsculas, Articulat CF, en la esquina del logo.
9. **Isotipo** — nunca rotarlo, nunca cambiar su orientación diagonal. El espacio negativo central es parte integral del símbolo.
10. **Tablas digitales** — línea superior `border-top: 2px solid #CCFF50`, encabezados en Menseal uppercase.
11. **Tablas en print** — línea superior en arena oscuro `#9B8B78` (lima no imprime siempre bien).
12. **Cifras/precios** — siempre en fuente monoespaciada (`JetBrains Mono` o equivalente).
13. **Lima en modo claro** — prohibido. Cambiar a arena oscuro `#9B8B78` cuando el fondo sea claro.
14. **No mezclar** más de 2 pesos de fuente en una misma sección.

---

## 11. RUTAS DE ASSETS

```
plaza-madero/
├── 01_LOGO/
│   ├── 01.png                    ← isotipo lima (#CCFF50) sobre negro
│   ├── 02.png                    ← isotipo arena claro (#D6B78D) sobre negro
│   ├── 03.png                    ← isotipo blue (#7C90E5) sobre negro
│   ├── 04.png                    ← isotipo negro (#222524) sobre claro
│   ├── 05.png                    ← isotipo hueso (#F5F7F0) sobre negro
│   ├── 06.png                    ← isotipo arena oscuro (#9B8B78) sobre negro
│   ├── Editable_isotipo.ai       ← archivo fuente Illustrator (editable)
│   ├── edit_.ai                  ← variante editable adicional
│   ├── Logo horizontal oscuro    ← isotipo arena + "PLAZA MADERO" dark en fondo negro
│   ├── Logo horizontal claro     ← isotipo hueso + "PLAZA MADERO" claro en fondo negro
│   └── Logo horizontal lima      ← isotipo lima + "PLAZA MADERO" claro en fondo negro
│
├── 02_TIPOGRAFIA/
│   ├── Menseal-Regular.otf       ← PRINCIPAL — instalar primero
│   ├── Menseal-Bold.otf          ← bold de la fuente principal
│   ├── Fontspring-DEMO-articulatcf-boldoblique-*.otf      ← slogan
│   └── Fontspring-DEMO-articulatcf-demiboldoblique-*.otf  ← apoyo slogan
│
├── 03_PALETA DE COLORES/
│   ├── CCFF50  ← Lima PM (acento digital primario)    Pantone 375 C
│   ├── 222524  ← Negro PM (identidad primaria)        Pantone Black 7 C
│   ├── D6B78D  ← Arena claro (acento cálido)          Pantone 728 C
│   ├── 9B8B78  ← Arena oscuro (acento print)          Pantone 7530 C
│   ├── 7C90E5  ← Blue (acento secundario digital)     Pantone 2715 C
│   └── F5F7F0  ← Hueso (fondo claro / reportes)       Pantone 663 C
│
└── 04_BRANDBOOK/
    └── BRANDBOOK_PM.pdf          ← Manual de marca oficial Plaza Madero
```

---

## 12. RELACIÓN CON EL SISTEMA GO

> Este archivo (`pm.md`) es el manual de identidad de **Plaza Madero** — sub-marca de Grupo Ortiz. Extiende el sistema base `context_design.md` con los tokens, tipografías y reglas específicas de PM.

| Elemento | Sistema GO | Plaza Madero PM |
|----------|-----------|-----------------|
| Color de acento | Naranja `#FB670B` | Lima `#CCFF50` (digital) / Arena `#D6B78D` (print) |
| Fuente principal | Blauer Nue | Menseal Regular |
| Fuente de apoyo | Conthic | Articulat CF (oblique) |
| Fondo default | Blanco / Crema | Negro `#222524` |
| Personalidad | Cálido, orgánico, cercano | Tecnológico, premium, convergente |
| Sector | Corporativo / Industrial | Retail tecnológico |

### Regla de carga para agentes e IA

```
Proyecto Plaza Madero        → context_design.md  +  pm.md
Proyecto multi-marca con PM  → context_design.md  +  brand_system.md  +  pm.md
Duda sobre qué marca usar    → brand_system.md §2 (Árbol de decisión)
```

---

*Última actualización: 2026-05-31 · Basado en BRANDBOOK_PM.pdf y assets oficiales Plaza Madero*
