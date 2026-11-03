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
que hace usable un documento de 9.500 líneas. En U1–U8 se porta como `INDICE.md` breve por unidad:
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
| Un único archivo gigante | Para U1–U8, un `APUNTE.md` teórico canónico por unidad, con los temas organizados en secciones; `INDICE.md` queda como navegación breve. Práctica y repaso van aparte. | Mantiene una sola fuente teórica por unidad y evita duplicar contenido o estados entre archivos temáticos. Los enlaces del índice apuntan a las secciones del apunte. |

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

### 3.1 Fidelidad docente y apoyos mínimos

Conservá los bloques conceptuales, términos, siglas y notación del profesor. El orden por dependencia de §1.8 sigue siendo válido, pero no autoriza a sustituir agrupaciones docentes por categorías editoriales propias: el estudiante debe poder relacionar apunte y clase. Por ejemplo, mantené reconocible el bloque «Características de interés» y escribí equivalencias como «uplink — enlace ascendente», no sólo su traducción.

Un apoyo conceptual puede aclarar un concepto ya visto; debe identificarse como tal y resolver una dificultad concreta. No agregues temas ni fórmulas para aparentar exhaustividad. Si una fórmula adicional no es necesaria para entender lo tratado, omitila; si es necesaria, indicá su procedencia o derivación y cumplí las reglas de símbolos, unidades, supuestos y ejemplo. Los ejemplos hipotéticos se rotulan como didácticos, no como datos de la cátedra.

No conviertas redondeos o diferencias de notación inocuas en erratas. Una discrepancia que afecte la definición, las unidades, el cálculo o la conclusión requiere separar: **qué afirma la cátedra → evidencia de contraste → conclusión y tratamiento en el apunte**. Si la evidencia no alcanza, registrá el pendiente sin resolverlo por intuición. Esto complementa la jerarquía de fuentes de §4; no vuelve infalible ninguna fuente.

### 3.2 Párrafos sin cortes manuales y cambios sólo de formato

Escribí cada párrafo y cada ítem en una línea lógica, sin insertar EOL por ancho fijo; el editor ajusta visualmente el texto. Conservá líneas en blanco entre párrafos y los saltos necesarios de encabezados, ítems separados y listas anidadas, tablas, citas con párrafos distintos, YAML, código, Mermaid y fórmulas. Un bloque estructurado no se aplana para cumplir la regla de prosa.

Cuando el pedido sea sólo de formato, no reescribas, corrijas ni amplíes contenido, ni cambies la configuración del editor. Compará antes y después: palabras y orden idénticos al normalizar sólo el espacio de la prosa redispuesta; estructura de listas y citas, enlaces, tablas, YAML, código, Mermaid y fórmulas conservados. La igualdad de texto sin espacios no basta para demostrar que se preservó la estructura Markdown. Si se detecta un error de contenido, informalo aparte sin corregirlo dentro de ese pedido.

---

## 4. Alcance, autoridad y fuentes

Son decisiones distintas y NO se mezclan:

- El **programa analítico** (`material/catedra/`) define qué entra en la materia y su vocabulario.
- El **documento original** es la autoridad para lo que afirma: PDF, filmina, guía o enunciado dentro
  de `material/`.
- `material/_cache/` es una transcripción derivada para buscar y redactar. Facilita el acceso, pero no
  es una fuente independiente ni reemplaza el original ante dudas de fórmulas, figuras o notación.
- `capturas/` prueba qué se registró en clase, **no que todo lo registrado sea correcto**. Markdown,
  imágenes y anexos actuales y futuros son inmutables: no corregir, reformatear, mover, renombrar ni
  borrar. La depuración y las discrepancias se escriben únicamente en `apuntes/`, citando la captura
  (archivo y fecha/sección) y el material que respalda la corrección.

Dentro del alcance del programa, se priorizan las fuentes así:

1. Material oficial de cátedra (`material/teoria/`, `material/practica/`).
2. Bibliografía **obligatoria**: Forouzan, Castro Lechtaler & Fusario, Liberatori, Ibe, Stallings.
3. Normas y recomendaciones citadas por la cátedra (UIT-T, IEEE, EIA/TIA).
4. Bibliografía complementaria (Tanenbaum, Abramson, Tomasi, Couch, Stremler…).
5. Conocimiento general del agente — **sólo como apoyo y siempre señalado como tal**.

