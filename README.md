# git-examen

### Solución ejercicio 1 

## -Qué comando utilizaste el paso 11? ¿Por qué?
en Git, se usa git reset --hard HEAD~1, que restablece el repositorio al commit anterior de forma irreversible. Este comando mueve el puntero de la rama,
sincroniza el Working Directory y el Staging Area con el commit objetivo, eliminando cualquier modificación posterior. 
Es crucial usarlo con precaución, ya que borra permanentemente cambios no guardados en commits previos. 
Si se ejecuta por error, puede recuperarse con git reflog y git reset --hard <hash>. 
Como alternativa menos destructiva, se recomienda git revert HEAD, que mantiene el historial al crear un nuevo commit que revierte los cambios.
