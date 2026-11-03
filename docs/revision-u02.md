# Revisión U02 — A/B

## Dictamen A

# Dictamen académico independiente U2 — Revisor A

Fecha cliente: **2026-10-13**. `skill_resolution: injected`.

## 1. Dictamen

**REQUIERE AJUSTES MENORES PEDAGÓGICOS Y DE TRAZABILIDAD.** P0: **0**; P1: **0**; P2: **3**; P3: **1**.
No encontré error matemático demostrado en los ejemplos, E1–16 o las 19 claves de repaso. No equivale a
certificar todo el programa ni autoriza cambiar `estado: en-progreso` a `revisado`. Hay exclusiones
expresas legítimas y límites de evidencia detallados abajo. No realicé correcciones.

IDs abiertos: **U02-A-001, U02-A-002, U02-A-003, U02-A-004**.

## 2. Independencia, versión e integridad

- Leí AGENTS.md y la metodología. Contrasté contenido y no acepté como prueba las autocertificaciones
  embebidas de QA. No leí informes de autores, otros revisores, `tmp/autor-*`, `estado.md` ni memoria ajena.
  La compatibilidad se comprobó contra archivos históricos, no contra conclusiones del autor.
- Identificación: HEAD `1f7384f49d656fac144da87e53db47345fcae289`, más estado de trabajo definido por
  `docs/consolidacion-u1-u6/snapshot-inicial.json`. La revisión es del contenido con esos hashes,
  no sólo del commit.
- Calculé SHA-256 propios de **401 entradas** antes y después: **0 diferencias** contra snapshot y
  **0 modificaciones durante la revisión**. Evidencia: `u02-a/hashes-antes.json`,
  `u02-a/hashes-despues.json`, `u02-a/qa-resultados.json`. Entre esas entradas hay 286 de `capturas/`
  o `material/`, incluidas 43 de `_cache`; ese conteo NO pretende ser el número de originales académicos.
- Comparé también rutas actuales de `apuntes/`, `capturas/` y `material/` con snapshot: **0 rutas adicionales**
  al cierre. No tengo inventario inicial propio de rutas no registradas fuera de esas carpetas.
- Las **4 copias PNG** coinciden byte a byte con originales mediante cálculo propio; no usé el campo
  `igual` del manifest como certificación. Sólo escribí este informe y recursos propios.

## 3. Cobertura efectiva de candidatos

Prefijos de esta tabla: T=`apuntes/teoria/02-senales-telecomunicaciones/`, P=`apuntes/practica/`,
R=`apuntes/repaso/`. Líneas de la versión auditada; páginas siempre PDF salvo indicación.

| Archivo / sección exacta | Cobertura y pruebas | Autoridad contrastada |
|---|---|---|
| T/APUNTE.md, portada y mapa, 1–56 | Fuentes, límites, estado y ubicación; no ampliar programa | Programa pp.2–3; capturas asociadas; fuentes de la tabla siguiente |
| `#senales`, 58–102 | Valores continuos/discretos, regeneración, umbrales hipotéticos 0/2 V con umbral 1 V; ejemplos 1,7/0,8 V, límite de decisión equivocada | U2 pp.2–3; UT2 señales pp.2–3; libro p.98 |
| `#parametros`, 104–171 | Seno, f/T/ω/fase, FRP/τ, media firmada/RMS; todas las fórmulas y ejemplos | U2 pp.12–14,24,27–28; libro pp.99–105; TP E4,6,7 |
| `#fourier`, 173–312 | Dirichlet, paridad, representación trigonométrica, integrales, cuadrada impar, armónicas, instrumentos, efecto del canal, discontinuidad/Gibbs | U2 pp.15–24; libro pp.105–112; Práctica 3; respuestas 2 p.1 |
| `#tren`, 314–441 | Compleja normalizada, sinc, desplazamiento, Dn vs Cn, conjugados/factor 2, signos/fase, todos los renglones E10 | U2 p.16/24; libro pp.108–110; respuestas 2 pp.2–4; PDF cuestionario pp.1–3 |
| `#ancho-banda`, `#primer-cero`, 444–599 | AB de señal/canal, infinito/aproximado, 3 dB, primer cero, conteo bilateral/unilateral, ejemplo 200/3600 Hz | U2 pp.7,22–24; libro pp.112,134–138; Teoría U3 clase 4; TP E9–12 |
| `#db-contexto`, 600–615 | Datos de equipo y conversiones logarítmicas; supuestos potencia/tensión, enlace a U6; sin extender U7 | U2 pp.4–11; Teoría 2 |
| `#oem`, 618–685 | E/H viajera, corrección dimensional, λ/T, polarización, escalas/bandas, alcance y energía no universales | U2 pp.25–29; UT2 señales pp.10–12; Práctica 2; hallazgo 002 |
| `#codigos`, 688–766 | Banda base, ejes de clasificación, media continua, 10 reglas y ejemplo completo 10110, Ethernet/TokenRing acotados | U2 pp.30–42; Banda Base pp.2,6–30; cuadro pp.1–3; UT2 codificación p.1; libro pp.139–153; hallazgo 001 |
| `#hdb3`, 768–790 | 000V/R00V, paridad, estado, signos y recuperación; ejemplo 111/0000/0000/0101 | U2 p.39; Banda Base pp.25–26; libro pp.154–155 |
| códigos secundarios/análisis, 792–836 | Miller, CMI, 2B1Q, 4B3T; B6ZS sólo como pendiente; espectros y límites PSD/BER | U2 pp.43–46; cuadro pp.2–3; Banda Base pp.31–33; libro pp.153–155; hallazgo 003 |
| `#filtros`, 839–891 | Cuatro tipos, 4 ejemplos, B, corte/real/ideal/selectividad, LC/cristal/activo | U2 pp.47–48; libro pp.156–159; Teoría 4 |
| `#pendientes`, 894–905; cierre, 928–949 | Pendientes honestos, resumen/checklist; QA 907–926 no se usó como evidencia | Confrontación propia anterior, metodología |
| T/INDICE.md | Navegación completa, 7 anclas históricas | Baseline `ee66ef7` y destinos actuales |
| T/serie-de-fourier.md; ancho-de-banda.md | Ambos stubs completos; 14+16 anclas históricas, sin segundo cuerpo teórico | `git show ee66ef7:<ruta>`; preguntas antiguas cotejadas con F09–14 |
| T/compatibilidad.md | Mapa de destinos y enlaces comprobados; afirmaciones de autor sobre QA/no-edición no se aceptaron como evidencia | Baseline y SHA/enlaces propios |
| T/recursos/manifest.json; `.gitkeep` | Manifest utilizado sólo como inventario de 4 pares; hashes propios; marcador vacío | Originales de cada par |
| P/tp-02-senales.md, 1–372 | Todo el desarrollo de E1–16, supuestos, gráficos, tablas, trampas y cierre; QA autor no es prueba | TP original pp.2–3 y hojas oficiales completas |
| R/u02-senales.md, 1–67 | S04, S05, S06, S07: opciones, clave, razonamiento y límites | Cuestionario U1/U2 Q4–7; U2 p.20,32–34,39,48; cuadro; libro p.134/157 |
| R/u02-fourier-y-ancho-de-banda.md, 1–89 | F01–F15: cada enunciado/clave; F06–08 y F15 recalculados; F10/13 escalamiento; legado preservado | Pilotos/ficha en `ee66ef7`; cuestionario U3 Q2; U2/Fourier/AB originales |

