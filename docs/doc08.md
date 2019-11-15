
# Como crear un HOOK para habilitar un despliegue automatico 

<!---parte de Iñaki---->
al crear en el hook lo primero que tendremos que hacer es crear lo siguiente:
1.  Un script llamado deploy.sh que haga el git pull
2. Un PHP llamado deploy.php que ejecute dicho script

En el deploy.sh estará escrito lo siguiente:




<!-- BOGDDAN -->
* Item 1: Lo priemro que hay que hacer es comprobar si esta o no instalado Git utilizando el comando git --version 

![Repositorio Configuraciones](images/doc8/Screenshot_1.png)x

*   Item 2: Ahora hay que crear la siguiente estructura de carpetas ("/home/<usuario>/repo/dweb.git/")
    y  en la carpeta de dweb.git inicializas la carpeta inicialias Git con git init: 

```bash
    mkdir repo 
    cd repo
    mkdir dweb.git
    cd dweb.git
    git init --bare
```
* Item 3: Ahora hay que crear un archivo que automatiza la actualización del servidor.
    Nota: En realidad lo que haces es forzar a borrar y volver a descargar todos el repositorio de gitHub

    * Item 3a: Creamos el archivo donde definiremos la instrucción
```bash
cd /home/<usuario>/repo/dweb.git/hooks/
nano post-receive
```
Y en achivo ponermo esta instrucción: 
```bash
#!/bin/sh

GIT_WORK_TREE=/home/<usuario>/www/dweb.io git checkout -f
```
El -f por que asi fuerzas a que se realize el comando, ya que si a la hora de bajar todo el repositorio saldrian ventanas de si "estas seguro de que quieres sobreescribir" y el servidor se quedaía sin hacer nada.

Ahora lo guardamos 
```bash
chmod 0775 post-receive
```