---
unidades: [1, 2, 3, 4]
tipo: cuestionario
estado: completo
fuentes:
  - primer_parcial/1.jpeg
  - primer_parcial/2.jpeg
actualizado: 2026-11-15
---

# Primer parcial — Primera instancia, Tema J (U1–U4)

**Alcance:** las diez preguntas de opción múltiple que figuran en las dos fotos del Tema J. La instancia abarca U1–U4; las consignas fotografiadas se concentran en U2–U4. Esto no cubre el programa entero de la instancia ni reproduce una clave oficial.

**Fuente del enunciado:** [foto 1 (Q01–Q06)](../../primer_parcial/1.jpeg) y [foto 2 (Q07–Q10)](../../primer_parcial/2.jpeg). Se transcribe el texto impreso de las preguntas y opciones, no las marcas manuscritas; las opciones se resuelven independientemente de esas marcas.

<details>
<summary>Mostrar clave rápida</summary>

**1d · 2a · 3e · 4e · 5c · 6e · 7b · 8d · 9c · 10e.** Q04 se responde según la clasificación de cátedra; abajo se aclaran las dos acepciones de PAM.

</details>

<a id="q01"></a>
## Q01 — Técnicas y jerarquías de multiplexación

### Enunciado original

Qué asociación de palabras es correcta:

a. FDM – digital – ancho de banda

b. STDM – time slots – ineficiencia

c. SDH – plesiócrono – STM

d. WDM – longitud de onda – fibra óptica

e. TDM – norma USA – OC

f. Ninguna

**Datos y condiciones:** no hay datos numéricos. Se pide elegir la asociación completa correcta, no sólo identificar un término que coincida.

<details>
<summary>Mostrar resolución razonada</summary>

1. En una misma fibra pueden viajar varios canales ópticos al mismo tiempo. El multiplexor los combina usando una longitud de onda distinta por canal; el demultiplexor los vuelve a separar.
2. **Respuesta: d) WDM – longitud de onda – fibra óptica.**
3. **Distractores:** a) FDM sí reparte ancho de banda, pero no se define como digital: en el esquema del TP suma subbandas y produce un agregado analógico incluso si transporta datos digitales. b) STDM usa ranuras por demanda justamente para evitar las reservas vacías del TDM fijo; puede agregar control y colas, pero «ineficiencia» no lo identifica. c) STM corresponde a SDH, que es **síncrona**; la jerarquía plesiócrona es PDH. e) TDM es una técnica, no una norma estadounidense; OC designa niveles ópticos de SONET. f) se descarta porque d) sí es correcta.

**Evidencia:** [U4, WDM](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#wdm-cdm), [STDM](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#stdm), [PDH/SDH/SONET](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#pdh-sdh); [TP4 E9–E10](../practica/tp-04-modulacion-multiplexacion.md#e9); [Multiplexación, filminas pp. 5, 23–24 y 28–29](../../material/teoria/U4/U4%20MULTIPLEXACION.pdf#page=5).

</details>

<a id="q02"></a>
## Q02 — Cuándo coinciden baudios y bit/s

### Enunciado original

Cuándo resulta igual la velocidad de modulación y la binaria?

a. Cuando el número de estados es igual a dos

b. Cuando la transmisión es serie

c. Cuando la transmisión es simplex

d. Cuando es inferior a 120 bps

e. Ninguna

**Datos y condiciones:** no se da una velocidad concreta; «120 bps» figura sólo como opción. Se pregunta cuándo coinciden numéricamente ambas tasas.

<details>
<summary>Mostrar resolución razonada</summary>

1. El receptor observa **símbolos**; cada uno puede representar uno o varios **bits**. Para el mapeo fijo de símbolos del TP, con $n$ estados y $n$ potencia de dos, $V_t=V_m\log_2 n$.

| Símbolo | Significado | Unidad |
|---|---|---|
| $V_m$ | Tasa de símbolos | baudios (símbolo/s) |
| $V_t$ | Tasa binaria transmitida | bit/s |
| $n$ | Cantidad de estados; $\log_2 n$ cuenta bits por símbolo | estados; bit/símbolo, respectivamente |

2. Con dos estados, cada símbolo representa un bit: por ejemplo, 1200 símbolos/s × 1 bit/símbolo = 1200 bit/s. Coinciden los **valores numéricos**, no las unidades.
3. **Respuesta: a) Cuando el número de estados es igual a dos.**
4. **Distractores:** b) serie dice cómo se envían los datos, no cuántos bits representa cada símbolo; c) simplex indica un solo sentido; d) estar por debajo de cierta tasa no fija los bits por símbolo; e) se descarta por a).

