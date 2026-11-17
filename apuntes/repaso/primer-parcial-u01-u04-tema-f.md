---
unidades: [1, 2, 3, 4]
tipo: cuestionario
estado: completo
fuentes:
  - primer_parcial/tema-f/hoja-1-vista-general.png
  - primer_parcial/tema-f/hoja-1-detalle-superior.png
  - primer_parcial/tema-f/hoja-1-detalle-inferior.png
actualizado: 2026-11-17
---

# Primer parcial — Tema F (U1–U4)

**Alcance:** cinco consignas de una hoja. El encabezado identifica el Tema F, pero no la fecha ni si corresponde a la primera instancia o a un recuperatorio. Las tres fotos muestran la misma hoja: [vista general](../../primer_parcial/tema-f/hoja-1-vista-general.png), [detalle superior](../../primer_parcial/tema-f/hoja-1-detalle-superior.png) y [detalle inferior](../../primer_parcial/tema-f/hoja-1-detalle-inferior.png). Las marcas manuscritas no se usan como clave.

<a id="q01"></a>
## Q01 — Código de línea polar NRZ

### Enunciado original

Dado el siguiente gráfico de este código de línea contestar:

[Gráfico y consigna en la foto original](../../primer_parcial/tema-f/hoja-1-detalle-superior.png)

a. ¿Qué tipo de código se trata? (unipolar, polar, bipolar, RZ, NRZ, Manchester)

b. Es autosincronizante?

c. Indique dos códigos que ocupen más ancho de banda que éste.

d. ¿La componente continua es nula?

**Datos y condiciones:** se leen 11 celdas, con la secuencia `11011000100`. Hay dos niveles de signos opuestos. La línea de 0 es una referencia del gráfico, no un tercer nivel usado para representar bits. No se dan valores de tensión ni duración.

<details>
<summary>Mostrar resolución razonada</summary>

1. **a) Polar NRZ.** Primero mirá el eje vertical: el 1 usa una tensión positiva y el 0 una negativa; eso da **polar**. Después mirá el interior de una celda: el nivel se sostiene hasta el borde del bit; eso da **NRZ**. No es unipolar porque usa ambos signos, ni AMI/bipolar porque los unos no alternan signo.
2. **b) No.** En la racha `000`, la señal permanece negativa durante tres intervalos. Sin reloj ni otras referencias, en ese tramo no hay flancos que le indiquen al receptor dónde termina un cero y empieza el siguiente.
3. **c) Polar RZ y Manchester.** A igual tasa de bits, en el modelo rectangular del curso, polar RZ vuelve a cero dentro del bit y Manchester cambia de signo en su mitad. Ambos introducen rasgos de duración de medio bit que el canal debe reproducir. Con el criterio de comparación espectral de la cátedra ocupan más banda que polar NRZ; no se afirma una relación universal independiente del pulso y del criterio.
4. **d) La media de este tramo no es nula.** Con celdas de igual duración y niveles simétricos de magnitud $A$ [V], hay 5 celdas en $+A$ y 6 en $-A$. El promedio es $(5A-6A)/11=-A/11$ [V]. Si el patrón se repite, ésa es su componente continua; si es sólo un recorte, es su media, no la media de toda la transmisión. El cuadro de cátedra dice «No posee» para polar NRZ: se cumple como media estadística si unos y ceros son equiprobables, no para cualquier patrón.

