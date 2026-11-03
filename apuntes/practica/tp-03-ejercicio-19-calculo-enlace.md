---
unidad: 7
tipo: tp
numero: 3
tema: Ejercicio 19 — cálculo de enlace con amplificador
estado: revisado
fuentes:
  - "material/practica/U 3/TP   3   2026.pdf, p. 4"
  - "material/practica/TRABAJO PRACTICO  EJ 19 CALCULO ENLACE.pdf, secciones 7 a 10, pp. 2-3"
procedencia:
  - "capturas/practica/clase 04.md, sección Ejercicio 19"
actualizado: 2026-10-13
---

## Ejercicio 19 — TP: cálculo de enlace con amplificador

**Estado de este ejercicio:** revisado contra el enunciado y verificado numéricamente.

**Fuentes de la consigna y los datos:** [TP3 oficial, p. 4](../../material/practica/U%203/TP%20%20%203%20%20%202026.pdf) contiene el ejercicio y el esquema de enlace. La guía ampliada [Cálculo de Enlace — Año 2026, secciones 7 a 10, pp. 2–3](../../material/practica/TRABAJO%20PRACTICO%20%20EJ%2019%20CALCULO%20ENLACE.pdf) aporta objetivos, parámetros y condiciones de entrega; su [cache textual](../../material/_cache/trabajo-practico-ej-19-calculo-enlace.txt) se usa sólo para búsqueda. Los cuatro conectores se identifican en el dibujo de la guía ampliada, p. 3, no en su extracción de texto.

### Enunciado oficial — transcripción literal (TP3, p. 4)

> 19. Para el siguiente enlace de comunicaciones en forma alámbrica (a través de una fibra óptica) entre dos puntos distantes dentro de la Ciudad Autónoma de Buenos Aires, uno es una Empresa cuya casa Matriz se encuentra en el límite con la Av Grl Paz a la altura de la localidad de Mataderos y el otro el Depósito de mercaderías de la citada empresa con ubicación en la Av Beiró a la altura de la localidad de Villa Devoto, Calcular los siguientes parámetros para que el enlace funcione correctamente:
>
> a) Calcular la ganancia y la sensibilidad del amplificador necesario para que el enlace funcione correctamente.
>
> Obtener : GA(Ganancia del Amp) y SA(Sensibilidad del Amp)
>
> b) Recalcular para L1 = 100m y L2 = 2000m. Analizar los resultados.
>
> c) Si se consiguen amplificadores de 3dB, 6dB y 9dB, ¿Cuál elegiría?, ¿Qué consecuencias trae para el circuito la elección que acaba de realizar ?

**Datos del enunciado y fuentes por dato:**

| Magnitud | Valor del enunciado | Fuente |
|---|---|---|
| Potencia de transmisión | $PTx=-3\ \mathrm{dBm}$ | TP3 p. 4; guía ampliada §8, p. 3 |
| Sensibilidad del receptor | $SRx=1\ \mathrm{mW}$ | TP3 p. 4; guía ampliada §8, p. 3 |
| Distancias iniciales | $L_1=500\ \mathrm{m}$; $L_2=1000\ \mathrm{m}$ | TP3 p. 4; guía ampliada §8, p. 3 |
| Atenuación por conector | $At=0.25\ \mathrm{dB}$ cada uno | TP3 p. 4; guía ampliada §8, p. 3 |
| Atenuación de fibra óptica | $1.0\ \mathrm{dB}/1000\ \mathrm{m}$ | TP3 p. 4; guía ampliada §8, p. 3 |
| Amplificadores disponibles para el inciso c | 3 dB, 6 dB y 9 dB | TP3 p. 4; guía ampliada §7, p. 3 |

El diagrama de la guía ampliada p. 3 muestra dos conectores por tramo, cuatro en total; ese detalle visual se usa para el cálculo y se atribuye a esa figura. El esquema del TP3 p. 4 muestra Tx–Amp–Rx y las longitudes $L_1$, $L_2$.

