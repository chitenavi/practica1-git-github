# Práctica del curso de git, gitHub y Sourcetree

## Ejercicio 1

-  **¿Qué comando utilizaste en el paso 11? ¿Por qué?**

   > ```ps
   > git reset --hard HEAD~1
   > ```
   >
   > Con _git reset_ deshacemos los commits, _--hard_ hace que modifique también el working copy al estado del commit anterior y con _HEAD~1_ nos referimos al commit justo anterior

-  **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

   > ```ps
   > git reflog
   > git reset --hard "hash"
   > ```
   >
   > Con _git reflog_ buscamos el "hash" del commit que hemos eliminado y con él restablecmos

-  **El merge del paso 13, ¿Causó algún conﬂicto? ¿Por qué?**

   > ```ps
   > git merge master
   > ```
   >
   > No hay conflicto, **git** devuelve el mensaje _Already up to date_. Viene a decir que los cambios que queremos ya los tenemos hechos, porque intentamos hacer un merge del hijo hacia el padre.

-  **El merge del paso 19, ¿Causó algún conﬂicto? ¿Por qué?**

   > ```ps
   > git checkout styled
   > git merge htmlify
   > ```
   >
   > Si hay conflicto, porque en ambas ramas hay diferentes versiones del _git-nuestro_. Editamos y nos quedamos con _styled_

-  **El merge del paso 21, ¿Causó algún conﬂicto? ¿Por qué?**

   > ```ps
   > git checkout master
   > git merge styled
   > ```
   >
   > No hay conflicto, se produce un _merge ff_ ya que _master_ está en la misma bifurcación y es el "abuelo" de _styled_.

-  **¿Qué comando o comandos utilizaste en el paso 25?**

   > ```ps
   > git log --graph
   > ```

-  **El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**

   > Si podría ser _ff_ porque _master_ es el padre de _title_, _master_ avanzaría hasta _title_ y para este caso, al contrario que el ejecutado, no crearía un nuevo commit.

-  **¿Qué comando o comandos utilizaste en el paso 27?**

   > ```ps
   > git reset HEAD~1
   > ```

-  **¿Qué comando o comandos utilizaste en el paso 28?**

   > ```ps
   > git restore .\git-nuestro.md
   > ```

-  **¿Qué comando o comandos utilizaste en el paso 29?**

   > ```ps
   > git branch -D title
   > ```

-  **¿Qué comando o comandos utilizaste en el paso 30?**

   > ```ps
   > git reflog
   > git reset --hard "hash"
   > ```
   >
   > Con _reflog_ busco el "hash" del _merge_ y con este lo restauramos

-  **¿Qué comando o comandos usaste en el paso 32?**

   > ```ps
   > git log
   > git reset --hard "hash"
   > ```
   >
   > Con _log_ busco el "hash" del primer commit y restablecemos _master_ ahí.

-  **¿Qué comando o comandos usaste en el punto 33?**

   > ```ps
   > git reflog
   > git reset --hard "hash"
   > git log
   > ```
   >
   > Con _reflog_ busco el "hash" del _merge_ del título y restablecemos _master_ ahí. Compruebo con _log_ que está todo bien
