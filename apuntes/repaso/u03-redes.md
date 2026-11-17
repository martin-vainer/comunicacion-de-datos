---
unidad: 3
estado: en-progreso
fuentes:
  - capturas/teoria/03-redes-telecomunicaciones/cuestionario_U3.md
  - capturas/practica/Clase 05.md
  - material/teoria/U3/U3 Redes de Telecomunicaciones.pdf
  - material/practica/U 3/UT 3 MEDIDA VELOCIDAD.pdf
actualizado: 2026-10-13
---

# Repaso U3 — Preguntas registradas

**Alcance parcial:** se reorganizan las cinco preguntas U3 existentes, no se crea simulacro ni preguntas nuevas. Incluye transferencia, baudios/bit/s, banda y sentidos. No evalúa RTPC/tráfico, RDSI, protocolos o topologías como si este cuestionario los cubriera. **Modalidad:** respondé una por vez antes de mirar soluciones; no tiempo/puntaje inventados.

## Trazabilidad por pregunta

| ID | Origen inmutable | Sección que respalda la corrección |
|---|---|---|
| U3-TQ1 | [Cuestionario U3](../../capturas/teoria/03-redes-telecomunicaciones/cuestionario_U3.md), Pregunta 1, perro/diskettes | [Transferencia](../teoria/03-redes-telecomunicaciones/APUNTE.md#velocidades); recálculo del enunciado |
| U3-TQ3 | Mismo archivo, Pregunta 3, radiodifusión | [Sentidos](../teoria/03-redes-telecomunicaciones/APUNTE.md#sentidos-modos); [F3](../../material/teoria/U3/U3%20Redes%20de%20Telecomunicaciones.pdf) p. 6 |
| U3-PQ1 | [Práctica 5](../../capturas/practica/Clase%2005.md), Pregunta 1, baudios/banda | [Multinivel y banda](../teoria/03-redes-telecomunicaciones/APUNTE.md#multinivel); F3 p. 2–4; [U6](../teoria/06-canales-comunicaciones/APUNTE.md) para ruido |
| U3-PQ2 | Mismo archivo, Pregunta 2, transferencia real | [Velocidades](../teoria/03-redes-telecomunicaciones/APUNTE.md#velocidades); F3 p. 3/FV p. 5 |
| U3-PQ4 | Mismo archivo, Pregunta 4, baudios/bps | [Multinivel](../teoria/03-redes-telecomunicaciones/APUNTE.md#multinivel); F3 p. 2/FV p. 5 |

**Reparto sin duplicación:** cuestionario_U3 **Q2**, tren de pulsos/Fourier, corresponde a [repaso U2](u02-fourier-y-ancho-de-banda.md). Práctica 5 **Q3**, «¿La unidad de medida dBm es para medir niveles de potencia?», corresponde a [repaso U6](u06-canales.md); aquí sólo se conserva procedencia y destino. No se responde ni se vuelve a formular como una pregunta U3.

## Preguntas y respuestas

### U3-TQ1 — Transferencia por un medio físico

> **Enunciado (transcripción literal — captura Cuestionario U3, Pregunta 1):** «Imagine que Ud. entrenó a su perro San Bernardo para llevar una caja con 4 diskettes en vez del barrilito de brandy. Cada diskette contiene 250000 Bytes. El perro viaja a 18 km/h. ¿Para qué rango de distancias el perro tiene mayor velocidad de transferencia que un enlace de 300 bps?»
>
> **Opciones originales:**
>
> a. Distancia menor que 133,33 km
>
> b. Distancia mayor que 133333 m
>
> c. Ninguna de las anteriores
>
> d. Distancia entre 140 y 233,33 km
>
> e. Distancia mayor de 233,33 km

**Datos:** 4 diskettes; 250000 Bytes por diskette; velocidad del perro de 18 km/h; enlace de comparación de 300 bps. Se pregunta por el rango de distancias.

#### U3-TQ1 — Respuesta a, con desigualdad estricta

**Resolución paso a paso.** No compares km/h directamente con bit/s: primero llevá la carga a bits y el desplazamiento a m/s.

**Paso 1 — carga total:**

$$
N=4\times250000\,byte\times8\,bit/byte=8000000\,bit.
$$

**Paso 2 — velocidad del perro:**

$$
v=18\,km/h=5\,m/s.
$$

**Paso 3 — tiempo y tasa media:**

$$
t=d/v,\qquad V=N/t=Nv/d.
$$

**Paso 4 — comparar con el enlace:**

$$
d<\frac{Nv}{300\,bit/s}=133333,3333\,m=133,3333333\,km.
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $N$ | Carga | bit |
| $v $ | Desplazamiento | m/s |
| $d $ | Distancia | m |
| $t $ | Viaje | s |
| $V$ | Transferencia media | bit/s |

**Supuestos:** viaje de ida a velocidad constante, entrega de toda la carga, sin tiempo de carga/lectura ni retorno; enlace 300 bit/s útiles sin overhead. 133,33 km es opción redondeada; en 133,333333 km exactos las tasas **empatan**, no supera. Cálculo de coherencia: 8000000/300=26666,6667 s; el perro recorre 133333,333 m en ese tiempo.

b/d/e proponen distancias donde el viaje tarda más y la tasa es menor. c no corresponde porque a expresa el rango correcto al redondeo. **Criterio de corrección:** carga×8, conversión de tiempo y sentido de desigualdad; confundir bytes/bits invalida el resultado. Buena tasa media no implica baja latencia de un bit individual.

### U3-TQ3 — Radiodifusión

> **Enunciado (transcripción literal — captura Cuestionario U3, Pregunta 3):** «¿Qué tipo de transmisión se utiliza en la radiodifusión comercial?»
>
> **Opciones originales:**
>
> a. Simplex
>
> b. Half duplex
>
> c. Semi duplex
>
> d. Full duplex
>
> e. Ninguno de los anteriores

**Condiciones/contexto:** pregunta conceptual sobre el servicio de radiodifusión comercial; no hay magnitudes numéricas. Se analiza la dirección del mismo canal de difusión.

#### U3-TQ3 — Respuesta a: simplex

**Resolución paso a paso.** **Paso 1:** identificar quién transmite y quién recibe en el servicio indicado: la emisora envía y los oyentes reciben. **Paso 2:** como no hay regreso por ese mismo servicio de radiodifusión, es simplex. Half/semi duplex requiere ambos sentidos alternados; full duplex, ambos simultáneos. Llamar a la emisora por otro servicio no transforma el canal de difusión. **Criterio:** explicar dirección, no sólo nombrar el ejemplo.

### U3-PQ1 — Límite de baudios

> **Enunciado (transcripción literal — captura Práctica 5, Pregunta 1):** «Indicar las causas por las cuales no se puede aumentar en determinados canales de comunicaciones la velocidad de modulación.»
>
> **Opciones originales:**
>
> a. Porque si aumento la velocidad de modulación, disminuye el ancho de banda, y por lo tanto también aumenta la potencia de ruido.
>
> b. Porque si aumento la velocidad de modulación, aumenta el ancho de banda, y por lo tanto también aumenta el ruido.
>
> c. Porque si aumento la velocidad de modulación, disminuye el ancho de banda, y por lo tanto no podemos aplicar transmisión multinivel.

**Condiciones/contexto:** pregunta conceptual, sin magnitudes numéricas. La afirmación de que al abrir más banda aumenta el ruido requiere que aumente la banda recibida y se mantenga fija la densidad espectral de ruido; la captura presenta esa relación sin explicitar el supuesto.

#### U3-PQ1 — b, pero con los supuestos explícitos

**Resolución paso a paso.** **Paso 1:** la opción b es la marcada por cátedra y la coherente con acortar pulsos manteniendo su forma: se requieren componentes de frecuencia más altas y más banda. Un canal fijo no puede reproducir indefinidamente esos cambios. **Paso 2:** si se amplía recepción a más banda **con densidad de ruido fija**, se integra más potencia de ruido.

No memorizar «más baudios siempre más ruido»: si no se cambia el filtro o cambia el espectro de ruido, esa frase requiere revisar condiciones. a/c invierten la relación temporal/espectral; multinivel no deja de existir por aumentar baudios. **Criterio:** señal más rápida→banda requerida; ruido condicionado a banda de recepción y su densidad. Fórmula de ruido y unidades se desarrollan en U6, no se duplica aquí.

### U3-PQ2 — Transferencia real

> **Enunciado (transcripción literal — captura Práctica 5, Pregunta 2):** «¿Cuál es la velocidad real de transferencia de datos y en qué se mide?»
>
> **Opciones originales:**
>
> a. Es la cantidad de bits transmitidos que contienen información con o sin errores en un tiempo determinado. Se mide en bps.
>
> b. Es la cantidad de bits transmitidos en un tiempo determinado. Se mide en baudios.
>
> c. Es la cantidad de bits transmitidos que contienen información sin errores en un tiempo determinado. Se mide en bps.

**Condiciones/contexto:** pregunta conceptual de definición; no se dan valores. La tasa real se refiere a información útil recibida correctamente por unidad de tiempo.

#### U3-PQ2 — c: información correcta por tiempo

**Resolución paso a paso.** **Paso 1:** identificar el numerador como información útil sin errores. **Paso 2:** dividir por tiempo y expresar la tasa en **bit/s**. Según definición de F3 p. 3/FV p. 5, a cuenta transferencia sin excluir errores; b mezcla cantidad de bits con unidad de símbolos. Puede expresarse en byte/s convirtiendo por 8, no llamando ambas unidades indistintamente bps. **Criterio:** numerador útil/correcto, denominador temporal y unidad correcta.

### U3-PQ4 — Baudios frente a bit/s

> **Enunciado (transcripción literal — captura Práctica 5, Pregunta 4):** «¿Cuál de las siguientes afirmaciones describe correctamente la relación entre baudios y bits por segundo (bps)?»
>
> **Opciones originales:**
>
> a. Siempre son iguales independientemente del sistema de modulación.
>
> b. Los bps pueden ser mayores que los baudios si cada símbolo representa más de un bit.
>
> c. Los baudios siempre son mayores que los bps.

**Condiciones/contexto:** pregunta conceptual; no hay magnitudes numéricas dadas. La relación supone un mapeo fijo de bits a símbolos.

#### U3-PQ4 — b: varios bits por símbolo

**Resolución paso a paso.** **Paso 1:** calcular cuántos bits representa cada símbolo a partir de la cantidad de estados. **Paso 2:** multiplicar esa relación por la velocidad de modulación.

$$
V_t=V_m\log_2n.
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $V_t $ | Tasa de bits bruta | bit/s |
| $V_m $ | Tasa de símbolos | baudios |
| $n $ | Estados disponibles | conteo |

**Supuesto:** mapeo fijo con $n $ potencia de 2, sin descontar redundancia/overhead. **Ejemplo registrado en la respuesta original:** 4 estados→2 bit/símbolo; 1000 baudios→2000 bit/s. a es falsa: no siempre un bit por símbolo; c es falsa por ese contraejemplo. «Mayor» compara cantidades numéricas bajo la conversión, no vuelve iguales las magnitudes. **Criterio:** bits por símbolo y estados, no sólo frase memorizada.

## QA y límites de uso

Fecha 2026-10-10: preguntas contrastadas con capturas, relaciones con F3/FV visuales; perro y ejemplo 4 estados recalculados. Respuestas debajo de su enunciado, origen eID conservados, sin preguntas nuevas. Las precisiones de banda/ruido se declaran para no evaluar una simplificación absoluta. Excluidos Q2 Fourier y Q3dBm de U3; no se evalúa PRI Europa pendiente. Estado **en-progreso** hasta reviews y comprobación transversal de los destinos U2/U6. Este repaso parcial no certifica la unidad entera.