**Evidencia:** [U3, velocidades y señalización multinivel](../teoria/03-redes-telecomunicaciones/APUNTE.md#velocidades); [TP3 E2 resuelto](../practica/tp-03-redes.md#e02) y [enunciado de cátedra, p. 2](../../material/practica/U%203/TP%20%20%203%20%20%202026.pdf#page=2); [UT3, Medida de velocidad, pp. 3–5](../../material/practica/U%203/UT%203%20MEDIDA%20VELOCIDAD.pdf#page=3).

</details>

<a id="q03"></a>
## Q03 — Respuesta en frecuencia de un canal telefónico

### Enunciado original

Cuál de los siguientes filtros es el que mejor se adapta a la respuesta en frecuencia de un canal telefónico?

a. Pasa bajos

b. Pasa altos

c. Rechazo de banda

d. Analógico

e. Ninguno

**Datos y condiciones:** el enunciado dice canal telefónico, sin frecuencias de corte. Se pide clasificar su respuesta en frecuencia.

<details>
<summary>Mostrar resolución razonada</summary>

1. Para el canal telefónico vocal del ejemplo de cátedra, la banda útil va aproximadamente de **300 a 3400 Hz**. Se conservan frecuencias intermedias y se atenúan las de ambos extremos: 1 kHz está dentro; 100 Hz y 5 kHz, afuera.
2. El modelo es **pasa banda**, que no figura entre las opciones. **Respuesta: e) Ninguno.**
3. **Distractores:** a) un pasa bajos no introduce el corte inferior de la banda vocal; b) un pasa altos no introduce el superior; c) rechazo de banda hace lo contrario de un pasa banda en el intervalo seleccionado; d) «analógico» no especifica qué frecuencias deja pasar.

**Evidencia:** [U2, filtros](../teoria/02-senales-telecomunicaciones/APUNTE.md#filtros), [filmina original, p. 48](../../material/teoria/U2/U%202%20Caracter%C3%ADsticas%20de%20las%20se%C3%B1ales%20de%20telecom.pdf#page=48), [repaso U2, S07](u02-senales.md) y [canal vocal en la filmina de hardware, p. 21](../../material/teoria/U8/U8%20Hardware%20de%20comunicaciones.pdf#page=21), esta última sólo como referencia cruzada para los dos cortes.

</details>

<a id="q04"></a>
## Q04 — Señal moduladora y señal modulada

### Enunciado original

La señal modulada es digital en el método de modulación:

a. PSK

b. PAM

c. QAM

d. FM

e. Ninguno.

**Datos y condiciones:** no hay datos numéricos. La consigna pregunta por la señal **modulada** (salida), no por la **moduladora** (entrada).

<details>
<summary>Mostrar resolución razonada</summary>

1. Leé la columna **«Modulada»** de la tabla de cátedra. PSK (a) y QAM (c) **sí son métodos de modulación digital** porque llevan símbolos digitales sobre una portadora sinusoidal, pero en esa tabla la señal resultante se clasifica como analógica. En FM (d), la señal resultante es también analógica.
2. En el esquema de **PAM analógica** (b), los pulsos aparecen en instantes discretos, pero su altura sigue pudiendo tomar cualquier amplitud de la entrada muestreada. Tener pulsos no equivale a cuantificar. PCM sí produce una secuencia digital con cuantificación y codificación; no figura en las opciones.
3. **Respuesta según la clasificación de cátedra: e) Ninguno.** El enunciado aislado es ambiguo: PAM también nombra **M-PAM digital**, con un alfabeto finito de amplitudes. Si la opción b) dijera «M-PAM con niveles discretos», no correspondería descartarla con el argumento usado para PAM analógica.