El inciso b sustituye las distancias por $L_1=100\ \mathrm{m}$ y $L_2=2000\ \mathrm{m}$. La guía ampliada especifica «La Ganancia (Ganancia del Amplificador) y SA (Sensibilidad del Amplificador)» para el inciso a; se conserva esa aclaración como texto de la guía, no se inserta en la transcripción del enunciado TP3. Las secciones 9–10 de esa guía piden resolución manuscrita, prolija, en orden a), b), c), y entrega escaneada en un solo PDF; son instrucciones de entrega, no condiciones físicas del cálculo.

### Conceptos que se aplican

**Idea física:** la fibra y los conectores atenúan la señal. El amplificador debe recibir una señal suficiente para funcionar y elevar su potencia para compensar las pérdidas restantes hasta el receptor. Son dos requisitos diferentes: **sensibilidad de entrada** y **ganancia**.

El método es el mismo balance de potencia de los ejercicios anteriores: en unidades logarítmicas, las pérdidas se restan y las ganancias se suman. No corresponde calcular pérdidas de propagación de microondas porque el vínculo es una fibra óptica.

```mermaid
flowchart LR
    TX[Transmisor] --> C1[Conector 1]
    C1 --> F1[Fibra L1]
    F1 --> C2[Conector 2]
    C2 --> AMP[Amplificador]
    AMP --> C3[Conector 3]
    C3 --> F2[Fibra L2]
    F2 --> C4[Conector 4]
    C4 --> RX[Receptor]
```

### Resolución paso a paso

#### Planteo general (notación y conversiones)

| Magnitud | Símbolo | Valor |
|---|---|---|
| Potencia del transmisor | $P_{Tx}$ | $-3\ \mathrm{dBm}$ |
| Sensibilidad del receptor | $S_{Rx}$ | $1\ \mathrm{mW}$ |
| Atenuación de la fibra | $\alpha_{FO}$ | $1\ \mathrm{dB/km}$ |
| Pérdida por conector | $A_c$ | $0{,}25\ \mathrm{dB}$ |
| Cantidad de conectores | — | 4 en total; 2 por tramo |

**Paso 1 — normalizar unidades:** para trabajar con el balance convierto la sensibilidad del receptor a dBm:

$$
S_{Rx}=10\log_{10}\left(\frac{1\ \mathrm{mW}}{1\ \mathrm{mW}}\right)
=\boxed{0\ \mathrm{dBm}}
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $S_{Rx}$ | Nivel mínimo de potencia que requiere el receptor | dBm en el balance |
| $1\ \mathrm{mW}$ del denominador | Potencia de referencia del dBm | mW |

Uso $10\log_{10}$ porque convierto **potencia**, no tensión. El argumento del logaritmo es adimensional.

**Paso 2 — modelar pérdidas:** llamo $A_1$ y $A_2$ a las pérdidas de cada tramo, incluyendo sus dos conectores:

$$
A_i=\alpha_{FO}L_i+2A_c\qquad(i=1,2)
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $A_i$ | Atenuación total del tramo $i$ | dB |
| $\alpha_{FO}$ | Atenuación por unidad de longitud | dB/km |
| $L_i$ | Longitud del tramo $i$ | km |
| $A_c$ | Atenuación de cada conector | dB |

Se utiliza la atenuación constante indicada en el enunciado. No se agregan empalmes ni otras pérdidas no especificadas.

**Paso 3 — plantear el balance:** la condición de funcionamiento del enlace es:

$$
P_{Rx}=P_{Tx}-A_1+G-A_2\geq S_{Rx}
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $P_{Rx}$, $P_{Tx}$ | Niveles de potencia recibida y transmitida | dBm |
| $A_1$, $A_2$ | Pérdidas de los tramos | dB |
| $G$ | Ganancia de potencia del amplificador | dB |
| $S_{Rx}$ | Umbral del receptor | dBm |

Para hallar la ganancia mínima tomo la igualdad. **No agrego factor de diseño porque no está indicado.** El cálculo utiliza el modelo de balance de potencia de la práctica; supone que el amplificador puede entregar la potencia calculada sin saturarse.

#### a) Ganancia y sensibilidad para las distancias originales

