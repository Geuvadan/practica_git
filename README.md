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



--#--#--#--#--#--#--#--#--#--#--#--#--#--#--

# Pasos llevados a cabo uno a uno

	1. $git init
	2. $nano git-nuestro.md
	3. $git add git-nuestro.md
	4. $git commit -m "Añado el archivo git-nuestro.md"
	5. $git branch styled
	6. $git branch
	7. $git checkout styled
	8. $git branch
	9. $nano git-nuestro.md
	10. $git add git-nuestro.md // $git commit -m "Modificación realizada a git-nuestro.md"
	11. $git reset --hard HEAD~1
	12. $git reflog // $git reset --hard <id anterior>
	13. $git merge master (already up tu date)
	14. $git checkout master
	15. $git branch htmlify
	16. $git checkout htmlify
	17. $nano git-nuestro.md
	18. $git add git-nuestro.md // $git commit -m "Modifico git-nuestro.md en htmlify"
	19. $git checkout styled // $git merge htmlify 
	20. (conflicto resuelto editando git-nuestro.md) // $git add git-nuestro.md // $git commit -m "Conflicto resuelto al hacer merge de htmlify en styled"
	21. $git checkout master // $git merge styled
	22. $git branch title // $git checkout title
	23. $nano git-nuestro.md // $git add git-nuestro.md // $git commit -m "Añado un título"
	24. $git checkout master
	25. $git log --graph --pretty=oneline
	26. $git merge --no-ff title
	27. $git reset HEAD~1
	28. $git checkout -- git-nuestro.md
	29. $git branch -D title
	30. $git reflog (ver el commit al que quiero ir) // $git checkout <id_commit> // $git checkout master // $git branch title <id_commit> // $git merge title
	31. (ya estoy en master) // $git branch -d htmlify // $git branch -d styled // $git branch -d title
	32. $git log // $git checkout <id_primer_commit>
	33. $git checkout <id_ultimo_commit>
	34. $git reflog // $git checkout <id_primer_commit> // $git tag inicial // $git checkout <id_paso10> // $git tag styled // $git checkout <id_paso18> // $git tag htmlify // $git checkout <id_paso30> // $git tag title
git checkout hmlify



--------- Subir el repo -------- 

Creado repo vacío en Github

	1. $git remote add origin <url>
	2. $git push origin master
	3. $nano README.md
	4. $git add README.md
	5. $git commit -m "subo el archivo README.md"