**Evidencia:** [U4, clasificación](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#modulacion), [pulsos analógicos](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#pulsos), [TP4 E4 (PSK)](../practica/tp-04-modulacion-multiplexacion.md#e4) y [TP4 E7 (clasificación)](../practica/tp-04-modulacion-multiplexacion.md#e7); [Modulación 1, tabla p. 5](../../material/teoria/U4/U4%20MODULACION%201.pdf#page=5) y [Modulación 2, pp. 3–4](../../material/teoria/U4/U4%20MODULACION%202.pdf#page=3). Para la otra acepción: [Gallager (MIT), §6.2](https://ocw.mit.edu/courses/6-450-principles-of-digital-communications-i-fall-2006/1e8d60eb6c0a68cc48e81af039fd4af6_book_6.pdf).

</details>

<a id="q05"></a>
## Q05 — Bits por símbolo en 64-PSK

### Enunciado original

En la modulación 64-PSK la velocidad de transmisión es:

a. 2 veces la de modulación

b. 4 veces la de modulación

c. 6 veces la de modulación

d. 8 veces la de modulación

e. Ninguno,

**Datos y condiciones:** 64-PSK, con 64 estados de fase. No se da una tasa de símbolos; sólo se pide la relación entre tasas.

<details>
<summary>Mostrar resolución razonada</summary>

1. Cada símbolo elige una fase entre 64. Un grupo de seis bits permite 64 combinaciones, porque $2^6=64$.
2. Con el mapeo de [Q02](#q02), resultan **6 bit/símbolo**. Por ejemplo, a 1000 baudios serían 6000 bit/s transmitidos (tasa bruta, no flujo útil luego de descontar control o redundancia).
3. **Respuesta: c) 6 veces la de modulación.** a), b) y d) implicarían respectivamente 4, 16 y 256 estados con ese mapeo. e) no corresponde porque c) coincide.

**Evidencia:** [U4, PSK y QAM](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#psk-qam); [TP4 E3 resuelto](../practica/tp-04-modulacion-multiplexacion.md#e3) y [enunciado, p. 2](../../material/practica/U%204/TP%204%20%202026.pdf#page=2), donde se hace el mismo razonamiento para 16-PSK.

</details>

<a id="q06"></a>
## Q06 — Longitud de onda y banda radioeléctrica

### Enunciado original

Se dispone de un equipo radioeléctrico que opera en 4 metros de longitud de onda. A qué frecuencia y banda del espectro radioeléctrico corresponde?

a. 150 MHz / UHF

b. 20 MHz / VHF

c. 150 MHz / VHF

d. 20 MHz / HF

e. Ninguno

**Datos y condiciones:** longitud de onda de 4 m. Se pide el par frecuencia/banda. El medio no se indica; se adopta propagación de radio en aire.

<details>
<summary>Mostrar resolución razonada</summary>

1. Una longitud de onda es la distancia que recorre la perturbación durante un período. En aire tomamos la velocidad de propagación aproximadamente igual a la de la luz en vacío.

| Símbolo | Significado | Unidad |
|---|---|---|
| $c$ | Velocidad de propagación aproximada en aire | m/s |
| $\lambda$ | Longitud de onda | m |
| $f$ | Frecuencia | Hz |

2. $f=c/\lambda=(3\times10^8\ \mathrm{m/s})/(4\ \mathrm m)=75\times10^6\ \mathrm{Hz}=75\ \mathrm{MHz}$. Está en **VHF (30–300 MHz)**.
3. **Respuesta: e) Ninguno**, porque no aparece **75 MHz / VHF**. c) y d) son pares coherentes para otras frecuencias, no para 4 m; a) y b) además asignan a 150 MHz y 20 MHz, respectivamente, una banda que no les corresponde.

**Evidencia:** [U2, OEM y espectro](../teoria/02-senales-telecomunicaciones/APUNTE.md#oem), [tabla de bandas de la práctica 2](../../capturas/practica/image-14.png) y [TP2 E5 resuelto](../practica/tp-02-senales.md#e5--longitud-de-onda-de-fm-88108-mhz) ([enunciado, p. 2](../../material/practica/U%202/TP%20%202%20%202026.pdf#page=2)), que aplica la misma relación en sentido inverso.

</details>

<a id="q07"></a>
## Q07 — Potencia de salida en dBm

### Enunciado original

Si la potencia de salida de un amplificador es de 100 mW, a qué equivale?

a. 1 dB

b. 20 dBm

c. 30 dB

d. 4 dBm

e. Ninguno

**Datos y condiciones:** potencia de salida de 100 mW. No se da la potencia de entrada. Se pide un nivel equivalente, no la ganancia del amplificador.

<details>
<summary>Mostrar resolución razonada</summary>

1. Para expresar una potencia positiva como nivel en dBm, comparala con la referencia fija de 1 mW. Como es una relación de **potencias**, usamos $10\log_{10}$, no $20\log_{10}$.

| Símbolo | Significado | Unidad |
|---|---|---|
| $P_{\mathrm{sal}}$ | Potencia de salida | mW |
| $P_{\mathrm{ref}}$ | Potencia fija de referencia (1 mW) | mW |
| $L_{\mathrm{sal}}$ | Nivel de potencia de salida | dBm |

2. $L_{\mathrm{sal}}=10\log_{10}(P_{\mathrm{sal}}/P_{\mathrm{ref}})=10\log_{10}(100/1)=20\ \mathrm{dBm}$.
3. **Respuesta: b) 20 dBm.** a) y c) están en dB, no expresan el nivel pedido ni se puede inferir una ganancia sin potencia de entrada; d) tiene la unidad, pero no el valor; e) se descarta por b).

