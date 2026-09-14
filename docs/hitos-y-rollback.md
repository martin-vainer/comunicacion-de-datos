# Hitos y rollback seguro

El punto de partida verificable está documentado en
[`respaldo-pre-harness-v1.md`](respaldo-pre-harness-v1.md) y marcado por el tag
`respaldo/pre-harness-v1`.

## Hitos

| Orden | Commit | Responsabilidad |
|---|---|---|
| 0 | `780cf0e` | Checkpoint previo al refactor, marcado con `respaldo/pre-harness-v1` |
| 1 | `d4fa40f` | Harness académico mínimo: flujo, plantillas y reglas |
| 2 | `944a52a` | Piloto contrastado de Fourier y ancho de banda |
| 3 | `56fb1e9` | Traslado sin cambios de las 14 capturas y sus 85 PNG asociados |
| 4 | `ee66ef7` | Bitácora completa, índices y enlaces hacia la capa histórica |
| 5 | `f513715` | Extracción canónica del ejercicio 19 y navegación U6/U7 |
| 6 | `ff123f1` | Registro de hitos y procedimiento de rollback seguro |

La tabla congela los hitos funcionales de la implementación v1. Una corrección documental posterior
puede no figurar en ella; antes de revertir, el comando de la sección siguiente muestra la secuencia
real completa y debe tomarse como autoridad.

Para obtener los hashes reales sin depender de este documento:

```powershell
git log --oneline --decorate respaldo/pre-harness-v1..HEAD
```

## Inspeccionar y revertir

Primero confirmar el estado y revisar el rango:

```powershell
git status --short
git diff respaldo/pre-harness-v1..HEAD
```

Para deshacer toda la implementación y volver al checkpoint, revertir **de lo más nuevo a lo más
antiguo**. Primero obtener la lista real; `git log` ya la muestra en el orden correcto para revertir:

```powershell
git log --format="%h %s" respaldo/pre-harness-v1..HEAD
```

Revertir primero cualquier corrección posterior que aparezca arriba de `ff123f1`. Luego continuar con
los hitos v1 conocidos. Ejecutar un comando por vez, revisar el resultado y continuar sólo con el
árbol limpio:

```powershell
git revert ff123f1
git revert f513715
git revert ee66ef7
git revert 56fb1e9
git revert 944a52a
git revert d4fa40f
```

Para deshacer sólo una etapa, comenzar por su commit más nuevo y detenerse antes del hito que se desea
conservar. No revertir `56fb1e9` mientras sigan vigentes `ee66ef7` o `f513715`, porque sus índices
enlazan rutas bajo `capturas/`.

Cada reversión crea un commit auditable y conserva la historia. No usar `git reset --hard`. Ante un
conflicto, abortar ese intento con `git revert --abort`, inspeccionar el estado y resolverlo de manera
explícita; no borrar archivos para forzar la reversión.

El checkpoint y sus tags son locales: no sustituyen un respaldo externo ni un remoto actualizado.
