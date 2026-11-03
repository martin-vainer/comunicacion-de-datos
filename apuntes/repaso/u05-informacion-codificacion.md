# U5 — Diez preguntas finales registradas

**Origen único de las preguntas:** [captura teórica del 01/10/2026](../../capturas/teoria/05-Teoría%20de%20la%20información%20y%20de%20la%20codificación/01_10_26_U5.md), **§22 «Resumen para estudiar», último bloque «Preguntas de autoevaluación»**, preguntas 1–10. No provienen de la captura práctica; no son un simulacro nuevo.

**Alcance:** repaso parcial de codificación conceptual, dificultad introductoria/intermedia; sin tiempo ni puntaje oficial. No se evalúan repertorio FIELDATA, tabla Aiken ausente, CCSID de clase, árbol incompleto de Huffman ni la identidad normativa universal AI5/ASCII. La pregunta Q07 usa el término original «escape», aclarado en la respuesta como **cambio de posición**.

En tutoría: una pregunta por vez, intento del estudiante, corrección del razonamiento. Primero respondé sin mirar el bloque de respuestas.

## Evidencia por pregunta

| ID | Origen exacto | Sección canónica | Respaldo / límite |
|---|---|---|---|
|U05-Q01|Captura §22, línea 917|[Fuente/canal](../teoria/05-teoria-informacion-codificacion/APUNTE.md#codificacion)|Huffman 1952, p. 1098–1099; protección en U6|
|U05-Q02|Captura §22, línea 918|[Con/sin pérdida](../teoria/05-teoria-informacion-codificacion/APUNTE.md#codificacion)|Distinción del registro; ejemplos no universalizan perfiles|
|U05-Q03|Captura §22, línea 919|[Bloques](../teoria/05-teoria-informacion-codificacion/APUNTE.md#propiedades)|Modelo binario inyectivo y ejemplo explícito|
|U05-Q04|Captura §22, línea 920|[Redundancias](../teoria/05-teoria-informacion-codificacion/APUNTE.md#propiedades)|Definiciones separadas;TP5 E12/14|
|U05-Q05|Captura §22, línea 921|[Distancia](../teoria/05-teoria-informacion-codificacion/APUNTE.md#propiedades)|Sustituciones alineadas; desarrollo U6|
|U05-Q06|Captura §22, línea 922|[Huffman](../teoria/05-teoria-informacion-codificacion/APUNTE.md#huffman)|Huffman 1952, PDF 1–2, p 1098–1099, inspección visual|
|U05-Q07|Captura §22, línea 923|[ITA2](../teoria/05-teoria-informacion-codificacion/APUNTE.md#ita2)|S.1 PDF 6–7,§4.4 y Cuadro 1; término original no redefine ASCII ESC|
|U05-Q08|Captura §22, línea 924|[BCD](../teoria/05-teoria-informacion-codificacion/APUNTE.md#bcd)|Construcción 8421 y conteo; no requiere tabla Aiken pendiente|
|U05-Q09|Captura §22, línea 925|[ASCII](../teoria/05-teoria-informacion-codificacion/APUNTE.md#ascii),[PC-8](../teoria/05-teoria-informacion-codificacion/APUNTE.md#pc8)|RFC 20§§2–4;IANA IBM 437 y Microsoft Code Pages|
|U05-Q10|Captura §22, línea 926|[EBCDIC](../teoria/05-teoria-informacion-codificacion/APUNTE.md#ebcdic)|IBM CCSID 37 comparado con RFC 20, no tabla universal|

## Preguntas

1. **U05-Q01.** ¿Cuál es la diferencia entre un código de fuente y un código de canal?
   **Datos / condiciones:** pregunta conceptual; no se proporcionan valores numéricos. Identificar y comparar las funciones de ambos códigos.
2. **U05-Q02.** ¿En qué se diferencian la compresión sin pérdida y la compresión con pérdida?
   **Datos / condiciones:** pregunta conceptual; no se proporcionan valores numéricos. Comparar ambos tipos de compresión según la reconstrucción del original.
3. **U05-Q03.** ¿Qué representan `k` y `n` en un código de bloque?
   **Datos / condiciones:** pregunta conceptual; no se dan valores de `k` o `n`. Interpretar ambas variables en el contexto de un código de bloque.
4. **U05-Q04.** ¿Cómo se calcula la redundancia de un código?
   **Datos / condiciones:** pregunta conceptual; no se especifican un código ni una convención de redundancia. La definición depende del modelo que se declare en la respuesta.
5. **U05-Q05.** ¿Qué información brinda la distancia mínima de Hamming?
   **Datos / condiciones:** pregunta conceptual; no se dan palabras de código ni una distancia numérica. Considerar el modelo de sustituciones alineadas.
6. **U05-Q06.** ¿Por qué Huffman asigna códigos más cortos a los símbolos frecuentes?
   **Datos / condiciones:** pregunta conceptual; no se dan probabilidades ni un árbol concreto. Explicar el efecto de las frecuencias sobre la longitud media.
7. **U05-Q07.** ¿Por qué Baudot necesita caracteres de escape?
   **Datos / condiciones:** pregunta conceptual sobre el repertorio de Baudot; no se proporcionan valores numéricos adicionales ni una secuencia concreta.
8. **U05-Q08.** ¿Qué combinaciones de BCD natural no representan dígitos decimales válidos?
   **Datos / condiciones:** pregunta conceptual sobre BCD natural; no se da una palabra binaria concreta. Considerar la representación de un dígito decimal en BCD.
9. **U05-Q09.** ¿Qué diferencia hay entre ASCII de 7 bits y PC-8 de 8 bits?
   **Datos / condiciones:** se comparan los formatos nombrados en la pregunta; no se dan valores de caracteres ni una página de códigos adicional.
10. **U05-Q10.** ¿Por qué ASCII y EBCDIC no deben intercambiarse sin una conversión de codificación?
    **Datos / condiciones:** pregunta conceptual; no se proporciona una cadena de bytes concreta ni una página CCSID para conversión.

---

## Respuestas razonadas y criterio de corrección

**Q01.** Fuente busca una representación compacta; canal agrega estructura redundante para controlar alteraciones. No se contradicen: puede comprimirse y después protegerse. **Respuesta suficiente:** objetivo de ambas funciones y diferencia de redundancia. **Error invalidante:** afirmar que Huffman es corrector de errores o que ASCII protege por tener una tabla de caracteres.

**Q02.** Sin pérdida recupera exactamente los datos originales; con pérdida permite diferencias para ahorrar representación según criterio de uso. No es lo mismo que un error del canal: el descarte es parte del diseño. **Suficiente:** exactitud de reconstrucción y razón del descarte. **Error:** llamar «sin pérdida» a una diferencia imperceptible pero no nula.

**Q03.** En un bloque binario$k$ cuenta bits de entrada y$n$ los de la palabra codificada de salida. Por ejemplo 0/1→000/111 tiene$k=1$ y$n=3$. **Suficiente:** definir ambos y no intercambiarlos. **Error:** $n$=cantidad de palabras válidas; esa cantidad es$M$, no$n$.

**Q04.** Depende de la definición. En un bloque de$k$bit a$n$bit, redundancia absoluta$n-k$bit/palabra; relativa$(n-k)/n$. En representación de fuente, el exceso medio es longitud media menos entropía, con equivalencia informativa en base 2. **Suficiente:** declarar modelo y unidad antes de calcular. **Error:** contar palabras inválidas y llamar a ese número «bits de redundancia», o usar un$k$fraccionario como tamaño de bloque binario de entrada. Fórmulas, símbolos, supuestos y ejemplo completo en [§6](../teoria/05-teoria-informacion-codificacion/APUNTE.md#propiedades).

**Q05.** Es la menor cantidad de posiciones diferentes entre dos palabras válidas. Cuanto mayor sea, más sustituciones puede tolerar el código sin confundirlas. En el modelo alineado y con decodificador adecuado, distancia 3 permite detector de hasta 2 errores o corrector de 1. **Suficiente:** explicar separación entre palabras y garantía, no sólo repetir «cuenta bits». **Error:** distancia entre un solo par=distancia mínima de todo el código, o garantía para inserciones/borrados no modelados.

**Q06.** La longitud media pondera cada longitud por su probabilidad; acortar los más frecuentes reduce más ese promedio. Huffman une los dos pesos menores y construye un árbol prefijo para recuperar exactamente los símbolos sin separadores adicionales. **Suficiente:** frecuencia→promedio y decodificación prefijo. **Error:** códigos universales por letra sin conocer frecuencias; ahorro garantizado incluyendo cualquier overhead.

**Q07.** En el ITA2 estudiado, cinco unidades permiten 32 combinaciones físicas, insuficientes para representar simultáneamente todo el repertorio de letras, cifras y controles en una sola posición. Los comandos de cambio a letras/cifras permiten reinterpretar una combinación según estado. «Escape» es el término de la pregunta, no un ASCII ESC insertado en ITA2. **Suficiente:** explicar 32 combinaciones y cambio de interpretación. **Error:** cinco bits representan 64 palabras físicas o retorno de carro borra la letra.

**Q08.** En BCD 8421 las palabras 1010,1011,1100,1101,1110 y 1111 no se asignan a dígitos 0–9. Su existencia no detecta toda alteración:0000→0001 sigue siendo válida. **Suficiente:** rango inválido y diferenciar patrón de dígito. **Error:** interpretar 1010 como decimal 10 válido en un único dígito BCD o asegurar corrección inherente.

**Q09.** ASCII básico usa 7 bit y 128 posiciones; PC-8 en la captura es IBM437, de 8 bit y 256 posiciones posibles. Comparte los valores básicos pero añade repertorio según página. ASCII de 7 bits más paridad no es PC-8: el octavo bit allí es protección, no selección de caracteres. **Suficiente:** tamaño, versión y función del octavo bit. **Error:** «ASCII extendido» es universal o 256 posiciones significan 256 imprimibles.

**Q10.** Los valores asignados al mismo carácter difieren: A es hex 41 en ASCII y hex C1 en EBCDIC CCSID 37. Convertir preserva el carácter y cambia sus bytes; reinterpretar los mismos bytes como otra tabla no. **Suficiente:** explicar asignación y reconocer página/CCSID. **Error:** igual longitud de almacenamiento implica compatibilidad; EBCDIC tiene un único repertorio universal.

## Control y límites

**2026-10-11:** cotejadas las diez preguntas del bloque FINAL de la captura teórica, evidencia y límites registrados; respuestas derivadas del apunte contrastado parcialmente. Los siete controles de información del primer bloque§9 no se convierten en nuevas preguntas de este archivo: su contenido se integra en las secciones 1–4 del canon. No se mezclan cuestionarios nuevos con el corpus autorizado.

Enlaces y anclas locales comprobados por el autor. Falta revisión independiente/transversal; no es evaluación integral de la unidad ni certificación de los temas pendientes.
