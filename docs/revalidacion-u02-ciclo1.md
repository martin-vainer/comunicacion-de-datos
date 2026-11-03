# Cierres U2 — ciclo 1 de correcciones dirigidas

Fecha: **2026-10-13**. `skill_resolution: injected`.
**Siete IDs corregidos y retesteados por el autor; aceptación independiente pendiente.**
La unidad conserva `estado: en-progreso`. Este documento no reemplaza los dictámenes originales,
no promueve la unidad a revisada/final y no incorpora preguntas nuevas.

## Alcance y versión

Guía exclusiva: `docs/consolidacion-u1-u6/sintesis-inicial.md`, `docs/revision-u02.md`,
`tmp/reviews/u02-a.md` y `tmp/reviews/u02-b.md`. No se leyeron informes de otras unidades.
Sólo cambiaron estos tres candidatos:

- `apuntes/teoria/02-senales-telecomunicaciones/APUNTE.md`.
- `apuntes/practica/tp-02-senales.md`.
- `apuntes/repaso/u02-senales.md` (razón de S05, sin alterar enunciados ni claves).

Los otros 18 archivos del paquete U2 inicial —incluidos pilotos, índice, ficha Fourier,
manifest, cuatro PNG y siete SVG— conservan sus bytes. Evidencia de partida:
[candidatos antes](../autor-u02/ciclo1/candidatos-antes.json).
Los originales/caches, snapshot inicial, síntesis e informes originales fueron sólo lectura.
No hubo build, instalación ni commit.

## U02-A-001 — misión de detectar presencia de señal

**Estado del autor: cerrado; retest pasó.**

- **Evidencia original:** captura `capturas/practica/clase 02.md`, apartado «misión»;
  `UT 2 SEÑALES TELCOM-CODIGOS DE LINEA.pdf`, PDF15, enumera explícitamente continua,
  sincronismo y presencia. `Señales Banda Base.pdf`, PDF16, ilustra el error de confundir
  una racha de ceros unipolares con medio libre. Ambos originales se renderizaron y vieron:
  [UT15](../autor-u02/ciclo1/ut-15.png), [BB16](../autor-u02/ciclo1/bb-16.png).
