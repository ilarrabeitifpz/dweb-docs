# 10. Desplegar proyecto privado alojado en GitHub en nuestro servidor público en GUEBS.
Estos son los pasos a seguir:

  - [Configurar Acceso SSH mediante clave publica-privada del servidor al repositorio GitHub](#configurar-acceso-ssh-mediante-clave-publica-privada-del-servidor-al-repositorio-github)
    1. [En nuestro servidor](#en-nuestro-servidor)
    2. [En GitHub](#en-github)

## Configurar Acceso SSH mediante clave publica-privada del servidor al repositorio GitHub

### 1. En nuestro servidor
Para conocer los **datos de acceso SSH** del servidor en GUEBS debes accede al **panel de control** de GUEBS Haz click ahí:
   
![Panel de Control](images/doc10/doc10-panel-de-control-guebs.png =100)
    
Copia los datos de conexión:
   
![Datos de conexión SSH](images/doc10/doc10-panel-de-contro-datos-de-acceso-ssh.png | width=100)

Si no recuerdas la contraseña del usuario SSH puedes poner una nueva pulsando en `Definir contraseña`

Abre un programa de **terminal** de linea de comandos que permita ejecutar el comando SSH. (OpenSSH client, Windows PowerShell o [MINGW](https://www.google.com/search?q=MINGW)) y ejecuta el comando SSH:

    ssh <usuario>@<ip> -p <puerto>

Te pedirá la contraseña.

Una vez conectado al servidor genera las llaves publica y privada mediante el comando `ssh-keygen`. Ponle un **nombre al archivo** pero y no escribas nada cuando te pida la `passphrase`, solamente pulsa Enter.

![Conexión al servidor por ssh](images/doc10/doc10-conectarse-al-servidor-por-ssh.png | width=100)

Esto habrá generado un par de claves publica-privada en el directorio actual. Escribiendo `ls -l` podrás visualizar una lista de los archivos.

![Clave pública y privada](images/doc10/doc10-claves-publica-y-privada.png width=100)

Ejecuta el comando **`cat`** seguido del nombre del archivo de la clave pública para mostrar su contenido, o abre el archivo con un editor como `nano`. Copia el contenido para llevarlo a [GitHub](https://github.com).

### 2. En GitHub
Accede a tu cuenta de GitHub *(con el usuario que te permita ver ese repositorio privado al que intentamos acceder)* y accede a `settings` en el icono de tu perfil.

![](images/doc10/doc10-github-settings.png | width=100)

Después pulsa en la subsección `SSH and GPG keys` y en el apartado **SSH keys** pulsa el botón **New SSH key**

![](images/doc10/doc10-github-new-ssh-key.png | width=100)

Y añade la clave publica del servidor que has copiado desde el terminal.

![](images/doc10/doc10-github-anadir-clave-publica.png | width=100)

##

