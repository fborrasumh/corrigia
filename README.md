# CorrigIA

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23055759.svg)](https://doi.org/10.5281/zenodo.23055759)

**Aplicación:** https://fborrasumh.github.io/corrigia/

Corrección asistida de **exámenes manuscritos** para profesorado de cualquier asignatura. Escribes el baremo, subes las copias escaneadas o fotografiadas y la IA transcribe cada respuesta, puntúa criterio a criterio y redacta un comentario para cada estudiante. La nota la calcula el código; tú revisas y decides. Un solo fichero (`index.html`), sin servidor ni cuenta, en **español, inglés y portugués**.

## Cuatro pasos

1. **El baremo.** Para cada pregunta: enunciado, respuesta esperada y criterios observables con sus puntos. Los puntos de la pregunta son la suma de sus criterios. La nota final se reescala a la escala que elijas (por defecto, sobre 10).
2. **Las copias.** Un PDF o una foto por estudiante, o un único PDF con todo el lote indicando cuántas páginas tiene cada copia.
3. **Corrección y revisión.** La IA corrige copia a copia; tú ves la copia junto a la corrección, cambias cualquier puntuación (la nota se recalcula), editas el comentario y marcas la copia como revisada.
4. **Resultados.** Media, mediana, desviación típica, aprobados y dominio por pregunta. Descarga de notas en CSV (Excel) e informe en Word con la nota y el comentario de cada estudiante.

## Qué hace la IA y qué hace el código

- **La IA** lee las imágenes, transcribe, propone puntos por criterio, los justifica y redacta el comentario.
- **El código** busca cada pregunta y criterio por su identificador, recorta al máximo los puntos que lo superan, pone a 0 lo que la IA no puntúa, suma y calcula la nota. Nunca toma una nota suelta de la IA. Marca como **dudosa** una respuesta ilegible, de confianza baja, sin transcripción o con puntos sin respuesta, y avisa de cada ajuste.
- **El profesor** decide: las exportaciones indican qué notas no ha revisado.

## Privacidad

Las imágenes de las copias y el baremo se envían a tu proveedor de IA (OpenAI, Google Gemini o Anthropic Claude) con tu propia clave; no hay servidor intermedio. Por defecto se **tapa la franja superior de la primera página** (donde suele ir el nombre) antes de enviarla, y antes del primer envío ves la imagen tal como sale. Más allá de esa franja, las imágenes no se pueden enmascarar. Todo lo demás (baremo, copias, correcciones y clave) se guarda solo en el navegador (IndexedDB y `localStorage`). **Antes de usarla con estudiantes reales, consulta con tu universidad** si ese tratamiento está cubierto (acuerdo con el proveedor, información al estudiantado).

## Límites

- La calidad de la lectura depende del modelo (debe leer imágenes) y de la letra. No se ha probado con una clave real en esta versión: las pruebas usan una IA simulada.
- Antes de usarla en un examen real, corrige con ella unas cuantas copias ya calificadas a mano y compara.
- La IA propone; la nota la pone el profesor.

## Ejemplo sin clave

«Ver un ejemplo» carga tres copias manuscritas simuladas, con su corrección precalculada, en el idioma de la interfaz. Una tiene una respuesta dudosa y en otra el código recorta una puntuación fuera de rango.

## Novedades de la versión 2.0.0

Rediseño con el sistema Forja: más simple (cuatro pasos, una sola llamada de IA por copia), para cualquier asignatura, en tres idiomas y con tres proveedores de IA. Se retiran la propuesta automática de criterios, los ejercicios de refuerzo y la copia JSON.

## Cómo citar

Borrás Rocher, F. (2026). *CorrigIA* (versión 2.0.0) [Software]. Universidad Miguel Hernández de Elche. https://doi.org/10.5281/zenodo.23055759

El DOI es el de concepto: apunta siempre a la última versión. GitHub ofrece la cita en APA y BibTeX con el botón *Cite this repository*, a partir de `CITATION.cff`.

## Autoría

Fernando Borrás Rocher · Universidad Miguel Hernández de Elche · ORCID [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)

Forma parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT © 2026 Fernando Borrás Rocher · Universidad Miguel Hernández de Elche.
