---
unidad: 2
tema: Ancho de banda
estado: completo
fuentes:
  - "material/teoria/U2/U 2 Características de las señales de telecom.pdf, pp. 7 y 22-24"
  - "material/practica/TP  2  2026.pdf, pp. 2-3"
  - "Ejercicio cuestionario 10-09-2026.pdf, pp. 1-3"
actualizado: 2026-09-13
---

# Ancho de banda

**Idea central**

> El ancho de banda mide un intervalo de frecuencias, pero el criterio que fija sus extremos depende de
> si hablamos de una señal, un canal o una convención de ejercicio.

**Por qué importa**

Una señal necesita componentes espectrales; un canal sólo transmite adecuadamente una región del
espectro. Comparar ambas cosas permite anticipar distorsión y, más adelante, entender límites de
velocidad. **Ancho de banda se mide en hertz; no en bit/s ni en baudios.**

**Requisito previo**

- [Serie de Fourier](serie-de-fourier.md) — de dónde salen las componentes del espectro.

> **Procedencia:** las definiciones de señal y línea corresponden a la presentación de U2, pp. 7 y
> 22-24. Las capturas [Teoría 2](apuntes-clase%202.md), [Teoría 3](apuntes-clase3.md) y
> [Práctica 2](../../practica/clase%2002.md) conservan el recorrido de clase, pero no son la autoridad.

---

## 1) El problema: ni la señal ni el medio son ideales

Una transición perfectamente vertical exige componentes de frecuencia arbitrariamente altas. Ningún
medio físico real las transmite todas con la misma ganancia y fase. Al limitar el espectro, el receptor
obtiene una señal redondeada o deformada.

### Modelo mental

Pensá el canal como una ventana sobre el eje de frecuencias:

```text
espectro que necesita la señal ∩ frecuencias que deja pasar el canal
                         ↓
             componentes que llegan al receptor
```

La presentación de U2, p. 23, confirma visualmente esto: al reducir el ancho de banda de un canal, una
señal digital periódica pierde detalle hasta parecerse a una senoidal.

---

## 2) Ancho de banda de una señal

### Concepto

El material de cátedra lo define como el intervalo del espectro donde se concentra la mayor cantidad de
energía. Para calcularlo hay que declarar **qué criterio delimita ese intervalo**: componentes no nulas,
porcentaje de energía, nivel relativo o primer cero, según el problema.

Si los extremos elegidos son $f_L$ y $f_H$:

$$
B=f_H-f_L
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $B$ | ancho de banda | Hz |
| $f_L$ | frecuencia límite inferior | Hz |
| $f_H$ | frecuencia límite superior | Hz |

**Supuestos y límites de validez:** la resta sólo mide el intervalo; no decide los límites. El criterio
para elegir $f_L$ y $f_H$ debe acompañar siempre el resultado. Una onda cuadrada ideal tiene ancho de
banda matemático infinito, aunque en ingeniería se la aproxime con uno finito.

### Ejemplo numérico

Si se decide conservar las componentes comprendidas entre $300\ \text{Hz}$ y $3400\ \text{Hz}$:

$$
B=3400\ \text{Hz}-300\ \text{Hz}=3100\ \text{Hz}=3{,}1\ \text{kHz}
$$

**Verificación de razonabilidad:** el extremo superior es mayor y la resta conserva la unidad Hz. No
puede concluirse cuánta información se transmite sólo con este número.

---

## 3) Ancho de banda de un canal por puntos de 3 dB

### Concepto

Para la línea de transmisión, la presentación de U2, p. 7, toma el intervalo entre las frecuencias donde
la atenuación alcanza $3\ \text{dB}$ respecto de una frecuencia de referencia. Si esas frecuencias son
$f_1$ y $f_2$, el ancho de banda del canal es $B=f_2-f_1$.

Una caída de potencia de aproximadamente $3\ \text{dB}$ representa cerca de la mitad de potencia:

$$
\frac{P_2}{P_1}=10^{-3/10}\approx0{,}501
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $P_1$ | potencia en la referencia | W |
| $P_2$ | potencia en el punto de corte | W |
| $P_2/P_1$ | relación de potencias | adimensional |
| $f_1,f_2$ | puntos de corte inferior y superior | Hz |

**Supuestos y límites de validez:** el valor $-3\ \text{dB}$ se interpreta aquí como relación de
potencias. Hablar de $20\log_{10}$ para tensión sólo es equivalente cuando las impedancias comparadas
son iguales.

