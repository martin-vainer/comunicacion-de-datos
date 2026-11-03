# Revisión U04 — A/B

## Dictamen A

# Dictamen independiente U04-A — revisión académica

- **Fecha:** 2026-10-13. **Identidad:** revisor académico A, independiente del autor y de otros revisores. **skill_resolution:** injected.
- **Objeto:** U4 canónica, navegación, 15 recursos gráficos, TP4 E1–10 y repaso Q1–4. Sin edición de candidatos ni originales, sin build, instalación o commit.
- **Dictamen:** **requiere corrección puntual antes de aprobar/promover**. No encontré errores de resultados numéricos ni de claves contextualizadas; sí una afirmación académica falsa sobre la evidencia Gray, una corrección de repaso no autosuficiente y una transcripción editorial inexacta. Conteo: **P0=0, P1=1, P2=1, P3=1**.
- `estado: en-progreso` es honesto. Esta revisión NO convierte la unidad en `revisado`: quedan pendientes explícitos de las fuentes y los issues de abajo. U7/U8 excluidas: su no desarrollo no es un defecto.

## 1. Integridad, independencia y procedimientos

Repositorio: `C:/Users/Martin/Documents/UTN_SISTEMAS/Anual_2026/comunicacion_de_datos`.

Leí AGENTS.md y metodología. No consulté informes de autores/otros revisores, `estado.md`, `revisiones.md`, `tmp/autor-*` ni conclusiones ajenas en memoria. Las autocertificaciones embebidas no se usaron como prueba. Sección 16 del APUNTE excluida del juicio sustantivo. Se comprobó existencia de enlaces al registro de imágenes sin leer sus conclusiones: procedencia gráfica reconstruida por hashes.

**Snapshot:** `docs/consolidacion-u1-u6/snapshot-inicial.json`, 401 entradas. SHA-256 del manifiesto: `1e29fd3bf30b9d99d07e0d3b73e2d7ef11f9d85bb7874b2630650412068a7bdd`. Comparación independiente Python con SHA-256 por archivo: **401/401 coinciden antes y después, 0 diferencias**. Evidencia propia: `u04-a/hashes-antes.json`, `u04-a/hashes-despues.json`; el control correcto fue comparación Python de cada hash con su esperado (no la salida inicial defectuosa del filtro PowerShell).

**Método real:** lectura completa de candidatos/capturas/caches; extracción auxiliar pypdf por página a recursos propios; Poppler renderizó todas las páginas originales (1000 px de ancho), inspección de todas las láminas, ampliación individual de páginas críticas M1 p.19, R p.3 y V p.1; inspección de las 69 imágenes únicas referidas por las cinco capturas. No se trató texto extraído como autoridad visual. Recalculé modelos, unidades, hipótesis y ejemplos mediante lectura manual y `u04-a/qa.py`: **95 entradas QA numéricas/estructurales sin fallo**, incluyendo Gray circular y coordenadas del SVG. Se comprobaron **91 enlaces locales de los cuatro candidatos**, todos existentes y con anclas explícitas válidas cuando corresponden; no se leyó contenido ajeno para validar una mera ruta.

## 2. Corpus original efectivamente contrastado

IDs de esta revisión coinciden sólo por comodidad con nombres de fuente, no con certificaciones del autor. Todas las páginas siguientes fueron leídas textualmente y vistas en originales renderizados, incluso portadas y páginas sólo gráficas.

