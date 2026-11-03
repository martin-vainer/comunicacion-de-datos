# Revisión U05 — A/B

## Dictamen A

# Revisión académica independiente — U5 (A)

**Fecha:** 2026-10-13  
**Dictamen:** rigor matemático y transcripción de los ejercicios revisados, **conformes en el alcance inspeccionado**. No encontré errores académicos P1 demostrados en las fórmulas, derivaciones o resultados recalculados. La unidad **no** puede declararse revisada/final: quedan pendientes programáticos con fuente/evidencia por recuperar y confirmar.

## Alcance y evidencia efectivamente revisada

- `apuntes/teoria/05-teoria-informacion-codificacion/APUNTE.md` (517 líneas), `INDICE.md` (24), `apuntes/practica/tp-05-informacion-codificacion.md` (343) y `apuntes/repaso/u05-informacion-codificacion.md` (65), lectura integral; no se usaron autocontroles ni informes de otros agentes.
- Captura teórica `capturas/teoria/05-Teoría de la información y de la codificación/01_10_26_U5.md`, §§1–22, y `capturas/practica/practica_un5.md`, enunciados/resoluciones E1–14; cotejé el texto con los destinos. No contienen imágenes adjuntas. `capturas/practica/Clase 05.md` fue inspeccionada para determinar alcance: es del 08/09 y registra TP3/U3, no es fuente U5.
- Originales visuales: TP5 oficial PDF pp. 2–3 (14 enunciados, secuencia y literales); Castro Lechtaler/Fusario 2013, PDF pp. 203–212 (impresas 177–186), incluidas figura 3.24 y las erratas visibles del Ejemplo 3-12; Huffman 1952, escaneo completo pp. 1–4 (impresas 1098–1101); UIT-T S.1, pp. impresas 2–3 (tabla y orden de transmisión); UIT-R M.1677-1, pp. impresas 2–3 (tabla Morse y temporización); programa analítico, p. 4. Renderes de revisión guardados sólo en `tmp/reviews/u05-a/source-render/`.
- Fuentes primarias web de caracteres contrastadas: RFC 20 (representación ASCII de 7 bits, bit alto cero en byte, tabla/control), registro IANA para IBM437/alias PC-8 e IBM para variantes EBCDIC/CCSID 37. Estas corroboran las afirmaciones que sí están en el alcance; no amplían el programa.

## Cobertura y recálculo

Los 22 fragmentos de la captura teórica se encuentran mapeados en APUNTE §16. Cobertura agrupada: §§1–9 → información/unidades, entropía, tasa; §§10–12 → funciones y propiedades de códigos; §§13–22 → Huffman, Morse, ITA2, BCD, FIELDATA, ASCII/PC-8/EBCDIC, comparación y repaso. Los vacíos de temario aparecen declarados; no los completé desde bibliografía.

Los 14 ejercicios del TP5 fueron recalculados independientemente (logaritmos en base 2 y redondeo al final). Coinciden los resultados presentados, con estas salvedades/hipótesis bien declaradas en el desarrollo:

| E | Resultado comprobado | Observación de interpretación |
|---:|---|---|
|1|20 Shannon|Requiere independencia entre posiciones; el TP explicita la hipótesis.| 
|2|$I(0)=0,584963$, $I(1)=1,584963$ Shannon; $H=0,918296$ Shannon/símbolo|Frecuencias de muestra son estimadores, no probabilidades verdaderas demostradas.| 
|3|$H=1,485475$ Shannon/mensaje|Ponderación correcta.| 
|4|$p=1/128$, 7 Shannon/símbolo, 42 Shannon/6 símbolos|La suma requiere independencia; declarada.| 
|5|CABLE = 12 Shannon|Producto de probabilidades requiere independencia; declarada.| 
|6|540000 Shannon; 1000 palabras = 16609,640474 Shannon; razón 32,511240; equivalencia 32511,239532 palabras|Conclusión sólo bajo independencia/equiprobabilidad/sin compresión; redondeo entero suficiente 32512.| 
|7|$H(0,5)=1$ Shannon/símbolo; tabla/gráfica correctas|La consigna combina caso equiprobable con curva paramétrica; TP lo separa correctamente.| 
|8|Gráfico: 2457600 Shannon y 73,142857 s; texto: 16000 bit físicos y 0,476190 s bajo tasa física ideal; razón de longitudes 153,6|No se infiere información estadística del texto desde “8 bit”; queda explícito que la tasa física/página requiere confirmación docente.| 
|9|$H=0,918296$, duración media 0,266667 s/símbolo, tasa 3,443609 Shannon/s|Promedio temporal ponderado correcto; no se sustituyen los datos por temporización Morse.| 
|10|2187500 Shannon/imagen; 43750000 Shannon/s (43,75 Mbit/s)|Es demanda/cota mínima necesaria, no capacidad real calculable sin modelo de canal.| 
|11|1400000 Shannon; 105360,498482 palabras, es decir 105361 para alcanzar/superar|Equivalencia estadística, no descripción semántica.| 
|12|252 palabras; $log_2 252=7,977280$; exceso 2,022720 bit/palabra; eficiencia 79,772799%; ocupación 24,609375%|Definiciones de redundancia no fijadas por consigna; se distinguen correctamente y se rotula equiprobabilidad.| 
|13|UTN/Red, bytes CP437 convertidos a decimal/hex/binario|Valores del subconjunto ASCII básico coinciden; mayúsculas/minúsculas y bytes correctos.| 
|14|Longitud fija 7 bit; $H_{max}=6,491853$; eficiencia equiprobable 92,740759%; exceso 0,508147 bit/símbolo; ocupación 70,3125%|No hay probabilidades en el enunciado: se informa eficiencia máxima/equiprobable y se distingue ocupación.| 

Repaso: los diez IDs U05-Q01–Q10 corresponden exactamente al bloque final (§22) de la captura; las respuestas y límites son congruentes con el apunte. No revisé como contenido U5 el archivo `Clase 05.md` de U3.

## Hallazgos

### U05-A-001 — P2 cobertura/evidencia: faltan pendientes accionables para ítems programáticos sin desarrollo

- **Ancla:** `apuntes/teoria/05-teoria-informacion-codificacion/APUNTE.md:436–447` y `:476–484`.
- **Demostrado:** el programa analítico p. 4 enumera explícitamente código de intercambio de datos, código 4 de 8, VIR, recomendación T.51, juegos primario/suplementario y Teletex. La tabla §16 dice que código 4/8 sólo aparece como antecedente; los demás no tienen desarrollo específico. Sin embargo, §17 no registra esos ítems con sección afectada, evidencia faltante y próxima comprobación; la fila general de cobertura pendiente no da un paso verificable. El estado `en-progreso` es honesto, por lo que esto no es una falsa declaración de completitud.
- **Impacto:** quien retome el apunte puede no saber qué evidencia falta para cerrar cada requisito del programa; la trazabilidad no llega al nivel de pendiente accionable exigido por la metodología §6.1.
- **Acción / cierre:** agregar pendientes por tema con ancla/destino, documento o tabla original a recuperar y comprobación requerida (incluido código 4/8). Mantenerlos pendientes hasta obtener esa evidencia; no completar tablas ni introducir material de terceros sin registro autorizado.

## Límites, integridad y QA

- Sin clave docente de E2/E8/E10/E12/E14 no es posible decidir qué convención exacta espera la cátedra; los desarrollos marcan los supuestos y no inventan respuestas oficiales.
- La tabla Huffman parcial de la captura no permite reconstruir frecuencias/árbol ni verificar su eficiencia; sí se verificaron visualmente el escaneo de 1952, el algoritmo general y el ejemplo alternativo CABLE.
- No hay original local de la tabla Aiken/paridad, FIELDATA, versión CCSID de la tabla de clase, identificación normativa VIR/T.51/Teletex ni completo repertorio de código 4/8. Esto limita la certificación, no demuestra error de sus contenidos no desarrollados.
- Las 10 páginas Castro citadas se inspeccionaron visualmente; sus erratas de entropía se recalcularon. No detecté discrepancias en Morse/ITA2 ni en conversiones ASCII/IBM437/EBCDIC verificadas.
- Hash inicial del manifiesto `docs/consolidacion-u1-u6/snapshot-inicial.json`: **401/401 coincidencias SHA-256**, cero diferencias/faltantes. Se repetirá al cierre. No se modificaron archivos fuente/candidatos; sólo recursos propios del revisor en `tmp/reviews/u05-a/`.
- Fórmulas, derivaciones y los 14 cálculos revisados: conformes bajo supuestos declarados. No se ejecutó build/install ni se editó contenido académico.

