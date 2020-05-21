# SSH básico
## ¿Qué es SSH?

Es un protocolo para controlar maquinas de forma remota, emplea dos claves para conectarnos de forma segura, una del "punto de acceso" y otra del "destino".

>Windows requiere instalacion de un cliente de SSH "Putty", a diferencia Linux y MacOS tienen preinstalada esta herramienta.

## Procedimiento de conexión

Abrimos terminal (verificamos estar en la raíz), despues generamos las claves o certificados con el comando:
```cmd
root@Usuario:~# ssh-keygen
```
nos pedirá una frase para generar los certificados (puede ir vacio), esto crea dos certificados, uno publico `id_rsa.pub` que será el que se compartirá con el destino para ser sustituido como contraseña y otro privado `id_rsa` (este no se debe compartir). Los certificados estarán alojados en el directorio `/Users/nombreusuario/.ssh/` 

Hacemos lo anterior también en la otra maquina. 

Desde la maquina destino utilizaremos dos ventanas de consola. En la primera el comando:
```console
root@Usuario:~# cat .ssh/id_rsa.pub
```
mostrara el contenido del certificado, lo seleccionamos y copiamos.

En la segunda terminal nos conectamos al destino remoto utilizando el siguiente comando:

```console
root@Usuario:~# ssh nombreusuario@0.0.0.0
```
donde nombre de usuario se refiere al usuario destino en la maquina a la que queremos conectarnos y 0.0.0.0 se debe sustituir por la ip de destino. 
> ###### Para averiguar la ip, de forma local se utiliza el comando `ipconfig` en Windows o `ifconfig` en Linux y Mac.

Enseguida nos preguntará si queremos guardar el fingerprint del servidor y escribimos *yes*.

Ahora con el comando:

```console
nombreusuario@0.0.0.0:~# nano .ssh/authorided_keys
```
abrirá el archivo authorized_keys, pegamos el certificado que copiamos antes y salimos y guardamos con *Ctrl+X* y *Enter*. Ahora podemos salir con `logout` y al volver a entrar ya no solicitará ingresar la contraseña. 

## Anexo

Algunos comandos básicos para el uso de directorios en consola:

`console.log('Hola mundo')` 

| Comando | Propiedades |
| :--------: | :-------: |
| ls | Muestra contenido del directorio (Archivos,Carpetas)|
| mkdir | Crea un directorio |
| touch | Crea un archivo si no existe y si existe cambia la fecha de modificacion|
|  mv | Mueve un archivo a una nueva ubicación |
|  cp | Copia un archivo a una nueva ubicación|
| cd| Permite entrar a un directorio|
|  rm| Borra un archivo|
|   rmdir| Borra una carpeta|
| nano, vim, emacs| Son editores de texto, abre un archivo con el editor|
| wget | Descarga un archivo de internet|
| cat | Despliega el contenido del archivo en la ventana de la consola|
