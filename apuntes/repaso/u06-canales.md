---
unidad: 6
estado: en-progreso
fuentes:
  - capturas/practica/Clase 05.md, Pregunta 3
  - material/teoria/U2/U 2 Características de las señales de telecom.pdf, p.5
actualizado: 2026-10-13
---

# Repaso U6 — Niveles de potencia

**Alcance:** una única pregunta existente; no es un simulacro nuevo ni cubre todo U6. La captura teórica del 08/10/2026 tiene checklist, no preguntas numeradas de autoevaluación. Las preguntas/ejercicios de ambas guías TP6 se trabajan en [práctica](../practica/tp-06-canales.md), sin duplicarlos como examen.

<a id="q-p5-3"></a>
## Q-P5-3 — Unidad dBm

**Evidencia:** [captura práctica5, 08/09/2026, Pregunta 3, líneas 97–104](../../capturas/practica/Clase%2005.md); enunciado en línea 99 y opciones en líneas 101–104. Contraste con [PDF U2 p.5](../../material/teoria/U2/U%202%20Características%20de%20las%20señales%20de%20telecom.pdf). Preguntas P5-1/2/4 corresponden a [repaso U3](u03-redes.md); esta pregunta es transversal y su fundamento vive en U6.

**Enunciado conservado:** «¿La unidad de medida dBm es para medir niveles de potencia?»

**Opciones:** Verdadero / Falso. Antes de abrir la corrección, justificá qué referencia usa, sin confundirlo con dB o dBmV.

### Datos / condiciones

Pregunta conceptual de verdadero/falso; no se proporcionan valores numéricos. Se pide clasificar dBm como unidad para medir niveles de potencia.

<details>
<summary>Corrección razonada</summary>

**Verdadero**, como indica la captura y confirma la clasificación de filmina5. El dBm expresa un nivel de potencia referido a 1 mW; no es una potencia lineal ni un cociente con referencia arbitraria.

$$
P_{dBm}=10\log_{10}\left(\frac{P}{1\,\mathrm{mW}}\right)
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $P$ | Potencia física positiva | mW |
| $P_{dBm}$ | Nivel respecto de 1 mW | dBm |

**Supuesto:** potencia positiva y referencia fija. **Ejemplos registrados:** 1 mW→0 dBm; 10 mW→10 dBm; 100 mW→20 dBm.

**Por qué no Falso:** dBm no mide tensión; para tensión referida a 1 mV se usa dBmV. Tampoco es simplemente dB: dB puede expresar una relación de potencias entre dos puntos, mientras dBm fija referencia de 1 mW.

**Errores frecuentes:** 0 dBm no significa señal nula y −10 dBm no significa potencia negativa. La explicación completa y balance están en [U6 dBm](../teoria/06-canales-comunicaciones/APUNTE.md#dbm).

</details>

## Control de evidencia

El 2026-10-11 se cotejaron el enunciado/opciones con la captura y la referencia de 1 mW con la imagen original de PDF U2 p.5. Cuentas verificadas en [QA U6](../teoria/06-canales-comunicaciones/evidencia-qa.md). Estado del paquete pendiente de revisión independiente; ninguna ambigüedad del programa se presenta como pregunta confirmada.
