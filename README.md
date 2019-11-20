# Respuestas al cuestionario

- **¿Qué comando utilizaste en el paso 11? ¿Por qué?**

$git reset --hard HEAD~1, para volver al commir anterior modificando el working area

- **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

$git reflog para poder ver el commit que he eliminado ya que no aparece con un simple $git log y $git reset --hard <id commit al que quiero llegar>

- **El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**

Conflicto no, pero avisa que master está "Already up to date" ya que está un commit por debajo de styled

- **El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**

Si, porque se ha modificado el mismo archivo en las mismas lineas en el mismo commit

- **El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**

No, al estar master un commit por debajo de styled, se ha actualizado, y al tener styled todos los commits de master, ha sido fast-forward

- **¿Qué comando o comandos utilizaste en el paso 25?**

$git log --graph --pretty=oneline por claridad, para que se vean los commits en una sola linea y el grafo sea más claro

- **El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**

Sí, porque title sólo estaba un commit por delante de master, incluía todos los commits anteriores.

- **¿Qué comando o comandos utilizaste en el paso 27?**

$git reset HEAD~1 para deshacer el merge sin perder los cambios en el working area

- **¿Qué comando o comandos utilizaste en el paso 28?**

$git checkout -- git-nuestro.md para descartar los cambio en working area

- **¿Qué comando o comandos utilizaste en el paso 29?**

$git branch -D title porque al no estar mergeada, -d no sirve

- **¿Qué comando o comandos utilizaste en el paso 30?**

$git reflog (ver el commit al que quiero ir) // $git checkout <id_commit> // $git checkout master // $git branch title <id_commit> (para volver a crear la rama) // $git merge title

- **¿Qué comando o comandos usaste en el paso 32?**

$git log // $git checkout <id_primer_commit>

- **¿Qué comando o comandos usaste en el punto 33?**

$git checkout <id_ultimo_commit>
