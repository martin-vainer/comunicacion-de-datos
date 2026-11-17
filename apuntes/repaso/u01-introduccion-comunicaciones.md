---
unidad: 1
estado: completo
fuentes:
  - "capturas/teoria/Cuestionarios/cuestionario U1 y U2.md, preguntas 1–3"
  - "material/teoria/U1/U1 Introduccion a las comunicaciones.pdf, pp. 6, 10–20"
  - "UIT-T V.24 (02/2000), descripción oficial; acceso 2026-10-10"
actualizado: 2026-10-13
---

# U1 — Repaso del cuestionario registrado

**Alcance:** sólo las preguntas 1–3 del cuestionario U1/U2 ya registrado. Modalidad: elección de opción y justificación conceptual; nivel introductorio. No es un simulacro nuevo ni evalúa U1 completa. Q4–7 corresponden a U2; no se incluyen modalidades pendientes ni conocimientos añadidos para ampliar el examen.

**Cómo usarlo:** respondé una pregunta por vez y justificá el límite o la función antes de mirar las soluciones. En una sesión con Tutor, esperar el intento antes de corregir. Las marcas de respuesta del original se quitaron de los enunciados para permitir autoevaluación; **el original no fue modificado**.

## Trazabilidad por pregunta

| ID | Origen inmutable | Sección para estudiar | Evidencia de contraste |
|---|---|---|---|
| U1-Q01 | [Cuestionario, Pregunta 1](../../capturas/teoria/Cuestionarios/cuestionario%20U1%20y%20U2.md#pregunta-1--circuito-teleinformático-básico) | [ETD, ECD y circuito](../teoria/01-introduccion-comunicaciones/APUNTE.md#circuito-y-enlace) | Teoría U1 p. PDF6; práctica `UT 1 COMUNICACIONES.pdf`, p. PDF4; diagramas inspeccionados. |
| U1-Q02 | [Cuestionario, Pregunta 2](../../capturas/teoria/Cuestionarios/cuestionario%20U1%20y%20U2.md#pregunta-2--modelo-osi) | [Modelo OSI](../teoria/01-introduccion-comunicaciones/APUNTE.md#modelo-osi) | Teoría U1 pp. PDF10–14 y19; descripción oficial de V.24, enlace en solución. |
| U1-Q03 | [Cuestionario, Pregunta 3](../../capturas/teoria/Cuestionarios/cuestionario%20U1%20y%20U2.md#pregunta-3--modelo-osi) | [Modelo OSI](../teoria/01-introduccion-comunicaciones/APUNTE.md#modelo-osi) | Teoría U1 pp. PDF10–14 y19; V.24, enlace en solución. |

Las páginas de teoría son de [U1 Introduccion a las comunicaciones.pdf](../../material/teoria/U1/U1%20Introduccion%20a%20las%20comunicaciones.pdf). El PDF es la autoridad; su cache sólo ayudó a buscar. Las soluciones explican cada alternativa, no sólo la correcta.

<a id="enunciados"></a>
## Preguntas y respuestas

### U1-Q01 — Circuito teleinformático básico

> **Enunciado (transcripción literal; captura, Pregunta 1):**
>
> **El circuito de datos de un Circuito Teleinformático Básico comprende:**
>
> 1. El ECD y el ETD
> 2. Ninguna de las opciones son elegibles
> 3. El ECD, el medio de comunicaciones y el ETD
> 4. Sólo el medio de comunicaciones
> 5. El ECD y el medio de comunicaciones

**Datos / condiciones:** no hay datos numéricos; se evalúa qué elementos comprende el circuito de datos en el modelo básico.

<a id="soluciones"></a>

#### U1-Q01 — Opción 5

El circuito de datos abarca **ECD del extremo A + medio + ECD del extremo B**. Los ETD producen o consumen los datos, pero no pertenecen al límite CD dibujado en teoría p. 6. La opción usa el singular «el ECD» como categoría de equipo; no elimina el ECD del otro extremo.

- **1:** agrega ETD y omite el medio; no describe CD.
- **2:** no corresponde porque 5 sí coincide con el dibujo.
- **3:** incluye ETD, por lo que excede CD.
- **4:** omite los equipos que adaptan los datos al circuito.
- **5:** reúne las categorías correctas: ECD y medio.

**Criterio de corrección:** elegir 5 y explicar los dos ECD y el medio, diferenciando el enlace entre ETD. Nombrar sólo «ECD a ECD» sin reconocer el medio deja incompleta la justificación.

### U1-Q02 — Modelo OSI: afirmación correcta

> **Enunciado (transcripción literal; captura, Pregunta 2):**
>
> **¿Qué afirmación es correcta respecto del modelo OSI?**
>
> a. Es un estándar del IEEE
>
> b. La norma V.24 es de la capa 1
>
> c. Ninguna de las anteriores
>
> d. Entre capas iguales se usan interfaces
>
> e. La compresión de datos es de la capa 5

**Datos / condiciones:** no hay datos numéricos; se evalúan afirmaciones conceptuales sobre el modelo OSI y V.24.

#### U1-Q02 — Opción b

La capa física define características mecánicas, eléctricas, funcionales y de procedimiento para transmitir bits. **V.24** define circuitos de intercambio entre ETD y ECD y se asocia a esa interfaz física en el cuestionario. Ver [UIT-T, V.24 (02/2000), título oficial](https://www.itu.int/rec/T-REC-V.24/en), consultado el 10/10/2026; no afirmar que V.24 especifica por sí sola todos los parámetros eléctricos ni que es idéntica a RS-232.

- **a:** OSI es el modelo de referencia de **ISO**, no IEEE (teoría p. 10).
- **b:** correcta según la interfaz física y el enfoque de Q2.
- **c:** falsa porque b es correcta.
- **d:** entre entidades pares de distintos sistemas se usan **protocolos**; las interfaces son entre capas adyacentes de un mismo sistema (p. 12).
- **e:** la compresión se presenta en **capa 6, presentación**, no en capa 5, sesión (p. 19).

**Criterio de corrección:** elegir b y reconocer el papel de la interfaz física; justificar protocolo/interfaz y presentación/sesión. La mera sigla sin función no alcanza para mostrar comprensión.

### U1-Q03 — Modelo OSI: afirmación incorrecta

> **Enunciado (transcripción literal; captura, Pregunta 3):**
>
> **¿Qué afirmación es incorrecta respecto del modelo OSI?**
>
> a. Es un estándar del IEEE
>
> b. Entre capas iguales se usan protocolos
>
> c. La norma V.24 es de la capa 1
>
> d. La criptografía es de la capa 6
>
> e. Ninguna de las anteriores

**Datos / condiciones:** no hay datos numéricos; hay que identificar la afirmación incorrecta entre las cinco opciones conceptuales.

#### U1-Q03 — Opción a

Se pide la afirmación **incorrecta**. La opción a atribuye OSI al IEEE, pero teoría p. 10 lo identifica como modelo de referencia de **ISO**. No confundas «organismo que normaliza redes» con «organismo que desarrolló este modelo».

- **a:** incorrecta, es la que debe marcarse.
- **b:** verdadera si «iguales» se entiende como entidades pares de la misma capa en sistemas distintos: cooperan mediante protocolos.
- **c:** verdadera en el sentido físico de V.24 explicado en Q2.
- **d:** verdadera dentro del reparto de funciones del modelo: la criptografía se presenta en capa 6. Esto no prohíbe implementaciones de cifrado en otros niveles de una tecnología real.
- **e:** no corresponde: a sí es incorrecta.

**Criterio de corrección:** elegir a, decir ISO y distinguir modelo abstracto de los organismos/protocolos concretos. Marcar b por confundir protocolo con interfaz invalida el razonamiento.

## Registro de comprobación

10/10/2026: cotejadas las tres preguntas con la captura inmutable; retiradas sólo sus marcas de respuesta en esta copia pedagógica. Cotejados visualmente los límites ED/CD, ISO, pares/adyacentes y presentación en las páginas indicadas; comprobado el alcance oficial de V.24. Enlaces locales y anclas resueltos por script. No hay cálculos ni datos numéricos de ejercicio; no se inventaron preguntas o puntajes. La revisión independiente del paquete sigue pendiente, y este repaso parcial NO certifica toda la unidad.
