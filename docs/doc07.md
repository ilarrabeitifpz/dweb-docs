# 7.Instalar Git y crear repositorio en servidor. Acceder a este repositorio desde cliente.

## Git en Servidor

* **Instala Git**
    * *Comprobar si está instalado ya*
    ![GitHub Logo](images/doc07/Git-Servidor/git-version.PNG)
    <br>
    * *Crea un nuevo repositorio llamado dweb (en tu home)*
        * mkdir repo 
        * cd repo
        * mkdir dweb.git
        * cd dweb.git
        * git init --bare
    ![GitHub Logo](images/doc07/Git-Servidor/repositorio-repo.PNG)
    ![GitHub Logo](images/doc07/Git-Servidor/repositorio-init.PNG)

    * *Crear un HOOK post-receive*
        * cd /home/(usuario)/repo/dweb.git/hooks/
        * nano post-receive
            #!/bin/sh

            GIT_WORK_TREE=/home/<usuario>/www/dweb.io git checkout -f
        * guardalo
        * chmod 0775 post-receive
    ![GitHub Logo](images/doc07/Git-Servidor/hook.PNG)
    ![GitHub Logo](images/doc07/Git-Servidor/hook-nano.PNG)
    ![GitHub Logo](images/doc07/Git-Servidor/hook-chmod.PNG)


## Git en Cliente

* **Descargar e instalar MING**
    * *Editor: Nano*
    ![GitHub Logo](images/doc07/Git-Cliente/git-set-up-editor.PNG)
    <br>
    * *PATH:  Git from the command line*
    ![GitHub Logo](images/doc07/Git-Cliente/git-set-up-PATH.PNG)
    <br>
    * *HTTPS: OpenSSL*
    ![GitHub Logo](images/doc07/Git-Cliente/git-set-up-HTTPS.PNG)
    <br>
    * *Line endings: commit Unix-style*
    ![GitHub Logo](images/doc07/Git-Cliente/git-set-up-line-ending.PNG)
    <br>
    * *Terminal emulator: MinTTY*
    ![GitHub Logo](images/doc07/Git-Cliente/git-set-up-terminal.PNG)
    <br>
    * Extra Options:
        * Enable file system caching
        * Enable Git Credential Manager
    ![GitHub Logo](images/doc07/Git-Cliente/git-set-up-extra-options.PNG)
