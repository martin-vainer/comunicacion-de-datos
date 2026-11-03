# Revisión U01 — A/B

## Dictamen A

# Dictamen académico independiente U1 — revisor A

Fecha de cierre: **2026-10-13**. Proyecto: `comunicacion_de_datos`. `skill_resolution: injected`.

**Estado: requiere cambios; no aprobado como unidad revisada.** Revisión completa del contenido candidato y de sus fuentes locales pertinentes, con límites externos y de independencia explicitados abajo. No se modificó el TP, el canónico, los originales, los caches ni archivos compartidos. No se ejecutaron builds, instalaciones o commits.

| Prioridad | Cantidad | IDs |
|---|---:|---|
| P0 — integridad | 0 | — |
| P1 — error académico | 1 | U01-A-001 |
| P2 — pedagogía/cobertura/evidencia | 1 | U01-A-002 |
| P3 — editorial | 2 | U01-A-003, U01-A-004 |

Bloqueantes para aprobación: **U01-A-001 y U01-A-002**. Además, no elevar el alcance parcial a U1 programática completa, ni dar por confirmada la definición de «interactivo diferido». Estos últimos límites ya están declarados: no se registran nuevamente como errores.

## 1. Identidad, alcance e independencia

Repositorio: `C:/Users/Martin/Documents/UTN_SISTEMAS/Anual_2026/comunicacion_de_datos`.

Se revisó la carpeta completa `apuntes/teoria/01-introduccion-comunicaciones/`: APUNTE, INDICE, siete PNG, registro de imágenes y `.gitkeep`; además TP1 completo, sus tres figuras y repaso U1. Se leyeron AGENTS y metodología como criterios. No se revisó técnicamente el contenido de las otras unidades enlazadas.

Snapshot de referencia: `docs/consolidacion-u1-u6/snapshot-inicial.json`, SHA-256 **`1E29FD3BF30B9D99D07E0D3B73E2D7EF11F9D85BB7874B2630650412068A7BDD`**. Comprobación propia de los **401 registros: 0 discrepancias**, antes del cierre y después de redactar. Los **16 archivos de identidad propia** tampoco cambiaron. Los hashes y comprobaciones reproducibles están en `tmp/reviews/u01-a/hashes-antes.json`, `hashes-despues.json` y `qa-resultados.json`.

| Candidato | SHA-256 antes = después |
|---|---|
| APUNTE.md | `DAA739D206799C359D8AE9D9679BEBF88A418F7A56DA81A20B2E6336715A2DBF` |
| INDICE.md | `D0A50D7AF533E567CDEDB98CB2E56FD1A03C0157C3E3CDDE0336C3775DC5C608` |
| imagenes/registro-imagenes.md | `262A611E1D46F4E5DE39F6FA03BF55A940E7136D7BE83F747E25903D012DDD11` |
| TP1 | `FC8859722D0AB0378C67C83D4ED74E0FFEFF6847BCD421A04E1AA01AF7B0A1A8` |
| Repaso U1 | `AA78886B59798C54B4F5F696A16617CE857C6E47A1865795E465D18C0DDAF044` |

No se abrieron informes de otros revisores, `estado.md`, carpetas `tmp/autor-*` ni conclusiones de memoria ajenas. El inventario sólo sirvió para localizar fuentes. **Excepción de independencia:** la extracción de APUNTE completo devolvió su autocontrol embebido (§8); quedó visible, aunque no se lo aceptó como prueba ni como conclusión. Por ello no se afirma ceguera perfecta respecto de ese bloque. Todos los resultados aquí documentados proceden de inspecciones originales, cuentas y scripts propios; el YAML tampoco fue tomado como aprobación. Esta excepción se comunicó al coordinador.

## 2. Cobertura efectiva de fuentes originales

Abreviaturas usadas en las matrices: T = PDF teórico U1; P = PDF práctico UT1; O = Organismos; E = enunciado TP1; R = respuestas TP1; C = Castro 2013 local. Páginas **PDF**, salvo indicación de impresas.

| Original | Páginas realmente contrastadas visualmente | Resultado / límite |
|---|---|---|
| `material/teoria/U1/U1 Introduccion a las comunicaciones.pdf` (T) | **1–25, todas** | Portada; historia gráfica; transmisión; modalidades; circuitos; canales; organismos; OSI; Internet/IoT/IIoT; cronología; IANA; IXP. P2 no está representada en el cache: U01-A-002. P22 se verificó como anticipo IIoT, no como catálogo de prestaciones de su equipo. |
| `material/practica/U 1/UT 1 COMUNICACIONES.pdf` (P) | **1–10, todas** | Definiciones, circuitos/canales, conversión de voz, convergencia, Internet y OSI. |
| `material/practica/U 1/Organismos  UT 1.pdf` (O) | **1–3, todas**, individualmente | Ficha histórica, no organigrama vigente. Nombre ISO y años contradictorios no se enseñan como hechos confirmados. Nombre EIA: U01-A-003. |
| `material/practica/U 1/TP 1  2026.pdf` (E) | **1–3, todas**, individualmente | Las veinte consignas se contrastaron con el candidato; datos numéricos verificados en original. |
| `material/practica/U 1/TP1-respuestas y resumen.pdf` (R) | **1–3, todas**, individualmente | Fórmulas y respuestas parciales p1–2. Interpolación RG-213 p3 excluida por no integrar las veinte consignas ni el candidato. |
| `material/catedra/PROGRAMA de la materia.pdf` | **2**, individualmente | Apartado U1; no se afirma revisión integral del programa del resto de unidades. |
| `material/teoria/DOC-20230425-WA0040.pdf` (C) | **4, 169–171 y 276–282**, todas individualmente | P4 acredita edición 2013. PDF169–171 = impresas143–145; PDF276–282 = impresas251–257. Modalidades, interacción, respuesta oportuna, servicios, interfaces, protocolos y capas. P279 incluye comparación TCP/IP no desarrollada por el candidato. |

Total: **56 páginas PDF originales**, no un muestreo presentado como revisión del libro entero. Renders y extracciones propios: `tmp/reviews/u01-a/{teoria,practica,organismos,enunciado,respuestas,programa,castro}/`. Las planchas se usaron para las filminas; las páginas bibliográficas y los documentos de enunciados/organismos se ampliaron individualmente. Los originales, no las transcripciones, decidieron figuras y glifos.

Capturas leídas completas:

- `capturas/teoria/01-introduccion-comunicaciones/Apuntes-clase 1.md` (T1): todos los fragmentos U1, incluida la lista de funciones OSI.
- `capturas/practica/clase 01.md` (P1): conceptos, diagramas y veinte ejercicios; expresiones eléctricas contrastadas con R1 y datos de E2–3.
- `capturas/teoria/Cuestionarios/cuestionario U1 y U2.md`: Q1–3, todas las opciones. Q4–7 leídas para delimitación, **fuera de U1**, no juzgadas aquí.
- `capturas/practica/image.png` e `image-1.png` a `image-9.png`: diez originales vistos individualmente y comparados con sus diez copias por hash.

Caches consultados sólo como auxiliares: `u1-introduccion-a-las-comunicaciones.txt`, `u1-introduccion-a-la-teleinformatica.txt`, `u1-organismos-de-comunicaciones.txt`, `tp-01-2026-enunciado.txt`, `tp-01-respuestas-y-resumen.txt`, `programa-analitico-comunicacion-de-datos.txt` y extracto `castro-fusario-2013-u1-sistemas-internet-osi-extracto.txt`. No se generaron o sobrescribieron caches compartidos.

## 3. Revisión sección por sección del canónico y navegación

