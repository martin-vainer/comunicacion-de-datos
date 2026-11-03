# Revisión U03 — A/B

## Dictamen A

# Revisión independiente U03-A — dictamen inicial

- **Identidad:** /root/review_u03_a, revisor académico A, 2026-10-13. `skill_resolution: injected`.
- **Status:** CAMBIOS REQUERIDOS (dos P2 demostrados); sin P0/P1/P3. No se autoriza «unidad final/revisada»: el alcance deliberadamente parcial y los pendientes RDSI permanecen explícitos.
- **Independencia:** no se emplearon dictámenes de otros revisores, reportes de autores, autocontroles/qa-autor.json ni memoria ajena como evidencia. El contenido QA autoafirmado del candidato no se tomó como prueba. Inventario utilizado para localizar rutas adicionales, sin adoptar sus conclusiones. Ningún candidato/original/cache/shared fue editado; sólo derivados propios en `tmp/reviews/u03-a/` e informe.
- **Snapshot:** `docs/consolidacion-u1-u6/snapshot-inicial.json`, SHA-256 `1e29fd3bf30b9d99d07e0d3b73e2d7ef11f9d85bb7874b2630650412068a7bdd`. 401 entradas comprobadas antes y después: **401/401 coinciden**, cero alteraciones respecto del snapshot y entre mediciones. Evidencia propia: `u03-a/hash-before.json`, `u03-a/hash-after.json`.

## Identidad de los candidatos

| Archivo | SHA-256 |
|---|---|
| `apuntes/teoria/03-redes-telecomunicaciones/APUNTE.md` | `2962e0145bd662919d87308fbe3ce4ed1d9ab457abd6526569b272a2666a6303` |
| `apuntes/teoria/03-redes-telecomunicaciones/INDICE.md` | `f3e53a80ab0a1159713fbe14e27aa76a769b23d0adc5a4aa26e3683353e4b26a` |
| `apuntes/practica/tp-03-redes.md` | `5ce621ffa1a5117120f785dcc7c51eec65a22ef03802d81e0d5caf190511d082` |
| `apuntes/repaso/u03-redes.md` | `d4838fb67f6f3ea6e6864ca0beb11c3296caccde56711fcc2bdbb6daa9f2a8bf` |

## Fuentes efectivamente examinadas

Los caches correspondientes se leyeron como auxiliares; los originales se renderizaron con Poppler y se observaron, no sólo se extrajo texto. F3/FV completas en contactos legibles; G3 p.2–3 además observadas individualmente. Capturas Markdown completas, incluidos segmentos mixtos para clasificar destino; todos sus 23 anexos de imagen observados.