Regla dura: **el nivel 5 nunca contradice al 1 en silencio.** Si el conocimiento general del agente
difiere del material de cátedra, se registra qué afirma cada fuente y qué evidencia permite resolverlo.
La prioridad de cátedra define el enfoque de examen, no vuelve correcto un error: una discrepancia
material sin resolver permanece visible como pendiente, no como afirmación verificada.

---

### 4.1 Contraste de datos críticos

Son críticos los valores usados en cálculos, límites, especificaciones y comparaciones. Antes de presentarlos como contrastados, volvé al original legible, no sólo al cache ni a la redacción del apunte. Ampliá la tabla o figura cuando haga falta; no completes un dígito dudoso por contexto ni copies un valor de una columna vecina.

Registrá el dato y su evidencia en el registro de revisión, sin saturar cada párrafo: archivo fuente, página o tabla/figura, fila y columna cuando correspondan, valor, unidad y condición —por ejemplo, típico/máximo, frecuencia, ventana o longitud—. Para una imagen sin paginación, identificá tabla y fila/columna. Diferenciá valores leídos de resultados calculados y supuestos didácticos; a estos últimos no les atribuyas una procedencia ficticia.

Si el original indica 0,4 y el candidato dice 0,5, hay una discrepancia de transcripción aunque todas las cuentas con 0,5 sean correctas. Si el original no permite distinguirlos, el dato permanece pendiente: no puede alimentar un ejercicio o una respuesta evaluada como confirmada. El registro de §6.2 y la plantilla teórica muestran cómo dejar esa evidencia.

---

## 5. Workflow para un tema nuevo

```txt
1. Leer el programa; mapear capturas y fuentes de material/ a los temas de cada unidad. No mover una
   captura mixta: integrar cada tema en la unidad que corresponda y enlazar su procedencia.
2. Buscar su transcripción en material/_cache/
3. Si no existe, generarla (ver abajo)
4. Usar la transcripción para buscar y redactar; contrastar el resultado con el PDF, que es la
   autoridad para texto, diagramas y notación
5. Para U1–U8, integrar la teoría en la sección correspondiente del `APUNTE.md` canónico de la unidad;
   conservar ejercicios resueltos en `apuntes/practica/` y actividades de evaluación/repaso en
   `apuntes/repaso/`. No modificar las capturas originales.
6. Actualizar el `INDICE.md` breve con enlaces a las secciones del apunte y a la práctica/repaso
   pertinentes. Registrar los pendientes de contraste junto a la sección afectada, no como estado
   independiente de un tema.
```

Generar cache textual (comprobar primero la disponibilidad y ubicación de `pdftotext`):

```bash
pdftotext -layout -enc UTF-8 "material/teoria/<archivo>.pdf" "material/_cache/<nombre>.txt"
```

Notas de entorno:

- Verificar herramientas por sesión. En la comprobación del 2026-10-10, PowerShell resolvió
  `pdftoppm` del runtime Poppler y `rg`, pero no `pdftotext` en su PATH; eso no demuestra que no exista
  en otro directorio o shell. Los diagnósticos previos sobre herramientas faltantes no son reglas.
- Si `pdftotext` no está accesible, localizar el runtime disponible o usar `pypdf` sólo si está
  instalado, guardando el cache en UTF-8. No instalar herramientas sin autorización.
- La extracción textual no verifica diagramas ni notación visual. Renderizar/inspeccionar las páginas
  originales cuando haga falta; si no se puede, registrar exactamente qué contraste falta.

> **No consolidar una sección del apunte si su PDF todavía no tiene cache textual**, salvo pedido
> explícito.

---

## 6. Estado del apunte canónico de unidad

En U1–U8 el destino es un solo `APUNTE.md` teórico por unidad. Su front matter lleva `unidad`, `estado`,
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

<a id="puerta-de-calidad"></a>
### 6.1 Puerta de calidad: cuándo es un apunte final

**Final no es otro estado:** se reserva para una unidad `revisado` con todo el alcance del programa
cubierto. Un apunte completo de un subconjunto declara sus exclusiones y no es la unidad final.
Antes de promover el estado, dejar en `APUNTE.md` evidencia de estos controles:

