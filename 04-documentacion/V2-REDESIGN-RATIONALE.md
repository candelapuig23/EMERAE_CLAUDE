# V2-REDESIGN-RATIONALE.md — Propuesta de rediseño "Corte transversal"

Documenta la propuesta de rediseño completo de la Home, generada con el flujo `new work` de Impeccable y aprobada por el usuario antes de su implementación. Entregable: `01-secciones-trabajo/0-home-emerae-v2-redesign.json`.

**Nota sobre herramientas:** este entorno no tenía Node.js disponible, por lo que los scripts del skill (`context.mjs`, `concept-seed.mjs`, `serve-question.mjs`) no pudieron ejecutarse. Se reconstruyó manualmente su función: lectura completa de `PRODUCT.md`, `DESIGN.md`, `INVENTARIO.md`, `PROJECT-STATUS.md`, `WORKFLOW.md`, `HANDOFF.md` y del contenido íntegro de `0-home-emerae-v1.json`; y en vez del reparto aleatorio de dirección creativa, se presentaron al usuario una dirección principal razonada más dos alternativas nombradas, de forma que la elección siguiera siendo real y no un valor por defecto del modelo.

## 1. Concepto creativo

**"El corte transversal."** El diferenciador de marca confirmado en `PRODUCT.md` es trabajar la raíz y la función de la adicción (protege, anestesia, evita), no solo el cese del consumo — un lenguaje ya botánico en el propio léxico de marca (*raíz, herida, sostener, recuperar*). La home original y la v1 dicen esto con palabras pero lo diseñan con la gramática genérica de cualquier landing: pastilla-eyebrow + título + N cajas, repetida en 7 de las 13 secciones.

La propuesta trata cada sección como un corte transversal: muestra una cosa real (una raíz, un camino, una carta, una línea de medida) una sola vez, con precisión, con líneas de anotación finas y etiquetas impresas que señalan sus partes — nunca una rejilla de tarjetas que sustituye a la cosa por un icono.

Deliberadamente **no** es un cuaderno vintage cálido (papel crema, texturas kraft, tono nostálgico) — esa es la deriva más común de cualquier dirección "editorial/cuaderno" y el propio proceso de Impeccable la señala como el sesgo por defecto de un modelo de IA. Se mantiene fría y clínica: Deep Navy, Clinical Blue, Morning Mist, blanco y grises — registro de lámina de herbario o plano de laboratorio, no de diario de viaje.

**Alternativas presentadas y no elegidas:** "El plano" (lenguaje de plano arquitectónico, ya que Emerae es un lugar físico real en Barcelona) y "La señalética" (sistema de wayfinding/andén con paradas numeradas). El usuario aprobó explícitamente "Corte transversal".

## 2. Nueva narrativa visual

- **Sustituye la pastilla-eyebrow repetida** por una anotación de línea + etiqueta (hairline de 1px + texto Inter en mayúsculas) en las 7 secciones que antes la usaban (Enfoque, Tratamiento, Qué tratamos, Por qué Emerae, Equipo, Familias, FAQ). La pastilla de 100px se conserva únicamente para controles interactivos reales (botones, tabs, tags de metodología), tal y como ya prescribe `DESIGN.md`.
- **Ningún patrón de "rejilla de tarjetas" nuevo.** Donde v1 ya usaba listas con separador (Enfoque, Tratamiento, Por qué Emerae) se conservó ese criterio y se reforzó con numeración/orden. Donde v1 sí usaba una rejilla de celdas iguales (Qué tratamos: 14 celdas en grid 2 columnas), se sustituyó por un listado ramificado con línea-tronco (`.ev2-branch`).
- **El tono claro varía entre secciones** (Pale Dawn → Blanco → Quiet Gray → Blanco → [Navy] → Pale Dawn → Blanco → Blanco → Quiet Gray → Blanco → Quiet Gray → Quiet Gray → [Navy]) en vez de repetir blanco de forma mecánica, manteniendo intacta la Two-Surface Rule de `DESIGN.md` (una sección es clara u oscura, nunca mezclada).
- **Dos motivos de "línea de medida" bookendan la home**: Confianza (arriba) presenta las cifras como marcas sobre una regla; Contacto (abajo) cierra con los 3 CTA como paradas sobre la misma gramática de línea. Es una rima estructural, no decorativa.
- **Instrument Serif itálica se mantiene exactamente donde `DESIGN.md` ya la reserva** (titulares emocionales, citas) — no se añade en ningún sitio nuevo ni se usa para UI funcional.

