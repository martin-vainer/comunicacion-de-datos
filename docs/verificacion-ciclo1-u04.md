# Revalidación U04 — ciclo 1


---

<!-- Evidencia original preservada: tmp/reviews/cierres-u04-ciclo1.md -->

# Cierres U4 — ciclo 1

Fecha: **2026-10-13**. Autor U4. Estado: **correcciones y retest del autor completos; espera re-revisión independiente**, unidad permanece `en-progreso`. No se borraron ni editaron los dictámenes iniciales. No se revisó contenido de otras unidades.

## U04-A-001 — Cerrado por corrección; hallazgo confirmado

**Admito el error de mi candidato:** M1/C5 NO tiene una contradicción interna tabla/diagrama. Se volvió a los originales antes de editar: M1 PDF p.19 y P PDF p.14 renderizados nuevamente con Poppler a 1800 px; C5 image-14 + tabla Markdown líneas 294–303; CP image-38 + tabla líneas 414–423. Lectura visual de cada punto, usando 0° a derecha y antihorario positivo. No se resolvió por mayoría A/B.

Los siguientes pares fueron leídos tanto en tabla como en diagrama de cada fuente; cada celda indica **tabla = diagrama**:

| Fase | M1 p.19 | C5 tabla/image-14 | P p.14 | CP tabla/image-38 |
|---:|:---:|:---:|:---:|:---:|
| 0° | 011 = 011 | 011 = 011 | 000 = 000 | 000 = 000 |
| 45° | 010 = 010 | 010 = 010 | 001 = 001 | 001 = 001 |
| 90° | 000 = 000 | 000 = 000 | 011 = 011 | 011 = 011 |
| 135° | 001 = 001 | 001 = 001 | 010 = 010 | 010 = 010 |
| 180° | 101 = 101 | 101 = 101 | 110 = 110 | 110 = 110 |
| 225° | 100 = 100 | 100 = 100 | 111 = 111 | 111 = 111 |
| 270° | 110 = 110 | 110 = 110 | 101 = 101 | 101 = 101 |
| 315° | 111 = 111 | 111 = 111 | 100 = 100 | 100 = 100 |

**Conclusión:** ambas convenciones son internamente consistentes y Gray circular. Para cada fase, etiqueta M1/C5 = etiqueta P/CP XOR `011`: invierte los dos bits finales. No es una contradicción dentro de M1 ni una etiqueta temporal distinta del mismo símbolo. El APUNTE conserva los dos mapeos en un cuadro y explica cuál adopta TP/repaso. Eliminada la afirmación falsa de su §5. La afirmación contraria de B queda superada por este cotejo, sin alterar su informe inicial. A001 **no se reclasifica como falso positivo**.

**Retest:** 32 pares fuente (8 × 4); igualdad tabla/dibujo en cada fuente; ocho etiquetas únicas y Hamming 1 en los ocho vecinos circulares, en ambos mapeos. Cuadro nuevo del APUNTE cotejado por script con esos valores. PNG fuente/copia intactos.

## U04-A-002 — Cerrado por autosuficiencia de Q2

La corrección local incluye ahora:
- 8-PSK: 14 400 bit/s, ocho filas fase/bits y diagrama ASCII propio, I/Q y convención explícitos.
- 16-PSK: 19 200 bit/s, dieciséis filas fase/bits y SVG propio embebido, todas las fases/etiquetas visibles.
- Comparación condicionada de ruido/QAM y límites de BER; los enlaces a TP quedan como ampliación, no reemplazan la salida.

No se presenta el PNG M1/C5 como solución de la convención alternativa. El SVG existente se reutiliza con los **4800 baudios de Q2**, sin importar los 2400 del TP E5. Retest: 24 filas de repaso coinciden con sus representaciones; Gray circular y coordenadas/etiquetas SVG comprobadas. Vistos render propio de todas las primitivas SVG con Pillow y vista monoespaciada del ASCII nuevo: sin superposiciones ni cortes. No se afirma render de navegador/Markdown.

