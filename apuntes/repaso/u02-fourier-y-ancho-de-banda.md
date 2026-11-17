# Repaso U2 — Fourier y ancho de banda

**Alcance parcial:** preguntas y mini ejercicios del piloto conservados, más preguntas que ya estaban
 en los pilotos y Q2 registrada en cuestionario U3. NO simulacro nuevo. Dificultad conceptual/aplicación;
modalidad oral/escrita, sin tiempo/puntaje. Datos de mini ejercicios son **hipotéticos heredados**,
no valores de normas. No se evalúan rankings PSD/BER, B6ZS ni difusión sin registro.

## Evidencia por ID

| IDs | Procedencia anterior | Canon y autoridad |
|---|---|---|
|F01–F02, F05, F09–F11|ficha conceptual 1,2,5 y piloto Fourier autoevaluación 1–3|[Fourier](../teoria/02-senales-telecomunicaciones/APUNTE.md#fourier), U2 pp. 15–24|
|F03–F04, F12–F14|ficha conceptual 3,4 y piloto AB autoevaluación 1–3|[AB](../teoria/02-senales-telecomunicaciones/APUNTE.md#ancho-banda), U2 pp. 7,22–24/libro PDF 112,134|
|F06–F08|mini ejercicios 1–3 de ficha (hipotéticos)|[Tren](../teoria/02-senales-telecomunicaciones/APUNTE.md#tren)/AB; resoluciones calculadas abajo|
|F15|[Cuestionario U3 Q2](../../capturas/teoria/03-redes-telecomunicaciones/cuestionario_U3.md), coincide con TP2 E10|[Tren](../teoria/02-senales-telecomunicaciones/APUNTE.md#tren), [TP2 E10](../practica/tp-02-senales.md#e9e12--tren-rectangular-y-espectro), U2 p. 24|

[Presentación U2](../../material/teoria/U2/U%202%20Características%20de%20las%20señales%20de%20telecom.pdf),
[Libro2013](../../material/teoria/DOC-20230425-WA0040.pdf).
Se conservaron preguntas coincidentes del piloto en IDs diferentes para evitar pérdida de trazabilidad.

## Preguntas y respuestas

**Bloqueo de procedencia F01–F14:** las fichas/pilotos a los que se atribuyen estos ítems no están localizados en `capturas/` ni en `material/`. Se conservan como preguntas heredadas, no verificables y **no presentadas como transcripción literal**. No se reconstruye ni se atribuye un enunciado de origen hasta localizar la fuente.

### Conceptuales heredadas de ficha

> **F01:** Explicá con tus palabras por qué una onda cuadrada necesita armónicas.

**Datos / condiciones:** No hay datos numéricos. Premisa pertinente: se pregunta por la representación de una onda cuadrada mediante armónicas.

**Respuesta F01:** Una senoidal sola es suave; las componentes altas permiten cambios rápidos. Al
  atenuarlas, bordes se redondean; forma temporal cambia aunque fundamental siga presente.

> **F02:** ¿Qué determina separación entre líneas? ¿Qué determina ceros de envolvente?

**Datos / condiciones:** No hay datos numéricos. Premisas pertinentes: se consideran la separación entre líneas espectrales y los ceros de la envolvente.

**Respuesta F02:** Separación 1/T=FRP; ceros dependen de τ, primer positivo 1/τ. Cambiar T sin τ no mueve ese cero.

> **F03:** Compará AB de señal y AB de canal.

**Datos / condiciones:** No hay datos numéricos. Premisa pertinente: comparar ancho de banda de señal y ancho de banda de canal.

**Respuesta F03:** Señal: intervalo relevante de componentes, bajo criterio. Canal: intervalo de respuesta
  utilizable, bajo tolerancia. Compararlos anticipa pérdida/deformación, no identifica ambos objetos.

> **F04:** ¿Por qué no alcanza decir B=fH−fL?

**Datos / condiciones:** No hay datos numéricos. Premisa pertinente: interpretar la expresión de intervalo entre frecuencias límite sin otro criterio especificado.

**Respuesta F04:** Resta sólo mide intervalo, no elige extremos. Hay que decir señal/canal y primer cero,
 3 dB u otro criterio. Cuadrada ideal tiene espectro infinito.

> **F05:** ¿Qué pierde señal digital cuando canal atenúa armónicas altas?

**Datos / condiciones:** No hay datos numéricos. Premisa pertinente: una señal digital atraviesa un canal que atenúa sus armónicas altas.

**Respuesta F05:** Pierde detalle temporal en flancos; pulsos pueden solaparse dificultando decisión.

### Mini ejercicios heredados — datos hipotéticos

> **F06:** T=2 ms: calculá f0 y primeras cinco armónicas (primeros cinco órdenes, incluso si una señal
>   específica tuviera algunos coeficientes 0).

**Datos / condiciones:** Valor hipotético heredado, no verificado como original: $T=2\ ms$. Se solicita hallar $f_0$ y los primeros cinco órdenes armónicos.

**Respuesta F06:** Convertí 2 ms=0,002 s; f0=1/0,002=500 Hz. Órdenes 1–5: 500,1000,1500,2000,2500 Hz.
  Frecuencia armónica=$nf_0$. Unidad resulta 1/s=Hz; un orden no necesariamente tiene amplitud no nula.

> **F07:** Canal con cortes 200 Hz y 3,6 kHz: calculá AB con unidad.

**Datos / condiciones:** Valores hipotéticos heredados, no verificados como originales: límites del canal de 200 Hz y 3,6 kHz. Se solicita calcular la diferencia entre ellos con unidad.

**Respuesta F07:** 3,6 kHz=3600 Hz; B=3600−200=3400 Hz=3,4 kHz. Ambos límites en la misma unidad.

> **F08:** Tren rectangular τ=0,25 ms/FRP = 200 Hz: primer cero, índice del cero y armónicas positivas no nulas
>   antes. No contar continua ni cero.

**Datos / condiciones:** Valores hipotéticos heredados, no verificados como originales: tren rectangular con $\tau=0{,}25\ ms$ y $FRP=200\ Hz$. Se solicitan el primer cero, su índice y los órdenes positivos no nulos anteriores.

**Respuesta F08:** τ=0,00025 s; T=1/200=0,005 s; B=4000 Hz; n0=B/200=20. Órdenes 1–19 no nulos antes del cero;
  orden 20 es cero. Criterio explícito, pulso rectangular; no ancho ideal infinito ni ancho bilateral 8000 Hz.

### Autoevaluaciones de pilotos, preservadas

> **F09:** ¿Por qué cuadrada pierde flancos si canal elimina armónicas altas?

**Datos / condiciones:** No hay datos numéricos. Premisa pertinente: el canal elimina armónicas altas de una onda cuadrada.

**Respuesta F09:** Una senoidal sola es suave; las componentes altas permiten cambios rápidos. Al
  atenuarlas, bordes se redondean; forma temporal cambia aunque fundamental siga presente.

> **F10:** ¿Qué cambia al duplicar T sin cambiar τ? Conservá amplitud A.

**Datos / condiciones:** No hay valores numéricos especificados. Condiciones: duplicar $T$, mantener $\tau$ y conservar la amplitud $A$.

**Respuesta F10:** Separación mitad; primer cero igual; ciclo τ/T a la mitad y $C_0$=Aτ/T a la mitad. El muestreo de envolvente
  ahora tiene líneas más juntas. Cambia amplitud normalizada porque la señal está activa menos fracción.

> **F11:** ¿Qué coeficientes se anulan para cuadrada impar y por qué?

**Datos / condiciones:** No hay datos numéricos. Premisa pertinente: se considera una onda cuadrada impar.

**Respuesta F11:** $a_0=a_n=0$ por imparidad; bn pares 0 por cancelación de integral, bn impares 4 A/(nπ).

> **F12:** ¿Por qué “ocupa 2000 Hz” queda incompleto sin criterio?

**Datos / condiciones:** No hay datos de un caso numérico. “2000 Hz” aparece como una afirmación de ancho de banda cuya suficiencia se debe evaluar, no como dato para un cálculo.

**Respuesta F12:** Resta sólo mide intervalo, no elige extremos. Hay que decir señal/canal y primer cero,
 3 dB u otro criterio. Cuadrada ideal tiene espectro infinito.

> **F13:** ¿Qué pasa con primer cero si τ se reduce a mitad?

**Datos / condiciones:** No hay valores numéricos especificados. Condición: reducir $\tau$ a la mitad.

**Respuesta F13:** Primer cero se duplica. Acortar τ ensancha envolvente; no usar esta ley para cualquier pulso/filtro.

> **F14:** ¿Por qué −3 dB no significa inexistencia de señal después del corte?

**Datos / condiciones:** No hay datos de un caso numérico. $-3\ dB$ es el criterio de corte mencionado para interpretar, no un conjunto de datos de ejercicio.

**Respuesta F14:** 3 dB es límite de tolerancia, potencia ≈0,501 de la referencia, no corte abrupto de existencia.

### Pregunta registrada del cuestionario U3

> **F15 — Enunciado (transcripción literal; captura U3, Pregunta 2):**
>
> Dados los siguientes datos de un tren de pulsos:
>
> - FRP = 100 pps
> - Velocidad de modulación = 2000 baudios
> - Amplitud del pulso $A = 1\ V$
>
> Se solicita:
>
> a. Realizar el gráfico de amplitud del espectro de Fourier.
>
> b. Calcular el ancho de banda y la cantidad de armónicas.
>
> c. Calcular el valor de la amplitud máxima de $C_n$.

**Datos:** FRP = 100 pps; velocidad de modulación = 2000 baudios; amplitud del pulso A = 1 V.

**Aclaración pedagógica (no parte del enunciado):** para desarrollar se adopta tren rectangular centrado y $\tau=1/V_m$, tal como se interpreta en el TP2 asociado. El ancho de banda se informa hasta el primer cero unilateral; se aclara aparte la diferencia entre orden del primer cero y armónicas positivas no nulas.

**Respuesta F15:** T = 10 ms, τ = 0,5 ms, D = 0,05. Líneas separadas 100 Hz; primer cero 2000 Hz, n = 20 con coeficiente 0;
 19 armónicas positivas no nulas antes y continua 0,05 V. Máximo |Cn| incluyendo 0=0,05 V; excluyendo 0,
 |C±1|≈0,049795 V. Desarrollo/gráfico en TP2 E10; no dar “20 no nulas”.

## Rúbrica y QA — 2026-10-11

Conceptuales: mecanismo de componentes, tolerancia y separación señal/canal. Numéricos: conversión,
fórmula con supuestos, resultado, unidad y conteo correcto. No basta una palabra o número suelto.
Cuentas F06–F08 y F15 recalculadas; enlaces y evidencia local comprobados al entregar. Estados pendientes
 del APUNTE no se usan como conocimiento confirmado. Revisión independiente pendiente.

## Control oral

> Tomame Fourier y ancho de banda desde el APUNTE U2, usando estos IDs. Una pregunta por vez,
> esperá mi respuesta, corregí explicando el porqué y no modifiques archivos.
