# INVENTARIO.md — Análisis técnico verificado de la home Emerae

Este documento traslada el análisis verificado de los 15 JSON de `00-originales` (1 home completa + 14 secciones individuales). Es documentación de referencia: no debe usarse como sustituto de la lectura del JSON original antes de modificar una sección, sino como mapa de orientación rápida.

Fuente: `00-originales/0-home_completa.json` y `00-originales/01-hero_emerae.json` … `13-cta_final.json`. Analizado y verificado el 23/07/2026.

---

## Resumen de la home

- **Total de archivos:** 15 (1 home completa + 14 secciones individuales).
- **Orden de las secciones dentro de la home:** Hero → Stats → Citas → Enfoque → Tratamiento → CTA intermedio → Adicciones → Por qué Emerae → Equipo → Familias → Testimonios → Logros → FAQ → CTA final.
- **Estructuras raíz mixtas:** 6 secciones usan `section`/`column` (legacy) y 8 usan `container` (flexbox moderno de Elementor).
- **Patrón dominante:** casi todo el diseño visual (tarjetas, carruseles, acordeones, selectores, animaciones) está implementado mediante widgets `html` con `<style>`/`<script>` embebidos e inline styles, no mediante controles nativos de Elementor.

---

## 1. Hero

- **Archivo:** `01-hero_emerae.json`
- **Objetivo:** presentación inicial de la home y segmentación de la intención del visitante (para mí / para alguien / soy profesional).
- **ID raíz:** `7dcdbd4a`
- **Estructura:** `container` (flexbox)
- **Widgets utilizados:** `html` (3), `heading` (1), `text-editor` (2)
- **HTML/CSS/JS personalizado:** 1 widget HTML con `<style>` embebido y `<script>` con funciones `emSelectL1` y `emSelectL2` que controlan un selector interactivo de 2 niveles + 9 paneles de contenido.
- **Animaciones/interacciones:** JS de navegación por niveles (toggle de clases `.active` / `.visible`); sin `@keyframes` CSS.
- **Responsive detectado:** sin claves responsive nativas de Elementor (`_tablet`/`_mobile`); el H1 usa tipografía fluida en `vw`.
- **Imágenes/recursos externos:** ninguno.
- **Enlaces/contenido pendiente:** los 9 paneles del selector contienen el texto placeholder `"Contenido por definir en la siguiente fase."`.
- **Riesgos técnicos:** toda la interacción depende de un único widget HTML autocontenido; editar o eliminar el `<script>` rompe la funcionalidad completa del selector.

---

## 2. Stats

- **Archivo:** `02-stats.json`
- **Objetivo:** prueba social rápida mediante cifras clave.
- **ID raíz:** `5ee6455b`
- **Estructura:** `section`/`column` (legacy)
- **Widgets utilizados:** `html` (1)
- **HTML/CSS/JS personalizado:** un único widget HTML con grid CSS inline (3 columnas: +25 años, 100% acreditados, BCN).
- **Animaciones/interacciones:** ninguna.
- **Responsive detectado:** sin claves responsive nativas; grid fijo `repeat(3,1fr)` sin media query propio.
- **Imágenes/recursos externos:** ninguno.
- **Enlaces/contenido pendiente:** ninguno detectado.
- **Riesgos técnicos:** sección muy simple pero 100% dependiente de un solo widget HTML sin fallback responsive propio.

---

## 3. Citas flotantes

- **Archivo:** `02.2-citas.json`
- **Objetivo:** refuerzo emocional mediante citas breves flotantes alrededor de una frase central.
- **ID raíz:** `6b72f10c`
- **Estructura:** `section`/`column` (legacy)
- **Widgets utilizados:** `html` (1)
- **HTML/CSS/JS personalizado:** 1 widget HTML con `<style>` embebido; 4 citas posicionadas de forma absoluta + frase central.
- **Animaciones/interacciones:** 4 animaciones CSS de flotación (`@keyframes floatA`, `floatB`, `floatC`, `floatD`).
- **Responsive detectado:** **única sección (junto a FAQ) con `@media` propio** — `@media(max-width:768px)` oculta las citas flotantes en móvil y ajusta el padding.
- **Imágenes/recursos externos:** ninguno.
- **Enlaces/contenido pendiente:** ninguno detectado.
- **Riesgos técnicos:** animaciones y posicionamiento absoluto acoplados al `min-height` del contenedor; cambios en la longitud del texto pueden romper el layout flotante.

---

## 4. Enfoque

