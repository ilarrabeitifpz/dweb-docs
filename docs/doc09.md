# comandos de git en cliente

### Inicio

![Git config --global](images/doc09/Config.png)

Antes de nada, tendremos que iniciar sesión con un usuario git config --global

###Iniciar repositorio

Cuando empezamos a trabajar en github podemos hacerlo desde un repositorio creado por nosotros o desde un repositorio remoto, creado por otro usuario.

En el caso de que queramos trabajar desde un repositorio nuestro tendremos que crearlo mediante el código:

![Git config --global](images/doc09/init.png)

La otra opción es trabajar en otro repositorio. Mediante el git clone, pasará todo lo que haya en el repositorio a nuestra carpeta.

![Git clone](images/doc09/clone.png)

### Ramas

Las ramas son una de las partes más importantes del trabajo, es el lugar en el que estás trabajando y valen para que los cambios no afecten tanto al proyecto del repositorio. las ramas en git se llaman "branch" y existen dos tipos: el "master" que es el más importante, una vez que haga push, los cambios se suben inmediatamente. En el caso de que no queramos subirlo directamente, podemos crear ramas que partan de esa rama master que lo que hará es mandarle una advertencia al master para poder subir los cambios; en dicha advertencia, el master podrá vez qué cambios quiere subir y podrá elegir si aceptarlas o no.

Para crear estas ramas, tenemos que escribir el comando:

![Git branch-name](images/doc09/branch-name.png)

Una vez creada la rama, tendremos que entrar en esa rama con el comando siguiente

![Git checkout](images/doc09/checkout.png)

una vez entrado en la rama y hayamos terminado el trabajo o hayamos avanzado mucho, la rama hace push y el master mediante 

![Git merge](images/doc09/merge.png)

En cuanto hayamos subido los cambios borraremos la rama con el comando

![Git -d](images/doc09/delete.png)

### Sincronizar cambios

Estos comandos son los comandos que utilizaremos para poder sincronizar nuestro repositorio local con el remoto.

Antes de subir los cambios de una rama, tendremos que comparar ambos proyectos (el del github y el de la rama) para ver si podría crear conflictos los cambios de la rama

![Git fetch](images/doc09/fetch.png)

En el caso de que queramos comparar dos ramas usaremos este otro comando:

![Git diff](images/doc09/diff.png)

Una vez comparados los dos proyectos, haremos git merge para juntar lo que se ha hecho en la rama con el proyecto.

![git Merge](images/doc09/GitMerge.png)

Para poder subir todo lo que tenemos en la rama master de nuestro repositorio local, tendremos que utilizar el comando "push" en el terminal, pero antes que nada, vamos a traer todo lo que haya en el repositorio remoto a nuestro repositorio local para no borrar los cambios que han hecho nuestros compañeros. Para eso, utilizaremos el comando pull en el terminal
##### pull

![git Merge](images/doc09/pull.png)

##### push

![git Merge](images/doc09/push.png)

### Hacer cambios

Para poder subir nuestros cambios tendremos que utilizar el comando "commit". Mediante este comando lo meteremos en nuestro repositorio local para luego posteriormente subirlo con push.

Al igual que tú haces tus cambios, tus compañeros también lo pueden hacer; por eso, git te da la posibilidad de ver los commits que habéis subido al repositorio de gitHub.

![git Merge](images/doc09/gitlog.png)

Hay tantos comandos diferentes que puedes utilizar con el log... aquí tienes unos cuantos útiles


![git Merge](images/doc09/gitlogPretty.png)

###### Poner los últimos 

![git Merge](images/doc09/gitlogMaxAcount.png)

![git Merge](images/doc09/gitlogDate.png)

[Más información](https://githowto.com/history)