## Dictamen

Rigor conceptual y numérico satisfactorio en lo efectivamente desarrollado, con incertidumbres docentes visibles y bien tratadas. Un hallazgo P2 de trazabilidad de pendientes programáticos; no encontré P0 ni P1 demostrados. U5 sigue **en-progreso** y no es revisada/final hasta resolver las fuentes pendientes y completar la cobertura que corresponda.


---

## Dictamen B

# Revisión pedagógica independiente U5-B — 2026-10-13

## Resumen ejecutivo (≤350 palabras)

Dictamen independiente de lectura integral para tres entregables: `apuntes/teoria/05-teoria-informacion-codificacion/APUNTE.md` (517 líneas), su `INDICE.md` (15 líneas), `apuntes/practica/tp-05-informacion-codificacion.md` (343 líneas; E1–E14) y `apuntes/repaso/u05-informacion-codificacion.md` (preguntas Q01–Q10). **No hay hallazgos P0 ni P1 demostrados.** Los cálculos revisados son consistentes; las unidades, hipótesis y distinciones de entropía, información/tasa, baudios, longitud física y eficiencia están tratadas con buen cuidado. Las catorce consignas coinciden con el TP oficial, y las diez preguntas preservan el bloque final de la captura, con límites y claves razonadas. El índice y los enlaces locales de los cuatro archivos se resolvieron: 88 enlaces locales, cero fallas.

Hallazgo pedagógico pendiente: el programa analítico incluye el repertorio de caracteres de ITA2, mientras el apunte sólo ofrece ejemplos y reconoce que no contiene la tabla completa. También quedan fuera de cobertura T.51, juegos primario/suplementario y Teletex; el apunte los declara explícitamente como pendientes/exclusiones, por lo que el estado `en-progreso` es honesto y no debe promoverse a `completo/revisado` sin resolver la cobertura.

Se verificaron visualmente el programa analítico PDF pp.1–7; TP5 oficial pp.2–3 (E1–E14); Castro/Fusario PDF pp.202–212 (impresas 176–186); y las cuatro páginas del escaneo Huffman (impresas 1098–1101). Se inspeccionó la captura teórica U5 §§1–22 y captura práctica E1–E14. Se corroboraron como recursos primarios oficiales ITU-T S.1, ITU-R M.1677-1, RFC 20, IANA, Microsoft e IBM; los PDF ITU externos fueron consultados como texto, no renderizados visualmente durante esta revisión. Las dos gráficas Mermaid se verificaron por fórmula/puntos, pero no se renderizaron.

## Cobertura y QA

- **Trazabilidad:** captura teórica §§1–22 mapeada en APUNTE §16; captura práctica y TP5 oficial E1–E14 cotejados. Repaso Q01–Q10 corresponde al bloque final de captura §22, sin preguntas ajenas ni simulacro presentado como oficial.
- **Secuencia:** información → unidades → entropía → tasa → codificación → propiedades → Huffman/Morse/ITA2 → códigos de caracteres; didácticamente coherente.
- **Práctica:** recuentos y resultados recalculados: E1–E14, incluyendo secuencia E2, CABLE, las dos comparaciones imagen/texto, duración media E9, límite E10, combinatoria E12, CP437 E13 y diseño fijo E14. No se detectaron errores matemáticos en la resolución. E8/E10/E12/E14 conservan las condiciones y ambigüedades sin convertirlas en una clave docente inventada.
- **Tablas/figuras:** tablas numéricas de entropía, ejemplos Huffman y valores CP437 comprobados; diagrama funcional de cadena y dos curvas Mermaid revisados en fuente. Figura de entropía original contrastada con Castro p.208 (impresa 182); fórmulas de sorpresa/unidades p.203, entropía y curva pp.207–209, tasa pp.210–211, conteo de elecciones p.212. El escaneo Huffman impreso pp.1098–1101 se miró íntegro; el caché textual limitado no se usó como autoridad.
- **Enlaces:** 88 enlaces locales en los cuatro candidatos, todos resolubles; anclas incluidas.
- **Integridad:** hash SHA-256 frente a `docs/consolidacion-u1-u6/snapshot-inicial.json`: 401/401 coincidían al inicio y 401/401 al cierre. No se modificó ningún candidato, fuente, captura ni caché. Recursos de revisión propios quedan bajo `tmp/reviews/u05-b/`.

