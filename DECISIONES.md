# DECISIONES.md — design-styles-lab

## 2026-09-27 — Scaffold inicial (Fase 1+2 juntas)
- **Decisión:** galería web estática única (`index.html` + `styles.css`), sin build ni dependencias.
- **Por qué:** André aprobó los 10 estilos de una vez; un solo archivo HTML es lo más rápido de revisar y deployar. Skills de imagen (SD/fal) quedan para v2 si algún estilo necesita raster real.
- **Demos 100% offline:** CSS/SVG puro, fuentes del sistema. Cero picsum, cero CDNs → funciona sin internet y pesa KBs.
- **Dirección de diseño (skill frontend-design):** lenguaje de catálogo de especímenes — papel cálido, tinta, etiquetas mono, numeración 01–10 (justificada: es un catálogo, el orden es el índice).
- **Recetas:** skill design-styles-reference aportó técnicas concretas (riso: multiply+offset+grano; collage: clip-path+rotación; neón: text/box-shadow en capas; papel: ruido SVG; doodle: border-radius wobbly).
- **Repo:** `andregil003/design-styles-lab`, público, MIT.
## 2026-09-27 — Estilo 01 Sticker Bomb ×15
- **Decisión:** página dedicada `styles/01-sticker-bomb.html` + `styles/01-sticker-bomb.css` (7 acabados + 7 superficies + 1 switcher interactivo con JS mínimo).
- **Por qué:** investigación en línea (artstyles, stickerapp, youstickers 2026): el acabado (holo/chrome/glitter/transparente/glow) y la superficie son las dos variables reales del estilo. El switcher mate/holo/chrome/glitter es la pieza estrella para la futura skill.
- **Patrón a repetir en estilos 02–10:** `styles/NN-nombre.html` + `styles/NN-nombre.css` + link desde la tarjeta del index.
## 2026-09-27 — Estilo 02 Technical X-Ray ×15
- **Decisión:** `styles/02-technical-xray.html` + `.css` (7 sujetos + 7 contextos + 1 Scan Layers interactivo piel/músculo/hueso/circuito).
- **Por qué:** el estilo vive de dos variables: QUÉ se escanea × DÓNDE se presenta. El interactivo de capas es la pieza estrella para la skill.
## 2026-09-27 — Estilo 03 Cross-Stitch ×15
- **Decisión:** `styles/03-cross-stitch.html` + `.css` (5 puntadas + 5 soportes + 4 letras + Stitch Lab interactivo letra×puntada).
- **Por qué:** truco CSS = glyph sólido + gemelo con `-webkit-text-stroke: dashed` desplazado = puntada. Conecta con `myCoolFont` (una variante bordada de fuente es viable).
## 2026-09-27 — Estilo 04 Watercolor ×15
- **Decisión:** `styles/04-watercolor.html` + `.css` (5 técnicas + 5 sujetos + 4 contextos + mini lienzo canvas para pintar con dedo/mouse).
- **Por qué:** el estilo se vende por imperfección: bordes wobbly (border-radius truco), crayón (SVG round caps) y papel siempre visible. El canvas interactivo es la pieza estrella.
## 2026-09-27 — Estilo 05 Aura ×15
- **Decisión:** `styles/05-aura.html` + `.css` (7 paletas + 7 aplicaciones + generador con paleta/blur/grano).
- **Por qué:** el aura se vende por contexto: la misma técnica en wallpaper, login o packaging cambia el valor. El generador es la pieza estrella (prototipo de fondos de marca).
## 2026-09-27 — Estilos 06–10 ×15 (lote final, sin interrupciones a pedido de André)
- **06 Radial:** `styles/06-radial.html` (5 huecos + 5 órbitas + 4 contextos + ruleta giratoria). Truco: fragmentos posicionados por ángulo `--a` con `rotate(a) translateX() rotate(-a)`.
- **07 Specimen:** `styles/07-specimen.html` (5 especímenes + 5 placas + 4 detalles + placa viva latín↔común). SVG minimal + Georgia itálica.
- **08 Riso:** `styles/08-riso.html` (5 combos de tinta + 5 sujetos + 4 contextos + lab de desregistro con slider). Clase `ink-X` cambia el par de tintas.
- **09 Spectral:** `styles/09-spectral.html` (5 sujetos + 5 colores + 4 aplicaciones + mezclador hue×intensidad con JS que pinta el glow).
- **10 Flat:** `styles/10-flat.html` (5 marcas + 5 piezas + 4 paletas + tablero con switcher). Cero degradados en demos (solo fotos ninguna).
- **Pendiente:** skill `design-styles-lab`, deploy público.
