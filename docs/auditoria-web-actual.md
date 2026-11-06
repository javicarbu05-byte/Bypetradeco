# Auditoría de la web actual by-petra.com

Fecha: 6 de noviembre de 2026. Método: rastreo con Chromium (Playwright) de las 173 URL del sitemap,
en escritorio (1440 px) y móvil (iPhone 13), con capturas, errores de consola, peticiones fallidas,
comprobación de todos los enlaces internos, SEO y peso de cada página.

**Límites:** desde el entorno de análisis no se podían cargar Instagram, Stripe (js.stripe.com) ni
Google Fonts, así que el feed de Instagram y el pago no se pudieron verificar. No se hizo ninguna
compra de prueba.

## Contexto técnico

- WordPress 6.3.14 + WooCommerce 8.3.4 (versiones de finales de 2023), tema OceanWP + Elementor.
- 14 plugins: elementor, header-footer-elementor, ocean-extra, ocean-modal-window,
  ocean-product-sharing, ocean-social-sharing, woocommerce, woocommerce-menu-bar-cart,
  woo-variation-gallery, woo-variation-swatches, yith-woocommerce-product-add-ons,
  instagram-feed, pixelyoursite (píxel de Facebook), creame-whatsapp-me (botón WhatsApp).
- Apache + PHP 8.2. HTTPS correcto y www redirige a la raíz.
- Contenido: 16 páginas, 45 productos, 22 categorías, 39 etiquetas, 38 páginas de atributos de color.
- Catálogo: platitos y bandejas (redondo/cuadrado/rectangular × 12 estampados), llaveros,
  chupeteros, neceseres, maletas, dibujos personalizados. Precios de 5 € a 64 €.
- Datos de contacto públicos: bypetra20@gmail.com, Instagram @bypetra.deco, Barcelona.

## 🔴 Errores críticos

1. **El email del pie de página no funciona.** En todas las páginas enlaza a
   `https://mail.google.com/mail/u/0/#inbox?compose=…`, una URL de la bandeja de Gmail de la
   dueña. A un cliente le abre su propio Gmail o una pantalla de error. Además genera un aviso de
   JavaScript en las 83 páginas. Solución: `mailto:bypetra20@gmail.com`.
2. **/contacto/ está rota.** Muestra el texto en bruto
   `[contact-form-7 id=»c0041ba» title=»Formulario de contacto 1″]` porque el plugin no está activo.
   Existe otra página, /contact/, con un formulario WPForms que sí funciona: páginas duplicadas.
3. **Enlaces que dan error 404:**
   - Inicio → `/producto/scottish-collection/`, `/producto/flowers-collection/`,
     `/producto/christmas-classic-combination/` (los bloques de colecciones de la portada).
   - /conjuntos-rectangular/ → `toile-de-jouy-rectangular`, `etnicos-rectangular`,
     `animal-print-rectangular`.
4. **La versión móvil está rota en las 83 páginas:** dos cabeceras superpuestas (el logo
   "BY PETRA" se pinta encima de "Maletas / Contacto"), dos menús, el pie de página duplicado,
   el email cortado y scroll horizontal (la página mide 495 px en una pantalla de 390 px).
5. **El configurador de producto confunde:** los pasos van 1, 2, 4, 5, 4 (no hay paso 3 y el 4 se
   repite), el tamaño se pide dos veces (paso 2 y paso 5) y aparece "10cm (8€) (+7,00€)", que
   contradice el precio mostrado. Afecta directamente a las ventas.