- **Archivo:** `03-enfoque.json`
- **Objetivo:** explicar el enfoque terapéutico ("la adicción no es falta de voluntad").
- **ID raíz:** `5173fdd7`
- **Estructura:** `section`/`column` (legacy), 2 columnas 50/50
- **Widgets utilizados:** `image` (1), `html` (4), `heading` (1), `text-editor` (1), `button` (1)
- **HTML/CSS/JS personalizado:** 3 widgets HTML (badge, cita superpuesta a la imagen, 3 tarjetas de beneficios).
- **Animaciones/interacciones:** ninguna.
- **Responsive detectado:** sin claves responsive nativas; columnas 50/50 fijas.
- **Imágenes/recursos externos:** 1 imagen real — `https://centroemerae.com/wp-content/uploads/2026/07/ChatGPT-Image-3-jul-2026-18_06_21.png`.
- **Enlaces/contenido pendiente:** botón "Ver cómo trabajamos →" enlaza a `#tratamiento` (ancla interna, válida si existe ese ID en la página publicada).
- **Riesgos técnicos:** la cita superpuesta usa `margin-top:-60px` sobre la imagen; frágil ante cambios de alto de imagen o de breakpoint.

---

## 5. Tratamiento

- **Archivo:** `04-tratamiento.json`
- **Objetivo:** detallar el método de trabajo clínico.
- **ID raíz:** `59a567ec`
- **Estructura:** `section`/`column` (legacy), con 2 sub-secciones anidadas (`isInner: true`)
- **Widgets utilizados:** `html` (2), `heading` (7), `button` (1), `text-editor` (5)
- **HTML/CSS/JS personalizado:** 2 widgets HTML (badge, tags de metodologías: TCC, EMDR, Regulación emocional).
- **Animaciones/interacciones:** ninguna.
- **Responsive detectado:** sin claves responsive nativas; H2 con tipografía fluida en `vw`.
- **Imágenes/recursos externos:** ninguno.
- **Enlaces/contenido pendiente:** botón "Primera consulta gratuita →" enlaza a `#contacto` (ancla interna).
- **Riesgos técnicos:** estructura anidada (`section` dentro de `section`) con varios widgets `heading` usados solo como números decorativos ("01", "02", "03"); frágil si se reordenan las tarjetas.

---

## 6. CTA intermedio

- **Archivo:** `05-cta_intermedio.json`
- **Objetivo:** invitar al primer contacto (llamada, WhatsApp, consulta gratuita).
- **ID raíz:** `2d2824c3`
- **Estructura:** `section`/`column` (legacy), con sub-sección anidada
- **Widgets utilizados:** `image` (1), `html` (2), `heading` (1), `text-editor` (1)
- **HTML/CSS/JS personalizado:** 1 widget HTML con las 3 tarjetas de contacto en `<a>`.
- **Animaciones/interacciones:** ninguna.
- **Responsive detectado:** sin claves responsive nativas.
- **Imágenes/recursos externos:** 1 imagen real — `https://centroemerae.com/wp-content/uploads/2026/07/republica-man-792821-scaled-e1783356750284.jpg`.
- **Enlaces/contenido pendiente:** **teléfono y WhatsApp con placeholder** — `tel:+34000000000` y `https://wa.me/34000000000`.
- **Riesgos técnicos:** datos de contacto ficticios; si se publica sin corregir, los CTAs de llamada y WhatsApp no funcionan.

---

## 7. Adicciones

- **Archivo:** `06-adicciones.json`
- **Objetivo:** listar qué se trata (sustancias, comportamentales, patología dual).
- **ID raíz:** `520b0ebf`
- **Estructura:** `section`/`column` (legacy)
- **Widgets utilizados:** `html` (3), `heading` (1), `text-editor` (1)
- **HTML/CSS/JS personalizado:** 2 widgets HTML — uno con botones de pestañas y `<script>` (función `showTab`), otro con `<style>` y las tarjetas de cada categoría.
- **Animaciones/interacciones:** JS de cambio de panel visible según pestaña activa (`showTab`).
- **Responsive detectado:** sin claves responsive nativas; grid de tarjetas `repeat(2,1fr)` fijo.
- **Imágenes/recursos externos:** ninguno.
- **Enlaces/contenido pendiente:** **todas las tarjetas de adicción enlazan a `href="#"`** (Alcohol, Cocaína, Cannabis, Opioides, MDMA, Chemsex, Tabaco, Otras drogas, Juego, Pornografía, Internet, Videojuegos, Compras, Comida); el enlace "Saber más sobre patología dual →" también apunta a `#`.
- **Riesgos técnicos:** la lógica JS y los IDs de datos (`tab-X` / `panel-X` / `desc-X`) están fuertemente acoplados por nombre; renombrar categorías sin actualizar el script rompe la interacción.

---

## 8. Por qué Emerae

