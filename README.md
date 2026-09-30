# CorrigIA

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23055759.svg)](https://doi.org/10.5281/zenodo.23055759)

**Aplicación:** https://fborrasumh.github.io/corrigia/

Corrección asistida de **exámenes manuscritos** para profesorado universitario. Escaneas o subes las copias de tus estudiantes; la IA lee cada respuesta, la puntúa criterio a criterio con **tu baremo** y redacta un comentario para cada estudiante. Tú revisas lo que propone, ajustas lo que haga falta y exportas las notas, los comentarios y un informe de la clase. Aplicación de un solo fichero (`index.html`), sin servidor ni cuenta, con el diseño de la familia Forja.

Recoge las funcionalidades de herramientas comerciales como Examino, con garantías adicionales pensadas para la evaluación universitaria.

## Cinco pasos

1. **El baremo.** Para cada pregunta: su enunciado, sus puntos, la respuesta esperada y criterios que suman esos puntos. La IA puede proponer el baremo a partir del enunciado (y la solución) en PDF, Word o foto.
2. **Las copias.** Tres formas de cargarlas:
   - un PDF con todo el lote, que se divide según las páginas de cada copia;
   - un fichero por estudiante;
   - fotos con la cámara del móvil.

   Se pueden unir copias, quitar páginas y poner nombres.
3. **La corrección.** Por cada pregunta, la IA transcribe lo escrito, indica qué criterios cumple y justifica la puntuación. Además, redacta un comentario: punto fuerte, dificultad y consejo.
4. **La revisión.** Copia y corrección lado a lado. Cambias cualquier criterio y la nota se recalcula; editas el comentario y marcas la copia como revisada.
5. **Los resultados.** Media, mediana, desviación típica, aprobados, histograma, dominio por pregunta y ejercicios de refuerzo a partir de los errores más repetidos. Exportación de notas a Excel (CSV), informes individuales en Word, informe de la clase en Word y copia completa en JSON.

## Garantías

- **La nota la calcula la app**, sumando los criterios del baremo: nunca se toma una cifra suelta de la IA. Si la IA puntúa un criterio por encima de su máximo, se recorta y se avisa.
- **Lo dudoso no pasa sin mirar.** Las respuestas ilegibles, de baja confianza o sin transcripción se marcan, y las exportaciones indican qué notas no ha revisado el profesor.
- **Anonimización** activa por defecto: se tapa la cabecera de la primera página en la imagen que se envía a la IA.
- **Ejemplo completo sin clave**: tres copias manuscritas simuladas de un parcial de Bioestadística.

## Protección de datos

Las imágenes de las copias se envían a OpenAI con la clave del profesor (guardada en `localStorage` como `ia_openai_key`); no hay servidor intermedio. Todo lo demás, incluidas las imágenes y las correcciones, se guarda en IndexedDB del navegador. **Antes de usarla con estudiantes reales, consulta con tu universidad** si ese tratamiento está cubierto (acuerdo con el proveedor, información al estudiantado) y mantén la anonimización activa.

## Límites

La calidad de la lectura depende del modelo y de la letra. Antes de usarla en un examen real, corrige con ella unas cuantas copias ya calificadas a mano y compara. La IA propone; la nota la pone el profesor.

## Cómo citar

Borrás Rocher, F. (2026). *CorrigIA* (versión 1.0.0) [Software]. Universidad Miguel Hernández de Elche. https://doi.org/10.5281/zenodo.23055759

El DOI es el de concepto: apunta siempre a la última versión. GitHub ofrece la cita en APA y BibTeX con el botón *Cite this repository*, a partir de `CITATION.cff`.

Forma parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT © 2026 Fernando Borrás Rocher · Universidad Miguel Hernández de Elche.
