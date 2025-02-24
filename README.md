# git-examen

### Solución ejercicio 1 

## -Qué comando utilizaste el paso 11? ¿Por qué?
en Git, se usa git reset --hard HEAD~1, que restablece el repositorio al commit anterior de forma irreversible. Este comando mueve el puntero de la rama,
sincroniza el Working Directory y el Staging Area con el commit objetivo, eliminando cualquier modificación posterior. 
Es crucial usarlo con precaución, ya que borra permanentemente cambios no guardados en commits previos. 
Si se ejecuta por error, puede recuperarse con git reflog y git reset --hard <hash>. 
Como alternativa menos destructiva, se recomienda git revert HEAD, que mantiene el historial al crear un nuevo commit que revierte los cambios.

## -Qué comando o comandos utilizaste el paso 12? ¿Por qué?
En el paso 12, utilicé git reflog para listar el historial reciente de movimientos del puntero HEAD, identificando el commit que deshice previamente (b20eef1 en HEAD@{1}). 
Luego, ejecuté git reset --hard b20eef1 para restaurar el estado del repositorio a ese commit, revirtiendo así la acción del paso 11 y asegurando que el historial y los cambios vuelvan a estar en su lugar.

## - El merge del paso 13, ¿Cuasó algún conflicto? ¿Por qué?

No, el **merge del paso 13 no causó conflictos** porque la rama `main` no tenía modificaciones en comparación con `styled`. Antes de fusionarlas, realicé `git pull origin main` para asegurarme de que `main` 
estuviera actualizada con los últimos cambios del repositorio remoto. Como `styled` contenía los cambios y `main` no tenía modificaciones concurrentes, Git pudo integrar los cambios automáticamente sin generar conflictos.

## - El merge del paso 19, ¿Cuasó algún conflicto? ¿Por qué?

No, el **merge del paso 19 no causó conflictos** porque no hubo modificaciones concurrentes en los mismos archivos o líneas de código en ambas ramas. Además,
ningún archivo fue eliminado o movido en una rama mientras se modificaba en la otra. Estas condiciones permitieron que Git realizara la fusión automáticamente sin necesidad de intervención manual.
