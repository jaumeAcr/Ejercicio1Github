1) He utilizado el comando git reset --hard HEAD~1. Lo he utilizado porque
con este comando puedo deshacer un commit, y con --hard también se perderán 
los cambios en mi working copy. Con HEAD~1 indico que quiero ir al commit 
anterior al commit en el que me encuentro. Así, una vez ejecutado el comando 
me encontraré en el commit anterior al que estoy deshaciendo, que es el commit
 en el que creaba el archivo poem.md y lo subía al repositorio.

2) He utilizado los comandos git reflog y git reset --hard 117b889. El 
primero lo he utilizado para averiguar el hash único que identifica a cada 
commit y así poder dirigirme a él mediante la función git reset --hard 117b889
. De esta manera el contenido del working copy se modifica y vuelvo a estar
 como si no hubiese realizado el commit del paso 11 del ejercicio.

3) El merge del paso 13 no causa ningún conflicto ya que cuando ejecuto el 
comando git merge master, me indica "Already up-to-date". Esto quiere decir 
que ya está actualizada ya que tanto la rama master como la rama htmlify 
apuntan al mismo commit y por tanto no hay ningún merge que hacer.

4) Si, el merge del paso 19 causó un conflicto. Porqué he modificado el 
contenido del mismo archivo en dos ramas diferentes. 
Entonces para evitar problemas git no ejecuta el merge, nos indica que debemos
 de solucionar los conflictos y despues hacer un commit, y así se podrá acabar
 de realizar el merge correctamente.

5) No, el merge del paso 21 no causó ningún conflicto. Porqué la rama master 
se encuentra en el commit "abuelo" del commit en el que se encuentra la rama 
htmlify. Por tanto cuando se hace el merge la rama master solo tiene que 
avanzar hasta el commit donde se encuentra la rama htmlify. El contenido del 
working copy solo se tiene que actualizar. Es fast-forward porque puede 
avanzar sin tener que crear un nuevo commit.

6) Utilicé el comando git log --graph --decorate

7) Si podría ser fast-forward, ya que la rama title apunta a un commit hijo de 
un commit al que apunta la rama master. En él hemos añadido un título, por 
tanto no se perdería el trabajo de la rama master haciendo el merge con fast-
forward.

8) Utilicé el comando git log para ver que commit era el anterior al commit 
en el que me encontraba, ya que me encontraba en el commit resultado de hacer 
el merge. Luego con git reset HEAD~1, me desplazaba al commit anterior y no 
modificaba el working copy ya que no ponía --hard.

9) Utilicé el comando git checkout -- poem.md

10) Utilicé el comando git branch -D title

11) Utilicé el comando git reset --hard 84eacbf.

12) Utilicé el comando git log para averiguar el hash del commit inicial y el 
comando git reset --hard <hash_del_commit> para volver al commit inicial.

13) Utilicé comando git reflog para averiguar el hash del commit final donde
 añadimos un título al poema, y a continuación el comando git reset --hard 
<hash_del_commit> para volver al commit cuando añadimos el título al poema.
 
