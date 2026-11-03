# U3 — Cierres de autor, ciclo 1

Fecha: 2026-10-13. Estado de unidad y TP: **en-progreso**, sin promoción. Corrección puntual sobre los dictámenes U3 A/B; no reemplaza la revalidación independiente. Entrega congelada al cerrar este ciclo.

## IDs y evidencia de cierre

| ID exacto | Corrección y ubicación | Evidencia / retest ejecutado | Resultado del autor |
|---|---|---|---|
| U03-A-001 | [TP3](../../apuntes/practica/tp-03-redes.md#e11), líneas 240 y 483: se atribuye exclusivamente a R1 p. 3 el incremento de 0,4 s; se aclara que P4 E11 ya divide por 0,9 | R1 p. 3 contrastada visualmente; P4 líneas 751–777 contiene el despeje y resultado correcto. Búsqueda de las dos atribuciones falsas previas, recálculo E11 y comparación de los 17 ejercicios restantes | Corregido; cierre propuesto |
| U03-B-001 | Mismas dos ubicaciones del TP3, sin editar P4 | Retest independiente de las definiciones y de ambos métodos: 4/0,9 = 4,444444… s; 4/4,4 = 0,909090… y no 0,9. Las dos menciones erróneas anteriores ya no aparecen en APUNTE/INDICE/TP/repaso U3 | Corregido; cierre propuesto |
| U03-A-002 | [APUNTE §5, protocolos](../../apuntes/teoria/03-redes-telecomunicaciones/APUNTE.md#protocolos), líneas 292–304: HDLC, LAP y LLC son nodos hermanos; LAP-B/D/F dependen sólo de LAP | F3 p. 9 observada visualmente y C5 líneas 44–50 cotejadas. Mermaid real renderizado: 12 nodos/11 aristas, tres aristas LAP→variantes y ninguna HDLC/LLC→variantes | Corregido; cierre propuesto |
| U03-B-002 | Mismo Mermaid, con advertencia KERMIT preservada en línea 306 | Inspección visual del PNG: etiquetas legibles, jerarquía y flechas correctas, sin agrupación de padres. Fuente renderizada idéntica al bloque del APUNTE y aristas verificadas en SVG | Corregido; cierre propuesto |

## E11: definiciones, unidades y supuestos revalidados

Se conserva el supuesto registrado de 8 bit/caracter y señalización binaria, por lo que 3600 baudios equivalen aquí a 3600 bit/s; no se universaliza esa igualdad. Rendimiento adimensional $\eta=N_{datos}/N_{total}=0,90$. Sin otras pausas o retransmisiones, $T=N_{total}/V_t=T_{ideal}/\eta$.

- $N_{datos}=1800\times8=14400$ bit; $N_{total}=14400/0,9=16000$ bit.
- $T_{ideal}=14400/3600=4$ s; $T_{total}=16000/3600=4,444444\ldots$ s, redondeado **4,44 s**.
- Incremento: $4/9=0,444444\ldots$ s. Control: $14400/T_{total}=3240$ bit/s, el 90% de 3600 bit/s.
- R1 p. 3 agrega 0,4 s y obtiene 4,4 s: su rendimiento implícito sería **90,909090…%**. P4 E11 no comete ese error: ya usa la división por 0,9.

## Render y QA del ciclo

- [Fuente Mermaid exacta](../autor-u03/ciclo1/protocolos-ciclo1.mmd), [SVG](../autor-u03/ciclo1/protocolos-ciclo1.svg), [PNG inspeccionado](../autor-u03/ciclo1/protocolos-ciclo1.png), [nodos/aristas extraídos](../autor-u03/ciclo1/render-qa.json). Mermaid v11 CDN + Playwright/Chrome headless; sin instalación ni build. Edge falló y la carga CDN sandboxada falló; ejecución puntual autorizada fuera del sandbox completó el render. No se incorporó contenido académico externo.
- PNG SHA-256: `c6ee14e11fea96b2159ca97480b1e4dd0e8dc82e0106e82879571fbd8c2fa236`.
- [QA numérico y enlaces](../autor-u03/ciclo1/qa-ciclo1.json): **31 aserciones numéricas reejecutadas**, **90/90 enlaces locales y anclas válidos**, **17/17 imágenes y originales coinciden con el manifiesto**. Además, aserciones específicas E11 y aristas Mermaid en [retest](../autor-u03/ciclo1/retest.py).
- [Preservación](../autor-u03/ciclo1/preservacion-ciclo1.json): **33/33 hashes del baseline iguales**; incluye capturas P4/C5, F3/R1 originales, cinco caches U3, 17 PNG, repaso, INDICE, E19 preexistente, informes A/B, revisión U3 y snapshot inicial.
- Otros **17 ejercicios E1–10/E12–18**, cuatro ejemplos A–D y bloque de enlace E19 iguales antes/después. Repaso intacto con sus cinco IDs: U3-TQ1/TQ3/PQ1/PQ2/PQ4. No se edita ni se recertifica E19.
- [Diff completo](../autor-u03/ciclo1/diff-ciclo1.txt): únicamente dos atribuciones TP, jerarquía Mermaid y fechas YAML de ambos archivos. No cambio de estado, anclas, alcance, imágenes ni preguntas. El QA histórico de autor permanece intacto; este registro distingue el retest actual.

## Límite y siguiente paso

Los cuatro IDs conservan identidad individual aunque converjan en dos correcciones. Pendientes anteriores de la unidad siguen vigentes. Corresponde al coordinador/revisores decidir el cierre independiente; el autor no declara U3 revisada. Sin commits, instalaciones ni builds; U3 congelada hasta nueva orden.