**Evidencia:** [U2, reglas de códigos y media](../teoria/02-senales-telecomunicaciones/APUNTE.md#codigos); [cuadro de códigos, pp. 1–2](../../material/practica/U%202/UT%202%20C%C3%B3digos%20de%20l%C3%ADnea%20cuadro%20comparativo.pdf).

</details>

<a id="q02"></a>
## Q02 — Potencia de salida y pérdida del splitter

### Enunciado original

Una señal de CATV se distribuye utilizando un cable coaxil. Al llegar a una comunidad de vecinos la señal se separa en varios coaxiles mediante un splitter HOLLAND como el de la figura. Si la señal de entrada es de 1 watt:

a. ¿Cuál es la potencia de salida en Watts en la boca de menor atenuación del HOLLAND?

b. ¿Cuál es el valor de pérdida que tiene el splitter HOLLAND en dB?

[Figura del splitter en la foto original](../../primer_parcial/tema-f/hoja-1-vista-general.png)

**Datos y condiciones:** entrada de 1 W. La figura marca −3.5 dB en una salida y −7 dB en cada una de las otras dos. Para las cuentas se usan esos valores nominales, referidos a la misma entrada; no se dan mediciones reales ni pérdidas adicionales de los cables.

<details>
<summary>Mostrar resolución razonada</summary>

1. **Primero elegí la boca:** −3,5 dB es la transferencia menos negativa, por lo tanto es la de menor atenuación. Si $G$ es la ganancia con signo de una boca [dB], $P_{sal}=P_{ent}10^{G/10}$, con las dos potencias en W. Se usa **10**, porque el cociente es de potencias.
2. **a) Boca de −3,5 dB:** $1\,\mathrm W\times10^{-3{,}5/10}=0{,}446684\,\mathrm W$, aproximadamente **0,447 W**. El signo menos debe producir menos de 1 W; si te da más, invertiste el sentido de la relación.
3. **b) Si se pregunta por la misma boca**, su pérdida de inserción es **3,5 dB** (ganancia −3,5 dB). En cada otra boca es **7 dB**. No hay un único valor de pérdida por boca y no se suman 3,5 + 7 + 7: las salidas no están en cascada.
4. **Si se pide la pérdida global del dispositivo**, sumá primero las potencias de las tres salidas, no sus decibeles. Cada boca de −7 dB entrega $1\,\mathrm W\times10^{-7/10}\approx0{,}199526\,\mathrm W$. La suma es $P_{tot}\approx0{,}845736\,\mathrm W$; la diferencia con la entrada es aproximadamente 0,154264 W. La pérdida global inferida es $10\log_{10}(P_{ent}/P_{tot})\approx\mathbf{0{,}728\,\mathrm{dB}}$, suponiendo las tres salidas operando con los valores nominales indicados. Es distinta de la pérdida desde la entrada hasta una boca.

**Evidencia:** [U2, unidades de transmisión](../teoria/02-senales-telecomunicaciones/APUNTE.md#db-contexto) y [U6, decibeles](../teoria/06-canales-comunicaciones/APUNTE.md#decibeles), como referencia cruzada del método; los valores de las bocas provienen de la foto.

</details>

<a id="q03"></a>
## Q03 — Constelación de 16 estados

### Enunciado original

El diagrama de estados representa la modulación con la relación de velocidades siguiente:

[Diagrama completo en la foto original](../../primer_parcial/tema-f/hoja-1-vista-general.png)

1. 32 PSK Vtx = 5 Vmod
2. 16 QAM Vtx = 4 Vmod
3. 64 QAM Vtx = 5 Vmod
4. 128 PSK Vtx = 6 Vmod
5. Ninguna es elegible

**Datos y condiciones:** se observan 8 puntos en la circunferencia exterior y 8 en la interior. El diagrama no da una tasa concreta. Se usa mapeo binario fijo sin redundancia; se compara tasa bruta con velocidad de modulación.

<details>
<summary>Mostrar resolución razonada</summary>

1. Contá **puntos**, no radios por ángulos. Hay dos radios (dos amplitudes) y los puntos también cambian de ángulo (fase). No es PSK pura: allí los estados tienen el mismo radio. La geometría circular de esta **16-QAM** no obliga a que sea una grilla rectangular.
2. Con $M$ estados y $b$ bits por símbolo, $M=2^b$. Como $16=2^4$, cada símbolo puede representar **4 bits**. $V_{tx}=V_{mod}\,b$; $V_{mod}$ se mide en símbolos/s (baudios), $b$ en bit/símbolo y $V_{tx}$ en bit/s. Por ejemplo, 1000 baudios darían 4000 bit/s en este mapeo.
3. **Respuesta: opción 2.** La 1 tiene un factor válido para 32 estados, pero no el orden ni la familia del dibujo. La 3 requeriría 64 puntos y 6 bits/símbolo. La 4 requeriría 128 puntos y 7 bits/símbolo, no 6. La 5 se descarta porque la 2 coincide.

**Evidencia:** [U3, multinivel](../teoria/03-redes-telecomunicaciones/APUNTE.md#multinivel) y [U4, PSK y QAM](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#psk-qam).

</details>

<a id="q04"></a>
## Q04 — Interpretación de la figura de amplitud y tiempo

### Enunciado original

Seleccione la respuesta adecuada referida a este gráfico. Corresponde a:

[Gráfico y opciones en la foto original](../../primer_parcial/tema-f/hoja-1-detalle-inferior.png)

a. Una señal modulada en amplitud.

b. A la técnica TDM

c. A la metodología FDM

d. A la tecnología OFDM

e. Ninguna de las opciones

**Datos y condiciones:** el eje horizontal dice `Time` y el vertical `Amplitude`. Se ven muestras a distintos niveles y niveles rotulados con palabras de ocho bits, desde `00000000` hasta `11111111`. El gráfico no identifica canales ni muestra una trama o un espectro.

<details>
<summary>Mostrar resolución razonada</summary>

1. Leé los ejes antes de elegir. Las líneas verticales se leen como amplitudes en instantes de muestreo. Las etiquetas binarias identifican niveles discretos: la figura ilustra **muestras cuantificadas con niveles que se pueden codificar**, propias del proceso PCM. No dibuja la secuencia de pulsos binarios en la línea ni permite deducir un código de línea concreto.
2. **Respuesta mejor sustentada por la figura: e) Ninguna de las opciones**, porque PCM o cuantificación no están en la lista. La a) puede tentar porque cambian las alturas, pero en el sentido habitual de AM se esperaría una portadora cuya envolvente sigue el mensaje, no una tabla de niveles binarios. Si «modulada en amplitud» se interpretara en un sentido amplio que incluyera una representación pulsada por amplitud, la redacción sería ambigua; no alcanza para identificar AM convencional.
3. **Por qué no b), c) ni d):** que haya muestras sucesivas no demuestra **TDM**: faltan varias fuentes o ranuras identificables. FDM separaría canales por bandas; OFDM mostraría subportadoras ortogonales. El dibujo no muestra ninguna de esas asignaciones. Una señal PCM puede **alimentar** un TDM después, pero el gráfico no demuestra que eso ocurra.

