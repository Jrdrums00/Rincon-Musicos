# Identidad Visual — Johan Rincón / Rincón del Músico

Guía de diseño para la página web. Dos marcas visuales complementarias bajo el mismo artista:

| Marca | Uso | Paleta |
|-------|-----|--------|
| **El Rincón del Músico** | Clases, academia, masterclasses | Azul/cyan sobre negro |
| **JSounds Store** | Tienda, instrumentos, ventas | Rojo sobre blanco/claro |

---

## 1. Paleta de Colores

### Fondos y Superficies (dark muted)

| Token | Hex | Uso |
|-------|-----|-----|
| `bg-base` | `#0A0A0A` | Background principal, base del logo academia |
| `bg-surface` | `#111827` | Cards, panels, secciones |
| `bg-secondary` | `#1F2937` | Secciones alternas, footer |

### Acentos — El Rincón del Músico (azul/cyan)

| Token | Hex | Uso |
|-------|-----|-----|
| `brand-primary` | `#0EA5E9` | CTA principal, links activos |
| `brand-light` | `#38BDF8` | Hover states, highlights, iconos |
| `brand-deep` | `#0369A1` | Headers, texto destacado, sombras |

### Acentos — JSounds Store (rojo)

| Token | Hex | Uso |
|-------|-----|-----|
| `store-accent` | `#CC0000` | Badges de oferta, precio, CTA tienda |
| `store-hover` | `#991B1B` | Hover del rojo |

### Neutros

| Token | Hex | Uso |
|-------|-----|-----|
| `text-primary` | `#F9FAFB` | Texto principal sobre fondo oscuro |
| `text-secondary` | `#9CA3AF` | Subtítulos, metadatos, captions |
| `border` | `#374151` | Bordes, divisores, separadores |

### Gradiente de Marca

```css
/* Replicando el degradado de la nota musical del logo academia */
background: linear-gradient(135deg, #0EA5E9 0%, #0369A1 50%, #1e3a5f 100%);
```

---

## 2. Tipografía

### Sistema de 3 Fuentes

| Rol | Fuente | Peso | Uso |
|-----|--------|------|-----|
| Display / Hero | **Bebas Neue** | 400 | Títulos grandes, secciones hero, números de impacto |
| Decorativa / Acento | **Shadows Into Light** | 400 | Citas, taglines artísticas, "Sobre nosotros" |
| Cuerpo / UI | **Roboto Condensed** | 300, 400, 700 | Párrafos, descripciones, botones, navegación |

**Por qué este sistema:**
- **Bebas Neue** → impacto visual fuerte, muy usado en marcas musicales/deportivas. Complementa el estilo de JSounds Store y genera contraste con la delicadeza de la otra fuente.
- **Shadows Into Light** → toque artístico y humano, conecta con la parte académica y la personalidad del músico. Mantiene la preferencia del usuario por esta fuente.
- **Roboto Condensed** → legibilidad en móvil, limpio, ahorra espacio horizontal en descripciones de servicios y precios. Mantiene la preferencia del usuario.

### Escala Tipográfica

```css
/* Hero / Banner principal */
.text-hero    { font-family: 'Bebas Neue'; font-size: clamp(72px, 10vw, 96px); }

/* Títulos de sección */
.text-h1      { font-family: 'Bebas Neue'; font-size: 48px; }
.text-h2      { font-family: 'Bebas Neue'; font-size: 36px; }
.text-h3      { font-family: 'Roboto Condensed'; font-size: 24px; font-weight: 700; }

/* Taglines artísticas */
.text-tagline { font-family: 'Shadows Into Light'; font-size: 22px; }

/* Cuerpo */
.text-body    { font-family: 'Roboto Condensed'; font-size: 16px; font-weight: 400; }
.text-small   { font-family: 'Roboto Condensed'; font-size: 14px; font-weight: 300; }
```

### Google Fonts — Import

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Roboto+Condensed:ital,wght@0,100..900;1,100..900&family=Shadows+Into+Light&display=swap" rel="stylesheet">
```

---

## 3. Logos y Uso

### Logo 1 — El Rincón del Músico
**Archivo original:** `docs/resourcers/Logo Johan muestra .PNG`
**Archivo transparente:** `docs/resourcers/logo-rincon-transparent.png`

- Usar en: Header principal, sección Clases de Batería, Masterclass, Academia
- Fondo recomendado: oscuro (`#0A0A0A` o gradiente de marca)
- El texto y nota musical son en azul/cyan — funcionan mejor sobre negro