### TP2: tabla exacta de ejercicio y recálculo

| ID | Qué comprobé / resultado independiente | Páginas originales relevantes |
|---|---|---|
| E1 | Ambos esquemas ASCII y interpretación; bordes ideales no implican banda finita | TP p.2; U2 pp.2–3; UT2 pp.2–3 |
| E2 | Las 5 ventajas y desventaja coinciden con enfoque docente; salvedades evitan leyes universales | TP p.2; respuestas 1 p.1; Práctica 2 |
| E3 | Decisión + forma/amplitud + reloj; error de decisión puede regenerarse limpio | TP p.2; respuestas 1 p.1; libro p.98 |
| E4 | A=300 V, ω=100π rad/s, f=50 Hz,T=20 ms,φ=90°,v(0)=300 V, media=0,RMS=212,132 V; λ no inventada sin v | TP p.2; U2 pp.12–14; libro pp.99–105 |
| E5 | 88 MHz→3,40909 m;108 MHz→2,77778 m; truncamiento oficial diferenciado de redondeo | TP p.2; respuestas 1 p.1 |
| E6 | A/τ/T y FRP diferenciados en ASCII; 10 ms→100 pps,τ=0,5 ms | TP p.2; respuestas 1 p.1; U2 p.24 |
| E7 | Igualación P=R media(i²)=RIcc²; ejemplo 2 A pico,10 Ω→Icc=√2 A,P=20 W; L absorbida en R total | TP p.2; libro p.104 |
| E8 | a0=an=0;bn=2(1−cos nπ)/(nπ), sólo impares; b1=1,27324,b3=0,424413,b5=0,254648 | TP p.2; respuestas 2 p.1; libro pp.107–108 |
| E9 | T=.25 s,τ=.05 s,D=.2,B=20 Hz,n0=5,4 líneas positivas previas; C0/A=.2; coeficientes 1–5 y SVG | TP p.2; respuestas 2 p.3 |
| E10 | T=.01 s,τ=.0005 s,D=.05,B=2000 Hz,n0=20,19 positivas previas; C0=.05 V; todos los coeficientes publicados, incluido C21 negativo | TP p.2; respuestas 2 p.4; PDF cuestionario pp.1–3 |
| E11 | T=1/300 s,τ=1/1200 s,D=.25,B=1200 Hz,n0=4,3 positivas previas; C0=.25,C1=.225079,C2=.159155,C3=.075026 V | TP p.3; respuestas 2 p.4 |
| E12 | T=.1 s,τ=.02 s,D=.2,B=50 Hz,n0=5,4 positivas previas; C0=.2,C1=.187098,C2=.151365,C3=.100910,C4=.046774 V | TP p.3; respuestas 2 p.4 no trae resolución completa |
| E13 | Banda base puede codificar; no es exclusividad de LAN; modulación distingue portadora | TP p.3; respuestas 1 p.1; U2 p.30; Banda Base pp.2,6 |
| E14 | 34 bits,10 unos; cada marca AMI y cada mitad bipolar RZ, sin reinicio entre filas; AB sólo comparativa, sin A/Tb dados | TP p.3; UT2 codificación p.1; U2 pp.32–37 |
| E15 | 17 bits,34 mitades por variante; todos los estados Manchester y diferencial concordantes con convención | TP p.3; UT2 codificación p.1; U2 pp.41–42 |
| E16 | 17 bits polar RZ; transición interior en cada celda; 9 unos/8 ceros→media A/34 si bloque repetido | TP p.3; Práctica 2; U2 pp.32–34; libro p.148, hallazgo 004 |

## 4. Originales: páginas y figuras efectivamente inspeccionadas

Texto extraído se usó sólo para búsqueda; fórmulas/figuras se contrastaron visualmente con renders
de originales. Renders propios `u02-a/<clave>/pNNN.png`; montajes `mNN.png`; inventario exacto `sources.json`.
**158 páginas PDF distintas**: 156 de fuentes temáticas más 2 del programa; no es muestreo presentado como libro completo.

| Original | Clave / páginas visuales | Figuras/fórmulas incluidas |
|---|---|---|
| material/teoria/U2/U 2 Características de las señales de telecom.pdf | slides, **1–48**, todas | Analógico/digital/regeneración; niveles dB/equipos/cable; seno/parámetros; Fourier/trenes/espectros/instrumentos; OEM/bandas; todos los diagramas de códigos/tablas/PSD; filtros |
| material/teoria/U2/Señales Banda Base.pdf | base, **1–33**, todas | Acoplamiento/DC, clasificación, pulsos NRZ/RZ/AMI/HDB3, Manchester/diferencial/Miller/CMI y espectros |
| material/practica/U 2/TP  2  2026.pdf | pract2, **1–3**, todas | Cada enunciado E1–16, secuencias y cuadrada |
| EXPRESIONES Y RTAS  UD 2 1RA PARTE.pdf | pract1, **1**, toda | Claves conceptuales y λ FM |
| EXPRESIONES  Y RTAS UD 2 2DA PARTE.pdf | pract0, **1–4**, todas | Integrales/paridad de E8, Cn, resultados E9–11, remisión E12 |
| UT 2 CODIFICACION - DIST CODIGOS.pdf | pract3, **1–3**, todas | Esquemas comparativos; p.2 fragmentaria, p.3 dos fragmentos 00V: no se atribuyó resolución inexistente |
| UT 2 Códigos de línea cuadro comparativo.pdf | pract4, **1–3**, todas | Cada fila y figura, incluido B6ZS como pendiente y rankings no universales |
| UT 2 SEÑALES TELCOM-CODIGOS DE LINEA.pdf | pract5, **1–17**, todas | Señales, parámetros, regeneración, espectro EM/λ, misión y clasificación de códigos |
| material/teoria/DOC-20230425-WA0040.pdf | book, **98–112,134–159**, 41 páginas | Secciones utilizadas de señales/Fourier/AB/códigos/filtros; todas las fórmulas/figuras de esas páginas. NO las 726 páginas del libro |
| Ejercicio cuestionario 10-09-2026.pdf | qexercise, **1–3**, todas | Tren100/2000/1 V, cálculo y espectro |
| material/catedra/PROGRAMA de la materia.pdf | programa, **2–3** | Alcance oficial de U2 y comienzo de U3; no revisión integral del programa |