- **Archivo:** `07-porque.json`
- **Objetivo:** argumentar diferenciación y credibilidad del centro.
- **ID raíz:** `522d96ba`
- **Estructura:** `container` (flexbox), 2 columnas 50/50
- **Widgets utilizados:** `html` (4), `heading` (1), `text-editor` (2)
- **HTML/CSS/JS personalizado:** 3 widgets HTML (caja de acreditación destacada, lista de 4 valores numerados).
- **Animaciones/interacciones:** ninguna.
- **Responsive detectado:** sin claves responsive nativas; columnas con `width:50%` fijo.
- **Imágenes/recursos externos:** ninguno.
- **Enlaces/contenido pendiente:** ninguno detectado.
- **Riesgos técnicos:** el título usa HTML embebido (`<span style="color:...">`) dentro del propio campo `title` del widget `heading`, no es texto plano.

---

## 9. Equipo

- **Archivo:** `08-equipo.json`
- **Objetivo:** presentar al equipo profesional.
- **ID raíz:** `74f09434`
- **Estructura:** `container` (flexbox)
- **Widgets utilizados:** `html` (3), `heading` (1), `text-editor` (1)
- **HTML/CSS/JS personalizado:** 1 widget HTML grande con `<style>` (incluye `@import` de Google Fonts "Inter") y carrusel (`<script>` con funciones `eqUpdate`, `eqNext`, `eqPrev`, `eqGoTo`).
- **Animaciones/interacciones:** carrusel JS con `transform` + dots de navegación; sin `@keyframes` CSS.
- **Responsive detectado:** sin claves responsive nativas; el carrusel calcula el ancho de tarjeta en JS vía `offsetWidth`, no mediante media query.
- **Imágenes/recursos externos:** ninguno (las "fotos" del equipo son siluetas CSS decorativas, no imágenes reales).
- **Enlaces/contenido pendiente:** **5 de 6 perfiles son placeholder `"Nombre Apellido"`** (solo Paula Ferrer tiene datos reales); además, el carrusel define `eqPages=3` en el script pese a tener 6 tarjetas, lo que sugiere una paginación de dots incompleta respecto al contenido real.
- **Riesgos técnicos:** `@import` de Google Fonts duplicado respecto a otras secciones (ver Testimonios); el cálculo de ancho vía `offsetWidth` es sensible al momento de carga/render (FOUC).

---

## 10. Familias

- **Archivo:** `09-familias.json`
- **Objetivo:** dirigirse específicamente a familiares de la persona con adicción.
- **ID raíz:** `23f668bd`
- **Estructura:** `container` (flexbox), split imagen/texto sobre fondo oscuro
- **Widgets utilizados:** `html` (3), `heading` (1), `text-editor` (2), `button` (1)
- **HTML/CSS/JS personalizado:** 1 widget HTML (cita de la directora superpuesta a la imagen con gradiente).
- **Animaciones/interacciones:** ninguna.
- **Responsive detectado:** sin claves responsive nativas; anchos en `%` fijos (44%/50%).
- **Imágenes/recursos externos:** 1 imagen real — `https://centroemerae.com/wp-content/uploads/2026/07/going-walk-seaside-winter-scaled-e1783151065925-1.jpg`.
- **Enlaces/contenido pendiente:** botón "Información para familias →" enlaza a `#` (sin destino real).
- **Riesgos técnicos:** `custom_css` fuerza `overflow:hidden`; contenedor con `min_height` fijo (580px) que puede recortar contenido en pantallas pequeñas.

---

## 11. Testimonios

- **Archivo:** `10-testimonios.json`
- **Objetivo:** mostrar experiencias reales de pacientes y familiares (prueba social cualitativa).
- **ID raíz:** `4ea25265`
- **Estructura:** `container` (flexbox)
- **Widgets utilizados:** `html` (2), `heading` (1)
- **HTML/CSS/JS personalizado:** 1 widget HTML grande con `<style>` (`@import` de Google Fonts) y carrusel (`<script>` con funciones `tmUpdate`, `tmNext`, `tmPrev`, `tmGoTo`).
- **Animaciones/interacciones:** carrusel JS con `transform` + dots, mismo patrón que la sección Equipo.
- **Responsive detectado:** sin claves responsive nativas.
- **Imágenes/recursos externos:** ninguno.
- **Enlaces/contenido pendiente:** **2 de 5 testimonios son placeholder** — `"Testimonio placeholder — reemplazar con testimonio real de Paula."`; el script define `tmPages=3` pese a haber 5 tarjetas, mismo posible desajuste de paginación que en Equipo.
- **Riesgos técnicos:** el carrusel duplica prácticamente el mismo código JS/CSS que el de la sección Equipo (oportunidad de reutilización a valorar en el futuro, sin tocar ahora); el número de dots (3) no coincide con el número real de tarjetas (5).

---

## 12. Logros

