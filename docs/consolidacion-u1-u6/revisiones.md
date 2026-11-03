# Registro de revisiones independientes

## Versión inicial

- Manifiesto: [snapshot-inicial.json](snapshot-inicial.json).
- SHA-256 del manifiesto: `1e29fd3bf30b9d99d07e0d3b73e2d7ef11f9d85bb7874b2630650412068a7bdd`.
- Control de congelamiento: 259 originales intactos; 774 enlaces locales sin faltantes.
- `git diff --check` global señaló dos líneas vacías finales en stubs U2. No se corrigen durante esta ronda; advertencias LF/CRLF no prueban cambios de bytes actuales.
- Los candidatos y sus evidencias quedan sin modificaciones hasta reunir los trece dictámenes iniciales.
- Reanudación 2026-10-13 tras límite de uso: snapshot sin diferencias ni agregados, 259 originales intactos, 774 enlaces válidos. U1-A/U1-B/U2-A retomados; sus interrupciones no cuentan como dictámenes.
- A: revisión académica integral. B: revisión pedagógica integral, también contrastada con originales. C: revisión transversal.

## Dictámenes iniciales

| Dictamen | Agente independiente | Estado | Informe |
|---|---|---|---|
| U1-A | review_u01_a | Recibido: requiere cambios, límites de contraste declarados | tmp/reviews/u01-a.md |
| U1-B | review_u01_b | Recibido: requiere cambios, límites de contraste declarados | tmp/reviews/u01-b.md |
| U2-A | review_u02_a | Recibido: ajustes menores; DOC legacy sin contraste visual | tmp/reviews/u02-a.md |
| U2-B | review_u02_b | Recibido: requiere correcciones; límites U2 declarados | tmp/reviews/u02-b.md |
| U3-A | review_u03_a | Recibido: requiere cambios | tmp/reviews/u03-a.md |
| U3-B | review_u03_b | Recibido: observaciones; coincide en dos hallazgos P2 | tmp/reviews/u03-b.md |
| U4-A | review_u04_a | Recibido: requiere corrección puntual; P1/P2/P3 | tmp/reviews/u04-a.md |
| U4-B | review_u04_b | Recibido: un hallazgo P2 | tmp/reviews/u04-b.md |
| U5-A | review_u05_a | Recibido: P2 de trazabilidad de pendientes; sin P1 | tmp/reviews/u05-a.md |
| U5-B | review_u05_b | Recibido: falta cobertura ITA2; detalles editoriales | tmp/reviews/u05-b.md |
| U6-A | review_u06_a | Recibido: sin issues demostrados P0–P3 | tmp/reviews/u06-a.md |
| U6-B | review_u06_b | Recibido: una observación editorial P3; mantener en-progreso | tmp/reviews/u06-b.md |
| Global-C | review_global_c | Recibido: sin hallazgos transversales demostrados | tmp/reviews/global-c.md |

Los informes completos se preservan en `tmp/reviews/` y como copias locales en `docs/revision-uNN.md`/`docs/revision-transversal-u1-u6.md`. La síntesis accionable es [síntesis inicial](sintesis-inicial.md). Las sospechas no se convirtieron en errores demostrados por consenso ni los límites de cobertura en aprobaciones.

## Correcciones y cierre

## Revalidación ciclo 1

- Nueva identidad: [snapshot ciclo 1](snapshot-ciclo1.json), 401 rutas.
- Todos los IDs de la matriz se revalidaron PASS focalmente por revisores A/B de las seis unidades. U05-B entregó una errata de integridad: su primera cuenta correspondía al snapshot inicial; ver `tmp/reviews/revalidacion-u05-b-ciclo1-errata.md`. El checker raíz confirma snapshot ciclo 1 sin diferencias ni agregados.
- Global-C ciclo 1 confirmó 259 originales y 805 enlaces intactos. Emitió C-C1-001 (P2) por estado operativo obsoleto; **cerrado** al sincronizar la tabla de seguimiento de `estado.md`, conservando ambos snapshots y el historial inicial.
- La comprobación independiente confirmó C-C1-001 cerrado (`tmp/reviews/cierre-C-C1-001.md`).
- Resumen de cierre por unidad: [U1](../verificacion-ciclo1-u01.md), [U2](../verificacion-ciclo1-u02.md), [U3](../verificacion-ciclo1-u03.md), [U4](../verificacion-ciclo1-u04.md), [U5](../verificacion-ciclo1-u05.md), [U6](../verificacion-ciclo1-u06.md). Verificación global: [ciclo 1](../verificacion-transversal-ciclo1.md). Informes focales originales preservados en `tmp/reviews/`.
- **Resultado revalidación:** 12 revisiones unitarias focales A/B y el control global ciclo 1 recibidos; los cierres individuales reportan PASS para los issues iniciales. El informe U2-B se corrigió con errata: el conteo 388/401 correspondía a comparar contra el snapshot inicial; el snapshot correcto de ciclo 1 verifica 401/401 hashes y cero agregados.
- Las seis unidades siguen `en-progreso`: esta revalidación comprueba cambios, no certifica por sí misma cobertura íntegra del programa ni el estatus `revisado/final`.
- Ciclo 2 automático: no iniciado; no hay hallazgos iniciales abiertos. Los pendientes de fuente/cobertura permanecen expresamente abiertos, no son defectos aprobados. No se lanza ciclo automático sólo para elevar el estado.
