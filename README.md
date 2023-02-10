Ejercitacion Final

Primero cree el repositorio desde la pagina Github y luego lo clone a mi maquina con el comando:
```
$ git clone https://github.com/Kiara-Cosentino/devjumpers
```
Con los siguientes comandos creo el archivo README.md, lo modifico, hago el commit y lo subo al repositorio:
```bash
$ touch README.md
$ git add .
$ commit -m "commit inicial"
$ git status 
$ git push
```
Ignorar archivos

primero creo el archivo privado.txt y la carpeta privado de la siguiente manera:
```bash
$ touch privado.txt
$ mkdir privado
```
Posteriormente creo un archivo llamado .gitignore, este le informara a git que tendra que ignorar aquellos archivos que se encuentren en él. 
```bash
$ touch .gitignore
```
Dentro de este ingrese los nombres de los archivos a ignorar (privado y privado.txt) y luego hice el push:
```
$ git add .
$ git commit -m "ignorar archivos"
$ git status
$ git push
```
Añadir fichero 1.txt
Cree el archivo 1.txt con el comando:
```bash
$ touch 1.txt
```
Crear rama v0.2
Cree la rama v0.2 con el comando:
```bash
git branch v0.2
```
Entre a esta rama con el comando:
```bash
$ git checkout v0.2
```
Y alli cree un archivo 2.txt:
```bash
$ touch 2.txt
```
Para subirlo utilice los siguientes comandos:
```bash
$ git add .
$ git commit -m "creacion de archivo txt en la rama v0.2"
$ git push
```
Me tiro un error que solucione utilizando el comando que me especificaba la consola:
```bash
$ git push --set-upstream origin v0.2
```
Merge directo
Me posiciono en la rama Main con el comando:
```bash
$ git checkout main
```
Y luego hago el merge con la rama v0.2 de esta manera:
```bash 
$ git merge v0.2
```
Merge con conflicto
En el Main agregue la palabra "Hola" en el archivo 1.txt y le hice un commit:
```bash
$ echo "Hola" > 1.txt
$ git add 1.txt
$ git commit -m "Agregado HOLA al archivo 1.txt en Main"
```
Despues me dirigi a la rama v0.2 y escribi "Adios" en el archivo 1.txt:
```bash
$ git checkout v0.2
$ echo "Adios" > 1.txt
$ git add 1.txt
$ git commit -m "Agregado ADIOS al archivo 1.txt en v0.2"
```
Para hacer el merge me posiciono en la Main y utilizo los comandos:
```bash 
$ git checkout main
$ git merge v0.2
```
La consola me tira el siguiente error: 
```bash
Auto-merging 1.txt
CONFLICT (content): Merge conflict in 1.txt
Automatic merge failed; fix conflicts and then commit the result.
```
Listado de ramas
Con el siguiente comando veo aquellas ramas que han sido fusionadas correctamente: 
```bash
$ git branch --merged
```
Y con este, aquellas que no hayan sido fusionadas: 
```bash
$ git branch --no-merged
```
Como resultado obtengo que la rama Main esta fusionada pero la v0.2 no lo esta. 
Para resolver esto, modifico el archivo 1.txt manualmente dejando unicamente las palabras "Hola" y "Adios".
Para actualizar la iformacion uso lo siguiente:
```bash
$ git add .
$ git commit -m "conflicto resuelto" 
```
Y para verificar si ambas ramas estan bien fusionadas:
```bash
$ git branch --merged
``` 
Lo que me arroja que Main y v0.2 han sido mergeadas correctamente. 
Finalmente elimino la rama con:
```bash 
$ git branch -D v0.2
```
Listado de cambios
Para visualizar todos los commits realizados hasta ahora utilizo:
```bash
$ git log --oneline --decorate --all --graph
```
Lo que me arroja el siguiente resultado:
```bash
$ git log --oneline --decorate --all --graph
*   a5cdc7a (HEAD -> main) conflicto resuelto
|\
| * 3b1b54c Agregado ADIOS al archivo 1.txt en v0.2
* | 7f54c04 agregado HOLA al archivo 1.txt en Main
|/
* 9d4580d (origin/v0.2) creacion de archivo txt en rama v0.2
* 1cc414c (origin/main) ignorar archivos
* a1bc7a8 commit inicial
```
Crear una tabla
| NOMBRE | GITHUB |
| -- | -- |
| Ivan de la Parte | [Ivan](https://github.com/ivandelaparte/devjumpers)
| Maria Arteaga | [maryjse](https://github.com/maryjse)
| Armando Torres Quintana | [ArmaTQ](https://github.com/ArmaTQ)
| Leandro Cuevas | [leandro-cuevas](https://github.com/leandro-cuevas)
| Franco Formigo | [francobenjaminformigo](https://github.com/francobenjaminformigo)

Colaborador: Ivan de la Parte. 