## U04-A-003 — Cerrado por fidelidad del literal

V PDF p.1 se renderizó e inspeccionó nuevamente; su fila imprime `BER = 16-6 (VER 1)` en línea base. §5 y fila de pendientes ahora conservan **`16-6 (VER 1)`**, no `16^-6`, sin suponer exponente ni corregir a una potencia. Sigue pendiente la condición BER: ningún ejercicio usa ese literal como número confirmado. Retest textual: dos apariciones correctas y ninguna `16^-6` en APUNTE.

## U04-B-001 — Cerrado por acotación explícita de alcance

Se eligió la alternativa autorizada **acotar**, no introducir un modelo ajeno. M1 pp.5–6/C5 sólo respaldan clasificación/definición de PM. El mapa separa PM de los modelos FM; §3 y “Para examen” dicen expresamente que PM se exige como definición/distinción respecto de FM, no cálculo de ecuación/índice/banda. El ejemplo estático queda rotulado como aclaración conceptual propia. El pendiente deja visible la ausencia de modelo y ejemplo calculado fuente. No se afirma cobertura cuantitativa del punto PM del programa ni se añade una pregunta evaluable sobre ella.

Retest: esas restricciones aparecen en mapa, cuerpo, objetivo de examen y pendientes; FM mantiene fórmulas, unidades, supuestos y cálculos previos. No se añadieron fórmulas PM ni temas externos.

## Retest global de rutas U4

Ejecución: `tmp/autor-u04/ciclo1/retest.py` con Python bundled; salida **PASS, exit 0**. Evidencia: `tmp/autor-u04/ciclo1/retest.json` y `qa-base.json`.

- **34 recálculos** base PCM/PSK/FM/Delta/E1/T1/PDH/STM/FDM/OFDM/STDM/WDM; TP conserva E1–10 y repaso Q1–4. Sin errores. Q2 tasas y separaciones contrastadas con sus cuadros; no cálculo BER nuevo.
- **107 enlaces/anclas locales** sin errores. En unidades enlazadas sólo existencia/ancla, no revisión sustantiva.
- **14 PNG** origen/copia SHA-256 idénticos; SVG 16-PSK válido y geometría/etiquetas coincidentes. No se cambió ningún PNG ni el SVG reutilizado.
- **290 hashes protegidos** antes/después: 286 entradas material/capturas/caches del snapshot más manifiesto inicial, síntesis U4 y dos informes U4-A/B. Cero diferencias. Los 286 hashes coinciden además con el snapshot inicial. No se exige que otros candidatos, corregidos por sus autores, conserven su hash inicial.
- Figura Q2: render de primitivas SVG y ASCII propio vistos; no Mermaid afectado ni cambios de sus bloques, por lo tanto no hay retest de motor Mermaid que atribuir a este ciclo.
- `git diff --check` de rutas U4: sin errores. Sin build/install/commit.

Los pendientes μ/FSK/FM/WDM/CDM no se resolvieron ni se evaluaron como confirmados. Tras entrega, archivos U4 congelados hasta orden del coordinador.

---

<!-- Evidencia original preservada: tmp/reviews/revalidacion-u04-a-ciclo1.md -->

# Revalidación independiente U04-A — ciclo 1

**Fecha:** 2026-10-13 · **skill_resolution:** injected. **Alcance:** sólo retest focal, no revisión total de U4; sin editar candidatos/originales ni build, install o commit. **Resultado: 3 PASS; unidad sigue `en-progreso`.**