Capturas Markdown leídas: Teoría U2 `apuntes-clase 2.md`, `apuntes-clase3.md`, `apuntes-clase 4.md`;
Práctica `clase 02.md`, `clase 03.md`; tramo AB de Teoría U3 `apuntes-clase 4.md`;
Cuestionarios `cuestionario U1 y U2.md` Q4–7 y `cuestionario_U3.md` Q2. En capturas mixtas, velocidades
se reconocieron como U3, no se exigió duplicarlas en U2; preguntas de otras unidades no se evaluaron aquí.

### Figuras de archivo independientes: lista exacta

| Grupo | Archivos inspeccionados visualmente | Resultado |
|---|---|---|
| Capturas Teoría U2 | `image.png`, **image-1.png a image-18.png** (19) | Cada original, sin modificar; fórmulas/diagramas cotejados con filminas |
| Capturas Práctica | **image-10.png a image-16.png** (7) | Seno/parámetros, espectro EM/escalas y cuadrada |
| Captura Teoría U3 | **image-6.png** (1) | AB relevante |
| PNG candidatos | `codigos-base.png`, `espectro-electromagnetico.png`, `multinivel.png`, `espectros-codigos.png` (4) | Visual + SHA propia; figura multinivel observada en 003 |
| PNG raíz | `espectro_fourier_tren_pulsos.png` (1) | Ordenadas compatibles con Cn normalizado, líneas100 Hz/cero2000 Hz; sólo lado positivo mostrado |
| SVG candidatos | **tp2-e09-espectro.svg, tp2-e10-espectro.svg, tp2-e11-espectro.svg, tp2-e12-espectro.svg** | 140 líneas espectrales y 2404 puntos de envolvente recalculados; error de altura <6e−14 px en líneas y <.005 px en envolvente redondeada |
| SVG candidatos | **tp2-e14-codigos.svg, tp2-e15-codigos.svg, tp2-e16-codigos.svg** | 7 filas,119 celdas/238 mitades; 476 puntos, todos los niveles y coordenadas concordantes |

Total: **32 PNG inspeccionados** (27 capturas,4 copias,1 raíz) y **7 SVG**. Los SVG se inspeccionaron como
XML y mediante rasterización propia de sus primitivas con Pillow: **no** afirmo haber probado renderer del
visor Markdown/navegador, ni su dash-array/tipografía exactamente. No hay clipping manifiesto en el raster
interpretado; etiquetas y escalas verificadas. El aspecto de originales fue observado, no reconstruido como autoridad.

## 5. QA académico propio

Resultados calculados en `u02-a/qa-resultados.json`; script reproducible `u02-a/qa.py`.
Complemento algebraico/manual: integrales de paridad y seno en ciclo, producto par/impar, integral de
pulso centrado, conjugación y factor 2, dimensión de Dn [V·s], signo/fase en lóbulos negativos,
límite sinc(0), RMS y calentamiento resistivo. No se confundieron media rectificada y firmada.

- Cuadrada: a0=an=0; pares bn=0, impares4/(nπ); C1=−j2/π, módulo.63662 y amplitud real1.27324.
- Tren E10: C0=.05,C1=.049795,C2=.049182,C5=.045016,C10=.031831,C19=.002621,C20=0,
  C21=−.002371 V; D0=.0005 V·s. El conteo19 es correcto; 20 es índice del cero, no armónica no nula.
- dB: 43 dB→19952.62 en potencia;42.9 dBmV→139.64 mV;2.3 dBmV→1.30 mV;
  −3 dB→.501187 en potencia y .707946 en tensión a iguales resistencias.
- OEM:100 MHz→10 ns/3 m;1 MHz→300 m;600 MHz→.5 m;2.4 GHz→.125 m;5 GHz→.06 m;
  28 GHz→.010714 m. Argumento ω(t−z/v) dimensionalmente válido, original ωt−y/v no lo es.
- Continua: unipolar1100=.5 V;polar1100=0;polar1110=.5 V;Manchester media0 por bit.
  Recalculé 10 códigos para10110, HDB3 completo, Miller1001 y CMI101. 2B1Q001110 y terna4B3T1010
  correctos **para tabla declarada**; 25% menos símbolos no prueba por sí solo 25% menos banda.
- F06–08 yF15 correctos; F10 al duplicarT conserva primer cero, reduce separación yC0 a mitad;
  F13 reduceτ a mitad y duplica primer cero. Todas las claves S04–07/F01–15 contrastadas con sus límites.
- Filtros: comprobé las 4 bandas y todos los ejemplos100/500/1000/5000 Hz, B=3100 Hz;
  ideal/real y fase distinguidos. No exige ancho finito para pasaaltos ideal sin límite superior.
- **153 enlaces locales** de los5 Markdown de carpeta U2 y TP/repasos:0 fallos de ruta/ancla.
  Slugs estáticos compatibles con encabezados, no ejecución de plataforma Markdown.
- Baseline `ee66ef7`: **37 anclas antiguas** preservadas (14 Fourier,16 AB,7 índice),0 faltantes.
  Las6 preguntas de autoevaluación de pilotos se encuentran enF09–F14; ficha anterior enF01–F08.

## 6. Hallazgos accionables

### U02-A-001 — P2 — Falta una misión registrada de los códigos

- **Ubicación:** `apuntes/teoria/02-senales-telecomunicaciones/APUNTE.md#codigos`, líneas695–701 y834–836.
- **Claim observado:** enumera continua, sincronismo y espectro, pero no desarrolla detección de
  **presencia de señal en línea**; no está excluida explícitamente.
- **Evidencia:** `material/practica/U 2/UT 2 SEÑALES TELCOM-CODIGOS DE LINEA.pdf`, p.15 visual,
  misión3; `capturas/practica/clase 02.md`, línea75, misma misión.
- **Naturaleza:** faltante demostrado; no error de las tres propiedades existentes.
- **Consecuencia:** respuesta de examen sobre misión de códigos omite un punto explícito de clase.
- **Acción:** agregar explicación breve de distinguir actividad/ausencia del dato0 y conectarla con
  código concreto. No extender programa ni afirmar que cualquier instante de tensión0 prueba ausencia.
- **Prueba de cierre:** ejemplo de racha0000, con observación durante una ventana de bits, que explique
  por qué unipolarNRZ puede confundirse con silencio y un código con pulsos/transiciones ayuda; fuente p.15
  y respuesta de examen incluyen las tres misiones.

### U02-A-002 — P2 — E/H corregidas, pero sin aplicación numérica

