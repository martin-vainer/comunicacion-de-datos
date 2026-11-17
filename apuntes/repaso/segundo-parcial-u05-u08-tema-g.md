---
unidades: [5, 6, 7, 8]
tipo: cuestionario
estado: completo
fuentes:
  - segundo_parcial/1.jpeg
  - segundo_parcial/2.jpeg
actualizado: 2026-11-17
---

# Segundo parcial — Tema G (U5–U8)

**Alcance:** las diez preguntas de opción múltiple de las dos hojas fotografiadas. Hay reconocimiento de conceptos y dos cálculos directos. La cobertura corresponde a estas consignas, no a todo el programa de U5–U8. La fecha no está indicada en las hojas y las respuestas no son una clave oficial.

**Fuente del enunciado:** [hoja 1 (Q01–Q06)](../../segundo_parcial/1.jpeg) y [hoja 2 (Q07–Q10)](../../segundo_parcial/2.jpeg). Este examen es distinto del [cuestionario de repaso U5–U8](segundo-parcial-u05-u08.md). Para usarlo de autoevaluación, elegí y justificá una opción antes de desplegar la resolución.

<details>
<summary>Mostrar clave rápida</summary>

**1b · 2c · 3c · 4c · 5b · 6c · 7c · 8c · 9b · 10d.** Q01 se lee en el sentido de codificación de canal; Q10 se responde según la clasificación de cátedra.

</details>

<a id="q01"></a>
## Q01 — Objetivo de la codificación

### Enunciado original

> ¿Cuál es el objetivo principal de la Teoría de la Codificación?
>
> a) Medir la cantidad de información en una fuente.
>
> b) Asegurar que la información se transmita con la menor cantidad de errores posible, incluso en presencia de ruido o interferencias.
>
> c) Determinar la capacidad máxima de un canal sin ruido.
>
> d) Diseñar interfaces digitales para la conexión de dispositivos.
>
> e) Ninguna de las opciones.

**Datos y condiciones:** no hay datos numéricos. Se pide identificar un objetivo; la opción b) plantea un canal con posibles perturbaciones.

<details>
<summary>Mostrar resolución razonada</summary>

1. Si el ruido altera bits, al receptor no le alcanza con saber cómo se representan los datos: necesita distinguir una palabra válida de una recibida con errores. La **codificación de canal** agrega redundancia estructurada para detectarlos o corregirlos dentro de los límites del código; no elimina el ruido físico.
2. **Respuesta: b).** Es la opción que describe ese objetivo. La consigna dice «Teoría de la Codificación» en sentido amplio, pero b) apunta específicamente a proteger la transmisión. No la confundas con la **codificación de fuente**, que busca representar los datos de manera más compacta.
3. **Distractores:** a) describe la medición de información de la fuente; c) corresponde al estudio de capacidad del canal ideal; d) trata de interfaces físicas, no de cómo se protege el mensaje; e) no aplica porque b) sí responde en el sentido indicado.

**Evidencia:** [hoja 1, pregunta 1](../../segundo_parcial/1.jpeg); [U5, codificación de fuente y de canal](../teoria/05-teoria-informacion-codificacion/APUNTE.md#codificacion); [filmina U5, p. 2](../../material/teoria/U5/U%205%20TI%20y%20codific.pdf#page=2) distingue medición, capacidad y codificación; [filmina U6, p. 22](../../material/teoria/U6/U%206%20Canales%20de%20Comunicaciones%20y%20control%20de%20errores.pdf#page=22) ubica los métodos de control de errores.

</details>

<a id="q02"></a>
## Q02 — Distancia de Hamming y corrección garantizada

### Enunciado original

> Si un código tiene una distancia Hamming mínima de 7, ¿cuántos errores puede corregir como máximo?
>
> a) Hasta 1 error
>
> b) Hasta 2 errores
>
> c) Hasta 3 errores
>
> d) Hasta 4 errores
>
> e) Ninguna de las opciones

**Datos y condiciones:** distancia de Hamming mínima de 7 posiciones de bit. Se pide el máximo de errores cuya corrección está garantizada por palabra de código, no cuántos se pueden detectar.

<details>
<summary>Mostrar resolución razonada</summary>

