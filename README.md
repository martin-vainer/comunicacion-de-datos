# Comunicación de Datos — UTN

Apuntes y material de la asignatura **Comunicación de Datos**, Ingeniería en Sistemas de Información,
Universidad Tecnológica Nacional. Plan 2023 · Nivel 4º · Cuatrimestral.

## Estructura

```
apuntes/          Producción propia, en Markdown
  BITACORA.md      Recorrido cronológico y trazabilidad de las clases
  teoria/         Un directorio por unidad; destino U1–U8: APUNTE.md canónico + INDICE.md breve
  practica/       TPs, guías de ejercicios, laboratorios
  repaso/         Preguntas y actividades derivadas de apuntes consolidados
  resumenes/      Cuadros y fórmulas de repaso rápido
  _plantillas/    Plantillas de captura, apunte, ejercicio e índice

capturas/         Originales de clases y cuestionarios, con imágenes/anexos; siempre inmutables
  teoria/         Capturas teóricas en el subárbol de su unidad original
  practica/       Capturas prácticas y mixtas

primer_parcial/   Fotos originales de examen — U1–U4
segundo_parcial/  Fotos originales de examen — U5–U8

material/         Fuentes de terceros — no se editan
  teoria/         PDFs, libros, filminas de cátedra
  practica/       Enunciados, guías, datasets, código
  catedra/        Programa analítico, cronogramas
```

## Navegación

- [TODOs — Lista canónica de pendientes](todos.md)

- [Unidad 1 — Introducción a las comunicaciones](apuntes/teoria/01-introduccion-comunicaciones/INDICE.md)
- [Unidad 2 — Características de las señales](apuntes/teoria/02-senales-telecomunicaciones/INDICE.md)
- [Unidad 3 — Redes de telecomunicaciones](apuntes/teoria/03-redes-telecomunicaciones/INDICE.md)
- [Unidad 4 — Modulación, digitalización y multiplexación](apuntes/teoria/04-modulacion-digitalizacion-multiplexacion/INDICE.md)
- [Unidad 5 — Teoría de la información y codificación](apuntes/teoria/05-teoria-informacion-codificacion/INDICE.md)
- [Unidad 6 — Canales de comunicaciones](apuntes/teoria/06-canales-comunicaciones/INDICE.md)
- [Unidad 7 — Medios de comunicaciones](apuntes/teoria/07-medios-comunicaciones/INDICE.md)
- [Unidad 8 — Hardware de comunicaciones](apuntes/teoria/08-hardware-comunicaciones/INDICE.md)
- [Práctica](apuntes/practica/INDICE.md)
- [Repaso y cuestionarios](apuntes/repaso/INDICE.md)
- [Resumen del primer parcial (U1–U4)](apuntes/resumenes/primer-parcial-u01-u04.md)
- [Resumen del segundo parcial (U5–U8)](apuntes/resumenes/segundo-parcial-u05-u08.md)
- [Parciales: fotos originales y resoluciones](docs/flujo-agentico.md#parciales)

La campaña de [consolidación U1–U6](docs/consolidacion-u1-u6/estado.md) integra sólo lo registrado en
capturas y material específico; la bibliografía sirve para contrastarlo, no para ampliar el temario.
Los seis paquetes U1–U6 están entregados como **candidatos**, pendientes de revisión independiente.
La [bitácora](apuntes/BITACORA.md) enlaza las 22 capturas Markdown y separa evidencia original de destino.
El seguimiento operativo está en el documento de campaña; el **estado académico de cada unidad está
únicamente en su `APUNTE.md`**. Ni un índice ni la existencia de un archivo certifican revisión.

U7/U8 quedan fuera de esta campaña. Se conserva la navegación histórica U7 y el ejercicio transversal
E19 sin ampliar su revisión a U7. U8 tiene su propio apunte desde las presentaciones de `material/teoria/U8/`;
su cobertura y sus pendientes se declaran en el documento, sin heredar el estado de otras unidades.

El criterio de consolidación para U1–U8 es un único `APUNTE.md` por unidad, con temas por secciones;
`INDICE.md` sólo navega ese contenido. La práctica resuelta y el repaso/autoevaluación permanecen en
`apuntes/practica/` y `apuntes/repaso/`. El estado `revisado` representa la unidad entera, no una sección.

## Cómo se usa

Los apuntes son Markdown plano: matemática en LaTeX (`$...$`), diagramas en Mermaid. Se leen en
cualquier editor, en GitHub o en Obsidian.

Tres entradas cubren necesidades distintas:

- Los índices anteriores: navegar por tema o tipo de actividad.
- [Bitácora de clases](apuntes/BITACORA.md): recuperar el recorrido de la cursada y saber dónde se
  originó cada contenido.
- [`capturas/`](capturas/): consultar el registro histórico íntegro, sin confundirlo con material
  académicamente revisado.

Durante la clase se usa la [plantilla de captura rápida](apuntes/_plantillas/captura-clase.md), sin
YAML obligatorio. `capturas/` conserva evidencia original actual y futura: no se modifica, mueve,
renombra ni borra ningún archivo, imagen o anexo. El trabajo de depuración se hace en `apuntes/`,
integrando capturas y material por unidad. Las correcciones se explican allí, con procedencia; los
ejercicios y el repaso se guardan por separado.

Un apunte **final** debe pasar la [puerta de calidad](apuntes/_plantillas/metodologia.md#puerta-de-calidad):
cobertura del programa, evidencia por sección, contraste integral y controles documentados. Los
[cuestionarios/simulacros](apuntes/_plantillas/metodologia.md#cuestionarios-simulacros) usan contenido
verificado, con trazabilidad y corrección razonada; una unidad parcial nunca se presenta como examen
completo. Estas reglas describen el objetivo, no certifican el estado actual de los apuntes.

Este repo está preparado para trabajarse con agentes, pero no depende de ellos. El circuito y los
pedidos operativos están en [Flujo agéntico](docs/flujo-agentico.md); las reglas del agente están en
[AGENTS.md](AGENTS.md), y la [metodología](apuntes/_plantillas/metodologia.md) es la única autoridad
pedagógica.

Los hitos del refactor y su reversión segura se documentan en
[Hitos y rollback](docs/hitos-y-rollback.md).

## Bibliografía obligatoria

- Forouzan, B. A. (2021). *Data Communications and Networking with TCP/IP*. McGraw Hill.
- Castro Lechtaler, A. y Fusario, R. (2015). *Comunicaciones y redes para profesionales en sistemas de información*. Alfaomega.
- Liberatori, M. (2018). *Redes de datos y sus protocolos*. Eudem.
- Ibe, O. (2018). *Data Communication Networks*. Wiley.
- Stallings, W. (2007). *Comunicaciones y Redes de Computadoras*. Pearson Prentice Hall.
