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

## Pedido para trabajar una unidad

> «Consolidá la unidad N desde sus capturas y material, sin tocar los originales. Declará cobertura,
> depurá el APUNTE.md y verificá todas sus secciones. Informá los controles ejecutados, evidencia y
> pendientes; sólo marcá revisado si pasa la puerta de calidad. Actualizá su índice y dejá el repaso aparte.»

Para entrenar sin modificar archivos:

> «Tomame un simulacro de la unidad N con contenido verificado: una pregunta por vez, sin mostrar la
> respuesta antes de mi intento. Corregí con razones y referencia a la sección y fuente.»
