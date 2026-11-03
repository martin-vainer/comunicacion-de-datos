---
unidad: 5
tipo: cuestionario
estado: borrador
fuentes:
  - Consignas y opciones aportadas por el estudiante en conversación (2026-10-13)
  - material/practica/U 5/TP  5  2026.pdf, p. 2, ejercicio 2 (mismo tren; consigna más amplia)
  - capturas/teoria/05-Teoría de la información y de la codificación/01_10_26_U5.md, §8
  - material/teoria/U6/U 6 Canales de Comunicaciones y control de errores.pdf, p. 3
actualizado: 2026-10-13
---

# Cuestionario — Unidad 5: entropía de una fuente binaria

**Alcance:** cuestionario en desarrollo; por ahora contiene tres preguntas tipo test. No es una evaluación integral de la unidad.

**Origen:** las consignas y opciones siguientes se transcriben de los mensajes del estudiante. El TP5 oficial contiene el mismo tren de pulsos que Q01, pero su ejercicio 2 también pide la información asociada a cada símbolo; no se presenta como fuente de esas opciones.

### Q01 — Entropía de una secuencia binaria

#### Enunciado original (transcripción literal)

> Dado un tren de pulsos correspondientes a la siguiente secuencia: 010101000001, Calcular la ENTROPÍA de la fuente
>
> Pregunta 1Respuesta
> a.
> 0,9 Sh/Simbolo
> b.
> 0,92 Sh/Simbolo
> c.
> 0,92 Sh/Seg

#### Datos y condiciones

- **Datos numéricos:** secuencia `010101000001`, con 12 símbolos observados: ocho ceros y cuatro unos.
- **Premisas o condiciones:** se estiman las probabilidades de la fuente con las frecuencias relativas de esta muestra y se aplica el modelo de fuente binaria de memoria nula. La secuencia sola no demuestra independencia ni determina las probabilidades verdaderas de la fuente.
- **Qué se pide:** calcular la entropía media por símbolo y elegir la opción correspondiente.
- **Dato que falta para una tasa:** no se informa duración de símbolo ni ritmo de emisión.

<details>
<summary>Mostrar resolución razonada</summary>

#### Resolución paso a paso

1. **Interpretación:** la entropía promedia la información de los resultados posibles; no es la información puntual de un cero o un uno ni una cantidad por unidad de tiempo.
2. **Probabilidades estimadas:**

   $$\widehat p_0=\frac{8}{12}=\frac23,\qquad \widehat p_1=\frac{4}{12}=\frac13$$

3. **Formalización y unidades:**

   $$\widehat H(X)=-\sum_i \widehat p_i\log_2\widehat p_i$$

   | Símbolo | Significado | Unidad |
   |---|---|---|
   | $X$ | Símbolo emitido por la fuente | símbolo |
   | $\widehat p_i$ | Probabilidad estimada del símbolo $i$ | Adimensional |
   | $\widehat H(X)$ | Información media estimada por símbolo | Shannon/símbolo |

   **Supuesto:** modelo discreto de dos símbolos y memoria nula, usando las frecuencias observadas como estimaciones de probabilidad.

4. **Cálculo:**

   $$\begin{aligned}
   \widehat H(X)&=-\left(\frac23\log_2\frac23+\frac13\log_2\frac13\right)\\
   &=0{,}9182958\ldots\ \text{Shannon/símbolo}\approx0{,}92\ \text{Shannon/símbolo}.
   \end{aligned}$$

5. **Respuesta y revisión de opciones:**
   - **b** es la opción más precisa y probablemente la esperada.
   - **a también es válida** si se redondea el mismo resultado a una cifra decimal: $0{,}9183\ldots\to0{,}9$. Por eso el ítem no tiene una respuesta única si no se fija la precisión de redondeo.
   - **c no corresponde:** `Sh/Seg` expresa una tasa; para obtenerla haría falta multiplicar la entropía por el ritmo de emisión en símbolos/s. Ese dato no está dado.

