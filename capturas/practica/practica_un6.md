---
unidad: 6
tipo: consignas
numero: 6
tema: Capacidad de canales y tratamiento de errores
estado: borrador
fuentes:
  - capturas/practica/practica_un6.md
actualizado: 2026-10-13
---

# Trabajo práctico N.º 6

<div align="center">

**Capacidad de los canales, tasa de información y tratamiento de errores**

</div>

---

## Primera parte

### Capacidad de los canales y relación con la tasa de información

#### 1. Canal telefónico

Teniendo en cuenta que en un canal telefónico la relación señal-ruido típica es de **30 dB**, con:

- **FCI:** 300 Hz
- **FCS:** 3300 Hz

¿Cuál es el límite superior de la tasa de transmisión de datos confiable?

**solucion:**



#### 2. Relación señal-ruido

Calcular la relación señal-ruido **S/N**, expresada en dB, para los siguientes casos:

- **a.** $\Delta f = 3000\ \text{Hz}$, $C = 10\,000\ \text{bit/s}$.
- **b.** $\Delta f = 10\ \text{kHz}$, $C = 10\,000\ \text{bit/s}$.
- **c.** $\Delta f = 1\ \text{kHz}$, $C = 10\ \text{kbit/s}$.

Graficar la variación de **S/N**, expresada en dB, en función del ancho de banda $\Delta f$, expresado en Hz. Extraer conclusiones.

#### 3. Canal sin ruido

¿Cuál es la capacidad máxima de un canal sin ruido?

#### 4. Duplicación de la capacidad

Necesitamos duplicar la capacidad de transporte de información de un canal de datos cuyo ancho de banda es de **4 kHz** y cuya relación señal-ruido es de **20 dB**.

Sabiendo que utilizaremos el mismo canal, determinar cuántas veces debemos aumentar la potencia de la señal original para lograrlo.

¿Cuál es la nueva relación señal-ruido, expresada en dB?

#### 5. Aumento de la potencia de ruido

Tenemos un canal cuyo ancho de banda es de **4 kHz** y cuya relación señal-ruido es de **20 dB**.

Sabiendo que, por desperfectos, aumenta al doble su potencia de ruido, estimar en forma porcentual la caída en la capacidad de transporte.

¿Cuál es la nueva relación señal-ruido, expresada en dB?

#### 6. Línea telefónica

Se mide el rendimiento de una línea telefónica de **3,1 kHz de ancho de banda**. Cuando la señal es de **10 V** y el ruido es de **5 mV**:

¿Cuál es la tasa máxima de datos soportada por esta línea telefónica?

---

## Segunda parte

### Tratamiento de los errores en las redes de datos

#### 1. Causas de error

Indicar las principales causas de errores en las redes de datos.

#### 2. Políticas de tratamiento

¿Qué políticas se emplean para el tratamiento de los errores en las redes de datos?

#### 3. Corrección de errores y calidad de servicio

¿Cómo incide la corrección de errores en la calidad de servicio de las redes?

#### 4. Tasa de error de bit

En una red de transmisión de datos se reciben **20 bits erróneos** sobre un total de **200 000 bits**.

¿Cuál es el **BER**?

#### 5. Comportamiento de una LAN Ethernet

La medición anterior se realizó sobre una **LAN Ethernet**.

¿Qué comportamiento puede esperarse de dicha red?

#### 6. Detección de errores mediante CRC

Dado el siguiente mensaje a transmitir, $M(x)$, y teniendo como polinomio generador:

$$
G(x) = x^4 + x + 1
$$

Aplicar el método de detección de errores **CRC** y determinar la información a transmitir.

$$
M(x) = 1\ 0\ 1\ 1\ 0\ 1\ 0\ 1\ 1\ 0\ 1
$$

Repetir el procedimiento del lado del receptor y extraer conclusiones.

#### 7. Protocolos que emplean CRC

Citar por lo menos cuatro protocolos que empleen **CRC** para la detección de errores.

#### 8. Protocolos que emplean suma de verificación

Citar por lo menos cuatro protocolos que empleen el método de **suma de verificación** para la detección de errores.

#### 9. Códigos correctores de errores

Cuando se emplean códigos correctores de errores, citar ejemplos.

#### 10. Manifestación y medición del error

¿Cómo se manifiesta el error en las redes de datos y cómo se mide?
