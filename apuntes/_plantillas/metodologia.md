# Metodología de apuntes — Comunicación de Datos

Este documento define **cómo se escribe un apunte en este repo**. Es la autoridad: las plantillas son
la forma, esto es el criterio. Si una plantilla y este documento se contradicen, manda este documento.

Está derivado del análisis de los apuntes de **Desarrollo de Software (1C2026)**
(`../../DDS/Apuntes_Desarrollo_de_Software.md`, 9.500 líneas, y su `docs/metodologia-apuntes.md`),
un sistema de apuntes que ya funcionó en una cursada real con agentes de IA. Acá está lo que se
rescató, lo que se adaptó y lo que se descartó.

---

## 1. Qué se rescató de DDS (y por qué funciona)

### 1.1 La regla del apunte

DDS abre con una sola línea que gobierna todo:

> `concepto -> ejemplo mínimo -> ejemplo real (repo) -> errores típicos`

Funciona porque impone un **orden de comprensión**: nunca se define algo antes de mostrar qué problema
resuelve, y nunca se cierra un tema sin decir dónde se lo confunde.

**Nuestra versión** (adaptada a una materia cuantitativa y física):

> `problema físico -> concepto -> modelo mental -> formalización (fórmula, unidades y supuestos) -> ejemplo numérico -> caso real cuando aporte -> errores típicos -> respuesta de examen`

### 1.2 Anatomía del concepto central

DDS estandarizó siete bloques por concepto: Problema, Concepto, Modelo mental, Ejemplo mínimo, Ejemplo
real del repo, Error típico, Para examen. La consistencia es lo que hace el apunte navegable a los tres
meses, cuando no te acordás de nada.

Para los conceptos centrales se adopta esta secuencia, con los cambios de vocabulario de §2. No es una
lista de subtítulos obligatorios para cada concepto secundario: esos se resuelven con definición, ejemplo
y relación con la unidad (ver §1.9).

### 1.3 "Para examen" y "Resumen mental"

El hallazgo más valioso de DDS. Cada concepto cierra con una respuesta **oral, compacta, de dos o tres
oraciones**, y cada clase cierra con un "Resumen mental" + checklist.

> *El resumen mental es obligatorio porque transforma el apunte en discurso de examen.*
> — `docs/metodologia-apuntes.md` de DDS

Esto es lo que separa un apunte de un resumen. Un resumen te deja entender; el resumen mental te deja
**contestar**. En una materia con final oral, es la sección que más rinde.

### 1.4 Gotchas concretos y verificables

DDS registra las contradicciones en vez de taparlas, con path o link. Ejemplo real del apunte:

> *"`ProductoService.eliminar` hace soft delete; `ProductoRepository.eliminar` hace hard delete. No
> rompe, pero hay una decisión de diseño mezclada."*

La regla: **si el material de cátedra dice una cosa y la bibliografía otra, se registra, no se
promedia**. En Comunicación de Datos esto va a pasar seguido —notación de dB, definiciones de baudio,
qué se considera "capa física"— y hay que dejarlo visible.

### 1.5 Jerarquía de fuentes explícita

DDS numeró la prioridad de fuentes y la respetó. Sin eso, el agente mezcla el PDF de cátedra con lo que
sabe de memoria y no se distingue qué entra en el parcial.

### 1.6 Cache textual de los PDFs

DDS mantiene `_cache_pdf_text/` con la transcripción de cada PDF. Regla dura: **no se redacta el apunte
de una sección si su PDF no tiene cache textual**. Es lo que permite buscar, citar y contrastar sin releer
binarios.

### 1.7 Índice de lectura al frente

DDS abre con una tabla "Bitácora / Índice de lectura": clase, tema central, fuente, en qué anclar. Es lo
que hace usable un documento de 9.500 líneas. En U1–U4 se porta como `INDICE.md` breve por unidad:
enlaza secciones del `APUNTE.md` y el orden de lectura, sin repetir su desarrollo ni duplicar su estado.

### 1.8 Orden por dependencia conceptual, no por orden del PDF

> *Si un tema necesita otro para entenderse, va después aunque el PDF lo muestre antes.*

En esta materia importa el doble: el programa analítico presenta Fourier en la Unidad 2 y Shannon en la
Unidad 6, pero no se puede entender capacidad de canal sin ancho de banda. El apunte respeta la
dependencia, y enlaza hacia atrás.

### 1.9 Plantilla flexible

> *No todos los conceptos necesitan todos los subtítulos. Los conceptos centrales sí; los secundarios
> pueden ser más breves.*

Un concepto secundario se resuelve con definición + ejemplo + relación con la unidad. Forzar los ocho
bloques en todo genera relleno, y el relleno no se estudia.

---

## 2. Qué se adaptó (DDS es de código, esta materia no)

