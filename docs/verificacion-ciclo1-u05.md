# Revalidación U05 — ciclo 1


---

<!-- Evidencia original preservada: tmp/reviews/cierres-u05-ciclo1.md -->

# U5 — Cierres del autor, ciclo 1

**Fecha:** 2026-10-13. **Estado:** cuatro correcciones implementadas y retesteadas por el autor; **pendientes de revalidación independiente**. U5/TP5 continúan `en-progreso`. Este registro no edita ni sustituye los dictámenes iniciales ni declara resuelta la cobertura programática faltante.

**Guía del ciclo:** [síntesis inicial](../../docs/consolidacion-u1-u6/sintesis-inicial.md), [revisión consolidada U5](../../docs/revision-u05.md), [A](u05-a.md) y [B](u05-b.md). Los cuatro IDs se conservan por separado.

## U05-A-001 — Pendientes programáticos accionables

- **Causa confirmada:** la lista anterior agrupaba carencias y no daba, para cada requisito, evidencia a recuperar y próximo chequeo. No era una afirmación de completitud.
- **Corrección:** [APUNTE §17](../../apuntes/teoria/05-teoria-informacion-codificacion/APUNTE.md#pendientes), líneas 525–543: 13 filas con ancla/destino, confirmado/documentado, evidencia faltante, próxima búsqueda/comprobación y criterio verificable de cierre. [§16](../../apuntes/teoria/05-teoria-informacion-codificacion/APUNTE.md#cobertura), líneas 478–522, enlaza separadamente los requisitos programáticos.
- **Requisitos individualizados:** código 4 de 8 (`#pendiente-codigo-4-de-8`), intercambio, AI5/VIR, T.51, juegos primario/suplementario/Teletex, Aiken/paridad, FIELDATA, CCSID, tabla particular Huffman, ambigüedades docentes TP5 y revalidación. No se rellenó ninguno de esos repertorios sin evidencia.
- **Evidencia y límite:** programa analítico PDF p.4, requisito identificado también por ambos dictámenes. Las rutas de búsqueda en `material/teoria/`/capturas son **rutas para recuperar evidencia, no documentos supuestamente disponibles**. La fuente/tabla que falta está nombrada por fila; fuentes nuevas requieren curaduría/cache antes de consolidación.
- **Retest:** 13 anclas únicas existentes, destinos comprobados, tabla Markdown de 13 filas/5 columnas renderizada e inspeccionada sin desborde horizontal. 112 enlaces locales del corpus U5, cero fallas. Evidencia: [qa.json](../autor-u05-ciclo1/qa.json), [render-qa.json](../autor-u05-ciclo1/render-qa.json), [representación de §17](../autor-u05-ciclo1/pendientes.png).
- **Resultado del autor:** defecto de trazabilidad corregido. Los requisitos académicos todavía carentes de fuente siguen pendientes; no se certifica su cobertura.

## U05-B-001 — Repertorio ITA2 completo y límites normativos

- **Causa confirmada:** el canon sólo describía cinco unidades, valores de ejemplo y shifts; el programa exige además repertorio.
- **Corrección:** [APUNTE §9 / repertorio](../../apuntes/teoria/05-teoria-informacion-codificacion/APUNTE.md#ita2-repertorio), líneas 347–406, incluye las **32 combinaciones**, letras A–Z, diez cifras, símbolos y controles, A/Z y binario en orden de elementos 1→5. El elemento 1 se transmite primero; identificador de fila no es valor decimal. [Cobertura](../../apuntes/teoria/05-teoria-informacion-codificacion/APUNTE.md#cobertura) y [INDICE](../../apuntes/teoria/05-teoria-informacion-codificacion/INDICE.md), línea 9, enlazan el desarrollo.
- **Fuente:** [UIT-T S.1 (03/1993), ficha oficial](https://www.itu.int/rec/T-REC-S.1-199303-I/en), [PDF español previamente curado](../curador-ejecucion/externos/itu-t-s1-1993-es-ita2.pdf), **PDF pp.5–8 / impresas 1–4**, §§2–4 y Cuadro 1/S.1 (PDF p.7). [Cache previo](../../material/_cache/u5-contraste-itu-t-s1-1993-ita2-es.txt) auxiliar; la tabla y reglas se cotejaron contra el PDF visual, no sólo su texto extraído. No se atribuye esta tabla a una lámina de clase ausente.
- **Límites explicitados:** cifras de combinaciones 6–8 de uso nacional/privado, sin asignación internacional universal y sólo por acuerdo expreso entre administraciones; WRU = cambio a cifras (30) + combinación 4; 4/10 pueden producir símbolos de control impresos; 32 no se utiliza en fase de comunicación del télex internacional, con usos nacionales/bilaterales delimitados en §4.7. No se universaliza tipografía o caja; retorno del carro no borra caracteres. No se añaden bits de framing al conteo.
- **Retest:** 32/32 filas cotejadas visualmente con Cuadro 1; script verifica patrones A/Z, traducción A→0/Z→1, 32 binarios únicos que cubren todo el espacio de cinco posiciones, A–Z, diez cifras y controles. Shifts 29/30 correctos. Ejemplo en estado inicial letras: `10000 11011 10000 11111 10000` → **E3E**, 25 unidades sin arranque/parada. Tabla renderizada: 32 filas y cinco columnas; sin desborde.
- **Evidencia:** [render original de tabla en alta resolución](../autor-u05-ciclo1/s1-table-high-7.png), páginas originales [5](../autor-u05-ciclo1/s1-5.png), [6](../autor-u05-ciclo1/s1-6.png), [8](../autor-u05-ciclo1/s1-8.png); [tabla Markdown renderizada](../autor-u05-ciclo1/ita2.png) y [qa.json](../autor-u05-ciclo1/qa.json).
- **Resultado del autor:** repertorio registrado ahora desarrollado para **esa edición de S.1**; pendiente de revalidación. No equivale al cierre de AI5/VIR/T.51/Teletex ni de los demás vacíos.

## U05-B-002 — Inciso c) de E4

- **Causa confirmada:** «Supuesto adicional dec)» pegaba palabras y no identificaba correctamente el inciso.
- **Corrección:** [TP5 E4](../../apuntes/practica/tp-05-informacion-codificacion.md#ejercicio-04), línea 111: «**Supuesto adicional del inciso c):** las seis posiciones son independientes; así se puede sumar la información de sus símbolos para obtener la de la palabra».
- **Evidencia:** [TP5 oficial](../../material/practica/U%205/TP%20%205%20%202026.pdf), PDF p.2, y texto de incisos a–d del desarrollo; c) calcula palabra de seis símbolos, d) entropía por emisión.
- **Retest:** etiqueta anterior ausente; nueva referencia presente. $p=1/128$, información puntual 7 Shannon, palabra independiente $6\log_2 128=42$ Shannon; entropía 7 Shannon/símbolo, no 42. Recalculado en [qa.json](../autor-u05-ciclo1/qa.json), clave E4.
- **Resultado del autor:** errata corregida, sin cambio numérico; pendiente de revalidación.

## U05-B-003 — Spacing de E9–E13

- **Causa confirmada:** faltaban espacios entre texto/LaTeX, valores/unidades, palabras y literales de código.
- **Corrección:** [TP5 E9–E13](../../apuntes/practica/tp-05-informacion-codificacion.md#ejercicio-09), líneas 210–301: `tasa $T$ [Shannon/s]`, `312500 píxeles/imagen`, `$C\geq43,75$ Mbit/s`, `400 líneas × 500 puntos`, `redundancia $R$`, `tres bytes = 24 bit`, literales `UTN`/`Red` y otras separaciones equivalentes.
- **Retest de conservación:** [spacing.py](../autor-u05-ciclo1/spacing.py) guardó el fragmento [antes](../autor-u05-ciclo1/spacing-before.md); tres comparaciones pasan: tokens numéricos idénticos, fórmulas idénticas salvo whitespace y **todo el texto idéntico al quitar whitespace**. No se cambiaron cifras, hipótesis ni literales; 25 reemplazos dirigidos, no formateo global.
- **Representación final inspeccionada:** `marked` bundled + Chrome headless; [E9–E10](../autor-u05-ciclo1/e09-e10.png), [E11–E12](../autor-u05-ciclo1/e11-e12.png), [E13](../autor-u05-ciclo1/e13.png) vistas. Tabla CP437 de seis filas y bloques de UTN/Red legibles, sin desborde horizontal. **LaTeX protegido como literal:** este test editorial no certifica composición MathJax ni todos los lectores Markdown.
- **Evidencia:** [spacing-check.json](../autor-u05-ciclo1/spacing-check.json), [render-qa.json](../autor-u05-ciclo1/render-qa.json), [renderer](../autor-u05-ciclo1/render.cjs), recálculos E9–E13 en [qa.json](../autor-u05-ciclo1/qa.json).
- **Resultado del autor:** espacios corregidos, contenido preservado; pendiente de revalidación.

## Retest numérico E1–E14

Logaritmos base 2, precisión completa para operaciones y redondeo al final; resultados coinciden con el candidato. Se conservan las hipótesis y ambigüedades docentes existentes, no se inventa clave oficial.

| E | Resultado recalculado | Unidad / condición |
|---:|---|---|
| 1 | 20 | Shannon por palabra independiente de cuatro caracteres |
| 2 | I(0)=0,584963; I(1)=1,584963; H=0,918296; secuencia=11,019550 | Shannon puntuales / Shannon por símbolo; estimación desde 8 ceros y 4 unos |
| 3 | 1,485475 | Shannon/mensaje |
| 4 | p=0,0078125; I=7; palabra=42; H=7 | Probabilidad; Shannon; Shannon/símbolo |
| 5 | CABLE=12; H=2,25 | Shannon puntuales y Shannon/símbolo |
| 6 | Imagen=540000; mil palabras=16609,640474; razón=32,511240; equivalente=32511,239532 → 32512 enteras | Shannon y palabras, independencia/equiprobabilidad |
| 7 | H(0,5)=1; extremos 0; curva simétrica | Shannon/símbolo |
| 8 | Imagen=2457600; texto físico=16000; tiempos 73,142857 y 0,476190; razón=153,6 | Shannon / bit / s, tasas e independencia condicionadas |
| 9 | H=0,918296; duración media=0,266667; tasa=3,443609 | Shannon/símbolo; s/símbolo; Shannon/s |
| 10 | Imagen=2187500; tasa=43750000 | Shannon/imagen; Shannon/s; cota ideal de demanda, no capacidad real conocida |
| 11 | 105360,498482 → 105361 enteras | Palabras equivalentes |
| 12 | M=252; descartadas=772; H=7,977280; exceso=2,022720; eficiencia=79,772799%; ocupación=24,609375% | Conteos separados del exceso bit/palabra; equiprobabilidad explícita |
| 13 | UTN: 85/84/78, hex55/54/4E; Red: 82/101/100, hex52/65/64 | Bytes CP437, binarios de ocho posiciones y roundtrip comprobados |
| 14 | n=7; H máximo=6,491853; eficiencia=92,740759%; exceso=0,508147; ocupación=70,3125% | 90 palabras únicas de siete bits; máxima eficiencia equiprobable, no entropía real sin probabilidades |

## Integridad, controles y entrega congelada

- [Verificador reproducible](../autor-u05-ciclo1/verificar.py), Python bundled sin build/install: E1–E14, tablas/códigos/estados, links y YAML. **112 enlaces/anclas locales**, cero errores; tablas sin columnas desalineadas; fuentes locales del front matter existentes; `estado: en-progreso`, canon sin `tema`.
- [Baseline del ciclo](../autor-u05-ciclo1/before.json): **292/292 archivos protegidos conservan SHA-256**, cero diferencias/faltantes. Incluye capturas, material original/caches, PDF S.1 preparado, síntesis, revisión U5, reviews A/B y snapshot inicial. No se pretende que las 401 entradas del snapshot permanezcan iguales: los candidatos se corrigieron deliberadamente.
- Sólo modificados académicamente APUNTE, INDICE y TP5. Repaso **idéntico** al inicio; se conservan sus diez preguntas y claves. Nuevos scripts/renders de autor en `tmp/autor-u05-ciclo1/` y este cierre autorizado. Sin originales alterados, instalaciones, builds ni commits.
- Brechas académicas restantes: las 13 filas de §17; especialmente código 4/8, identidad de intercambio, AI5/VIR, T.51, juegos primario/suplementario/Teletex, Aiken/FIELDATA/CCSID y convenciones docentes. **No pasar a completo/revisado** sin cobertura/fuentes y revalidación.
- Entrega congelada tras cerrar el ciclo; no modificar hasta nueva orden de ROOT.

**skill_resolution: injected**

---

<!-- Evidencia original preservada: tmp/reviews/revalidacion-u05-a-ciclo1.md -->

# Revalidación focal U5-A-001 — ciclo 1

**Fecha:** 2026-10-13 · **Dictamen:** **PASS** para la corrección de trazabilidad; no es certificación integral de U5.

Comparé el original del programa analítico, PDF p. 4, con §16–17 de `APUNTE.md`. El programa enumera explícitamente, entre otros, código 4/8, intercambio de datos, Fieldata, AI N.º 5/VIR, T.51 y los juegos primario, suplementario y Teletex. §16 los deja enlazados al destino y caracteriza el alcance efectivamente desarrollado. §17 anuncia claramente que los faltantes siguen pendientes y no se evalúan como conocimientos confirmados.

**Checklist:** 13/13 filas identificables con ancla, destino/tema, evidencia faltante o límite documentado, búsqueda/acción siguiente y criterio verificable de cierre. Ejemplos: 4/8 pide tabla/asignación original y cotejo de peso; T.51 requiere edición y páginas; intercambio de datos impide asumir que equivale a EBCDIC. No recertifico VIR, T.51 ni otros repertorios sin sus fuentes.

El front matter conserva `estado: en-progreso`; no hay declaración de cobertura final. Revisé 95 enlaces locales en APUNTE/INDICE y 13 anclas de pendiente: **0 fallas**. SHA-256 (APUNTE `078a9963…a0924`, INDICE `f16b5349…1022`, TP5 `bacfdd38…bd88`) coincide con snapshot ciclo1. Integridad manifiesto: **401/401 antes** de escribir este informe y **401/401 después**, 0 diferencias/faltantes.

**Límites:** dictamen focal exclusivamente U05-A-001; el texto extraído del programa se contrastó con el PDF, no certifica cobertura integral ni corrige pendientes académicos.

**skill_resolution:** injected

---

<!-- Evidencia original preservada: tmp/reviews/revalidacion-u05-b-ciclo1.md -->

# Revalidación independiente U05-B — ciclo 1

**Alcance focal:** sólo U05-B-001/002/003; no es revisión integral de U5. `APUNTE.md` conserva `estado: en-progreso`.

| ID | Dictamen | Evidencia de cierre |
|---|---|---|
| U05-B-001 | **PASS** | Cotejé visualmente las 32 filas del Cuadro 1/S.1 con el repertorio: PDF p.7 (impresa 3); A=0/Z=1, elementos 1→5 y combinaciones 29/30 coinciden. pp.5–6 confirman repertorio, estados y cambios; p.8 confirma límites de combinación 32 y Cuadro 2 confirma funciones/figuras de controles. Letras, cifras/símbolos, A/Z y binarios del apunte coinciden; nota de variantes no universaliza 6–8 ni el uso de 32. Anclas de repertorio/cobertura e índice resuelven. |
| U05-B-002 | **PASS** | TP E4 c identifica independencia de las seis posiciones; 42 Shannon por palabra y 7 Shannon/símbolo son consistentes con 128 equiprobables. Etiqueta ya no dice «dec)». |
| U05-B-003 | **PASS** | E9–E13 presenta separaciones legibles entre texto, LaTeX, magnitudes y unidades (p. ej. Shannon/s, píxeles/imagen, Mbit/s, líneas × puntos, bytes = bit, `UTN`/`Red`). Los números/unidades visibles concuerdan con los valores registrados en el cierre; no encontré variación numérica en el contenido revisado. |

**Integridad y enlaces:** snapshot v1: 401 rutas; 388 hashes idénticos y 13 diferencias, incluidas las tres candidatas U5 esperadas; no faltan rutas. No investigué las otras diferencias. APUNTE 81, INDICE 23 y TP5 4 enlaces: 108/108 rutas y anclas locales resolubles. No evalué la cobertura total ni fuentes/capturas locales pendientes: no promover estado. **Límite:** revalidación focal; no declara U5 completa/revisada.

**skill_resolution: injected**

---

<!-- Evidencia original preservada: tmp/reviews/revalidacion-u05-b-ciclo1-errata.md -->

# Errata — revalidación U05-B, ciclo 1

**Corrección del enunciado de integridad (no reemplaza el informe original):** el dato «388/401 iguales y 13 diferencias» se obtuvo al comparar con `snapshot-inicial.json`; no describe el snapshot de ciclo 1. Mi dictamen focal PASS para U05-B-001/002/003 no cambia: la verificación comprobó ahora que las tres candidatas U5 están en el manifiesto ciclo 1 y sus hashes actuales coinciden.

**Comprobación independiente:** `docs/consolidacion-u1-u6/snapshot-ciclo1.json` tiene SHA-256 `bb1dc05265cd738b0a8ba46e1accee0642b04a8cf662eca1889b1322fcc139eb`, 401 rutas únicas, cero duplicadas o ausentes, cero discrepancias SHA-256 y cero discrepancias de tamaño (bytes). El checker raíz reportó `snapshot_diferencias: []` y `snapshot_agregados: []`. Mi verificación independiente confirma hashes/rutas del manifiesto; no reproduce el conteo de agregados porque el manifiesto, por sí solo, no define el filtro de archivos del paquete. No comparé el conjunto completo del árbol.

U5 conserva `estado: en-progreso`; este resultado no declara cobertura completa ni revisión integral.