| Sección / líneas APUNTE | Afirmaciones y ejemplos revisados | Original contrastado / resultado |
|---|---|---|
| Frente, 1–67 | YAML, alcance, cobertura programática, mapa de capturas | Programa PDF2; T1–25/P1–10/E1–3; estado `en-progreso` prudente. U01-A-002 sobre evidencia de historia, no sobre la exclusión explícita. |
| §1 `teleinformatica-y-explotacion`, 70–137 | Telecomunicaciones + informática; centralizado/distribuido; batch/remoto/tiempo compartido/interactivo real y diferido; online/offline; ejemplos y errores | T4–5/P2–3; T1/P1; C169–171; IBM. Criterios no excluyentes correctamente distinguidos. «Diferido» orientativo y no evaluable: límite honesto. |
| §2 `transmision-y-canal`, 141–222 | Información vs señal; punto a punto/multipunto, local/remota; ETD/ECD/canal; módem, banda base, regeneración; A/D/A; atenuación/distorsión/ruido | T3,7–8/P3,5–7; P1; imágenes1–5. Modulación duplicada en dibujo correctamente aclarada como demodulación receptora. Efectos definidos cualitativamente y remitidos a unidades posteriores. |
| §3 `circuito-y-enlace`, 226–275 | ETD/ECD, interfaz, CD ambos ECD + medio, ED extremos ETD; ejemplo y errores | T6/P4; imagen0; Q1. Corrige sin tocar la captura la omisión del medio. Límites CD/ED consistentes con original. |
| §4 `redes-internet-ixp`, 279–351 | Nodos/enlaces; cuatro topologías y LAN/MAN/WAN; red de redes; hosts/interfaces IP/routers; convergencia; IoT/IIoT; ARPA/ARPANET; NIC/IANA; IXP/ISP | T21–25/P8–9/E3; T1/P1; RFC e instituciones indicados en §6 del informe. Ejemplos son cualitativos y están identificados. No equipara malla con topología única ni fecha de actividad con fundación. Línea325 distingue correctamente ARPA1958 y ARPANET1969; discordancia localizada en TP: U01-A-001. |
| §5 `normalizacion`, 355–379 | Interoperabilidad, organismos de competencias distintas; ISO/OSI, IETF/RFC, IANA, roles históricos; RFC no necesariamente estándar | T9–10,23–24/O1–3; T1; fuentes institucionales. No adopta como vigentes las listas antiguas. Nombre EIA erróneo sólo en TP. |
| §6 `modelo-osi`, 383–461 | Entidades, servicio/interfaz/protocolo/PDU; siete funciones y ejemplos; encapsulación lógica; archivo extremo a extremo; QoS/UDP/Frame Relay/V.24 | T10–20/P10; C276–282; T1/Q2–3; imagen6; RFC768/1490 y UIT V.24. Revisadas las siete filas y siete acciones del ejemplo. Responsabilidades abstractas no prometen confiabilidad de UDP ni equivalencia total Frame Relay=capa3. |
| §7, 465–476 | Diez gotchas: CD/ED, ISO, malla, organismos, canal real, RFC, UDP/Frame Relay, historia, ficha, explotación | Cada aclaración contrastada con las fuentes anteriores. No se acepta su rótulo «verificado» como certificación. |
| §8, 480–489 | Tres pendientes y límite NIC/IANA | Falta criterio de cátedra para diferido; alcance parcial declarado; solicitud de juicio independiente. U01-A-002 también afecta fila486. Tabla de autocontrol492–506 no se utiliza como prueba. |
| §9, 510–517 | Separación de TP/repaso; Q1–3 vs Q4–7 | Rutas/anclas comprobadas; correcto destino separado. |
| §10, 521–525 | Puentes a U2/U3/U4 | Anclas/rutas válidas; relación conceptual apropiada. No revisión técnica de unidades destino. |
| §11, 529–547 | Resumen mental y once ítems de checklist | Coherentes con alcance desarrollado, sin definición confirmada de diferido ni cifras inventadas. |
| INDICE completo | Seis secciones, gotchas, pendientes, registro, orden de lectura, TP/repaso/capturas | Todos los enlaces resuelven. Advierte que alcance parcial no es U1 final. |
| Registro de imágenes completo | Procedencia, siete hashes y límites de esquemas | Recalculados los hashes propios; siete coincidencias, páginas fuente correctas. No se confunde una captura exclusiva con filmina. |

**Metodología:** los cinco conceptos centrales (§1,2,3,4,6) explican problema, concepto, modelo, criterios/funciones, ejemplo, errores y respuesta oral; normalización es concepto secundario. U1 canónica no contiene ecuaciones cuantitativas: no corresponde inventar ejemplos numéricos decorativos para límites CD/ED o roles OSI. La formalización cualitativa explicita el alcance del modelo. Resumen y checklist presentes. Las cuentas reales están en TP y se recalcularon todas.

## 4. TP1: veinte consignas, fórmulas y recálculos

Las consignas E1–11 provienen de E p2 y E12–20 de E p3. Se confrontaron con R p1–2 sin dar por verdaderas sus respuestas. Todos los resultados numéricos finales del candidato son correctos bajo sus supuestos.

| Ejercicio / líneas TP | Revisión propia completa | Resultado / evidencia |
|---|---|---|
| E1,57–67 | Ohm y cierre V/A | 120/3 = **40 Ω**; R2 coincide. |
| E2,69–85 | Longitud km→m; despeje y unidades de resistividad | 20×16/4000 = **0,08 Ω·mm²/m**; R2 coincide. |
| E3,87–106 | Sección vs diámetro; hilo uniforme y ρ constante | π×2,6²/4 = **5,309291585 mm²**; L = **3318,307240 m = 3,318307 km → 3,32 km**. Con S ya redondeada a5,31 sale3318,75m, no exactamente3318: diferencia de redondeo intermedio, sin cambio de respuesta final ni error académico material. R no resuelve E3; datos comprobados en E2. |
| E4,108–125 | Dos lámparas en serie, único camino y dos polos acoplados | Grafo y original image8 representan las dos cargas; apertura corta ambas. U01-A-004 en alt. Protección genérica, no receta de instalación. |
| E5,127–147 | Dos ramas sobre mismos nodos, QF antes/después de las ramas | Grafo consistente; una carga abierta no abre la otra. Imagen7 es apoyo serie/paralelo/mixto, no dibujo protegido; el texto explicita esa diferencia. |
| E6,149–161 | Tensión/corriente totales; RT vs R3 | RT=100/1=**100 Ω**; R3=100−2−8=**90 Ω**. Image9 y R2 concuerdan. |
| E7,163–180 | Suma de conductancias y control de límite | 1/2+1/10+1/8=**0,725 S**; RT=40/29=**1,379310345 Ω →1,38 Ω**, menor que2Ω. |
| E8,182–206 | Potencia, tiempo, energía y costo separados | TV=**1,6 kWh**, calefactor=**1,5 kWh**, diferencia=**0,1 kWh**, total=**3,1 kWh**, ×$60/kWh=**$186**. Tarifa es dato de consigna, no precio vigente. |
| E9,208–222 | P=VI y luego Ohm | V=25/2,5=**10 V**; R=10/2,5=**4 Ω**. |
| E10,224–234 | Variación de tensión, R constante explícita | 15²/4=**56,25 W**; no atribuye al filamento real R constante. |
| E11,236–256 | Resistencia de carga fija y disminución respecto de potencia inicial | R=220²/1100=**44 Ω**; P200=200²/44=**909,090909 W**; caída=100[1−(200/220)²]=**17,3553719% →17,36%**. |
| E12,258–262 | Disciplinas y explicación oral | T4–5/P2: definición correcta. |
| E13,264–277 | Sector UIT-T; reforma1992; WTSA, grupos, TSAG, TSB; recomendaciones no leyes automáticamente | Historia y marco institucional primarios; voluntariedad corroborada además con página oficial de recomendaciones. No se exige corregir sólo por la referencia menos precisa «en breve». |
| E14,279–294 | Agencia vs redes; ARPA1958/DARPA1972, ARPANET1969, NSFNET1985; dos hitos MILNET; cierre parcial | DARPA/NSF/RFC881/RFC1302 corroboran las distinciones. **U01-A-001**: comparación final con «1960» atribuye al objeto equivocado la fecha de T23. |
| E15,296–308 | Hosts, routers, redes/enlaces, direcciones y proveedores; malla no completa | P9/T21/P1; las direcciones no se presentan como equipos. Correcto. |
| E16,310–316 | Información codificada y representación física, local/remota | T3/P3; correcto en nivel introductorio. |
| E17,318–338 | Cuatro sitios, LAN, WAN y única salida central | E3/P1; todos los caminos externos pasan por central. No presupone VPN/alquiler; carga y dependencia central explicadas. |
| E18,340–357 | Mainframe, dos terminales locales y uno remoto, ECD y enlace | E3/T4–5/P1; procesamiento central y acceso remoto sin tecnología impuesta. |
| E19,359–370 | ISO, IEEE, ANSI y EIA; normalización vs coordinación | O1–2 y organismos primarios; tres primeros correctos. **U01-A-003**: nombre histórico EIA. |
| E20,372–395 | Función de ISP y seis categorías del informe fijo; DSL, HFC, fibra, radio y satélite | E3/P9 y fuentes ENACOM: explicación técnica coherente, sin promesas de cobertura/precios. **Límite documental:** no se pudo abrir el PDF2025T4 ni el registro citados; no se certifica su gráfico exacto. Véase §6. |

