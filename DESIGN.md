---
name: Emerae
description: Centro especializado en el tratamiento de adicciones en Barcelona — sistema visual documentado a partir de los 14 JSON de Elementor Pro en 00-originales.
colors:
  deep-navy: "#031830"
  clinical-blue: "#045CB4"
  morning-mist: "#BDDAE8"
  paper: "#ffffff"
  quiet-gray: "#f7f8f9"
  pale-dawn: "#f0f6fa"
  slate: "#4a5a6a"
  fog: "#7a8a9a"
typography:
  display:
    fontFamily: "Instrument Serif, Georgia, serif"
    fontSize: "clamp(2.4rem, 5.2vw, 3.4rem)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Instrument Serif, Georgia, serif"
    fontSize: "clamp(1.8rem, 2.8vw, 2.4rem)"
    fontWeight: 400
    lineHeight: 1.15
    letterSpacing: "-0.015em"
  title:
    fontFamily: "Inter, sans-serif"
    fontSize: "0.95rem"
    fontWeight: 600
    lineHeight: 1.4
  body:
    fontFamily: "Inter, sans-serif"
    fontSize: "1rem"
    fontWeight: 300
    lineHeight: 1.75
  label:
    fontFamily: "Inter, sans-serif"
    fontSize: "0.72rem"
    fontWeight: 500
    letterSpacing: "0.08em"
rounded:
  pill: "100px"
  lg: "24px"
  md: "16px"
  sm: "12px"
  circle: "50%"
spacing:
  xs: "8px"
  sm: "16px"
  md: "24px"
  lg: "48px"
  xl: "80px"
  section-y: "120px"
components:
  button-primary:
    backgroundColor: "{colors.clinical-blue}"
    textColor: "{colors.paper}"
    rounded: "{rounded.pill}"
    padding: "14px 28px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.deep-navy}"
    rounded: "{rounded.pill}"
    padding: "14px 28px"
  badge:
    backgroundColor: "rgba(4,92,180,0.06)"
    textColor: "rgba(4,92,180,0.75)"
    rounded: "{rounded.pill}"
    padding: "5px 14px 5px 10px"
    typography: "{typography.label}"
  card:
    backgroundColor: "{colors.quiet-gray}"
    rounded: "{rounded.sm}"
    padding: "24px"
  card-dark:
    backgroundColor: "rgba(255,255,255,0.06)"
    rounded: "{rounded.lg}"
    padding: "36px 32px"
---

# Design System: Emerae

## Overview

**Creative North Star: "La pausa sostenida"**

Todo el sistema respira: generosidad de aire en cada sección (paddings verticales de 96–120px), pocas sombras, formas redondeadas sin agresividad, y una tipografía serif itálica que se permite pausas emocionales dentro de una estructura por lo demás sobria y clínica. El diseño no acelera ni interrumpe — se comporta como el propio proceso terapéutico que representa: sin prisa, sin presión, con la calma como forma de autoridad.

La superficie por defecto es plana: bloques de color completo (navy oscuro frente a blanco o gris muy suave) hacen el trabajo que en otros sistemas haría la sombra. La profundidad aparece solo cuando algo necesita distinguirse activamente — una cita flotante, un acordeón abierto, una tarjeta de testimonio — nunca como decoración ambiental de fondo.

Dos registros conviven deliberadamente: uno clínico-editorial en Inter (sobrio, ligero, peso 300 en el cuerpo de texto) para explicar y estructurar, y uno emocional en Instrument Serif itálica para las frases que necesitan sentirse escritas a mano, no diseñadas — titulares, citas, manifiestos.

**Key Characteristics:**
- Superficies planas por defecto; la sombra se reserva para estados activos o elementos ya flotantes, nunca para decorar en reposo.
- Bloques de color completo (navy / blanco / gris) como principal herramienta de jerarquía y ritmo entre secciones, no la tipografía por sí sola.
- Serif itálica reservada exclusivamente para lo emocional (titulares grandes, citas, manifiestos); Inter para todo lo funcional.
- Pastillas (100px) como firma de forma: badges, botones, etiquetas de metodología — nunca esquinas vivas en elementos interactivos.
- La paleta de 3 colores de marca se aplica hoy con más de 50 variantes de opacidad improvisadas; este documento introduce una escala tonal disciplinada para sustituir ese uso ad-hoc (ver Colors y Elevation & Depth).

