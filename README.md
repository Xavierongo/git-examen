Git nuestro
Git nuestro que estas en los repos
Comprimidos sean tus commits
Venga a nosotros tu log
En el local como en el remote
Danos hoy nuestro pull de cada día
Perdona nuestros conflictos
Como también perdonamos los de otros geeks
No nos dejes caer en detached HEAD
y líbranos de SVN
git commit --amend




### Solución ejercicio 1 
## -Qué comando utilizaste el paso 11? ¿Por qué?
Ejecuté este comando porque git reset mueve el puntero de la rama actual al commit anterior, 
y con la opción --hard restablece tanto el staging area como el working copy al estado del commit referenciado. 
HEAD~1 indica el commit previo al actual (en este caso, 662f5d4), lo que elimina definitivamente el último commit del historial y sus cambios asociados.

## -Qué comando o comandos utilizaste el paso 12? ¿Por qué?
En el paso 12, ejecuté git reflog para listar el historial detallado de movimientos del puntero HEAD, lo que me permitió identificar el commit (349505c) que había sido afectado por acciones previas (como resets o cambios de rama).

## - El merge del paso 13, ¿Cuasó algún conflicto? ¿Por qué?
No, el merge del paso 13 no causó conflictos porque la rama `main` no tenía modificaciones en comparación con `styled`. Antes de fusionarlas, realicé `git pull origin main` para asegurarme de que `main` 


## - El merge del paso 19, ¿Cuasó algún conflicto? ¿Por qué?
No, el merge del paso 19 no causó conflictos porque no hubo modificaciones concurrentes en los mismos archivos o líneas de código en ambas ramas. Además,
ningún archivo fue eliminado o movido en una rama mientras se modificaba en la otra. Estas condiciones permitieron que Git realizara la fusión automáticamente sin necesidad de intervención manual.

## - El merge del paso 21, ¿Cuasó algún conflicto? ¿Por qué?
No, el merge del paso 21 no causó conflictos porque la rama main no tenía modificaciones pendientes; al no existir cambios concurrentes en los mismos archivos o líneas de código, la fusión se realizó sin problemas.


## -Qué comando o comandos utilizaste el paso 25? ¿Por qué?
Usé el comando `git log --graph --decorate --all`, que muestra el historial de commits en todas las ramas de forma visual, incluyendo gráficos y etiquetas de las ramas locales y remotas.

## El merge del paso 26, ¿Podria ser fast forward? ¿Por qué?
Podría haber sido fast-forward si main estuviera al día, pero se usó `--no-ff` para forzar un commit que evidencie la fusión.


## -Qué comando o comandos utilizaste el paso 27? ¿Por qué?
Usé el comando `git reset --mixed HEAD^`, que revierte el merge retrocediendo al commit anterior y mantiene los cambios en el working copy como no preparados.

## -Qué comando o comandos utilizaste el paso 28? ¿Por qué?
En el paso 28 se ejecutaron tres comandos: primero, `git restore --staged .` para quitar todos los cambios del área de preparación; luego, `git restore .` para revertir las modificaciones en el directorio de trabajo; y finalmente, `git status` para confirmar el estado actual del repositorio.



## -Qué comando o comandos utilizaste el paso 29? ¿Por qué?
En el paso 29, usé `git branch -D title` para borrar la rama local y, si también quería eliminarla del remoto, `git push origin --delete title`.


## -Qué comando o comandos utilizaste el paso 30? ¿Por qué?
git reflog (para encontrar el hash del merge deshecho)
git reset --hard <hash>

## -Qué comando o comandos utilizaste el paso 32? ¿Por qué?
git checkout <hash-del-primer-commit>
Para volver al commit inicial.