### Auditoría de cada relación matemática

`V=RI` y despejes `R=V/I`, `I=V/R`; `R=ρL/S`, `ρ=RS/L`, `L=RS/ρ`; `S=πd²/4`; `P=VI`, `P=V²/R`, `P=I²R` (esta última en captura/resumen); `E=Pt` y forma equivalente `E=VIt`; suma de R en serie; suma de1/R en paralelo; porcentaje de caída: todas algebraica y dimensionalmente consistentes. E1–3/E6–11 suministran ejemplos calculados de todas las relaciones empleadas en el candidato; no se agregó una ecuación ajena al corpus.

Símbolos y unidades en TP32–45: V, I, R, ρ, L, S, d, P, E, t. V/A=Ω; ρL/S cierra enΩ; V·A=W; W·h=Wh, kW·h=kWh; se cancelan kWh en costo. La energía con tiempo en segundos se expresaría enJ, noWh: el candidato usa horas en sus cuentas. Las potencias AC del modelo resistivo se interpretan con tensiones/corrientes eficaces y sin reactancia; no se extiende `P=VI` a potencia activa de cualquier carga reactiva. E3 declara uniformidad; E10–11 explicitan la idealización térmica.

Recalculadas también las magnitudes deducibles de los esquemas auxiliares de image7: serie260+330=**590Ω**, corriente230/590=**0,3898305A**; paralelo260||330=**145,423729Ω**; mixto260+(130||330)=**353,260870Ω**. No hay resultados contradictorios incorporados al texto. Su subdibujo RLC rotulado AC usa un símbolo de fuente ambiguo y carece de frecuencia/datos completos: es un dibujo original auxiliar, no una resolución exigida o desarrollada. No se inventa un cálculo de impedancia ni se lo contabiliza como ejemplo resuelto verificado.

## 5. Figuras, Mermaid y repaso

| Figura original → copia | Uso / contraste concreto |
|---|---|
| image.png → teoría/imagenes/image.png | Límites ED/CD: rótulo ED superior recortado en captura, confirmado en T6/P4. |
| image-1.png → teoría/imagenes/image-1.png | Red analógica, T7/P5; flechas, módems y rotulación receptora corregida en explicación, sin editar imagen. |
| image-2.png → teoría/imagenes/image-2.png | Filtro/COD/DECOD/modulador; sólo captura, sin falsa página PDF. |
| image-3.png → teoría/imagenes/image-3.png | Canal digital ECTD/RR, T8/P6; regeneración explicada funcionalmente. |
| image-4.png → teoría/imagenes/image-4.png | Filtro/COD/DECOD sin portadora; sólo captura, no universalidad. |
| image-5.png → teoría/imagenes/image-5.png | Teléfono A/B, códecs A/D y D/A, T8/P7; muestreo/cuantificación/codificación sólo anticipo U4. |
| image-6.png → teoría/imagenes/image-6.png | Siete capas y agrupaciones, T10/P10; nombres/orden contrastados. |
| image-7.png → práctica/assets/tp-01-circuitos-serie-paralelo.png | Serie/paralelo/mixto y dibujo RLC auxiliar, cuentas arriba. No representa QF y el candidato lo advierte. |
| image-8.png → práctica/assets/tp-01-lamparas-serie.png | LAMP1 y LAMP2 en serie, protección bipolar; alt incorrecto: U01-A-004. |
| image-9.png → práctica/assets/tp-01-resistencias-serie.png | E6, R1=2/R2=8, R3 desconocida,100V/1A, total100Ω; no confundir total con incógnita. |

**10/10 copias idénticas por SHA-256**; vista individual de los diez originales. Los hashes completos quedan en `qa-resultados.json`. Las imágenes pertenecientes a los PDF se inspeccionaron en las56páginas registradas, no se juzgaron desde el cache.

**Mermaid: cinco bloques**, APUNTE162–168 y TP114–121,133–143,324–336,344–355. Revisados nodos, flechas, ramas, caminos y coherencia con las explicaciones. **No se ejecutó motor ni render visual Mermaid**; no se afirma validación de layout/sintaxis por un renderizador. No se detectó contradicción semántica en sus grafos.

**Repaso completo:** tres preguntas, quince alternativas y sus tres correcciones razonadas. Q1 conserva cinco opciones y selecciona **5: ECD+medio**, corroborada T6/P4. Q2 selecciona **b: V.24 capa física**, con UIT V.24 y T14; descarta servicio=interfaz, compresión en sesión y normalización MAC en física. Q3 selecciona **a: OSI es ISO, no IEEE**, corroborada T10/P10/C276–282; criptografía capa6 y responsabilidades físicas se explican en el nivel del modelo, no como prohibición de cifrar en otras arquitecturas. Enunciados separados de soluciones, original inmutable, trazabilidad por pregunta y pendientes no convertidos en preguntas confirmadas. Estado `completo` referido a las tres preguntas declaradas, no a todo U1.

**Navegación:** 109 enlaces locales extraídos de APUNTE, INDICE, registro, TP y repaso: **0 rutas/anclas faltantes**. El comprobador verifica destinos locales y anclas Markdown; no certifica que una URL externa esté accesible. Fuente de resultados: script propio `qa.py`, no conteo autoral.

## 6. Verificación primaria externa y límites reales

Consultas propias de contraste, no ampliación del programa. Se inspeccionó el fragmento que fundamenta cada afirmación; no se afirma lectura integral de cada RFC o sitio.