## 3. Cambios por sección

| Sección | Cambio principal | Qué se conserva sin tocar |
|---|---|---|
| Hero | De selector centrado en pastillas a un "cruce de caminos": titular asimétrico a la izquierda, bifurcación de 3 ramas a la derecha (mismo mecanismo JS de 2 niveles, re-skinado) | Los 2 titulares, el párrafo, los 9 paneles de contenido (todavía "por definir" donde v1 ya lo resolvió), la línea de cierre "Primera consulta gratuita · Sin compromiso · Confidencial" |
| Confianza | De 3 columnas con separador a marcas sobre una línea de medida (regla) | Las 3 cifras, la nota de verificación pendiente del "+25" |
| Manifiesto | Se mantiene deliberadamente mínima (un único titular itálico) — cambia solo el tono de fondo para no repetir blanco | El titular completo con sus `<span>` de énfasis |
| Enfoque | La lista de 3 beneficios pasa a notas numeradas (01/02/03) en el margen | Imagen real, cita superpuesta, párrafos, pull-quote, botón |
| Tratamiento | Los 3 ítems inferiores pasan de grid a "camino de proceso" (línea con 3 paradas) | Badge→anotación, titular, párrafo, tags de metodología, botón, caja de acreditación |
| Enfermedad del alma | Sin cambio estructural — se mantiene mínima por ser contenido explícitamente provisional; solo cambia el tono de fondo | Los 2 párrafos y la nota "pendiente del texto original de Esmeralda" |
| Qué tratamos | La rejilla de 14 celdas iguales pasa a un listado ramificado con línea-tronco (mismo tablist accesible, misma navegación por teclado) | Los 3 tabs, los 14 ítems (nombre+descripción+enlace), el panel de patología dual |
| Por qué Emerae | Badge→anotación; el resto ya era lista, se conserva | Historia de origen, 4 valores, nota de listado provisional, franja de historia |
| Equipo | De grid de tarjetas a "fichas de campo" lado a lado con etiqueta tipo especimen | Las 2 fichas exactas (Paula real + ficha pendiente), cita de cierre |
| Familias | Cambio mínimo (badge oscuro→anotación oscura); la composición imagen+cita+tarjeta ya era distintiva | Imagen real, cita de Paula, los 3 párrafos, CTA de familia, botón |
| Testimonios | De 3 tarjetas discontinuas en grid a 3 entradas de cuaderno en columna única, numeradas | Los 3 textos "PENDIENTE — NO PUBLICAR" exactos |
| FAQ | El acordeón deja de ser tarjetas blancas con sombra y pasa a una lista plana con separadores finos | Las 6 preguntas y respuestas completas, mecanismo de apertura única |
| Contacto | La fila de CTA pasa a "paradas sobre una línea" que rima con Confianza; el CTA principal es visualmente más pesado que los 2 pendientes | Los 3 CTA exactos (consulta gratuita, llamar, WhatsApp) y sus placeholders `PENDIENTE — NO PUBLICAR` |

## 4. Decisiones responsive