1. **Cobertura:** tabla breve `tema del programa + términos/siglas docentes → sección → captura/material (página o sección) → cubierto/pendiente`. Incluir conceptos y figuras relevantes, no sólo contar páginas. Un tema sin captura puede desarrollarse desde material; sin evidencia suficiente queda pendiente. Distinguir lo visto en clase de lo exigido por el programa.
2. **Rigor y enfoque:** contrastar cada sección con originales; verificar fórmulas, símbolos, unidades,
   supuestos, cálculos, resultados y diagramas. Explicar conceptos centrales con la secuencia de §1.1;
   comprobar errores típicos, respuesta de examen, resumen mental y checklist. No agregar relleno ni
   confundir limpieza de redacción con verificación.
3. **Trazabilidad:** cada sección identifica su captura de origen, cuando exista, y el material que
   sostiene sus afirmaciones, con páginas o secciones. Las discrepancias se registran explícitamente;
   no ocultarlas ni resolverlas sin evidencia.
4. **Integridad y navegación:** comprobar enlaces y anclas, unidad de destino y separación teoría /
   práctica / repaso. Verificar que no se modificaron originales; no restaurar ni borrar cambios previos
   del estudiante para que el control parezca pasar.
5. **Registro de revisión:** fecha, alcance, fuentes, controles ejecutados y resultados, limitaciones y pendientes, separados por tipo según §6.2. No dar por ejecutado un control sólo porque figura en un checklist.

Una sección sin contrastar, un cálculo dudoso o una figura inaccesible impide `revisado`. Si la cobertura
es parcial, nombrar el alcance real; nunca anunciar «unidad final» o «simulacro integral» por omisión.

---

<a id="revision-diferenciada"></a>
### 6.2 Revisión diferenciada y evidencia

Informá tres tipos de comprobación por separado. Ninguno sustituye a los demás ni habilita por sí solo el estado `revisado`:

| Tipo de control | Evidencia que debe registrarse | Qué no demuestra por sí solo |
|---|---|---|
| Estructural | Archivos y secciones examinados; resultado de enlaces, anclas, formato e integridad de originales | Corrección de datos, fórmulas o explicaciones |
| Recálculo | Entradas utilizadas, operación o procedimiento, unidades y resultado obtenido | Que las entradas coincidan con la fuente ni que el modelo sea aplicable |
| Contraste técnico | Original y localizador legible; comparación de conceptos, datos críticos, fórmulas, condiciones, figuras y vocabulario docente | Cobertura integral de secciones que no se contrastaron |

En cada tipo indicá **alcance → método realmente usado → resultado → limitaciones y pendientes**. Si una comprobación no se ejecutó, escribí «no realizado»; si no corresponde, explicá por qué. Una discrepancia no se transforma en «comprobado» porque otro tipo de control haya pasado. El revisor debe volver a la fuente original, no limitarse a aceptar las cuentas o la afirmación de verificación del redactor.

