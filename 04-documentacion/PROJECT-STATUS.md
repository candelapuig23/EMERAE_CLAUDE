# PROJECT-STATUS.md — Estado de avance por sección

Este documento se actualiza cada vez que se crea una nueva versión de trabajo, se realiza una prueba responsive en Elementor, o se aprueba una versión final (ver `WORKFLOW.md`, paso 16). Refleja el estado real del trabajo, no el análisis técnico (para eso, ver `INVENTARIO.md`).

Última actualización: 23/07/2026 — estado inicial tras verificación de los 15 JSON originales. Ninguna sección tiene todavía versión de trabajo.

| Nº | Sección | Archivo original | Archivo de trabajo actual | Estado | Probada en escritorio | Probada en tableta | Probada en móvil | Versión final | Observaciones |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Hero | `00-originales/01-hero_emerae.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | Selector de intención con 9 paneles en estado placeholder ("Contenido por definir en la siguiente fase") |
| 2 | Stats | `00-originales/02-stats.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | Sección completa; sin claves responsive nativas |
| 3 | Citas | `00-originales/02.2-citas.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | Única sección con `@media` propio; citas ocultas en móvil por diseño |
| 4 | Enfoque | `00-originales/03-enfoque.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | Botón enlaza a ancla interna `#tratamiento` |
| 5 | Tratamiento | `00-originales/04-tratamiento.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | Botón enlaza a ancla interna `#contacto` |
| 6 | CTA intermedio | `00-originales/05-cta_intermedio.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | Teléfono y WhatsApp con placeholder `+34000000000`; requiere datos reales |
| 7 | Adicciones | `00-originales/06-adicciones.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | Todas las tarjetas de adicción enlazan a `#`; requiere destinos reales |
| 8 | Por qué Emerae | `00-originales/07-porque.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | Sección completa; sin contenido pendiente detectado |
| 9 | Equipo | `00-originales/08-equipo.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | 5 de 6 perfiles son placeholder "Nombre Apellido"; posible desajuste de paginación del carrusel |
| 10 | Familias | `00-originales/09-familias.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | Botón "Información para familias" sin destino real (`#`) |
| 11 | Testimonios | `00-originales/10-testimonios.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | 2 de 5 testimonios son placeholder; posible desajuste de paginación del carrusel |
| 12 | Logros | `00-originales/11-logros.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | Contenido completo pero redundante editorialmente con Stats |
| 13 | FAQ | `00-originales/12-faq.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | Botón "Haznos una pregunta" sin destino real (`#`); claves responsive nativas declaradas sin valor |
| 14 | CTA final | `00-originales/13-cta_final.json` | Pendiente | Original analizado | Pendiente | Pendiente | Pendiente | Pendiente | 3 CTAs finales sin destino real ni datos de contacto |

## Leyenda de estados posibles

- **Original analizado** — estado inicial; solo se ha leído y documentado el JSON original, sin crear ninguna versión de trabajo.
- **Propuesta presentada** — se ha analizado la sección y presentado una propuesta de cambio, pendiente de aprobación del usuario.
- **En trabajo** — existe al menos una versión (`vN`) en `01-secciones-trabajo`, pendiente de prueba en Elementor.
- **Probada en Elementor** — la versión de trabajo se ha importado manualmente y revisado en escritorio/tableta/móvil.
- **Aprobada** — el usuario ha aprobado la versión tras la prueba visual; se copia a `03-versiones-finales`.

Este archivo debe actualizarse siguiendo el paso 16 de `WORKFLOW.md` cada vez que cambie el estado de una sección.