**Fuente/evidencia de la respuesta:** [TP5 oficial, p. 2, ejercicio 2](../../material/practica/U%205/TP%20%205%20%202026.pdf), que contiene la misma secuencia y pide también la información de cada símbolo; [resolución desarrollada del TP5, ejercicio 2](../practica/tp-05-informacion-codificacion.md#ejercicio-02); definición y unidad en [apunte canónico U5, §3](../teoria/05-teoria-informacion-codificacion/APUNTE.md#entropia). El cálculo se verifica con las frecuencias relativas y la fórmula de entropía; las opciones tipo test proceden del mensaje del estudiante.

</details>

### Q02 — Condición de entropía máxima

#### Enunciado original (transcripción literal)

> **Cuando la Entropia de una fuente es Máxima ?**
>
> Pregunta 2Respuesta<br>
> a.<br>
> Cuando la Fuente es equiprobale.&#92;<br>
> b.<br>
> Cuando la Fuente genera simbolos con distinta probabilidad de ocurrencia.&#92;<br>
> c.<br>
> Cuando la Fuente es equiprobale y de memoria nula.

#### Datos y condiciones

- **Datos numéricos:** no se proporcionan probabilidades ni la cantidad $N$ de símbolos del alfabeto.
- **Premisas o condiciones:** se compara la entropía para un alfabeto fijo. En el enfoque de la unidad, la entropía por símbolo se estudia para una fuente de memoria nula; si la fuente tiene memoria, hay que distinguir la entropía marginal de la incertidumbre nueva por símbolo.
- **Qué se pide:** identificar cuándo se alcanza la entropía máxima.

<details>
<summary>Mostrar resolución razonada</summary>

#### Resolución paso a paso

1. **Concepto:** con un alfabeto fijo de $N$ símbolos, la entropía de un símbolo alcanza su máximo cuando las alternativas son equiprobables. Si un símbolo aparece con más probabilidad que otros, hay más posibilidad de anticiparlo y la entropía es menor.
2. **Formalización y unidades:**

   $$H(X)=-\sum_{i=1}^{N}p_i\log_2 p_i\leq\log_2 N$$

   | Símbolo | Significado | Unidad |
   |---|---|---|
   | $N$ | Cantidad de símbolos posibles del alfabeto | Símbolos |
   | $p_i$ | Probabilidad del símbolo $i$ | Adimensional; $\sum_i p_i=1$ |
   | $H(X)$ | Entropía de un símbolo | Shannon/símbolo |

   La igualdad $H(X)=\log_2 N$ se alcanza si y sólo si $p_i=1/N$ para todo $i$. Para una fuente binaria equiprobable, $H(X)=\log_2 2=1$ Shannon/símbolo.

3. **Qué aporta “memoria nula”:** significa que cada símbolo es independiente de los anteriores. La equiprobabilidad marginal, por sí sola, no demuestra independencia. Por ejemplo, una fuente que alterna determinísticamente 0 y 1, empezando con una fase aleatoria, tiene $P(0)=P(1)=0{,}5$ y $H(X_n)=1$ Shannon/símbolo; una vez conocido el símbolo anterior, el siguiente queda determinado, así que no aporta incertidumbre nueva.

4. **Respuesta y revisión de opciones:**
   - **c** es la respuesta más completa y probablemente la esperada si se pregunta por una fuente cuya entropía por emisión está modelada sin memoria.
   - **a también es verdadera** para maximizar la entropía de la distribución de un símbolo con alfabeto fijo. Además, c incluye la condición de a; por lo tanto, tal como está escrito, el test permite más de una respuesta defendible.
   - **b es incorrecta:** probabilidades distintas no maximizan la entropía para un alfabeto fijo.

**Fuente/evidencia de la respuesta:** [apunte canónico U5, §3](../teoria/05-teoria-informacion-codificacion/APUNTE.md#entropia), que establece el máximo con símbolos equiprobables y advierte que equiprobabilidad y memoria nula son supuestos distintos. La elección de **c** como respuesta esperada es una inferencia por el encuadre del curso, no una clave oficial provista.

</details>

### Q03 — Tasa de información y capacidad del canal

#### Enunciado original (transcripción literal)

> **Que relación existe entre la Tasa de Información de una fuente y la Capacidad de un canal ??**
>
> Pregunta 3Respuesta<br>
> a.<br>
> Que la tasa de información debe ser menor o igual a la capacidad de un canal.<br>
> b.<br>
> Que la capacidad de un canal eventualmente debe ser mayor a la tasa de información.<br>
> c.<br>
> Que la tasa de información debe ser eventualmente menor a la capacidad de un canal.

#### Datos y condiciones

- **Datos numéricos:** no se dan valores de tasa ni de capacidad.
- **Premisas o condiciones:** comparar magnitudes en unidades informativas por segundo compatibles y respecto del modelo de canal considerado.
- **Qué se pide:** expresar la relación general entre la tasa informativa generada por la fuente y la capacidad máxima del canal.

<details>
<summary>Mostrar resolución razonada</summary>

#### Resolución paso a paso

1. **Concepto:** la fuente genera información a una tasa $\Gamma$; el canal tiene una capacidad máxima $C$. Si $\Gamma>C$, la fuente ofrece información más rápido de lo que el canal puede sostener según ese modelo, y la transmisión no puede mantenerse sin exceder el límite.
2. **Formalización y unidades:**

   $$\Gamma=\frac{H(X)}{\overline{\tau}},\qquad \Gamma\leq C$$

   | Símbolo | Significado | Unidad |
   |---|---|---|
   | $H(X)$ | Información media por símbolo de la fuente | Shannon/símbolo |
   | $\overline{\tau}$ | Duración media de un símbolo | s/símbolo |
   | $\Gamma$ | Tasa de información de la fuente | Shannon/s; bit/s en base 2 |
   | $C$ | Capacidad máxima del canal según su modelo | bit/s; comparable con Shannon/s en base 2 |

   **Supuesto:** fuente y canal se comparan en la misma escala de información por segundo. En el modelo del curso, $\Gamma\leq C$ es el límite general; para diseñar comunicación asintóticamente fiable se opera por debajo, con $\Gamma<C$ y codificación adecuada.

3. **Ejemplo:** si la fuente genera $1000$ Shannon/s y el canal ofrece $800$ bit/s, las unidades son comparables en base 2 y $\Gamma>C$. Esa demanda excede la capacidad; no alcanza con aumentar la velocidad física sin cambiar las condiciones del canal o reducir la tasa de información.

4. **Respuesta y revisión de opciones:**
   - **a** expresa la relación general $\Gamma\leq C$ que figura en el material de U5.
   - **b y c** expresan, con las mismas palabras en distinto orden, el caso más estricto $\Gamma<C$. Esa condición es apropiada para comunicación asintóticamente fiable, pero no es distinta entre ambas opciones y ya cumple la desigualdad de a.
   - **Conclusión:** la respuesta más directa al enunciado general es **a**. Si se busca una sola respuesta, convendría quitar `eventualmente` de b/c o aclarar que se pregunta por el régimen de comunicación fiable; tal como están, las tres opciones se solapan.

**Fuente/evidencia de la respuesta:** la [captura teórica U5, §8](../../capturas/teoria/05-Teor%C3%ADa%20de%20la%20informaci%C3%B3n%20y%20de%20la%20codificaci%C3%B3n/01_10_26_U5.md) expresa $\Gamma\leq C$; el [PDF de canales U6, p. 3](../../material/teoria/U6/U%206%20Canales%20de%20Comunicaciones%20y%20control%20de%20errores.pdf) define $C$ como velocidad máxima y señala que $\Gamma>C$ provoca errores. La precisión sobre operar por debajo para fiabilidad asintótica está desarrollada en [apunte canónico U5, §4](../teoria/05-teoria-informacion-codificacion/APUNTE.md#tasa) y [apunte U6, §2](../teoria/06-canales-comunicaciones/APUNTE.md#capacidad).

</details>

## Control y límites

**Q01:** la clave no debe publicarse como inequívocamente `b` sin advertir la ambigüedad: `a` es el mismo resultado redondeado a menos cifras. Ninguna de las opciones permite inferir un valor exacto ni una tasa temporal.

**Q02:** la clave más completa es `c`, pero `a` también expresa una condición suficiente para maximizar la entropía de un símbolo con alfabeto fijo. No se encontró una clave oficial que resuelva esta superposición de opciones.

**Q03:** `a` es la relación general; para fiabilidad asintótica se exige diseñar por debajo de la capacidad. b y c expresan el mismo caso estricto y son más fuertes que a, así que el ítem no separa las respuestas con claridad.
