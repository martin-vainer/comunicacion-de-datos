---
unidades: [1, 2, 3, 4]
tipo: cuestionario
estado: completo
fuentes:
  - primer_parcial/tema-no-visible/hoja-1.png
actualizado: 2026-11-17
---

# Primer parcial — Tema no visible en la foto (U1–U4)

**Alcance:** cinco consignas de la [hoja fotografiada](../../primer_parcial/tema-no-visible/hoja-1.png). La toma no permite identificar fecha, tema ni instancia; no se los deduce de las marcas. En el margen inferior izquierdo no se lee completa la numeración de las dos últimas consignas: Q04 y Q05 son rótulos editoriales por orden de aparición. La resolución es independiente de las anotaciones manuscritas.

<a id="q01"></a>
## Q01 — Código de línea bipolar NRZ (AMI)

### Enunciado original

Dado el siguiente gráfico de este código de línea contestar:

[Gráfico en la foto original](../../primer_parcial/tema-no-visible/hoja-1.png)

a. ¿Qué tipo de código se trata? (unipolar, polar, bipolar, RZ, NRZ, Manchester)

b. Es autosincronizante?

c. Indique dos códigos que ocupen más ancho de banda que éste.

d. ¿La componente continua es nula?

**Datos y condiciones:** la señal tiene tres alturas relativas: positiva, cero y negativa. El gráfico no calibra tensiones ni tiempos; para promediar el tramo se toman celdas iguales y marcas simétricas $\pm A$ [V].

<details>
<summary>Mostrar resolución razonada</summary>

1. **a) Bipolar NRZ, o AMI.** El 0 se representa en el nivel medio. Los 1 son marcas que alternan de signo: por ejemplo, las dos primeras marcas tienen polaridades opuestas. Como cada marca ocupa la celda completa sin volver a cero dentro de ella, es **NRZ**. No es polar NRZ: allí el 0 usaría una tensión de signo opuesto al 1, no el nivel cero.
2. **b) No garantiza autosincronismo.** Los unos generan marcas alternadas que ayudan a recuperar reloj, pero una racha arbitrariamente larga de ceros deja la señal plana en cero. En ese caso faltan transiciones para fijar los bordes de bit. Que este recorte tenga muchos flancos no garantiza que cualquier secuencia los tenga.
3. **c) Bipolar RZ y Manchester.** A igual tasa de bits, el bipolar RZ mantiene la alternancia de marcas pero acorta cada marca para retornar a cero dentro del bit. Manchester obliga a una transición central incluso con ceros consecutivos. Con los pulsos rectangulares y la comparación del curso, esas variaciones más rápidas requieren más banda que AMI NRZ. No se deduce un ancho exacto en Hz sin tasa y criterio de medición.
4. **d) El AMI ideal no acumula continua sostenida**, porque cada par de marcas sucesivas aporta la misma área con signo opuesto; los ceros no suman área. **Eso no obliga a que esta ventana tenga media cero:** al recorrer la grilla se leen los niveles `0 + − 0 + − + 0 − 0 + − + − 0 + 0 − 0 +`, es decir 7 marcas positivas, 6 negativas y 7 celdas en cero. Para este recorte, la media es $(7A-6A)/20=A/20$ [V]. Si se envían más bits en AMI, la alternancia continúa a través de los límites; reiniciar siempre con el mismo signo al repetir un bloque impar alteraría la regla.

**Evidencia:** [U2, códigos de línea y componente continua](../teoria/02-senales-telecomunicaciones/APUNTE.md#codigos); [cuadro comparativo de códigos, pp. 1–2](../../material/practica/U%202/UT%202%20C%C3%B3digos%20de%20l%C3%ADnea%20cuadro%20comparativo.pdf).

</details>

<a id="q02"></a>
## Q02 — Presupuesto de potencia de un enlace de fibra

### Enunciado original

Se requiere montar un enlace de fibra óptica uniendo dos equipos separados 30000 metros uno de otro. La potencia del transmisor es de 2 mW y la sensibilidad del receptor es de – 60 dBm.

a. Cuál será la especificación de atenuación máxima a requerir de la fibra que se debe emplear para no usar amplificador, expresada en dB/Km.

b. Si se emplea una fibra óptica de 5 dB/Km, se requiere amplificador para recibir la señal? Si así fuera, ¿de qué ganancia?

[Esquema Tx–Rx en la foto original](../../primer_parcial/tema-no-visible/hoja-1.png)

**Datos y condiciones:** distancia $d=30000$ m = 30 km; potencia de emisión 2 mW; sensibilidad $S_R=-60$ dBm; en b), atenuación específica de 5 dB/km. No se informan conectores, empalmes, márgenes ni otras pérdidas. Se busca llegar al menos al umbral nominal de potencia.