- **Ubicación:** `APUNTE.md#oem`, líneas631–652.
- **Claim observado:** E(z,t) yH(z,t) cuentan con unidades/supuestos; ejemplos sólo evalúan λ yT.
- **Evidencia:** fórmulas originales en U2 p.26 y esquema p.28; metodología exige ejemplo calculado
  para toda fórmula. Los ejemplos del candidato no sustituyen z,t,E0,H0,φ en campos.
- **Naturaleza:** faltante pedagógico demostrado; la corrección dimensional es correcta.
- **Consecuencia:** el estudiante puede repetir la errata corregida sin entender retardo espacial/fase.
- **Acción:** un ejemplo hipotético pequeño que calcule ambos campos, declarando amplitudes y fase;
  no añadir ecuaciones diferenciales, impedancias ni contenidos U7.
- **Prueba de cierre:** a100 MHz y v=3·10⁸ m/s, z=.75 m,t=0,φ=0 da argumento−π/2 y ambos campos0;
  otra posición/instante muestra repetición. Aclarar unidades y amplitudes hipotéticas. No es necesario
  adoptar estos números: sí evaluar explícitamente el argumento y los dos resultados.

### U02-A-003 — P2 — Figura multinivel usa asignación diferente sin advertencia local

- **Ubicación:** `APUNTE.md#codigos`, líneas801–810; `recursos/multinivel.png`, panel superior derecho2B1Q.
- **Claim observado:** tabla y ejemplo siguen U2 p.43, luego enlace presenta comparación de pp.43–44,
  sin identificar que el gráfico no usa la misma asignación.
- **Evidencia visual:** U2 p.43:01→−.833 V,10→+2.5 V. En U2 p.44/captura `image-16.png` y copia
  multinivel, primera celda01 está **sobre** eje0 y segunda10 **debajo**. No pueden ser el dibujo de
  aquella tabla con polaridad/etiquetas actuales.
- **Naturaleza:** discrepancia demostrada, **no** prueba de mapping2B1Q universalmente incorrecto.
  El texto ya dice que niveles no son universales; falta identificar qué convención usa este recurso concreto.
- **Consecuencia:** un alumno que verifica el ejemplo contra la figura obtiene signo opuesto y no sabe
  si falló su regla, la tabla o el dibujo.
- **Acción:** aclaración adyacente: figura de otra asignación o inconsistencia del original; no modificar
  imagen/captura. Si no puede establecerse asignación completa, no usar ese panel para comprobar tabla p.43.
- **Prueba de cierre:** lector puede señalar qué salida de01/10 corresponde al ejemplo y por qué
  el panel original no lo verifica; original se conserva y no se generaliza una tabla de estándar no registrada.

### U02-A-004 — P3 — Página bibliográfica equivocada para polar RZ

- **Ubicación:** `apuntes/practica/tp-02-senales.md`, E16, línea345.
- **Claim observado:** cita “libro PDF149/impresa123” para polarRZ/autosincronismo.
- **Evidencia visual:** libro `DOC-20230425-WA0040.pdf` **PDF148/impresa122**, §2.8.5.4,
  figura2.43 y explicación polarRZ; PDF149/123 desarrolla bipolarAMI/diferencial (§2.8.5.6–7).
- **Naturaleza:** error de localización demostrado. U2 pp.32–34 y cuadro p.1 sí sustentan la resolución,
  por lo que no convierte la clave E16 en error académico P1.
- **Consecuencia:** quien sigue esa cita encuentra otro código y pierde trazabilidad.
- **Acción/prueba de cierre:** corregir sólo referencia aPDF148/122; comprobar título/figura de la
  página y mantener las otras fuentes válidas. No corregido en esta auditoría.

## 7. Límites y pendientes que NO se convierten en errores

- Revisé todo el contenido académico candidato y sus preguntas, no todos los documentos del repositorio.
  No revisé el libro de726 páginas entero ni unidades U1/U3–U6 enteras; los cruces se delimitaron arriba.
- U2 declara difusión sin registro, B6ZS/reglas de rankings BER/PSD no confirmadas y temas U7/U8 fuera
  de alcance. Se conservan como pendientes/exclusiones, no como conocimiento evaluado: **no son hallazgos**.
  No consulté Internet ni incorporé bibliografía externa para ampliar el programa.
- Auxiliares ampliados al cierre (evidencia propia `u02-a/auxiliares.json`):
  - `Fourier en tiempo real v2.xlsx`: inspección XML de Hoja1, inventario de71 celdas con fórmula,
    imagen original incrustada visualizada. Recalculados **61 Cn** (n=−30…30) para A=18,τ=250 ms,T=700 ms:
    máximo error del valor almacenado <9e−16. Evidencia `xlsx-check.json`. No abrí Excel ni recalculé
    dinámicamente sus gráficos/interfaz o el caso límiteT=τ.
  - `Unidad de medida de sonoridad dB.docx`: leído texto XML completo y **12 imágenes originales**
    de símbolos/fórmulas. Sus escalas acústicas no se integran ni se evalúan en el candidato; no amplié
    programa con acústica. No rendericé paginación nativa de Word.
  - ZIP: inventario exacto, `Códigos de línea comparados.jpg` visualizada completa (hoja manuscrita
    de12 filas de códigos); el `.doc` binario incluido no se pudo revisar con renderer nativo.
  - RAR: listado y extracción sólo a recursos propios mediante `tar`; contiene `Fotocopia de codigo
    linea 1.doc` y `Fotocopia de codigo linea 2.doc`. **No** revisión visual de esos2 `.doc` legacy:
    no hay lector/render disponible comprobado; una extracción JPEG por firma no produjo imagen válida.
  Estas son inspecciones parciales explícitas, no certificación de todos los formatos originales.
  Los2 DOC delRAR y1 DOC delZIP quedan como límite real de evidencia, no error del candidato.
- Además de32 PNG principales y7SVG, se visualizaron14 imágenes auxiliares (12DOCX,1XLSX,1JPGZIP).
- Inspección visual PDF mediante Poppler y montajes; detalles discutidos se abrieron también individualmente.
  No hay OCR usado como autoridad. La legibilidad de un rótulo original insuficiente no se mejoró inventando datos.
- No probé enlaces externos ni render final de la app; comprobación local estática y rasterSVG interpretado.
  No ejecuté build, instalación, commits ni cambios a originales/caches/candidatos.
- Recomiendo cerrar001–004 y revalidar sus secciones. Esto no sustituye la validación pendiente del material
  expresamente excluido ni el protocolo de13 dictámenes antes de corregir.

## Key Learnings:

1. En U2, normalizar Cn y distinguirlo de amplitud unilateral evita factor2 y confusión de unidades V/V·s.
2. La figura multinivel original y la tabla2B1Q usan signos distintos: una copia fiel puede necesitar aclaración.
3. El contenido correcto puede conservar deuda pedagógica o una cita incorrecta sin ser una clave matemática errónea.


---

## Dictamen B

# Dictamen independiente U02-B — revisión pedagógica integral del corpus delimitado

- **Revisor:** B, independiente, no autor. **Fecha:** 2026-10-13. **skill_resolution:** injected.
- **Dictamen:** **REQUIERE CORRECCIONES**: P0=0, P1=1, P2=1, P3=1. No promover a `revisado` ni llamar unidad final. El estado actual `en-progreso` es honesto.
- **Raíz R:** `C:/Users/Martin/Documents/UTN_SISTEMAS/Anual_2026/comunicacion_de_datos`. Todas las rutas abreviadas abajo se resuelven desde R.
- **Identidad congelada:** `docs/consolidacion-u1-u6/snapshot-inicial.json`; SHA256 `1E29FD3BF30B9D99D07E0D3B73E2D7EF11F9D85BB7874B2630650412068A7BDD`; **401 archivos comprobados antes y después, 0 ausentes, 0 diferencias**. Evidencia propia: `tmp/reviews/u02-b/hash-before.json` y `hash-after.json`.
- No se modificaron candidatos, capturas, material, caches ni documentos compartidos. No builds, instalaciones ni commits. Sólo este informe y derivados propios de auditoría.
- Ceguera mantenida: no se leyeron informes/conclusiones de autores u otros revisores, `tmp/autor-*`, estado/revisiones de consolidación ni hallazgos ajenos de Engram. Los bloques de autocertificación dentro de candidatos NO se tomaron como evidencia de ejecución.

## 1. Cobertura efectiva y autoridad

### Candidatos leídos completos

| Candidato | Cobertura |
|---|---|
| `apuntes/teoria/02-senales-telecomunicaciones/APUNTE.md` | Todo: alcance, §1 señales/regeneración, §2 parámetros/media/RMS, §3 Fourier trigonométrico/complejo/tren, §4 AB señal/canal/primer cero/dB, §5 OEM, §6 códigos, §7 filtros, pendientes, resumen y checklist. QA embebido ignorado como certificación. |
| `INDICE.md`, `serie-de-fourier.md`, `ancho-de-banda.md`, `compatibilidad.md` de esa carpeta | Lectura completa; stubs/anclas y mapa de compatibilidad comprobados. `.gitkeep` inventariado, sin contenido académico. |
| `recursos/manifest.json` y cuatro PNG | Manifesto leído; hashes originales/copia recalculados; imágenes originales inspeccionadas visualmente. |
| Siete SVG `tp2-e09/10/11/12-espectro`, `tp2-e14/15/16-codigos` | XML, rasterización independiente y revisión visual completos; geometría de líneas/medias celdas recalculada. |
| `apuntes/practica/tp-02-senales.md` | **E1–E16 completos**, consignas, desarrollo, tablas, siete gráficos, resultados y límites. |
| `apuntes/repaso/u02-fourier-y-ancho-de-banda.md` | **F01–F15**: enunciados, procedencia, claves, cálculos, rúbrica y exclusiones. |
| `apuntes/repaso/u02-senales.md` | **S04–S07**: las cuatro preguntas, opciones, claves, razones y distractores. |

### Originales específicos: texto y contraste visual, no muestreo

Todas las páginas de los siguientes nueve PDF se extrajeron a derivados propios y se inspeccionaron mediante Poppler/contact sheets. **115 páginas** en total; portadas y páginas sin desarrollo también vistas.

| Alias | Original | Páginas PDF efectivamente vistas |
|---|---|---|
| U2 | `material/teoria/U2/U 2 Características de las señales de telecom.pdf` | **1–48**, todos los gráficos/fórmulas: instrumentos, amplitudes, Fourier, tren, OEM, códigos, multinivel, espectros y filtros. |
| BB | `material/teoria/U2/Señales Banda Base.pdf` | **1–33**: pulsos, misiones, CC/reloj/presencia, NRZ/RZ/AMI, diferencial, Manchester, Miller, HDB3, 4B3T y CMI. |
| UT | `material/practica/U 2/UT 2 SEÑALES TELCOM-CODIGOS DE LINEA.pdf` | **1–17**: parámetros, espectro EM, clasificación, misiones y condiciones de línea. |
| TP | `material/practica/U 2/TP  2  2026.pdf` | **1–3**; E1–16 de pp.2–3. |
| R1 | `material/practica/U 2/EXPRESIONES Y RTAS  UD 2 1RA PARTE.pdf` | **1**. |
| R2 | `material/practica/U 2/EXPRESIONES  Y RTAS UD 2 2DA PARTE.pdf` | **1–4**: Fourier y respuestas E9–12, incl. remisión de E12. |
| Esquemas | `material/practica/U 2/UT 2 CODIFICACION - DIST CODIGOS.pdf` | **1–3**, todas las formas de onda y diagramas. |
| Cuadro | `material/practica/U 2/UT 2 Códigos de línea cuadro comparativo.pdf` | **1–3**, filas/propiedades/notas, no sólo encabezados. |
| Q10 | `Ejercicio cuestionario 10-09-2026.pdf` | **1–3**. Fourier/tren se asigna U2; perro/tasa y simplex U3. |

**Libro:** `material/teoria/DOC-20230425-WA0040.pdf`, Castro Lechtaler/Fusario del repositorio: lectura y contraste visual **PDF98–112 y PDF134–159**, **41 páginas**, impresas72–86 y108–133. Comprende fundamentos/umbral/parámetros/Fourier/tren y AB/banda base/códigos/filtros. No se afirma haber revisado las 726 páginas del libro ni sus capítulos ajenos. Las páginas intermedias de dB se remitieron a U6, no se auditaron como contenido canónico de esta unidad.

**Programa:** `material/catedra/PROGRAMA de la materia.pdf`, **pp. PDF2–3** originales vistos para alcance/vocabulario U2; no se interpreta programa como autorización para agregar temas sin registro.

**Capturas Markdown:** lectura completa de las ocho fuentes de la matriz §2. **28 imágenes originales** revisadas visualmente: 19 archivos `image.png`/`image-1.png`–`image-18.png` de teoría U2; siete `capturas/practica/image-10.png`–`image-16.png`; `capturas/teoria/03-redes-telecomunicaciones/image-6.png`; `espectro_fourier_tren_pulsos.png` raíz. Las cuatro copias PNG de candidatos coinciden byte a byte con sus originales, pero eso NO certifica su coherencia didáctica (véase B-001).

