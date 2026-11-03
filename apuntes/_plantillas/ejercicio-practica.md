---
unidad: 0
tipo: tp                  # tp | guia | laboratorio
numero: 0
tema: Título
estado: borrador          # borrador | en-progreso | completo | revisado
fuentes:
  - material/practica/<enunciado>.pdf
actualizado: AAAA-MM-DD
---

<!--
PLANTILLA DE EJERCICIO / TP
Criterio completo en apuntes/_plantillas/metodologia.md.

Regla: el ejercicio resuelto sirve si enseña el MÉTODO, no si muestra el resultado.
Por eso "Qué conceptos entran" va ANTES del desarrollo, y "Trampas" va después.
-->

# TP NN — Título

**Fuente del enunciado:** `material/practica/<archivo>.pdf`, pp. X–Y; si proviene de una captura, indicá archivo y línea/sección.
**Fuente del desarrollo preexistente (si aplica):** `capturas/practica/<archivo>.md`, líneas/sección …
**Teoría que lo respalda:** [Tema](../teoria/NN-unidad/archivo.md)

## Enunciado (transcripción literal)

Transcribí el enunciado completo y tal cual aparece en la fuente: consigna, subítems, tablas, opciones,
variables, cifras, signos y unidades. Se pueden normalizar los saltos de línea para que se lea; no se
parafrasea ni se corrigen en silencio errores del original. Si hay una errata o discrepancia, conservá
el texto fuente y agregá una nota pedagógica separada, con la evidencia de la aclaración.

## Datos

| Dato | Símbolo | Valor | Unidad |
|---|---|---|---|
| ... | ... | ... | ... |

Listá sólo los valores y condiciones que se extraen del enunciado; no inventes datos ni sustituyas la
consigna. Para una pregunta conceptual, indicá «No hay datos numéricos» y enumerá las premisas o
condiciones que sí da. Si no hay dato pertinente, decilo. Separá explícitamente:

**Qué se pide:** ...
**Qué NO se pide:** ... <!-- delimitar evita resolver de más -->

## Qué conceptos entran

Antes de tocar la calculadora: qué tema se está evaluando y por qué se eligió este método y no otro.

- Concepto: ...
- Por qué corresponde este método: ...
- Método alternativo descartado y motivo: ...

## Estrategia

```txt
1. Pasar S/N de dB a veces
2. Aplicar Shannon-Hartley
3. Contrastar con el límite de Nyquist
4. Quedarse con el menor de los dos
```

Primero el camino, después la cuenta. Si el camino no está claro, la cuenta no sirve.

<a id="desarrollo"></a>
## Resolución paso a paso

Si la captura ya contiene un desarrollo correcto y claro, conservá su orden, método, cuentas y
resultados: no lo reescribas desde cero. Añadí sólo las explicaciones pedagógicas necesarias para
que se entienda por qué se da cada paso. Si encontrás un error en el desarrollo original, separá y
documentá la transcripción original de la corrección; nunca cambies la fuente ni corrijas sin evidencia.

### Paso 1 — Título del paso

Justificación en una oración, después la cuenta.

$$
\text{cuenta}
$$

**Resultado parcial:** valor con unidad.

### Paso 2 — ...

## Resultado

**R:** valor con unidad.

**Verificación de razonabilidad**

- ¿La unidad cierra dimensionalmente?
- ¿El orden de magnitud tiene sentido físico?
- ¿El resultado respeta los límites teóricos (Nyquist, Shannon, capacidad del medio)?

## Trampas del ejercicio

- **Trampa:** ...
  **Por qué se cae:** ...
  **Cómo evitarla:** ...

<!-- Ej.: dar S/N en dB y aplicarlo directo en Shannon sin convertir a veces. -->

## Errores de unidad frecuentes

| Confusión | Correcto |
|---|---|
| baudio = bit/s | $V_t = V_m \cdot \log_2 n$ — sólo coinciden si $n = 2$ |
| dB de potencia vs. de tensión | $10\log_{10}$ vs. $20\log_{10}$ |

## Variantes probables en parcial

- Sólo incluir variantes justificadas por el programa/material registrado. Las hipotéticas se rotulan
  como tales, se mantienen en alcance y se resuelven con datos/supuestos explícitos: ...

## Para examen

> Cómo explicarías la resolución en voz alta, sin hacer la cuenta.
