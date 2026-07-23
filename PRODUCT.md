# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Dos audiencias primarias, con el mismo peso estratégico entre sí:

- **La persona que busca ayuda para sí misma**, en cualquier fase de decisión — desde quien no sabe si lo que vive es una adicción, hasta quien ya está listo para empezar tratamiento.
- **Un familiar o persona cercana** que busca ayuda para alguien que quiere, a menudo sin saber cómo acercarse o qué hacer cuando la persona todavía no acepta ayuda.

Audiencia secundaria: **profesionales que pueden derivar un paciente** (médicos, terapeutas, otros centros). Existe en la home (segmentación del hero, sección "Por qué Emerae") pero no es el foco principal de conversión.

## Product Purpose

Emerae es un centro especializado en el tratamiento de adicciones en Barcelona (presencial y online). Ofrece una primera consulta gratuita y sin compromiso, y acompaña a la persona y a su entorno familiar durante todo el proceso de recuperación. El éxito del producto (la home) es que la persona correcta —paciente o familiar, en cualquier fase de duda o decisión— dé el primer paso de contacto.

## Positioning

El mecanismo diferencial confirmado es que el tratamiento no se limita a que la persona deje de consumir — se trabaja **la función y el origen de la adicción** en la historia de esa persona (protege, anestesia o evita un dolor) como base para sostener el cambio. Esto es lo que ordena todo el mensaje de marca.

A esto se suma el origen de marca, también acordado: Emerae nace de la **vocación e ilusión de dos generaciones** — no como una oportunidad empresarial, sino como la continuación de un compromiso personal y profesional con las personas, las familias y la sociedad. La adicción es prioritaria en el tratamiento por ese mismo recorrido personal y profesional del equipo (idea acordada, registrable como tal).

**Retirado — no vigente como diferenciador:** "Especialización exclusiva en adicciones", "es lo único en lo que trabajamos" y cualquier formulación de que Emerae se dedica exclusivamente a las adicciones. Motivo: se prevé ampliar servicios más allá de las adicciones, por lo que el concepto de exclusividad no debe usarse como diferenciador ni en ningún otro contexto de marca.

## Operating Context

- La home vive como JSON exportado de **Elementor Pro** dentro de este repositorio, no como código de aplicación. El "producto" que se diseña aquí es, en la práctica, la estructura y contenido de esos JSON.
- El sitio en producción corre en **WordPress** (`centroemerae.com`); no hay acceso a ese entorno desde este proyecto ni se realiza ninguna acción sobre él.
- Toda importación de JSON a Elementor para pruebas visuales es manual y la realiza el usuario — nunca se automatiza.
- Flujo de trabajo y versionado ya establecidos y de cumplimiento obligatorio: ver `CLAUDE.md` y `04-documentacion/WORKFLOW.md`.
- Por la naturaleza del servicio (salud mental / adicciones), la confidencialidad del proceso terapéutico es un compromiso explícito y recurrente en el copy existente (ver sección "Por qué Emerae": "Confidencialidad total"); la denominación exacta del acuerdo/contrato de confidencialidad está pendiente de que Paula la confirme.
- Existe un documento editorial de mayor autoridad que el copy actual de los JSON: `04-documentacion/Documento_maestro_revision_Home_Centro_Emerae (1).docx`, resultado de dos reuniones de revisión del equipo clínico/directivo. Ante discrepancia con `00-originales`, prevalece el documento maestro — pero solo su contenido marcado ACORDADO se trata como aprobado; RECOMENDACIÓN y REDACCIÓN PROPUESTA requieren aprobación explícita del usuario antes de implementarse.

## Capabilities and Constraints

