# Repaso U2 — Preguntas registradas de señales

**Alcance parcial:** instrumentos, códigos y filtros; dificultad conceptual básica/media, modalidad
oral o elección, sin tiempo/puntaje de simulacro. No se agregan preguntas nuevas. Las cuatro vienen
 de [Cuestionario U1/U2](../../capturas/teoria/Cuestionarios/cuestionario%20U1%20y%20U2.md), Q4–7.
B6ZS, rankings BER/PSD sin supuestos y temas sin registro quedan excluidos.

## Evidencia por pregunta

| ID | Original | Sección canónica | Contraste |
|---|---|---|---|
|U2-S04|Q4: analizador de espectro|[Fourier](../teoria/02-senales-telecomunicaciones/APUNTE.md#fourier)|U2 p. 20 instrumentos|
|U2-S05|Q5: mayor banda y autorreloj|[Códigos](../teoria/02-senales-telecomunicaciones/APUNTE.md#codigos)|cuadro p 1; U2 pp. 32–34|
|U2-S06|Q6: inductivo, baja continua y banda|[HDB3](../teoria/02-senales-telecomunicaciones/APUNTE.md#hdb3)|U2 p. 39; Banda Base pp.10–11,26|
|U2-S07|Q7: respuesta canal|[Filtros](../teoria/02-senales-telecomunicaciones/APUNTE.md#filtros)|U2 p. 48; libro PDF 134/157|

Fuentes: [U2](../../material/teoria/U2/U%202%20Características%20de%20las%20señales%20de%20telecom.pdf),
[cuadro](../../material/practica/U%202/UT%202%20Códigos%20de%20línea%20cuadro%20comparativo.pdf),
[Banda Base](../../material/teoria/U2/Señales%20Banda%20Base.pdf).

## Preguntas y respuestas

> **U2-S04 — Enunciado (transcripción literal; captura, Pregunta 4):**
>
> **Las variaciones en el tiempo de una señal de comunicaciones pueden ser apreciadas en forma directa mediante un analizador de espectro.**
>
> - Verdadero
> - Falso

**Datos / condiciones:** no hay datos numéricos; es una afirmación conceptual para marcar verdadero o falso.

**S04: falso.** Osciloscopio representa amplitud-tiempo; analizador de espectro representa amplitud o
potencia-frecuencia. Decir sólo “falso” sin distinguir ejes no demuestra comprensión.

> **U2-S05 — Enunciado (transcripción literal; captura, Pregunta 5):**
>
> **¿Qué código de línea ocupa más ancho de banda y es autosincronizante?**
>
> a. Unipolar NRZ
>
> b. Ninguno de los anteriores
>
> c. Bipolar RZ
>
> d. Polar NRZ
>
> e. Polar RZ

**Datos / condiciones:** no hay datos numéricos; se elige entre las cinco alternativas de código de línea listadas. La comparación física que fundamenta la respuesta se explica aparte; la captura no agrega condiciones cuantitativas.

**S05: polar RZ.** **Supuesto de comparación (no está en el enunciado):** mismo intervalo de bit; frente a NRZ, el pulso RZ ocupa una fracción menor de cada intervalo y exige mayor ancho de banda. Pulso de signo positivo para 1 y negativo para 0 y retorno 0 dentro de toda celda:
transición por bit, incluso rachas. Pulso más corto que NRZ amplía espectro. Unipolar NRZ y polar NRZ
pierden referencias en rachas iguales; bipolar RZ no pulsa durante 0, así que no asegura reloj en ceros
largos. “Ninguno” no corresponde porque hay candidato que cumple ambos atributos.

La actividad también ayuda a reconocer una emisión durante una racha de ceros, sin confundir un
cero informativo con falta de señal. El retorno instantáneo a 0 de polar RZ no significa reposo;
se observa una ventana adecuada al código. Presencia y sincronismo son finalidades distintas:
[distinción y ejemplo](../teoria/02-senales-telecomunicaciones/APUNTE.md#presencia-senal).

> **U2-S06 — Enunciado (transcripción literal; captura, Pregunta 6):**
>
> **¿Qué código es más adecuado para un medio con etapas inductivas, sin continuidad óhmica, requiriendo mínima componente continua y menor ancho de banda?**
>
> a. Polar RZ
>
> b. Ninguno de los anteriores
>
> c. Unipolar NRZ
>
> d. Bipolar RZ
>
> e. HDB3

**Datos / condiciones:** no hay datos numéricos; las premisas conceptuales son etapas inductivas, ausencia de continuidad óhmica, mínima componente continua y menor ancho de banda.

**S06: HDB3.** Alterna marcas y sustituye cuatro ceros manteniendo reloj; balance de signos reduce
continua incompatible con acoplamiento inductivo. Polar RZ tiene reloj pero pulso corto más exigente;
bipolar RZ no resuelve ceros largos; unipolar NRZ tiene continua y ceros sin transiciones. Se responde
entre las opciones del material, no que HDB3 sea óptimo para cualquier medio/tasa.

> **U2-S07 — Enunciado (transcripción literal; captura, Pregunta 7):**
>
> **¿Qué filtro se adapta mejor a la respuesta en frecuencia de un canal de comunicaciones?**
>
> 1. Pasa bajo
> 2. Pasa alto
> 3. Pasa banda
> 4. Rechazo de banda

**Datos / condiciones:** no hay datos numéricos; la pregunta no da los cortes ni la forma de respuesta del canal. Para justificar «pasa banda» se explicita en la respuesta el supuesto de un canal con corte inferior no nulo y corte superior.

**S07: pasa banda en el contexto de dos cortes.** Deja intervalo intermedio; pasa bajos no elimina
 bajas frecuencias, pasa altos no impone corte superior, rechazo de banda elimina justamente el medio.
Si se responde que un canal de banda base puede modelarse pasa bajos, es una aclaración correcta:
no negar esa excepción por memorizar “todo canal pasa banda”.

## Rúbrica y control — 2026-10-11

Respuesta aceptable: elección correcta **más mecanismo físico**, supuestos y distinción de distractores.
Error invalidante: Hz=bit/s, polaridad=garantía de continua 0 para cualquier secuencia, RZ=retorno intermedio,
HDB3 sustituye tres ceros, filtro real=apagado exacto fuera de corte.
Preguntas/fuentes y respuestas contrastadas; S05/S07 acotadas para no generalizar. Revisión independiente
pendiente; es repaso parcial, no simulacro ni certificación de unidad revisada.

**Retest 2026-10-13:** se amplió sólo la razón de S05 con presencia frente a cero informativo y
enlace al canon; no cambiaron los cuatro enunciados, opciones ni claves. Dictámenes iniciales cerrados;
aceptación independiente de las correcciones pendiente. No se incorporan preguntas nuevas.

**Modo Tutor:** una pregunta por vez, esperar intento, corregir con evidencia. No editar archivos al tomar oral.
