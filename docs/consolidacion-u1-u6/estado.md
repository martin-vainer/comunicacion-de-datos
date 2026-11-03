# Ejecución de consolidación U1–U6

## Alcance y reglas

- Sólo conocimiento registrado en capturas y material específico. Bibliografía para contraste y aclaración, no para añadir temas programáticos nuevos.
- U7/U8 fuera de alcance; los ejercicios transversales existentes pueden enlazarse sin extender su revisión a una unidad.
- Originales y cambios previos preservados. Sin builds, instalaciones, commits ni issues en GitHub.
- Baseline: [originales](baseline-originales.json) y [estado Git previo](baseline-git.txt), registrados antes de la preparación.
- Curador: nuevos caches e inventario de fuentes. Autores: rutas unitarias asignadas. Coordinador: documentos compartidos y reportes.
- Cada PDF utilizado requiere cache antes de consolidar su sección; el texto no sustituye contraste visual.

## Propiedad de escritura

| Responsable | Rutas asignadas |
|---|---|
| Curador | Nuevos archivos de `material/_cache/`; PDFs de contraste en `tmp/curador-ejecucion/externos/`; `docs/consolidacion-u1-u6/inventario-fuentes.md` (entrega terminada) |
| Autor U1 | Carpeta teórica U1; `apuntes/practica/tp-01-comunicaciones.md` sólo por error demostrado; nuevo `apuntes/repaso/u01-introduccion-comunicaciones.md` |
| Autor U2 | Carpeta teórica U2 y stubs compatibles; nuevo `apuntes/practica/tp-02-senales.md`; `apuntes/repaso/u02-fourier-y-ancho-de-banda.md` y nuevo `u02-senales.md` |
| Autor U3 | Carpeta teórica U3; nuevo `apuntes/practica/tp-03-redes.md`; nuevo `apuntes/repaso/u03-redes.md`; E19 existente sólo referencia |
| Autor U4 | Carpeta teórica U4; nuevo `apuntes/practica/tp-04-modulacion-multiplexacion.md`; nuevo `apuntes/repaso/u04-modulacion-multiplexacion.md` |
| Autor U5 | Carpeta teórica U5; nuevo `apuntes/practica/tp-05-informacion-codificacion.md`; nuevo `apuntes/repaso/u05-informacion-codificacion.md` para las diez preguntas de la captura teórica |
| Autor U6 | Carpeta teórica U6; nuevo `apuntes/practica/tp-06-canales.md` si existe guía registrada; nuevo `apuntes/repaso/u06-canales.md` sólo para preguntas registradas transversales |
| Coordinador | Bitácora, portada, índices generales, reportes, manifiestos y recursos mixtos sin dueño unitario único |

Ningún autor escribe en un recurso de otro. Las propuestas sobre compartidos se devuelven al coordinador. Los autores no generan caches propios.

## Seguimiento

| Etapa | Estado |
|---|---|
| Baseline de originales/cambios previos | Registrado: 259 archivos |
| Curaduría y caches | Completada: 27 nuevos caches iniciales + 3 de contraste U5, 42 total; 12 históricos intactos |
| Autores U1–U3 | Candidatos ciclo 1 entregados; U1–U3 siguen en-progreso; retests focales A/B recibidos |
| Autores U4–U6 | Candidatos ciclo 1 entregados; U4–U6 siguen en-progreso; retests focales A/B recibidos |
| Integración de navegación compartida | Cerrada: seis candidatos y 22 capturas trazadas; sin marcas en producción |
| Snapshot de candidatos | Inicial y ciclo 1 congelados: `snapshot-inicial.json`, `snapshot-ciclo1.json`; fuentes y caches incluidos |
| 12 reviews unitarias + 1 transversal | 13 dictámenes iniciales sintetizados; informes completos en `docs/revision-uNN.md` y revisión transversal |
| Correcciones/revalidación | Ciclo 1 aplicado; focos U1–U6 revalidados A/B; control global y cierre C-C1-001 recibidos. Ver `docs/verificacion-ciclo1-uNN.md` y `docs/verificacion-transversal-ciclo1.md` |
| Cierre de integridad/estados | Checker de ciclo 1: 259 originales intactos, 401 entradas del snapshot sin diferencias/agregados, 805 enlaces válidos. Estados académicos honestos `en-progreso`; `revisado/final` no se asignan por retest focal |

## Revisión y aceptación

### Candidatos recibidos

- U1–U6: teoría, navegación, práctica y repaso están consolidados como candidatos. Ciclo 1 cerró los issues de los dictámenes iniciales con notas de retest por ID; consultar `sintesis-inicial.md` y cierres de autor. No se promovió ninguna unidad a `revisado` ni `final`.
- Los pendientes de fuentes/cobertura y las limitaciones de revisión continúan visibles por unidad; `docs/revision-u01.md`…`u06.md` contienen dictámenes A/B iniciales.

El paquete de candidatos se congeló con teoría, práctica, repaso, imágenes, navegación, fuentes y caches en `snapshot-inicial.json`; tras el ciclo 1 quedó `snapshot-ciclo1.json`. La revisión inicial usó la misma versión para dos revisores independientes por unidad y uno transversal; las correcciones comenzaron sólo al recibir los 13 dictámenes.

Cada dictamen registra secciones/evidencias comprobadas, limitaciones y hallazgos con ID, prioridad, ubicación, evidencia, acción y prueba de cierre. Una sospecha se distingue de un error demostrado. Los autores corrigieron y los revisores revalidaron focalmente con evidencia; ciclo 1 está cerrado, ciclo 2 no se inicia sin una falla/issue demostrado.

Los originales deben conservar rutas/bytes. Los caches nuevos se identifican como derivados; los existentes no se sobrescriben. Un pendiente o falta de cobertura nunca se oculta detrás de `revisado` o «final».
