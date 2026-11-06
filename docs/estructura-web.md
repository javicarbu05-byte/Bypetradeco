# Estructura de la nueva web de By Petra (propuesta v1)

Propuesta basada en la auditoría (`docs/auditoria-web-actual.md`). Pendiente de validar.

## 1. Mapa del sitio

```text
INICIO
├── TIENDA
│   ├── Platitos y bandejas   (filtros: forma · colección · tamaño)
│   ├── Llaveros
│   ├── Chupeteros
│   ├── Neceseres
│   ├── Maletas
│   ├── Dibujos personalizados
│   └── Navidad               (solo en temporada)
│        └── Ficha de producto (configurador por pasos)
├── CÓMO FUNCIONA             (elegir → personalizar → recibir)
├── SOBRE PETRA               (historia, taller, hecho a mano)
├── AYUDA
│   ├── Envíos y plazos
│   ├── Cambios y devoluciones
│   └── Preguntas frecuentes
├── CONTACTO                  (formulario + WhatsApp + email + Instagram)
├── CESTA → PAGO → CONFIRMACIÓN
├── MI CUENTA                 (opcional)
└── LEGAL: Aviso legal · Condiciones de venta · Privacidad · Cookies
```

**Menú principal (máx. 5):** Tienda ▾ · Cómo funciona · Sobre Petra · Contacto · (Buscar + Cesta)

**En todas las páginas:** barra de aviso arriba, cabecera única, pie de página, botón flotante de
WhatsApp y banner de cookies con consentimiento real.

**Regla de catálogo:** un producto por estampado; la forma (redondo/cuadrado/rectangular) y el
tamaño son opciones dentro de la ficha, no productos separados.

## 2. Croquis

### Inicio (escritorio)

```text
┌──────────────────────────────────────────────────────┐
│ Hecho a mano en Barcelona · Envío en 5-10 días       │
├──────────────────────────────────────────────────────┤
│ BY PETRA    Tienda ▾   Cómo funciona   Sobre Petra   │
│             Contacto                  Buscar  Cesta  │
├──────────────────────────────────────────────────────┤
│         [  FOTO GRANDE: mesa puesta con platitos ]   │
│                                                      │
│    Detalles personalizados, hechos a mano            │
│    [ Ver la tienda ]   [ Cómo personalizar ]         │
├──────────────────────────────────────────────────────┤
│ CATEGORÍAS                                           │
│ [Platitos y ] [Llaveros] [Chupeteros] [Neceseres]    │
│ [ bandejas  ] [Maletas ] [Navidad (temporada)   ]    │
├──────────────────────────────────────────────────────┤
│ CÓMO FUNCIONA                                        │
│  1. Elige        2. Personaliza      3. Lo recibes   │
│  el producto     iniciales/nombre    en 5-10 días    │
├──────────────────────────────────────────────────────┤
│ MÁS VENDIDOS                          Ver todo →     │
│ [foto]      [foto]      [foto]      [foto]           │
│ Nombre      Nombre      Nombre      Nombre           │
│ desde 8 €   15 €        26 €        45 €             │
├──────────────────────────────────────────────────────┤
│ COLECCIÓN DE TEMPORADA  (banner Navidad / Otoño)     │
├──────────────────────────────────────────────────────┤
│ [foto Petra]   SOBRE PETRA: 3 líneas de historia     │
│                [ Conócenos ]                         │
├──────────────────────────────────────────────────────┤
│ OPINIONES  ★★★★★  "…"   ★★★★★  "…"   ★★★★★  "…"      │
├──────────────────────────────────────────────────────┤
│ INSTAGRAM @bypetra.deco   [ ][ ][ ][ ][ ][ ]         │
├──────────────────────────────────────────────────────┤
│ PIE: Tienda | Ayuda (envíos, FAQ) | Contacto         │
│      WhatsApp · Email · Instagram · Newsletter       │
│      Aviso legal · Privacidad · Cookies · Condiciones│
└──────────────────────────────────────────────────────┘
```

### Categoría (escritorio)

