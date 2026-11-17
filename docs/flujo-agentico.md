# Flujo agéntico de estudio

Este documento explica **cómo trabajar** con un agente. Las reglas pedagógicas viven únicamente en
[`apuntes/_plantillas/metodologia.md`](../apuntes/_plantillas/metodologia.md) y las instrucciones
obligatorias en [`AGENTS.md`](../AGENTS.md). El repositorio sigue siendo utilizable sin agentes ni
Engram.

## Circuito cotidiano

```text
capturar → proponer integración → contrastar → consolidar → practicar
```

1. **Capturar:** el estudiante registra originales nuevos durante la clase con la
   [plantilla mínima](../apuntes/_plantillas/captura-clase.md) dentro de `capturas/`. No exigir YAML ni
   pulir redacción; guardar las imágenes junto al Markdown para que sus enlaces relativos sobrevivan.
   Los agentes consultan esas capturas, no las modifican: Markdown, imágenes y anexos actuales o futuros
   permanecen como evidencia original, aun después de consolidar su contenido.
2. **Proponer integración:** identificar unidades y temas posibles; actualizar la bitácora. No
   corregir, mover, renombrar ni borrar ningún original dentro o fuera de `capturas/`.
3. **Contrastar:** localizar el material original y su cache; verificar conceptos, figuras, cuentas,
   unidades y supuestos contra el original.
4. **Consolidar:** para U1–U8, integrar `capturas/` + `material/` como secciones del único `APUNTE.md` de la
   unidad; mantener `INDICE.md` como navegación breve y conservar la procedencia por sección. Llevar
   ejercicios resueltos y actividades de repaso por separado. Anotar cada verificación pendiente junto
   a la sección afectada. Antes de declararlo final, aplicar la
   [puerta de calidad](../apuntes/_plantillas/metodologia.md#puerta-de-calidad) a la unidad entera.
5. **Practicar:** mantener el enunciado de fuente literal, después los datos/condiciones extraídos y
   luego la resolución paso a paso; conservar desarrollos correctos y ampliarlos pedagógicamente sin
   reescribirlos de más. Ejercicios y autoevaluación van separados del apunte teórico; responder de a
   una y corregir el razonamiento. Para generar cuestionarios o simulacros, seguir el
   [protocolo de repaso](../apuntes/_plantillas/metodologia.md#cuestionarios-simulacros): cobertura y
   evidencia por pregunta, respuestas separadas cuando permitan autoevaluación y corrección razonada.
   Para nuevos archivos de repaso, usar la [plantilla de cuestionario](../apuntes/_plantillas/cuestionario-repaso.md).

<a id="parciales"></a>
## Parciales: fotos originales y resoluciones

| Instancia | Unidades | Fotos originales | Resolución |
|---|---|---|---|
| Primer parcial, primera instancia, Tema J | U1–U4 | [`primer_parcial/`](../primer_parcial/) · [hoja 1](../primer_parcial/1.jpeg) · [hoja 2](../primer_parcial/2.jpeg) | [10 preguntas resueltas](../apuntes/repaso/primer-parcial-u01-u04-tema-j.md) |
| Primer parcial, Tema F (instancia no indicada) | U1–U4 | Misma hoja: [vista general](../primer_parcial/tema-f/hoja-1-vista-general.png) · [detalle superior](../primer_parcial/tema-f/hoja-1-detalle-superior.png) · [detalle inferior](../primer_parcial/tema-f/hoja-1-detalle-inferior.png) | [5 consignas resueltas](../apuntes/repaso/primer-parcial-u01-u04-tema-f.md) |
| Primer parcial, tema e instancia no visibles | U1–U4 | [hoja fotografiada](../primer_parcial/tema-no-visible/hoja-1.png) | [5 consignas resueltas](../apuntes/repaso/primer-parcial-u01-u04-tema-no-visible.md) |
| Segundo parcial, Tema G | U5–U8 | [`segundo_parcial/`](../segundo_parcial/) · [hoja 1](../segundo_parcial/1.jpeg) · [hoja 2](../segundo_parcial/2.jpeg) | [10 preguntas resueltas](../apuntes/repaso/segundo-parcial-u05-u08-tema-g.md). El [cuestionario de repaso U5–U8](../apuntes/repaso/segundo-parcial-u05-u08.md) es otro recurso. |

Las carpetas guardan evidencia original, no soluciones. No editar, mover ni renombrar las fotos. Cuando se pida resolver un examen, transcribir las preguntas y opciones impresas, separar los datos y justificar cada respuesta en `apuntes/repaso/` con referencias al apunte, a los TPs pertinentes y al material de cátedra. Las marcas de estudiantes no se usan como clave. Si la opción correcta no figura o la consigna depende de una convención, explicitarlo con evidencia, sin corregir silenciosamente el enunciado.

## Roles

### Curador

Clasifica una captura, ubica material y propone destinos. No convierte incertidumbre en certeza ni
reescribe contenido académico sin autorización.

> «Actuá como Curador. Clasificá esta clase, proponé destinos por tema y actualizá la bitácora. No
> consolides ni corrijas todavía.»

### Tutor

Explica desde el fenómeno físico hacia el modelo y la formalización. En ejercicios guía el método
antes del resultado; hace una pregunta concreta y espera la respuesta.

> «Actuá como Tutor. Explicame ancho de banda usando los apuntes revisados y después haceme una sola
> pregunta de control. No modifiques archivos.»

### Verificador

Contrasta afirmaciones, diagramas, notación, unidades, cálculos y supuestos con el material original.
Registra discrepancias; no las promedia ni las corrige en silencio.

> «Actuá como Verificador. Revisá todas las secciones del `APUNTE.md` de la unidad contra las fuentes
> originales, listá evidencia y pendientes por sección. No cambies el estado de la unidad a `revisado`
> si queda una discrepancia material o una sección sin contrastar.»

## Autorización para editar

Consultar, explicar, evaluar o verificar **no autoriza cambios**. Para editar, el pedido debe decirlo:

> «Consolidá esta captura como sección del `APUNTE.md` canónico de su unidad, conservá la procedencia y
> actualizá el `INDICE.md` y la bitácora. Dejá ejercicios y repaso separados.»

Antes de leer en profundidad, el agente abre la portada o la bitácora, luego el `INDICE.md` de la unidad
y recién después el `APUNTE.md` canónico y las fuentes estrictamente necesarias.

## Cierre de cambios con Git

1. Antes de editar, revisá `git status --short` para distinguir los cambios que ya existían de los tuyos.
2. Al terminar cada cambio lógico, verificá su contenido y revisá el diff. Prepará sólo los archivos o bloques propios; comprobá el alcance con `git diff --cached` antes de commitear.
3. Cerrá el cambio con un commit según [las reglas de Git](../AGENTS.md#8-git) e informá su hash. Una consulta sin cambios no requiere commit.

## Pedido para trabajar una unidad

> «Consolidá la unidad N desde sus capturas y material, sin tocar los originales. Declará cobertura,
> depurá el APUNTE.md y verificá todas sus secciones. Informá los controles ejecutados, evidencia y
> pendientes; sólo marcá revisado si pasa la puerta de calidad. Actualizá su índice y dejá el repaso aparte.»

Para entrenar sin modificar archivos:

> «Tomame un simulacro de la unidad N con contenido verificado: una pregunta por vez, sin mostrar la
> respuesta antes de mi intento. Corregí con razones y referencia a la sección y fuente.»
