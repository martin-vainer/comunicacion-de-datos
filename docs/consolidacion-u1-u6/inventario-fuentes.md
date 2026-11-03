# Inventario operativo de fuentes — consolidación U1–U6

**Fecha:** 2026-10-10 (America/Buenos_Aires). **Estado:** preparación de fuentes; NO certifica unidades revisadas.

## Alcance y ownership

La agrupación por unidades de las tablas sólo organiza fuentes; la asignación exclusiva por ruta está en [estado de ejecución](estado.md#propiedad-de-escritura).

- Sólo contenido registrado en capturas y material específico U1–U6. La bibliografía sirve para contrastar/aclarar, nunca para abrir temas.
- Originales y 12 caches históricos preservados byte a byte. No se modificaron capturas, APUNTE, README ni bitácora. Se crearon 27 caches nuevos; total 39 `.txt`.
- Curador: caches nuevos e inventario. Autor U1–U2: sus APUNTE/INDICE/práctica/repaso. Autor U3–U4: sus destinos. Autor U5–U6: sus destinos. Root coordina archivos compartidos y verificación.
- Teoría → un APUNTE canónico por unidad; soluciones → apuntes/practica; cuestionarios → apuntes/repaso. El ownership por SECCIÓN debe completarlo cada autor, sin editar esta evidencia original.

## Entorno y alcance visual real

- pypdf 6.14.2 instalado en Python bundled; pdftoppm Poppler funcional. No pdftotext en PATH ni en Poppler bin; no se instaló nada.
- Nuevos caches UTF-8 incluyen original, título, páginas, SHA-256, extractor y delimitación por página PDF; no OCR. El cache no prueba fidelidad de fórmulas/figuras.
- Muestras renderizadas E INSPECCIONADAS: TP6 primera parte p. PDF 2 (seis ejercicios), U6 p. PDF 28 (división CRC), Castro/Fusario p. PDF 4 (edición 2013). Sólo esas páginas; las demás permanecen pendientes visuales.
- Poppler emitió advertencias de fuentes Symbol/ArialUnicode al renderizar libro; el cotejo de fórmulas sigue siendo individual. Los renders están en tmp/curador-ejecucion y son auxiliares, no fuentes.

## Bloqueos y prioridades concretas

1. U5: no hay PDF teórico U5 en material. Captura del 01/10 y TP5 existen; libro extracto confirma información/entropía/tasa, pero no respalda por sí solo todas las tablas/características de códigos. Registrar pendientes donde falte contraste bibliográfico original; no inventar la filmina faltante.
2. Solución personal raíz `Martín Vainer - Comunicación de Datos.pdf`: sus 3 páginas carecen de texto; `material/practica/Martín Vainer - CD.pdf` pp. 4–6 también. Cache existe pero no sirve para leer solución: inspeccionar original visualmente antes de integrar.
3. U2: respuestas Fourier p.2, esquemas de codificación pp.2–3 y distintas filminas son gráficas; usar original para convención HDB3/Manchester y amplitudes, no inferir desde texto roto.
4. U3/U4: tablas, constelaciones, tramas y diagramas contienen gráficos poco extraíbles; autores deben renderizar páginas de sus secciones.
5. U6: hay TP6 en dos partes; no se afirma resuelto. El ejercicio CRC p.28 requiere cotejo de XOR; inspección visual hecha, pero no recalculada aquí. Mantener método/cuentas para el autor/verificador.

## Fuentes listas para búsqueda y redacción condicionada al contraste

| Unidad / destino | Original (ruta actual) | Cache | Páginas PDF | Visual / páginas con poco texto |
|---|---|---|---|---|
| Marco U1–U6 | `material/catedra/Programa comunicacion de datos Año 2026 - martes jueves 2do cuat K3673.pdf` | `material/_cache/cronograma-comunicacion-de-datos-2026-k3673.txt` (histórico) | 2 | Pendiente integral |
| U2/U3: cuestionario | `Ejercicio cuestionario 10-09-2026.pdf` | `material/_cache/ejercicio-cuestionario-2026-09-10.txt` (histórico) | 3 | Pendiente integral |
| Marco U1–U6 | `material/catedra/PROGRAMA de la materia.pdf` | `material/_cache/programa-analitico-comunicacion-de-datos.txt` (histórico) | 7 | Pendiente integral; poco texto: 7 |
| U1 | `material/practica/U 1/TP 1  2026.pdf` | `material/_cache/tp-01-2026-enunciado.txt` (histórico) | 3 | Pendiente integral |
| U1 | `material/practica/U 1/TP1-respuestas y resumen.pdf` | `material/_cache/tp-01-respuestas-y-resumen.txt` (histórico) | 3 | Pendiente integral |
| U2 | `material/practica/U 2/TP  2  2026.pdf` | `material/_cache/tp-02-2026.txt` (histórico) | 3 | Pendiente integral |
| U2/U3: práctica de enlace | `material/practica/TRABAJO PRACTICO  EJ 19 CALCULO ENLACE.pdf` | `material/_cache/trabajo-practico-ej-19-calculo-enlace.txt` (histórico) | 3 | Pendiente integral |
| U1 | `material/practica/U 1/UT 1 COMUNICACIONES.pdf` | `material/_cache/u1-introduccion-a-la-teleinformatica.txt` (histórico) | 10 | Pendiente integral; poco texto: 1,2,5,6,7,10 |
| U1 | `material/teoria/U1/U1 Introduccion a las comunicaciones.pdf` | `material/_cache/u1-introduccion-a-las-comunicaciones.txt` (histórico) | 25 | Pendiente integral; poco texto: 2,7,8,22 |
| U1 | `material/practica/U 1/Organismos  UT 1.pdf` | `material/_cache/u1-organismos-de-comunicaciones.txt` (histórico) | 3 | Pendiente integral |
| U2 | `material/teoria/U2/U 2 Características de las señales de telecom.pdf` | `material/_cache/u2-caracteristicas-senales-telecom.txt` (histórico) | 48 | Pendiente integral; poco texto: 6,13,18,19,20,21,23,29,33,34,36,37,38,43,44,45,46,48 |
| U6 | `material/teoria/U6/U 6 Canales de Comunicaciones y control de errores.pdf` | `material/_cache/u6-canales-comunicaciones-control-errores.txt` (histórico) | 38 | Pendiente integral; muestra p.28 inspeccionada; poco texto: 17,18,22,23,24,25,26,28,29,30,37,38 |
| U2/U3: práctica de enlace | `Martín Vainer - Comunicación de Datos.pdf` | `material/_cache/calculo-enlace-vainer-raiz-resolucion.txt` (nuevo) | 3 | Pendiente integral; poco texto: 1,2,3 |
| U2/U3: práctica de enlace | `material/practica/Martín Vainer - CD.pdf` | `material/_cache/martin-vainer-cd.txt` (nuevo) | 6 | Pendiente integral; poco texto: 4,5,6 |
| U2 | `material/practica/U 2/EXPRESIONES  Y RTAS UD 2 2DA PARTE.pdf` | `material/_cache/u2-expresiones-y-rtas-ud-2-2da-parte.txt` (nuevo) | 4 | Pendiente integral; poco texto: 2 |
| U2 | `material/practica/U 2/EXPRESIONES Y RTAS  UD 2 1RA PARTE.pdf` | `material/_cache/u2-expresiones-y-rtas-ud-2-1ra-parte.txt` (nuevo) | 1 | Pendiente integral |
| U2 | `material/practica/U 2/UT 2 CODIFICACION - DIST CODIGOS.pdf` | `material/_cache/u2-ut-2-codificacion-dist-codigos.txt` (nuevo) | 3 | Pendiente integral; poco texto: 2,3 |
| U2 | `material/practica/U 2/UT 2 Códigos de línea cuadro comparativo.pdf` | `material/_cache/u2-ut-2-codigos-de-linea-cuadro-comparativo.txt` (nuevo) | 3 | Pendiente integral |
| U2 | `material/practica/U 2/UT 2 SEÑALES TELCOM-CODIGOS DE LINEA.pdf` | `material/_cache/u2-ut-2-senales-telcom-codigos-de-linea.txt` (nuevo) | 17 | Pendiente integral; poco texto: 1,4,6,9,11,13,16,17 |
| U3 | `material/practica/U 3/EXPRESIONES  Y RTAS UD NRO 3 (1ra PARTE).pdf` | `material/_cache/u3-expresiones-y-rtas-ud-nro-3-1ra-parte.txt` (nuevo) | 3 | Pendiente integral |
| U3 | `material/practica/U 3/EXPRESIONES  Y RTAS UD NRO 3 (2da PARTE).pdf` | `material/_cache/u3-expresiones-y-rtas-ud-nro-3-2da-parte.txt` (nuevo) | 5 | Pendiente integral |
| U3 | `material/practica/U 3/TP   3   2026.pdf` | `material/_cache/u3-tp-3-2026.txt` (nuevo) | 4 | Pendiente integral |
| U3 | `material/practica/U 3/UT 3 MEDIDA VELOCIDAD.pdf` | `material/_cache/u3-ut-3-medida-velocidad.txt` (nuevo) | 17 | Pendiente integral; poco texto: 1,4,9,10,11,12,14,15,16,17 |
| U4 | `material/practica/U 4/EXPRESIONES  Y RTAS UNIDAD  TEMATICA NRO 4.pdf` | `material/_cache/u4-expresiones-y-rtas-unidad-tematica-nro-4.txt` (nuevo) | 4 | Pendiente integral |
| U4 | `material/practica/U 4/TP 4  2026.pdf` | `material/_cache/u4-tp-4-2026.txt` (nuevo) | 3 | Pendiente integral |
| U4 | `material/practica/U 4/U 4 - PARAMETROS PRINCIPALES DE  LOS DIFERENTES METODOS DE MODULACION.pdf` | `material/_cache/u4-u-4-parametros-principales-de-los-diferentes-metodos-de-modulacion.txt` (nuevo) | 1 | Pendiente integral; poco texto: 1 |
| U4 | `material/practica/U 4/UT 4 MODULACION Y MULTIPLEXACION.pdf` | `material/_cache/u4-ut-4-modulacion-y-multiplexacion.txt` (nuevo) | 20 | Pendiente integral; poco texto: 1,4,6,11,13,18,20 |
| U5 | `material/practica/U 5/TP  5  2026.pdf` | `material/_cache/u5-tp-5-2026.txt` (nuevo) | 3 | Pendiente integral |
| U6 | `material/practica/U6/TP   6   (2da parte)  2026.pdf` | `material/_cache/u6-tp-6-2da-parte-2026.txt` (nuevo) | 3 | Pendiente integral |
| U6 | `material/practica/U6/TP  6 (1ra parte)    2026.pdf` | `material/_cache/u6-tp-6-1ra-parte-2026.txt` (nuevo) | 2 | Pendiente integral; muestra p.2 inspeccionada |
| U2 | `material/teoria/U2/Señales Banda Base.pdf` | `material/_cache/u2-senales-banda-base.txt` (nuevo) | 33 | Pendiente integral; poco texto: 1,3,5,7,24,27,28,29 |
| U3 | `material/teoria/U3/U3 Redes de Telecomunicaciones.pdf` | `material/_cache/u3-u3-redes-de-telecomunicaciones.txt` (nuevo) | 28 | Pendiente integral; poco texto: 6,7,8,16,21,23,24 |
| U4 | `material/teoria/U4/U4 MODULACION 1.pdf` | `material/_cache/u4-u4-modulacion-1.txt` (nuevo) | 27 | Pendiente integral; poco texto: 7,9,10,11,13,14,15,16,18,21,22,23 |
| U4 | `material/teoria/U4/U4 MODULACION 2.pdf` | `material/_cache/u4-u4-modulacion-2.txt` (nuevo) | 13 | Pendiente integral; poco texto: 2,4,7,8,11,12 |
| U4 | `material/teoria/U4/U4 MULTIPLEXACION.pdf` | `material/_cache/u4-u4-multiplexacion.txt` (nuevo) | 36 | Pendiente integral; poco texto: 4,7,8,9,10,12,17,18,20,21,25,27,32,33,34,36 |
| U1–U6 | `material/teoria/DOC-20230425-WA0040.pdf` | `material/_cache/castro-fusario-2013-u1-sistemas-internet-osi-extracto.txt` (nuevo) | 726; extracto 3–4, 48–49, 66–89, 167–173, 276–283 | Pendiente integral; ficha p.4 inspeccionada |
| U1–U6 | `material/teoria/DOC-20230425-WA0040.pdf` | `material/_cache/castro-fusario-2013-u2-fourier-db-banda-base-extracto.txt` (nuevo) | 726; extracto 98–121, 124–129, 134–159 | Pendiente integral; ficha p.4 inspeccionada |
| U1–U6 | `material/teoria/DOC-20230425-WA0040.pdf` | `material/_cache/castro-fusario-2013-u5-informacion-entropia-extracto.txt` (nuevo) | 726; extracto 202–212 | Pendiente integral; ficha p.4 inspeccionada |
| U1–U6 | `material/teoria/DOC-20230425-WA0040.pdf` | `material/_cache/castro-fusario-2013-u6-canales-errores-extracto.txt` (nuevo) | 726; extracto 194–202, 212–248 | Pendiente integral; ficha p.4 inspeccionada |

## Trazabilidad de caches históricos

Los SHA-256 de fuente de los caches que los declaran se compararon contra TODOS los PDFs actuales (material y raíz). Los restantes se asociaron por contenido/ruta: tienen hash ACTUAL registrado, no una certificación retrospectiva de bytes fuente.

| Cache histórico | Vínculo fuente actual | SHA-256 fuente actual | SHA-256 cache preservado |
|---|---|---|---|
| `material/_cache/cronograma-comunicacion-de-datos-2026-k3673.txt` | correspondencia por contenido/ruta; cache histórico sin hash de fuente, no prueba criptográfica retrospectiva; `material/catedra/Programa comunicacion de datos Año 2026 - martes jueves 2do cuat K3673.pdf` | `ea4fb228edc9fbde1515a9168f296b1fb87d12ed7e23ef56d321e02b56e4f438` | `6252d8f777e5759bf3e3e23b945986e64862e67426331d271801453e54a62c9b` |
| `material/_cache/ejercicio-cuestionario-2026-09-10.txt` | SHA-256 declarado en cache y verificado contra original actual; `Ejercicio cuestionario 10-09-2026.pdf` | `01562d496b527ca4f91d8c64fdf835896d6f4ae340c32f0b1f9365b7c886ab53` | `5ab605e385df7153474f1d79d7910da4097d93c169ff41c7f3b32399055dcbe7` |
| `material/_cache/programa-analitico-comunicacion-de-datos.txt` | correspondencia por contenido/ruta; cache histórico sin hash de fuente, no prueba criptográfica retrospectiva; `material/catedra/PROGRAMA de la materia.pdf` | `516b95c28e17602e9c656536bd43f1e9ac27433847b5cd9eb72818387a6d986e` | `b1ebb0a6d85b67a0ea7580e836bdf9d4e13c37d5c42509ccfec36bdf005d09c5` |
| `material/_cache/tp-01-2026-enunciado.txt` | correspondencia por contenido/ruta; cache histórico sin hash de fuente, no prueba criptográfica retrospectiva; `material/practica/U 1/TP 1  2026.pdf` | `4e3ae55c0190373a945e2b88e462f67e1b3a01a1f52ab7536ba0fc0aa4fb0cb7` | `d00fc44a067341f7744b0a2d0d4c068f24dde250098e9148ad57a2a0c62448f1` |
| `material/_cache/tp-01-respuestas-y-resumen.txt` | correspondencia por contenido/ruta; cache histórico sin hash de fuente, no prueba criptográfica retrospectiva; `material/practica/U 1/TP1-respuestas y resumen.pdf` | `8c7abcecda62e03d4f77a3b562647aa7454011127b61fe070a415fc436291dc7` | `c7cfe5dcb2db40f2b719707fd914ce9e2e65f083b5c9ceab6dbb4b49666144ec` |
| `material/_cache/tp-02-2026.txt` | SHA-256 declarado en cache y verificado contra original actual; `material/practica/U 2/TP  2  2026.pdf` | `52f907d3c4881c34434be1ca8dcf18468afdae6fab86fcff26b02056a4f2e247` | `67a151757328afc415e4b8b928dc4468265fc1a357e5da1ef414020f6afa37a8` |
| `material/_cache/trabajo-practico-ej-19-calculo-enlace.txt` | correspondencia por contenido/ruta; cache histórico sin hash de fuente, no prueba criptográfica retrospectiva; `material/practica/TRABAJO PRACTICO  EJ 19 CALCULO ENLACE.pdf` | `09625607fc69503bb58cb0cf1e854ed28679f35131d8b9c91cae5db58415572c` | `c0da99209a4d2cd6e5639f691d7557e7bf5d0fa2e4ce5ef5b92caf5ceff3b0ce` |
| `material/_cache/u1-introduccion-a-la-teleinformatica.txt` | correspondencia por contenido/ruta; cache histórico sin hash de fuente, no prueba criptográfica retrospectiva; `material/practica/U 1/UT 1 COMUNICACIONES.pdf` | `144a805a73d241ecb9810163281b13b3b9dcb0a167895514a37ed195f6152969` | `2d174374c739032ea1fe15c82db12a2d0166b610b289b4ce5b4a37f1a1e2a8dc` |
| `material/_cache/u1-introduccion-a-las-comunicaciones.txt` | correspondencia por contenido/ruta; cache histórico sin hash de fuente, no prueba criptográfica retrospectiva; `material/teoria/U1/U1 Introduccion a las comunicaciones.pdf` | `e10b8175bc2a6093d62e4a7a9e1dbdc76e594d57f2ed5551bf717d01eb15b25b` | `d569ee0f739118fdd3abc7566550bd5b3935465a82667a8c7983099a7610f055` |
| `material/_cache/u1-organismos-de-comunicaciones.txt` | correspondencia por contenido/ruta; cache histórico sin hash de fuente, no prueba criptográfica retrospectiva; `material/practica/U 1/Organismos  UT 1.pdf` | `04888473c04ca218ac1abd8e8b543e7f54202106a09b9010a68030d518d33e37` | `52634f1194216acc722961ba2b1d8ca91359a73d4d47b65f665ad7b163c873f4` |
| `material/_cache/u2-caracteristicas-senales-telecom.txt` | SHA-256 declarado en cache y verificado contra original actual; `material/teoria/U2/U 2 Características de las señales de telecom.pdf` | `2df3d853f92b76da06a4a3e01bf3d701ad5e7ed2a4537d56d64c9ae5554037f2` | `8bfb94b15ed870f80e346a6b9c3edc9b61da0138584a63c2d4990c0a326dd4a2` |
| `material/_cache/u6-canales-comunicaciones-control-errores.txt` | correspondencia por contenido/ruta; cache histórico sin hash de fuente, no prueba criptográfica retrospectiva; `material/teoria/U6/U 6 Canales de Comunicaciones y control de errores.pdf` | `3e4dc09b027b9d9c43df662a29cba26e3f605133a24e1973e4ffaffcaf30c233` | `d85b00b9a890c5b40046b207aa0be3643930659214b4644545d45f809792e344` |

**Ruta vieja trazada por hash:** `tp-02-2026.txt` declara `material/practica/TP  2  2026.pdf`; su fuente actual verificada es `material/practica/U 2/TP  2  2026.pdf`. `ejercicio-cuestionario-2026-09-10.txt` coincide por hash con el PDF existente en raíz; no falta fuente ni se duplicó cache.

## Mapa de capturas por archivo y encabezados principales

Los encabezados se conservan tal como están escritos; NO son afirmaciones verificadas. Los subencabezados detallados se consultan en el original. Capturas mixtas alimentan distintas unidades sin moverse.

| Captura original | Encabezados principales (h1/h2) | Destino / ownership propuesto |
|---|---|---|
| `capturas/practica/clase 01.md` | teleinformatica:; transmision de datos:; esquema de comunicaciones:; esquema basico de telecomunicaciones:; circuito teleinformatico basico:; modelo simplificado de la comunicacion de datos- canal analogico:; otras fomras de comuniacion - canal digital:; redes de comunicaciones:; internet: red de redes.; modelo OSI: interconexión de sistemas abiertos.; TP1:; expresiones matematicas:; tp1: | U1 teoría + TP1 práctica → autor U1–U2; matemática eléctrica sólo práctica |
| `capturas/practica/clase 02.md` | señales analógias y digitales; TP 2 (primera parte): | U2 teoría + TP2 práctica → autor U1–U2 |
| `capturas/practica/clase 03.md` | Clase 03:; medidas de la velocidad:; relacion entre velocidades:; señales periodicas:; formas de representacion series de fourier: | Velocidades U3 → autor U3–U4; Fourier U2 → autor U1–U2 |
| `capturas/practica/clase 04.md` | Clase 04:; repaso: medidas de la velocidad:; sincronismo:; unidades de transimicion(DB); unidades de transmision:; calculo de enclace: Balance de enlace; ejercicios: TRABAJO PRÁCTICO N°3; Ejercicio 19 — TP: cálculo de enlace con amplificador | Velocidades/sincronismo y TP3/enlace U3 → autor U3–U4; dB/ancho de banda U2 → autor U1–U2; valores de medios sólo ejemplos registrados |
| `capturas/practica/Clase 05.md` | CUESTIONARIO UD Nro 3; Pregunta 1 – Velocidad de modulación y ancho de banda; Pregunta 2 – Velocidad real de transferencia de datos; Pregunta 3 – Unidad dBm; Pregunta 4 – Relación entre baudios y bps; Resumen rápido | U3 repaso → autor U3–U4; dBm enlaza U2 |
| `capturas/practica/clase 06.md` | UNIDAD 4:; MODULACIÓN; SEÑALES INTERVINIENTES; ESQUEMA BÁSICO DE MODULACIÓN; Metodos de modulacion; modulacion por onda continua; modulacion por pulsos; Clasificacion de las tecnicas de modulacion; 1. Modulación por onda continua; 2. Modulación por pulsos; Tipos de modulación; Modulación por onda continua; Portadora; Parámetros que pueden modificarse; Modulación AM — Modulación de Amplitud; Señal moduladora; Señal portadora; Señal modulada; Modulación AM - FM; Modulación de amplitud — AM; Modulación de frecuencia — FM; modulacion de fase - señal 2-psk / B-PSK; asiganación de secuencia de bits y de estados - DIAGRAMA DE FASES - modulacinon 4-PSK/Q-psk; construccion del codigo de gray; Modulación M-PSK; Separación entre fases; Cantidad de bits por símbolo; Relación entre velocidad de transmisión y velocidad de modulación; Ejemplo: 8-PSK; Asignación de bits y fases; Multiplexación; Tipos de técnicas de multiplexación:; TRABAJO PRÁCTICO N° 4 | U4 teoría + TP4 práctica → autor U3–U4 |
| `capturas/practica/clase_practica_1er_parcial.md` | - clase 22-09-2026 pre primer instancia del primer parcial | Sólo fecha 22/09; sin contenido académico que consolidar |
| `capturas/practica/practica_un5.md` | clase practica de 06-10-2026; contenido de clase de práctica; Trabajo Práctico N° 5; Teoría de la información y codificación | U5 teoría/práctica TP5 → autor U5–U6; soluciones registradas requieren recálculo |
| `capturas/teoria/01-introduccion-comunicaciones/Apuntes-clase 1.md` | U1: introduccion a las comunicaciones; circuito teleinformatico basico:; TRANSMISIÓN DE DATOS; la importancia de la normalización de las comunicaciones; MODELO de REFERENCIA OSI:; internet: red de redes.; interconexion de redes: | U1 teoría → autor U1–U2 |
| `capturas/teoria/02-senales-telecomunicaciones/apuntes-clase 2.md` | U2: caracteristicas de las Señales de telecomunicaciones; características de las; unidades de transmisión:; Amplificación y Atenuación; Definición de ancho de banda de una línea de transmisión usando dB; UNIDADES DE TRANSMISIÓN; Atenuaciones en medios de comunicaciones; SEÑALES DE COMUNICACIONES; parametros; serie de fourier | U2 teoría → autor U1–U2 |
| `capturas/teoria/02-senales-telecomunicaciones/apuntes-clase 4.md` | codigos de linea o banda base; Cuadro comparativo de códigos de línea; CÓDIGO 2B 1Q / 4B 3; ANÁLISIS ESPECTRAL DE CÓDIGOS; FILTROS | U2 teoría → autor U1–U2 |
| `capturas/teoria/02-senales-telecomunicaciones/apuntes-clase3.md` | ANCHO DE BANDA; TREN DE PULSOS RECTANGULARES; ONDAS ELECTROMAGNÉTICAS (OEM) | U2 teoría → autor U1–U2 |
| `capturas/teoria/03-redes-telecomunicaciones/apuntes-clase 4.md` | Medidas de la velocidad; Velocidad de modulación — Línea de Tx; Velocidad de transmisión (binaria) — Circuito de datos CD; Relación entre velocidades; Velocidad de transferencia de datos (Throughput) — Enlace de datos ED; Velocidad real de transferencia de datos — ED; Relación entre velocidades; Ancho de banda; Relación entre ancho de banda y velocidad de transmisión; Temas de transmisión de datos; Transmisión multinivel; Tipos de transmisión; Modos de transmisión; Sincronismo; Transmisión según sincronización | U3 teoría → autor U3–U4; cuestionario_U3 pregunta2 Fourier → U2 repaso autor U1–U2 |
| `capturas/teoria/03-redes-telecomunicaciones/apuntes-clase 5.md` | Transmisión / Protocolos; Protocolo asociado a una transmisión; Protocolo asincrónico; Tipos de sincronismo; Estructura general; Características del protocolo asincrónico; Protocolo sincrónico; Estructura general de un bloque; Características del protocolo sincrónico; Redes de Telecomunicaciones; Composición; Representación de una red; Redes; Punto a punto; Difusión multipunto; Red conmutada; Internet; Enlaces de comunicaciones; Tipos de enlaces; CUADRO COMPARATIVO: COSTOS VS VOLUMEN DE DATOS; Tipos de conmutación; Topologías de red; Malla; Estrella; Bus o lineal; Ring o anillo; Híbridas; Cuadro comparativo | U3 teoría → autor U3–U4; cuestionario_U3 pregunta2 Fourier → U2 repaso autor U1–U2 |
| `capturas/teoria/03-redes-telecomunicaciones/cuestionario_U3.md` | Cuestionario – Comunicación de Datos; Pregunta 1 – Velocidad de transferencia de un medio físico; Pregunta 2 – Tren de pulsos y espectro de Fourier; Pregunta 3 – Tipo de transmisión en radiodifusión; Resumen rápido | U3 teoría → autor U3–U4; cuestionario_U3 pregunta2 Fourier → U2 repaso autor U1–U2 |
| `capturas/teoria/04-modulacion-digitalizacion-multiplexacion/clase 5.md` | primera parte:; Modulación; Proceso de modulación; Señales involucradas; Esquema de una transmisión modulada:; Tipos de modulación; modulación por onda continua - modulacion en amplitud (AM); portadora:; am: moduladora; ASK:; VARIACION DE NIVEL DE PORTADORA; POR SUPRESION DE PORTADORA; ANCHO DE BANDA; FM; Señal modulada; Conclusiones:; FSK; ANCHO DE BANDA; PSK; SEÑAL 2-PSK / B-PSK; ASIGNACION DE SECUENCIA DE BITS Y DE ESTADOS; CONSTRUCCIÓN DEL CÓDIGO DE GRAY; MODULACION M-PSK; Modulación M-QAM; Modulación 16-QAM; Diagrama de estados o constelación; COMPARACIÓN DE MODULACIÓN   M-PSK / M-QAM; VARIANTES M-PSK; VARIANTES M-PSK; VARIANTES M-PSK o M-QAM; segunda parte:; MODULACION POR PULSOS ANALOGICA; DIGITALIZACION DE UNA SEÑAL ANALOGICA | U4 teoría → autor U3–U4 (incluye multiplexación registrada; no desarrollar medios U7) |
| `capturas/teoria/04-modulacion-digitalizacion-multiplexacion/clase 6.2.md` | Multiplexación; Multiplexación; Multiplexación — Características; Multiplexación: Voz / Datos; Técnicas de multiplexación; FDM — Multiplexación por División de Frecuencia; OFDM — Multiplexación por División de Frecuencia Ortogonal; TDM — Multiplexación por División de Tiempo; Armado de tramas TDM; TDM aplicado a señales PCM; PCM 30 — Esquema E1 - LEY A; PCM 24 — Esquema T1 - LEY mu; Comparación E1 vs T1; Concepto clave; Órdenes superiores de multiplexación TDM; Jerarquía PDH europea; Formación de los distintos órdenes; ¿Por qué la velocidad no es simplemente 4 veces la anterior?; Concepto clave de PDH; Órdenes superiores de multiplexación TDM; SDH — Jerarquía Digital Síncrona; Características principales de SDH; Principal diferencia respecto de PDH; Equipos Add-Drop; SDH y SONET; Equivalencias principales; Trama SDH — STM-1; Estructura simplificada de una trama STM-1; Tramas STM-N; Contenedores Virtuales — VC; Tipos de Contenedores Virtuales; SDH vs. PDH; Concepto clave; STDM — Multiplexación Estadística por División de Tiempo; TDM vs. STDM; WDM — Multiplexación por División de Longitud de Onda; Principio de funcionamiento; Características principales de WDM; Capacidad total; DWDM — Dense Wavelength Division Multiplexing; WDM vs. SDH/SONET; Equipamiento WDM; Comparación FDM y WDM; Conceptos clave; CWDM y DWDM; CDM — Multiplexación por División de Código; Multiplexación como método de acceso múltiple | U4 teoría → autor U3–U4 (incluye multiplexación registrada; no desarrollar medios U7) |
| `capturas/teoria/04-modulacion-digitalizacion-multiplexacion/Clase 6.md` | modulacion parte 2.; TIPOS DE CUANTIFICACIÓN; leyes de cuantificación; MODULACIÓN POR PULSOS DIGITAL; Digitalización para PCM; Modulación Delta (DM); Modulacion DELTA ADAPTATIVA (ADM); Modulacion PCM DIFERENCIAL (DPCM) | U4 teoría → autor U3–U4 (incluye multiplexación registrada; no desarrollar medios U7) |
| `capturas/teoria/05-Teoría de la información y de la codificación/01_10_26_U5.md` | Comunicación de Datos; Unidad 5: Teoría de la información y de la codificación; 1. Idea general de la teoría de la información; 2. Medida de la información; 3. Unidades de información; 4. Fuente binaria equiprobable; 5. Entropía; 6. Propiedades matemáticas de la entropía; 7. Entropía de una fuente binaria de memoria nula; 8. Tasa de información de la fuente; 9. Resumen para estudiar; Continuación: teoría de la codificación; 10. Teoría de la codificación; 11. Clasificación de los códigos; 12. Propiedades de los códigos; 13. Código o algoritmo de Huffman; 14. Código Morse; 15. Código Baudot e ITA N.º 2; 16. Decimal codificado en binario: BCD; 17. FIELDATA; 18. ASCII de 7 bits; 19. PC-8 o ASCII extendido de 8 bits; 20. EBCDIC de 8 bits; 21. Comparación de los códigos vistos; 22. Resumen para estudiar | U5 teoría → autor U5–U6 |
| `capturas/teoria/06-Canales de comunicaciones/08_10_2026.md` | Clase del 08/10/2026 — U6: Canales de comunicaciones y control de errores; Cómo leer esta clase; 1. Canales de comunicaciones; 2. Capacidad de un canal; 3. Nyquist y Hartley: canal sin ruido; 4. Uso de la medida de la información: niveles y bits; 5. Shannon-Hartley: el ruido limita la capacidad; 6. Fenómenos que afectan al canal; 7. Atenuación; 8. Tipos de ruido; 9. Factor de ruido de amplificadores o canales; 10. Distorsión y ecualización; 11. Tasa de error: BER; 12. Efecto del ancho de banda sobre una señal digital; 13. Interferencia intersímbolos, ISI; 14. Detección y corrección: redundancia y compromisos; 15. Paridad par, impar, longitudinal y bidimensional; 16. Paridad cíclica o entrelazada; 17. Chequeo de redundancia cíclica: CRC; 18. Checksum; 19. Corrección hacia atrás: ARQ; 20. ARQ Stop and Wait: parar y esperar; 21. ARQ Sliding Windows: ventana deslizante; 22. Corrección hacia adelante: FEC; 23. Códigos autocorrectores y Hamming; Aclaraciones del material y límites de este desarrollo; Resumen mental; Anexo — Las 38 láminas originales, sin modificar su contenido | U6 teoría → autor U5–U6 |
| `capturas/teoria/Cuestionarios/cuestionario - modulacion y multiplexacion.md` | Cuestionario – Modulación y Multiplexión; Pregunta 1 – Tipo de modulación según el parámetro de la portadora; Pregunta 2 – PSK, velocidad de transmisión y probabilidad de error; Pregunta 3 – Digitalización de señales analógicas; Pregunta 4 – Ruido granular y multiplexión | U4 repaso → autor U3–U4 |
| `capturas/teoria/Cuestionarios/cuestionario U1 y U2.md` | Cuestionario – Comunicación de Datos; Pregunta 1 – Circuito Teleinformático Básico; Pregunta 2 – Modelo OSI; Pregunta 3 – Modelo OSI; Pregunta 4 – Analizador de espectro; Pregunta 5 – Códigos de línea; Pregunta 6 – Código de línea y componente continua; Pregunta 7 – Respuesta en frecuencia de un canal; Recordatorios rápidos | U1 y U2 repaso → autor U1–U2 |

## Anexos, fuentes no PDF y complementos no abiertos

| Original / conjunto | Uso permitido y estado |
|---|---|
| `capturas/practica`: `image-1.png`, `image-10.png`, `image-11.png`, `image-12.png`, `image-13.png`, `image-14.png`, `image-15.png`, `image-16.png`, `image-17.png`, `image-18.png`, `image-19.png`, `image-2.png`, `image-20.png`, `image-21.png`, `image-22.png`, `image-23.png`, `image-24.png`, `image-25.png`, `image-26.png`, `image-27.png`, `image-28.png`, `image-29.png`, `image-3.png`, `image-30.png`, `image-31.png`, `image-32.png`, `image-33.png`, `image-34.png`, `image-35.png`, `image-36.png`, `image-37.png`, `image-38.png`, `image-39.png`, `image-4.png`, `image-40.png`, `image-41.png`, `image-42.png`, `image-43.png`, `image-44.png`, `image-5.png`, `image-6.png`, `image-7.png`, `image-8.png`, `image-9.png`, `image.png` | Anexos originales inmutables; propiedad del autor de captura, visual pendiente salvo muestra explícita. No se mueven. |
| `capturas/teoria/02-senales-telecomunicaciones`: `image-1.png`, `image-10.png`, `image-11.png`, `image-12.png`, `image-13.png`, `image-14.png`, `image-15.png`, `image-16.png`, `image-17.png`, `image-18.png`, `image-2.png`, `image-3.png`, `image-4.png`, `image-5.png`, `image-6.png`, `image-7.png`, `image-8.png`, `image-9.png`, `image.png` | Anexos originales inmutables; propiedad del autor de captura, visual pendiente salvo muestra explícita. No se mueven. |
| `capturas/teoria/03-redes-telecomunicaciones`: `image-1.png`, `image-2.png`, `image-3.png`, `image-4.png`, `image-5.png`, `image-6.png`, `image.png` | Anexos originales inmutables; propiedad del autor de captura, visual pendiente salvo muestra explícita. No se mueven. |
| `capturas/teoria/04-modulacion-digitalizacion-multiplexacion`: `image-1.png`, `image-10.png`, `image-11.png`, `image-12.png`, `image-13.png`, `image-14.png`, `image-15.png`, `image-16.png`, `image-17.png`, `image-18.png`, `image-19.png`, `image-2.png`, `image-20.png`, `image-21.png`, `image-22.png`, `image-23.png`, `image-24.png`, `image-25.png`, `image-26.png`, `image-27.png`, `image-28.png`, `image-29.png`, `image-3.png`, `image-30.png`, `image-31.png`, `image-32.png`, `image-33.png`, `image-34.png`, `image-35.png`, `image-36.png`, `image-37.png`, `image-38.png`, `image-39.png`, `image-4.png`, `image-40.png`, `image-41.png`, `image-42.png`, `image-43.png`, `image-44.png`, `image-45.png`, `image-46.png`, `image-47.png`, `image-48.png`, `image-49.png`, `image-5.png`, `image-50.png`, `image-51.png`, `image-52.png`, `image-53.png`, `image-54.png`, `image-6.png`, `image-7.png`, `image-8.png`, `image-9.png`, `image.png` | Anexos originales inmutables; propiedad del autor de captura, visual pendiente salvo muestra explícita. No se mueven. |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026`: `pagina-01.png`, `pagina-02.png`, `pagina-03.png`, `pagina-04.png`, `pagina-05.png`, `pagina-06.png`, `pagina-07.png`, `pagina-08.png`, `pagina-09.png`, `pagina-10.png`, `pagina-11.png`, `pagina-12.png`, `pagina-13.png`, `pagina-14.png`, `pagina-15.png`, `pagina-16.png`, `pagina-17.png`, `pagina-18.png`, `pagina-19.png`, `pagina-20.png`, `pagina-21.png`, `pagina-22.png`, `pagina-23.png`, `pagina-24.png`, `pagina-25.png`, `pagina-26.png`, `pagina-27.png`, `pagina-28.png`, `pagina-29.png`, `pagina-30.png`, `pagina-31.png`, `pagina-32.png`, `pagina-33.png`, `pagina-34.png`, `pagina-35.png`, `pagina-36.png`, `pagina-37.png`, `pagina-38.png` | Anexos originales inmutables; propiedad del autor de captura, visual pendiente salvo muestra explícita. No se mueven. |
| `capturas/teoria/Cuestionarios`: `image.png` | Anexos originales inmutables; propiedad del autor de captura, visual pendiente salvo muestra explícita. No se mueven. |
| `material/catedra/Condiciones de cursada.doc` | Auxiliar original; no editado ni extraído. No habilita tema nuevo. |
| `material/practica/U 1/CONEXION LLAVE TERMICA.jpg` | Auxiliar original; no editado ni extraído. No habilita tema nuevo. |
| `material/teoria/CAPITULOS DEL LIBRO DE LA CATEDRA-20260813.zip` | Contenedor no extraído ni modificado; los PDFs disponibles se inventarían por separado. No se afirma equivalencia por nombre. |
| `material/teoria/U2/Códigos de línea cuadro comparativo.zip` | Contenedor no extraído ni modificado; los PDFs disponibles se inventarían por separado. No se afirma equivalencia por nombre. |
| `material/teoria/U2/Fotocopia de codigo linea.rar` | Contenedor no extraído ni modificado; los PDFs disponibles se inventarían por separado. No se afirma equivalencia por nombre. |
| `material/teoria/U2/Fourier en tiempo real v2.xlsx` | Fourier U2: hoja original no analizada. Autor U1–U2 sólo si usa datos de esta hoja, debe contrastarlos. |
| `material/teoria/U2/Unidad de medida de sonoridad dB.docx` | dB U2: documento original no extraído. Autor U1–U2 tiene filminas/capturas/libro con cache; si usa este DOCX, contrastar original. |

**Bibliografía y filminas complementarias no usadas todavía:** Tanenbaum (819 páginas), Stallings (897 páginas) y PDFs Capitulo_1a/2b/3b/4b/5a/6a y Clase7a–11a quedan originales intactos, sin cache nuevo. No se usan para redactar hasta crear su extracto/cache si efectivamente aportan contraste. Cap5a/Clase7a/8a y contenido interfaces de Cap6a corresponden mayormente U7/U8 fuera del alcance. Bibliografía NO define alcance.

## Precisiones bibliográficas y páginas

- DOC-20230425-WA0040.pdf: Castro Lechtaler y Fusario, *Comunicaciones: una introducción a las redes digitales de transmisión de datos y señales isócronas*, 1.ª ed., Alfaomega, 2013. Ficha visual p. PDF 4: ISBN 978-987-1609-35-2. No citarlo como edición2015.
- La edición bibliográfica declara 736 páginas; este archivo tiene 726 páginas PDF. El número PDF no sustituye el impreso: se registra ambos al citar.
- Libro U1 sistemas §3.2.4.2: p. PDF 170–171 / impresas144–145; extracto incluye contexto PDF167–173. Internet extracto PDF66–89 / impresas40–63. OSI PDF276–283 / impresas250–257.
- Libro U2 §2.7: PDF134–138 / impresas108–112; códigos UIT-T §2.8.6 aparece al final de PDF155; PDF156 ya inicia §2.9 Filtros. No atribuir ambas páginas enteras a §2.8.6. Fourier extracto incluye PDF106–112 / impresas80–86.
- Libro U5 información/entropía/tasa: PDF202–212 / impresas176–186. El extracto incluye capacidad y uso de la medida de información para conexión U6, sin abrir temas nuevos.
- Libro U6 extracto PDF194–202 y212–248: canal, capacidad, ruido/distorsión y métodos de error. Omitir secciones no registradas (p.ej. detalles meteorológicos o códigos no vistos) aunque estén en el extracto.

## Control de preservación y próximos pasos

- Baseline verificado: 259 archivos originales/cache históricos; discrepancias: 0. Todos conservan su SHA-256.
- Cada autor completa mapa fino fuente/captura/página → sección APUNTE y separación teoría/práctica/repaso. Este inventario no reemplaza ese mapa.
- Prioridad autores: cotejo visual de fórmulas/figuras de SUS páginas y recálculos; no promoción a revisado por mera existencia de cache.
- Verificador final debe comprobar enlaces, unidades, supuestos, cuentas, fidelidad con capturas/material, exclusiones y preservación baseline.

## Apéndice — contraste externo acotado U5 (2026-10-11)

Estos documentos públicos fueron descargados SÓLO a `tmp/curador-ejecucion/externos/` y se usan como apoyo a ITA2, Morse y Huffman YA registrados. No son nuevas clases, no amplían el programa y no reemplazan la captura de cátedra. Los tres caches son nuevos; los39 anteriores se conservaron. Total actualizado:42caches `.txt`. Descarga inicial sandbox falló por resolución dehost; descarga autorizada con escalación completó los tresPDF sin instalaciones.

### UIT-T S.1 (03/1993), Alfabeto Telegráfico Internacional N.º 2, versión española
- PDF temporal: `tmp/curador-ejecucion/externos/itu-t-s1-1993-es-ita2.pdf` (8páginasPDF).
- Origen: https://www.itu.int/rec/dologin_pub.asp?id=T-REC-S.1-199303-I!!PDF-S&lang=e&type=items
- Ficha / identificador: https://www.itu.int/rec/T-REC-S.1-199303-I/en
- Cache nuevo: `material/_cache/u5-contraste-itu-t-s1-1993-ita2-es.txt`.
- SHA-256 PDF: `7518b9135178efdff8fc05dce8f987bb0e3c768c12f1ebaf149574384c9bbac9`.
- SHA-256 cache: `46d603b9fa5873c95fd763f03b972ca2766e6813f7ca7fedf243105ab4933458`.
- Inspección visual real: PDF1 portada; PDF6/impresa2 §§3.1–3.2 y4.4; PDF7/impresa3 Cuadro1/S.1. No revisión integral.
- Limitación / contraste acotado: ITA2: cinco unidades, 32 combinaciones, A=0/Z=1; cambio letras/cifras combinaciones29/30; orden1 se transmite primero. La tabla es parcialmente rota en extracción y debe leerse visualmente.

### UIT-R M.1677-1 (10/2009), International Morse code, versión inglesa
- PDF temporal: `tmp/curador-ejecucion/externos/itu-r-m1677-1-2009-morse.pdf` (7páginasPDF).
- Origen: https://www.itu.int/dms_pubrec/itu-r/rec/m/R-REC-M.1677-1-200910-I!!PDF-E.pdf
- Ficha / identificador: https://www.itu.int/rec/R-REC-M.1677-1-200910-I/
- Cache nuevo: `material/_cache/u5-contraste-itu-r-m1677-1-2009-morse-en.txt`.
- SHA-256 PDF: `a3eab8884c24200f229ef20615ee3ae14329ba0f0a29c7a85a1eaa3cac442b97`.
- SHA-256 cache: `f8e88e252e70acd3f4eb96559ce6096574736c2a344d81808ce57498280cc35a`.
- Inspección visual real: PDF1 portada; PDF5/impresa3 §2.1–2.4 duración y separaciones. No revisión integral.
- Limitación / contraste acotado: Morse: raya=3puntos; separación interna=1punto, letras=3puntos y palabras=7puntos. Sólo contraste de Morse ya registrado; no incorporar procedimientos radiotelegráficos.

### David A. Huffman (1952), A Method for the Construction of Minimum-Redundancy Codes, Proceedings of the I.R.E., pp.1098–1101; reproducción escaneada hospedada en compression.ru
- PDF temporal: `tmp/curador-ejecucion/externos/huffman-1952-minimum-redundancy-codes.pdf` (4páginasPDF).
- Origen: https://compression.ru/download/articles/huff/huffman_1952_minimum-redundancy-codes.pdf
- Ficha / identificador: https://doi.org/10.1109/JRPROC.1952.273898
- Cache nuevo: `material/_cache/u5-contraste-huffman-1952-scan-texto-limitado.txt`.
- SHA-256 PDF: `e15818feb9ce9874dbe44073edd85da29fee08a96bc576fe4572211784d8842e`.
- SHA-256 cache: `9dcf98e2cd0570aba524870ca4ca97db503abfa896f40e11ba1454dd19591a7a`.
- Inspección visual real: PDF1/impresa1098 título/autor/September y condición prefijo; PDF2/impresa1099 cabecera1952 y Optimum Binary Code. No revisión integral de4p.
- Limitación / contraste acotado: Artículo original identificado visualmente por autor/título/revista/fecha y continuidad pp.1098–1099. PDF3–4 sin texto; PDF1–2 sólo cabeceras extraíbles (136y77caracteres). No OCR ni transcripción simulada. Para contraste algoritmo se requiere render, no buscar en este cache.

**Ownership:** autor U5 selecciona únicamente evidencia para secciones ya registradas. El escaneo Huffman NO quedó convertido a texto íntegro: su cache tiene cabeceras mínimas y los marcadores de pérdidas; algoritmo debe cotejarse visualmente en original. PDFs y renders temporales no están autorizados para moverse a material/ ni sobrescribir fuentes.