| Afirmación | Evidencia primaria realmente consultada / resultado |
|---|---|
| Batch sin interacción, ejemplos de lote; tiempo compartido conversacional concurrente | [IBM batch/online](https://www.ibm.com/docs/en/zos-basic-skills?topic=today-mainframe-workloads-batch-online-transaction-processing), contenido indexado por buscador oficial; acceso directo403. [IBM time-sharing2.5](https://www.ibm.com/docs/en/zos/2.5.0?topic=operations-controlling-time-sharing), contenido indexado, alternativa oficial de versión anterior: la URL3.2 citada devuelve403. Se corroboran conceptos, **no acceso directo ni identidad de la página3.2**. |
| Online/offline, operación del equipo distinta de acceso Internet | [Glosario IBM z/VM](https://www.ibm.com/support/pages/zvm/library/glossary/index.html), entradas online/offline vistas; respaldo directo. |
| Actividad NIC1970/1971, no fundación inferida | [RFC82](https://www.rfc-editor.org/rfc/rfc82.txt), pp5–6; [RFC95 HTML](https://www.rfc-editor.org/rfc/rfc95.html), pp1–2. TXT95 no entregó contenido útil; HTML del mismo RFC sí. |
| Precursor Postel1972 y nombre IANA1988, funciones actuales | [RFC349](https://www.rfc-editor.org/rfc/rfc349.txt), p1; [RFC1083](https://www.rfc-editor.org/rfc/rfc1083.txt), §§7.2/7.4; [IANA About](https://www.iana.org/about). No se deduce una fecha de fundación única. |
| RFC no necesariamente estándar o IETF | [RFC Editor: What is an RFC?](https://www.rfc-editor.org/series/rfc/), tipos documentales y corrientes; corroborado. |
| UDP no garantiza entrega/duplicados; Frame Relay lleva protocolos de red | [RFC768](https://www.rfc-editor.org/rfc/rfc768.txt), introducción; [RFC1490](https://www.rfc-editor.org/rfc/rfc1490.txt), resumen/introducción y§2. Corroborado; no desarrollo de arquitecturas completas. |
| V.24: circuitos de intercambio ETD/ECD, no toda RS-232 | [Ficha UIT V.24](https://www.itu.int/rec/T-REC-V.24/en), título oficial y recomendación identificada. No se auditan sus circuitos individuales: U8 excluida. |
| UIT1992 y organización UIT-T; voluntariedad | [Historia UIT](https://www.itu.int/en/history/Pages/FocusOnStandardization.aspx), [Marco UIT-T](https://www.itu.int/en/ITU-T/about/Pages/framework.aspx), [UIT-T en breve](https://www.itu.int/en/ITU-T/about/Pages/default.aspx); para no leyes automáticamente: [Recomendaciones UIT-T](https://www.itu.int/en/ITU-T/publications/Pages/recs.aspx), no obligatorias salvo adopción normativa. |
| ARPA1958, DARPA1972, ARPANET1969 | [DARPA: ARPA is born](https://www.darpa.mil/about/innovation-timeline/arpa-is-born),7feb1958; [cambio de nombre](https://www.darpa.mil/about/innovation-timeline/arpa-becomes-darpa); [ARPANET](https://www.darpa.mil/news/features/arpanet), cuatro nodos1969. |
| NSFNET1985 y papel histórico | [NSF historia](https://www.nsf.gov/about/history), apartado1985; [NSF Internet](https://www.nsf.gov/impacts/internet), papel de expansión. |
| MILNET: hito programado1983 vs reseña1984 | [RFC881](https://www.rfc-editor.org/rfc/rfc881.html), The Schedule,4oct1983; [RFC1302](https://www.rfc-editor.org/rfc/rfc1302.html), History. El TP no presenta como demostrada la reconciliación de hitos, lo cual es adecuado. |
| ISO nombre y rol; IEEE estándares; ANSI coordinación | [ISO About](https://www.iso.org/about), [catálogo IEEE](https://standards.ieee.org/standard/), [ANSI introduction](https://ansi.org/about/introduction); ficha O2 aporta IEEE802. |
| Nombre histórico EIA | [ECIA Staff](https://www.ecianow.org/staff/), antecedentes laborales EIA con nombre **Electronic Industries Alliance**; también documento histórico [EIA EP-7-C](https://www.ecianow.org/assets/docs/EIAStandards/3.4.2_EP-7-C.pdf), portada/foreword indexados. No se infiere que EIA siga activa. |
| ENACOM registro y clasificación2025T4 | Las dos URLs exactas del TP no pudieron abrirse por error de recuperación: [registro](https://www.enacom.gob.ar/informacion-de-prestadores_p1346) y [Resumen2025T4](https://indicadores.enacom.gob.ar/files/informes/nacionales/2025/T4/2025T4-01%20-%20Resumen.pdf). [Índice oficial](https://indicadores.enacom.gob.ar/Informes/nacionales) indexado confirma la existencia del resumen, **no el gráfico completo**. [Tipos de conexión ENACOM](https://www.enacom.gob.ar/tipos-de-conexion_p112) y datos abiertos indexados apoyan categorías técnicas. No sustituir silenciosamente estas consultas por inspección visual del PDF exacto. |

No se demostró falsedad de E20; la imposibilidad de recuperar sus originales externos es **limitación del revisor**, no hallazgo académico inventado. Para cerrarla, abrir el gráfico2025T4 y la entrada del registro, conservar evidencia verificable y contrastar cada categoría/denominación; no se requieren ni permiten agregar tecnologías al temario.

## 7. Hallazgos accionables

### U01-A-001 — P1 — Fecha de ARPA comparada erróneamente con inicio de ARPANET

- **Ubicación:** `apuntes/practica/tp-01-comunicaciones.md`, E14, ancla `ejercicio-14--redes-y-organismos-vinculados-con-el-origen-de-internet`, **línea294**, última oración.
- **Afirmación:** la fecha1960 de la filmina no coincide con fuentes que sitúan ARPANET en1969.
- **Evidencia:** T **PDF23**, vista original: el listado escribe ARPA(1960); el esquema inferior ya ubica ARPANET en1969. [DARPA creación](https://www.darpa.mil/about/innovation-timeline/arpa-is-born) documenta ARPA1958; [DARPA ARPANET](https://www.darpa.mil/news/features/arpanet) documenta operación1969. APUNTE325 distingue correctamente ambos.
- **Naturaleza:** **demostrado**, atribución de evidencia al objeto equivocado. No invalida la tabla principal de E14 ni obliga a reescribir el TP.
- **Consecuencia:** el estudiante puede creer que la filmina fecha mal ARPANET, cuando fecha mal la agencia, reproduciendo la confusión organismo/red que el ejercicio pretende corregir.
- **Acción mínima tras los dictámenes:** reemplazar sólo la comparación final:1960corresponde a ARPA y debe contrastarse con1958; mantener ARPANET1969 como hito distinto.
- **Prueba de cierre:** leer T23 y fuentes DARPA lado a lado; verificar que TP294 y APUNTE325 atribuyan cada fecha a la misma entidad. Mantener los originales y resto de resolución intactos.

### U01-A-002 — P2 — Mapa de evidencia histórica omite una lámina visual del corpus

- **Ubicación:** `apuntes/teoria/01-introduccion-comunicaciones/APUNTE.md`, tabla «Cobertura del programa», **línea46**; pendiente «Cobertura integral», **línea486**. Ancla de pendiente `8-pendientes-por-seccion`.
- **Afirmación:** historia general/revolución informática/sociedad del conocimiento/ética sin desarrollo registrado en filminas específicas usadas, con exclusión conjunta.
- **Evidencia:** T **PDF2**, original visual: gráfico histórico informática/comunicaciones1950–2000 con etapas y tecnologías. El cache deja esa página sin texto útil; APUNTE5 declara sólo pp3–25. ProgramaPDF2 distingue varios subtemas históricos.
- **Naturaleza:** **demostrado para la descripción de evidencia histórica**, no para sociedad/ética ni para todo el programa. Hay evidencia gráfica parcial en una fuente registrada y revisada; no se demostró material suficiente para todos los subtemas agrupados.
- **Consecuencia:** la cobertura mezcla «fuera del alcance elegido» con «sin evidencia», y el siguiente curador puede buscar material que ya está en el PDF o ignorar una página por depender del cache.
- **Acción mínima:** desagregar la fila o aclarar que existe historia gráfica parcial en T2, **no consolidada en este alcance**; conservar como exclusiones los restantes tópicos sin fuente. No exige redactar historia, ampliar el temario ni incorporar bibliografía nueva.
- **Prueba de cierre:** matriz y pendientes reconocen T2 y separan disponibilidad de evidencia de inclusión efectiva; alcance y YAML siguen honestos. Si se decide integrar la lámina en otra fase autorizada, trazar cada dato y no deducir historia adicional desde el dibujo.

### U01-A-003 — P3 — Nombre híbrido incorrecto de EIA

- **Ubicación:** `apuntes/practica/tp-01-comunicaciones.md`, E19, ancla `ejercicio-19--iso-ieee-ansi-y-eia`, **línea368**.
- **Afirmación:** *Electronics Industries Alliance* presentado como denominación histórica.
- **Evidencia:** O **PDF1** usa otro nombre histórico de la asociación, no respalda ese híbrido. [ECIA Staff](https://www.ecianow.org/staff/) emplea **Electronic Industries Alliance**, sin s al final de Electronic; documento EIA EP-7-C ofrece la misma denominación.
- **Naturaleza:** **demostrado**, nombre propio editorial; la función histórica general y cautela de vigencia son adecuadas.
- **Consecuencia:** se memoriza y reproduce una expansión incorrecta, atribuida falsamente a la ficha.
- **Acción mínima:** corregir Electronic y agregar respaldo primario para esa denominación, o conservar literalmente el nombre histórico de la ficha distinguiendo la época. No inventar continuidad actual.
- **Prueba de cierre:** cotejo letra por letra con fuente primaria y referencia que sostenga el nombre elegido.

### U01-A-004 — P3 — Texto alternativo cuenta una lámpara donde hay dos

- **Ubicación:** `apuntes/practica/tp-01-comunicaciones.md`, E4, ancla `ejercicio-4--dos-lámparas-en-serie-con-protección`, **línea 123**.
- **Afirmación:** alt «una lámpara en serie».
- **Evidencia:** original `capturas/practica/image-8.png`, visto individualmente: **LAMP1 y LAMP2**; copia `assets/tp-01-lamparas-serie.png` idéntica. Consigna E4 del enunciado PDF p. 2 solicita dos; Mermaid y explicación también tienen dos.
- **Naturaleza:** **demostrado**, editorial/accesibilidad, no error en el circuito.
- **Consecuencia:** el lector que depende del alt recibe una descripción contradictoria con el ejercicio.
- **Acción mínima:** cambiar únicamente «una» por «dos» o describir explícitamente las dos lámparas y la protección.
- **Prueba de cierre:** alt coincide con original y consigna; SHA de PNG sigue idéntico.

## 8. Dictamen y límites de aprobación

El contenido conceptual desarrollado es consistente con la cátedra en CD/ED, teleinformática, canales introductorios, Internet, normalización y OSI; los veinte ejercicios están presentes y todos los resultados numéricos recalculados son correctos. El TP existente debe preservarse: las correcciones solicitadas son puntuales y demostradas. Las exclusiones explícitas no cuentan como huecos escondidos.

**No procede aprobar aún:** corregir U01-A-001 y la matriz de evidencia U01-A-002; atender dos erratas P3. Para certificación de todas las referencias externas queda por inspeccionar el PDF/registro ENACOM exactos y recuperar las páginas IBM citadas o documentar formalmente el contraste alternativo. No se afirma QA visual Mermaid ni lectura integral de libros/sitios. La excepción del autocontrol embebido impide describir esta revisión como perfectamente ciega; el contraste propio completo está registrado para auditarla.

No se hicieron cambios correctivos, por la espera de los trece dictámenes iniciales. Un cierre posterior debe comprobar cada prueba de cierre y hashes originales de nuevo. No basta cambiar `estado` ni aceptar una autocertificación. Si se pide U1 programática completa, se requiere material autorizado para los tópicos excluidos; no expandir desde bibliografía. U7/U8 siguen fuera del alcance.

## Key Learnings:

1. El cache U1 omite la lámina histórica visual PDF2: ausencia de texto extraído no demuestra ausencia de evidencia.
2. En T23,1960se atribuye a ARPA; corregirlo contra1958, no contra el inicio de ARPANET1969.
3. Revisar todas las cuentas y fuentes locales no equivale a certificar un PDF externo inaccesible ni el render de un grafo Mermaid.


---

## Dictamen B

# Dictamen independiente U01-B — Pedagogía y cobertura integral

**Fecha:** 2026-10-13. **Revisor:** B, independiente, no autor. **skill_resolution:** injected.

**Resultado:** REQUIERE CAMBIOS. P0: 0; P1: 0; P2: 2; P3: 2. No aprobación integral final: además de los hallazgos, falta contraste reproducible de las dos fuentes ENACOM de TP E20. Esto no demuestra que E20 sea falso. No se corrigió ningún candidato.

## 1. Identidad, independencia e integridad

Raíz absoluta de todos los identificadores relativos de este informe: `C:/Users/Martin/Documents/UTN_SISTEMAS/Anual_2026/comunicacion_de_datos/`.

Abreviaturas de ubicación, inequívocas:

- **A:** `C:/Users/Martin/Documents/UTN_SISTEMAS/Anual_2026/comunicacion_de_datos/apuntes/teoria/01-introduccion-comunicaciones/APUNTE.md`.
- **P:** `C:/Users/Martin/Documents/UTN_SISTEMAS/Anual_2026/comunicacion_de_datos/apuntes/practica/tp-01-comunicaciones.md`.
- **R:** `C:/Users/Martin/Documents/UTN_SISTEMAS/Anual_2026/comunicacion_de_datos/apuntes/repaso/u01-introduccion-comunicaciones.md`.

Snapshot: `docs/consolidacion-u1-u6/snapshot-inicial.json`; SHA256 `1e29fd3bf30b9d99d07e0d3b73e2d7ef11f9d85bb7874b2630650412068a7bdd`.

| Candidato | SHA256 revisado |
|---|---|
| A | `daa739d206799c359d8ae9d9679bebf88a418f7a56da81a20b2e6336715a2dbf` |
| P | `fc8859722d0ab0378c67c83d4ed74e0ffeff6847bcd421a04e1aa01af7b0a1a8` |
| R | `aa78886b59798c54b4f5f696a16617ce857c6e47a1865795e465d18c0ddaf044` |

Se recuperó sólo checkpoint propio; no se consultaron informes ajenos, `estado.md`, conclusiones de autores ni `tmp/autor-*`. A se leyó entero, incluida su estructura final, pero la autocertificación NO fue evidencia. El registro de imágenes sirvió como objeto candidato/rutas; se verificaron copias de manera independiente. Las certificaciones globales comunicadas por coordinación no sustituyen este QA.

Lectura de AGENTS y metodología completa al inicio. Hash inicial propio `hashes-antes.json`, checkpoint ampliado `hashes-checkpoint.json` y contraste final `hashes-despues.json`, bajo `tmp/reviews/u01-b/`: **83 archivos, cero diferencias con snapshot y checkpoint**. La selección incluye imágenes de otras clases únicamente para integridad; NO se afirma haber revisado académicamente esas imágenes. El libro y programas que se utilizaron también están hasheados. No se hizo auditoría global de todos los originales del repositorio.

## 2. Cobertura efectivamente realizada

### Candidatos, capturas y originales

| Objeto | Lectura/contraste efectivo |
|---|---|
| Carpeta teórica U1 | A completo, sus once secciones; INDICE completo; registro completo; siete figuras y sus originales. `.gitkeep` sólo integridad. |
| P | Completo: símbolos, supuestos, veinte enunciados/resoluciones, diagramas E4/5/17/18, resúmenes y checklist. No se aprobó automáticamente por preexistir. |
| R | Completo: alcance, trazabilidad, Q1–Q3, soluciones y cada distractor. |
| Captura teórica U1 | `capturas/teoria/01-introduccion-comunicaciones/Apuntes-clase 1.md` completa, incluido OSI detallado, Internet e IXP. |
| Captura práctica inicial | `capturas/practica/clase 01.md` completa, conceptos, diez imágenes y veinte consignas. |
| Cuestionario U1/U2 | `capturas/teoria/Cuestionarios/cuestionario U1 y U2.md` completo para delimitar; Q1–Q3 contrastadas, Q4–Q7 de U2 excluidas. |
| Búsqueda de otras capturas | Búsqueda textual transversal en Markdown de `capturas/` por U1/teleinformática/OSI/Internet/TP1/Ohm. Clase02 identificada como U2; menciones de Internet en clase05 pertenecen al desarrollo U3. No se agregaron preguntas ni programas de otras unidades. |

### Páginas originales visualmente inspeccionadas, no sólo extraídas/renderizadas

| Fuente original | Páginas PDF vistas | Tratamiento y figuras comprobadas |
|---|---:|---|
| `material/teoria/U1/U1 Introduccion a las comunicaciones.pdf` | **1–25, todas** | Evolución p2; definiciones/modalidades pp3–5; límites ED/CD p6; canal analógico p7 y digital/A-D-A p8; organismos p9; OSI pp10–20 con pares, interfaces, encapsulación y siete capas; IoT/IIoT pp21–22; cronología p23; mapa RIR p24; IXP p25. |
| `material/practica/U 1/UT 1 COMUNICACIONES.pdf` | **1–10, todas** | Transmisión, teleinformática, circuito, modelos analógico/digital/A-D-A, red/Internet/OSI y sus figuras. |
| `material/practica/U 1/Organismos  UT 1.pdf` | **1–3, todas** | Nombres y funciones, errores históricos y distinción de normalización/regulación. |
| `material/practica/U 1/TP 1  2026.pdf` | **1–3, todas** | Veinte consignas, valores/unidades y pedidos de diagramas. |
| `material/practica/U 1/TP1-respuestas y resumen.pdf` | **1–3, todas** | Fórmulas/símbolos y esquema p1; resultados y respuestas p2; interpolación de cable p3 identificada como ajena al TP oficial. |
| `material/catedra/PROGRAMA de la materia.pdf` | **2** | Apartado U1, contraste de alcance; no se afirma revisión visual de todo el programa. |
| `material/catedra/Programa comunicacion de datos Año 2026 - martes jueves 2do cuat K3673.pdf` | **1–2, todas** | Cronograma: U1 y repaso de Física, carácter híbrido y parcial U1–U4. No altera alcance registrado. |
| `material/teoria/DOC-20230425-WA0040.pdf` | **169–171 y276–282**, todas las páginas de estos rangos | Definiciones de procesamiento/tiempo real; capas OSI y diagramas de encapsulación. Bibliografía para aclarar, NO nuevos temas. No se leyó el libro entero. |
| `material/teoria/CAPITULOS DEL LIBRO DE LA CATEDRA-20260813/Capitulo_1a.pdf` | **1–13, todas** | 73 diapositivas: historia, sociedad, redes, organización y normalización. Se revisó como contraste bibliográfico; no se reclama convertir todo su contenido en temario registrado. |

**Total: 70 páginas PDF originales pertinentes visualmente revisadas.** Se usaron planchas de cuatro páginas para filminas legibles y páginas individuales para detalles densos; se recorrieron todas las páginas enumeradas, no una muestra. Renders propios en `tmp/reviews/u01-b/`. Poppler emitió advertencias de fuentes Symbol/ArialUnicode al renderizar ciertos documentos; el contenido relevante se mantuvo legible y se contrastó con extracción. No se interpreta la advertencia como validación de glifos invisibles.

**Raster originales:** `capturas/practica/image.png`, `image-1.png` a `image-9.png`, más `material/practica/U 1/CONEXION LLAVE TERMICA.jpg`: **11 inspeccionados visualmente**. Las siete copias teóricas y tres assets TP coinciden byte a byte con sus diez originales: `copias-imagenes.json`. El circuito inferior RLC del collage no se toma como modelo universal de CA; el texto limita ese collage a contexto visual.

Los caches U1, TP y programa se usaron para búsqueda/lectura auxiliar. Ninguna cifra, límite CD/ED ni corrección de rótulo se validó exclusivamente por cache. En particular, p2 del PDF teórico evidencia información gráfica que no aparece adecuadamente en extracción textual.

## 3. Tabla original → destino/tratamiento

T1 = captura teórica clase1; P1 = captura práctica clase01; T = PDF teórico U1; UT = PDF práctico comunicaciones.

| Fragmento original | Destino comprobado | Tratamiento y juicio |
|---|---|---|
| T1 líneas1–4: parciales/híbrido/ruta PPT | No concepto teórico; cronograma original2026 | Contexto administrativo. No pérdida académica. Ruta histórica no se reescribe. |
| T p2: computación y comunicaciones1950–2000, centralización/distribución/integración | Sin destino específico; A línea46 afirma ausencia | Exclusión de historia expresamente declarada; no se registra como error. Para mejor trazabilidad, conviene distinguir este fragmento disponible de temas sin evidencia. |
| T pp4–5; T1 líneas27–33; P1 líneas3–5 | A §1 | Integra disciplinas, centralizado/distribuido, modalidades, ejemplos y criterio online/offline. Interactivo diferido explícitamente provisional, no evaluado. |
| T p3; T1 líneas18–25; P1 líneas7–24 | A §2 y P E16 | Señal física, local/remoto/punto-multipunto, cadena funcional; confiabilidad/seguridad/tiempo real como objetivos, no garantías. Ruido/distorsión/atenuación secundarios, detalle U6. |
| T p6; UT p4; T1 líneas8–15; P1 image.png | A §3; R Q1 | CD=ECD+medio+ECD; ED incluye relación entre ETD. Corrige la omisión del medio en captura sin tocarla. |
| T p7/UT p5; P1 images1–2 | A §2 canal analógico | Explica adaptación a portadora, modulación/demodulación y bloques; corrige «modulación» del receptor original. No da bits por el aire como abstracción física literal. |
| T p8/UT p6; P1 images3–4 y frase «bits directamente» | A §2 canal digital | Codificación de línea/ECTD/regeneración; diferencia sin portadora de ausencia de representación física. Interior filtro/COD/DECOD preservado. |
| T p8/UT p7; P1 image5 y líneas43–44 | A §2 A-D-A | Muestreo/cuantificación/codificación como anticipo; no invade PCM cuantitativo U4. |
| P1 líneas46–64; UT pp8–9 | A §4; P E15/17 | Topologías y extensión con ejemplos; host/interfaz IP/router/red autónoma. No identifica Internet con una estrella universal. |
| T pp21–22; T1 líneas141–142 | A §4 | IoT/IIoT definidos con ejemplo doméstico/industrial y relación al concepto de red. Sólo anticipo, no catálogo industrial nuevo. |
| T p23; T1 evolución vacía; clave TP p2 E14 | A §4; P E14 | Separa organismo y red, NIC e IANA históricos. Las fechas se verifican con primarias; TP atribuye mal «1960»: **U01-B-002**. |
| T p24 RIR; bibliografía DNS/gobernanza | A §4 IANA; resto excluido | IANA categorías y coordinación introducidas. Mapa vigente, cifras y gobernanza ampliada explícitamente fuera. No error por no importar todo el libro/mapa. |
| T p25; T1 líneas148–153 IXP/NAP y enlaces | A §4 | Conserva función intercambio, modelo mental/ejemplo; poster2024, cifras, video y despliegue actual no se presentan como evidencia vigente ni nuevos objetivos evaluables. |
| T p9; T1 líneas36–38; P1 UIT/ENACOM; Organismos pp1–3 | A §5; P E13/19 | Normalización vs regulación; expansiones/función introductoria y advertencias históricas. UIT-T estructura mejor desarrollada en TP. EIA error editorial: **U01-B-003**. |
| T pp10–13; T1 líneas40–63; P1 image6 | A §6; R Q2/3 | OSI, siete capas, pares/protocolo, adyacentes/interfaz, servicios/entidades/PDU; ejemplo extremo a extremo. No se exige tamaño de trama ni stack real de siete dispositivos. |
| T pp14–20; T1 líneas65–135 | A §6 tabla y ejemplo | Todas las responsabilidades centrales listadas; corrige UDP confiable, ubicación total de FrameRelay y equivalenciaV24/RS232. Algunos términos sólo repetidos: **U01-B-001**. |
| P1 fórmulas líneas71–86; clave p1 | P símbolos/supuestos y E1–3/6–11 | Resistividad, área no diámetro, potencia vs energía, conversiones y resistencia constante. Glifos verificados en original. |
| P1 image7–9; enunciado E4–7; llave térmicaJPG | P E4–7 | Serie/paralelo, protección bipolar acoplada explicada como esquema académico; no instrucción de instalación. Alt E4 inexacto: **U01-B-004**. |
| TP E12–20 / P1 líneas130–143 / clavep2 | P E12–20 | Todas las consignas tienen respuesta; esquemasE17/18 siguen centralización solicitada. E20 acceso fijo tratado sin prometer cobertura, pero ENACOM pendiente de contraste revisor. |
| Clave p3 interpolación RG213 | Exclusión expresa P línea27 | Fuera del enunciado TP; no es pérdida silenciosa ni obligación de incorporar U7. |
| Cuestionario Q1–3 | R Q1–3, referencias A §3/6 | Enunciados separados de claves; alternativas y justificación de cada distractor comprobadas. |
| Cuestionario Q4–7 / U7/U8 | Fuera U1 | Exclusión expresa, no error de cobertura. V24 sólo asociación física introductoria. |
| Capitulo1a historia/sociedad/economía/gobernanza ampliada | Contraste, no incorporación automática | No se usa bibliografía para expandir temario. El fragmento visualT p2 existe, pero la historia está explícitamente excluida del alcance y no se la exige. |

## 4. QA académico y pedagógico real

### Progresión de aprendizaje

| Núcleo | Resultado independiente |
|---|---|
| Teleinformática/explotación | Problema de equipos separados→procesamiento/comunicación→comparación funcional→ejemplos. Diferencia tiempo real y simple rapidez; modalidad dudosa visible y no examinada. No corresponde inventar fórmula numérica para categorías cualitativas. |
| Transmisión/canal | Parte de necesidad de representar información físicamente, no de una fórmula. Modelos analógico/digital/A-D-A con lectura de bloques y errores típicos. Suficiente para explicar la cadena introductoria. |
| Circuito/enlace | Límites de componentes claros, diagrama→interpretación→error original→respuesta de oral. No resta el medio ni elimina el segundo ECD por el singular de Q1. |
| Redes/Internet | Distinción red/host/router/organismo/IXP; modelos y casos concretos; alcance acotado. La exclusión histórica es explícita y admisible; la atribución del TP necesita incidencia002, sin reemplazar el núcleo correcto. |
| Normalización | Concepto secundario con problema interoperabilidad, organismos y función mínima; TP E13 responde constituciónUIT-T. No requiere ocho bloques repetidos por organismo. |
| OSI | Tiene motivación, relaciones, tabla, ejemplo, errores y respuesta de examen. Falla puntual: varios nombres funcionales siguen sin modelo mental concreto (001). El ejemplo no demuestra por sí solo esos términos. |
| Cierre/navegación | Resumen mental, checklist y enlaces funcionales; estados en-progreso A/completo P/R no equivalen a revisado. No se detectó falsa etiqueta revisado. |

### Fórmulas, resultados y veinte ejercicios

Recalculados con Python propio y contraste manual de dimensiones; archivo `calculos.json`. Relaciones $V=RI$, $R=\rho L/S$, $S=\pi d^2/4$, $P=VI=V^2/R$, $E=Pt$, serie y paralelo. Tabla común define todos los símbolos/unidades; conductor uniforme y carga resistiva ideal, $R$ constante en variación de tensión. No se comparan W y kWh como si fueran equivalentes.

| Ejercicio | Prueba realizada / resultado |
|---|---|
| 1 | $120/3=40\ \Omega$. Coincide. |
| 2 | $20\cdot16/4000=0,08\ \Omega\,mm^2/m$. Conversión km→m correcta. |
| 3 | $S=5,3092916\ mm^2$; $L=3318,3072\ m\simeq3,32\ km$. Redondeo candidato compatible. |
| 4 | Dos lámparas serie; único camino; apertura de una apaga ambas; QF dos polos del mismo aparato. Figura original tiene dos, no una. |
| 5 | Dos ramas paralelas; nodo común y retorno; protección anterior/posterior a bifurcación acoplada. Apertura de rama no interrumpe la otra. |
| 6 | $R_T=100/1=100\ \Omega$; $R_3=100-2-8=90\ \Omega$. Figura distingue equivalente de incógnita. |
| 7 | $R_T=(1/2+1/10+1/8)^{-1}=1,37931\ \Omega<2\ \Omega$. |
| 8 | TV1,6kWh; calefactor1,5kWh; total3,1kWh; costo$186. El de menor potencia puede gastar más por el tiempo. |
| 9 | $V=25/2,5=10\ V$; $R=4\ \Omega$. |
| 10 | Con Rconstante, $15^2/4=56,25\ W$. Supuesto explícito, no ley real de lámpara caliente. |
| 11 | $R=220^2/1100=44\ \Omega$; $P_{200}=909,09\ W$; caída17,355%≈17,36%. |
| 12 | Informática+telecomunicaciones, integración funcional, no disciplinas desconectadas. |
| 13 | UIT-T exCCITT, funciones de recomendación; WTSA/TSAG/grupos/TSB contrastados con UIT. No confundido con legislación nacional. |
| 14 | Agencia vs red correcto; cuatro nodos1969; MILNET cronograma1983 vs reseña1984 no promediados. Incidencia de atribución002. |
| 15 | Hosts y routers; IP a interfaz; red de redes con interconexión mallada, no exige malla completa. |
| 16 | Datos codificados representados en señales físicas; no garantiza ausencia de errores. |
| 17 | Mermaid cuatro sedes cada una conLAN, WAN privada y salidaInternet única central. Consigna respetada. |
| 18 | Mainframe procesamiento central, terminal local y remoto con comunicaciones; no fija tecnología inexistente en consigna. |
| 19 | ISO/IEEE/ANSI/EIA con función; IEEEE original normalizado; expansiónEIA003. |
| 20 | FunciónISP y seis categorías acceso fijo, no velocidades/precios inventados. FuenteENACOM fechada: pendiente revisor; no aprobar por aparente plausibilidad. |

**Resultado aritmético:** cero errores numéricos demostrados. Diagramas Mermaid se inspeccionaron en su fuente y por estructura de nodos/flechas; **no hubo build ni render Mermaid independiente**. No se certifica presentación gráfica del renderer.

### Repaso

- Q1: opción5 confirmada por límitesCD originalT p6/UT p4; texto explica dosECD pese al singular. Las otras cuatro alternativas analizadas, no sólo clave repetida.
- Q2: b, V24 física; compresiónpresentación, protocolospares, ISO noIEEE. Evidencia originalT pp10–20 y título/alcanceV24.
- Q3: a incorrecta, IEEE; protocolospares/criptografíacapa6/V24capa1 correctos en nivel registrado. Se explica también alternativa«ninguna».
- No respuestas adelantadas en enunciados, separación secciones, criterios de corrección y rutas a fuente/estudio. No se evalúa interactivo diferido como confirmado ni Q4–7 deU2.

### Fuentes externas primarias contrastadas

Sólo verifican afirmaciones ya candidatas, no agregan temario:

- Función/estructura UIT-T y origen CCITT: [estructura UIT-T](https://www.itu.int/en/ITU-T/about/Pages/framework.aspx), [historia UIT](https://www.itu.int/en/history/Pages/FocusOnStandardization.aspx), [UIT-T](https://www.itu.int/en/ITU-T/about/Pages/default.aspx).
- Historia: [ARPANET DARPA](https://www.darpa.mil/news/features/arpanet), [ARPA→DARPA](https://www.darpa.mil/about/innovation-timeline/arpa-becomes-darpa), [NSF historia](https://www.nsf.gov/about/history); cronograma literal [RFC881](https://www.rfc-editor.org/rfc/rfc881.html) y reseña posterior [RFC1302](https://www.rfc-editor.org/rfc/rfc1302.html). No se trató un plan como certificación de ejecución.
- NIC y registros históricos: [RFC82](https://www.rfc-editor.org/rfc/rfc82.txt), [RFC95](https://www.rfc-editor.org/rfc/rfc95.html), [RFC349](https://www.rfc-editor.org/rfc/rfc349.txt), [RFC1083](https://www.rfc-editor.org/rfc/rfc1083.txt); distinción actual [IANA](https://www.iana.org/about).
- Precisión técnica: [UDP RFC768](https://www.rfc-editor.org/rfc/rfc768.txt), [FrameRelay RFC1490](https://www.rfc-editor.org/rfc/rfc1490.txt), [V24 UIT](https://www.itu.int/rec/T-REC-V.24/en).
- Normalización: [ISO](https://www.iso.org/about), [ANSI](https://ansi.org/about/introduction), [IEEE catálogo](https://standards.ieee.org/standard/), [Electronic Industries Alliance, NIST](https://csrc.nist.gov/glossary/term/electronic_industries_alliance).
- IBM glosario online/offline y documentación indexada de batch/time-sharing: [glosario](https://www.ibm.com/support/pages/zvm/library/glossary/index.html), [batch/online](https://www.ibm.com/docs/en/zos-basic-skills?topic=today-mainframe-workloads-batch-online-transaction-processing), [time-sharing](https://www.ibm.com/docs/en/zos/3.2.0?topic=operations-controlling-time-sharing). Las dos últimas aperturas directas fallaron; se consultó contenido indexado oficial y se trianguló con Castro169–171. No equivale a inspección íntegra de esos sitios.

**Enlaces locales:** 109 comprobados, cero archivos/anchors Markdown inexistentes. Incluye A/INDICE/registro/P/R, URLs decodificadas y anchors explícitos/derivados; comprobador propio `qa-final.py` y detalle `enlaces-locales.json`. Para PDF sólo se comprobó archivo; páginas citadas contrastadas visualmente en la lista de arriba. No se validaron todos los enlaces externos del repositorio.

## 5. Incidencias accionables

### U01-B-001 — P2 — OSI conserva vocabulario sin suficiente significado operativo

- **Ubicación:** A `#modelo-osi`, **líneas416–419 y441–447**.
- **Claim:** sesión administra testigo; transporte multiplexa/regula flujo; enlace asegura transparencia; red trata congestión.
- **Evidencia:** T **pp15–18**, funciones enumeradas; T1 **líneas79–80,89,102–110**; bibliografía local **PDF277–281** aclara funciones. Metodología §3 «Nada colgado» y conceptos secundarios definición+ejemplo+relación. En el candidato no se define qué testigo se administra ni qué hace transparente una delimitación; «multiplexa» y «congestión» siguen como nombres. El ejemplo posterior repite transferencia/calidad/diálogo sin concretarlos.
- **Naturaleza:** faltante pedagógico demostrado, no falsa ubicación de capas. No exige implementar protocolos, tramas o multiplexación cuantitativa deU4.
- **Consecuencia:** alumno puede recitar tabla, pero no explicar en oral estas responsabilidades ni distinguir regulación de flujo de congestión.
- **Acción:** pequeñas aclaraciones/ejemplos cualitativos de esos términos ya registrados, con procedencia: permiso de diálogo, preservar datos al delimitar, separar conversaciones sobre servicio común, receptor lento vs red sobrecargada. No forzar fórmulas nuevas; definir antes del ejemplo las siglas que se conserven como ejemplos de protocolos.
- **Prueba de cierre:** alumno explica cada uno con caso de una frase sin repetir el nombre; señala capa y problema que resuelve, sin arquitectura ampliada. Revisar coherencia con fuente y que «testigo» de sesión no se confunda con TokenRing de enlace.

### U01-B-002 — P2 — Comparación histórica atribuye una fecha al objeto equivocado

- **Ubicación:** P **línea294**, `#ejercicio-14--redes-y-organismos-vinculados-con-el-origen-de-internet`.
- **Claim:** fecha1960 de filmina no coincide con inicioARPANET1969.
- **Evidencia:** T **p23**: el texto1960 refiere a **ARPA**; el gráfico de la misma página muestra **ARPANET1969**. P líneas287–288 ya distingue agenciaARPA1958 de redARPANET1969; la comparación final pierde esa distinción. Original y [DARPA](https://www.darpa.mil/news/features/arpanet) sostienen1969 para red.
- **Naturaleza:** atribución/procedencia demostrada; la fechaARPANET1969 del candidato es correcta. No controversia sobre1983/1984MILNET.
- **Consecuencia:** falsa contradicción original↔fuente, estudiante aprende a corregir fecha de agencia con inicio de red; perjudica precisamente la distinción de E14.
- **Acción:** si se conserva nota, describir errorARPA1960 frente a establecimientoARPA1958 con primaria pertinente y reconocer que el gráfico sí fechaARPANET1969.
- **Prueba de cierre:** cada fecha tiene organismo/red e hito propios; comparación visual p23 no atribuye1960 aARPANET y coincide con tabla y A§4.

### U01-B-003 — P3 — Expansión inglesa de EIA mal escrita

- **Ubicación:** P **línea368**, E19 tabla.
- **Claim:** «Electronics Industries Alliance».
- **Evidencia:** `Capitulo_1a.pdf` **p12, diapositiva72**: Electronic Industries Alliance; [NIST denominación](https://csrc.nist.gov/glossary/term/electronic_industries_alliance). `Organismos UT1.pdf` p1 usa variante histórica distinta, que no justifica formar esta expansión híbrida.
- **Naturaleza:** demostrado editorial; no se reclama asignarle vigencia actual ni cambiar toda la historia institucional.
- **Consecuencia:** memorizar expansión defectuosa en consigna explícita de definir siglas.
- **Acción:** «Electronic Industries Alliance», mantener advertencia histórica y fuente inequívoca.
- **Prueba de cierre:** expansión textual coincide con fuente; no nuevo claim de operación actual.

### U01-B-004 — P3 — Texto alternativo cuenta una lámpara donde hay dos

- **Ubicación:** P **línea123**, E4 imagen `assets/tp-01-lamparas-serie.png`.
- **Claim:** «una lámpara en serie».
- **Evidencia:** original `capturas/practica/image-8.png` y copia byte-idéntica: **dos lámparas**; consignaTP p2 E4 y MermaidP líneas117–118 también dos.
- **Naturaleza:** demostrado editorial/accesibilidad, no error del circuito.
- **Consecuencia:** descripción alternativa contradice la tarea y figura para quien depende del texto.
- **Acción:** corregir alt a dos lámparas; no editar bytes originales.
- **Prueba de cierre:** alt, esquema y consigna coinciden.

## 6. Límites, pendientes y dictamen

1. **ENACOM E20:** fallaron apertura web de [prestadores](https://www.enacom.gob.ar/informacion-de-prestadores_p1346), [Resumen2025T4](https://indicadores.enacom.gob.ar/files/informes/nacionales/2025/T4/2025T4-01%20-%20Resumen.pdf) y portal de informes; acceso directo Python falló por DNS. No se descargó sustituto ni se aceptó copia autoral. Quedan sin contraste independiente la atribución regulatoria específica y el gráfico/seis categorías/«otros». La descripción genérica de medios es plausible, pero no confirma que el informe respalde exactamente la fila «fibra hasta domicilio». **Limitación de revisión, no issue de falsedad.** Cierre: recuperar original fechado o copia local trazable, verificar gráfico y distinguir categoría general fibra de la arquitectura residencial concreta descrita.
2. No revisión de todo el libro726p, todos los programas ni toda Internet: sólo los rangos y afirmaciones declarados. Bibliografía no incorpora contenido nuevo de U1 ni U7/U8.
3. No simulación del aprendizaje con una persona ni evaluación interactiva realizada: las pruebas de cierre pedagógicas son criterios propuestos, no resultados obtenidos.
4. No render finalMarkdown/Mermaid ni build; QA de esos diagramas es estructural. No certificación de cada URL externa.
5. Modalidad interactivo diferido permanece provisional honesta; no se la examina como respuesta confirmada. No se penalizan exclusiones explícitas que sean auténticas y trazables.

**Dictamen:** revisión documental local integral del alcance registradoU1 efectuada, con límites externos explícitos. La organización conceptual y el TP cuantitativo son sólidos; repasoQ1–Q3 tiene claves y distractores confirmados. Las dos incidenciasP2 impiden recomendar cierre pedagógico/procedencia como revisado, y ENACOM impide afirmar contraste integral de todas las fuentes de TP. Solicitar cambios focalizados y reverificación. No corresponde rehacer unidad entera, añadir temario bibliográfico ni corregir candidatos antes de reunir los trece dictámenes iniciales.

## Key Learnings:

1. Una filmina gráfica puede contener historia registrada que el cache no recupera: evidencia visual antes de declarar ausencia.
2. Fechas de organismo y red son objetos distintos; una corrección histórica debe conservar el hito.
3. Una tabla OSI completa no asegura comprensión si responsabilidades como testigo y transparencia quedan sólo nombradas.
4. Fuentes externas inaccesibles limitan aprobación; no prueban por sí mismas error académico.
