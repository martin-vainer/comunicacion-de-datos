# Diagnóstico de apuntes y harness — 2026-10-10

## Objetivo y alcance de esta revisión

Preparar una fuente confiable de estudio y de generación de cuestionarios/simulacros, integrando
`capturas/` y `material/` en `apuntes/`, siempre por unidad y sin alterar los originales.

Tres subagentes revisaron consolidación/calidad, fuentes/caches y harness. El diagnóstico incluye
inventario, navegación, estados declarados y muestras académicas/visuales; **no es una revisión
técnica integral de todas las unidades**. No certifica ningún apunte como final.

Inventario comprobado: **22 capturas Markdown** (14 teóricas y 8 prácticas), **45 PDFs en material/**,
2 PDFs adicionales en raíz y **12 caches textuales**. Algunas capturas alimentan varias unidades;
contarlas por unidad no permite sumarlas como archivos distintos. Un placeholder tampoco es una clase
desarrollada.

## Estado por unidad

| Unidad | Producción depurada actual | Fuentes y bloqueo principal | Próxima acción |
|---|---|---|---|
| U1 | Único APUNTE canónico existente, `en-progreso`; TP1 `completo`, 20 ejercicios. | Mejor preparación documental. Pendientes explícitos: modalidades de explotación y funciones/fechas NIC–IANA. | Cerrar pendientes, comprobar cobertura y registrar revisión integral. |
| U2 | Piloto de Fourier y ancho de banda; no hay APUNTE unitario. | Teoría y TP2 tienen cache; banda base y varias respuestas no. Faltan integración de señales, OEM, códigos de línea, filtros y práctica. | Primera consolidación extensa, después del cierre de U1. |
| U3 | Sin APUNTE; TP3 E19 separado y revisado. | Teoría, TP3 y respuestas sin cache específico. Las capturas cubren numerosos temas, no prueban cobertura total. | Consolidar velocidades, sincronismo, redes/protocolos y verificar faltantes de programa. |
| U4 | Sin APUNTE; tres capturas teóricas más práctica y cuestionario. | PDFs de modulación/multiplexación y TP4 sin cache específico; muchas tablas/fórmulas son imágenes. | Consolidar con contraste visual, incluyendo PCM y jerarquías. |
| U5 | Sin teoría canónica; existen capturas teórica y práctica extensas. | TP5 disponible; no se identificó PDF teórico dedicado ni cache específico. | Rastrear respaldo bibliográfico y cobertura de códigos/entropía antes de certificar. |
| U6 | Sin APUNTE; captura extensa con anexo de 38 láminas. | PDF y cache disponibles, pero el cache omite contenido gráfico. Quedan temas del programa por contrastar. | Integrar y verificar visualmente; declarar alcance y pendientes. |
| U7 | Sólo índice teórico y apoyo transversal en práctica/capturas mixtas. | Bibliografía auxiliar disponible; sin capturas propias ni TP dedicado identificado. | Delimitar lo dictado y lo disponible; no confundir fibra/WDM aislados con unidad completa. |
| U8 | Sin apunte ni capturas propias identificadas. | Bibliografía auxiliar disponible; sin PDF de unidad ni TP dedicado identificado. | Identificar alcance/fuentes antes de redactar; mantener provisional cualquier cobertura parcial. |

## Hallazgos que impiden usar el inventario como certificación

1. **Bitácora desactualizada:** [BITACORA](../apuntes/BITACORA.md), líneas 3–29, sigue registrando
   18 piezas. Faltan teoría y práctica U5, teoría U6 y el placeholder de práctica pre-parcial.
2. **Índice U4 desactualizado:** [INDICE U4](../apuntes/teoria/04-modulacion-digitalizacion-multiplexacion/INDICE.md),
   línea 19, dice que multiplexación no está registrada; la bitácora ya identifica la captura Teoría 6.2
   y la práctica 6 que sí la desarrollan. Registro existente no significa consolidación validada.
3. **U1 todavía tiene pendientes reales:** [APUNTE U1](../apuntes/teoria/01-introduccion-comunicaciones/APUNTE.md),
   líneas 375–376. TP1 ya está completo; la memoria antigua que lo describía pendiente no debe guiar
   el próximo trabajo.
4. **Piloto U2 no equivale a unidad completa:**
   [Fourier](../apuntes/teoria/02-senales-telecomunicaciones/serie-de-fourier.md), líneas 175–212,
   presenta la forma compleja sin calcular un coeficiente numérico. El comentario de normalización
   de líneas 218–224 requiere revisar la lámina: no es una errata demostrada por este diagnóstico.
5. **Entrenamiento todavía mínimo:** [índice de repaso](../apuntes/repaso/INDICE.md) y
   [ficha U2](../apuntes/repaso/u02-fourier-y-ancho-de-banda.md) no constituyen simulacros integrales
   de unidades verificadas.
6. **Cache no garantiza fidelidad:** el subagente de fuentes inspeccionó visualmente dos muestras
   (paridad U6 y tabla de parámetros U4) y confirmó información gráfica ausente del texto extraído.
   Las demás páginas no quedaron visualmente certificadas por este muestreo.
7. **Procedencia no es identidad bibliográfica:** el libro `DOC-20230425-WA0040.pdf` se identifica
   como una obra de Castro Lechtaler–Fusario de 2013; no atribuirlo automáticamente a la edición/título
   de 2015 del programa. El cuestionario del 10/09 está en raíz y coincide por hash con su cache;
   no falta la fuente. El cache TP2 conserva ruta vieja, pero su hash coincide con el original actual.

## Harness ajustado en esta sesión

- [AGENTS](../AGENTS.md): capturas permanentemente inmutables, incluyendo imágenes/anexos; canon por U1–U8.
- [Metodología](../apuntes/_plantillas/metodologia.md#puerta-de-calidad): puerta de calidad con cobertura,
  evidencia por sección, contraste, controles ejecutados y registro de revisión. Final no es sinónimo
  de limpio ni un nuevo estado.
- [Protocolo de repaso](../apuntes/_plantillas/metodologia.md#cuestionarios-simulacros): evidencia por
  pregunta, alcance declarado, soluciones justificadas y rúbrica; pendientes excluidos de evaluación.
- [Flujo](flujo-agentico.md), [portada](../README.md) y plantillas alineados con esas reglas.
- Entorno verificado por sesión: `pdftoppm` bundled funciona; `pdftotext` de Git presenta problemas
  de ejecución y no está en PATH de PowerShell. Hay alternativas bundled de extracción. Ninguna
  herramienta disponible demuestra que una revisión visual ya se ejecutó.

Los controles son documentales/manuales: no se añadió infraestructura de software. Los cambios de
harness no modifican estados académicos ni certifican retroactivamente las unidades.

## Orden de trabajo recomendado

**Cerrar U1 → consolidar U2 → U3 → U4 → U5 → U6.** U7/U8 dependen de aclarar cobertura y fuentes.
En cada unidad: actualizar trazabilidad; disponer de caches; integrar teoría/práctica por separado;
contrastar originales y cálculos; aplicar puerta de calidad; revisar el resultado con el estudiante.
El alcance efectivamente dictado y el programa se distinguen explícitamente: no ampliar en silencio.

Pendiente inmediato: cierre académico de U1 y actualización de bitácora/índices afectados. Ningún
apunte académico ni original se modificó en este diagnóstico; no hubo builds ni commits.

Control de cierre: los **254 archivos** presentes en `capturas/` y `material/` conservan sus rutas y
SHA-256 respecto del inicio de esta tarea; no se añadió ni eliminó ninguno. Los cambios previos del
estudiante se preservaron. `git diff --check` pasó; 11 enlaces del informe resuelven a archivos
existentes y el agente del harness comprobó 23 enlaces/anclas publicados de sus documentos.
