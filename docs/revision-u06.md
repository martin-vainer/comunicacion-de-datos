# Revisión U06 — A/B

## Dictamen A

# Auditoría académica U6-A — canales de comunicaciones

Fecha: 2026-10-13. Revisión ciega independiente A. `skill_resolution: injected`.

## Resumen ejecutivo (≤350 palabras)

**Veredicto: sin hallazgos demostrados de severidad P0–P3 en el alcance revisado; U6 sigue honestamente `en-progreso`, no `revisado`.** No encontré errores sustantivos en las fórmulas/cuentas clave del apunte ni en las 16 consignas resueltas. Las soluciones mantienen visibles los supuestos (en particular tensiones de E6-I y la interpretación de BER sobre Ethernet), y las limitaciones del CRC, paridad, ARQ/FEC y Hamming están explicadas correctamente. La cobertura de material registrado se distingue de la cobertura total del programa: eco y efecto pelicular se declaran fuera del corpus registrado, no como temas cubiertos.

El contraste visual integral cubrió las 38 láminas originales U6 (pp.1–38; p.1 sólo identificatoria), TP6-I p.2, TP6-II pp.2–3, U2 pp.4–11 y Castro/Fusario 2013, PDF pp.199–200 (impresas pp.173–174). Se leyeron las capturas U6, U2 clase 2 y práctica 4/5 relacionadas. Las cantidades verificadas por recálculo independiente coinciden: Shannon TP-I E1–2/E4–6; BER E4-II; CRC del ejemplo de filminas y TP-II; eficiencias de paridad/Hamming y utilización Stop-and-Wait. No se modificaron materiales.

Limitación deliberada: no se auditó contenido U7/U8 ni se convirtió el libro de referencia en fuente para incorporar temas no registrados. Al no surgir defectos demostrados, no asigno acciones de cierre ficticias.

## Integridad y método

- `docs/consolidacion-u1-u6/snapshot-inicial.json`: 401 entradas verificadas antes y después; 0 ausentes o con hash distinto en ambas comprobaciones.
- Sólo lectura en fuentes/capturas/caches/candidato; no build, instalación, commit ni modificación de originales. Informe y hojas de contacto propias en `tmp/reviews/u06-a/`.
- Fuentes originales visuales; cache usado únicamente para localizar/encontrar texto. Cálculos rehechos con script local independiente, no con evidencia de autocontrol.

## Cobertura exacta

- `apuntes/teoria/06-canales-comunicaciones/APUNTE.md`: secciones 1–23 completas y cierre/cobertura/mapa/pendientes, líneas 1–1500 aproximadamente; auditados conceptos, tablas, LaTeX, ejemplos, excepciones y anexo. Imágenes originales U6, pp.1–38, vistas en 10 hojas de contacto (páginas 2–38 como evidencia técnica; p.1 portada). Especial foco visual p.4–7 (Nyquist/Shannon), 9–15 (atenuación/ruido/factor), 17–18 (banda/ISI), 24–29 (paridad/CRC/checksum), 32–38 (ARQ/FEC/Hamming).
- `INDICE.md`: todos sus enlaces y rutas temáticas; correlación con APUNTE y TP/repaso.
- `apuntes/practica/tp-06-canales.md`: primera parte E1–E6 y segunda parte E1–E10 (16 preguntas; numeración original reinicia); páginas originales TP6-I p.2, TP6-II pp.2–3; link de Hamming en p.3 comprobado como referencia sin consigna numérica.
- `apuntes/repaso/u06-canales.md`: Q-P5-3 dBm, enunciado, respuesta y conversiones; respaldo visual U2 p.5 y captura Clase 05.
- Fuentes relacionadas: PDF U2 pp.4–11; captura U2 clase 2 (segmento dB); captura práctica 4 (unidades y balance); captura Clase 05, pregunta dBm; libro Castro/Fusario §§3.5.4–3.5.6, PDF pp.199–200. Las imágenes U2 se vieron en hoja de contacto. `capturas/teoria/06-Canales.../08_10_2026.md` leída íntegra; sus PNG originales 38 páginas inspeccionados visualmente.

## Recalculo y controles

- TP-I E1: `B=3300−300=3000 Hz`, `S/N=10^(30/10)=1000`, `C=29 901,6788 bit/s`.
- E2: para 3000/10000/1000 Hz y 10000 bit/s, respectivamente, `9,58056 / 0 / 30,09876 dB`.
- E4: `s'= (1+100)^2−1=10200`, factor de potencia `S'/S=102`, nueva SNR `40,0860 dB`.
- E5: `s'=50`, SNR `16,9897 dB`, caída capacidad `14,8056%`.
- E6-I: con supuesto explicitado de misma resistencia y tensiones eficaces, `s=4 000 000`, `C=67 987,8637 bit/s`.
- TP-II E4 BER `20/200000=10^-4=0,01%`.
- CRC U6 p.28: resto `1101`, secuencia `1101011101`, verificación resto cero. CRC TP-II E6: resto `0110`, trama `101101011010110`, verificación cero.
- Eficiencias/estimaciones citadas: doble paridad `35/48=72,9167%`; Hamming (7,4) `4/7=57,1429%`; Stop-and-Wait ejemplo `1/21=4,7619%`; ruido térmico didáctico `1,242·10^-17 W`.
- No se detectaron fallas dimensionales, logaritmo equivocado, confusión dB/dBm, tasa/baudios o errores aritméticos en esas cuentas. La atribución del rótulo duplicado $P_2$ de U6 p.38 como errata está respaldada por la tabla y palabra formada.

