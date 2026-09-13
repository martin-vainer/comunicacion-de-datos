# Comunicación de Datos — UTN

Apuntes y material de la asignatura **Comunicación de Datos**, Ingeniería en Sistemas de Información,
Universidad Tecnológica Nacional. Plan 2023 · Nivel 4º · Cuatrimestral.

## Estructura

```
apuntes/          Producción propia, en Markdown
  BITACORA.md      Recorrido cronológico y trazabilidad de las clases
  teoria/         Un directorio por unidad del programa (01 a 08)
  practica/       TPs, guías de ejercicios, laboratorios
  _plantillas/    Plantillas de captura, apunte, ejercicio e índice

material/         Fuentes de terceros — no se editan
  teoria/         PDFs, libros, filminas de cátedra
  practica/       Enunciados, guías, datasets, código
  catedra/        Programa analítico, cronogramas
```

## Unidades

1. Introducción a las comunicaciones
2. Características de las señales de telecomunicaciones
3. Redes de telecomunicaciones
4. Modulación, digitalización y multiplexación de señales
5. Teoría de la información y de la codificación
6. Canales de comunicaciones
7. Medios de comunicaciones
8. Hardware de comunicaciones

## Cómo se usa

Los apuntes son Markdown plano: matemática en LaTeX (`$...$`), diagramas en Mermaid. Se leen en
cualquier editor, en GitHub o en Obsidian.

Dos entradas cubren necesidades distintas:

- [Índice de la Unidad 2](apuntes/teoria/02-senales-telecomunicaciones/INDICE.md): navegar por tema.
- [Bitácora de clases](apuntes/BITACORA.md): recuperar el recorrido de la cursada y saber dónde se
  originó cada contenido.

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
