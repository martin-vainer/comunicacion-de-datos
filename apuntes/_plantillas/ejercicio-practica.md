---
unidad: 0
tipo: tp                  # tp | guia | laboratorio
numero: 0
tema: Título
estado: borrador          # borrador | en-progreso | completo | revisado
fuentes:
  - material/practica/<enunciado>.pdf
  - material/_cache/<enunciado>.txt
actualizado: AAAA-MM-DD
---

<!--
PLANTILLA DE EJERCICIO / TP
Criterio completo en apuntes/_plantillas/metodologia.md.

Regla: el ejercicio resuelto sirve si enseña el MÉTODO, no si muestra el resultado.
Por eso "Qué conceptos entran" va ANTES del desarrollo, y "Trampas" va después.
-->

# TP NN — Título

**Fuente del enunciado:** `material/practica/<archivo>.pdf`
**Teoría que lo respalda:** [Tema](../teoria/NN-unidad/archivo.md)

## Enunciado

Transcripción o resumen fiel. No reformular de manera que cambie lo pedido.

## Datos

| Dato | Símbolo | Valor | Unidad |
|---|---|---|---|
| Ancho de banda | $B$ | | Hz |

**Qué se pide:** ...
**Qué NO se pide:** ...   <!-- delimitar evita resolver de más -->

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

## Desarrollo

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

- Si en vez de pedir $C$ piden $B$, se despeja: ...
- Si agregan ruido impulsivo, cambia porque: ...

## Para examen

> Cómo explicarías la resolución en voz alta, sin hacer la cuenta.
