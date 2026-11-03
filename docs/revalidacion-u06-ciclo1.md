# Cierre de autor U6 — ciclo 1

**Fecha:** 2026-10-13. **ID:** U06-B-001. **Prioridad inicial:** P3, editorial/pedagógica. **Resultado:** corregido y autocontrol aprobado; disponible para revalidación independiente. **Estado del apunte:** `en-progreso`, sin promoción ni ampliación de alcance.

## Evidencia y corrección puntual

- Informes de origen, sólo leídos: [síntesis U6 A/B](../../docs/revision-u06.md) y [dictamen B](u06-b.md).
- Ubicación: [APUNTE U6, sección de ruido](../../apuntes/teoria/06-canales-comunicaciones/APUNTE.md#ruido), §8.1, línea **524**.
- Evidencia de cátedra: [PDF U6, p.10](../../material/teoria/U6/U%206%20Canales%20de%20Comunicaciones%20y%20control%20de%20errores.pdf); [lámina PNG p.10](../../capturas/teoria/06-Canales%20de%20comunicaciones/recursos-08-10-2026/pagina-10.png), inspeccionada visualmente en este ciclo. La filmina agrupa los términos en un rótulo y explica el origen en la agitación térmica; muestra $N=kTB$ y una distribución dibujada. El original permanece intacto.
- Antes: «8.1. Térmico, blanco, gaussiano o de Johnson».
- Ahora: «8.1. Ruido de origen térmico (denominado de Johnson): modelo de cátedra blanco y gaussiano».
- Se reemplazó **únicamente esa línea**. Al invertir el reemplazo sobre los bytes posteriores, se recuperan exactamente los bytes anteriores. El desarrollo, la atribución p.10, las fórmulas, cuentas, tabla de unidades, supuestos y restantes secciones son idénticos. No se cambió `estado` ni se agregó contenido.

## Test de comprensión y criterio de cierre

**Prueba editorial, no nueva pregunta publicada de repaso:** ¿«origen, densidad espectral y distribución» son sinónimos?

**Respuesta que permiten el título nuevo y el desarrollo intacto:** **NO**. «Térmico» identifica el origen por agitación térmica; «Johnson» es denominación del ruido térmico. «Blanco» describe una densidad espectral aproximadamente plana en la banda; «gaussiano» describe la distribución de amplitudes. El modelo de cátedra combina estas propiedades; no implica que todo ruido blanco sea térmico ni gaussiano. Los cuatro fragmentos explicativos se comprobaron presentes mediante aserciones. La denominación de Johnson ya no aparece coordinada como alternativa equivalente a blanco/gaussiano.

## QA ejecutado y preservación

| Control | Resultado |
|---|---|
| Diferencia autorizada | Una sola línea de encabezado; el resto del APUNTE coincide byte a byte |
| Enlaces/anclas locales de APUNTE, INDICE, TP6 y repaso | **112 comprobados, 0 rotos**; APUNTE U5 ya presente |
| Fórmula/cuentas de §8.1 | $N=kTB$ intacta; a 300 K y 3000 Hz: $1,242\cdot10^{-17}$ W; con 6000 Hz: $2,484\cdot10^{-17}$ W; unidades/supuestos intactos |
| Retest numérico/polinomial original, sólo segmento puro | **22 controles aprobados**, incluidos Shannon/SNR, BER, dos CRC, paridad de filas/columnas y Hamming (16 palabras, distancia mínima 3, 112 inversiones simples corregidas) |
| Matemática y navegación | Delimitadores de bloque equilibrados; anclas HTML existentes sin cambios |
| Originales/caches del snapshot | **286 entradas** verificadas contra SHA-256 inicial, 0 diferencias |
| Informe inicial, snapshot, INDICE, evidencia QA, TP6, repaso y recursos propios | Hash antes/después idéntico; no se escribieron |
| Acciones prohibidas | Sin build, instalación, commit ni modificación de fuentes/capturas/caches/reportes iniciales |

La antigua evidencia QA conserva su fecha/resultados históricos: este cierre documenta el retest actual sin reescribirla. Eco, efecto pelicular y señalización telefónica siguen sin desarrollo autorizado del corpus; no se incorporan desde bibliografía. No se pretende revalidar otras unidades ni sustituir el dictamen independiente.

## Huella del candidato corregido

- SHA-256 APUNTE antes: `94f4f0360e25546a19fad18f76b1a41f537879af8b7b4a6dbaf7eef095c70e3b`.
- SHA-256 APUNTE después: `eb7a3a9d4f214e475929696dea93bd6cc884d97dfc076f15e33073d5290777cc`.
- SHA-256 PNG de evidencia p.10: `dac9b93b83783e013fbca5ef98d945b239dcea6bc8fae78e6de4da77ca08f38e`.

**Congelado al finalizar:** no se realizarán más ediciones hasta orden del coordinador. Cierre de autor, pendiente de aceptación/retest del revisor correspondiente.