**1. Atenuaciones.** Convierto las longitudes: $L_1=0{,}5\ \mathrm{km}$ y $L_2=1\ \mathrm{km}$.

$$
A_1=1\ \frac{\mathrm{dB}}{\mathrm{km}}\cdot0{,}5\ \mathrm{km}
+2\cdot0{,}25\ \mathrm{dB}=\boxed{1\ \mathrm{dB}}
$$

$$
A_2=1\ \frac{\mathrm{dB}}{\mathrm{km}}\cdot1\ \mathrm{km}
+2\cdot0{,}25\ \mathrm{dB}=\boxed{1{,}5\ \mathrm{dB}}
$$

**2. Sensibilidad requerida.** Primero calculo cuánto llega al amplificador:

$$
P_{\mathrm{ent,A}}=P_{Tx}-A_1
=-3\ \mathrm{dBm}-1\ \mathrm{dB}=\boxed{-4\ \mathrm{dBm}}
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $P_{\mathrm{ent,A}}$ | Nivel de potencia en la entrada del amplificador | dBm |
| $P_{Tx}$ | Nivel de potencia transmitida | dBm |
| $A_1$ | Pérdida antes del amplificador | dB |

El umbral de sensibilidad del amplificador debe ser igual o inferior a la potencia que llega:

$$
\boxed{S_A\leq-4\ \mathrm{dBm}}
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $S_A$ | Umbral mínimo de potencia de entrada que admite el amplificador | dBm |

El valor límite solicitado es **$S_A=-4\ \mathrm{dBm}$**. Por ejemplo, un umbral de $-5\ \mathrm{dBm}$ también sirve; uno de $-3\ \mathrm{dBm}$ no alcanza a admitir la señal de $-4\ \mathrm{dBm}$.

Como referencia, convierto el nivel de entrada a potencia:

$$
P=1\ \mathrm{mW}\cdot10^{p/10}
=1\ \mathrm{mW}\cdot10^{-4/10}
\approx\boxed{0{,}398\ \mathrm{mW}}
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $P$ | Potencia lineal | mW |
| $p$ | Valor numérico del nivel expresado en dBm; aquí $-4$ | — |

La conversión usa la referencia de $1\ \mathrm{mW}$; un nivel negativo en dBm no significa potencia negativa.

**3. Ganancia mínima.** Despejo del balance:

$$
G_{\min}=S_{Rx}-P_{Tx}+A_1+A_2
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $G_{\min}$ | Ganancia para llegar justo al umbral del receptor, sin margen | dB |
| $S_{Rx}$, $P_{Tx}$ | Niveles de sensibilidad y transmisión | dBm |
| $A_1$, $A_2$ | Pérdidas de cada tramo | dB |

$$
G_{\min}=0\ \mathrm{dBm}-(-3\ \mathrm{dBm})+1\ \mathrm{dB}+1{,}5\ \mathrm{dB}
=\boxed{5{,}5\ \mathrm{dB}}
$$

**Comprobación:** al amplificador llegan $-4\ \mathrm{dBm}$; con $5{,}5\ \mathrm{dB}$ de ganancia salen $1{,}5\ \mathrm{dBm}$. El segundo tramo pierde $1{,}5\ \mathrm{dB}$, de modo que llegan al receptor $0\ \mathrm{dBm}=1\ \mathrm{mW}$, exactamente su sensibilidad.

#### b) Recálculo para L1 = 100 m y L2 = 2000 m

**1. Atenuaciones.** Ahora $L_1=0{,}1\ \mathrm{km}$ y $L_2=2\ \mathrm{km}$:

$$
A_1=1\ \frac{\mathrm{dB}}{\mathrm{km}}\cdot0{,}1\ \mathrm{km}
+0{,}5\ \mathrm{dB}=\boxed{0{,}6\ \mathrm{dB}}
$$

$$
A_2=1\ \frac{\mathrm{dB}}{\mathrm{km}}\cdot2\ \mathrm{km}
+0{,}5\ \mathrm{dB}=\boxed{2{,}5\ \mathrm{dB}}
$$

