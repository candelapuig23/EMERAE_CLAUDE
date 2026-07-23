# WORKFLOW.md — Flujo de trabajo obligatorio

Este documento define el proceso que debe seguirse para modificar cualquier sección de la home de Emerae. Es de cumplimiento obligatorio para toda tarea de edición, independientemente de su tamaño. Complementa las reglas permanentes de `CLAUDE.md`.

## Flujo obligatorio, paso a paso

1. **Seleccionar una única sección.** No se trabaja sobre varias secciones a la vez salvo petición expresa del usuario.
2. **Leer su JSON original** en `00-originales` (nunca trabajar de memoria ni sobre supuestos de una lectura anterior si ha pasado tiempo o contexto).
3. **Consultar `INVENTARIO.md`, `PRODUCT.md` y `DESIGN.md` cuando existan**, para entender el análisis técnico ya verificado y cualquier lineamiento de producto o diseño disponible.
4. **Analizar problemas y oportunidades** de la sección: placeholders, enlaces pendientes, riesgos técnicos, inconsistencias, sin todavía tocar el archivo.
5. **Presentar una propuesta sin modificar archivos.** La propuesta debe explicar qué se cambiaría y por qué, en términos concretos.
6. **Esperar la aprobación** explícita del usuario antes de crear ningún archivo nuevo.
7. **Crear una nueva versión en `01-secciones-trabajo`**, con sufijo de versión incremental (`v1`, `v2`, `v3`...), nunca sobrescribiendo una versión previa.
8. **Validar la sintaxis JSON** de la nueva versión (el archivo debe parsear correctamente antes de continuar).
9. **Comparar la versión con el original**, verificando qué cambió y que no se haya alterado nada fuera del alcance solicitado.
10. **Informar exactamente de los cambios** realizados, de forma clara y verificable.
11. **Importar manualmente en una página de prueba de Elementor** (la importación la realiza el usuario; nunca se automatiza).
12. **Revisar escritorio, tableta y móvil** en esa página de prueba.
13. **Incorporar capturas a `02-referencias`** (en la subcarpeta correspondiente: `escritorio`, `tablet` o `movil`).
14. **Corregir mediante una nueva versión, sin sobrescribir**, si la revisión visual detecta problemas.
15. **Guardar la versión aprobada en `03-versiones-finales`**, una vez validada visualmente y aprobada por el usuario.
16. **Actualizar `PROJECT-STATUS.md`** reflejando el nuevo estado, archivo de trabajo actual, resultados de las pruebas responsive y versión final.

## Prohibiciones

- **No modificar originales.** `00-originales` es de solo lectura en todo momento, sin excepciones.
- **No trabajar directamente sobre toda la home** cuando el usuario solo ha solicitado una sección concreta.
- **No importar nada automáticamente en WordPress ni en Elementor.** Toda importación y publicación la realiza el usuario de forma manual.
- **No dar por aprobada una versión que no haya sido probada en Elementor.** Un JSON sintácticamente válido no garantiza el resultado visual correcto (ver `CLAUDE.md`, punto 8).
- **No eliminar HTML, CSS o JavaScript sin evaluar sus dependencias** (funciones referenciadas por `onclick`, IDs usados por selectores JS, animaciones `@keyframes`, imports de fuentes, etc.).