Usá el registro y la tabla compacta de evidencia de la [plantilla teórica](apunte-teoria.md#registro-revision). No exijas una fila por cada número de un ejemplo hipotético: concentrá el contraste de fuente en los datos críticos tomados de material real. En práctica y repaso, mantené además la literalidad y la evidencia por pregunta de §8.

La revisión es un conjunto de comprobaciones con alcance explícito, no una garantía de ausencia total de errores. Sólo la puerta de calidad completa de §6.1 permite promover el estado de la unidad.

---

## 7. Lo que NO se hace

- No transcribir la filmina. El apunte **reconstruye**, no copia.
- No pegar una fórmula sin tabla de símbolos, unidades y supuestos.
- No inventar valores, normas ni números de recomendación UIT-T. Si no está en el material y no se sabe
  con certeza, se escribe `<!-- PENDIENTE: verificar en material -->` y se avisa.
- No tapar contradicciones entre cátedra y bibliografía.
- No mezclar unidades del programa en un mismo `APUNTE.md`.
- No editar originales dentro de `material/`; sólo generar derivados en `material/_cache/`.
- No modificar ningún original de `capturas/`, aunque tenga errores.
- No meter cuestionarios ni flashcards dentro del apunte principal. El apunte **explica**; los ejercicios
  resueltos y el material de repaso **entrenan**, y van aparte, enlazados desde `INDICE.md`.

---

<a id="cuestionarios-simulacros"></a>
## 8. Práctica, cuestionarios y simulacros confiables

Se guardan en `apuntes/practica/` los TPs, guías y ejercicios resueltos; los cuestionarios/simulacros
van en `apuntes/repaso/`. Una evaluación conversacional no modifica archivos. Usá fuentes contrastadas,
indicá su localizador preciso y declará el alcance/pendientes; una sección verificada de una unidad en
progreso puede alimentar práctica o repaso **parcial**, pero no certificar toda la unidad.

### 8.1 TPs, guías y ejercicios resueltos

- **Enunciado literal primero:** transcribí completo el texto de la fuente que se está resolviendo,
  incluyendo subítems, datos, unidades, tablas y opciones, sin paráfrasis ni correcciones silenciosas.
  Sólo se normalizan saltos de línea. Referenciá archivo y página/sección del PDF o archivo/línea de la
  captura; las capturas y los PDFs originales son inmutables.
- Si una errata, ambigüedad o discrepancia necesita aclaración, mantené intacta la transcripción y
  agregá la nota por separado, con procedencia/evidencia. No presentes una lectura probable como si
  fuera la consigna original.
- **Datos después del enunciado:** resumí los valores, símbolos y unidades que efectivamente brinda la
  consigna, más sus condiciones. No reemplaza el enunciado ni agrega parámetros inferidos. En preguntas
  conceptuales o sin números, escribí que no hay datos numéricos y enumerá las premisas pertinentes;
  nunca inventes datos para llenar la tabla.
- Después de `Datos`, explicá qué se pide y desarrollá la **resolución paso a paso**, justificando por
  qué corresponde cada método, conversión, fórmula, sustitución y conclusión. Mostrá unidades y
  supuestos. Una comprobación o enseñanza adicional va identificada como nota pedagógica, no mezclada
  con lo que afirma la fuente.
- **Preservación conservadora:** si el desarrollo ya registrado en una captura es correcto y claro,
  conservá su orden, método, cuentas, resultados y formato sustantivo. No lo reescribas entero ni
  reemplaces la voz del docente por otra solución; agregá únicamente las explicaciones que hagan falta
  para aprender el porqué de cada paso. Si corregís un error, explicá el motivo y citá la evidencia,
  manteniendo tanto el original como la corrección claramente distinguibles.
- En cuestionarios de opción múltiple, conservá literal la pregunta, el orden de opciones y la notación;
  presentá después las condiciones/datos extraídos y una resolución razonada. Si se usa para
  autoevaluación, separá la respuesta de la consigna y explicá también por qué las opciones incorrectas
  no aplican. No transformes distractores para hacerlos más sencillos.

### 8.2 Cuestionarios y simulacros confiables

Sólo se escriben cuando el estudiante autoriza; usar secciones contrastadas y registrar el alcance:
unidad/es, temas, dificultad, modalidad y, para un simulacro, tiempo/puntaje. Si hay temas excluidos o
pendientes, declararlos; no evaluar una afirmación no verificada como cierta.

- Cada pregunta tiene un identificador y vincula su sección de `APUNTE.md` y la evidencia original
  (archivo y página/sección). Una tabla común evita repetir referencias extensas.
- Transcribir fielmente preguntas/opciones del origen cuando se practique sobre una evaluación
  registrada; ver el formato de `Datos`/condiciones en §8.1. Para preguntas nuevas, los datos
  hipotéticos se identifican como tales y la evidencia no se atribuye a la fuente original.
- Mezclar comprensión, distinciones, aplicación y cálculos cuando correspondan; no limitarse a
  memorizar definiciones.
- Separar enunciados de respuestas/rúbrica cuando permita autoevaluación sin anticipar la solución.
  Cada respuesta explica el porqué; los cálculos muestran unidades y supuestos. La rúbrica aclara qué
  razonamiento da puntaje y qué errores lo invalidan. Las opciones incorrectas tienen explicación.
- Antes de publicar, verificar claridad y resolubilidad del enunciado, respuesta/rúbrica, cálculos,
  evidencia, enlaces y cobertura declarada. Registrar fecha y pendientes; si falta una comprobación,
  marcar borrador y excluir ese ítem de la evaluación hasta resolverla.
- En modo Tutor, preguntar de a una, esperar el intento y corregir el razonamiento con evidencia.