**Evidencia:** [U4, PCM](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#pcm), [TDM](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#tdm) y [Modulación 2, pp. 3–4](../../material/teoria/U4/U4%20MODULACION%202.pdf#page=3), donde se distinguen muestreo, cuantificación y codificación.

</details>

<a id="q05"></a>
## Q05 — Enlace de 300 bps frente al transporte físico

### Enunciado original

Imagine que Ud. entrenó a su perro San Bernardo para llevar una caja con 4 diskettes en vez del barrilito de brandy. Cada diskette contiene 250000 Bytes. El perro viaja a 18 km/hora. ¿Para qué rango de distancias el perro tiene mayor velocidad de transferencia que un enlace de 300 bps?

[Vista general](../../primer_parcial/tema-f/hoja-1-vista-general.png) · [detalle inferior](../../primer_parcial/tema-f/hoja-1-detalle-inferior.png)

**Datos y condiciones:** 4 diskettes de 250000 bytes, 18 km/h y enlace de 300 bit/s. Se compara entregar el mismo lote completo, en un viaje de ida, suponiendo velocidad constante y sin tiempos de carga, lectura, protocolo ni propagación adicional.

<details>
<summary>Mostrar resolución razonada</summary>

1. **Primero poné los datos en la misma unidad.** La caja contiene $4\times250000=1000000$ bytes, es decir **8 000 000 bit**. No dividas bytes directamente por bit/s.
2. **Tiempo del enlace:** 8 000 000 bit ÷ 300 bit/s = 26 666,67 s, aproximadamente **7 h 24 min 27 s**. Ése es el tiempo que el perro tiene que mejorar. Llevar muchos bits juntos no altera su velocidad física; sí cambia la tasa media de entrega del lote.
3. **Distancia de empate:** convertí 18 km/h a **5 m/s**. En el tiempo del enlace, el perro recorre $5\,\mathrm{m/s}\times26666{,}67\,\mathrm s=133333{,}33\,\mathrm m$, aproximadamente **133,333 km**. Como el tiempo de viaje aumenta con la distancia, para cualquier distancia positiva por debajo del umbral llega antes que el enlace.
4. **Respuesta:** $0<d<133\tfrac13\,\mathrm{km}$, donde $d$ es la distancia de ida. A $133\tfrac13\,\mathrm{km}$ hay empate; por encima es más rápido el enlace. Control: a 90 km tarda 5 h y el lote llega a una media de unos 444 bit/s, mayor que 300 bit/s. Si el problema contara regreso o tiempos fijos, el umbral cambiaría.

**Evidencia:** [U3, velocidades y entrega útil](../teoria/03-redes-telecomunicaciones/APUNTE.md#velocidades); datos y criterio de comparación aplicados al enunciado fotografiado.

</details>
