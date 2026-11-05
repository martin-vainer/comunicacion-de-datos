---
unidad: 8
tipo: cuestionario
estado: borrador
fuentes:
  - apuntes/repaso/recursos/u08-interfaces-digitales/pregunta-01.png
  - apuntes/repaso/recursos/u08-interfaces-digitales/pregunta-02.png
  - apuntes/repaso/recursos/u08-interfaces-digitales/pregunta-03.png
  - apuntes/repaso/recursos/u08-interfaces-digitales/pregunta-04.png
  - material/teoria/U8/U8 Hardware de comunicaciones.pdf
  - UIT-T V.24 (02/2000)
  - UIT-T V.28 (03/1993)
actualizado: 2026-11-05
---

# Cuestionario de teoría — Unidad 8: interfaces digitales

**Alcance:** cuatro preguntas conceptuales de selección simple sobre RS-232, null-módem y V.24. No es un simulacro de la unidad ni cubre las demás interfaces o los módems.

**Cómo usarlo:** elegí una opción y justificá por qué antes de desplegar la resolución. Las capturas se enlazan dentro de cada resolución porque muestran la opción que el aula marcó como correcta. La fecha de la clase no figura en las imágenes; la fecha del encabezado es la de documentación y contraste.

**Fuente de cátedra:** [U8 Hardware de comunicaciones](../../material/teoria/U8/U8%20Hardware%20de%20comunicaciones.pdf), en adelante **H**; la portada es la página 1. Se contrastaron las pp. 8–11, 14 y 16. **Límite:** Q03 y Q04 se conservan para interpretar la devolución del aula, no para calificar automáticamente afirmaciones generales sin precisar su alcance.

## Q01 — Respuesta a RTS

### Enunciado original

En la recomendación RS 232, ¿qué señal es la respuesta a RTS?

Seleccione una:

- a. DSR
- b. Clear to send
- c. Ninguna de las anteriores
- d. RTD
- e. Request to send

### Datos y condiciones

- **Datos numéricos:** no hay.
- **Condición y pedido:** identificar, para RS-232, la señal de control que responde a RTS.

<details>
<summary>Mostrar resolución razonada</summary>

1. **Separá el pedido de la habilitación.** El DTE activa RTS (*Request to Send*) para pedir la emisión. En la secuencia estudiada, el DCE responde con CTS (*Clear to Send*) cuando está en condiciones de aceptar los datos del DTE para transmitirlos.
2. **Respuesta marcada por el aula: b. Clear to send.**
3. **Distractores:** a indica que el DCE está listo (DSR), no que responde al pedido de emisión; c no aplica porque CTS está entre las opciones; d no corresponde a la señal de respuesta de la secuencia; e desarrolla RTS, el pedido original.

