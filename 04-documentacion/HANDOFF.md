# HANDOFF.md — Estado del proyecto Home Emerae

Documento de traspaso para retomar el trabajo en una sesión nueva sin perder contexto. Generado el 23/07/2026.

## 1. Objetivo del proyecto

Analizar, planificar y versionar mejoras sobre la home de Emerae (centro especializado en el tratamiento de adicciones en Barcelona), construida en **Elementor Pro** y exportada como JSON. El trabajo no consiste en reconstruir el sitio con otra tecnología, sino en producir nuevas versiones de esos JSON — compatibles con Elementor Pro — que eleven el diseño y corrijan el contenido conservando la identidad de marca actual. Toda modificación se versiona; nada se publica sin pruebas visuales en Elementor y aprobación explícita del usuario.

## 2. Trabajo realizado hasta ahora

1. Inspección completa de `00-originales` (15 JSON) y verificación programática de que `0-home_completa.json` es la concatenación exacta, en orden, de las 14 secciones individuales (IDs raíz, orden y contenido idénticos).
2. Documentación permanente del proyecto: reglas de gobierno (`CLAUDE.md`), inventario técnico verificado de las 14 secciones (`INVENTARIO.md`), tabla de estado (`PROJECT-STATUS.md`) y flujo de trabajo obligatorio (`WORKFLOW.md`).
3. `/impeccable init` → creación de `PRODUCT.md` (contexto de producto: usuarios, posicionamiento, restricciones).
4. Lectura completa del documento maestro de revisión editorial (`Documento_maestro_revision_Home_Centro_Emerae (1).docx`, resultado de dos reuniones de revisión), comparación con `PRODUCT.md` y aplicación de correcciones aprobadas por el usuario (ver sección 7).
5. `/impeccable document` → creación de `DESIGN.md` y `.impeccable/design.json` (sistema visual documentado a partir de los 14 JSON, con una escala tonal y de sombra disciplinada propuesta como refinamiento).
6. Construcción y validación de la primera versión completa de la nueva Home: `01-secciones-trabajo/0-home-emerae-v1.json` (13 secciones, generado programáticamente, 10 validaciones automáticas superadas).

## 3. Archivos creados

| Archivo | Contenido |
|---|---|
| `CLAUDE.md` | Reglas permanentes del proyecto |
| `PRODUCT.md` | Contexto de producto (corregido tras el documento maestro) |
| `DESIGN.md` | Sistema visual documentado + refinamiento de color/sombra |
| `.impeccable/design.json` | Sidecar de tokens, rampas tonales y componentes de firma |
| `04-documentacion/INVENTARIO.md` | Análisis técnico verificado de las 14 secciones originales |
| `04-documentacion/PROJECT-STATUS.md` | Estado de avance por sección (todavía sin actualizar tras la v1, ver sección 9) |
| `04-documentacion/WORKFLOW.md` | Flujo de trabajo obligatorio y prohibiciones |
| `01-secciones-trabajo/0-home-emerae-v1.json` | Primera versión completa de la nueva Home |
| `04-documentacion/HANDOFF.md` | Este documento |

No creados por esta asistencia (aportado por el usuario): `04-documentacion/Documento_maestro_revision_Home_Centro_Emerae (1).docx`.

## 4. Estado de PRODUCT.md y DESIGN.md

- **PRODUCT.md**: vigente y actualizado. Creado con `/impeccable init` y corregido tras contrastarlo con el documento maestro — se retiró la "especialización exclusiva" como diferenciador, se reclasificaron los 5 testimonios como no reales, se marcó la cronología de marca y la taxonomía terapéutica como pendientes de verificación, y se añadieron Paula y Esmeralda como autoridades de validación. Sin cambios pendientes conocidos.
- **DESIGN.md**: vigente y actualizado. Creado con `/impeccable document` en modo escaneo sobre los 14 JSON. Incluye un refinamiento explícito (a petición del usuario) de la paleta y las sombras: una escala tonal de 8 pasos por color y una escala de sombra de 2 roles, sustituyendo la proliferación de opacidades ad-hoc del sistema original. Sin cambios pendientes conocidos.

## 5. Skills instaladas

- **impeccable** — única skill de diseño relevante para este proyecto. Su hook de detección de diseño está activo y se disparó durante la construcción de `0-home-emerae-v1.json` (hallazgos de tamaños de fuente y radios fuera de la escala documentada); todos los hallazgos se revisaron y resolvieron consolidando constantes de tipografía reutilizables en el generador.

## 6. Estado de los JSON originales

`00-originales` contiene 15 JSON (1 home completa + 14 secciones individuales) y permanece **intacta y de solo lectura** durante todo el proyecto. Verificado repetidamente en cada tarea: mismos tamaños y fechas de archivo desde el inicio de la sesión, los 15 parsean correctamente. Ningún archivo de esta carpeta ha sido modificado, sobrescrito, renombrado ni eliminado en ningún momento.