<details>
<summary>Mostrar resolución razonada</summary>

1. El receptor no compara «2 mW contra −60 dBm» directamente: ambas potencias deben estar en la misma escala. El nivel de salida $P_T$ [dBm] es $10\log_{10}(2\,\mathrm{mW}/1\,\mathrm{mW})=3{,}0103\,\mathrm{dBm}$. Que la sensibilidad sea negativa no significa potencia negativa: está por debajo de la referencia de 1 mW.
2. **a) Cuánta pérdida admite el enlace:** entre $3{,}0103$ dBm y $-60$ dBm hay **63,0103 dB** de presupuesto. Si la fibra pierde $\alpha$ [dB/km], la pérdida total en $d$ [km] es $\alpha d$ [dB]. Al repartir el presupuesto entre los 30 km, queda $63{,}0103\,\mathrm{dB}/30\,\mathrm{km}\approx\mathbf{2{,}10034\,\mathrm{dB/km}}$ como máximo. Es un caso límite, sin margen.
3. **b) Qué llega con la otra fibra:** 5 dB/km × 30 km = **150 dB** de pérdida. Sin amplificación llegan $3{,}0103-150=-146{,}9897$ dBm, por debajo de la sensibilidad. Por lo tanto, **sí requiere ganancia** en el modelo del ejercicio.
4. **Ganancia mínima:** no se compensan los 150 dB enteros; alcanza con cubrir la diferencia hasta el umbral: $-60-(-146{,}9897)=\mathbf{86{,}9897\,\mathrm{dB}}$, aproximadamente **87 dB**. Control: $3{,}0103+86{,}9897-150=-60$ dBm usando los valores redondeados. Es ganancia neta teórica de presupuesto, no una recomendación de usar un único amplificador real: faltan datos de ruido, potencia y margen.

**Evidencia:** [TP3 E17, mismo presupuesto inicial](../practica/tp-03-redes.md#e17), [TP3 E18, cálculo del déficit](../practica/tp-03-redes.md#e18) y [U6, balance de enlace](../teoria/06-canales-comunicaciones/APUNTE.md#balance-enlace) como referencia cruzada del método.

</details>

<a id="q03"></a>
## Q03 — Constelación de 32 estados sin opción correcta

### Enunciado original

El diagrama de estados representa la modulación con la relación de velocidades siguiente:

[Constelación y opciones en la foto original](../../primer_parcial/tema-no-visible/hoja-1.png)

1. 32 PSK Vtx = 5 Vmod
2. 128 QAM Vtx = 7 Vmod
3. 64 QAM Vtx = 5 Vmod
4. 128 PSK Vtx = 6 Vmod
5. Ninguna es elegible

**Datos y condiciones:** se cuentan los puntos dibujados, no los numeritos manuscritos. Hay 16 en el anillo exterior, 12 en el intermedio y 4 en el interior; no se da una velocidad nominal. Se usa un mapeo binario fijo sin redundancia.

<details>
<summary>Mostrar resolución razonada</summary>

1. **Tipo por geometría:** del centro a un punto leés amplitud; del eje de referencia al punto leés fase. Si fuera PSK pura, todos quedarían en un único radio. Acá hay tres radios y distintas fases, compatible con una **constelación QAM de 32 estados**. No hace falta que sea rectangular.
2. **Relación de velocidades:** $16+12+4=32$ es el total de estados efectivamente dibujados. Como $32=2^5$, hacen falta 5 bits para etiquetar cada símbolo: **$V_{tx}=5V_{mod}$**, donde $V_{mod}$ se mide en baudios y el factor representa 5 bit/símbolo. Por ejemplo, 1000 baudios representarían 5000 bit/s brutos. Tener tres radios no implica sólo tres estados, y no se multiplican los radios por todos los ángulos posibles.
3. **Respuesta: opción 5.** La 1 acierta el número de estados y el factor, pero falla la familia. La 2 es una relación válida para 128-QAM sin redundancia, que no es esta constelación. La 3 falla el orden y el factor: 64 estados dan 6 bits/símbolo. La 4 falla la familia, el número de estados y el factor: 128 estados dan 7 bits/símbolo.

**Evidencia:** [U3, relación multinivel](../teoria/03-redes-telecomunicaciones/APUNTE.md#multinivel) y [U4, constelaciones PSK/QAM](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#psk-qam).

</details>

<a id="q04"></a>
## Q04 — Reconocer OFDM en el espectro

### Enunciado original

Seleccione la respuesta adecuada referida a este gráfico. Corresponde a:

[Espectro y opciones en la foto original](../../primer_parcial/tema-no-visible/hoja-1.png)

a. Una señal modulada en amplitud.

b. La técnica TDM

c. La metodología FDM

d. La tecnología OFDM

e. Ninguna de las opciones

**Datos y condiciones:** el eje horizontal indica frecuencia; se ven cinco subportadoras con centros equiespaciados y lóbulos superpuestos. No hay escala numérica de ancho de banda en Hz.

<details>
<summary>Mostrar resolución razonada</summary>

1. La pista no es sólo que haya varios picos. Mirá uno de los centros: en el máximo de una subportadora, las curvas de las otras pasan por cero en el dibujo ideal. A pesar de que sus espectros ocupan porciones comunes, las subportadoras se pueden distinguir con la ventana de recepción adecuada.
2. **Respuesta: d) La tecnología OFDM.** En el modelo ideal de U4, la separación de centros $\Delta f$ [Hz] es $1/T_u$, donde $T_u$ [s] es la duración útil del símbolo. Por ejemplo, con $T_u=1$ ms se separan 1 kHz. La ortogonalidad depende de esa grilla y del sincronismo; no se deduce que cualquier superposición sea inocua.
3. **Distractores:** a) no es la figura típica de una portadora AM con sus bandas laterales; b) TDM distingue turnos en el tiempo y el dibujo está en frecuencia; c) OFDM es una forma de división por frecuencia, pero frente a FDM convencional la pista decisiva es la superposición **ortogonal**, no la separación en bandas con guardas entre canales; e) se descarta porque d) identifica el patrón específico.

