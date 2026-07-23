# CLAUDE.md — Proyecto Home Emerae (Elementor Pro)

Este archivo establece las reglas permanentes de trabajo para cualquier sesión que opere sobre este proyecto. Estas reglas prevalecen sobre cualquier atajo o conveniencia puntual.

## 1. Naturaleza del proyecto

Este proyecto contiene la home de Emerae construida con **Elementor Pro**, exportada como JSON. El trabajo consiste en analizar, planificar y versionar mejoras sobre esos JSON — no en reconstruir la página con otras tecnologías.

## 2. `00-originales` es de solo lectura absoluta

- La carpeta `00-originales` contiene los JSON exportados directamente desde Elementor y es **intocable**.
- **Nunca** modificar, sobrescribir, renombrar, mover ni eliminar ningún archivo de `00-originales`, bajo ninguna circunstancia ni aunque se solicite de forma implícita.
- Cualquier tarea que requiera cambiar contenido debe operar sobre copias nuevas en `01-secciones-trabajo`, nunca sobre el original.

## 3. Estructura de referencia de los JSON

- `0-home_completa.json` es la **referencia global** de la home: contiene la concatenación exacta y verificada de las 14 secciones individuales, en orden.
- Existen **15 JSON en total** dentro de `00-originales`: 1 archivo de home completa + 14 archivos de sección individual.
- Las 14 secciones, en orden, son: Hero, Stats, Citas, Enfoque, Tratamiento, CTA intermedio, Adicciones, Por qué Emerae, Equipo, Familias, Testimonios, Logros, FAQ, CTA final.
- El detalle completo de cada sección está documentado en `04-documentacion/INVENTARIO.md` y debe consultarse antes de proponer cualquier cambio.

## 4. Sistema de versionado

- Todas las modificaciones se crean como archivos **nuevos** dentro de `01-secciones-trabajo`.
- Cada iteración se guarda con sufijo de versión incremental: `v1`, `v2`, `v3`, etc. (por ejemplo: `06-adicciones_v1.json`, `06-adicciones_v2.json`).
- **Nunca sobrescribir una versión anterior.** Cada intento nuevo es un archivo nuevo; el historial completo se conserva.
- Las versiones que hayan sido probadas en Elementor y aprobadas por el usuario se copian a `03-versiones-finales`.
- El estado de cada sección se registra y actualiza en `04-documentacion/PROJECT-STATUS.md`.

## 5. Compatibilidad técnica con Elementor Pro

- Toda estructura JSON generada debe mantenerse **compatible con Elementor Pro** (misma sintaxis de `elType`, `settings`, `elements`, `widgetType`, `id`, etc. que usan los originales).
- **No inventar propiedades, widgets ni estructuras** que no existan o no sean compatibles con los JSON originales. Si una propiedad no aparece en ningún archivo de `00-originales`, no se debe asumir que Elementor la soporta sin verificarlo.
- Respetar que **algunas secciones usan el sistema legacy `section`/`column`** y otras usan **`container`** (flexbox). Esto es intencional y refleja distintas fases de construcción del sitio.
- **No migrar `section`/`column` a `container`** (ni al revés) salvo que se solicite expresamente para esa sección concreta.
- **Priorizar la conservación de los widgets existentes** por encima de sustituirlos por alternativas "más modernas" o "más limpias".
- Mantener correctamente el **HTML, CSS y JavaScript personalizado** embebido en los widgets `html`: no eliminarlo, simplificarlo ni reescribirlo sin que se solicite explícitamente, y siempre evaluando sus dependencias (funciones JS referenciadas por `onclick`, IDs usados por selectores, animaciones `@keyframes`, etc.).
- **No utilizar React, Tailwind, Framer Motion ni ninguna librería externa.** El único stack válido dentro de los widgets HTML es HTML/CSS/JS vanilla, consistente con lo ya usado en los archivos originales.

## 6. Alcance de las modificaciones

- **No modificar más secciones de las solicitadas.** Cada tarea de edición debe limitarse a la(s) sección(es) que el usuario pida explícitamente.
- Conservar y revisar los ajustes de **escritorio, tableta y móvil** de cada sección; no eliminar ni ignorar configuraciones responsive existentes (nativas de Elementor o vía `@media` dentro del HTML custom).
- **No sustituir contenido placeholder** (textos "por definir", nombres genéricos, testimonios de relleno, etc.) **sin haber recibido el contenido real** del usuario.
- **No alterar teléfonos, enlaces de WhatsApp ni enlaces pendientes** (`href="#"`, números placeholder como `+34000000000`, etc.) **sin recibir los datos correctos** por parte del usuario.

## 7. Proceso de trabajo obligatorio

- Validar la **sintaxis JSON** después de cada modificación (el archivo debe parsear correctamente).
- **Comparar siempre** cada nueva versión con su JSON original correspondiente, documentando qué cambió exactamente.
- **Explicar y planificar los cambios antes de aplicarlos** — nunca modificar directamente sin presentar antes la propuesta y obtener aprobación.
- El flujo de trabajo detallado paso a paso está definido en `04-documentacion/WORKFLOW.md` y debe seguirse para cada sección.

## 8. Límites de actuación fuera de los archivos

- **No realizar ninguna acción sobre el WordPress publicado** (no hay acceso ni se debe intentar acceder al sitio en producción).
- **No importar automáticamente ningún JSON ni Website Kit** en Elementor. Toda importación a Elementor para pruebas la realiza el usuario manualmente.
- **No asumir que un JSON válido producirá necesariamente el resultado visual correcto.** La validez sintáctica del JSON no garantiza el renderizado esperado — toda versión debe probarse visualmente en Elementor (escritorio, tableta y móvil) antes de considerarse aprobada.

## 9. Documentación viva del proyecto

- `04-documentacion/INVENTARIO.md`: análisis técnico verificado de las 14 secciones.
- `04-documentacion/PROJECT-STATUS.md`: estado de avance de cada sección (original / en trabajo / probada / aprobada).
- `04-documentacion/WORKFLOW.md`: flujo de trabajo obligatorio y prohibiciones.
- `PRODUCT.md` y `DESIGN.md` (cuando existan) deben consultarse también antes de proponer cambios de contenido o de estilo.

Estas reglas son permanentes y aplican a todas las sesiones futuras sobre este proyecto.