1. Dos palabras válidas están separadas por al menos 7 cambios de bit. Si la palabra recibida está a 3 cambios o menos de la enviada, queda a 4 cambios o más de cualquier otra palabra válida. Así, elegir la más cercana no genera ambigüedad.
2. Para un código de bloque binario y errores de sustitución, con decodificación por mínima distancia, el máximo garantizado en el peor caso es:

$$
t=\left\lfloor\frac{d_{\min}-1}{2}\right\rfloor
=\left\lfloor\frac{7-1}{2}\right\rfloor=3.
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $d_{\min}$ | Menor distancia entre dos palabras válidas | Posiciones de bit distintas |
| $t$ | Máximo de errores siempre corregibles | Bits erróneos por palabra |

3. **Respuesta: c) Hasta 3 errores.**
4. **Distractores:** a) y b) están dentro del alcance, pero no son el máximo; d) no se puede garantizar: entre dos palabras separadas por 7 hay una recibida a 4 cambios de una y 3 de la otra, y cualquiera podría ser la enviada si se admiten hasta 4 cambios; e) se descarta porque c) coincide. En modo de sólo detección, hasta 6 cambios no pueden transformar una palabra válida en otra; detectar no es corregir.

**Evidencia:** [hoja 1, pregunta 2](../../segundo_parcial/1.jpeg); [U6, códigos autocorrectores](../teoria/06-canales-comunicaciones/APUNTE.md#hamming); [Tratamiento de los errores, p. 16](../../material/practica/U%206/UT%20Nro%206%20TRATAMIENTO%20DE%20LOS%20ERRORES.pdf#page=16), límites de detección y corrección.

</details>

<a id="q03"></a>
## Q03 — Unidad de información con base diez

### Enunciado original

> Si en la fórmula para medir la información, $I(xi) = \log_b (1 / P(xi))$, la base (b) es 10, ¿qué unidad de información se utiliza?
>
> a) Shannon
>
> b) Nat
>
> c) Hartley
>
> d) Bit
>
> e) Ninguna de las opciones.

**Datos y condiciones:** la base del logaritmo es 10. No se da una probabilidad concreta; se pide la unidad, no la cantidad de información.

<details>
<summary>Mostrar resolución razonada</summary>

1. Un resultado menos probable aporta más información al observarlo. La base del logaritmo fija la escala con la que medimos esa información; no modifica la probabilidad del resultado.

| Símbolo | Significado | Unidad |
|---|---|---|
| $I(xi)$ | Información del resultado $xi$ | Hartley para base 10 |
| $P(xi)$ | Probabilidad del resultado, mayor que cero y a lo sumo uno | Adimensional |
| $b$ | Base del logaritmo | Adimensional |

2. **Ejemplo didáctico:** si un resultado tiene probabilidad $0{,}1$, entonces $\log_{10}(1/0{,}1)=\log_{10}(10)=1$ Hartley.
3. **Respuesta: c) Hartley.**
4. **Distractores:** a) corresponde a base 2; b) a base natural $e$; d) como unidad de información equivale al Shannon (base 2), y como dígito designa un 0 o un 1; e) no aplica.

**Evidencia:** [hoja 1, pregunta 3](../../segundo_parcial/1.jpeg); [U5, unidades y dígitos binarios](../teoria/05-teoria-informacion-codificacion/APUNTE.md#unidades); [filminas U5, pp. 4–5](../../material/teoria/U5/U%205%20TI%20y%20codific.pdf#page=4).

</details>

<a id="q04"></a>
## Q04 — Entropía de una fuente de memoria nula

### Enunciado original

> ¿Qué describe la Entropía de una fuente de memoria nula?
>
> a) La cantidad de bits en los que difieren dos secuencias
>
> b) La máxima velocidad de transmisión que se puede cursar libre de errores
>
> c) El valor medio de información o incertidumbre de una fuente
>
> d) La disminución de la intensidad de la señal útil
>
> e) Ninguna de las opciones.

**Datos y condiciones:** la fuente es de memoria nula: conocer los símbolos anteriores no cambia las probabilidades del próximo. No se dan probabilidades ni tasa de emisión.

<details>
<summary>Mostrar resolución razonada</summary>

