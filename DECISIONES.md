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
## 2026-09-27 — Estilos 11–15 ×15 (segunda temporada, deep dive de scouts en skills)
- **11 Brutalist:** `styles/11-brutalist.*` (kit + contextos + detalles + switch Swiss↔Terminal que repinta el body por `data-mode`).
- **12 Minimal:** `styles/12-minimal.*` (silencios + piezas + reglas + switch de densidad; cero sombras/gradientes).
- **13 Dark Luxe:** `styles/13-darkluxe.*` (superficies + componentes + piezas SaaS + switcher de acento por variable).
- **14 Pixel:** `styles/14-pixel.*` (sprites box-shadow + UI arcade + efectos CRT + maquinita de monedas con contador).
- **15 Flow:** `styles/15-flow.*` (un motor canvas de ~40 líneas, 15 configs por `data-*`; lab con sliders; rAF cancelable).
- **Index:** 5 tarjetas nuevas (11–15) + TOC + título actualizados.
- **Pendiente:** skill `design-styles-lab`, deploy público.
## 2026-09-30 — Estilo 16 Trending Effects ×2
- **Decisión:** `styles/16-trending-effects.html` + `.css` (thermal FLIR con switch low/mid/high + CRT fósforo con power on/off). Prompts re-redactados propios, foco preservado; imágenes del Notion no copiadas.
- **Por qué:** caza hunterPuck de página Notion "Trending EFFECTS prompts" (2 efectos). Son edit-prompts, no estilos de catálogo ×15 — se publican como par simple honesto, sin inflar a 15. Smoke de `fal-ai-image --help` OK; generación real pendiente (sin FAL_KEY).
## 2026-09-30 — Estilo 17 Estilos para IA ×13 (nombre general, sin "reel")
- **Decisión:** `styles/17-estilos-ia.html` + `.css` (port de la skill: 13 tarjetas con demo + prompt + paleta, CSS separado, header/toc/footer del repo). Sin la palabra "reel" en ningún lado: es un catálogo general de recetas para IA.
- **Por qué:** la skill ya tenía este contenido y el repo no — se sincronizan para que la galería pública y la skill no diverjan.
- **Joya:** filtro por ambiente (todos/neón/oscuro/claro/retro) con `data-mood` + acento de color por tarjeta, números 01–13, hover lift. Detalle extra por demo: grano VHS en dreamcore, ojo vigilante en dark fantasy, estrellas en candy, "Nº 001" en toy, ticker en punk.
## 2026-09-30 — Rewrite total 16+17 (borrón y cuenta nueva, pedido de André)
- **Decisión:** 16 pasa de ×2 a ×8 (retrato + paisaje + escala + HUD conmutable + terminal + scan-lab con sliders + apagado CRT con colapso + estática animada). 17 suma filtro + detalles por demo. Se borran `17-reel-parte4.*` (renombre general).
- **Por qué:** la primera versión se veía barata y vaga. Más densidad, más controles reales, mismos prompts (André los aprobó) y misma regla offline.
## 2026-09-30 — +10 y +10 (pedido de André: más de lo mismo, pero bueno)
- **16 → ×18:** T5 multitud (3 firmas), T6 motor (núcleo pulsante), T7 termómetro, T8 huellas que se enfrían, T9 visor dron FPV; C5 BIOS POST, C6 reloj con hora viva (JS), C7 ecualizador 12 barras, C8 insert coin, C9 radar con barrido.
- **17 → ×23:** vaporwave, memphis, cyber calle, holográfico (hue-rotate), noir, kawaii, glitch RGB-split, origami, blueprint, cottage. Filtros existentes los cubren (moods ya definidos).
## 2026-09-30 — Dedup 16 (×18→×14, pedido de André: quitar lo que se repite)
- **Fuera 4:** T4 HUD táctico (se pisaba con T9 visor dron) · C2 scan-lab (scanlines ya en 14-pixel) · C5 BIOS (misma pantalla mono que C1 terminal, que guarda el prompt) · C8 insert coin (arcade ya en 14-pixel).
- **Renumerado 01–14** sin huecos; CSS/JS muertos eliminados (t-hudex, c-lab, c-coin, c-bios + handlers). Quedan 3 joyas: heat, apagado CRT, reloj vivo.