6. **Páginas vacías publicadas e indexables:** /blog/ ("Parece que no podemos encontrar lo que
   estás buscando"), /maletas/ (vacía), /neceseres/ (solo el título), /author/p20-deco/ y las
   plantillas internas `?oceanwp_library=footer-callout`, `?oceanwp_library=new-cabecera` y
   `/elementor-hf/pie-de-pagina/`, que aparecen en el sitemap.

## 🟠 Rendimiento

- Las tres páginas /conjuntos-* pesan **unos 30 MB cada una**: 140 imágenes JPG de 1024 px
  (~250–320 KB cada una) mostradas a 340 px. Tardaron 11–12 s en cargar.
- Fichas de producto entre 1,5 y 16 MB (Otoño cuadrado 15,8 MB), con 150–185 peticiones.
- Servidor lento: 1–4 s hasta el primer byte en productos; no hay caché de página.
- Sin WebP/AVIF. La portada pesa 2,2 MB para 3 fotos.

## 🟠 SEO

- **Ninguna página tiene meta description.**
- El H1 de todas las páginas es "BY PETRA" (el logo, repetido dos veces). Los productos no tienen
  su nombre como H1.
- Títulos duplicados: "FLORES", "VICHY", "CAZA"… se repiten en las versiones redondo, cuadrado y
  rectangular; las tres páginas de conjuntos se titulan "Platitos y Bandejas"; varios productos se
  llaman "¡PERSONALIZA TU PLATITO EN FONDO ESTAMPADO!". Los nombres son instrucciones en
  mayúsculas, no nombres de producto.
- Título de la portada genérico: "By-Petra – Decoración".
- Sin datos estructurados (schema Product) ni Open Graph: al compartir un enlace en WhatsApp o
  redes no sale imagen ni descripción.
- Alrededor del 60 % de las imágenes de producto no tienen texto alternativo (Flores redondo: 60 de 99).
- Idioma mezclado: "Cart", "My Account", "Contact", y en la portada "AUTUMN COLLECTION",
  "SCOTTISH COLLECTION", "FLOWERS COLLECTION", "CHRISTMAS CLASSIC".
- 39 páginas de etiquetas y 38 de colores indexables con contenido duplicado o escaso. Una
  etiqueta tiene una errata: `plantas-rectagular`.

## 🟠 Legal / RGPD (conviene que lo revise un profesional)

- Se carga el píxel de Facebook (PixelYourSite) y no hay ningún gestor de consentimiento de
  cookies. La política dice "quedando aceptado su uso al navegar", un consentimiento tácito que la
  AEPD no considera válido.
- La política de cookies parece copiada de otra web: menciona cookies de `notin.es` y de Twitter.
- La política de privacidad enlaza a `presencialismo.com` (otra empresa; textos de RRHH).
- El "Aviso legal" contiene en realidad las condiciones de venta. Falta separar aviso legal,
  condiciones de venta, envíos y devoluciones (sobre todo para productos personalizados).
- El pie de página dice "© By Petra 2021".

## 🟡 Técnico y seguridad

- WordPress y WooCommerce sin actualizar desde 2023, y la versión se muestra públicamente.
- El sitemap publica el nombre de usuario `p20-deco`, lo que facilita ataques al login.
- Plugins que se solapan (Elementor + Header Footer Elementor + librería OceanWP): esa es la causa
  de las cabeceras y pies duplicados.
- En fichas y carrito aparece el error "Stripe is not defined". En este entorno js.stripe.com
  estaba bloqueado, así que puede ser un falso positivo: hay que hacer una compra de prueba real.

## 🟡 Diseño, experiencia y conversión

- **Portada muy pobre:** tres fotos y "¡Síguenos en Instagram!". No explica qué es By Petra, ni que
  es hecho a mano y personalizado, ni muestra productos, precios o reseñas. Los bloques de
  colecciones enlazan a páginas 404.
- No hay página "Sobre nosotros" ni historia de Petra.
- Plazos de entrega (2–15 días laborables), envíos y devoluciones escondidos dentro del aviso legal.
- Navegación de platitos complicada: menú de tres niveles y cada forma (redondo/cuadrado/
  rectangular) es un producto distinto. Sería mejor un producto por estampado con la forma como opción.
- Tienda: tarjetas de alturas distintas, "Dibujos personalizados" sin precio, todo en mayúsculas.
- Texto gris muy claro y pequeño (contraste insuficiente). Pie con texto blanco sobre gris claro.

## ✅ Puntos fuertes que conservar

- Muy buena fotografía de producto y de ambiente (mesas puestas, bordados).
- Producto personalizable atractivo, con precios asequibles (5–64 €).
- Botón de WhatsApp y canal de Instagram activos.
- HTTPS correcto.