- Mobile-first en cada dispositivo nuevo: el "cruce de caminos" del Hero se apila verticalmente y conserva la jerarquía (rama → subramas → panel) sin perder la interacción.
- El listado ramificado de Qué tratamos usa `column-count:2` en escritorio/tablet y `column-count:1` en móvil (breakpoint 767px), evitando desbordamiento horizontal.
- La línea de medida de Confianza cambia de marcas horizontales a una lista vertical con tick a la izquierda en móvil, en vez de forzar 3 columnas apretadas.
- El "camino de proceso" de Tratamiento pasa de 3 columnas con separador vertical a una columna con separador izquierdo en tablet/móvil (breakpoint 1023px).
- Todos los botones y elementos interactivos mantienen `min-height:44px` para área táctil.
- Se respeta `@media (prefers-reduced-motion: reduce)` en cada widget con transición (Hero, Qué tratamos, FAQ), desactivando transiciones no esenciales.
- No se han añadido carruseles ni acordeones nuevos; el único acordeón (FAQ) y los dos mecanismos de pestañas/selector (Hero, Qué tratamos) ya existían en v1 y se conservan por ser funcionalmente necesarios.

## 5. Interacciones

Los 3 mecanismos JS de v1 se reimplementan con la misma lógica exacta (guardas de inicialización idempotentes, manejo de teclado en tabs, un solo ítem abierto a la vez en FAQ) bajo nuevos nombres de clase (`ev2-*`) para evitar colisión si ambas versiones llegaran a convivir en una misma página de pruebas de Elementor. Ningún `onclick` ni referencia cruzada se ha roto: los IDs referenciados por `aria-controls` / `getElementById` coinciden exactamente entre el HTML y el script de cada widget.

## 6. Recursos pendientes (sin inventar nada)

Igual que en v1, se mantienen explícitamente sin resolver — y visualmente honestos, no disfrazados:
- Contenido real de los 9 paneles del selector del Hero.
- Cifra de años de experiencia (`+25`) pendiente de verificación documental.
- Texto original de Esmeralda para la sección "Enfermedad del alma".
- 5/6 fichas de equipo (nombres, cargos, fotos) — la ficha placeholder usa un contorno sin completar, no una foto-silueta disfrazada de foto real.
- 3 testimonios reales (pacientes/familiares) — ninguno inventado.
- Teléfono y WhatsApp reales en Contacto.
- Todos los `href="#"` de las tarjetas de Qué tratamos, del enlace de patología dual y del enlace "Conocer nuestra historia".

## 7. Validaciones efectuadas

- **Sintaxis JSON**: parseo correcto con `ConvertFrom-Json` (PowerShell) tras cada sección añadida y en el archivo final completo (13/13 secciones).
- **IDs únicos**: 95 elementos en el árbol completo, 0 duplicados (verificado programáticamente).
- **Balance de HTML embebido**: 3/3 pares `<script>`/`</script>`, 28/28 pares `<style>`/`</style>`.
- **Paridad de contenido**: los 13 titulares (`title`) coinciden carácter a carácter con los de la v1; recuento de `PENDIENTE` (6), `href='#'` (19) y `aria-controls` (9) coincide con lo esperado a partir del inventario de contenido de la v1.
- **Codificación**: sin evidencia de corrupción de acentos (0 coincidencias de secuencias mal codificadas).
- **Pendiente de validar por el usuario** (fuera del alcance de este entorno, según `CLAUDE.md` punto 8 y `WORKFLOW.md` pasos 11-13): importación manual en Elementor y revisión visual en escritorio, tablet y móvil. Un JSON sintácticamente válido no garantiza el resultado visual correcto.

## 8. Diferencias relevantes respecto a la v1

- Ningún texto, cifra, enlace o dato de contacto se ha alterado: la v1 sigue siendo la fuente de verdad de contenido y esta propuesta es una reinterpretación puramente compositiva.
- No se ha migrado ninguna sección entre `section`/`column` y `container`: todas las secciones nuevas usan `container` (flexbox), igual que hacía ya la v1 completa (la v1, a diferencia de `00-originales`, había unificado las 13 secciones bajo `container`).
- Los 3 mecanismos interactivos (selector del Hero, tabs de Qué tratamos, acordeón FAQ) se conservan funcionalmente idénticos; solo cambia su piel visual.
- El archivo `0-home-emerae-v1.json` no se ha modificado, sobrescrito ni movido en ningún momento.
