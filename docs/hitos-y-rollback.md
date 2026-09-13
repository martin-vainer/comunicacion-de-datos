# Hitos y rollback seguro

El punto de partida verificable está documentado en
[`respaldo-pre-harness-v1.md`](respaldo-pre-harness-v1.md) y marcado por el tag
`respaldo/pre-harness-v1`.

## Hitos

| Orden | Commit | Responsabilidad |
|---|---|---|
| 0 | checkpoint `780cf0e` | Preservación previa al refactor |
| 1 | `docs: incorpora harness academico minimo` | Flujo, navegación, plantillas y reglas |
| 2+ | commits posteriores | Piloto y migraciones por lotes, separados del harness |

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

Para deshacer hitos, usar `git revert <hash>` desde el commit más nuevo hacia el más antiguo. Cada
reversión crea un commit auditable y conserva la historia. No usar `git reset --hard`.

El checkpoint y sus tags son locales: no sustituyen un respaldo externo ni un remoto actualizado.