1. Cada resultado aporta una cantidad de información según su probabilidad. La entropía hace el promedio ponderado de esos aportes: mide la incertidumbre **por símbolo** antes de observarlo. Por ejemplo, una fuente binaria sin memoria y equiprobable aporta en promedio 1 bit/símbolo; si siempre emite lo mismo, aporta 0 bit/símbolo. Memoria nula no significa entropía nula.
2. **Respuesta: c) El valor medio de información o incertidumbre de una fuente.**
3. **Distractores:** a) define la distancia de Hamming; b) apunta a la capacidad del canal, una tasa en bit/s, no una medida de la fuente en bit/símbolo; d) describe atenuación; e) no aplica.

**Evidencia:** [hoja 1, pregunta 4](../../segundo_parcial/1.jpeg); [U5, entropía](../teoria/05-teoria-informacion-codificacion/APUNTE.md#entropia); [filminas U5, pp. 5–7](../../material/teoria/U5/U%205%20TI%20y%20codific.pdf#page=5); [TP5, E7](../practica/tp-05-informacion-codificacion.md#ejercicio-07).

</details>

<a id="q05"></a>
## Q05 — Teorema de Shannon-Hartley

### Enunciado original

> El Teorema de Shannon-Hartley es importante porque relaciona fundamentalmente:
>
> a) La velocidad de transmisión y el retardo de grupo
>
> b) El ancho de banda y la relación señal/ruido (S/N)
>
> c) La atenuación y la distancia
>
> d) La singularidad y la longitud de bloque de un código
>
> e) Ninguna de las opciones.

**Datos y condiciones:** no hay datos numéricos. Se pide identificar qué magnitudes vincula el teorema al determinar la capacidad del canal.

<details>
<summary>Mostrar resolución razonada</summary>

1. El canal sólo deja pasar una banda de frecuencias y el ruido dificulta distinguir las señales recibidas. Juntas, esas restricciones limitan cuánta información por segundo se puede enviar con probabilidad de error arbitrariamente pequeña. Para un canal limitado en banda con ruido blanco gaussiano aditivo y potencia media de señal limitada:

$$
C=B\log_2\left(1+\frac{S}{N}\right).
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $C$ | Capacidad teórica del canal | bit/s |
| $B$ | Ancho de banda (la filmina usa $\Delta f$) | Hz |
| $S$, $N$ | Potencias medias de señal y ruido en la banda | W |
| $S/N$ | Relación de potencias | Adimensional (veces, no dB) |

2. **Ejemplo didáctico:** con 3 000 Hz de ancho de banda y señal y ruido de igual potencia ($S/N=1$ vez, o 0 dB), se obtiene $3\,000\log_2(2)=3\,000$ bit/s. No es la tasa efectiva de un equipo particular.
3. **Respuesta: b) El ancho de banda y la relación señal/ruido (S/N).** Son las dos entradas que determinan la capacidad en este modelo.
4. **Distractores:** a) el teorema sí da un límite de tasa, pero el retardo de grupo no aparece; c) la atenuación puede afectar indirectamente a $S/N$, pero ni ella ni la distancia son las variables de la fórmula; d) son propiedades de un código; e) no aplica.

**Evidencia:** [hoja 1, pregunta 5](../../segundo_parcial/1.jpeg); [U6, Shannon-Hartley](../teoria/06-canales-comunicaciones/APUNTE.md#shannon); [filminas U6, pp. 6–7](../../material/teoria/U6/U%206%20Canales%20de%20Comunicaciones%20y%20control%20de%20errores.pdf#page=6); [TP6, primera parte, E1](../practica/tp-06-canales.md#p1-e1) para practicar con una relación dada en dB.

</details>

<a id="q06"></a>
## Q06 — Origen del ruido de Johnson

### Enunciado original

> El ruido blanco, gaussiano o de Johnson, se produce principalmente por:
>
> a) Acoplamiento inductivo entre líneas que transportan señales
>
> b) Comportamiento no lineal en transmisores o receptores
>
> c) La agitación térmica de los electrones presente en los medios de transmisión y dispositivos electrónicos
>
> d) Picos de corta duración, pero de gran amplitud que aparecen a intervalos irregulares
>
> e) Ninguna de las opciones.

**Datos y condiciones:** no se dan temperatura, ancho de banda ni potencia. Se pregunta por el origen físico del ruido que la cátedra identifica como térmico o de Johnson.

<details>
<summary>Mostrar resolución razonada</summary>

