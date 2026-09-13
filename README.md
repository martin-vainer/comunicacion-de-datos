# Comunicación de Datos — UTN

Apuntes y material de la asignatura **Comunicación de Datos**, Ingeniería en Sistemas de Información,
Universidad Tecnológica Nacional. Plan 2023 · Nivel 4º · Cuatrimestral.

## Estructura

```
apuntes/          Producción propia, en Markdown
  BITACORA.md      Recorrido cronológico y trazabilidad de las clases
  teoria/         Un directorio por unidad del programa (01 a 08)
  practica/       TPs, guías de ejercicios, laboratorios
  repaso/         Preguntas y actividades derivadas de apuntes consolidados
  _plantillas/    Plantillas de captura, apunte, ejercicio e índice

capturas/         Registro histórico de clases y cuestionarios, con sus imágenes
  teoria/         Capturas teóricas en el subárbol de su unidad original
  practica/       Capturas prácticas y mixtas

material/         Fuentes de terceros — no se editan
  teoria/         PDFs, libros, filminas de cátedra
  practica/       Enunciados, guías, datasets, código
  catedra/        Programa analítico, cronogramas
```

## Navegación por contenido existente

- [Unidad 1 — Introducción a las comunicaciones](apuntes/teoria/01-introduccion-comunicaciones/INDICE.md)
- [Unidad 2 — Características de las señales](apuntes/teoria/02-senales-telecomunicaciones/INDICE.md)
- [Unidad 3 — Redes de telecomunicaciones](apuntes/teoria/03-redes-telecomunicaciones/INDICE.md)
- [Unidad 4 — Modulación, digitalización y multiplexación](apuntes/teoria/04-modulacion-digitalizacion-multiplexacion/INDICE.md)
- [Unidad 6 — Canales de comunicaciones](apuntes/teoria/06-canales-comunicaciones/INDICE.md)
- [Unidad 7 — Medios de comunicaciones](apuntes/teoria/07-medios-comunicaciones/INDICE.md)
- [Práctica](apuntes/practica/INDICE.md)
- [Repaso y cuestionarios](apuntes/repaso/INDICE.md)

Las unidades 5 y 8 todavía no tienen apuntes ni capturas propios; su alcance permanece definido en el
programa y en `AGENTS.md`. No se crean índices vacíos.

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
YAML obligatorio. Después se contrasta la captura y recién entonces se consolida como apunte por tema.

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