### Caso real

Filtros, amplificadores y líneas se caracterizan mediante su respuesta en frecuencia. Dos equipos
pueden anunciar el mismo intervalo en hertz, pero no ser equivalentes si usan tolerancias o criterios de
corte distintos.

---

## 4) Tren de pulsos y primer cero

Para el tren rectangular estudiado en [Serie de Fourier](serie-de-fourier.md#2-forma-compleja-y-tren-rectangular),
la envolvente espectral tiene su primer cero positivo en:

$$
B_{\text{primer cero}}=\frac{1}{\tau}
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $B_{\text{primer cero}}$ | intervalo desde continua hasta el primer cero | Hz |
| $\tau$ | duración del pulso rectangular | s |

**Supuestos y límites de validez:** no es una ley universal de ancho de banda. Es el criterio explícito
del TP 2 para un pulso rectangular ideal. El espectro continúa después del primer cero en lóbulos de
menor amplitud.

En el ejercicio con $V_m=2000\ \text{baudios}$ se toma $\tau=1/V_m=0{,}5\ \text{ms}$; entonces:

$$
B_{\text{primer cero}}=\frac{1}{0{,}0005\ \text{s}}=2000\ \text{Hz}
$$

Las líneas están separadas por $FRP=100\ \text{Hz}$, por lo que el primer cero coincide con
$n=2000/100=20$. La componente $n=20$ vale cero: hay **19 armónicas no nulas** entre la continua y el
primer cero, aunque el material resuelto usa la frase “20 armónicas hasta el primer cero”.

### Error típico

- **Error:** repetir $B=1/\tau$ para cualquier señal o canal.
  **Por qué está mal:** esa igualdad sale de los ceros de la sinc de un pulso rectangular.
  **Lo correcto:** nombrar la forma de señal y el criterio de primer cero.
- **Error:** expresar ancho de banda en bit/s.
  **Por qué está mal:** bit/s mide tasa de transmisión; Hz mide extensión espectral.
  **Lo correcto:** relacionarlos más adelante mediante un modelo con supuestos, como Nyquist o Shannon.
- **Error:** creer que fuera del ancho de banda la energía desaparece siempre.
  **Por qué está mal:** una definición efectiva o a $3\ \text{dB}$ fija un límite convencional; no afirma
  que el espectro sea exactamente cero.

### Para examen

> El ancho de banda es un intervalo de frecuencias medido en hertz. Sus extremos dependen del criterio:
> para una línea pueden ser los puntos de $3\ \text{dB}$ y, para el tren rectangular del TP, se toma el
> primer cero de la envolvente en $1/\tau$. Por eso nunca hay que dar un ancho de banda sin decir de qué
> objeto se habla y cómo se delimitó.

---

## 5) Pendiente de contraste

La frase de cátedra “donde se concentra la mayor cantidad de energía” no fija un porcentaje ni umbral
único para una señal genérica. Se conserva como definición cualitativa y se explicitan criterios
calculables por separado. Falta contrastar la terminología exacta con la bibliografía obligatoria antes
de marcar este apunte `revisado`.

---

## 6) Resumen mental

Si te preguntan **“¿qué es ancho de banda?”**, contestá:

> Es el intervalo de frecuencias relevante de una señal o utilizable de un canal, medido en hertz. Se
> calcula como frecuencia superior menos inferior, pero esos extremos requieren un criterio explícito.
> Si el canal deja afuera componentes importantes, la forma recibida se distorsiona.

**Checklist para examen**

- decir Hz, no bit/s ni baudios;
- distinguir ancho de banda de señal y de canal;
- declarar el criterio de corte;
- explicar los puntos de $3\ \text{dB}$;
- limitar $1/\tau$ al pulso rectangular y al primer cero;
- conectar menos ancho de banda con mayor deformación.

## Relación con otras unidades

- **U3:** velocidad de modulación y velocidad de transmisión;
- **U4:** espectro de señales moduladas;
- **U6:** capacidad de canal según Nyquist y Shannon-Hartley.

## Preguntas de autoevaluación

1. ¿Por qué “una señal ocupa 2000 Hz” queda incompleto si no se declara el criterio?
2. ¿Qué pasa con el primer cero espectral si $\tau$ se reduce a la mitad?
3. ¿Por qué $-3\ \text{dB}$ no significa que a partir del corte no exista señal?
