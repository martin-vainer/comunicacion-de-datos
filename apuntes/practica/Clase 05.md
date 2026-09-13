8/9/2026

seguimos los ejercicios del TRABAJO PRÁCTICO N°3 :Medidas de Velocidad. Calculo de enlaces, unidades de medida. (resueltos en el archivo de la clase practica 04)

tambien se realizo este cuestionario:

# CUESTIONARIO UD Nro 3

## Pregunta 1 – Velocidad de modulación y ancho de banda

**Indicar las causas por las cuales no se puede aumentar en determinados canales de comunicaciones la velocidad de modulación.**

### Opciones

a. Porque si aumento la velocidad de modulación, disminuye el ancho de banda, y por lo tanto también aumenta la potencia de ruido.

b. **Porque si aumento la velocidad de modulación, aumenta el ancho de banda, y por lo tanto también aumenta el ruido. ✅**

c. Porque si aumento la velocidad de modulación, disminuye el ancho de banda, y por lo tanto no podemos aplicar transmisión multinivel.

### Respuesta correcta

**b. Porque si aumento la velocidad de modulación, aumenta el ancho de banda, y por lo tanto también aumenta el ruido.**

### Explicación

Al aumentar la **velocidad de modulación**, transmitimos más símbolos por segundo.

Eso hace que la señal cambie más rápidamente, por lo que necesita transmitir componentes de frecuencia más altas.

Por lo tanto:

**Mayor velocidad de modulación → mayor ancho de banda requerido**

Además, la potencia de ruido térmico depende del ancho de banda:

$$
N = kTB
$$

donde:

- $N$ = potencia de ruido
- $k$ = constante de Boltzmann
- $T$ = temperatura
- $B$ = ancho de banda

Entonces:

**Mayor ancho de banda → mayor potencia de ruido**

Por eso no siempre se puede aumentar indefinidamente la velocidad de modulación: el canal tiene un ancho de banda limitado y además aumenta el ruido recibido.

---

## Pregunta 2 – Velocidad real de transferencia de datos

**¿Cuál es la velocidad real de transferencia de datos y en qué se mide?**

### Opciones

a. Es la cantidad de bits transmitidos que contienen información con o sin errores en un tiempo determinado. Se mide en bps.

b. Es la cantidad de bits transmitidos en un tiempo determinado. Se mide en baudios.

c. **Es la cantidad de bits transmitidos que contienen información sin errores en un tiempo determinado. Se mide en bps. ✅**

### Respuesta correcta

**c. Es la cantidad de bits transmitidos que contienen información sin errores en un tiempo determinado. Se mide en bps.**

### Explicación

La **velocidad real de transferencia de datos** tiene en cuenta solamente los bits de información que llegan correctamente al receptor.

Por eso se consideran los bits:

- útiles;
- correctamente recibidos;
- sin errores.

Se mide en:

$$
\boxed{bps = bits\ por\ segundo}
$$

La opción **b** es incorrecta porque los **baudios** no miden bits por segundo, sino símbolos por segundo.

**Idea importante:**

- **bps → bits por segundo**
- **baudios → símbolos por segundo**

---

## Pregunta 3 – Unidad dBm

**¿La unidad de medida dBm es para medir niveles de potencia?**

### Opciones

- **Verdadero ✅**
- Falso

### Respuesta correcta

**Verdadero**

### Explicación

El **dBm** se utiliza para expresar un nivel de potencia tomando como referencia una potencia de:

$$
1\ mW
$$

La fórmula es:

$$
P_{dBm} = 10\log_{10}\left(\frac{P}{1\ mW}\right)
$$

Algunos valores de referencia:

$$
1\ mW = 0\ dBm
$$

$$
10\ mW = 10\ dBm
$$

$$
100\ mW = 20\ dBm
$$

Por lo tanto, el dBm expresa un **nivel absoluto de potencia** referido a $1\ mW$.

---

## Pregunta 4 – Relación entre baudios y bps

**¿Cuál de las siguientes afirmaciones describe correctamente la relación entre baudios y bits por segundo (bps)?**

### Opciones

a. Siempre son iguales independientemente del sistema de modulación.

b. **Los bps pueden ser mayores que los baudios si cada símbolo representa más de un bit. ✅**

c. Los baudios siempre son mayores que los bps.

### Respuesta correcta

**b. Los bps pueden ser mayores que los baudios si cada símbolo representa más de un bit.**

### Explicación

Los **baudios** indican cuántos símbolos se transmiten por segundo:

$$
1\ baud = 1\ símbolo/s
$$

Los **bps** indican cuántos bits se transmiten por segundo:

$$
1\ bps = 1\ bit/s
$$

La relación entre ambos es:

$$
R_b = R_s \cdot \log_2(M)
$$

donde:

- $R_b$ = velocidad de transmisión en bps
- $R_s$ = velocidad de modulación en baudios
- $M$ = cantidad de símbolos posibles

### Ejemplo

Si tenemos una modulación con:

$$
M = 4
$$

cada símbolo representa:

$$
\log_2(4)=2\ bits
$$

Si transmitimos a:

$$
1000\ baudios
$$

entonces:

$$
R_b = 1000 \cdot 2
$$

$$
R_b = 2000\ bps
$$

Por lo tanto:

$$
\boxed{2000\ bps > 1000\ baudios}
$$

Esto ocurre porque cada símbolo representa más de un bit.

---

# Resumen rápido

- **Mayor velocidad de modulación → mayor ancho de banda requerido**
- **Mayor ancho de banda → mayor potencia de ruido**
- **Velocidad real de transferencia → bits útiles recibidos sin errores por segundo**
- **bps → bits por segundo**
- **baudios → símbolos por segundo**
- **dBm → nivel de potencia referido a 1 mW**
- Si cada símbolo representa más de un bit:

$$
\boxed{bps > baudios}
$$

- Relación general:

$$
\boxed{R_b = R_s \cdot \log_2(M)}
$$