- **U04-A-001 — PASS.** Reabrí M1 p.19 (`m1-19.png`), P p.14 (`p-14.png`), CP `image-38.png` y C5 `image-14.png`, incluyendo tablas y diagramas. En cada una, los ocho pares fase/etiqueta coinciden. M1/C5: 011,010,000,001,101,100,110,111; P/CP: 000,001,011,010,110,111,101,100 para 0°–315° cada 45°. M1/C5 = P/CP XOR `011`; ambos mapeos son Gray circulares. APUNTE `#psk-qam` ahora identifica diferencia entre fuentes, no contradicción interna.
- **U04-A-002 — PASS.** CQ Q2.1 pide cuadro y diagrama. Repaso incluye tabla+ASCII 8-PSK y tabla+SVG 16-PSK. Revisé los 16 labels, cierre Gray, geometría SVG (`psk16-preview.png`) y 4800 baudios → 14 400/19 200 bit/s. Salida autosuficiente; comparación de error condicionada, sin BER inventada.
- **U04-A-003 — PASS.** V p.1 (`v-1.png`) dice literalmente `BER = 16-6 (VER 1)` en línea base. APUNTE conserva ese literal (dos ocurrencias), no `16^-6`; sigue ambiguo y no se usa numéricamente.

El cierre enumera los tres IDs; acciones reflejadas en APUNTE/repaso y Q2 conserva 4800 baudios, no los 2400 del TP E5. Anchors explícitos únicos: APUNTE 16, repaso 4; sin duplicados. Snapshot ciclo1: **401/401 hashes coinciden antes y después**, cero faltantes/diferencias. No revalidé otros issues de U4.

---

<!-- Evidencia original preservada: tmp/reviews/revalidacion-u04-b-ciclo1.md -->

# Revalidación independiente — U04-B-001

**Resultado: PASS con alcance deliberadamente limitado.** Unidad **en-progreso**; esto no certifica U4 completa. No consulté informes A ni conclusiones ajenas.

## Evidencia y criterios

- **Límite de fuente/programa:** el programa analítico (`material/catedra/PROGRAMA de la materia.pdf`, p. 3) incluye modulación de fase. M1 original, pp. 5–6, y C5, líneas 85–90, sólo clasifican PM como continua analógica y fase como parámetro; no aportan modelo/ecuación o datos de cálculo PM.
- **Acotación:** el mapa (`APUNTE.md`, línea 46) y §§3 / «Para examen» (líneas 158–162, 189) limitan PM a definición/distinción respecto de FM; dicen que no se exige ni evalúa modelo, índice, banda ni cálculo, y dejan pendiente su ausencia fuente. No hay fórmula ni promesa cuantitativa.
- **Ejemplo / fuentes:** mensaje constante (línea 160) está rotulado aclaración conceptual propia, no ejercicio de cátedra. FM puede mantener frecuencia desplazada; PM fase desplazada: ejemplo no falso. No se añadió bibliografía/modelo externo; formalización siguiente es FM.
- **Rutas:** 16 anclas únicas, cero enlaces rotos en APUNTE; ancla `#fm-pm` desde INDICE resuelve.

## Integridad

Snapshot ciclo 1: 401 entradas; SHA-256 `BB1DC05265CD738B0A8BA46E1ACCEE0642B04A8CF662ECA1889B1322FCC139EB`. Candidatos (coinciden con snapshot): APUNTE `10de5412d93eaaa960c781036e0f4bcf62a3fb4621afc5c210cb2840fd77f573`; INDICE `c6c0f09d58ddef3589175771813da2160cf5a71fdc7bae8df7cbd4bd7784467c`. Fuentes sin cambios: M1 `328229bce1d5331fc617e255bb4ece385e7ded254c63100a9b65fb20a59c0b5e`; C5 `f78306c245f5009a0719983792f79ab2b65149bb4762755a93ece17927cef5af`; programa `516b95c28e17602e9c656536bd43f1e9ac27433847b5cd9eb72818387a6d986e`.

**Cierre B:** PASS por acotación coherente, sin falso alcance cuantitativo. PM permanece en el programa; apunte explicita cobertura parcial; U4 no se declara revisada. `skill_resolution: injected`.