**Evidencia:** [U4, FDM y OFDM](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md#fdm-ofdm) y [Multiplexación, p. 11](../../material/teoria/U4/U4%20MULTIPLEXACION.pdf#page=11), cuyo panel derecho coincide con el gráfico fotografiado.

</details>

<a id="q05"></a>
## Q05 — Rendimiento y sincronismo asincrónico

### Enunciado original

Para una transmisión asincrónica:

a. Calcular el rendimiento en % cuando el programa de comunicaciones que se emplea esta parametrizado con 7 bits de datos y 2 bits de parada.

b. Qué tipos de sincronismo hay en esta transmisión? Explicarlos brevemente.

[Consigna en la parte inferior de la foto original](../../primer_parcial/tema-no-visible/hoja-1.png)

**Datos y condiciones:** 7 bits de datos y 2 tiempos de bit de parada. El formato asincrónico del curso añade 1 bit de arranque por carácter. La consigna no dice si hay paridad ni cuánto silencio hay entre caracteres; se calcula la trama sin paridad como caso base y se explicita la variante.

<details>
<summary>Mostrar resolución razonada</summary>

1. **a) Separá información y control.** El arranque y la parada ocupan tiempo en la línea pero no son parte de los 7 bits de información. Sin paridad cada carácter consume $1+7+2=10$ tiempos de bit, de los cuales 7 son útiles. Rendimiento: $7/10\times100=\mathbf{70\,\%}$.
2. **Si hubiese paridad**, consumiría un tiempo adicional de bit: $7/11\times100\approx\mathbf{63{,}64\,\%}$. No se agrega por suposición al resultado base. Si hubiera pausas entre caracteres, disminuiría el rendimiento medido sobre todo el tiempo transcurrido; los valores anteriores son del formato del carácter.
3. **b) Sincronismo de carácter:** la transición de arranque tras el reposo marca dónde empieza el carácter. Como entre caracteres puede haber una pausa irregular, el receptor obtiene una nueva referencia en cada arranque. La parada deja el intervalo previsto antes de poder comenzar otro.
4. **Sincronismo de bit:** detectado el arranque, el receptor usa su reloj local a la tasa acordada para estimar el centro de cada intervalo y leer los siete bits en orden. Incluso si varios bits tienen el mismo nivel, los puede separar por el tiempo transcurrido. «Asincrónica» no significa «sin reloj». La consigna no establece una delimitación por bloques; eso sería otra estructura por encima del carácter.

**Evidencia:** [U3, sincronismo y rendimiento](../teoria/03-redes-telecomunicaciones/APUNTE.md#sincronismo), [formato asincrónico en U3, p. 10](../../material/teoria/U3/U3%20Redes%20de%20Telecomunicaciones.pdf#page=10) y [TP3, ejercicios de transmisión asincrónica](../practica/tp-03-redes.md#e06).

</details>
