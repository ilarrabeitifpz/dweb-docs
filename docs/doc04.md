# Generar claves publica-privada y configurar servidor para conexión remota SSH sin contraseña.

1. Generar las llaves desde la parte del cliente:
Primero entras en el CMD de tu ordenador y escribes el comando `ssh-keygen`

![](images/doc4/doc_4_Windows10_keygen.jpg)


2. Subir la llave publica al servidor

  *Es recomendable instalar [Link a wingw10](http://mingw-w64.org/doku.php)*


3. Cambias el nombre de la llave publica a authorized_keys
  ![](images/doc4/doc_4_llavesCreadas.jpg)


4. Le das permisos de lectura y escritura a la llave publica creada
  ![](images/doc4/doc_4_DarPermisos.jpg)

5. 