```text
┌──────────────────────────────────────────────────────┐
│ Inicio › Platitos y bandejas                         │
├──────────────────────────────────────────────────────┤
│ PLATITOS Y BANDEJAS                         (H1)     │
│ 2 líneas: qué son, materiales, para qué sirven       │
├──────────────────────────────────────────────────────┤
│ Filtros: Forma ▾  Colección ▾  Precio ▾   Ordenar ▾  │
├──────────────────────────────────────────────────────┤
│ [foto]      [foto]      [foto]      [foto]           │
│ Flores      Vichy       Navidad     Caza             │
│ desde 8 €   desde 8 €   desde 8 €   desde 8 €        │
│                                                      │
│ [foto]      [foto]      [foto]      [foto]   ...     │
└──────────────────────────────────────────────────────┘
```

### Ficha de producto (escritorio)

```text
┌──────────────────────────────────────────────────────┐
│ Inicio › Platitos y bandejas › Flores                │
├──────────────────────────────────────────────────────┤
│ ┌──────────────┐  PLATITO FLORES          (H1)       │
│ │              │  desde 8 €                          │
│ │  FOTO GRANDE │                                     │
│ │  (se cambia  │  1. Forma                           │
│ │  al elegir)  │  (Redondo) (Cuadrado) (Rectangular) │
│ └──────────────┘  2. Estampado                       │
│ [mini][mini][mini] [o][o][o][o][o][o][o][o]          │
│                   3. Tamaño                          │
│                   (10 cm · 8 €) (15 cm · 15 €)       │
│                   4. Texto o iniciales (opcional)    │
│                   [______________]  máx. 10 letras   │
│                                                      │
│                   TOTAL: 15 €                        │
│                   [- 1 +]  [ AÑADIR A LA CESTA ]     │
│                   Hecho a mano · Envío 5-10 días     │
│                   ¿Dudas? Escríbenos por WhatsApp    │
├──────────────────────────────────────────────────────┤
│ [Descripción]  [Medidas y cuidados]  [Envíos]        │
├──────────────────────────────────────────────────────┤
│ TAMBIÉN TE PUEDE GUSTAR  [p]  [p]  [p]  [p]          │
└──────────────────────────────────────────────────────┘
```

### Ficha de producto (móvil)

```text
┌────────────────────────────┐
│ ≡     BY PETRA      Cesta  │
├────────────────────────────┤
│ [   FOTO PRODUCTO   ]      │
│   • • • (deslizar)         │
├────────────────────────────┤
│ PLATITO FLORES             │
│ desde 8 €                  │
├────────────────────────────┤
│ 1. Forma                   │
│ 2. Estampado               │
│ 3. Tamaño                  │
│ 4. Texto                   │
├────────────────────────────┤
│ Descripción ▾              │
│ Envíos ▾                   │
├────────────────────────────┤
│ [ AÑADIR · 15 € ]  ← fijo  │
└────────────────────────────┘
```

### Contacto

```text
┌──────────────────────────────────────────────────────┐
│ CONTACTO                                    (H1)     │
│ Respondemos en menos de 24 h                         │
├──────────────────────────────────────────────────────┤
│ Nombre    [______________]                           │
│ Email     [______________]                           │
│ Teléfono  [______________] (opcional)                │
│ Mensaje   [______________]                           │
│ [x] Acepto la política de privacidad                 │
│ [ ENVIAR ]                                           │
├──────────────────────────────────────────────────────┤
│ WhatsApp: 673 051 280 · bypetra20@gmail.com          │
│ Instagram @bypetra.deco · Taller en Barcelona        │
└──────────────────────────────────────────────────────┘
```

### Resto de páginas (una línea cada una)

- **Cómo funciona:** 3 pasos con foto + plazos + FAQ corta + botón "Ir a la tienda".
- **Sobre Petra:** foto de Petra y del taller, historia, valores (hecho a mano, Barcelona, regalo único).
- **Envíos y devoluciones:** tabla de plazos y precios por zona; aviso de que lo personalizado no se devuelve salvo defecto.
- **FAQ:** acordeón con las 8–10 preguntas que más llegan por WhatsApp.
- **Cesta / pago:** resumen con la personalización de cada producto visible antes de pagar.

## 3. Decisiones pendientes

1. ¿Venta online con pago (como ahora) o catálogo con pedido por WhatsApp?
2. Plataforma: rehacer en WordPress/WooCommerce limpio, pasar a Shopify, o web a medida.
3. Gastos de envío y si hay envío gratis a partir de cierto importe.
4. ¿Solo español o también inglés?