## Hallazgos

### U05-B-001 — P2 académico/cobertura — repertorio ITA2 no desarrollado

- **Archivo/ancla/línea:** `apuntes/teoria/05-teoria-informacion-codificacion/APUNTE.md#ita2`, líneas 350–358; cobertura líneas 442–447.
- **Afirmación/evidencia:** el programa analítico original, PDF p.4, incluye “Código para el servicio télex: el Alfabeto Internacional N.º 2” y “Repertorio de caracteres del Alfabeto Internacional N.º 2”. El apunte sólo presenta cinco unidades, estado, dos valores de ejemplo y shifts; no incorpora el repertorio. La propia tabla de cobertura limita el tratamiento a “núcleo contrastado” y “no tabla histórica completa”.
- **Naturaleza:** faltante de cobertura demostrado (no error factual). El alcance está declarado; el estado `en-progreso` es correcto.
- **Impacto:** no alcanza para preparar el subtema del programa desde el canon ni para declarar U5 completo.
- **Acción/prueba de cierre:** integrar una tabla/repertorio ITA2 sustentado por S.1 o conservar un pendiente explícito por falta de fuente de clase; validar las 32 combinaciones, orden de bits/condiciones A-Z y cambios letras/cifras contra la fuente primaria antes de actualizar cobertura/estado.

### U05-B-002 — P3 editorial — errata visible en supuesto de E4

- **Archivo/ancla/línea:** `apuntes/practica/tp-05-informacion-codificacion.md#ejercicio-04`, línea 111.
- **Afirmación/evidencia:** “Supuesto adicional dec)” no forma una etiqueta inteligible; en contexto se refiere a independencia de símbolos para el inciso c), no d).
- **Naturaleza:** defecto editorial demostrado.
- **Impacto:** puede hacer que quien estudia no relacione la hipótesis de independencia con la información de la palabra de seis símbolos.
- **Acción/prueba de cierre:** corregir la referencia al inciso c) y verificar que la dependencia matemática quede explícita en el inciso correspondiente.

### U05-B-003 — P3 editorial — espaciado irregular alrededor de fórmulas/unidades

- **Archivo/ancla/línea:** TP5 E9–E13, líneas 213, 226, 228, 233, 255, 267, 276 y 301; ejemplo: “tasa$T$[Shannon/s]”, “312500píxeles/imagen” y “tresbytes =24 bit”.
- **Naturaleza:** defecto de edición demostrado.
- **Impacto:** empeora la lectura de consignas con magnitudes y unidades, precisamente donde la materia exige distinguirlas.
- **Acción/prueba de cierre:** normalizar espacios entre texto, delimitadores LaTeX, valores y unidades; revisar una representación Markdown final sin cambiar cifras ni contenido.

## Limitaciones del dictamen

- El PDF del libro se contrastó visualmente sólo en las páginas citadas del tramo aplicable (202–212), no en las 726 páginas completas.
- Los PDFs de ITU-T S.1 y ITU-R M.1677-1 referidos en el apunte se consultaron desde sus sitios oficiales en formato textual accesible; no se obtuvo un render visual verificable en esta sesión. Por ello no afirmo inspección visual propia de esas páginas.
- Las tablas no incluidas (Aiken, FIELDATA, CCSID de la captura) siguen correctamente pendientes; no se completaron mediante conocimiento general.
- No se evaluó U7/U8, ni se usaron fuentes bibliográficas para ampliar el programa.

## Veredicto

**U5 parcialmente sólida y utilizable para estudio, con estado `en-progreso`; no certificable como completa/revisada.** Aritmética y trazabilidad de las secciones/exercises revisados son sólidas; mantener la brecha de repertorio ITA2 y las exclusiones programáticas visibles. Corregir las dos cuestiones editoriales para reducir ruido de lectura.