## Colors

La paleta es deliberadamente corta — dos tintas y un neutro oscuro que cumple doble función — pero hoy se aplica con decenas de opacidades distintas sobre esas mismas tintas (`rgba(4,92,180,0.06)` junto a 0.08, 0.12, 0.13, 0.15, 0.16, 0.2, 0.25, 0.75, 0.85...). Se propone sustituir esa proliferación por la escala tonal fija documentada en el sidecar — mismos tres colores de marca, aplicación disciplinada, ningún matiz nuevo.

### Primary
- **Clinical Blue** (#045CB4): acción y foco. Botones primarios, enlaces, el punto del badge, cifras destacadas (stats, logros), estado activo de pestañas, dots de carrusel y acordeón. Es el único color que "empuja" a actuar.

### Secondary
- **Morning Mist** (#BDDAE8): el acento sobre fondo oscuro. Aparece casi exclusivamente dentro de secciones con fondo Deep Navy (Tratamiento, Familias, CTA final) — nunca sobre fondo claro. Subrayado de citas, iconos decorativos, badges en modo oscuro.

### Neutral
- **Deep Navy** (#031830): color de doble función — fondo de sección completa en los bloques de mayor peso emocional (Tratamiento, Familias, CTA final) y color de texto principal (títulos) en las secciones claras. No existe un "navy de texto" distinto del "navy de fondo": es el mismo token, dos aplicaciones.
- **Paper White** (#ffffff): fondo por defecto de la mayoría de secciones.
- **Quiet Gray** (#f7f8f9): superficie de tarjeta sobre fondo claro (stats, tarjetas de beneficio, FAQ).
- **Pale Dawn** (#f0f6fa): uso único — fondo del Hero. No se repite en ninguna otra sección; funciona como una "entrada" visualmente distinta antes del blanco/gris del resto de la home.
- **Slate** (#4a5a6a): cuerpo de texto sobre fondo claro.
- **Fog** (#7a8a9a): texto secundario o silenciado, sobre claro y oscuro.

### Named Rules
**The Two-Surface Rule.** Cada sección es o bien clara (Paper/Quiet Gray + texto Deep Navy/Slate) o bien oscura (Deep Navy + texto blanco/Morning Mist) — nunca mezcladas dentro de la misma sección. El contraste entre secciones consecutivas marca el ritmo del scroll, no el color de texto dentro de una sección.

**The Tonal Discipline Rule (refinamiento propuesto).** En vez de improvisar una opacidad nueva cada vez que se necesita una variante suave de Clinical Blue o Morning Mist, usar la escala tonal de 8 pasos del sidecar (`.impeccable/design.json → extensions.colorMeta`) para fondos de badge, bordes hairline y estados hover/activos. Sustituye gradualmente las rgba ad-hoc actuales sin cambiar ningún matiz de marca.

## Typography

**Display Font:** Instrument Serif (con fallback Georgia, serif)
**Body Font:** Inter (con fallback sans-serif)

**Character:** Un emparejamiento deliberadamente asimétrico: Instrument Serif aporta calidez editorial y pausa emocional (siempre en cursiva cuando se usa para lo afectivo); Inter aporta neutralidad clínica y legibilidad funcional. Nunca se usan para el mismo propósito — la serif no estructura, el Inter no emociona.

### Hierarchy
- **Display** (400, `clamp(2.4rem, 5.2vw, 3.4rem)`, line-height 1.1, cursiva): el H1 del Hero. Único lugar con tamaño fluido en `vw`.
- **Headline** (400, `clamp(1.8rem, 2.8vw, 2.4rem)`, line-height 1.15): títulos de sección (H2), a menudo también en cursiva cuando cierran una idea emocional (Por qué Emerae, Equipo, Testimonios).
- **Title** (600, 0.95rem, line-height 1.4, Inter): títulos de tarjeta o componente (nombre de profesional, título de beneficio).
- **Body** (300, 1rem, line-height 1.75, Inter): párrafos de cuerpo. El peso 300 es deliberado — más ligero que el peso por defecto del navegador, refuerza la sensación de aire.
- **Label** (500, 0.72rem, letter-spacing 0.08em, Inter, mayúsculas): el badge/eyebrow que abre casi cada sección ("Nuestro Tratamiento", "El equipo"...).

### Named Rules
**The Italic-Means-Emotional Rule.** La cursiva en Instrument Serif no es decorativa: marca sistemáticamente el momento más humano o vulnerable del texto (titulares del hero, manifiestos, citas). Nunca debe aplicarse a texto funcional o de navegación.

## Layout

- Ancho de contenido: `max-width: 1100px` en las secciones `container` (flexbox); las secciones legacy `section`/`column` no fijan un ancho máximo explícito y dependen del padding lateral.
- Padding de sección: dos escalas conviven — 120px/80px vertical/lateral en secciones legacy, y 96px vertical con 140px lateral en secciones `container`. Ambas son intencionadas (reflejan las dos fases de construcción del sitio) y no deben unificarse sin que se solicite expresamente (ver `CLAUDE.md`).
- Estructura raíz mixta: 6 de 14 secciones usan `section`/`column` (Elementor legacy), 8 usan `container` (flexbox moderno). Ninguna migración implícita entre ambos sistemas.
- Responsive: casi ausente a nivel de controles nativos de Elementor (solo FAQ declara `boxed_width_tablet`/`boxed_width_mobile`, sin valor asignado). El comportamiento responsive real vive dentro de los widgets `html`, mayormente vía `@media(max-width:768px)` (una sola aparición, en Citas) o vía unidades fluidas (`vw`) en tamaños de fuente del Hero y Tratamiento.
- Grillas de tarjetas: `repeat(2,1fr)` o `repeat(3,1fr)` fijas en CSS inline, sin fallback de columna única declarado — punto de fragilidad conocido en móvil (ver `04-documentacion/INVENTARIO.md`).

## Elevation & Depth

El sistema es **prácticamente plano**: solo 4 `box-shadow` en las 14 secciones, todas de opacidad muy baja (0.04–0.07) y radio de difusión amplio (16–32px) — sombras ambientales, nunca sombras "duras" ni de contacto. La profundidad entre bloques se transmite casi por completo mediante color plano (Deep Navy vs. Paper/Quiet Gray), no mediante elevación.

Se propone formalizar esto en una escala mínima de 2 niveles, sustituyendo los 4 valores ad-hoc actuales (cada uno ligeramente distinto sin motivo aparente) por dos roles con propósito claro:

### Shadow Vocabulary
- **ambient** (`box-shadow: 0 4px 24px rgba(3,24,48,0.06)`): estado de reposo de elementos que ya flotan sobre el fondo (tarjeta de cita flotante, tarjeta de testimonio, contenedor de FAQ).
- **lifted** (`box-shadow: 0 2px 24px rgba(3,24,48,0.07), 0 0 0 1px rgba(3,24,48,0.04)`): estado activo o en foco (ítem de FAQ abierto, tarjeta en hover) — añade el anillo de 1px que ya existe hoy en Testimonios como señal adicional de "seleccionado".

### Named Rules
**The No-Ambient-Shadow-At-Rest Rule.** Las superficies planas (secciones, tarjetas de contenido estándar) no llevan sombra en reposo. La sombra aparece únicamente en elementos que ya se comportan como objetos flotantes sobre el fondo, o en su estado activo — nunca como decoración por defecto de una tarjeta cualquiera.

## Shapes

- **La pastilla (100px) es la firma de forma del sistema**: aparece en botones, badges y etiquetas de metodología (el radio más repetido, con diferencia, de todo el sistema). Cualquier elemento interactivo nuevo (botón, chip, filtro) debería adoptar este radio por defecto.
- Tarjetas de contenido: radio 12–16px (`sm`/`md`) sobre fondo claro; contenedores más grandes (imágenes, bloques destacados) suben a 20–24px (`lg`).
- Iconos circulares (punto del badge, icon-box, avatar de carrusel, flecha de navegación): `border-radius: 50%`, casi siempre sobre un cuadrado de 36–40px.
- Bordes: sistema "hairline" consistente — 1px, siempre en opacidad baja (0.06–0.25) del propio Deep Navy o Morning Mist según el fondo. Nunca un borde sólido de color puro ni un grosor mayor a 1.5px.

## Components

### Buttons
- **Shape:** pastilla completa (100px de radio) — sin excepciones observadas.
- **Primary:** fondo Clinical Blue sólido, texto blanco, padding `14px 28px`, Inter 500 0.82rem.
- **Ghost / Secondary:** fondo transparente, borde hairline 1px (`rgba(7,33,61,0.2)` sobre claro, `rgba(255,255,255,0.25)` sobre oscuro), texto Deep Navy o Morning Mist según el fondo.
- **Hover / Focus:** no hay estados hover definidos a nivel de widget de botón en el código fuente actual — es una ausencia, no una decisión de diseño (ver Do's and Don'ts).

### Badge / Eyebrow (componente de firma)
El patrón más repetido del sistema — aparece en 12 de las 14 secciones: una pastilla pequeña con un punto de color y texto en mayúsculas que abre casi cada bloque de contenido.
- **Estilo claro:** fondo `rgba(4,92,180,0.06)`, borde `rgba(4,92,180,0.15)`, texto `rgba(4,92,180,0.75)`, punto sólido Clinical Blue de 5–6px.
- **Estilo oscuro:** fondo `rgba(189,218,232,0.1)`, borde `rgba(189,218,232,0.2)`, texto `rgba(189,218,232,0.85)`, punto sólido Morning Mist.
- **Padding:** `5px 14px 5px 10px` (asimétrico: menos a la izquierda para dejar sitio al punto).

### Cards / Containers
- **Corner Style:** 12–16px sobre fondo claro; 24px sobre fondo oscuro (tarjetas de Tratamiento).
- **Background:** Quiet Gray sobre sección clara; `rgba(255,255,255,0.06)` sobre sección Deep Navy.
- **Border:** ausente sobre claro; hairline `rgba(189,218,232,0.12)` sobre oscuro.
- **Shadow Strategy:** ninguna en reposo (ver Elevation & Depth), salvo en tarjetas ya flotantes (citas, testimonios).
- **Internal Padding:** 20–24px en tarjetas pequeñas; 36px/32px en tarjetas grandes (Tratamiento).

### Carousel (componente de firma)
Patrón idéntico reutilizado en Equipo y Testimonios: track flexbox desplazado por `transform`, navegación con flechas circulares (40px, borde hairline, invierten a fondo Deep Navy en hover) y dots (6px circular, se estiran a pastilla de 20px en estado activo con color Clinical Blue). Implementado dos veces con nombres de función distintos (`eq*` / `tm*`) pero CSS casi idéntico.

### Accordion (FAQ)
Ítems con `border-radius: 14px`, número de pregunta en Morning Mist, chevron circular de 26px que invierte a Clinical Blue sólido cuando el ítem está abierto, transición de `max-height`. Solo un ítem abierto a la vez.

### Navigation / Tabs (selector del Hero, pestañas de Adicciones)
Pastillas de 100px: estado inactivo con fondo semitransparente y borde hairline, estado activo con fondo Clinical Blue sólido y texto blanco. Mismo lenguaje visual que los botones primarios — el sistema no distingue entre "botón" y "selector" a nivel de estilo.

## Do's and Don'ts

### Do:
- **Do** reservar la pastilla de 100px para todo elemento interactivo (botón, badge, tab, filtro).
- **Do** mantener la serif itálica exclusivamente para momentos emocionales (titulares grandes, citas, manifiestos) — nunca para UI funcional.
- **Do** usar bloques de color completo (Deep Navy vs. Paper/Quiet Gray) como principal herramienta de ritmo entre secciones, no la tipografía.
- **Do** aplicar la escala tonal de 8 pasos del sidecar para cualquier variante de opacidad nueva de Clinical Blue o Morning Mist, en vez de improvisar un valor rgba nuevo.
- **Do** mantener el sistema de bordes hairline (1px, opacidad baja) en vez de bordes sólidos gruesos.

### Don't:
- **Don't** añadir sombra decorativa a una tarjeta en reposo — la sombra se reserva para elementos ya flotantes o en estado activo (ver The No-Ambient-Shadow-At-Rest Rule).
- **Don't** mezclar superficie clara y oscura dentro de la misma sección (ver The Two-Surface Rule).
- **Don't** introducir un cuarto color de marca sin decisión expresa — la paleta de 3 tintas + neutros es deliberadamente corta.
- **Don't** migrar `section`/`column` a `container` (ni al revés) como parte de una tarea de estilo — es una decisión estructural que requiere aprobación expresa (ver `CLAUDE.md`).
- **Don't** dar por sentado un estado hover en botones: hoy no existe definido en el código fuente; cualquier hover que se añada debe decidirse explícitamente, no asumirse.