- **Corrección:** [canon, presencia](../../apuntes/teoria/02-senales-telecomunicaciones/APUNTE.md#presencia-senal),
  TP2 E13, respuesta oral, resumen y checklist. El ejemplo declara reposo a 0 V, A=1 V y Tb=1 ms.
  `0000` en unipolar NRZ y ese reposo son indistinguibles por tensión sola; polar NRZ muestra
  −1 V constante sin transiciones; Manchester mantiene actividad/transiciones.
- **Retest:** cuatro celdas/4 ms, ocho medias celdas por variante; el nivel unipolar es idéntico
  al reposo supuesto. Polar NRZ es no nulo pero sin cambios interiores; Manchester cambia en cada
  celda. Se verificó que el canon excluye expresamente «tensión instantánea cero = línea inactiva».
  Polar RZ sigue emitiendo aunque retorne a cero. No se universaliza el supuesto de reposo.

## U02-A-002 — aplicación numérica de E(z,t) y H(z,t)

**Estado del autor: cerrado; retest pasó.**

- **Evidencia:** las expresiones registradas de U2 PDF26 y su representación PDF28 sustentan
  el modelo ya presente en `#oem`; el ejemplo agregado es explícitamente hipotético, no un nuevo
  resultado oficial ni un desarrollo de ecuaciones diferenciales.
- **Corrección:** se dan f=100 MHz, v=3·10⁸ m/s, z=0,75 m, φ=0, E0=3,77 V/m y H0=0,010 A/m.
  Ambas amplitudes son datos del ejemplo, no una deducción de una desde la otra. Se aplica
  la misma fase retardada a ambos campos y se conservan sus respectivas unidades.
- **Retest numérico:** z/v=2,5 ns y ω=2π·10⁸ rad/s. Para t=0, fase −π/2, E=0 V/m y H=0 A/m
  (residuo flotante del coseno <10⁻¹²). Para t=2,5 ns, fase 0, E=3,77 V/m y H=0,010 A/m;
  para t=7,5 ns, fase π, E=−3,77 V/m y H=−0,010 A/m. La tabla publicada coincide.
  El signo instantáneo no se presenta como inversión de propagación.

## U02-A-003 — incompatibilidad de convención 2B1Q al enlazar figura

**Estado del autor: cerrado; retest pasó.**

- **Evidencia visual:** [U2 PDF43](../autor-u02/ciclo1/u2-43.png) asigna
  00→−2,5 V, 01→−0,833 V, 10→+2,5 V, 11→+0,833 V.
  [U2 PDF44](../autor-u02/ciclo1/u2-44.png) dibuja 01 positivo y 10/11 negativos.
  El eje gráfico no tiene calibración numérica suficiente para imputarle voltajes específicos.
- **Corrección:** aviso accesible **antes** del enlace a `multinivel.png`, y tabla reconstruida
  de los diez dibits con la convención de p.43. Se explicita que otra asignación no es por sí misma
  inválida; el panel histórico no sirve para validar los signos de la tabla adoptada.
  La imagen original y su copia se conservaron intactas.
- **Retest:** se comprobó el mapeo de los cuatro dibits, incluido 01/10. Para
  `01 10 11 10 10 11 11 01 01 01`, la tabla adoptada produce, en V:
  `−0,833; +2,5; +0,833; +2,5; +2,5; +0,833; +0,833; −0,833; −0,833; −0,833`.
  Los signos del panel histórico son `+ − − − − − − + + +`: se muestra la divergencia de los diez,
  no sólo la primera pareja. La decodificación inversa recupera los 20 bits.
  El ejemplo previo `001110` sigue dando `−2,5; +0,833; +2,5 V`.

## U02-A-004 — página bibliográfica de polar RZ

**Estado del autor: cerrado; retest pasó.**

- **Evidencia original:** [Castro/Fusario PDF148](../autor-u02/ciclo1/libro-148.png), impresa122,
  título **§2.8.5.4 Polar con retorno a cero (RZ)** y **fig.2.43**. La página describe pulso positivo
  para 1, negativo para 0, retorno a cero y recuperación del reloj; es la localización correcta.
- **Corrección:** TP2 E16 ahora cita PDF148/impresa122, §2.8.5.4 y fig.2.43, con enlace `#page=148`.
  Se retiró la atribución a PDF149/impresa123 en esa resolución.
- **Retest:** se abrió y vio el original; se verificó ruta/fragmento y literal de la referencia.
  E16 conserva los 17 bits, 9 unos/8 ceros, todas las parejas polar RZ y media de bloque A/34.
  No se cambió el resultado ni el SVG para corregir una cita.

## U02-B-001 — contradicción 2B1Q (convergente con A-003)

**Estado del autor: cerrado; retest pasó.**

- **Evidencia:** contraste independiente de autor con U2 PDF43/44 y los dos renders enlazados en A-003.
  La tabla y el gráfico muestran signos incompatibles para 01/10; no se decide un mapping universal.
- **Corrección:** el aviso precede al recurso; los diez símbolos calculados se separan del dibujo
  histórico, que sigue idéntico. El lector sabe qué convención reproducir y cuál no puede usar como control.
- **Prueba específica:** orden del aviso antes del enlace comprobado automáticamente; valores
  y signos de los diez dibits, ejemplo `001110` y roundtrip de 20 bits pasaron. PNG fuente/copia conservan SHA-256.

## U02-B-002 — presencia omitida en canon y TP2 E13 (convergente con A-001)

**Estado del autor: cerrado; retest pasó.**

- **Evidencia:** misión literal de Práctica2/UT PDF15; problema físico del original BB PDF16,
  inspeccionados por el autor como se detalla en A-001.
- **Corrección:** canon `#presencia-senal`, E13 y razón de S05 existente están enlazados. Se separan
  presencia, sincronismo y decisión del dato; no se agregaron preguntas ni una clave nueva.
- **Prueba específica:** el retest de `0000` distingue reposo supuesto/unipolar NRZ, polar NRZ
  con actividad sin reloj y Manchester con transiciones; también contempla el retorno a 0 de polar RZ.
  Ambos enlaces desde E13/S05 resuelven y permanecen **19 IDs** de repaso en total.

## U02-B-003 — referencia polar RZ (convergente con A-004)

**Estado del autor: cerrado; retest pasó.**

- **Evidencia:** PDF148/impresa122, §2.8.5.4 y fig.2.43 visibles en el original.
- **Corrección:** E16 remite a esa localización, no PDF149/123.
- **Prueba específica:** búsqueda dirigida de la atribución anterior en E16 negativa; referencia nueva
  presente, enlace al libro resuelto, 34 medias celdas y decodificación de E16 intactas.
  La corrección bibliográfica no se convirtió en cambio de regla ni de valor medio.

## QA de regresión realizado

Script y resultados nuevos, sin sobrescribir autocontroles iniciales:
[retest.py](../autor-u02/ciclo1/retest.py) · [qa-ciclo1.json](../autor-u02/ciclo1/qa-ciclo1.json).
Versión de entrega: [SHA-256 después del ciclo](../autor-u02/ciclo1/entrega-despues.json).

| Ítem | Retest / resultado |
|---|---|
| TP E1–3 | Relectura cualitativa de consignas y resolución: ambas representaciones, cinco ventajas acotadas, regeneración sin corregir mágicamente una decisión errónea. No tienen una cuenta numérica pedida. |
| E4 | f=50 Hz, T=20 ms, ω=100π rad/s, φ=π/2, v(0)=300 V; integración periódica numérica: media≈0, RMS=212,132034 V. λ no inventada. |
| E5 | λ(88 MHz)=3,4090909 m; λ(108 MHz)=2,7777778 m; rango y redondeo conservados. |
| E6 | T=10 ms, τ=0,5 ms y FRP=100 pps para ejemplo heredado; intervalos distintos en diagrama. |
| E7 | Icc=√2 A y P=20 W para ejemplo hipotético; integración media cuadrática comprobada, no media firmada. |
| E8 | bn para n=1–20 recalculados: pares 0, impares4/(nπ); primeros1,273240/0,424413/0,254648. |
| E9 | T=0,25 s, τ=0,05 s, D=0,2, B=20 Hz, n0=5,4 armónicas positivas antes; C0/A=0,2. |
| E10 | T=0,01 s, τ=0,0005 s, D=0,05, B=2000 Hz, n0=20,19 positivas; C0=0,05 V y C1≈0,049794637 V. |
| E11 | T=1/300 s, τ=1/1200 s, D=0,25, B=1200 Hz, n0=4,3 positivas; C0=0,25 V. |
| E12 | T=0,1 s, τ=0,02 s, D=0,2, B=50 Hz, n0=5,4 positivas; C0=0,2 V. No se inventó solución oficial. |
| E9–12 SVG | Todas las **140 líneas** y **2404 puntos de envolvente** cotejados con sinc y coordenadas; cero/lóbulos posteriores y unidades coherentes. |
| E13 | Relectura de misión y contraste presencia/dato/reloj; sigue diferenciando banda base de portadora modulada. |
| E14 | Secuencia completa: 34 bits/10 marcas; signos AMI alternan sin reinicio y bipolar RZ retorna a0. No A/Tb inventados. |
| E15 | 17 bits; Manchester y diferencial decodifican secuencia original, previo− y convención de dato preservados. |
| E16 | 17 bits/9 unos; pares polarRZ y media A/34, con cita corregida. |
| E14–16 SVG | **238 medias celdas** leídas de geometría XML concordantes con reglas y decodificación; siete filas intactas. |
| Repaso | S05 amplía sólo su razón; F01–F15/S04–S07 conservan **19 IDs**. F06–08/F15 y sus recursos no cambiaron; enlaces se revalidaron. |
| Navegación | **157 enlaces locales**, incluidos los cuatro nuevos; **0 fallas**, U4/U6 ahora resueltos. Sólo navegación, no auditoría académica de otras unidades. |
| Compatibilidad | **37/37 anclas históricas** presentes:30 pilotos + 7 índice; ambos stubs/índice sin modificaciones. |
| Tablas | **38** con columnas consistentes; UTF-8 sin caracteres de reemplazo y delimitadores de bloque matemático balanceados. |
| Integridad | **286 originales/caches** iguales al snapshot inicial; **291 archivos de sólo lectura** iguales antes/después incluyendo síntesis, snapshot e informes. Cuatro PNG y siete SVG del paquete U2 siguen intactos. |

Contraste visual nuevo del ciclo: **siete páginas originales** (U2 43/44, UT15, BB16, Castro148,
TP2 2/3), además de la lectura de la misión capturada. Poppler advirtió fuentes Symbol/ArialUnicode
en algunos originales; los elementos concretos usados en los siete renders se pudieron inspeccionar.
No se reconstruyeron figuras históricas como si fueran autoridad ni se reemplazaron sus bytes.

## Límites conservados / siguiente puerta

- No se convirtió en revisión propia integral la cobertura de 158 páginas declarada por los dictámenes.
  Este ciclo verifica cambios dirigidos y regresión, no todo el programa ni toda la biblioteca.
- Se conservan pendientes legítimos: difusión/conductor-dieléctrico sin desarrollo registrado,
  PSD/BER y B6ZS sin condiciones corroboradas, límites OEM poco legibles. No se evalúan como hechos.
- URL/videos no reproducidos; DOC/XLSX/ZIP/RAR auxiliares no usados; páginas bibliográficas ajenas
  y contenidos remitidos a otras unidades no se certifican. No se garantiza render tipográfico en todos los visores.
- Ningún simulacro/pregunta nuevo; no se alteraron fuentes, caches, informes ni snapshot inicial.
- **Pendiente:** revisión independiente de estos cierres y aceptación raíz. Tras entregar este ciclo,
  U2 queda congelada hasta nueva orden; no se cambia a `revisado`/final.

## Key Learnings:

1. La convención 2B1Q debe declararse junto a la figura: otra asignación no es necesariamente inválida,
   pero no puede usarse para controlar signos de una tabla diferente.
2. Un cero informativo, falta de actividad y recuperación de reloj son tres cosas distintas;
   detectar presencia necesita un criterio temporal y de nivel compatible con el código.
3. La referencia precisa de polar RZ es Castro PDF148/impresa122 §2.8.5.4/fig.2.43.