**Evidencia:** [U2, unidades logarítmicas](../teoria/02-senales-telecomunicaciones/APUNTE.md#db-contexto), [filmina original, p. 5](../../material/teoria/U2/U%202%20Caracter%C3%ADsticas%20de%20las%20se%C3%B1ales%20de%20telecom.pdf#page=5), [TP3 E13 resuelto](../practica/tp-03-redes.md#e13) y [práctica 5, Q3](u06-canales.md#q-p5-3) como referencia cruzada.

</details>

<a id="q08"></a>
## Q08 — Probabilidad de error: 16-QAM frente a 16-PSK

### Enunciado original

La modulación 16-QAM respecto de la 16-PSK tiene:

a. Más cambios de fase

b. Mayor velocidad de transmisión

c. Más bits para representar los estados que adopta

d. Menor probabilidad de error

e. Ninguno

**Datos y condiciones:** ambas modulaciones tienen 16 estados. No se informa el canal ni el ruido. Para comparar errores se adopta el caso usual de 16-QAM cuadrada y 16-PSK con detección coherente, ruido blanco gaussiano aditivo e igual relación de energía por bit a densidad espectral de ruido ($E_b/N_0$).

<details>
<summary>Mostrar resolución razonada</summary>

1. En 16-PSK los 16 puntos están sobre un círculo; en 16-QAM cuadrada se reparten en una grilla variando amplitud y fase. A igual energía media de símbolo para estas dos constelaciones, los vecinos más próximos quedan más separados en 16-QAM: una perturbación tiene que desplazar más el punto para confundirlo con un vecino.
2. En la curva de cátedra, la 16-QAM da menos errores para un mismo $E_b/N_0$ en el rango de comparación. **Respuesta: d) Menor probabilidad de error.** No es una afirmación universal para cualquier canal, receptor o constelación.
3. **Distractores:** a) variar amplitud además de fase no implica más fases (16-PSK ya usa 16 fases distintas); b) a iguales baudios la tasa bruta coincide; c) ambas necesitan cuatro bits por estado, porque $2^4=16$; e) se descarta por d).