1. Incluso sin transmitir una señal, la agitación térmica de los portadores de carga produce fluctuaciones eléctricas en elementos resistivos. «De Johnson» identifica ese origen; «blanco» describe una densidad espectral aproximadamente plana en la banda de interés; «gaussiano» describe la distribución de amplitudes del modelo. No son tres nombres intercambiables para cualquier ruido.
2. **Respuesta: c).** La causa pedida es la agitación térmica de los electrones.
3. **Distractores:** a) describe diafonía por acoplamiento; b) puede generar productos de intermodulación cuando se mezclan señales; d) describe ruido impulsivo por su forma temporal; e) no aplica.

**Evidencia:** [hoja 1, pregunta 6](../../segundo_parcial/1.jpeg); [U6, tipos de ruido](../teoria/06-canales-comunicaciones/APUNTE.md#ruido); [filminas U6, pp. 10–13](../../material/teoria/U6/U%206%20Canales%20de%20Comunicaciones%20y%20control%20de%20errores.pdf#page=10).

</details>

<a id="q07"></a>
## Q07 — Corrección de errores hacia atrás

### Enunciado original

> ¿Cuál es un método de corrección de errores hacia atrás?
>
> a) FEC (Forward Error Correction)
>
> b) Código Hamming
>
> c) ARQ (Automatic Repeat Request)
>
> d) Checksum
>
> e) Ninguna de las opciones.

**Datos y condiciones:** no hay datos numéricos. Se pide reconocer el mecanismo de recuperación hacia atrás, no sólo una técnica de detección.

<details>
<summary>Mostrar resolución razonada</summary>

1. Si un bloque llega dañado, el receptor puede detectar el problema y la comunicación puede recuperarse con otro envío del bloque. En **ARQ** hay realimentación: por ejemplo, si no llega una confirmación positiva antes de vencer el temporizador, el emisor vuelve a transmitir. «Hacia atrás» alude al retorno de información de control, no a reparar el bloque cambiando bits en el receptor.
2. **Respuesta: c) ARQ (Automatic Repeat Request).**
3. **Distractores:** a) FEC es corrección hacia adelante, sin solicitar repetición para corregir dentro del alcance del código; b) Hamming es un ejemplo de código autocorrector en el receptor; d) un checksum puede ayudar a detectar el error, pero no organiza la retransmisión ni corrige por sí solo; e) no aplica.

**Evidencia:** [hoja 2, pregunta 7](../../segundo_parcial/2.jpeg); [U6, ARQ](../teoria/06-canales-comunicaciones/APUNTE.md#arq) y [FEC](../teoria/06-canales-comunicaciones/APUNTE.md#fec); [filminas U6, pp. 29 y 31–35](../../material/teoria/U6/U%206%20Canales%20de%20Comunicaciones%20y%20control%20de%20errores.pdf#page=31); [TP6, segunda parte, E2](../practica/tp-06-canales.md#p2-e2).

</details>

<a id="q08"></a>
## Q08 — Guiado en fibra óptica

### Enunciado original

> La Fibra Óptica funciona principalmente basándose en el principio de:
>
> a) Difracción de la luz
>
> b) Atenuación por impurezas
>
> c) Reflexión Total Interna (RTI)
>
> d) Dispersión cromática
>
> e) Ninguna de las opciones.

**Datos y condiciones:** no se dan índices de refracción ni ángulos; se pregunta qué fenómeno permite guiar la luz, no calcular el ángulo crítico.

<details>
<summary>Mostrar resolución razonada</summary>

1. En el modelo de rayos de una fibra de índice escalonado, el núcleo tiene mayor índice de refracción que el revestimiento. Si el rayo llega a esa frontera desde el núcleo con un ángulo mayor que el crítico, medido desde la **normal**, se refleja hacia el núcleo. A igualdad con el crítico se tiene el caso límite: el rayo refractado sería rasante, a 90° de la normal.
2. **Respuesta: c) Reflexión Total Interna (RTI).**
3. **Distractores:** a) la difracción no es el principio de guiado del modelo; b) la atenuación por impurezas reduce potencia, no confina la luz; d) la dispersión cromática ensancha el pulso porque sus componentes espectrales tienen distintos tiempos de propagación, no guía la señal; e) no aplica.