## 7. Decisiones editoriales importantes

- **Diferenciador confirmado**: trabajar la raíz/función de la adicción (protege, anestesia, evita), no solo el cese del consumo.
- **Retirado**: "Especialización exclusiva en adicciones" / "es lo único en lo que trabajamos" — se prevé ampliar servicios, el concepto de exclusividad no debe usarse.
- **Acordado**: origen de marca "vocación e ilusión de dos generaciones"; la adicción es prioritaria por el recorrido personal y profesional del equipo.
- **Ningún testimonio actual es real** (ni los 2 marcados como placeholder ni los otros 3 "redactados como muestra") — los 5 deben sustituirse por testimonios reales, anónimos y autorizados.
- **Teléfono 24h e intervención profesional**: mencionados en las reuniones de revisión pero sin alcance confirmado — no se presentan como servicios activos.
- **Cifra de años**: el JSON original es inconsistente ("+25" en Hero, "+20" en Logros) — ninguna cifra se da por buena sin verificación documental de la cronología.
- **Taxonomía terapéutica** (TCC / terapias de tercera generación / EMDR / regulación emocional / mindfulness): pendiente de validación clínica con Paula; TCC y "tercera generación" deben tratarse como conceptos distintos.
- **Cronología de marca** (~1999/2000, "Centro Terapéutico del Vallès", La Garriga, entidades, cargos): pendiente de verificación documental, no publicable como hecho confirmado.
- **Títulos profesionales del equipo**, incluido el de Paula ("Psicóloga clínica"): pendientes de verificación individual, no se afirman sin confirmar.
- **Autoridad editorial**: ante discrepancia entre `00-originales` y el documento maestro, prevalece el documento maestro — pero solo su contenido marcado ACORDADO se trata como aprobado; RECOMENDACIÓN y REDACCIÓN PROPUESTA requieren aprobación explícita del usuario.

## 8. Última tarea completada

Construcción y validación de `01-secciones-trabajo/0-home-emerae-v1.json`: 13 secciones (Hero, Confianza, Manifiesto, Enfoque, Tratamiento, Enfermedad del alma, Qué tratamos, Por qué Emerae, Equipo, Familias, Testimonios, FAQ, Contacto), con contenido ACORDADO/REDACCIÓN PROPUESTA aplicado, ausencias marcadas explícitamente como `PENDIENTE — NO PUBLICAR`, y las 10 validaciones técnicas solicitadas superadas (sintaxis, IDs únicos, HTML/CSS/JS balanceado, selectores aislados, responsive, comparación de esquema con `0-home_completa.json`). No copiada a `03-versiones-finales` ni marcada como aprobada.

> **Nota sobre este documento**: la instrucción original para este HANDOFF pedía listar como "próxima tarea" la generación de `01-secciones-trabajo/0-home-emerae-v1.json`. Ese archivo ya existe y está validado (ver arriba) — se refleja aquí como última tarea completada, no como pendiente, para que este documento sea fiable si se usa para retomar el trabajo. Si la intención era otra (por ejemplo, regenerar una v2, o que el archivo abierto en `Downloads` sea una versión distinta a revisar), conviene aclararlo antes de continuar.

## 9. Próxima tarea

Según `WORKFLOW.md` (pasos 11-16), lo que sigue tras crear una versión de trabajo es:
1. Importar manualmente `0-home-emerae-v1.json` en una página de prueba de Elementor.
2. Revisar visualmente en escritorio, tableta y móvil.
3. Incorporar capturas a `02-referencias/`.
4. Corregir mediante una nueva versión (`v2`, etc.) si algo falla — nunca sobrescribir `v1`.
5. Una vez aprobada, copiar a `03-versiones-finales` y actualizar `PROJECT-STATUS.md` (que hoy sigue marcando las 14 secciones originales como "Original analizado", sin reflejar todavía la existencia de esta v1).

## 10. Prompt recomendado para retomar el trabajo

```
Retoma el proyecto Home Emerae. Lee primero 04-documentacion/HANDOFF.md para
el contexto completo. El archivo 01-secciones-trabajo/0-home-emerae-v1.json
ya existe y está validado técnicamente, pero todavía NO se ha probado en
Elementor ni aprobado.

Ayúdame a [revisar los resultados de la prueba en Elementor / corregir algo
puntual de la v1 creando una v2 / actualizar PROJECT-STATUS.md tras la
aprobación] — no regeneres la v1 desde cero salvo que te lo pida explícitamente.

No modifiques nada dentro de 00-originales bajo ninguna circunstancia.
```

## 11. Advertencia

**`00-originales` es de solo lectura absoluta.** Ninguna sesión futura debe modificar, sobrescribir, renombrar, mover ni eliminar ningún archivo de esa carpeta, bajo ninguna circunstancia ni aunque se solicite de forma implícita. Cualquier cambio de contenido se hace siempre sobre archivos nuevos en `01-secciones-trabajo`.