### Logo 2 — JSounds Store
**Archivo original:** `docs/resourcers/ChatGPT Image 21 mar 2026, 14_38_34.png`
**Archivo transparente:** `docs/resourcers/logo-jsounds-transparent.png`

- Bombo rojo con efecto neon + texto "JSounds Store" en negro/gris oscuro
- Sin fondo — usar directamente sobre cualquier color de marca
- Usar en: Sección de venta de instrumentos, tienda, carrito, productos
- Separar visualmente de las secciones académicas (sección propia o header alterno)

> **Nota:** Con fondos removidos, ambos logos pueden usarse sobre cualquier fondo de marca. Ver sección 6 para proceso de transparencia.

---

## 4. Espaciado y Bordes

### Border Radius
```css
--radius-sm:   4px;   /* badges, chips, inputs */
--radius-md:   8px;   /* cards, modales, imágenes */
--radius-full: 9999px; /* botones pill, avatares */
```

### Escala de Espaciado (base 4px)
```
4px  · 8px  · 16px · 24px · 32px · 48px · 64px · 96px
```

### Sombras
```css
/* Glow azul sutil — cards destacados, botones activos */
box-shadow: 0 4px 24px rgba(14, 165, 233, 0.15);

/* Sombra neutra — cards estándar */
box-shadow: 0 2px 8px rgba(0, 0, 0, 0.4);
```

---

## 5. Botones CTA

```css
/* Primario — Academia / Clases */
.btn-primary {
  background: #0EA5E9;
  color: #ffffff;
  border-radius: 9999px;
  padding: 12px 32px;
  font-family: 'Roboto Condensed';
  font-weight: 700;
}
.btn-primary:hover { background: #0369A1; }

/* WhatsApp */
.btn-whatsapp {
  background: #25D366;
  color: #ffffff;
  /* Incluir icono SVG de WhatsApp */
}

/* Secundario / Outline */
.btn-secondary {
  background: transparent;
  border: 2px solid #0EA5E9;
  color: #0EA5E9;
  border-radius: 9999px;
  padding: 10px 32px;
}
.btn-secondary:hover {
  background: rgba(14, 165, 233, 0.1);
}

/* Tienda (JSounds Store) */
.btn-store {
  background: #CC0000;
  color: #ffffff;
  border-radius: 8px;
}
.btn-store:hover { background: #991B1B; }
```

---

## 6. Procesamiento de Logos — Remover Fondos

Solo el Logo 1 requiere procesamiento. El Logo 2 ya viene sin fondo.

### Script Python — Logo 1 únicamente

```python
# Requiere: pip install Pillow numpy
from PIL import Image
import numpy as np

def remove_dark_bg(input_path, output_path, threshold=40):
    """Elimina fondo negro/oscuro — Logo El Rincón del Músico."""
    img = Image.open(input_path).convert("RGBA")
    data = np.array(img)
    r, g, b, a = data[:,:,0], data[:,:,1], data[:,:,2], data[:,:,3]
    mask = (r < threshold) & (g < threshold) & (b < threshold)
    data[mask] = [0, 0, 0, 0]
    Image.fromarray(data).save(output_path)
    print(f"Guardado: {output_path}")

remove_dark_bg(
    "docs/resourcers/Logo Johan muestra .PNG",
    "docs/resourcers/logo-rincon-transparent.png",
    threshold=40
)
```

### Archivos de logo listos para usar

| Logo | Archivo | Estado |
|------|---------|--------|
| El Rincón del Músico | `logo-rincon-transparent.png` | Fondo negro removido con Pillow |
| JSounds Store | `ChatGPT Image 21 mar 2026, 14_38_34.png` | Sin fondo — usar directamente |

---

## 7. Checklist de Validación

- [ ] Contraste texto/fondo cumple WCAG AA (mínimo 4.5:1 para body, 3:1 para large text)
- [ ] Fonts precargadas con `<link rel="preconnect">` antes del import de Google Fonts
- [ ] Logos transparentes validados sobre fondo oscuro (`#0A0A0A`) y claro (`#F9FAFB`)
- [ ] Recorte de fondo limpio — sin halo blanco ni bordes duros visibles
- [ ] Sección academia y sección tienda visualmente diferenciadas (paleta azul vs. rojo)
- [ ] Botones WhatsApp presentes en secciones de contacto y clases
- [ ] Responsive: escala tipográfica funciona en mobile (usar `clamp()` para hero)
