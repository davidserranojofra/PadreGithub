#Práctica del curso de git, gitHub y Sourcetree
##Ejercicio 1

###1.- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

**git reset —hard HEAD~1** Uso este comando para tirar un commit atrás y con el —hard lo que hago es perder los cambios realizados, si no quisiese perder los cambios lo haría sin el —hard.

--

###2.- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

**git reflog** para listar todos los pasos que hemos realizado y buscar el commit donde de modificó git-nuestro.md y coger su identificador “98a9c06”. 

**git reset —hard 98a9c06** para volver al commit junto con sus cambios(—hard) y posicionando la rama styled apuntando a ese commit y HEAD apuntando a styled.

--

###3.- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué? 

No, porque en este caso la rama *styled* tenia ya toda la información de los commits de la rama *master*.

--
###4.- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? 

Si, porque al hacer el merge, tenia el mismo documento en ambos lados de la rama y las lineas de ambos documentos eran diferentes, así que git usa la famosa política(CYA), y te toca editar el archivo personalmente y decidir que es lo adecuado. 

Pasos a seguir cuando entra en el modo conflicto en este caso:

**nano git-nuestro.md** (modifico y guardo archivo).

**git add git-nuestro.md** (añado archivos al staging area).

**git commit** (añado archivos de staging area al repo).

--
###5.- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué? 

No, lo único que ha echo master es actualizar su rama y en estos momentos es la rama mas actualizada. Realmente todo y que he usado el comando *—no-ff*, asído un merge fast forwar y no dan conflicto nunca ya que son el linea.

--
###6.- ¿Qué comando o comandos utilizaste en el paso 25?

He utilizado el comando **git graph**, que es un *alias* que contiene (log —graph —decorate —pretty=oneline).

--
###7.- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 

Si, ya que se han añadido contenidos nuevos pero no crean conflicto, por lo tanto, seria como si la rama master apuntara al mismo commit de la rama title subiendo un commit hacia arriba.

En nuestro caso(—no-ff) existe un commit nuevo, donde se ha fusionado master con title, un commit por encima de la rama title.

--
###8.- ¿Qué comando o comandos utilizaste en el paso 27? 

**git reset HEAD~1**

-
###9.- ¿Qué comando o comandos utilizaste en el paso 28? 

**git checkout -- git-nuestro.md**, al contrario, si quisiéramos guardar los cambios haríamos un git add y un git commit. 

--
###10.- ¿Qué comando o comandos utilizaste en el paso 29? 

Usé el comando **git branch -d title** y me salto un error diciendo que esta rama aun no se había fusionado, así que forcé la eliminación con el comando **git branch -D title**

--
###11.- ¿Qué comando o comandos utilizaste en el paso 30? 

**git reflog**

**git reset —hard (y el id al que apunto, en mi caso) 552cfce**

--
###12.- ¿Qué comando o comandos usaste en el paso 32?

**git log** (para buscar todos los commit de la rama master y obtener el identificador donde se creo el primer commit).

**git checkout identificador-primer-comit(c61a8f021c652b45b8c78a3e582c0154b619c033)** (para apuntar con HEAD a este commit y obtener el poema en su primera versión). 

--
###13.- ¿Qué comando o comandos usaste en el punto 33? 

**git checkout master** , simplemente apunte HEAD a master ya que el puntero master es el mas avanzado y contiene todas las modificaciones del texto y el título.

---