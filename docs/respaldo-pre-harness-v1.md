# Respaldo previo al harness v1

Este documento describe el checkpoint local tomado antes de implementar el harness académico o reorganizar apuntes.

## Alcance

- Rama de origen al relevar: `main`.
- Commit base previo al checkpoint: `7e9c4558899db16eeb12e76670f01b9270f9ed89`.
- Archivos preexistentes inventariados: 162.
- Archivos incluidos en el checkpoint: 160 (174,77 MiB).
- Adjuntos PNG incluidos: 86.
- Documentos PDF incluidos: 33.
- Archivos Markdown incluidos: 21.
- Inventario con estado inicial, tamaño y SHA-256: [inventario-pre-harness-v1.csv](inventario-pre-harness-v1.csv).
- Manifiesto verificable: [sha256-pre-harness-v1.txt](sha256-pre-harness-v1.txt).

El inventario representa los archivos que existían antes de agregar esta documentación. Los tres archivos de `docs/` creados para el checkpoint quedan incluidos en el propio commit, aunque no se autocontabilizan en el manifiesto.

## Revisión de seguridad y exclusiones

Se revisaron nombres de archivo y archivos de texto mediante patrones comunes de credenciales (`api key`, `secret`, `password`, `token`, claves privadas y equivalentes). No se detectaron credenciales. Las coincidencias con «Token Ring» son terminología académica, no secretos.

Única exclusión:

- `tmp/pdfs/ej19.png` y `tmp/pdfs/ej19-p3.png`: renders auxiliares de inspección, registrados con hash en el inventario pero excluidos de Git mediante `/tmp/`.

No se excluyó contenido académico. Se preservan los originales, los apuntes, las imágenes y también los paquetes comprimidos aunque parte de su contenido esté extraído; cualquier deduplicación futura deberá hacerse después del checkpoint y en un commit separado.

## Restauración controlada

El tag anotado `respaldo/pre-harness-v1` identifica el estado completo del checkpoint. Para inspeccionarlo sin modificar el trabajo actual:

```powershell
git show respaldo/pre-harness-v1
git diff respaldo/pre-harness-v1..HEAD
```

Para revertir cambios posteriores, crear commits inversos con `git revert` desde el más nuevo al más antiguo. No usar `git reset --hard`. Este checkpoint es local y no reemplaza un respaldo externo mientras no exista un remoto actualizado.