**2. Sensibilidad requerida.** Aplicando el mismo balance al primer tramo:

$$
P_{\mathrm{ent,A}}=-3\ \mathrm{dBm}-0{,}6\ \mathrm{dB}
=\boxed{-3{,}6\ \mathrm{dBm}}
$$

$$
\boxed{S_A\leq-3{,}6\ \mathrm{dBm}}
$$

El valor límite es $-3{,}6\ \mathrm{dBm}$, equivalente a:

$$
P=1\ \mathrm{mW}\cdot10^{-3{,}6/10}
\approx\boxed{0{,}437\ \mathrm{mW}}
$$

**3. Ganancia mínima.**

$$
G_{\min}=0\ \mathrm{dBm}-(-3\ \mathrm{dBm})+0{,}6\ \mathrm{dB}+2{,}5\ \mathrm{dB}
=\boxed{6{,}1\ \mathrm{dB}}
$$

**Comprobación:** entran al amplificador $-3{,}6\ \mathrm{dBm}$ y salen $2{,}5\ \mathrm{dBm}$. Después de perder $2{,}5\ \mathrm{dB}$ en el segundo tramo, llegan $0\ \mathrm{dBm}$ al receptor.

**Análisis:** al acortarse el primer tramo, llega más potencia al amplificador: pasa de $-4$ a $-3{,}6\ \mathrm{dBm}$. Por eso, la sensibilidad requerida es menos exigente. Sin embargo, la longitud total aumenta de $1{,}5$ a $2{,}1\ \mathrm{km}$. Los $0{,}6\ \mathrm{km}$ adicionales producen $0{,}6\ \mathrm{dB}$ más de pérdida; la ganancia mínima aumenta en esa misma cantidad, de $5{,}5$ a $6{,}1\ \mathrm{dB}$.

#### c) Elección entre amplificadores de 3, 6 y 9 dB

Como el inciso no aclara si la elección corresponde a las distancias originales o a las modificadas, comparo ambos casos:

| Ganancia disponible | Caso a: mínimo 5,5 dB | Caso b: mínimo 6,1 dB |
|---|---|---|
| 3 dB | No alcanza | No alcanza |
| 6 dB | Alcanza | No alcanza |
| 9 dB | Alcanza | Alcanza |

**Para el caso b elegiría 9 dB**, porque es la menor ganancia disponible que alcanza el valor requerido. Para el caso a bastan 6 dB. Si debo elegir un único modelo que sirva para ambos, elegiría **9 dB**, con sensibilidad de $-4\ \mathrm{dBm}$ o menor.

Con 9 dB en el caso b, la potencia recibida es:

$$
P_{Rx}=-3\ \mathrm{dBm}-0{,}6\ \mathrm{dB}+9\ \mathrm{dB}-2{,}5\ \mathrm{dB}
=\boxed{2{,}9\ \mathrm{dBm}}
$$

$$
P=1\ \mathrm{mW}\cdot10^{2{,}9/10}
\approx\boxed{1{,}95\ \mathrm{mW}}
$$

El margen sobre la sensibilidad es:

$$
M=P_{Rx}-S_{Rx}=2{,}9\ \mathrm{dBm}-0\ \mathrm{dBm}
=\boxed{2{,}9\ \mathrm{dB}}
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $M$ | Margen de potencia sobre la sensibilidad del receptor | dB |
| $P_{Rx}$ | Nivel de potencia recibida | dBm |
| $S_{Rx}$ | Umbral del receptor | dBm |

Este margen permitiría absorber hasta $2{,}9\ \mathrm{dB}$ de pérdidas adicionales en el balance completo antes de alcanzar el umbral del receptor, **siempre que también se mantenga una entrada suficiente en el amplificador**. No garantiza por sí solo que esas pérdidas adicionales puedan ubicarse antes del amplificador.

No elijo 6 dB para el caso b porque:

$$
P_{Rx}=-3\ \mathrm{dBm}-0{,}6\ \mathrm{dB}+6\ \mathrm{dB}-2{,}5\ \mathrm{dB}
=-0{,}1\ \mathrm{dBm}
$$