| ID | Original | Páginas PDF vistas | Contraste efectivo |
|---|---|---:|---|
| M1 | `material/teoria/U4/U4 MODULACION 1.pdf` | **1–27, 27/27** | Clasificación/cadena 2–6; AM 7–8; ASK/FSK/FM 9–14; PSK/Gray 15–19; QAM 20–24; offset/diferencial/TCM 25–27 |
| M2 | `material/teoria/U4/U4 MODULACION 2.pdf` | **1–13, 13/13** | Pulsos 2–3; PCM/cuantificación/compansión 3–10; DM/ADM/DPCM 11–13 |
| X | `material/teoria/U4/U4 MULTIPLEXACION.pdf` | **1–36, 36/36** | MUX/QoS 2–5; FDM/jerarquía 6–10; OFDM 11–13; TDM/E1/T1 14–18; PDH 19–22; SDH/SONET/VC 23–27; STDM 28; WDM 29–33; CDM/acceso 34–36 |
| P | `material/practica/U 4/UT 4 MODULACION Y MULTIPLEXACION.pdf` | **1–20, 20/20** | Clasificación y señales 2–8; AM/FM/BPSK/Gray 9–14; multiplexación 15–20 |
| TP | `material/practica/U 4/TP 4  2026.pdf` | **1–3, 3/3** | Enunciados originales E1–8 p.2, E9–10 p.3 |
| R | `material/practica/U 4/EXPRESIONES  Y RTAS UNIDAD  TEMATICA NRO 4.pdf` | **1–4, 4/4** | Soluciones E1–3 p.1; E3–5 p.2; E5–10 p.3; comparativo E10 p.4 |
| V | `material/practica/U 4/U 4 - PARAMETROS PRINCIPALES DE  LOS DIFERENTES METODOS DE MODULACION.pdf` | **1, 1/1** | Todas filas, niveles/fases/estados, bits, eficiencia, banda normalizada y condición S/N/BER |
| C5 | `capturas/teoria/04-modulacion-digitalizacion-multiplexacion/clase 5.md` | **1–379 líneas** | Completa, todas sus imágenes incluidas |
| C6 | `capturas/teoria/04-modulacion-digitalizacion-multiplexacion/Clase 6.md` | **1–194 líneas** | Completa, PCM/compansión/variantes |
| C62 | `capturas/teoria/04-modulacion-digitalizacion-multiplexacion/clase 6.2.md` | **1–1458 líneas** | Completa, incluidos todos órdenes, WDM/CDM y métodos finales |
| CP | `capturas/practica/clase 06.md` | **1–994 líneas** | Completa, clasificación, Gray, MUX y E1–10 |
| CQ | `capturas/teoria/Cuestionarios/cuestionario - modulacion y multiplexacion.md` | **1–132 líneas** | Completa Q1–4 y respuesta gráfica |

**Total PDF específico: 104/104 páginas. Capturas: 69/69 imágenes únicas**; 55 del directorio teórico U4, 13 de práctica y 1 del cuestionario. Inventario exacto, hashes y agrupación visual en `u04-a/captures-manifest.json`; páginas y archivos en `u04-a/pdf-manifest.json`. Láminas PDF `M1/M2/X/P/R/TP/V-sheet-*` y capturas `capture-sheet-1,5,…,69.png` realmente inspeccionadas.

**Siete caches existentes leídos completos:** `u4-u4-modulacion-1.txt`, `u4-u4-modulacion-2.txt`, `u4-u4-multiplexacion.txt`, `u4-ut-4-modulacion-y-multiplexacion.txt`, `u4-tp-4-2026.txt`, `u4-expresiones-y-rtas-unidad-tematica-nro-4.txt`, `u4-u-4-parametros-principales-de-los-diferentes-metodos-de-modulacion.txt`, todos en `material/_cache/`. V sólo transcribe título: la tabla se verificó visualmente, no por cache.

## 3. Cobertura del candidato, sección por sección

APUNTE: `apuntes/teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md`; INDICE del mismo directorio.