- Trata tanto **adicciones a sustancias** (alcohol, cocaína, cannabis, opioides, MDMA, chemsex, tabaco, otras) como **adicciones comportamentales** (juego, pornografía, internet, videojuegos, compras, comida), y **patología dual** (adicción + trastorno mental asociado). Revisión clínica completa de estas descripciones pendiente.
- Modalidades de terapia: individual, grupal y familiar.
- Metodologías mencionadas en el copy — TCC, terapias de tercera generación, EMDR, regulación emocional, mindfulness — deben tratarse como **taxonomía pendiente de validación clínica con Paula**, no como lista cerrada. TCC y "terapias de tercera generación" son conceptos distintos que hoy aparecen fusionados en el copy y deben separarse. Mindfulness debe mostrarse como etiqueta reconocible por el público aunque forme parte de un marco terapéutico más amplio.
- Servicios mencionados en revisión editorial pero **inexistentes hoy en el JSON y sin confirmar**: acompañamiento telefónico 24h para pacientes (alcance, pacientes, situaciones y responsable pendientes) e intervención profesional cuando la persona no acepta ayuda (pendiente de validación con Paula). No presentar ninguno de los dos como servicio activo hasta confirmación.
- Modalidad de atención: presencial en Barcelona y online, con la misma calidad de acompañamiento en ambas; pendiente confirmar que "presencial y online" aplica realmente a todos los servicios anunciados.
- Primera consulta gratuita, sin compromiso; la duración de "una hora" está pendiente de confirmar antes de afirmarla.
- Restricciones editoriales explícitas: no publicar precios, no publicar una duración cerrada del proceso (p. ej. "dos años"), no incluir recomendaciones generales sobre baja laboral.
- Constricción técnica permanente: toda modificación debe mantenerse compatible con la sintaxis de Elementor Pro (ver `CLAUDE.md`); no se introducen frameworks ni librerías externas.

## Brand Commitments

- Nombre: **Emerae**.
- Voz confirmada tras dos reuniones de revisión editorial: hablar de la persona antes que de la etiqueta; comprender antes que juzgar, sin moralizar ni culpabilizar; explicar lo complejo con palabras sencillas; transmitir esperanza sin prometer resultados garantizados; combinar emoción (home) y rigor (páginas internas); evitar la "titulitis".
- Léxico confirmado para el universo verbal de marca: *persona, historia, herida, realidad, dolor, función, raíz, comprender, sostener, herramientas, cambio, arropar, acompañar, respeto, ética, vocación, responsabilidad, familia, recuperar*.
- Léxico a limitar o evitar: "adicto" como identidad fija; "mala persona" (salvo uso muy cuidadoso para desmontar el estigma); "exclusivo" / "única especialidad"; promesas de abstinencia "de por vida" como resultado garantizado; jerga técnica sin explicar; críticas directas a la competencia; "intrusismo" sin una estrategia legal y de marca clara; "alta" si el equipo no usa ese concepto.
- Compromiso explícito de confidencialidad total del proceso terapéutico (concepto confirmado); la denominación exacta del acuerdo/contrato de confidencialidad está pendiente de que Paula la confirme.
- Origen de marca confirmado: Emerae nace de la vocación e ilusión de dos generaciones; no es un proyecto construido alrededor de una oportunidad empresarial, sino la continuación de un compromiso con las personas, las familias y la sociedad. La adicción es prioritaria en el tratamiento por el recorrido personal y profesional del equipo (idea acordada).
- Dos figuras clave de marca y autoridad de validación: **Paula** (valida taxonomía clínica, cargos y formaciones del equipo, y la denominación del acuerdo de confidencialidad) y **Esmeralda**, socia fundadora (aporta el contenido histórico/fundacional de la marca; su ficha profesional y su bio están pendientes de validación). Ningún título profesional —incluido el de Paula— debe darse por confirmado sin verificación individual.

## Evidence on Hand

**Real y confirmado:**
- 3 imágenes reales alojadas en `centroemerae.com` (secciones Enfoque, CTA intermedio, Familias).
- 1 nombre y rol de equipo confirmado: Paula Ferrer, Directora del centro. Su título profesional exacto (p. ej. "Psicóloga clínica") está pendiente de verificación individual — ver Brand Commitments.