**Evidencia:** [captura Q01](recursos/u08-interfaces-digitales/pregunta-01.png); H pp. 10–11; [apunte U8: establecimiento](../teoria/08-hardware-comunicaciones/APUNTE.md#establecimiento); [UIT-T V.24, §§3.7–3.8 y 4.3.1](https://www.itu.int/rec/T-REC-V.24-200002-I/en), circuitos 105 y 106 y su interacción.

</details>

## Q02 — Función de SIG

### Enunciado original

En la recomendación RS 232, ¿qué función cumple el circuito SIG?

Seleccione una:

- a. Detección de señal de llamada.
- b. Respuesta sólo sentido DTE DCE
- c. Ninguna de las anteriores
- d. Retorno común de señales.
- e. Seguridad eléctrica.

### Datos y condiciones

- **Datos numéricos:** no hay.
- **Condición y pedido:** identificar la función de SIG en la interfaz RS-232.

<details>
<summary>Mostrar resolución razonada</summary>

1. **Buscá la referencia de tensión.** El receptor necesita una referencia común para interpretar los niveles eléctricos. En las filminas, SIG es la tierra de señalización: sirve de referencia y retorno común, no de señal de control.
2. **Respuesta marcada por el aula: d. Retorno común de señales.**
3. **Distractores:** a es función de RI; b confunde un retorno común con una señal de control direccional; c no aplica porque la función figura en d; e confunde la tierra de señalización con la tierra de protección, que la filmina rotula GND.

**Evidencia:** [captura Q02](recursos/u08-interfaces-digitales/pregunta-02.png); H pp. 9–10, circuito 102; [apunte U8: señales](../teoria/08-hardware-comunicaciones/APUNTE.md#senales); [UIT-T V.24, §3.1](https://www.itu.int/rec/T-REC-V.24-200002-I/en).

</details>

## Q03 — Cable null módem

### Enunciado original

En la recomendación RS 232, ¿qué afirmación es correcta respecto del cable null módem?

Seleccione una:

- a. La longitud máxima es de 30 metros.
- b. Tiene el mismo tipo de conector en ambos extremos.
- c. Deben cruzarse los conductores de GND y SIG.
- d. No deben cruzarse los conductores de RTS con CTS
- e. Ninguna de las anteriores

### Datos y condiciones

- **Dato en una opción:** 30 metros; es una afirmación a evaluar, no una premisa confirmada.
- **Condición y pedido:** seleccionar la afirmación correcta sobre el cable null módem. El enunciado no especifica un esquema de cableado ni los conectores de los equipos.

<details>
<summary>Mostrar resolución razonada y salvedad</summary>

1. **Seguí las señales, no la forma del conector.** Para unir dos DTE sin módem, la salida de datos de cada equipo tiene que llegar a la entrada del otro (TD ↔ RD). La referencia de señal se conecta con su equivalente.
2. **Respuesta marcada por el aula: b. Tiene el mismo tipo de conector en ambos extremos.** Coincide con el ejemplo DB-25 de la cátedra, que muestra dos fichas hembra. No es una condición general: [Lantronix documenta un null-módem con DE-9 y DB-25](https://ltrxdev.atlassian.net/wiki/spaces/LTRXTS/pages/105906724/RS232%2BSerial%2BCable%2BWiring), apartado «PC to DTE DB25». La función la determina el cableado, no la igualdad de conectores.
3. **Distractores en la lectura de cátedra:** a no es un máximo propio del null-módem ni se desprende del material; c confunde el retorno de señal con la protección (H p. 14 conserva SIG de extremo a extremo); d no vale como regla: H p. 14 usa puentes locales y H p. 16 muestra un cruce RTS/CTS entre extremos; e no coincide con la corrección del aula porque b describe el montaje ilustrado. Sin esa referencia implícita, b no se sostiene como regla general.

**Evidencia:** [captura Q03](recursos/u08-interfaces-digitales/pregunta-03.png); H pp. 8, 10, 14 y 16; [apunte U8: cables y variantes](../teoria/08-hardware-comunicaciones/APUNTE.md#cables). El cable con fichas diferentes es un contraejemplo documentado por el fabricante, no un ejemplo de la cátedra.

</details>

## Q04 — Alcance de V.24

### Enunciado original

En la recomendación V.24, ¿qué afirmación es incorrecta?

Seleccione una:

- a. La longitud máxima es de 15 metros.
- b. Ninguna de las anteriores
- c. El conector principal es el DB 25
- d. Prevee una caída de tensión de 2 v entre extremos
- e. Es una interfaz DTE DTE

### Datos y condiciones

- **Datos en las opciones:** 15 metros, DB 25 y 2 v; son afirmaciones a evaluar, no premisas confirmadas.
- **Condición y pedido:** seleccionar la afirmación **incorrecta**. La consigna dice V.24; las filminas estudian el conjunto bajo el rótulo «RS 232 / V.24».

<details>
<summary>Mostrar resolución razonada y salvedad</summary>

1. **Identificá los roles.** En la interfaz de referencia, los circuitos de intercambio conectan un DTE (equipo terminal de datos) con un DCE (equipo de terminación del circuito de datos). No es el montaje DTE–DTE de un null-módem.
2. **Respuesta marcada por el aula: e. Es una interfaz DTE DTE.** Es incorrecta para V.24.
3. **Distractores en la lectura de cátedra:** a toma los 15 m del caso clásico mostrado en H p. 8; c toma el DB-25 ilustrado en esa misma página, junto al de nueve contactos; d toma el margen de 2 V entre los niveles de emisión y recepción de H p. 9; b no identifica la afirmación incorrecta de la clave.
4. **Salvedad normativa:** V.24 define circuitos y remite lo eléctrico y lo mecánico a otras normas. No fija por sí sola un máximo universal de 15 m ni un único conector; su §2 vincula la longitud con la carga capacitiva y otras características eléctricas aplicables. Los 2 V son la diferencia entre 5 V y 3 V en magnitud para los niveles del ejemplo, **no** una caída de tensión fija entre extremos. Por eso, si se lee la consigna como una pregunta estricta sobre V.24, e sigue siendo falsa, pero a, c y d tampoco pueden tomarse como afirmaciones normativas tal como están escritas.

**Evidencia:** [captura Q04](recursos/u08-interfaces-digitales/pregunta-04.png); H pp. 8–9; [apunte U8: RS-232 / V.24](../teoria/08-hardware-comunicaciones/APUNTE.md#rs232); [UIT-T V.24, §§1.1–1.3 y 2](https://www.itu.int/rec/T-REC-V.24-200002-I/en) y [UIT-T V.28, §§4–5](https://www.itu.int/rec/T-REC-V.28-199303-I/en).

</details>