**Caches:** usados como auxiliares: nueve transcripciones U2/TP/respuestas/codificación y programa; el extracto largo del libro se consultó por tramos, sin afirmar lectura íntegra del cache. Los originales y las 41 páginas pertinentes del libro sí fueron contrastados. No se crearon/editaron caches compartidos; extracciones/render propios están en `tmp/reviews/u02-b/`.

## 2. Clasificación de todos los bloques de capturas pertinentes

Claves: **I** integrado; **C** integrado con corrección/acotación; **R** remitido a unidad principal fuera de esta auditoría; **P** pendiente explícito/no evaluable; **F** faltante demostrado. La asignación R no certifica la calidad de toda la unidad de destino.

| Original y bloque | Destino / tratamiento verificado |
|---|---|
| `capturas/teoria/02-senales-telecomunicaciones/apuntes-clase 2.md`, 20/08: analógico/digital, ventajas, ruido, CODEC | APUNTE §1 y TP E1–2 **I/C**: regeneración con umbral y posibilidad de error; no eliminación mágica del ruido. CODEC se vincula a U4. |
| Misma: dB relativos, dBm/dBmV, relaciones potencia/tensión/corriente e impedancias | APUNTE §4 vínculo unidades logarítmicas → U6 **R/C**. Se exige RMS/carga resistiva; no se hereda silenciosamente potencia real como cociente de impedancia compleja. |
| Misma: usos y valores típicos de dB, ejemplo amplificador 43 dB | APUNTE §4 enlace U6 **R**; no presentado como normativa universal U2. |
| Misma: Tx42,9 dBmV / Rx2,3 dBmV, cálculo de tensiones | APUNTE §4 vínculo U6 **R**. Registro conservado sin tratar valores medidos como límites de norma. |
| Misma: coaxial F6TSVM 75Ω, tabla de atenuación vs frecuencia/longitud y divisor | APUNTE §4 caso y vínculo U6 **R**; ilustra atenuación, no expansión a estudio de medios U7. Tabla detallada permanece original. |
| Misma: AB por puntos3dB | APUNTE §4 **I/C**, potencia mitad vs tensión RMS0,707 sobre igual R. |
| Misma: periódicas/no periódicas, tiempo/frecuencia, serie/transformada, parámetros | APUNTE §2–3 **I/C**, distingue serie periódica de transformada; instrumentos por ejes. |
| `apuntes-clase3.md`, sin fecha: AB/energía | APUNTE §4 **I/C**, distingue criterio de señal del AB de canal. |
| Misma: tren rectangular, envolvente sinc, líneas por T y ceros por τ | APUNTE §3 tren/§4 primer cero; TP E9–12, F06–08/F15 **I/C**; normalización y conteo del primer cero corregidos. |
| Misma: OEM, campos E/H y gráficos | APUNTE §5 **I/C**, propagación y corrección dimensional; diferencia espectro EM/espectro de señal. |
| `apuntes-clase 4.md`, 03/09: cuadro completo de códigos/polaridad/NRZ/RZ/diferencial | APUNTE §6 y TP E14–16 **I/C**; retorno a cero, no nivel intermedio; ejemplos con convención. |
| Misma: definición PSD ligada a τ/área y pulsos→AB→bits/s | APUNTE §6 análisis espectral y §4 **C**, PSD por Hz; no convierte ancho de pulso directamente en velocidad informativa universal. |
| Misma: rankings densidad, error y AB del cuadro | APUNTE §6 **P/C**: sin supuestos, no leyes; excluidos de repaso como verdad confirmada. |
| Misma: HDB3/relleno/violaciones/paridad | APUNTE §6 HDB3 y S06 **I/C**; cuatro ceros, R/V, estado conservado. |
| Misma: diferencial, Manchester/bifase, Manchester diferencial y ejemplos tecnológicos | APUNTE §6 y TP E15 **I/C**; FDDI no repetido como Manchester, Ethernet histórico acotado. |
| Misma: 2B1Q tabla/cuatro niveles y figura | APUNTE §6 **I**, pero **incompatibilidad sin aviso** texto/figura: B-001. |
| Misma: 4B3T tabla redundante/ternas/historia y comparación25% | APUNTE §6 **I/C**, símbolos no bits; reducción AB condicionada, sin inventar algoritmo de selección. |
| Misma: análisis espectral de códigos/gráficos | APUNTE §6 **I/C**; área firmada, PSD y condiciones distinguibles. |
| Misma: filtros/AB/cortes/selectividad/ideal-real/LC-cristal-activos/símbolos | APUNTE §7 **I/C**, cuatro familias y esquemas conceptuales; no promete rechazo físico infinito. |
| `capturas/practica/clase 02.md`, 18/08: señal/analogía amplitud/duración/parámetros | APUNTE §1–2 y TP E3–4 **I/C**, T[s] no Hz, fase/unidades/ejemplos. |
| Misma: polaridad, regeneración/repetidor, espectro EM/λ | APUNTE §1/§5/§6 y TP E5–6 **I/C**, alcance no depende sólo de λ. |
| Misma: banda base, código de línea y misión disminuir CC/sincronismo | APUNTE §6 y TP E13 **I**. |
| Misma: tercera misión **detectar presencia de señal** (línea75) | **F**, omitida en canon y TP E13: B-002. |
| Misma: HDB3 “tercer cero” | APUNTE §6 y S06 **C**, se reemplaza grupo0000, no tercer cero. |
| Misma: consignas/respuestas E1–3, E5–6, E13–16 y diagramas | TP E1–16 y APUNTE secciones correspondientes **I/C**; desarrollo propio se distingue de hoja oficial, secuencias completas. |
| `capturas/practica/clase 03.md`, 25/08: velocidades Vm/Vtx/Vtd/Vrtd, multinivel | U3 **R**; U2 sólo remite/conserva supuesto τ del tren; no reutiliza AB=1/τ como ley de todos los códigos. |
| Misma: periodicidad/Dirichlet/trigonométrica/coefs/paridad | APUNTE §2–3 y TP E8 **I/C**; condiciones suficientes; onda impar no implica todos bn no nulos. |
| Misma: forma compleja/espectro/coeficientes del tren | APUNTE §3 y TP E9–12 **I/C**, normalización y signos explicitados. |
| `capturas/teoria/03-redes-telecomunicaciones/apuntes-clase 4.md`, 03/09: AB/senal-canal | APUNTE §4 **I/C**; los otros bloques velocidades/tipos/arquitecturas quedan U3 **R**. Se leyó la captura completa para separar fragmentos, sin certificar U3. |
| `capturas/teoria/03-redes-telecomunicaciones/cuestionario_U3.md`, Q2 completo incl gráfico/resultados | APUNTE §3 ejemplo E10, TP E10, F15 **I/C**; corrige contar20 como armónicas no nulas:19 positivas antes del cero. |
| Mismo cuestionario, Q1 perro y Q3 simplex | U3 **R**, no faltantes U2. Q10 PDF1/3 acompaña esos bloques. |
| `capturas/teoria/Cuestionarios/cuestionario U1 y U2.md`, Q4 instrumento | S04 y APUNTE §3 **I**, clave falsa justificada por ejes. |
| Mismo, Q5 polar RZ | S05/TP E16/APUNTE §6 **I/C**, comparación sólo entre opciones y con Tb/pulso común. |
| Mismo, Q6 HDB3 | S06/APUNTE HDB3 **I/C**, mecanismo físico/distractores. |
| Mismo, Q7 canal/filtro | S07/APUNTE §7 **I/C**, pasa banda bajo dos cortes no nulos, admite canal banda base pasa bajos. |
| Mismo, recordatorios de instrumentos/códigos/filtro | Mismos destinos **I/C**; no “todo canal pasa banda”. Q1–3/recordatorios CTB/OSI son U1/arquitecturas **R**, no se evalúan como U2. |
| Pilotos presentes | Stubs/anclas conservados y destinos navegables; preguntas heredadas F01–14 con desarrollo/claves en repaso. No se certifica equivalencia con versiones históricas no disponibles en esta revisión. |