## Hallazgos

**Ninguno demostrado (P0/P1/P2/P3).** Sin tareas de cierre.

## Limitaciones y estado

- Programa U6 incluye temas adicionales no desarrollados en el material/capturas revisados (p.ej., eco y efecto pelicular). El candidato los marca explícitamente como no cubiertos/no registrados, por lo que no los trato como error del apunte ni los completo con bibliografía.
- El candidato puede ser pedagógicamente consistente y aun no cubrir el programa completo; `en-progreso` es el estado apropiado. No recomiendo elevarlo a `completo` o `revisado` por esta auditoría parcial de fuentes registradas.


---

## Dictamen B

# Revisión pedagógica independiente U6 — B

**Fecha:** 2026-10-13  
**Veredicto:** **APTO CON UNA OBSERVACIÓN MENOR; mantener `en-progreso`.** No hallé bloqueos académicos/cálculos en el contenido contrastado. No promover a `completo/revisado`: eco, efecto pelicular y señalización telefónica siguen explícitamente pendientes por falta de evidencia dentro del corpus autorizado.

## Snapshot y alcance comprobado

- Snapshot inicial: `docs/consolidacion-u1-u6/snapshot-inicial.json` (401 entradas). Comparé hash SHA-256 y tamaño de **53 entradas relevantes** antes de concluir —APUNTE, INDICE, TP, repaso, fuentes/caches U6 y captura U6—: **cero discrepancias**. No modifiqué candidato ni evidencia original.
- Leí integralmente `apuntes/teoria/06-canales-comunicaciones/APUNTE.md` y `INDICE.md`, `apuntes/practica/tp-06-canales.md` (TP-I E1–6 y TP-II E1–10 / enlace Hamming) y `apuntes/repaso/u06-canales.md` (Q-P5-3).
- Contraste visual: PDF teórico U6 pp. 1–38 y las 38 láminas PNG preservadas en la captura; recorrí las páginas en contacto visual y amplié p.14 (factor de ruido), p.25 (paridad), p.28 (CRC) y p.38 (Hamming). Las páginas PNG coinciden con el PDF. Comparé asimismo TP-I p.2 y TP-II pp.2–3; U2 pp.3–11 para dB/dBmV/cable/divisor (amplié pp.5, 9–11), además de las capturas de clase U2, práctica 4 y práctica 5 pertinentes. Consulté los caches U6 y TP como auxiliar, nunca como autoridad.
- Comprobé enlaces/anclas locales de los cuatro documentos: ninguno roto. Contraste externo puntual de los protocolos de E7/E8 con los RFC/recursos citados y disponibles, incluido UDP (RFC 768), IPv4, TCP, ICMP, PPP, SCTP y AAL5.

## Cobertura y QA pedagógica

La progresión física → modelo → formalización/unidades → ejemplo → errores/respuesta oral es consistente en los conceptos centrales. Se distingue con claridad Hz/muestras/s/baudios/bit/s, S/N lineal frente a dB y potencia frente a tensión; las condiciones de tensión/impedancia en TP-I E6 y el alcance cualitativo de TP-II E5 se declaran, no se ocultan. El tratamiento separa detección, retransmisión y FEC; se señalan correctamente los límites de paridad, CRC y Hamming. Secciones 1–23, mapa de procedencia, pendientes, resumen y checklist son navegables y el índice no duplica contenido. La única pregunta de repaso queda marcada como parcial y la solución coincide con la fuente.

Recalculé los resultados principales de TP-I E1–6 (incluido Shannon, SNR/potencias, porcentaje y supuesto de E6), TP-II E4/E6, BER, CRC y Hamming, y revisé los ejemplos numéricos de ruido, atenuación, factor de ruido, paridad y ARQ: no encontré discrepancias. Las cifras reportadas cierran con sus unidades y supuestos.

## Hallazgos

### U06-B-001 — P3 pedagogía/editorial

- **Archivo/ancla:** `apuntes/teoria/06-canales-comunicaciones/APUNTE.md`, §8.1, línea 524: “Térmico, blanco, gaussiano o de Johnson”.
- **Afirmación/evidencia:** el título puede leerse como sinonimia; sin embargo, la explicación posterior (líneas 547–551) correctamente distingue origen térmico, espectro blanco y distribución gaussiana. La lámina U6 p.10 agrupa esos términos en su rótulo.
- **Naturaleza / consecuencia:** ambigüedad menor de memorización, no error en el desarrollo. Un lector que estudie por encabezados podría repetir que “blanco/gaussiano/Johnson” son sinónimos.
- **Acción sugerida:** conservar la atribución a la lámina, pero titular «Ruido térmico (modelo de cátedra: blanco y gaussiano)» o marcar desde el encabezado que son propiedades diferentes.
- **Prueba de cierre:** que el título y el texto permitan responder por separado qué describe el origen, la densidad espectral y la distribución de amplitudes.

**Conteo:** P0 0 · P1 0 · P2 0 · P3 1.

## Limitaciones

Auditoría pedagógica, no reescritura ni revisión integral de U2/U3/U5 o de TP3. Las cuestiones fuera del corpus U6 no se desarrollaron ni se certificaron. No leí informes de autores/revisores ni documentos de registro internos, en cumplimiento del protocolo de ceguera.

**skill_resolution:** injected (AGENTS.md y metodología del proyecto fueron suministrados/leídos; no se requirió una skill adicional).