- **Archivo:** `11-logros.json`
- **Objetivo:** reforzar trayectoria y confianza mediante cifras (segunda sección de cifras, tras Stats).
- **ID raíz:** `58bab07b`
- **Estructura:** `section`/`column` (legacy), con sub-sección anidada de 3 columnas
- **Widgets utilizados:** `html` (1), `heading` (4), `text-editor` (4)
- **HTML/CSS/JS personalizado:** un pequeño widget HTML de badge; el resto son widgets nativos.
- **Animaciones/interacciones:** ninguna.
- **Responsive detectado:** sin claves responsive nativas.
- **Imágenes/recursos externos:** ninguno.
- **Enlaces/contenido pendiente:** ninguno detectado.
- **Riesgos técnicos:** no es un riesgo técnico sino de contenido — esta sección es muy similar/redundante con Stats (#2): cifras casi idénticas (+25 vs +20 años, 100%, BCN). No requiere corrección técnica, pero es una duplicidad editorial a valorar más adelante.

---

## 13. FAQ

- **Archivo:** `12-faq.json`
- **Objetivo:** resolver dudas frecuentes de los visitantes.
- **ID raíz:** `405ebcab`
- **Estructura:** `container` (flexbox)
- **Widgets utilizados:** `html` (2), `heading` (1), `text-editor` (1), `button` (1)
- **HTML/CSS/JS personalizado:** 1 widget HTML grande con acordeón (`<style>` + `<script>` con función `toggleFaq`).
- **Animaciones/interacciones:** JS de apertura/cierre del acordeón (clase `.open`, transición de `max-height`).
- **Responsive detectado:** **única sección junto con Hero que declara claves responsive nativas de Elementor** — `boxed_width_tablet` y `boxed_width_mobile`, ambas presentes pero sin valor definido (`size: ""`), es decir, declaradas pero no resueltas.
- **Imágenes/recursos externos:** ninguno.
- **Enlaces/contenido pendiente:** botón "Haznos una pregunta →" enlaza a `#` (sin destino real).
- **Riesgos técnicos:** `custom_css` inyecta un fondo SVG en base64 con el texto "FAQ" y fuerza `height:600px` fijo en el contenedor; si el acordeón creciera en contenido podría recortarse (aunque el script solo permite un ítem abierto a la vez, mitigando el riesgo).

---

## 14. CTA final

- **Archivo:** `13-cta_final.json`
- **Objetivo:** cierre de página con llamada a la acción final.
- **ID raíz:** `245d6380`
- **Estructura:** `container` (flexbox)
- **Widgets utilizados:** `html` (4), `heading` (1), `text-editor` (3)
- **HTML/CSS/JS personalizado:** 2 widgets HTML decorativos (glows radiales de fondo) + 1 widget HTML con los 3 CTAs finales y los datos de contacto.
- **Animaciones/interacciones:** ninguna.
- **Responsive detectado:** sin claves responsive nativas.
- **Imágenes/recursos externos:** ninguno.
- **Enlaces/contenido pendiente:** **los 3 CTAs finales** ("Pedir primera consulta gratuita →", "Llámanos", "WhatsApp") **enlazan a `href="#"`**, sin número de teléfono ni link de WhatsApp reales (a diferencia de la sección 6, que sí incluía placeholders numéricos).
- **Riesgos técnicos:** el fondo del `container` usa un color global de Elementor vía `__globals__` (`globals/colors?id=065e55b`); si ese color global se elimina o renombra en el kit de Elementor, el fondo de esta sección se rompe.

---

## Resultado de la comparación con `0-home_completa.json`

Verificación realizada comparando, sección por sección, el nodo raíz de cada archivo individual (`content[0]`) contra el bloque correspondiente dentro de `content[]` de `0-home_completa.json` (comparación exacta, deep-equal, tras parseo JSON):

| Comprobación | Resultado |
|---|---|
| Las 14 secciones están incluidas en la home completa | ✅ Confirmado (14/14) |
| Aparecen en el mismo orden que los archivos individuales | ✅ Confirmado — orden idéntico al listado de este documento |
| Los IDs raíz coinciden | ✅ Confirmado — los 14 IDs coinciden exactamente |
| El contenido de cada sección es equivalente | ✅ Confirmado — deep-equal exacto en las 14 secciones |
| No falta ni sobra ninguna sección | ✅ Confirmado — 14 secciones en ambos lados, correspondencia 1:1 |
| Existen diferencias entre el JSON individual y su versión en la home | ❌ Ninguna diferencia detectada |

**Conclusión:** `0-home_completa.json` es una concatenación exacta y sin alteraciones de los 14 archivos individuales de `00-originales`, en el orden documentado. Esta verificación queda aprobada y sirve de línea base para todo el trabajo posterior.
