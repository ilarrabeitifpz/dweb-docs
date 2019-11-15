# 3. Conectarse mediante SSH a servidores.

Estos son los pasos a seguir:

- [Conectarse vía SSH para comprobar conectividad y permisos](#conectarse-via-ssh-para-comprobar-conectividad-y-permisos)
- [Copiar directorio de proyecto web a servidor mediante el comando scp](#copiar-directorio-de-proyecto-web-a-servidor-mediante-el-comando-scp)

## Conectarse vía SSH para comprobar conectividad y permisos
Para empezar, comentar que SSH es un protocolo que facilita las conexiones entre dos sistemas. Con una conexión SSH podremos acceder a una máquina que tenga instalado y activo un servidor SSH. Nosotros accederemos vía terminal.
En Ubuntu, el cliente SSH viene instalado por defecto. Si quisiéramos instalar el servidor SSH tendríamos que escribir el siguiente comando:

    sudo apt-get install ssh

Para conectarnos mediante SSH a una máquina remota simplemente tendremos que escribir el siguiente comando en el terminal:

    ssh [<usuario>@]<hostname>[:<puerto>]

**Usuario**: Tiene que ser un nombre de usuario válido en la máquina remota.
**Hostname**: Puede ser una dirección IP, un dominio, un hostname interno, etc.
**Puerto**: Si el puerto de la máquina remota no es el habitual (el puerto 22) tendremos que especificarlo.    

*Ejemplo*: `ssh user@192.168.1.2`

## Copiar directorio de proyecto web a servidor mediante el comando scp
A continuación, voy a explicar como copiar un directorio desde local a servidor mediante el comando scp. 