$$
P=1\ \mathrm{mW}\cdot10^{-0{,}1/10}
\approx0{,}977\ \mathrm{mW}<1\ \mathrm{mW}
$$

Aunque falten solamente $0{,}1\ \mathrm{dB}$, no se cumple el requisito. No corresponde redondear $6{,}1$ a $6\ \mathrm{dB}$ para elegir el equipo.

En el caso a, con 6 dB llegan $0{,}5\ \mathrm{dBm}$ y queda un margen de $0{,}5\ \mathrm{dB}$. Si uso 9 dB en ese mismo caso, llegan $3{,}5\ \mathrm{dBm}$ y queda un margen de $3{,}5\ \mathrm{dB}$.

**Consecuencia y límite del cálculo:** una mayor ganancia aumenta la potencia recibida y el margen. No puede afirmarse que el receptor se sature solo por superar su sensibilidad: esta es su umbral mínimo, no su límite máximo. Como consideración técnica general, para comprobar el funcionamiento real también se deben verificar la potencia máxima de salida del amplificador y la máxima admisible del receptor; el enunciado no proporciona esos datos.

### Cierre para estudiar — no es necesario transcribirlo en la entrega

#### Resultados y verificación de razonabilidad

| Resultado | Caso a | Caso b |
|---|---|---|
| Pérdida antes del amplificador | 1 dB | 0,6 dB |
| Pérdida después del amplificador | 1,5 dB | 2,5 dB |
| Potencia de entrada al amplificador | −4 dBm | −3,6 dBm |
| Sensibilidad requerida | $S_A\leq-4\ \mathrm{dBm}$ | $S_A\leq-3{,}6\ \mathrm{dBm}$ |
| Ganancia mínima | 5,5 dB | 6,1 dB |
| Menor ganancia disponible que sirve | 6 dB | 9 dB |

Las unidades cierran: dB/km por km da dB, y la diferencia entre dos niveles en dBm da dB. En ambos casos el transmisor parte 3 dB por debajo del umbral del receptor; por eso la ganancia debe compensar las pérdidas totales **más esos 3 dB**. Con la ganancia mínima se llega exactamente a 1 mW, sin margen.

#### Errores típicos

- **Contar solo dos conectores:** hay cuatro en el esquema; se pierden 0,5 dB en conectores por tramo.
- **Confundir dB con dBm:** 0 dBm equivale a 1 mW; 0 dB indica una relación de potencias igual a uno.
- **Confundir sensibilidad con potencia recibida:** la primera es un umbral del equipo; la segunda resulta del enlace. Se igualan únicamente para determinar el caso límite.
- **Interpretar “más sensible” como un número mayor:** un umbral de −5 dBm admite señales más débiles que uno de −4 dBm.
- **Redondear hacia abajo la ganancia mínima:** 6 dB no satisface un requisito de 6,1 dB.
- **Llamar saturación a superar la sensibilidad:** falta conocer el límite máximo del receptor para afirmarlo.
- **Confundir margen global con margen de entrada:** una ganancia mayor no corrige una señal que ya llega por debajo del umbral admisible del amplificador.

#### Resumen mental

> Primero calculo la pérdida de cada tramo contando fibra y conectores. Con el primer tramo determino qué señal debe admitir el amplificador; con el enlace completo determino cuánto debe amplificar. Elijo una ganancia disponible que no quede por debajo de la calculada y verifico tanto la entrada del amplificador como la potencia final en el receptor.

#### Checklist de examen y entrega

- [ ] Puedo explicar por qué hay cuatro conectores y dos pérdidas por tramo.
- [ ] Distingo sensibilidad, potencia recibida y ganancia, con sus unidades.
- [ ] Puedo justificar por qué el caso b recibe más potencia en el amplificador pero necesita mayor ganancia.
- [ ] Puedo demostrar por qué 6 dB no alcanza en el caso b.
- [ ] Para entregar: resolución manuscrita y prolija, en orden a), b), c), con nombre y apellido arriba a la derecha de cada hoja.
- [ ] Escanear solamente la resolución en un único PDF identificado con nombre y apellido.
