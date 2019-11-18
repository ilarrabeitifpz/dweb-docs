# 7.Instalar Git y crear repositorio en servidor. Acceder a este repositorio desde cliente.

## Git en Servidor

* **Instala Git**
    * *Comprobar si está instalado ya*
    ![GitHub Logo](images/doc07/Git-Servidor/git-version.PNG)
    
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
    
    * *PATH:  Git from the command line*
    ![GitHub Logo](images/doc07/Git-Cliente/git-set-up-PATH.PNG)
    
    * *HTTPS: OpenSSL*
    ![GitHub Logo](images/doc07/Git-Cliente/git-set-up-HTTPS.PNG)
    
    * *Line endings: commit Unix-style*
    ![GitHub Logo](images/doc07/Git-Cliente/git-set-up-line-ending.PNG)
   
    * *Terminal emulator: MinTTY*
    ![GitHub Logo](images/doc07/Git-Cliente/git-set-up-terminal.PNG)
    
    * Extra Options:
        * Enable file system caching
        * Enable Git Credential Manager
    ![GitHub Logo](images/doc07/Git-Cliente/git-set-up-extra-options.PNG)

* **Crea un espacio de trabajo para el proyecto DWEB**
    * Abre el terminal (MINGW) en tu espacio de trabajo.
        ![GitHub Logo](images/doc07/Git-Servidor/git-clone-git-bash.PNG)
    
    ![GitHub Logo](images/doc07/Git-Servidor/git-bash-here.PNG)
    
    * Haz un clon de tu repositorio: git clone (usuario)@(ip)):/home/(usuario)/repo/dweb.git
        ![GitHub Logo](images/doc07/Git-Servidor/git-cloned.PNG)
    
    * Crea un contenido (index.html) para tu proyecto y (usando comandos de Git) súbelo al repositorio
        ![GitHub Logo](images/doc07/Git-Servidor/index-html.PNG)
    * Configura tu usuario A NIVEL DE REPOSITORIO con git config --local user.name "User".... etc...
        ![GitHub Logo](images/doc07/Git-Servidor/git-cofig-usuario.PNG)


    

