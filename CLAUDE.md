# Bypetradeco — memoria del proyecto

## Objetivo
Crear una nueva web para la marca **By Petra** (by-petra.com): decoración y regalos personalizados
hechos a mano en Barcelona (platitos y bandejas estampados, llaveros, chupeteros, neceseres y
maletas bordados). Instagram: @bypetra.deco · Email: bypetra20@gmail.com.

## Estado
- 2026-11-06: repositorio vacío. Se auditó la web actual (WordPress + WooCommerce + Elementor).
  Informe completo en `docs/auditoria-web-actual.md`.
- 2026-11-06: propuesta de estructura y croquis en `docs/estructura-web.md` (pendiente de validar).
- 2026-11-06: croquis visual estilo dibujado a mano (para la tía/Petra): https://claude.ai/artifact/WBAQv9f7izM3wNeTLzdDiK
- 2026-11-06: PDFs para compartir: `docs/croquis-web-by-petra.pdf` y `docs/auditoria-web-by-petra.pdf`. Esperando feedback de la tía antes de los siguientes pasos.
- Decisiones abiertas: venta online o pedido por WhatsApp, plataforma, gastos de envío, idiomas.

## Lecciones de la auditoría que la nueva web debe resolver
- Móvil primero (la web actual se rompe en móvil).
- Imágenes optimizadas (WebP, tamaños responsive, lazy loading).
- SEO básico: H1 por página, meta description, Open Graph, schema Product, alt en imágenes.
- Todo en español (nada de "Cart", "Contact"...).
- Configurador de personalización claro: pasos numerados y sin repetir opciones.
- Un producto por estampado, con la forma (redondo/cuadrado/rectangular) como opción.
- Portada que explique la marca, con productos destacados; páginas "Sobre Petra" y "Envíos y devoluciones".
- Banner de cookies con consentimiento real antes de cargar el píxel de Facebook.
- Enlace de email con `mailto:`.

## Convenciones
- Idioma de trabajo con el usuario: español.
- Rama de desarrollo: `claude/exciting-knuth-8dpe1s`.