| Sección/ancla | Fuentes contrastadas | Resultado académico/pedagógico |
|---|---|---|
| YAML, introducción, procedencias | Siete originales; cinco capturas | Estado/alcance honestos; referencias por sección; corpus registrado, no expansión |
| 1 `modulacion` | M1 2–6; P 2–8; C5/CP | Cadena y distinción información/representación correctas; seno, período/pulsación y unidades verificadas |
| 2 `am` | M1 7–8; P9; C5/CP | Envolvente, DBL/BLU/portadora y variantes; modelo didáctico, no fórmula atribuida literalmente |
| 3 `fm-pm` | M1 5–6,12; P10; R3; C5/CP | Índice/Carson correctos; banda significativa aproximada y sensibilidad ambigua advertidos; PM básico registrado |
| 4 `ask-fsk` | M1 9–14; P6–7; C5/CP | ASK/OOK/FSK, amplitud/frecuencia y representación; criterio π/2 conservado como pendiente, no regla comprobada |
| 5 `psk-qam` | M1 15–27; P11–14; V1; C5/CP/CQ | Tasas, Gray, geometrías QAM, curvas y variantes correctas; **U04-A-001**, **003** |
| 6 `pulsos` | M2 2–3; P5–7; C5/CP | PAM/PDM/PPM distinguidos con tres ejemplos; amplitud aún continua |
| 7 `pcm` | M2 3–10; X16–18; C5/C6/CP | Muestreo/cuantificación/codificación, error, compansión y leyes; igualdad límite y 128/7 versus PCMU separados |
| 8 `delta-dpcm` | M2 11–13; C6 | DM paso fijo, empate convencional, sobrecarga/granular; ADM cambia paso; DPCM predicción y repertorio explícitos |
| 9 `multiplexacion` | X2–5; P15–16; C62/CP | No ganancia ilimitada de capacidad; presupuesto tasa/control y QoS contextualizados |
| 10 `fdm-ofdm` | X6–13; P17; C62/CP | Guardas, cinco órdenes analógicos, ortogonalidad y cadena IFFT/FFT; pregrupo sólo nombrado según fuente |
| 11 `tdm` | X14–18; P18; C62/CP | Entrelazado bits/caracteres, E1/PCM30 y T1/PCM24; bruto/voz/control; CAS robado no cada octeto |
| 12 `pdh-sdh` | X19–27; C62 | Relojes, justificación, órdenes/períodos, SDH/SONET/STM-N, add/drop, punteros/VC; E5 y VC2 corrigenda documentadas |
| 13 `stdm` | X28; P19; R4; C62/CP | Dinámica, identificación/buffers, control y cola; no promesa de atender picos gratis |
| 14 `wdm-cdm` | X29–36; P20; C62/CP | WDM/CWDM/DWDM, equipos, combinación SDH; CDM y seis métodos al nivel registrado, sin desarrollo U7/U8 |
| 15 `pendientes` | Contraste anterior | Dudas FM/FSK/BER/μ/absolutos ópticos y código visibles, no evaluadas como verdad |
| 16 registro autor | Excluido | No se aceptó como evidencia ni se usaron sus conclusiones |
| 17 `practica` y relaciones | TP/R/CP/CQ | Destinos práctica/repaso separados y enlaces válidos |
| 18 resumen/checklist | Contenido anterior | Resumen mental y preguntas de examen presentes; no ausencia metodológica central generalizada |
| INDICE entero | APUNTE/TP/repaso | Navegación breve y 19 enlaces locales resolubles; exclusiones y estado coherentes |

## 4. Figuras: contraste de TODAS

Las 14 PNG candidatas son **idénticas byte a byte** a originales inspeccionados. El hash no sustituye el juicio visual: se utilizó después de mirar originales para asegurar que la copia no cambió. `u04-a/figures.json` contiene SHA-256 por figura y procedencia obtenida sin registro autoral.

| Recurso candidato | Captura original teórica U4 | PDF/concepto contrastado |
|---|---|---|
| `am-espectro.png` | image-3.png | M1 p.8, bandas positivas/negativas y DBL/BLU |
| `psk8-fuente.png` | image-14.png | M1 p.19, cada etiqueta angular; **001** |
| `qam-constelacion.png` | image-16.png | M1 p.21, ocho puntos/radios/fases y señal temporal |
| `psk-qam-errores.png` | image-19.png | M1 p.24, Pe logarítmico frente Eb/N0 y comparación condicionada |
| `pulsos.png` | image-24.png | M2 p.2, altura/ancho/posición |
| `cuantificacion.png` | image-27.png | M2 p.5, entrada/compresión/cuántificador |
| `ley-a.png` | image-29.png | M2 p.7, segmentos/escala positiva; no inferir longitud con signo sólo del eje |
| `delta.png` | image-32.png | M2 p.11, escalera, arranque y sobrecarga |
| `ofdm.png` | image-37.png | X p.11, centros y ceros de otras subportadoras |
| `e1.png` | image-40.png | X p.17, 32 slots, TS0/16 y 30 voz |
| `pdh.png` | image-44.png | X p.22, órdenes y tasas redondeadas de tres jerarquías |
| `tdm-stdm.png` | image-45.png | X p.28, asignación fija/dinámica, no longitud variable obligatoria |
| `wdm.png` | image-46.png | X p.29, combinación/separación ópticas |
| `acceso-multiple.png` | image-54.png | X p.35, frecuencia/tiempo/código |
| `psk16-propio.svg` | Reconstrucción propia, no original | TP E5, CP tabla16/R pp.2–3: 16 puntos, radio225, signos I/Q, pasos22,5°, etiquetas Gray y cierre circular correctos |

**SVG:** leído todo XML, verificado cada coordenada/etiqueta por script y visto render propio de todos sus primitives con Pillow (`svg-render-subset.png`). Subconjunto completo de etiquetas del archivo soportado; Arial sustituye sans-serif. Edge headless no produjo captura; NO afirmo QA de motor de navegador/Markdown. Diagramas Mermaid y ASCII se revisaron semánticamente, sin build/render Markdown.