**Ausente — marcado como pendiente, futuro trabajo NO debe fabricar estos datos:**
- Los 5 testimonios de la sección Testimonios: ninguno es real. Los 2 marcados literalmente como `"Testimonio placeholder — reemplazar con testimonio real de Paula"` y los otros 3 (redactados "como muestra", sin marcar como placeholder en el JSON) deben sustituirse igualmente por testimonios reales, anónimos y autorizados por escrito por pacientes/familiares.
- 5 de 6 bios y fotos del equipo (actualmente `"Nombre Apellido"` genérico; las "fotos" son siluetas CSS decorativas, no fotografías reales).
- Ficha profesional y bio de Esmeralda, socia fundadora — no existe hoy en ningún JSON.
- Teléfono y número de WhatsApp reales (actualmente `+34000000000` / `wa.me/34000000000` en la sección CTA intermedio).
- Destinos reales para varios CTA que hoy apuntan a `#`: tarjetas de tipo de adicción (sección Adicciones), "Información para familias", "Haznos una pregunta" (FAQ), y los 3 CTAs de la sección CTA final (incluyendo ahí también teléfono/WhatsApp).
- Contenido de los 9 paneles del selector de intención del Hero (hoy: "Contenido por definir en la siguiente fase").
- Cifra de años de experiencia: el JSON actual es internamente inconsistente ("+25" en Hero, "+20" en Logros); ninguna de las dos cifras debe darse por buena hasta verificación documental de la cronología.
- Cronología y hechos concretos de la historia de la marca — fecha de inicio aproximada (~1999/2000), denominación "Centro Terapéutico del Vallès", La Garriga, entidades, cargos y otros hitos: mencionados como acuerdo de reunión editorial, pero **no verificados documentalmente**. No deben presentarse como evidencia pública confirmada hasta su verificación.

**Fuente editorial de referencia:** `04-documentacion/Documento_maestro_revision_Home_Centro_Emerae (1).docx` — documento de mayor autoridad editorial que el copy actual de los JSON, resultado de dos reuniones de revisión. Ante discrepancia, prevalece el documento maestro, pero solo su contenido marcado ACORDADO se trata como aprobado.

## Product Principles

1. **La función/raíz de la adicción es el único diferenciador confirmado.** Todo copy o feature nuevo debe reforzar que Emerae trabaja el origen y la función de la adicción (protege, anestesia, evita), no solo el cese del consumo. La "especialización exclusiva" queda retirada como diferenciador — se prevé ampliar servicios, por lo que el concepto de exclusividad no debe usarse en ningún contexto de marca.
2. **Paciente y familiar conducen la conversión; el profesional acompaña sin robar protagonismo.** Las decisiones de jerarquía visual o de contenido priorizan a estas dos audiencias; la vía de derivación profesional se mantiene visible pero secundaria.
3. **Confidencialidad y enfoque no moralizante son innegociables.** Ningún copy nuevo debe sonar clínico-frío, moralizante ni culpabilizador (tampoco hacia las familias); el trato cercano es tan parte del producto como el rigor terapéutico.
4. **No inventar evidencia.** Testimonios, bios de equipo, cifras, cronología de marca, teléfonos o enlaces ausentes se documentan como pendientes (ver Evidence on Hand) y solo se completan con datos reales aportados por el usuario o validados por Paula/Esmeralda — nunca se fabrican.
5. **El documento maestro de revisión editorial prevalece sobre el copy actual de los JSON.** Ante cualquier discrepancia entre `00-originales` y `04-documentacion/Documento_maestro_revision_Home_Centro_Emerae (1).docx`, prevalece el documento maestro — pero solo lo marcado ACORDADO se trata como aprobado; RECOMENDACIÓN y REDACCIÓN PROPUESTA requieren aprobación explícita del usuario antes de implementarse.
6. **El vehículo técnico es Elementor Pro vía JSON, no una reconstrucción libre.** Toda propuesta de producto debe seguir siendo implementable dentro de las restricciones ya documentadas en `CLAUDE.md`.
