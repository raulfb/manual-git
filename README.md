# manual-git

## Comandos git en local

git init empieza en esa carpeta un repositorio.

git add nombrearchivo.txt añades a staging(estado temporal, memoria ram) el archivo

git rm nombrearchivo remueves el archivo de staging

git rm --cached nombrearchivo

git commit -m "numero de version" Envia los datos a la base de datos del sistema de control de versiones.

git add . agregas todos los archivos que hayan cambiado al respositorio.

git status ver estado cambios realizados.

git show muestra todos los cambios (un historico de cambios)

git show nombrearchivo muestra todos los cambios realizados en un archivo.

git log nombrearchivo ver historia entera de un archivo.

git log ver historial de cambios 

git log --stat mestra mas informacion que git log

git log --all --graph ver info repo donde puedes ver las ramas representadas visualmente

git log --all --graph --decorate --oneline muestra la info de una forma mucho mas visual

git push subir archivo a otro repositorio remoto

git pull traer archivo de un repositorio

git checkout trae los cambios del repositorio a local.

git checkout master nombrearchivo trae la version actual

git checkout tag nombrearchivo trae la version del commit de un determinado archivo

### Configuraciones

git config --global user.name "Nombre de usuario"
git config --global user.email "email del usuario"

git config --list ver el nombre de usuario y el email
git config --list --show-origin ver archivo donde se guarda el email y el nombre de usuario

merge sirve para unir dos ramas

git diff tag tag para comparar dos commits (el primero con el segundo) (el tag lo sacamos con git log nombrearchivo)

git reset tag --hard Volver al estado de un determinado commit(borra todo de git log, es muy fuerte)

git reset tag --soft Volver al estadod e un determinado commit pero los cambios que esten en staging siguen ahí.

git diff sirve para ver las diferencias 

## Comandos con repositorios remotos.

git clone https://github.com/raulfb/Minijuego-pokemon.git Clona el repositorio remoto en local

git push enviar datos al repositorio remoto

git fetch traer datos del repositorio remoto al local(no lo copia en los archivos)

git merge fusiona

git pull Sincroniza los datos del repositorio remoto con el local(fusiona fetch y merge)

git branch desarrollo Crea la rama/branch desarrollo.

git checkout desarrollo Sirve para cambiarme a la rama de desarrollo.

git branch ver listado de ramas branches

git merge desarrollo fusionar ambas ramas (ejecurtar desde master)

git push --set-upstream origin development


## hithub

git remote add origin direccionrepositorio 

git remote -v ver direcciones repositorios (fetch trar push enviar)

git remote set-url origin urlrepo cambiar url del repositorio de github

git tag -a v0.1 -m "texto para el tag" referenciacommit Crear un tag

git tag lista los tags creados 

git show-ref --tags ver a que commit esta referenciado cada tag

git push origin --tags Subir los tags al repo remoto

git tag -d nombretag eliminar el tag

git push origin :refs/tags/nombretag elimina el tag de la interfaz grafica de github.

git show-branch --all muestra informacion de los cambios hechos en cada rama .
git push origin rama1 envia la rama de nombre rama1 al repo remoto.

## Git rebase

git rebase experimento se pega la historia a la rema master
git rebase master 
(Esto sirve para recoger todos los cambios comfirmados en un rama y ponerlos en la otra.)

## Git stash

git stash guardamos un estado temporal
git stash list muestra una lista de los stash que tenemos.
git stash pop recuperamos los cambios guardados en stash.
git stash branch nombrerama guarda los cambios del stash en una rama.
git stash drop para borrar el stash.

## Git clean 

git clean --dry-run lista el listado de archivos que va a borrar.
git clean -f borrar los archivos que se han listado anteriormente.
git clean -f nombrearchivo borra el archivo que deseamos.

git cherry-pick hash Para trarse un determinado commit

git commit --amend guarda los cambios en el ultimo commit

git reflog Muestra una lista de todo el historial de commits, cada uno con su hash y HEAD

## busquedas

git log --all --grep='aaa' busca la palabra aaa en el historico de commits
git grep -n palabra muestra en la linea que esta lo que estamos buscando
git grep -c nos muestra cuentas veces se repite una palabra y en que archivos está

git shortlog muestra el historico de commits hechos por cada usuario

git config --global alias.nombrealias "Comando que queremos ejecutar"

git branch -a ver todas las ramas (las locales se pintan de blanco, en la que estas de verde y las remotas de rojo)