**Fuera de alcance, NO hallazgos:** ecuación de difusión y desarrollo no registrado conductor/dieléctrico del programa; expansión de medios/interfaces U7–U8; páginas ajenas de bibliografía; B6ZS/rankings materiales marcados pendientes. Las fuentes específicas aportan aclaración del registro, no autorización para desarrollar toda la biblioteca.

## 3. QA independiente ejecutado

### Progresión y comprensibilidad

La ruta señal→parámetros→Fourier→AB→OEM→códigos→filtros es razonable; las dependencias están antes de las fórmulas. Centrales poseen problema/modelo/formalización/unidades/supuestos/ejemplo/errores/respuesta oral; secundarios no se inflan artificialmente. Resumen mental y checklist presentes. Destaca la distinción continua/media firmada frente a RMS/energía, canal frente a señal y espectro bilateral frente a amplitud real. Los ejercicios muestran método antes del resultado. La tercera misión de los códigos queda fuera pese al registro (B-002).

### Cuentas, reglas y claves

Comprobación manual y recomputación Python propia, no ejecución de autocontroles del autor. Evidencia `qa-independent.json` y `qa.py`.

- Parámetros APUNTE: T2ms→f500Hz, ω1000πrad/s y ejemplo temporal; RMS seno300V=212,132V, media ciclo0. TP E4: f50Hz,T20ms, faseπ/2,v(0)=300V, RMS212,132V. Ejemplos media vs RMS y área firmada cotejados con condiciones.
- TP E5: FM88–108MHz, λ2,77778–3,40909m para v=3·10^8m/s. Ejemplos OEM/frecuencia/λ y argumento de onda dimensionalmente correctos bajo medio uniforme supuesto.
- TP E7: demostración potencia sobre R resistiva revisada; ejemplo hipotético i=2sen(ωt)A,R10Ω: I_RMS=√2A,P=20W. No se atribuyen esos datos al TP.
- Fourier APUNTE/TP E8: a0=an=0; bn=2[1−cos(nπ)]/(nπ), pares0, impares4/(nπ). Primeras amplitudes1,273240;0,424413;0,254648V para ±1V. Condiciones/valor de convergencia en saltos revisados; no se hereda “todo bn≠0”.
- Fourier complejo: Cn=integral/T y síntesis con signos opuestos; Dn de filmina sin1/T tiene V·s y síntesis1/T. C−n=Cn* para señal real; Rn=2|Cn| para n>0. Desplazamiento introduce fase; lóbulo negativo de coeficiente no es magnitud negativa.
- E9: T0,25s,τ0,05s,D0,2,B20Hz,n0=5,4 armónicas positivas no nulas antes del cero,C0/A0,2. E10: T0,01s,τ0,0005s,D0,05,B2000Hz,n0=20,19 positivas,C0=0,05V. E11: T1/300s,τ1/1200s,D1/4,B1200Hz,n0=4,3 positivas,C0=0,25V. E12: T0,1s,τ0,02s,D0,2,B50Hz,n0=5,4 positivas,C0=0,2V. Todos los coeficientes publicados y ceros recalculados, no sólo C0.
- Cuatro SVG espectrales: **21/81/17/21 líneas** respectivamente; alturas verificadas contra |D·sinc(nD)| y envolvente/intervalos frecuenciales; cero y lóbulos posteriores visibles. No son espectros continuos del tren.
- E14: **34 bits/10 marcas**; AMI alterna sin reinicio entre filas; bipolar RZ conserva primera mitad y vuelve a0. E15: **17 bits/34 medias celdas** por variante; Manchester0=+−,1=−+ y diferencial previo−,0cambia inicio; decodificación reproduce secuencia. E16 polar RZ: pulso incluso para0;9unos/8ceros, media de bloque repetido A/34. Todas las medias celdas de las **siete filas dibujadas** verificadas leyendo geometría XML independiente de las tablas; coinciden.
- HDB3: ejemplo completo 111|0000|0000|0101, conteos3/0, V positiva luego negativa, relleno AMI y recuperación0000 verificados. Miller1001 y CMI101 comprobados operativamente. 4B3T reducción de símbolos25%, no bits; tabla específica y elección por historia acotadas. 2B1Q tabla/ejemplo correcto, gráfico incompatible B-001.
- AB: ejemplos fH−fL y primer cero, unilateral/bilateral y n0 vs cantidad de líneas correctos. −3dB potencia≈0,501 y tensión≈0,708 a igual R; no se trasladó10log a tensión. Filtros reales/acoplamiento/raíles de rechazo no idealizados como universales.
- **19 claves**: F01–F15 y S04–S07 contrastadas, incl. mini ejercicios numéricos F06–08 y F15. Datos hipotéticos rotulados; repaso parcial no vendido como simulacro integral; distracciones S05/S07 razonadas bajo supuestos. No se evalúan pendientes B6ZS/PSD/BER como hechos.

### Navegación, recursos y entorno

- **153 enlaces locales Markdown** revisados (archivo y ancla destino, incluyendo stubs): **0 errores**. No se siguieron links hacia reportes/estados como contenido; sólo resolución de ruta/ancla donde correspondía.
- Cuatro PNG: SHA256 fuente=copia=manifesto para cada uno; no modificación de originales.
- Poppler disponible y probado; Python del runtime con pypdf/PIL/reportlab disponible. No se instalaron dependencias. Render SVG mediante primitivas XML fieles (rect/text/line/polyline), PDF/Poppler; **Arial sustituida por Helvetica** en derivados propios. La evaluación geométrica se hace sobre XML original, por lo que esa sustitución no afecta signos/medias celdas; no certifica tipografía exacta en cada visor.
- 115 páginas específicas +41 libro +2 programa = **158 páginas originales inspeccionadas**. Contact sheets completos `src00-sheet*`–`src08-sheet*`, `book-sheet01`–`book-sheet21`, `capture-sheet01`–`capture-sheet14`; propios PDF/PNG SVG y JSON en carpeta del revisor.

