---
unidad: 1                # Reemplazar por el número de unidad (U1–U4)
estado: borrador          # borrador | en-progreso | completo | revisado
fuentes:
  - material/teoria/<archivo>.pdf, pp. X-Y
  - Forouzan (2021), cap. N
actualizado: AAAA-MM-DD
---

<!--
PLANTILLA DE APUNTE TEÓRICO CANÓNICO DE UNIDAD
Para U1–U4: un único APUNTE.md por carpeta de unidad. Los temas son secciones enlazables.
Criterio completo en apuntes/_plantillas/metodologia.md — leerlo antes de la primera vez.
El front matter se aplica a toda la unidad: no agregues un campo tema.

Regla del apunte:
  problema físico -> concepto -> modelo mental -> formalización -> ejemplo numérico
  -> caso real -> errores típicos -> respuesta de examen

Los conceptos CENTRALES usan los ocho bloques.
Los conceptos SECUNDARIOS se resuelven con: definición + ejemplo + relación con la unidad.
Forzar los ocho bloques en todo genera relleno, y el relleno no se estudia.
-->

# Unidad N — Nombre de la unidad

**Fuentes generales del apunte**

- Material de cátedra: `material/teoria/<archivo>.pdf`
- Bibliografía: ...
- Normas / recomendaciones: UIT-T X.NN, IEEE 802.N

<!-- El cache textual es un derivado de trabajo: no se registra como fuente independiente. -->

**Idea central de la unidad**

> Una sola oración. Qué capacidad conceptual reúne la unidad y por qué importa.

**Por qué importa**

Dos o tres oraciones conectando con lo anterior y anticipando lo que viene. Sirve para que el tema no
quede como un compartimento aislado.

**Requisitos previos**

- [Tema previo](../NN-unidad/APUNTE.md#seccion) — qué hay que tener claro antes de entrar acá.

---

<a id="tema-principal"></a>
## 1) Tema o sección principal

**Fuentes de esta sección:** `material/teoria/<archivo>.pdf`, pp. X–Y; ...

### Concepto central: nombre

#### Problema físico

Qué situación física o de ingeniería aparece ANTES del concepto. Sin esto el concepto se memoriza en
lugar de entenderse.

#### Concepto

Definición clara y breve. Nada colgado: si aparece una sigla o una norma, se dice qué es acá mismo.

#### Modelo mental

Analogía, cadena de señal o diagrama. Una imagen mental que se pueda recordar.

```txt
fuente -> codificador -> modulador -> canal -> demodulador -> decodificador -> destino
```

```mermaid
graph LR
  F[Fuente] --> C[Codificador] --> M[Modulador]
  M --> CH[(Canal + ruido)]
  CH --> D[Demodulador] --> DC[Decodificador] --> DS[Destino]
```

<!-- Diagrama sólo si aporta. Si es decorativo, no va. -->

#### Formalización

$$
\text{fórmula}
$$

| Símbolo | Significado | Unidad |
|---|---|---|
| $B$ | Ancho de banda | Hz |
| $C$ | Capacidad del canal | bit/s |

**Supuestos y límites de validez**

Cuándo la fórmula deja de aplicar. Ej.: Nyquist supone canal SIN ruido; Shannon supone ruido blanco
gaussiano aditivo. Aplicarlas fuera de su supuesto es error de concepto, no de cuenta.

#### Ejemplo numérico

Enunciado corto, desarrollo paso a paso, resultado **con unidad**.

No alcanza con dejar planteada la fórmula: hay que mostrar el número que sale.

```txt
Datos:    B = 3100 Hz, S/N = 30 dB
Paso 1:   S/N (veces) = 10^(30/10) = 1000
Paso 2:   C = 3100 · log2(1 + 1000) ≈ 3100 · 9,97
Resultado: C ≈ 30,9 kbit/s
```

**Verificación de razonabilidad:** ¿el orden de magnitud cierra? ¿la unidad cierra?

#### Caso real (cuando aporte)

Dónde aparece esto fuera del pizarrón: una norma, una tecnología, un valor de catálogo. Si no aporta a
la comprensión o no hay una fuente verificable, omitilo.

- Norma / recomendación: ...
- Tecnología o equipo: ...
- Valores típicos reales: ...

<!-- Este bloque es el ancla a la realidad. Un número real vale más que tres párrafos. -->

#### Errores típicos

- **Error:** ...
  **Por qué está mal:** razonamiento técnico, no "porque sí".
  **Lo correcto:** ...

#### Para examen

> Respuesta oral compacta, de dos o tres oraciones. Como si te lo preguntaran en el final y tuvieras
> que contestar sin pizarrón.

---

### Concepto secundario: nombre

Definición + ejemplo + relación con la unidad. Sin los ocho bloques.
Si aparece una fórmula, aplican igualmente la tabla de símbolos con unidades, sus supuestos y un ejemplo
numérico calculado.

<a id="tema-siguiente"></a>
## 2) Siguiente tema o sección

Repetí la estructura que corresponda al tema: conceptos centrales con sus bloques y secundarios con
definición + ejemplo + relación. Usá un identificador HTML estable y breve para que `INDICE.md`
pueda enlazar esta sección.

## N) Gotchas del material

Contradicciones concretas y verificables. No se promedian, se registran.

1. **Qué dice A vs. qué dice B**
   - Cátedra: ...
   - Bibliografía / norma: ...
   - Cuál se toma en este apunte y por qué: ...
   - Fuente: `material/...`, p. X

---

## N+1) Pendientes por sección

Registrá cada comprobación que falte en la sección afectada. Si no hay pendientes, escribí `Ninguno`.
Un pendiente material impide marcar la unidad como `revisado`.

| Sección | Qué falta verificar | Fuente o próxima acción |
|---|---|---|
| [Tema](#tema-principal) | ... | ... |

## N+2) Práctica y repaso

Los ejercicios resueltos y las preguntas de autoevaluación no van dentro de este apunte. Enlazá aquí
los recursos separados cuando existan:

- [Práctica de la unidad](../../practica/INDICE.md)
- [Repaso de la unidad](../../repaso/INDICE.md)

## N+3) Relación con otras unidades

- [Tema relacionado](../NN-unidad/APUNTE.md#seccion) — en qué se apoya o qué habilita.

## N+4) Resumen mental

Si te preguntan **"¿qué organiza esta unidad y cómo se conectan sus temas?"**, contestá:

> Discurso oral compacto que integra la unidad. Cuatro o cinco oraciones máximo.

**Checklist para examen**

- concepto clave 1;
- concepto clave 2;
- fórmula y su supuesto;
- error típico;
- caso real / valor concreto cuando corresponda.

<!-- Las preguntas de autoevaluación y flashcards van en apuntes/repaso/, no acá. -->