**Evidencia:** [U4, comparación PSK/QAM](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#psk-qam), [Modulación 1, curva p. 24](../../material/teoria/U4/U4%20MODULACION%201.pdf#page=24), [TP4 E2–E3](../practica/tp-04-modulacion-multiplexacion.md#e2) para la constelación PSK y los bits por estado, y [repaso U4, Q2](u04-modulacion-multiplexacion.md#q2) para la comparación directa.

</details>

<a id="q09"></a>
## Q09 — Tasa binaria de un canal PCM

### Enunciado original

La velocidad de transmisión de señales digitalizadas sobre un canal telefónico (4 KHz) codificando cada muestra con 7 bits es de:

a. 64 Kbps

b. 128 Kbps

c. 56 Kbps

d. 1024 bps

e. Ninguno

**Datos y condiciones:** 4 kHz según el enunciado, 7 bit/muestra. No se da explícitamente la frecuencia de muestreo; se interpreta como el caso del TP4: 4 kHz como tope nominal del modelo de digitalización y 8000 muestras/s. Se pide la tasa de salida PCM sin entramado ni control adicional, no la capacidad de un enlace analógico.

<details>
<summary>Mostrar resolución razonada</summary>

1. Primero se cuentan **muestras por segundo**. En este ejercicio se usa la tasa nominal telefónica de 8000 muestras/s, el doble del tope idealizado de 4 kHz (una muestra cada 125 μs, como en TP4 E1). El cálculo al doble es el modelo del ejercicio, no una garantía de reconstrucción para cualquier señal con energía justo en el borde.

| Símbolo | Significado | Unidad |
|---|---|---|
| $f_s$ | Tasa de muestreo | muestra/s |
| $b$ | Bits por muestra | bit/muestra |
| $V_t$ | Tasa binaria de salida PCM | bit/s |

2. Cada muestra aporta siete bits: $V_t=f_sb=8000\ \mathrm{muestras/s}\times7\ \mathrm{bit/muestra}=56\,000\ \mathrm{bit/s}=56\ \mathrm{kbit/s}$.
3. **Respuesta: c) 56 Kbps.** A esa tasa de muestreo, a) sale con 8 bit/muestra, b) con 16 bit/muestra y d) no corresponde al producto; e) se descarta por c). Los 4 kHz nominales de este modelo no son los dos cortes del canal vocal de [Q03](#q03).

**Evidencia:** [U4, PCM](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#pcm); [Modulación 2, p. 3](../../material/teoria/U4/U4%20MODULACION%202.pdf#page=3); [TP4 E1 resuelto](../practica/tp-04-modulacion-multiplexacion.md#e1) ([enunciado, p. 2](../../material/practica/U%204/TP%204%20%202026.pdf#page=2)), que calcula exactamente los casos de 7 y 8 bit/muestra.

</details>

<a id="q10"></a>
## Q10 — Trama PCM24: canales y tasa de línea

### Enunciado original

La modulación PCM 24 tiene las siguientes características:

a. Norma T1, 30 canales telefónicos, velocidad 1,544 Mbps

b. Norma T1, 24 canales telefónicos, velocidad 2,048 Mbps

c. Norma E1, 32 canales telefónicos, velocidad 2,048 Mbps

d. Norma E1, 30 canales telefónicos, velocidad 2,048 Mbps

e. Ninguno de estas opciones es elegible

**Datos y condiciones:** se pide identificar la combinación de jerarquía, cantidad de canales telefónicos y tasa de línea para PCM24. Los valores de las opciones no son premisas.

<details>
<summary>Mostrar resolución razonada</summary>

1. PCM24 corresponde a **T1**: toma un octeto de cada uno de los 24 canales por trama y añade un bit de entramado. Eso da 193 bit/trama ($24\times8+1$), con una trama cada 125 μs, es decir, 8000 tramas/s.

| Símbolo | Significado | Unidad |
|---|---|---|
| $N_b$ | Bits por trama, incluido el de entramado | bit/trama |
| $f_{\mathrm{trama}}$ | Frecuencia de trama | trama/s |
| $V_{\mathrm{línea}}$ | Tasa bruta de línea | bit/s |

2. $V_{\mathrm{línea}}=N_b f_{\mathrm{trama}}=193\ \mathrm{bit/trama}\times8000\ \mathrm{tramas/s}=1\,544\,000\ \mathrm{bit/s}=1{,}544\ \mathrm{Mbit/s}$.
3. **Respuesta: e) Ninguno de estas opciones es elegible.** La combinación **T1, 24 canales, 1,544 Mbit/s** no aparece: a) cambia la cantidad de canales; b) cambia la tasa. c) confunde las 32 ranuras de E1 con canales telefónicos, y d) sí describe E1/PCM30 en el esquema de cátedra (30 canales de voz, una ranura de alineación/control y una de señalización), no PCM24.

**Evidencia:** [U4, TDM, E1 y T1](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#tdm), [Multiplexación, pp. 16–18](../../material/teoria/U4/U4%20MULTIPLEXACION.pdf#page=16) y [UIT-T G.733, equipo PCM primario de 1544 kbit/s](https://www.itu.int/rec/T-REC-G.733/en).

</details>

## Registro de verificación — 2026-11-15

- **Estructura:** 10 consignas y todas sus opciones cotejadas con las dos fotos; enlaces y anclas locales comprobados. Se conservan las unidades, signos y redacción impresos en los enunciados; las salvedades quedan en las resoluciones. Los hashes SHA-256 de las cuatro fotos registradas en el flujo no cambiaron.
- **Recálculo:** se comprobaron bits por símbolo, conversión de 4 m a 75 MHz, 100 mW a 20 dBm, tasa PCM de 56 kbit/s y tasa T1 de 1,544 Mbit/s.
- **Contraste técnico:** se revisaron las páginas pertinentes de los originales, en particular la tabla de filtros, la clasificación de modulación, la curva de error y la trama PCM24. Q04 queda explícitamente condicionada al vocabulario de cátedra. No se dispone de una clave oficial del Tema J.
