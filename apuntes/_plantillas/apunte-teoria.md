---
unidad: 1                # Reemplazar por el número de unidad (U1–U8)
estado: borrador          # borrador | en-progreso | completo | revisado
fuentes:
  - material/teoria/<archivo>.pdf, pp. X-Y
  - Forouzan (2021), cap. N
actualizado: AAAA-MM-DD
---

<!--
PLANTILLA DE APUNTE TEÓRICO CANÓNICO DE UNIDAD
Para U1–U8: un único APUNTE.md por carpeta de unidad. Los temas son secciones enlazables.
Criterio completo en apuntes/_plantillas/metodologia.md — leerlo antes de la primera vez.
El front matter se aplica a toda la unidad: no agregues un campo tema.
Aplicar fidelidad docente y formato de metodología §§3.1–3.2, datos críticos §4.1 y revisión diferenciada §6.2.
Los párrafos e ítems de ejemplo van en una línea lógica; no aplanar tablas, código, Mermaid ni fórmulas.

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

Dos o tres oraciones conectando con lo anterior y anticipando lo que viene. Sirve para que el tema no quede como un compartimento aislado.

**Requisitos previos**

- [Tema previo](../NN-unidad/APUNTE.md#seccion) — qué hay que tener claro antes de entrar acá.

**Alcance y cobertura**

<!-- Comparar con el programa. Incluir temas faltantes; no confundir lo visto en clase con la unidad
completa. Ninguna exclusión se oculta. "Final" exige la puerta de calidad de metodología §6.1. -->

| Tema del programa | Términos y siglas docentes | Sección | Captura/material y página o sección | Cobertura / pendiente |
|---|---|---|---|---|
| ... | Nombre usado en clase / sigla y equivalencia | [Tema](#tema-principal) | ... | ... |

<!-- Mantener reconocibles las agrupaciones del profesor y su notación. Ej.: «Características de interés» y «uplink — enlace ascendente». No incorporar nuevos temas para llenar esta matriz. -->

---

<a id="tema-principal"></a>
## 1) Tema o sección principal

**Fuentes de esta sección:** `material/teoria/<archivo>.pdf`, pp. X–Y; ...

**Procedencia de clase (si existe):** `capturas/...`, fecha y sección; no modificar el original.

### Concepto central: nombre

#### Problema físico

Qué situación física o de ingeniería aparece ANTES del concepto. Sin esto el concepto se memoriza en lugar de entenderse.

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

Cuándo la fórmula deja de aplicar. Ej.: Nyquist supone canal SIN ruido; Shannon supone ruido blanco gaussiano aditivo. Aplicarlas fuera de su supuesto es error de concepto, no de cuenta.

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

Dónde aparece esto fuera del pizarrón: una norma, una tecnología, un valor de catálogo. Si no aporta a la comprensión o no hay una fuente verificable, omitilo.

- Norma / recomendación: ...
- Tecnología o equipo: ...
- Valores típicos reales: ...

<!-- Este bloque es el ancla a la realidad. Un número real vale más que tres párrafos. -->

#### Errores típicos

- **Error:** ... **Por qué está mal:** razonamiento técnico, no "porque sí". **Lo correcto:** ...

#### Para examen

> Respuesta oral compacta, de dos o tres oraciones. Como si te lo preguntaran en el final y tuvieras que contestar sin pizarrón.

---

### Concepto secundario: nombre

Definición + ejemplo + relación con la unidad. Sin los ocho bloques. Si aparece una fórmula, aplican igualmente la tabla de símbolos con unidades, sus supuestos y un ejemplo numérico calculado.

<a id="tema-siguiente"></a>
## 2) Siguiente tema o sección

Repetí la estructura que corresponda al tema: conceptos centrales con sus bloques y secundarios con definición + ejemplo + relación. Usá un identificador HTML estable y breve para que `INDICE.md` pueda enlazar esta sección.

## N) Gotchas del material

Discrepancias importantes y verificables. No se promedian ni se corrigen en silencio. Las diferencias de redondeo o notación que no alteran el significado no se convierten en erratas.

1. **Qué dice A vs. qué dice B**
   - Cátedra: ...
   - Bibliografía / norma: ...
   - Evidencia de contraste y localizador: ...
   - Cuál se toma en este apunte y por qué: ...
   - Fuente: `material/...`, p. X
   - Si la evidencia no alcanza: pendiente y próxima comprobación ...

---

## N+1) Pendientes por sección

Registrá cada comprobación que falte en la sección afectada. Si no hay pendientes, escribí `Ninguno`. Un pendiente material impide marcar la unidad como `revisado`.

| Sección | Qué falta verificar | Fuente o próxima acción |
|---|---|---|
| [Tema](#tema-principal) | ... | ... |

<a id="registro-revision"></a>
## N+2) Registro de revisión

| Fecha | Tipo de control | Alcance y evidencia/localizadores | Método y resultado | Limitaciones / pendientes |
|---|---|---|---|---|
| AAAA-MM-DD | Estructural | Archivos y secciones: ... | No realizado; completar con comprobación efectuada | ... |
| AAAA-MM-DD | Recálculo | Entradas, unidades y cuentas: ... | No realizado; completar con procedimiento y resultado | ... |
| AAAA-MM-DD | Contraste técnico | Original, secciones, tablas/figuras y condiciones: ... | No realizado; completar con comparación y resultado | ... |

**Evidencia de datos críticos**

| Dato / sección | Fuente y localizador | Valor, unidad y condición de la fuente | Contraste y resultado |
|---|---|---|---|
| Atenuación máxima monomodo a 1550 nm | `material/teoria/U7/Folleto FO.jpg`, tabla Performance Data, fila Single-Mode / Maximum, columna 1550 nm | 0,4 dB/km; máximo, 1550 nm | Ejemplo: si el candidato dice 0,5 dB/km, registrar discrepancia de transcripción; un recálculo correcto con 0,5 no la resuelve |

<!-- La fila numérica es un ejemplo de cómo registrar un hallazgo, no una comprobación nueva ejecutada al copiar la plantilla. Sustituir por evidencia de los datos críticos reales de la unidad; no atribuir fuentes a supuestos didácticos. -->

<!-- Registrar sólo controles realmente ejecutados; si no aplica, justificar. Los resultados estructurales o aritméticos no certifican los datos ni las explicaciones. Revisión parcial no permite "revisado". Ver metodología §§6.1–6.2. -->

## N+3) Práctica y repaso

Los ejercicios resueltos y las preguntas de autoevaluación no van dentro de este apunte. Enlazá aquí los recursos separados cuando existan:

- [Práctica de la unidad](../../practica/INDICE.md)
- [Repaso de la unidad](../../repaso/INDICE.md)

## N+4) Relación con otras unidades

- [Tema relacionado](../NN-unidad/APUNTE.md#seccion) — en qué se apoya o qué habilita.

## N+5) Resumen mental

Si te preguntan **"¿qué organiza esta unidad y cómo se conectan sus temas?"**, contestá:

> Discurso oral compacto que integra la unidad. Cuatro o cinco oraciones máximo.

**Checklist para examen**

- concepto clave 1;
- concepto clave 2;
- fórmula y su supuesto;
- error típico;
- caso real / valor concreto cuando corresponda.

<!-- Las preguntas de autoevaluación y flashcards van en apuntes/repaso/, no acá. -->