| En DDS | Acá | Por qué |
|---|---|---|
| `Ejemplo real del repo` (archivo/rama/fragmento) | `Caso real` (norma UIT-T/IEEE, tecnología concreta, valor de catálogo) | No hay repo. El anclaje a la realidad es el estándar y el número medido: RS-232 con sus ±12 V, E1 a 2,048 Mbit/s, UTP Cat 6 a 250 MHz. |
| `Ejemplo mínimo` de código | `Formalización` + `Ejemplo numérico` | La materia es cuantitativa. El equivalente pedagógico de "correr el código" es **hacer la cuenta y verificar la unidad**. |
| `Gotchas reales del repo` | `Gotchas del material` | Contradicciones entre filminas, bibliografía y normas. |
| Lectura `request -> controller -> service` | Bloque `Modelo mental` con cadena de señal o diagrama Mermaid | El flujo acá es físico: `fuente -> codificador -> modulador -> canal -> demodulador -> decodificador -> destino`. |
| Un único archivo gigante | Para U1–U4, un `APUNTE.md` teórico canónico por unidad, con los temas organizados en secciones; `INDICE.md` queda como navegación breve. Práctica y repaso van aparte. | Mantiene una sola fuente teórica por unidad y evita duplicar contenido o estados entre archivos temáticos. Los enlaces del índice apuntan a las secciones del apunte. |

### 2.1 Lo que se agrega, propio de esta materia

- **Tabla de símbolos obligatoria** debajo de cada fórmula: símbolo, significado, **unidad**. En una
  materia donde se mezclan Hz, bit/s, baudios, dB, dBm y Erlang, omitir la unidad es el error más caro.
- **Supuestos y límites de validez** de cada fórmula. Nyquist supone canal sin ruido; Shannon supone
  ruido blanco gaussiano. Aplicar la fórmula fuera de su supuesto es error de examen, no de cuenta.
- **Verificación de razonabilidad** en cada ejercicio: ¿el orden de magnitud cierra?, ¿la unidad cierra?
  Detecta el 90 % de los errores de cuenta sin rehacerla.

---

## 3. Reglas de redacción

Estas seis reglas salen de `mejoras_generales.md` de DDS — la lista de correcciones que el propio
estudiante le hizo al apunte después de estudiarlo. Son las fallas reales, detectadas usando el apunte,
no en teoría:

1. **Nada colgado.** Si aparece una herramienta, norma o sigla, se dice qué es antes de usarla.
   *(Origen: "en la sección Jest: instalación y scripts explicar brevemente qué es Jest, si no queda
   súper colgado".)*
2. **Mostrar la salida, no sólo el procedimiento.** No alcanza con la fórmula: hay que mostrar el
   resultado, el valor, la forma de onda, la trama resultante.
   *(Origen: "da ejemplos de la salida, no solo de código".)*
3. **Ejemplos completos, no enlaces.** Si el concepto tiene varias piezas, se muestran todas. No se
   remite a otra sección para completar la idea.
   *(Origen: "no solo pongas el link a los ejemplos de las capas, agregá un ejemplo mínimo de cada una".)*
4. **Escribir para quien no sabe nada.** El lector objetivo es vos dentro de tres meses, sin contexto.
   Si un resumen queda tan comprimido que necesita conocimiento previo para entenderse, está mal.
   *(Origen: "si alguien que no entiende nada de la materia lo ve, le va a faltar contexto".)*
5. **Sin irse por las ramas.** Mejorar la explicación de lo que dio la cátedra ≠ agregar temas nuevos.
   El alcance lo fija el programa analítico.
   *(Origen: "no quiero que se vaya por las ramas, quiero que se respete el contenido ya dado".)*
6. **Un ejemplo por cada distinción.** Si el apunte distingue tres cosas (baudio vs. bit/s vs. Hz;
   FDM vs. TDM vs. STDM), van tres ejemplos. Una tabla comparativa sin ejemplos no fija nada.
   *(Origen: "tratemos de dar un ejemplo de cada uno, para que quede más claro".)*

---

## 4. Alcance, autoridad y fuentes

Son decisiones distintas y NO se mezclan:

- El **programa analítico** (`material/catedra/`) define qué entra en la materia y su vocabulario.
- El **documento original** es la autoridad para lo que afirma: PDF, filmina, guía o enunciado dentro
  de `material/`.
- `material/_cache/` es una transcripción derivada para buscar y redactar. Facilita el acceso, pero no
  es una fuente independiente ni reemplaza el original ante dudas de fórmulas, figuras o notación.

Dentro del alcance del programa, se priorizan las fuentes así:

1. Material oficial de cátedra (`material/teoria/`, `material/practica/`).
2. Bibliografía **obligatoria**: Forouzan, Castro Lechtaler & Fusario, Liberatori, Ibe, Stallings.
3. Normas y recomendaciones citadas por la cátedra (UIT-T, IEEE, EIA/TIA).
4. Bibliografía complementaria (Tanenbaum, Abramson, Tomasi, Couch, Stremler…).
5. Conocimiento general del agente — **sólo como apoyo y siempre señalado como tal**.

Regla dura: **el nivel 5 nunca contradice al 1 en silencio.** Si el conocimiento general del agente
difiere del material de cátedra, se escribe lo de cátedra y se registra la diferencia como gotcha.

---

## 5. Workflow para un tema nuevo

```txt
1. Identificar las fuentes de cada tema en material/teoria/ o material/practica/
2. Buscar su transcripción en material/_cache/
3. Si no existe, generarla (ver abajo)
4. Usar la transcripción para buscar y redactar; contrastar el resultado con el PDF, que es la
   autoridad para texto, diagramas y notación
5. Para U1–U4, integrar la teoría en la sección correspondiente del `APUNTE.md` canónico de la unidad;
   conservar ejercicios resueltos en `apuntes/practica/` y actividades de evaluación/repaso en
   `apuntes/repaso/`. No modificar las capturas originales.
6. Actualizar el `INDICE.md` breve con enlaces a las secciones del apunte y a la práctica/repaso
   pertinentes. Registrar los pendientes de contraste junto a la sección afectada, no como estado
   independiente de un tema.
```

Generar cache textual (`pdftotext` está disponible en este entorno, en `/mingw64/bin`):

```bash
pdftotext -layout -enc UTF-8 "material/teoria/<archivo>.pdf" "material/_cache/<nombre>.txt"
```

Notas de entorno:

- El lector de PDF nativo del agente **no funciona acá**: falta `pdftoppm`. Usar `pdftotext`.
- Alternativa si `pdftotext` falla: `python -c` con `pypdf`, escribiendo a archivo con
  `encoding='utf-8'`. Imprimir a stdout revienta con `UnicodeEncodeError` por la consola cp1252.
- No hay `bat`, `fd`, `eza`. Sí hay `rg`.

> **No consolidar una sección del apunte si su PDF todavía no tiene cache textual**, salvo pedido
> explícito.

---

## 6. Estado del apunte canónico de unidad

En U1–U4 hay un solo `APUNTE.md` teórico por unidad. Su front matter lleva `unidad`, `estado`,
`fuentes` y `actualizado`; no lleva `tema`, porque el documento reúne varios temas. Las fuentes se
citan también en las secciones donde se usan. El `estado` se aplica a toda la unidad, no a un tema ni a
una sección:

| Estado | Significa |
|---|---|
| `borrador` | Existe el esqueleto o hay notas sueltas en varias secciones. No se estudia de acá. |
| `en-progreso` | Una o más secciones están en elaboración o tienen ejemplos, cálculos o contrastes pendientes. |
| `completo` | El alcance declarado de la unidad está desarrollado con la metodología: conceptos centrales con su secuencia, fórmulas contextualizadas y ejemplos calculados; los secundarios conservan el tratamiento breve que les corresponde. Aún puede faltar la revisión integral de fuentes. |
| `revisado` | **Toda la unidad** fue contrastada con el programa y las fuentes originales pertinentes; se verificaron afirmaciones, diagramas, fórmulas, unidades, supuestos y cálculos. No quedan pendientes materiales de contraste. Es material de estudio confiable. |

No marques `revisado` porque una sección aislada ya fue verificada. Si la revisión es parcial, registrá
su alcance y los pendientes en una sección `Pendientes por sección` dentro de `APUNTE.md` o junto a la
sección afectada. Cada pendiente debe nombrar la sección, qué evidencia falta y cuál es la próxima
comprobación. Mientras quede un pendiente de contraste en cualquier sección, el estado de la unidad no
puede ser `revisado`.

Las capturas rápidas no llevan este estado ni front matter obligatorio: son registro de clase, no
material consolidado. Su trazabilidad vive en la bitácora hasta que se integran como secciones del
apunte canónico.

---

## 7. Lo que NO se hace

- No transcribir la filmina. El apunte **reconstruye**, no copia.
- No pegar una fórmula sin tabla de símbolos, unidades y supuestos.
- No inventar valores, normas ni números de recomendación UIT-T. Si no está en el material y no se sabe
  con certeza, se escribe `<!-- PENDIENTE: verificar en material -->` y se avisa.
- No tapar contradicciones entre cátedra y bibliografía.
- No mezclar unidades del programa en un mismo `APUNTE.md`.
- No editar nada dentro de `material/`.
- No meter cuestionarios ni flashcards dentro del apunte principal. El apunte **explica**; los ejercicios
  resueltos y el material de repaso **entrenan**, y van aparte, enlazados desde `INDICE.md`.