## 5. Fórmulas, ejemplos, tasas y supuestos

Resultados completos de 95 entradas en `u04-a/calculos.json`, script reproducible `qa.py`. Los checks son controles de lectura, no pruebas de un producto ni build. Todos los modelos calculables del candidato se verificaron; expresiones ambiguas explícitamente pendientes del original no se forzaron a un resultado.

| Familia | Resultados recalculados / hipótesis verificadas |
|---|---|
| Portadora | 1000 Hz → 1 ms, 2000π rad/s; 2 V a 0,25 ms con fase0. Argumento seno adimensional |
| AM | Ap2, μ0,5 → envolvente1–3 V; Bm3 kHz → DBL6/BLU3 kHz, 97–103/100–103 kHz a100 kHz; tono1 kHz laterales99/101. Índice0–1 y filtros ideales |
| FM | Δ1 MHz/tono10 kHz=100; Carson2,02 MHz; límites98,99–101,01 MHz. Angosta10 Hz/1000 Hz=0,01 y2020 Hz≈2 kHz. No soporte espectral exactamente finito |
| PSK/QAM | log2(2,4,8,16,128)=1,2,3,4,7; 4800×3/4=14400/19200 bit/s, 45°/22,5°; E3 1000×4=4000, E4 2400×3=7200. M2^b, sin overhead/TCM salvo ejemplo expreso |
| Geometría/Gray | Gray2/3/4 circular cambia1 bit incluso cierre. SVG tabla16 idéntica a su geometría. 16QAM rectangular16 pares I/Q: energía media10, distancia mínima2; PSK16 con igual energía: 2√10 sin(π/16)≈1,234. Curva respalda tendencia, no BER universal |
| Eficiencia/V | 9600/4000=2,4 y4800/4000=1,2 bit/s/Hz. V bits1/2/3/4/4, eficiencia0,7/1,4/2,1/2,8/2,8 y S/N13/16/22/30/28 dB contrastados; su banda normalizada1,4/0,7/0,47/0,35/0,35 es recíproca redondeada, no umbral nuevo. Condición BER sin resolver |
| Pulsos | 10000 pulsos/s →100 μs; PAM0,7 V, PDM1/2 μs, PPM1/2 μs son ejemplos de variables distintas, no equivalencia de bits |
| PCM | 125 μs →8000 muestras/s; 128→7→56000 bit/s;256→8→64000. fs≥2fmax ideal, igualdad crítica/anti-alias con margen. No Shannon ni confundir Hz con flujo |
| Cuantificación | (4−0)/4=1 V, representantes0,5/1,5/2,5/3,5;1,3−1,5=−0,2 V y límite0,5. Centralcells/sin saturación.0,02/0,1=20%,0,02/1=2%; compansión cualitativa, no precisión exacta inventada |
| DM/ADM/DPCM | Δ0,1, inicio0 y entradas0,15/0,25/0,18→110→0,1/0,2/0,1 V; 32k muestras/s=32k bit/s,31,25 μs, pendiente3200 contra demanda6400 V/s. ADM paso0,2 ilustrativo; DPCM1,3−1=0,3 y repertorio condicional |
| MUX/FDM/OFDM | 3×64+8=200 kbit/s;3×4+2×0,5=13 kHz;12×4=48 y900×4=3600<3716 kHz. Jerarquía12/60/300/900/2700 con48/240/1200/3716/12026 kHz según fuente.1 ms→1 kHz separación útil;8000/4=2000 bit/s por flujo |
| TDM/E1/T1 | A101+B011 intercalado10|01|11;256×8000=2,048 Mbit/s, voz1,920/control0,128;slot3,90625 μs/bit0,48828125 μs. T1(24×8+1)×8000=1,544 Mbit/s, campos1,536/alineación0,008. CAS robado en ciertas tramas |
| PDH | Nb/V: E1 125, E2 100,3788, E3 44,6927, E4 20,8525, E5 4,7576 μs; E2−4E1=0,256 y E3−4E2=0,576 Mbit/s.30×4 sucesivamente120/480/1920/7680; no multiplicador universal americano/japonés |
| SONET/SDH | OC1=51,84;OC3/9/12/24/48/192/768=155,52/466,56/622,08/1244,16/2488,32/9953,28/39813,12 Mbit/s. STM9×270N×8×8000, 2430 octetos STM1/38880 STM16. VC área2349 octetos150,336 Mbit/s; C42340→149,760; no todo datos usuario |
| STDM | TDM3×8=24 bits;2activos(8+2)=20,3activos=30; demanda48−salida32=cola16 kbit/s. IDs, formato hipotético y promedio/picos separados |
| WDM/CDM | 160×10=1600 Gbit/s=1,6 Tbit/s;8×10=80;32×10=320; C62 40×10=400 Gbit/s.1500 nm con c≈3e8→200 THz, no bit/s. Códigos(1,1)/(1,−1), producto0; A+ y B− suman(0,2); correlaciones/2 recuperan+1/−1. Sin ruido, sincronismo/igual potencia |