**Evidencia:** [hoja 2, pregunta 8](../../segundo_parcial/2.jpeg); [U7, comunicaciones ópticas](../teoria/07-medios-comunicaciones/apuntes-comunicacion-de-datos-u7.md#optica); [Medios de Comunicaciones Ópticas, pp. 3–4 y 12](../../material/teoria/U7/UT%207%20Medios%20de%20Comunicaciones%20opticas.pdf#page=4).

</details>

<a id="q09"></a>
## Q09 — Longitud de una antena de cuarto de onda

### Enunciado original

> Para una antena de ¼ de onda, si la frecuencia de operación (f) es 150 MHz, ¿cuál sería su longitud en metros?
>
> a) 0.25 m
>
> b) 0.5 m
>
> c) 1 m
>
> d) 2 m
>
> e) Ninguna de las opciones.

**Datos y condiciones:** frecuencia de operación $f=150$ MHz y antena de ¼ de onda. Se busca la longitud en metros; no se especifica un ajuste constructivo.

<details>
<summary>Mostrar resolución razonada</summary>

1. La longitud de onda es lo que avanza la onda en un período. Primero calculá esa distancia para la frecuencia dada; recién después tomá la cuarta parte. Usamos propagación en aire aproximada por la velocidad en vacío, como en el modelo de cátedra, sin correcciones de construcción.

| Símbolo | Significado | Unidad |
|---|---|---|
| $f$ | Frecuencia de operación | Hz al sustituir |
| $c$ | Velocidad aproximada de propagación en aire | m/s |
| $\lambda$ | Longitud de onda completa | m |
| $L$ | Longitud ideal de la antena | m |

2. Convertí $150$ MHz a $150\times10^6$ Hz, con 1 Hz equivalente a 1 ciclo/s. Entonces:

$$
\lambda=\frac{c}{f}\approx\frac{3\times10^8\ \text{m/s}}{150\times10^6\ \text{Hz}}=2\ \text{m},
\qquad L=\frac{\lambda}{4}=\frac{2\ \text{m}}{4}=0{,}5\ \text{m}.
$$

3. **Respuesta: b) 0.5 m.**
4. **Distractores:** a) 0,25 m es un octavo de esta onda, no un cuarto; «¼» es una fracción de la longitud de onda, no una longitud fija de 0,25 m. c) es media onda; d) es la onda completa; e) no aplica.

**Evidencia:** [hoja 2, pregunta 9](../../segundo_parcial/2.jpeg); [U7, radio y antenas](../teoria/07-medios-comunicaciones/apuntes-comunicacion-de-datos-u7.md#radio); [Medios de Comunicaciones, p. 24](../../material/teoria/U7/U7%20Medios%20de%20Comunicaciones.pdf#page=24), tabla de longitudes; [TP7, E5](../practica/tp-07-medios-comunicaciones.md#ejercicio-05) aplica el método inverso para una antena de cuarto de onda.

</details>

<a id="q10"></a>
## Q10 — Funciones principales de un módem

### Enunciado original

> Una de las funciones principales de un Módem es:
>
> a) Almacenamiento y procesamiento de la información
>
> b) Ecualización del canal
>
> c) Multiplexado de canales
>
> d) Codificación
>
> e) Ninguna de las opciones.

**Datos y condiciones:** no se indica un modelo de módem. Se pide reconocer **una** función principal según la clasificación de U8.

<details>
<summary>Mostrar resolución razonada</summary>

1. Para transmitir, el módem tiene que representar los datos de una forma que pueda enviarse por el medio y recuperarse del otro lado. La filmina separa dos funciones principales: **modulación**, que adapta la señal al medio, y **codificación**, que organiza la representación de los datos. No hace falta que ambas figuren entre las opciones.
2. **Respuesta: d) Codificación.** Que la modulación/demodulación dé nombre al módem no excluye que la cátedra clasifique también la codificación como principal.
3. **Distractores:** a) almacenamiento y procesamiento y c) multiplexado se clasifican como **especiales**; b) la ecualización compensa distorsiones del canal, pero en la tabla es **complementaria**; e) no aplica porque d) sí es principal.

**Evidencia:** [hoja 2, pregunta 10](../../segundo_parcial/2.jpeg); [U8, funciones e inteligencia del módem](../teoria/08-hardware-comunicaciones/APUNTE.md#funciones); [Hardware de comunicaciones, p. 20](../../material/teoria/U8/U8%20Hardware%20de%20comunicaciones.pdf#page=20), clasificación de cátedra.

</details>