| ID | Original | Páginas vistas | Alcance efectivo |
|---|---|---|---|
| F3 | `material/teoria/U3/U3 Redes de Telecomunicaciones.pdf` | 1–28, todas | Corpus teórico completo, figuras/tablas incluidas |
| FV | `material/practica/U 3/UT 3 MEDIDA VELOCIDAD.pdf` | 1–17, todas | Velocidades/sincronismo, relaciones dB, ejemplos y tablas |
| G3 | `material/practica/U 3/TP   3   2026.pdf` | 1–4, todas; 2–3 individuales | E1–18 completos; E19 sólo procedencia/referencia |
| R1 | `material/practica/U 3/EXPRESIONES  Y RTAS UD NRO 3 (1ra PARTE).pdf` | 1–3, todas | Todas respuestas E1–11 |
| R2 | `material/practica/U 3/EXPRESIONES  Y RTAS UD NRO 3 (2da PARTE).pdf` | 1–5, todas | Todas respuestas E12–18 |
| C4 | `capturas/teoria/03-redes-telecomunicaciones/apuntes-clase 4.md` | Documento completo + image.png/image-1.png/image-3.png | Velocidades, multinivel, direcciones/modos, sincronismo |
| C5 | `capturas/teoria/03-redes-telecomunicaciones/apuntes-clase 5.md` | Documento completo + image-2.png/image-4.png/image-5.png | Protocolos, redes, costos y topologías |
| TQ | `capturas/teoria/03-redes-telecomunicaciones/cuestionario_U3.md` | Documento completo + image-6.png | Q1/Q3 U3; Q2 Fourier sólo localizado U2 |
| P3 | `capturas/practica/clase 03.md` | Documento completo + image-16.png | Velocidades U3; Fourier sólo clasificación U2 |
| P4 | `capturas/practica/clase 04.md` | Líneas 1–1808 completas + image-17.png a image-31.png | E1–18 y ejemplos; E19 referencia; banda a−3 dB U2 y fundamentos dB U6 |
| P5 | `capturas/practica/Clase 05.md` | Documento completo | Q1/Q2/Q4 U3; Q3 dBm identificado U6, NO imputado como pérdida U3 |
| EQ | `Ejercicio cuestionario 10-09-2026.pdf` | 1–3, todas | Es sólo Fourier Q2: pertenece U2, no contenido U3 perdido |
| E19G | `material/practica/TRABAJO PRACTICO  EJ 19 CALCULO ENLACE.pdf` | 1–3, todas | Control de referencia, enunciado y cuatro conectores; no revisión integral nueva de E19 |
| E19R | `Martín Vainer - Comunicación de Datos.pdf` | 1–3, todas | Manuscrito observado para identidad del recurso ligado a E19; no reescritura/certificación |
| E19M | `material/practica/Martín Vainer - CD.pdf` | 1–6, todas | P.1–3 enunciado, p.4–6 manuscrito; identidad/referencia E19 |
| PA | `material/catedra/PROGRAMA de la materia.pdf` | p.3, sección U3 completa | Contraste del alcance programático; no revisión integral del programa |
| I430 | [UIT-T I.430 (11/1995), resumen oficial](https://www.itu.int/ITU-T/recommendations/rec.aspx?lang=es&rec=3248) | Resumen español, líneas web 53–55 | Confirma interfaz S/T y 192 kbit/s. No se utilizó PDF nuevo sin cache |

Total: **72 páginas originales de fuentes asociadas vistas**, más p.3 del programa; seis capturas completas y 23 imágenes. Fuentes E19/Fourier examinadas para clasificación/procedencia, sin convertirlas en nuevas revisiones de otras unidades.

## Tabla de cobertura exacta: teoría y navegación

| Sección APUNTE / líneas | Contraste efectuado | Resultado/límite |
|---|---|---|
| Alcance/fuentes/mapa, 21–65 | PA p.3; F3/FV/G3 y seis capturas | Exclusiones visibles correctas; no equivalencia con programa completo |
| §1 velocidades, 67–118 | F3 p.2–4; FV p.2–5; C4/P3/P4 | Cuatro numeradores diferenciados, símbolos y conversiones; desigualdad no estricta justificada |
| §2 multinivel/banda, 120–183 | F3 p.2/4–5; FV p.2–5; P4 image-18; G3 E4/R1 p.2 | 12 bits→6 dibits, estados y criterio primer cero correctos; no afirma capacidad Shannon |
| §3 sentidos/modos, 185–210 | F3 p.5–7; C4; TQ Q3 | Tres sentidos, serie/paralelo, dos canales≠dos cables; ejemplo 8 ms/1 ms correcto |
| §4 sincronismo/rendimiento, 212–282 | F3 p.8–11; FV p.6–8; C4/C5/P4; G3/R1 E3/E5–7/E11 | Tres sincronismos, framing, supuestos, 1,5 parada y recálculos correctos |
| §5 protocolos, 285–306 | F3 p.9–11 y árbol C5 | Definiciones/limitación KERMIT claras; **U03-A-002** por agrupación ambigua LAP |
| §6 redes/enlaces/costos, 309–342 | F3 p.12–15; C5 y sus imágenes | Corrección de costos confirmada leyendo mínimos: circuitos→paquetes→dedicada |
| §7 conmutación, 345–362 | F3 p.14/16/19; C5 | Sesión/circuito vs paquetes y circuito virtual vs reserva física diferenciados; no throughput inventado |
| §8 topologías, 364–419 | F3 p.17–18; C5 tabla/diagramas | Cinco tipos, 6/10 enlaces correctos; tabla histórica limitada, no ranking universal |
| §9 RTPC, 422–451 | F3 p.19–25 texto/figuras | Abonados/lazos/centrales/troncales, espacio/tiempo, PBX, evolución VoIP, 2H/4H e híbridos; no ampliación U8 |
| §10 tráfico/señalización, 454–484 | F3 p.26 y contexto 19–25 | Erlangs y llamadas/h×h/llamada correctos; distingue medias y límites de dimensionamiento |
| §11 RDSI, 487–501 | F3 p.27–28 + resumen I.430 | Sumatorias correctas; BRI160 y PRI Europa explícitamente no validados/excluidos de examen |
| Pendientes/resumen/checklist, 504–533 | Metodología §§6–8; contraste propio anterior | Estados honestos; QA de autor ignorado como certificación; checklist conecta conceptos |
| INDICE completo, 1–21 | 90 enlaces propios del paquete, sección destino | Navegación breve, rutas/anclas existentes; no duplicación de teoría/estado |

Compresión, grado de servicio/dimensionamiento, hiperservicios, gestión y restantes exclusiones declaradas no son errores de cobertura del alcance autorizado. Impiden anunciar unidad final programática, pero NO obligan a inventar temas.

## Tabla exacta: práctica y recálculos

Todas las relaciones algebraicas fueron verificadas contra el problema descrito, tablas de símbolos, unidades y supuestos. Los 98 controles numéricos independientes (incluidas conversiones, balances inversos y 16 filas de tabla) figuran en `u03-a/numeric-recalculation.json`: **98/98 pasan**. No se reutilizó script/autocontrol del autor.

| Ítem / líneas TP | Fuente original/página | Verificación y resultado |
|---|---|---|
| Herramientas 34–88 | FV p.2–17; G3/R1/R2 | Bit/s≠baud; eficiencia fraccional; niveles dBm±dB; margen no pérdida física |
| E1 91–107 | G3 p.2; R1 p.1; P4 E1 | 8000/1200=6,6666667 s; 8 bit/carácter y binario explícitos |
| E2 110–116 | G3 p.2; R1 p.1 | log2(2)=1; igualdad numérica, no de unidades |
| E3 119–133 | G3 p.2; R1 p.1; P4 E3 | 1+8+1+1,5=11,5; 17250/75=230 s; datos160 s/overhead70 s |
| E4 136–149 | G3 p.2; R1 p.2; P4 E4 | 4 bit/símbolo;16 estados;833,333 µs |
| E5 152–163 | G3 p.2; R1 p.2; P4 E5 | 1500/1518=98,81422925%;control1,18577% |
| E6 166–177 | G3 p.2; R1 p.2; P4 E6 | Ambos casos:7/9=77,7778%,7/10=70% |
| E7 180–194 | G3 p.2; R1 p.2–3; P4 E7 | Sync3,413333 s,async5,12 s,66,6667%; caída33,3333 pp/suba tiempo50% |
| E8 197–203 | G3 p.2; R1 p.3; F3 p.2–4; P5 Q1 | Acortar pulso duplica baud/primer cero; aumento ruido sólo bajo supuestos |
| E9 206–212 | G3 p.2; R1 p.3 | Access rate≠throughput/Shannon;2400×0,7=1680 bit/s |
| E10 215–221 | G3 p.2; R1 p.3 | Factores físicos vs control; BER adimensional |
| E11 224–240 | G3 p.2; R1 p.3; P4 líneas693–777 | 14400/0,9/3600=4,4444444 s; **U03-A-001** atribución falsa del error a P4 |
| E12 243–257 | G3 p.2; R2 p.1; P4 E12/image-25 | 10,8 dB;−4,2 dBm=0,3801894 mW |
| E13 260–276 | G3 p.3; R2 p.2; P4 E13/image-26 | 7 dB;salida−7 dBm=0,1995262 mW; no umbral inventado |
| E14 279–300 | G3 p.3; R2 p.2–3; P4 E14/image-27 | 33,0103−9=24,0103 dBm;251,7850824 mW; signo del umbral correcto |
| E15 303–321 | G3 p.3; R2 p.3; P4 E15/image-28 | Reserva10 dB, conectores1,2 dB;fibra1,8 dB;600m/9000m |
| E16 324–338 | G3 p.3; R2 p.3–4; P4 E16/image-29 | 40 dB;33 dBm=1995,262315 mW;Rx−7 dBm |
| E17 341–357 | G3 p.3; R2 p.4; P4 E17/image-30 | (3,0103+60)/30=2,100343332 dB/km;máximo, no mínimo |
| E18 360–381 | G3 p.3; R2 p.4–5; P4 E18/image-31 | RG58 total51 dB,Rx−1 dBm,Gmín31 dB;RG218 total9 dB,Rx41 dBm,margen11 dB |
| E19 referencia 384–386 | G3 p.4; E19G p.2–3; recurso existente | Enlace válido; escenarios/3–6–9 dB/fibra concuerdan; no certificación integral nueva |
| P4 A 393–405 | FV p.12; P4 image-22 | Rx13,6 dBm,umbral≤10,6 dBm;reserva3 dB |
| P4 B 407–421 | FV p.13/15; P4 amplificación | Dos duplicaciones3,01030 dB,cuadruplicación6,02060 dB;43 dB=19952,62315 veces |
| P4 C 423–436 | FV p.16; P4 cablemódem | 42,9→139,636836 mV;2,3→1,30316678 mV;20log, referencia1 mV |
| P4 D 438–474 | FV p.17; tabla P4 | 16 filas coinciden con original;3,28083990 factor de unidades;55MHz/200m→10,5 dB;divisor−3,01030 dB |

Se recalcularon también todos los ejemplos del APUNTE: cuatro tasas1000/800/760 y100/95 byte/s;1200×log2(2/4),dos canales4800 bit/s;serie8ms/paralelo1ms;malla6/10 y4 enlaces nuevos;tráfico3 Erlangs;RDSI144/1536/2048 kbit/s (última suma confirma sólo dato impreso pendiente). Ejemplo60s/10s de circuitos es conceptual: no inventa resultado de throughput.

## Repaso: cinco preguntas completas

| ID | Origen / evidencia | Control efectivo |
|---|---|---|
| U3-TQ1 | TQ Q1; APUNTE §1 | 8 Mbit,5m/s,umbral133333,3333m;desigualdad estricta;opciones y supuestos verificados |
| U3-TQ3 | TQ Q3; F3 p.6 | Simplex; distractores justificados por dirección/simultaneidad |
| U3-PQ1 | P5 Q1; F3 p.2–4 | Opción b con forma/filtro/densidad ruido explícitos; no «siempre» |
| U3-PQ2 | P5 Q2; F3 p.3/FV p.5 | Útiles/correctos por tiempo;bit/s vs baud vs byte/s |
| U3-PQ4 | P5 Q4; F3 p.2/FV p.5 | 4 estados→2 bit/símbolo;1000baud→2000bit/s;contraejemplos |

Enunciados separados de soluciones; evidencia y criterios razonados. Q2 Fourier tiene destino U2 comprobado; Q3 dBm tiene destino U6 comprobado, no pérdida de U3.

## Figuras y recursos

**17/17 PNG de candidatos tienen SHA-256 idéntico a su captura original**, obtenido buscando hashes propios, sin leer manifiesto de autor. `u03-a/image-copy-hashes.json` conserva correspondencias/hash. Todos fueron vistos en las capturas originales y comparados con las páginas de filminas cuando existen.

| PNG candidato | Original inmutable | Contraste PDF |
|---|---|---|
| sentidos | C4 image.png | F3 p.6 |
| serie-paralelo | C4 image-1.png | F3 p.7 |
| sincronismo-bit | C4 image-3.png | F3 p.8 |
| nube | C5 image-2.png | F3 p.12 |
| costos-volumen | C5 image-4.png | F3 p.15 |
| circuitos-paquetes | C5 image-5.png | F3 p.16 |
| multinivel | P4 image-18.png | FV p.4/F3 p.5 |
| asincronico | P4 image-19.png | FV p.7/F3 p.10 |
| sincronico | P4 image-20.png | FV p.8/F3 p.11 |
| balance-ejemplo | P4 image-22.png | FV p.12 |
| tp12 | P4 image-25.png | R2 p.1/G3 p.2 |
| tp13 | P4 image-26.png | R2 p.2/G3 p.3 |
| tp14 | P4 image-27.png | R2 p.2/G3 p.3 |
| tp15 | P4 image-28.png | R2 p.3/G3 p.3 |
| tp16 | P4 image-29.png | R2 p.3/G3 p.3 |
| tp17 | P4 image-30.png | R2 p.4/G3 p.3 |
| tp18 | P4 image-31.png | R2 p.4/G3 p.3 |

Además vistos: TQ image-6/P3 image-16 (Fourier U2), P4 image-17 (velocidades), image-21 (amplificador/atenuador), image-23 (banda U2), image-24 (balance y error unidad advertido). Figuras no copiadas F3 p.17–18/21–28 leídas para sustentar sus secciones. Mermaid de malla enumera los seis enlaces sin dobles conteos. Mermaid de protocolos requiere aclaración U03-A-002. No se ejecutó render/build de Mermaid: verificación semántica/sintaxis estática, no de compatibilidad de un visor.

## Issues

### U03-A-001 — P2 — Se atribuye a P4 un error que su texto no contiene

- **Archivo/ancla/líneas:** `apuntes/practica/tp-03-redes.md#e11`, línea240; repetido en tabla de discrepancias, línea483.
- **Claim:** «R1 p.3 y P4 calculan […] agregan0,4s y dan4,4s» / «R1/P4 suma10% al tiempo».
- **Evidencia:** R1 p.3 sí suma0,4s y obtiene4,4s. En cambio `capturas/practica/clase 04.md`, sección E11, líneas753–777, presenta η=Tideal/Ttotal, despeja Ttotal=Tideal/η y calcula4/0,9≈4,44s. Snapshot asegura que se comparó el original recibido, no uno corregido durante revisión.
- **Naturaleza:** demostrado; error de trazabilidad histórica, **no** de resultado consolidado.
- **Impacto:** se registra una discrepancia falsa con una captura inmutable correcta; degrada confianza y atribuye al estudiante un error inexistente en ese registro.
- **Acción mínima:** limitar atribución al solucionario R1. Explicitar que P4 ya contiene el método correcto. No cambiar captura ni fórmula/resultado correcto del candidato.
- **Prueba de cierre:** contrastar nuevamente R1 p.3 y P4 E11; quitar todas las imputaciones equivalentes a «P4 suma10%» y conservar4,4444444s.

### U03-A-002 — P2 — Nodo agrupado oculta qué familia tiene variantes LAP-B/D/F

- **Archivo/ancla/líneas:** `apuntes/teoria/03-redes-telecomunicaciones/APUNTE.md#protocolos`, líneas298–299.
- **Claim/representación:** `B --> B1[HDLC, LAP y LLC]` seguido de `B1 --> L[LAP-B, LAP-D y LAP-F]`.
- **Evidencia:** F3 p.9 vincula B/D/F a **LAP**; C5 sección «Protocolo asociado a una transmisión» lo representa explícitamente con HDLC,LAP,LLC como hermanos y B/D/F sólo hijos de LAP.
- **Naturaleza:** demostrado como pérdida de precisión de la relación en el diagrama consolidado; no se afirma que el autor haya escrito una clasificación textual falsa.
- **Impacto:** el modelo mental permite interpretar variantes de todo el grupo; una relación importante se vuelve ambigua justo en el recurso destinado a aclararla.
- **Acción mínima:** separar HDLC,LAP,LLC en nodos hermanos y enlazar LAP→LAP-B/D/F. Mantener advertencia de KERMIT y no agregar formatos de tramas.
- **Prueba de cierre:** inspección estática del árbol: sólo el nodo LAP debe tener descendientes LAP-B/D/F; contraste con F3 p.9 y C5.

## QA real, límites y dictamen

- Python bundled y Poppler verificados en esta sesión. Render de originales correcto, con advertencias Symbol/ArialUnicode registradas; fórmulas/tablas críticas legibles y contrastadas con texto y recálculos. No instalación/build/commit.
- **90 enlaces locales comprobados, cero rutas/anclas fallidas**. Links a manifiesto/qa-autor sólo existencia: sus conclusiones/contenido NO leídos/usados. Evidencia `u03-a/links.json`.
- Fuentes/candidatos completos dentro del corpus U3 autorizado: no muestreo rotulado integral. Programa sólo sección U3. E19 preexistente se leyó para comprobar enlace/afirmaciones usadas, no para renovar su estado revisado.
- 160 kbit/s BRI y PRI Europa siguen pendientes contextualizados. No son conocimientos confirmados evaluados; no imputarlos como errores nuevos de cuenta. La descripción192kbit/s S/T sí está respaldada por resumen oficial I.430.
- No cobertura nueva de U7/U8 ni evaluación de temas excluidos. No se promete programa completo ni funcionamiento real del amplificador con sólo presupuesto de potencia.
- **Dictamen inicial:** aplicar los dos cambios P2 al finalizar la ronda ciega y revalidar específicamente atribución E11/árbol LAP. Las matemáticas de E1–18 y A–D y las cinco preguntas U3 no presentan error demostrado. Mantener estado `en-progreso` y exclusiones/pedientes; no declarar unidad final programática. Los originales permanecen íntegros.

## Key Learnings:

1. En E11, P4 ya divide4/0,9; el método de sumar10% pertenece a R1 p.3, no a esa captura.
2. Agrupar HDLC,LAP,LLC en un nodo Mermaid vuelve ambigua la descendencia LAP-B/D/F; la jerarquía debe conservarse explícitamente.


---

## Dictamen B

# Revisión pedagógica independiente U03-B

## Identidad, alcance y dictamen

- Revisor: B, independiente de autores y otros revisores. Fecha: 2026-10-13. `skill_resolution: injected` (reglas compactas recibidas; AGENTS.md y metodología releídos; workflow PDF de lectura visual aplicado).
- Raíz: `C:/Users/Martin/Documents/UTN_SISTEMAS/Anual_2026/comunicacion_de_datos`.
- **Dictamen: CON OBSERVACIONES; requiere dos correcciones P2 antes de cerrar este paquete.** P0=0; P1=0; P2=2; P3=0. No se encontró pérdida de ejercicios, preguntas o fragmentos U3 del corpus asignado. No se certifica toda la unidad del programa ni se promueve `en-progreso`.
- Candidatos íntegros leídos: `apuntes/teoria/03-redes-telecomunicaciones/APUNTE.md` (incluye once secciones, alcance, cierre y pendientes), `INDICE.md`, `apuntes/practica/tp-03-redes.md` E1–18 y ejemplos A–D, `apuntes/repaso/u03-redes.md` cinco preguntas. Las autocertificaciones del candidato no son evidencia de este dictamen; no se abrieron controles de autor, reportes de otros revisores, estado.md, revisiones.md ni memorias ajenas.
- E19: se verificó únicamente existencia/enlace y correspondencia del resumen con G3 p.4 y encabezado de la resolución preexistente. No se reescribió ni se revalidó su solución/U7. U7/U8 fuera de alcance.

### Snapshot e integridad

Snapshot: `docs/consolidacion-u1-u6/snapshot-inicial.json`, SHA-256 `1e29fd3bf30b9d99d07e0d3b73e2d7ef11f9d85bb7874b2630650412068a7bdd`, **401 entradas**. Control independiente antes: **401/401 idénticas**, ninguna ausencia. Control después: **401/401 idénticas**, ninguna ausencia. Evidencia completa en `u03-b/hashes-antes.json` y `u03-b/hashes-despues.json`.

| Candidato | SHA-256 observado |
|---|---|
| APUNTE.md | 2962e0145bd662919d87308fbe3ce4ed1d9ab457abd6526569b272a2666a6303 |
| INDICE.md | f3e53a80ab0a1159713fbe14e27aa76a769b23d0adc5a4aa26e3683353e4b26a |
| tp-03-redes.md | 5ce621ffa1a5117120f785dcc7c51eec65a22ef03802d81e0d5caf190511d082 |
| u03-redes.md | d4838fb67f6f3ea6e6864ca0beb11c3296caccde56711fcc2bdbb6daa9f2a8bf |

Los **17 PNG de recursos** fueron hasheados contra imágenes de capturas, sin usar manifiesto de autor: 17/17 idénticos. Tabla completa origen→copia/hash en `u03-b/images.json`. Sólo se escribieron este informe y recursos propios bajo `tmp/reviews/u03-b/`; ningún build, instalación, commit, reparación de candidato ni modificación de originales/caches.

## Fuentes y QA real

Identificadores de fuentes usados en las tablas siguientes (todos bajo la raíz indicada):

| ID | Fuente original / lectura efectiva |
|---|---|
| Programa | `material/catedra/PROGRAMA de la materia.pdf`, p.3, texto y visual de U3 |
| F3 | `material/teoria/U3/U3 Redes de Telecomunicaciones.pdf`, **p.1–28 completas**, texto/cache y visual |
| FV | `material/practica/U 3/UT 3 MEDIDA VELOCIDAD.pdf`, **p.1–17 completas**, texto/cache y visual |
| G3 | `material/practica/U 3/TP   3   2026.pdf`, **p.1–4 completas**, visual; p.2–4 ampliadas |
| R1 | `material/practica/U 3/EXPRESIONES  Y RTAS UD NRO 3 (1ra PARTE).pdf`, **p.1–3 completas**, texto y visual; p.3 ampliada |
| R2 | `material/practica/U 3/EXPRESIONES  Y RTAS UD NRO 3 (2da PARTE).pdf`, **p.1–5 completas**, texto y visual; p.3 ampliada |
| C4 | `capturas/teoria/03-redes-telecomunicaciones/apuntes-clase 4.md`, íntegra, 03/09/2026 |
| C5 | `capturas/teoria/03-redes-telecomunicaciones/apuntes-clase 5.md`, íntegra, sin fecha explícita |
| TQ | `capturas/teoria/03-redes-telecomunicaciones/cuestionario_U3.md`, íntegra; Q2 sólo distribución U2 |
| P3 | `capturas/practica/clase 03.md`, íntegra; tramo Fourier separado como U2 |
| P4 | `capturas/practica/clase 04.md`, íntegra E1–18 y ejemplos; E19 sólo referencia |
| P5 | `capturas/practica/Clase 05.md`, íntegra; Q3 distribuida U6 |

Caches de esos cinco PDFs leídos completos como auxiliares, **no autoridades independientes**. Se comprobó disponibilidad actual de Python bundled, PIL, pypdf y pdftoppm. Render independiente: 57 páginas U3 + p.3 del programa; contactos cada cuatro páginas, originales ampliados cuando la densidad de los enunciados requería lectura. Todas las páginas fueron observadas, no una muestra. Recursos `f3-*`, `fv-*`, `g3-*`, `r1-*`, `r2-*`, `programa-*` dentro del directorio propio.

- **22 imágenes referidas por C4/C5/TQ/P4 observadas** en cuatro contactos propios, `capt-contact-1/7/13/19.jpg`: teoría image.png/image-1…6.png y práctica image-17…31.png. Fourier image-6 sólo identificación y destino U2; no se atribuye su exclusión a pérdida U3. Los 17 PNG de candidato son byte a byte iguales a originales ya observados. Figuras de RTPC/RDSI/topologías restantes se contrastaron en F3, aunque no se copien al candidato.
- **40 recálculos primarios independientes, 40/40 correctos**, guardados en `calculations.json`; se comprobaron además conversiones y controles inversos impresos, fracciones de eficiencia, desigualdades y supuestos, no sólo su coincidencia con solucionarios. E2/E8/E10 son controles conceptuales sin respuesta numérica requerida. La tabla de 16 frecuencias del ejemplo D fue cotejada íntegramente con FV p.17/P4, incluidos redondeos.
- **86 enlaces locales** de APUNTE/INDICE/práctica/repaso comprobados, 86/86 archivo y ancla existentes: `links-final.json`. Se excluyen enlaces a QA/manifiesto de autor, intencionalmente no leídos. Un primer parser falló al interpretar paréntesis en nombres PDF; fue sustituido por el parser con paréntesis equilibrados. Es un fallo de herramienta de revisión, **no un enlace roto del candidato**.
- Contraste externo limitado a la referencia ya incluida: [resumen oficial UIT-T I.430 (11/1995)](https://www.itu.int/ITU-T/recommendations/rec.aspx?lang=es&rec=3248), consultado 13/10/2026: declara puntos S/T y 192 kbit/s. Respalda la precisión del candidato sin resolver por inferencia los 160 kbit/s sin interfaz de F3.

## Tabla exhaustiva de fragmentos → destinos / tratamiento

El destino se refiere a APUNTE U3 salvo que se indique TP o repaso. Agrupar fuentes coincidentes no elimina fragmentos: cada sección original identificada tiene tratamiento explícito.

| Fragmento original y localización | Destino / tratamiento comprobado |
|---|---|
| C4 medidas: modulación, transmisión, transferencia, real y desigualdad; P3 repaso; FV p.2–5; F3 p.2–3 | §1 `#velocidades`; símbolos→bits→útiles→correctos; distingue bit/s/byte/s y admite igualdades |
| C4 AB, costos y relación Vm/Vtx; F3 p.4 | §2 `#multinivel`; banda necesaria y criterio rectangular; costos de uso en §6, no universaliza mayor AB/mayor precio como ley |
| C4 multinivel; P3 suma de m canales y n=2^N; P4 repaso/multinivel; FV p.2–5/F3 p.5 | §2; fórmula individual/agregada, ejemplo dos canales, secuencia de seis dibits; image-18→multinivel.png |
| C4 simplex/half/full y image.png; F3 p.6 | §3 `#sentidos-modos`; tres ejemplos, simultaneidad vs cables; sentidos.png preservado |
| C4 serie/paralelo e image-1; F3 p.7 | §3; ejemplo 8 bits/8 vías, limita tendencia distancia/velocidad; serie-paralelo.png preservado |
| C4 bit/carácter/bloque e image-3; F3 p.8; P4 definición/FV p.6 | §4 `#sincronismo`; identifica qué frontera se sincroniza; sincronismo-bit.png |
| C5 árbol de protocolos; F3 p.9 | §5 `#protocolos`; definición, árbol, precaución KERMIT; defecto de padre LAP: **U03-B-002** |
| C5 asincronía, arranque/parada/paridad, tiempos y características; P4 image-19; F3 p.10/FV p.7 | §4; tabla, símbolos, supuestos y E3/E6; no usa “mejor en canales pobres” como ley; asincronico.png |
| C5 bloque, características y compromiso; P4 header/final e image-20; F3 p.11/FV p.8 | §4; eficiencia E5/E11, repetición costosa con bloque largo; campos de dirección no universales; sincronico.png |
| C5 composición/terminales/nodos/enlaces/nube; image-2; F3 p.12 | §6 `#redes`; función de cada elemento y ejemplo cuatro accesos; nube.png |
| C5 punto a punto, difusión multipunto, conmutada, Internet; F3 p.13 | §6 tabla; explica bus Ethernet como ejemplo, no todo Ethernet |
| C5 enlaces según puntos/características; F3 p.14 | §6; criterios independientes dedicado/conmutado y punto a punto/multipunto |
| C5 costos vs volumen e image-4; F3 p.15 | §6; mínimo circuitos→paquetes→dedicada; corrige captura invertida con evidencia; costos-volumen.png |
| C5 circuitos/paquetes e image-5; F3 p.14/16 | §7 `#conmutacion`; establecimiento/ocupación/colas, circuito virtual y datagrama; ejemplo 60 s/10 s; circuitos-paquetes.png |
| C5 malla, fórmula, dibujos; F3 p.17 | §8 `#topologias`; 4 nodos=6 enlaces, quinto añade4; Mermaid malla completo |
| C5 estrella, bus, anillo, híbridas; F3 p.17–18 | §8 tabla; centros, medio común, recorrido, combinación; ejemplos y compromisos cualitativos preservados |
| C5 cuadro comparativo; F3 p.18 | §8; cinco filas y cuatro topologías cotejadas; conserva como cuadro de cátedra, no ley universal |
| F3 p.19 RTPC fases y componentes | §9 `#rtpc`; establecimiento/mantenimiento/desconexión y cuatro componentes |
| F3 p.20–22 espacio/tiempo; matrices3 etapas y bus | §9; rutas vs intervalos y ejemplo dos comunicaciones; PCM/TDM desarrollo U4, sin dimensionamiento nuevo |
| F3 p.23 pública/privada y planos | §9; PSTN/PBX, urbano/interurbano/internacional y control; no describe arquitectura histórica como regla actual |
| F3 p.24 tres esquemas voz/datos/VoIP | §9; separación, gateways e integración con camino secundario; sin ampliar productos/hardware U8 |
| F3 p.25 2H/4H, híbridos y balance | §9; explica separación de sentidos, no exige cuatro hilos para full duplex; eco/balance U6 |
| F3 p.26 SAC/SCC | §10 `#trafico`; control asociado/común; A/D no universalizados |
| F3 p.26 A=C×TR y gráfico horario | §10; λ×TR, unidades, 3 Erlangs hipotéticos y diferencia media/pico; sin ErlangB/C |
| F3 p.27 integración servicios y lista PCM/TDM/PDH/SDH/SONET | §11 `#rdsi`, referencia U4; no se desarrolla jerarquía nueva en U3 |
| F3 p.28 B/D y tabla BRI/PRI | §11; sumas BRI/USA cotejadas, BRI160 y PRI Europa pendientes explícitos y no evaluados como hechos confirmados |
| P3 señales periódicas/Fourier, TQ Q2/image-6 | Destino U2: APUNTE y repaso U2 F15 existente; sólo distribución/enlaces en U3. **No pérdida U3** |
| P4 dB/logaritmos/unidades relativas/absolutas; FV p.9–11 | Base U6, herramientas TP comunes para no repartir resolución; ningún catálogo U7/U8 |
| P4 usos y tabla valores dB, ejemplo dos amplificadores/image-22; FV p.12 | TP A y B: 13,6 dBm recibidos, umbral≤10,6; redondeos3/6 dB declarados |
| P4 tres ganancias 10→20/40→80/10→40W; FV p.13 | TP B: 3,0103/3,0103/6,0206dB; cociente, no potencia absoluta |
| P4 banda −3dB/image-23; FV p.14 | Marco U2; TP declara destino. Imagen reconocida, no pérdida U3 ni fórmula nueva aquí |
| P4 amplificador43dB; FV p.15 | TP B: factor19952,62315; sólo ganancia registrada, sin certificar ficha de equipo |
| P4 cablemódem42,9/2,3dBmV; FV p.16 | TP C:139,636836/1,30316678mV, referencia1mV y factor20, no dBm |
| P4 tabla16frecuencias/coaxial75Ω/divisor; FV p.17 | TP D: tabla completa y unidades,10,5dB hipotéticos para200m, divisor−3,0103dB; no especificación universal de todo coaxial |
| P4 balance general y ejemplo1200m/image-24 | TP herramientas/E12; margen como reserva y dBm±dB=dBm; imagen mixta con radio no se desarrolla como U7 |
| G3 p.2 E1/P4 E1/R1 p.1 | TP `#e01`:6,66667s condicionado a8bits y n2; faltantes del enunciado visibles |
| G3 p.2 E2/P4 E2/R1 p.1 | TP `#e02`:n2/1bit por símbolo; igualdad numérica no igualdad de magnitudes |
| G3 p.2 E3/P4 E3/R1 p.1 | TP `#e03`:11,5 tiempos,230s; parada1,5 viene de R1; corrige intercambio paridad/parada de P4 sin editarla |
| G3 p.2 E4/P4 E4/R1 p.2 | TP `#e04`:16 estados,4bits/símbolo,833,333µs |
| G3 p.2 E5/P4 E5/R1 p.2 | TP `#e05`:98,8142%, mismo byte arriba/abajo |
| G3 p.2 E6/P4 E6/R1 p.2 | TP `#e06`:77,7778%/70%, ambos casos del enunciado |
| G3 p.2 E7/P4 E7/R1 p.2–3 | TP `#e07`:100%/66,6667%,3,41333/5,12s; distingue puntosporcentuales y50% de aumento de tiempo |
| G3 p.2 E8/P4 E8/R1 p.3 | TP `#e08`:causa física banda/deformación, ruido condicionado, no relación absoluta |
| G3 p.2 E9/P4 E9/R1 p.3 | TP `#e09`:tasa nominal de acceso, no throughput ni Shannon;1680bit/s hipotéticos |
| G3 p.2 E10/P4 E10/R1 p.3 | TP `#e10`:AB/Vm/SN/BER/pulso/modulación preservados y clasificados, BER no bit/s |
| G3 p.2 E11/P4 E11/R1 p.3 | TP `#e11`:4,44444s correcto; atribución falsa a P4: **U03-B-001** |
| G3 p.2 E12/P4 E12 e image-25/R2 p.1 | TP `#e12`:−4,2dBm/0,380189mW, control inverso;tp12.png |
| G3 p.3 E13/P4 E13 e image-26/R2 p.2 | TP `#e13`:−7dBm/0,199526mW; salida no sensibilidad;tp13.png |
| G3 p.3 E14/P4 E14 e image-27/R2 p.2–3 | TP `#e14`:251,785082mW, precisión interna y umbral≤recepción;tp14.png |
| G3 p.3 E15/P4 E15 e image-28/R2 p.3 | TP `#e15`:600/9000m,2 conectores1,2dB y FD10;tp15.png |
| G3 p.3 E16/P4 E16 e image-29/R2 p.3–4 | TP `#e16`:33dBm/1995,262315mW,FD3;tp16.png |
| G3 p.3 E17/P4 E17 e image-30/R2 p.4 | TP `#e17`:α≤2,100343dB/km,sin margen declarado;tp17.png |
| G3 p.3 E18/P4 E18 e image-31/R2 p.4–5 | TP `#e18`:RG58 déficit31dB;RG218 recepción41dBm/margen11dB;tp18.png; no inventa inciso c |
| G3 p.4/P4 E19 y archivo previo | TP `#e19` e INDICE:enlace existente y resumen fiel; excluida revisión de solución |
| TQ Q1 perro | Repaso U3-TQ1:8Mbit,5m/s,d<133,333km,latencia vs tasa;originales a–e preservados |
| TQ Q3 radiodifusión | Repaso U3-TQ3:simplex,respuesta explica sentido;opciones a–e preservadas |
| P5 Q1 banda/ruido | Repaso U3-PQ1:b de captura con hipótesis de ruido explícita;distractores explicados |
| P5 Q2 transferencia real | Repaso U3-PQ2:c,útiles/correctos/tiempo y bit/s;distractores explicados |
| P5 Q3 dBm | Repaso U6 `#q-p5-3` encontrado; distribución y enlace U3. **No pérdida U3** |
| P5 Q4 baudios/bit/s | Repaso U3-PQ4:b,4 estados/1000baudios→2000bit/s;opciones y explicación preservadas |

## Evaluación pedagógica efectiva

La progresión va de contar intervalos/bits a framing, después organización de la red y ocupación telefónica. §1/2/4/8/10 tienen formalización, tablas de unidades/supuestos y ejemplos calculados; §3/6/7/9 tienen ejemplos físicos concretos coherentes con su carácter cualitativo. §5/11 son tratamientos parciales explícitos, no capítulos agregados. Hay errores típicos/respuestas de examen, resumen mental y checklist; práctica completa y repaso separado. El índice ofrece un orden por dependencias sin duplicar estado. No corresponde exigir un simulacro ni preguntas nuevas cuando se consolidan cinco existentes.

Se comprobó particularmente: baudios≠flancos, primer cero≠espectro total, no dividir bits útiles por baudios sin declarar mapeo, eficiencia0,9 como divisor, puntosporcentuales≠aumento de tiempo, margen≠pérdida física, potencia recibida≠umbral, sensibilidad más baja admite señal más débil, dB≠dBm≠dBmV, datos de ejercicio≠estándares de medios. No hay resultado de E1–18 pendiente material de cuenta detectado. La unidad no debe volverse `revisado` mientras persistan cifras RDSI y programa excluido.

Fuera de alcance explícito (no issues): compresión, congestión/grado de servicio/dimensionamiento, hiperservicios, registros/tarificación, gestión/supervisión/mantenimiento, clasificación exhaustiva por arquitectura, catálogo U7/hardware U8. Sus ausencias están declaradas; exigir desarrollo desde bibliografía ampliaría indebidamente el pedido. Sí permanecen como pendientes para una futura unidad final del programa.

## Issues propios y pruebas de cierre

### U03-B-001 — P2 — Atribución falsa a la captura de una corrección E11

- **Naturaleza:** error demostrado de evidencia/procedencia, no error del cálculo nuevo.
- **Ubicación:** `apuntes/practica/tp-03-redes.md` `#e11`, línea240, y tabla de discrepancias línea483.
- **Claim del candidato:** R1 **y P4** suman0,4s al tiempo ideal y dan4,4s.
- **Evidencia:** R1 p.3 sí lo hace (observada ampliada); `capturas/practica/clase 04.md`, E11, líneas733–778 desarrolla η=Tideal/Ttotal, despeja Ttotal=Tideal/η y presenta4/0,9≈4,44s. P4 ya tiene el método correcto.
- **Impacto:** el estudiante aprende una historia falsa de discrepancias y no puede confiar en la trazabilidad de la corrección; “demostrada” amplifica la falsa atribución.
- **Acción:** atribuir el método incorrecto exclusivamente a R1; registrar que P4 coincide con la corrección. No modificar captura ni resultado4,44444s.
- **Prueba de cierre:** cotejo textual/visual de los dos originales y búsqueda de todas las menciones R1/P4 en E11/tabla: ninguna debe volver a afirmar que P4 suma10% al tiempo.

### U03-B-002 — P2 — El árbol compactado pierde el padre específico de las variantes LAP

- **Naturaleza:** defecto demostrado de diagrama/taxonomía; no sospecha técnica externa.
- **Ubicación:** `apuntes/teoria/03-redes-telecomunicaciones/APUNTE.md` `#protocolos`, líneas298–299: nodo único `[HDLC, LAP y LLC]` conduce a `[LAP-B, LAP-D y LAP-F]`.
- **Evidencia:** F3 p.9 dibuja HDLC, LAP y LLC como pares y las variantesB/D/F salen **sólo de LAP**. C5 árbol textual líneas20–29 y Mermaid líneas41–51 conserva esa estructura.
- **Impacto:** el lector no puede distinguir de cuál protocolo son las variantes; la compresión gráfica transforma una relación específica en descendencia de un grupo entero.
- **Acción:** separar nodos HDLC/LAP/LLC y conectar LAP únicamente conB/D/F. Conservá la precaución KERMIT; no hace falta agregar formatos ni nuevos temas.
- **Prueba de cierre:** observar Mermaid renderizado y contrastarlo con F3p.9: tres hermanos, variantes únicamente debajo de LAP; no flecha desde el grupo conjunto.

## Límites y próximos pasos

- Revisión **integral del corpus asignado U3**, no de todo el programa, otras unidades ni todas las especificaciones actuales de redes. Los contactos visuales cubrieron todas las páginas; no se ejecutó un render Markdown/Mermaid del candidato. La semántica del árbol fue contrastada desde código fuente y originales, no desde una captura renderizada del Mermaid.
- No se resolvió PRI Europa ni el punto de referencia de160kbit/s BRI: el candidato los conserva como pendientes y fuera de conocimiento evaluado. La consulta I.430 confirma sólo la cifra S/T que sí afirma.
- El encabezado/estado de E19 preexistente no fue usado como certificación ni objeto de reparación.
- Tras recibir todos los dictámenes iniciales, corregir U03-B-001/002 y repetir únicamente sus pruebas de cierre más integridad/enlaces. No promover estado por estas dos correcciones aisladas.

## Key Learnings:

1. Una cuenta correcta puede contener una discrepancia de procedencia falsa: P4 E11 ya usa4/0,9; sólo R1 suma0,4s.
2. Agrupar protocolos en un nodo Mermaid puede perder el padre de las variantes aun conservando sus nombres.
3. La exclusión explícita de Fourier/dBm hacia U2/U6 no es pérdida de contenido U3; los destinos fueron localizados.