Comprobaciones externas limitadas a aclaraciones ya citadas, no extensión del programa: [RFC3551 §4.5.14](https://datatracker.ietf.org/doc/html/rfc3551#section-4.5.14) confirma octetos PCMA/PCMU; [UIT-T G.707 12/2003 §10.1.3, PDF p.107](https://www.itu.int/rec/dologin_pub.asp?id=T-REC-G.707-200312-S%21%21PDF-E&lang=e&type=items) confirma tributario6312 kbit/s; [Cisco CAS doc22444, PDF p.1](https://www.cisco.com/c/en/us/support/docs/voice/digital-cas/22444-t1-cas-ios.pdf) confirma extracción periódica; [Cisco CWDM](https://www.cisco.com/c/en/us/products/collateral/interfaces-modules/cwdm-transceiver-modules/product_data_sheet09186a00801a557c.html) distingue transceptores y MUX/OADM pasivos. El HTML CAS dio error, se usó su PDF oficial. No se auditó íntegramente G.707 ni estas fuentes largas, sólo las afirmaciones pertinentes.

## 6. TP4 y repaso: cobertura efectiva individual

| Ítem | Evidencia original | Control y resultado |
|---|---|---|
| E1 | TP2/R1/CP | Datos exactos, filtro interpretado pasa-bajos, 56/64 kbit/s y margen de muestreo; correcto |
| E2 | TP2/R1 | Separación22,5°=π/8, no salto obligatorio; correcto |
| E3 | TP2/R1–2 | Relación4 bits/símbolo y ejemplo1000→4000; correcto |
| E4 | TP2/R2/P14/CP | Señales digital/analógica/analógica; ocho etiquetas, ASCII/mapeo coherentes, Gray circular, Vm×3; correcto |
| E5 | TP2/R2–3/CP | 9600/2400=4,16PSK; todas16 filas/coords SVG,22,5°; no asevera realizabilidad sin ruido/banda; correcto |
| E6 | TP2/R3/CP | Carson2020 kHz=2,02 MHz, índice100 y ubicación; correcto |
| E7 | TP2/R3/M1 5/P7 | Todas cuatro familias y ejemplos; PCM origen analógico frente representación codificada aclarados |
| E8 | TP2/R3/CP | Clave FM frente ruido de amplitud; no inmunidad ni ranking universal; correcto |
| E9 | TP3/R3/CP | FDM agregado analógico/TDM digital en esquema del TP, no prohibición TDM analógico; correcto |
| E10 | TP3/R4/P17–19/CP | Todas filas, ejemplos13 kHz/24/20/30 bits y corrigenda simplex/SNR/costos/eficiencia; correcto |
| Q1 | CQ1/M1 5–6,12–14 | e: FM/FSK ausentes; distractores explicados |
| Q2 | CQ2+imagen/M1 19–24 | 14400/19200, Gray, distancias y condiciones correctos; **002**, salida gráfica requerida remitida al TP |
| Q3 | CQ3/M2 3–5 | a: muestreo→cuantificación→codificación; correcto |
| Q4 | CQ4/M2 4,11–12/X15–17 | b sólo en voz→PCM→TDM; ruido pertenece cuantificador/Delta, no TDM per se; contextualización correcta |

## 7. Issues accionables

### U04-A-001 — P1 académico — falsa discrepancia entre tabla y figura Gray

- **Ubicación:** `apuntes/teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md`, `#psk-qam`, **línea252**.
- **Claim:** «Figura C5 image-14/M1 p.19: su diagrama y la tabla contigua emplean asignaciones diferentes».
- **Evidencia primaria:** M1 **p.19**, inspección individual `u04-a/M1-19.png`; C5 image-14 y tabla C5 **líneas294–304**. Tabla y dibujo originales coinciden exactamente: 0°011,45°010,90°000,135°001,180°101,225°100,270°110,315°111. El PNG candidato conserva ese dibujo sin alteración.
- **Naturaleza:** **demostrado**, no sospecha. La tabla CP/P adoptada por el candidato sí es diferente (000 a0°), pero NO lo son la tabla y figura dentro de M1/C5.
- **Impacto:** atribuye un defecto inexistente a la fuente y enseña a desconfiar de un mapeo internamente consistente; la advertencia de no mezclar convenciones necesita identificar correctamente qué se compara.
- **Acción:** decir que **M1/C5 usa una asignación distinta de CP/P**, ambas válidas e internamente coherentes; eliminar la atribución falsa a su tabla contigua. No tocar originales ni cambiar tabla TP correcta.
- **Prueba de cierre:** cotejar los ocho pares tabla/dibujo de M1 p.19 y los ocho del TP E4; todas coincidencias dentro de cada convención, un bit en todo vecino circular. Una diferencia entre convenciones no se describe como contradicción dentro de la fuente.

### U04-A-002 — P2 pedagogía — corrección Q2 depende de otro archivo para su salida pedida

- **Ubicación:** `apuntes/repaso/u04-modulacion-multiplexacion.md`, corrección **U04-Q02**, **líneas60–61** (consigna líneas26–29).
- **Claim/ausencia:** la consigna requiere proponer diagrama y cuadro; la corrección lista fases 8PSK, pero remite al TP para ver el dibujo; 16PSK también remite para diagrama/tabla. No hay diagrama de estados autocontenido en esa corrección.
- **Evidencia:** CQ **Pregunta2.1** requiere diagrama+cuadro y su imagen los presenta; metodología **§3 regla3 «Ejemplos completos, no enlaces»** y regla2 «Mostrar la salida». Los resultados correspondientes existen y son correctos en TP E4/E5: no se denuncia ausencia global ni error de números.
- **Naturaleza:** **faltante local demostrado**, no error académico. La respuesta sigue utilizable navegando, pero no cumple autosuficiencia del ejemplo.
- **Impacto:** dificulta corregirse en el mismo recurso y puede dejar la salida pedida sin comparación visual directa.
- **Acción:** incorporar el diagrama8PSK y tabla correspondiente en corrección Q2; si se mantiene la repetición gráfica16, incluir SVG/tabla16 o delimitar explícitamente qué se repite. Conservar links como profundización, no como reemplazo de la salida.
- **Prueba de cierre:** leyendo sólo la corrección Q2 se puede contrastar cada punto/fase/etiqueta solicitada y verificar su Gray circular; no se requiere abrir TP para completar el ejemplo mínimo.

### U04-A-003 — P3 editorial/evidencia — notación BER citada con exponente inexistente

- **Ubicación:** mismo APUNTE, `#psk-qam`, **línea280**, y `#pendientes`, **línea757** (fila PSK/QAM).
- **Claim:** la fuente «se imprime `16^-6 (VER1)`».
- **Evidencia:** V **p.1**, inspección individual `u04-a/V-1.png`: la fila imprime **`BER = 16-6 (VER 1)`**, con todos los caracteres en la línea base; no aparece un exponente -6 ni el símbolo `^`.
- **Naturaleza:** **transcripción editorial inexacta demostrada**. El candidato acierta en NO utilizarlo como umbral universal: no se encontró un cálculo BER erróneo derivado de esto.
- **Impacto:** el lector puede interpretar una potencia donde el original sólo contiene notación corrupta/ambigua; deteriora fidelidad del registro de pendiente.
- **Acción:** transcribir literalmente `16-6 (VER 1)` y conservar su carácter dudoso; no corregir a10^-6 sin evidencia.
- **Prueba de cierre:** texto del pendiente fiel al facsímil, incertidumbre explícita y ningún ejercicio que presuponga un BER numérico confirmado.

## 8. Límites, fuera de alcance y decisión final

- **No muestreo presentado como integral:** se visitaron 104 páginas PDF y las 69 imágenes. El contraste es integral del **corpus U4 asignado**, no de toda bibliografía/U1–U6 ni de futuros temas U7/U8.
- La promoción a revisado sigue bloqueada por los pendientes materiales registrados (sensibilidad FM, criterio FSK, condición BER, simplificación μ y absolutos WDM/CDM). Que estén declarados y no se evalúen como confirmados es correcto; no los conté como errores adicionales del candidato ni los resolví inventando datos.
- V tiene banda normalizada redondeada leída y contrastada, no desarrollada como nuevo ejercicio por falta de contexto BER/detector; no se usó su S/N para cálculo de rendimiento. TCM/OQPSK/PM se verificaron al nivel registrado, sin traer protocolos/algoritmos nuevos.
- No probé un motor Mermaid/Markdown ni render de navegador del SVG. Sí revisé estructura semántica y toda geometría, y vi render de sus primitives; límite de tipografía/render UI explícito.
- Las pruebas de enlaces son existencia/anclas, no revisión sustantiva de contenido de unidades enlazadas. Registro de imágenes sólo existencia, trazabilidad reconstruida propia.

**Cierre:** corregir **U04-A-001**; atender autosuficiencia **002** y literalidad **003**. Luego repetir pruebas de cierre específicas y conservar estado honesto hasta que las dudas materiales tengan evidencia suficiente. No hay error de tasa, unidad o resultado demostrado en E1–10/Q1–4. Candidatos/originales/caches preservados: 401 hashes coincidentes.

## Key Learnings:

1. El mapeo8PSK de M1 p.19 y su diagrama coinciden; la diferencia real es entre M1/C5 y CP/P, no dentro de la misma filmina.
2. Una fuente de parámetros con BER tipográficamente ambiguo no respalda un umbral numérico: se conserva el literal y su incertidumbre.
3. La trazabilidad gráfica independiente puede reconstruirse por SHA-256 más inspección visual sin leer certificaciones autorales.


---

## Dictamen B

# Revisión pedagógica independiente U4 — B

Fecha: 2026-10-13. Alcance: `APUNTE.md`, `INDICE.md`, TP4 E1–E10, repaso Q1–Q4; capturas de clase 5, clase 6, clase 6.2 completa, práctica 6 y cuestionario; siete PDF originales de U4 y sus caches disponibles. Revisión de contenido, enseñanza, cálculos, unidades, figuras, enlaces y trazabilidad. No se modificó contenido de estudio, originales ni caches.

## Snapshot e integridad

- `docs/consolidacion-u1-u6/snapshot-inicial.json`: 401 entradas; SHA-256 cotejados antes y después; 0 faltantes y 0 cambios.
- Informe propio: `tmp/reviews/u04-b.md`.
- Sólo se renderizaron copias de inspección propias bajo `tmp/reviews/u04-b/render/`; originales intactos.

## Cobertura efectivamente revisada

- Teoría: lectura de las 18 secciones de `APUNTE.md` (líneas 1–798), todas las filas del mapa de procedencia, pendientes y estado; 4 secciones del `INDICE.md` (líneas 1–12). Revisadas las 14 figuras enlazadas en `recursos/` y consistencia con sus referencias/registro de imágenes.
- Práctica: E1–E10, herramientas comunes y autocontrol, líneas 1–216; contraste con TP original, 3 páginas, y respuestas, 4 páginas.
- Repaso: Q1–Q4 y correcciones, líneas 1–78; contraste completo con captura y gráfico de respuesta Q2.
- Capturas: clase 5 (248 líneas), clase 6 (121), clase 6.2 (906; MUX/QoS, FDM/OFDM, TDM/E1/T1, PDH/SDH/SONET, STDM/WDM/CDM), práctica 6 (669; E1–E10), cuestionario Q1–Q4. Leídas de punta a punta para mapear destinos y discrepancias; no se tomaron como autoridad factual por sí solas.
- Originales PDF inspeccionados visualmente página por página en hojas de contacto (revisión detallada del texto/cache y ampliación de páginas con figuras/cálculos relevantes): `U4 MODULACION 1.pdf` pp.1–27; `U4 MODULACION 2.pdf` pp.1–13; `U4 MULTIPLEXACION.pdf` pp.1–36; `UT 4 MODULACION Y MULTIPLEXACION.pdf` pp.1–20; `U 4 - PARAMETROS...pdf` p.1; `EXPRESIONES Y RTAS...pdf` pp.1–4; `TP 4 2026.pdf` pp.1–3. Caches correspondientes existentes para las siete fuentes; no se generaron ni alteraron.

## Mapa de fragmentos originales → destino y tratamiento

- C5 + M1 pp.2–27 + P pp.2–14: conceptos de modulación, AM/FM/ASK/FSK/PSK/QAM, Gray, constelaciones, variantes y ruido → §§1–5 y TP E2–E8; errores del material (portadora/señal resultante, mapeo Gray, sensibilidad y tabla BER dudosa) corregidos o anotados como pendientes.
- C5/CP + M2 pp.2–13: PAM/PDM/PPM, PCM, cuantificación/compansión, A/μ, DM/ADM/DPCM → §§6–8; TP E1/E7 y repaso Q3/Q4; diferencia entre ruido de cuantización y multiplexación aclarada.
- C62/CP + X pp.2–36 + P pp.15–20: MUX, FDM/OFDM, TDM, E1/T1, PDH, SDH/SONET, STDM, WDM/CDM/acceso → §§9–14 y E9–E10; valores redondeados o afirmaciones absolutas contrastados, no universalizados.
- TP4 pp.2–3 + respuestas pp.1–4 + CP: enunciados E1–E10 → TP E1–E10; E1 PCM, 16/8-PSK, Gray, Carson y E9/E10 recalculados/contrastados.
- CQ Q1–Q4 + figura original → repaso Q1–Q4; conserva IDs, corrección separada, no asume clave universal para Q4.

## QA independiente

- Recalculados: 125 μs→8000 muestras/s; 128/256 niveles→56/64 kbit/s; separaciones 16/8-PSK; tasas 14,4/19,2 kbit/s a 4800 baudios; 9600/2400→16 estados; FM 2,02 MHz; ejemplos FDM/TDM/STDM; E1 2,048 Mbit/s; T1 1,544 Mbit/s; períodos PDH de tabla; STM-1 155,52 Mbit/s; ejemplo CDM.
- Las etiquetas Gray 8-/16-PSK cierran con distancia de Hamming 1; gráfico fuente C5 difiere de su tabla y el apunte identifica que no se mezclan.
- Las 14 figuras registradas se cotejaron visualmente; las cifras potencialmente engañosas del diagrama E1/PDH y las curvas PSK/QAM quedan explicadas/condicionadas. Sin discrepancia gráfica adicional demostrada.
- Revisados enlaces Markdown relativos y anclas en los cuatro artefactos: sin enlaces internos rotos.
- Las cuestiones μ-law, criterio FSK angosta/ancha, BER, sensibilidades FM y absolutos WDM/CDM están registradas como pendientes y no se presentan como conocimiento confirmado.

## Issues

### U04-B-001 — P2 pedagogía/cobertura — formalizar PM o acotar su objetivo de examen

- **Ubicación:** `apuntes/teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md:151–188`, en particular 155–156 y 182–188.
- **Afirmación/observación:** la sección distingue correctamente FM de PM y da un ejemplo conceptual de mensaje constante, pero su formalización sólo presenta la ecuación e índice de FM; no explica cómo la fase se aparta según el mensaje ni ofrece un ejemplo PM propio. La cobertura del mapa la incluye junto a FM como “básico”.
- **Evidencia:** alcance del programa U4 incluye AM/FM/PM; captura `capturas/teoria/04-modulacion-digitalizacion-multiplexacion/clase 5.md` líneas 87 y 227, y M1 PDF p.6 enumera amplitud/frecuencia/fase como parámetros modificables. En el corpus revisado no encontré un modelo PM específico que permita atribuir una fórmula/ejemplo a la cátedra.
- **Naturaleza:** faltante pedagógico demostrado; no es error técnico demostrado ni se afirma que el material de cátedra contenga la ecuación ausente.
- **Impacto:** el lector puede recitar “PM cambia fase” y distinguir el ejemplo estático, pero no explicar con precisión cómo se codifica una moduladora variable; queda menos preparada que AM/FM una familia expresamente listada en el programa.
- **Acción/prueba de cierre:** o bien precisar en mapa/“Para examen” que PM se exige sólo como definición/clasificación por falta de desarrollo fuente, o completar con explicación y ejemplo de fase contra moduladora respaldados por bibliografía obligatoria/norma dentro del alcance. Verificar que el agregado diferencie fase instantánea de frecuencia instantánea y cite fuente.

## Veredicto

Buen candidato en-progreso, integralmente trazable y pedagógicamente sólido en la mayoría de la unidad; discrepancias y cuentas principales tratadas con prudencia. No encontré P0 ni P1 demostrados. Un faltante P2 acotado para PM impide recomendar “revisado” sin decisión pedagógica; mantener `en-progreso` hasta resolverlo y completar el circuito de revisiones independientes previsto. No hubo correcciones ni build.
