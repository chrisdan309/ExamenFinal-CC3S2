# Examen final
## Parte 1
### Pregunta 1
La pregunta uno nos pide producir un conflicto de fusión (merge) utilizando algún repositorio de las actividades realizadas.

Para ello previamente debemos tener unas dos ramas creadas las cuales harán los cambios en los mismos archivos.

Utilizando el comando `git checkout -b <nombre_de_ la rama>` creamos una nueva rama.

![Creacion_branch_1](image.png)

Relizamo los mismos pasos para crear el segundo branch

![Creacion_branch_2](image-1.png)

Podemos verificar los branch creados al utilizar el comando `git branch`

![look_branch](image-2.png)

En esa captura podemos visualizar los branch que contiene nuestro repositorio, siendo estos `main`, `PRIMER_BRANCH`, `SEGUNDA_BRANCH`

Lo que vamos a realizar es editar el archivo readme desde ambas branch agregando `Hola desde <número-del_branch> branch`

Los pasos que vamos a realizar son los siguientes:

![Alt text](image-3.png)

En el archivo README, el cual usaremos para generar el problema de fusión, vamos a colocar mensajes diferentes de diferentes branch.

En este caso utilizamos `echo "Hola dede el primer branch" > README.md` para editar el archivo.

Luego con el comando `cat README.md` visualizamos el interior del mismo.

Finalmente utilizamos los comandos de git para finalmente realizar un push a esa rama utilizando lo comandos `add`, `commit`, `push`. Tener en cuenta que en el comando push utilizamos el como argumentos el remote y la branch, en este caso `origin`, dónde está alojado nuestro repositorio y `PRIMER_BRANCH` que es la rama donde estamos.

Luego de haber realizado el push con éxitos vamos a realizar el cambio en la `SEGUNDA_RAMA`

![Alt text](image-4.png)

![Alt text](image-5.png)

Siguiendo los pasos realizados de la edición del archivo, el visualizarlo, y los comandos de git para agregar, commitear y pushear

![Alt text](image-6.png)

Luego cambiamos al `PRIMER_BRANCH` y realizamos el merge del `SEGUNDA_BRANCH` al primero utilizando el comando merge

> [!NOTE]
> Mientras seguía avanzando con la explicación me di cuenta que estaba generando un merge conflict al editar mismos archivos en lugar del `Non-fast-forward (error)`, por lo cual se cambió el enfoque y se tuvieron que solucionar ambos conflictos que ahora serán explicados, por lo cual se procederá a generar el `Non-fast-forward (error)` en la rama `PRIMER_BRANCH`


Vamos realizar cambios desde otro directorio sin realizar el pull en uno de ellos, así no estará actualizado.

![Alt text](image-7.png)

Desde otro directorio en el mismo branch realizamos cambios para obtener el conflicto

![Alt text](image-8.png)

En ambos direcctorios podemos visualizar utilizando pwd que estamos en diferentes directorios.

Pra solucionarlo debemos traer los cambios con un git pull pero nos dirá el siguiente mensaje.

![Alt text](image-9.png)

Por lo tanto agregamos `git pull --rebase origin PRIMER_BRANCH` 

![Alt text](image-10.png)

Ahora tenemos que indicar como se realizará el rebase, en este caso utilizando --skip resolverá los problemas y podremos realizar el push.

![Alt text](image-11.png)

### Pregunta 2





## Parte 2
Utilizando el repositorio brindado se realizará la siguiente actividad.

El objetivo de esta actividad es crear un controlador que reciba la solicitud del usuario y un modelo que llama al servicio TMDb remoto para obtener información de la película-