## 4. Hallazgos demostrados

### U02-B-001 — P1 académico: tabla 2B1Q y gráfico incompatible sin advertencia

- **Ubicación:** `C:/Users/Martin/Documents/UTN_SISTEMAS/Anual_2026/comunicacion_de_datos/apuntes/teoria/02-senales-telecomunicaciones/APUNTE.md`, §6 «Códigos secundarios registrados», **líneas801–809**, recurso `recursos/multinivel.png` (banda2B1Q).
- **Claim observado:** la regla declarada es 01→−0,833V y10→+2,5V; a continuación se ofrece la figura como comparación del mismo código, sin declarar otra correspondencia.
- **Evidencia:** original **U2 PDF43** declara esa tabla, que el texto respeta. **U2 PDF44**/captura `image-16.png`/copia multinivel: la primera pareja **01** se dibuja **por encima de0**; el siguiente **10** por debajo, contradiciendo el signo de la tabla. Inspección directa de original/copias; ver `src01` p44 y captura correspondiente. El hash igual sólo demuestra fidelidad de copia.
- **Naturaleza:** **demostrado**, incompatibilidad interna de convención, no acusación de que toda correspondencia alternativa de niveles sea físicamente inválida.
- **Impacto:** alumno que aplica la regla correcta no puede reproducir la figura usada para aprender; incentiva codificar por memoria de dibujo y aceptar signos contradictorios.
- **Acción:** mantener originales intactos; señalar al lado del enlace que la figura usa correspondencia diferente/no sirve para validar tabla elegida, o producir derivado correcto explícitamente rotulado, sin reemplazar evidencia histórica.
- **Prueba de cierre:** tabla elegida, ejemplo y figura didáctica deben producir signos coherentes para **01 y10** y los diez dibits de la secuencia de figura. Si se conserva original, advertencia visible que explique la diferencia antes de usarlo.

### U02-B-002 — P2 cobertura pedagógica: tercera misión registrada omitida

- **Ubicación:** `C:/Users/Martin/Documents/UTN_SISTEMAS/Anual_2026/comunicacion_de_datos/apuntes/teoria/02-senales-telecomunicaciones/APUNTE.md`, ancla `#codigos`, **líneas693–701**. TP2 E13 tampoco desarrolla esa misión.
- **Claim/omisión:** se explican disminuir continua, recuperar sincronismo y ajustar espectro, pero no **permitir detectar presencia de señal en línea**. No hay definición/ejemplo ni pendiente que clasifique ese fragmento.
- **Evidencia:** captura **`capturas/practica/clase 02.md`, línea75**, «misión»; original **UT PDF15**, **BB PDF7,16,31**; libro **PDF141/impresa115**, tercera viñeta de misión. Figura/explicación BB p16 muestra inconveniente de asociar ausencia de nivel activo con0. Todos contrastados visualmente.
- **Naturaleza:** **faltante demostrado** dentro de registro; no se exige contenido adicional de biblioteca o del programa.
- **Impacto:** el apunte no conserva las tres finalidades que el estudiante debería distinguir; puede confundir0informativo con ausencia de transmisión.
- **Acción:** integrar como concepto secundario dentro de §6: problema, definición breve, ejemplo de racha0000 unipolar vs código con actividad, distinción de presencia y recuperación de reloj. No copiar la generalización de que todo instante de tensión0 significa línea inactiva.
- **Prueba de cierre:** alumno puede responder «¿qué diferencia hay entre recibir bits0 y no recibir señal?» con una comparación concreta y supuestos; original→sección y checklist/repaso pertinente registran el tratamiento sin editar captura.

### U02-B-003 — P3 editorial: página del libro incorrecta en polar RZ

- **Ubicación:** `C:/Users/Martin/Documents/UTN_SISTEMAS/Anual_2026/comunicacion_de_datos/apuntes/practica/tp-02-senales.md`, **E16, línea345**.
- **Claim observado:** «Fuente ... libro PDF149/impresa123» para polar RZ/autosincronismo.
- **Evidencia:** libro original **PDF148/impresa122**, **§2.8.5.4/fig2.43**, describe polar RZ y autosincronismo. **PDF149/impresa123** describe bipolar sin retorno/AMI y codificación diferencial, no el fundamento citado de polar RZ.
- **Naturaleza:** **demostrado**; desarrollo/regla/resultados de E16 correctos. Es trazabilidad editorial, no fallo de cuenta.
- **Impacto:** dificulta contrastar el ejemplo y conduce a una familia de código distinta al buscar la cita.
- **Acción y cierre:** corregir sólo referencia a PDF148/impresa122 §2.8.5.4, luego abrir esa página y verificar figura/explicación. Original sin cambios.

## 5. Sospechas, límites y condiciones del dictamen

- **Sin sospechas abiertas convertidas en hallazgos.** No se penaliza falta de desarrollo universal de PSD/BER/B6ZS: su incertidumbre está declarada y no se evalúa como verdad. Las exclusiones de difusión/U7/U8 se respetan.
- Esta revisión es integral del **corpus registrado U2 delimitado**, no de todo el programa ni de U1/U3/U6. Las remisiones cruzadas se clasificaron; no se auditaron íntegramente sus destinos. No corresponde declarar «unidad2 final» aun cerrando estos tres hallazgos.
- Videos/URL de las capturas no reproducidos; se revisó la captura completa y se contrastó lo usado con sus PDF/imágenes originales disponibles. No se atribuye verificación del contenido del video ni estándares vigentes externos. Archivos auxiliares ajenos/no usados (DOC/XLSX/ZIP/RAR) no se declaran revisados.
- No hay comparación retrospectiva de contenido de pilotos históricos: sólo stubs actuales/mapa/anclas y preguntas que el candidato declara heredadas, examinadas por sí mismas. Tampoco se certifica render tipográfico final de Markdown en todos los clientes.
- Requiere cerrar B-001/B-002 y ajustar B-003 antes de aceptación de la consolidación registrada. Después reauditar los cambios sin modificar evidencia inmutable; conservar pendientes legítimos y estado honesto.

## Key Learnings:

1. Una copia con SHA256 idéntico puede preservar una figura académicamente incompatible con la tabla elegida; fidelidad de copia y coherencia pedagógica son controles distintos.
2. Presencia de señal, sincronismo y reducción de continua son finalidades distintas de la codificación de línea.
