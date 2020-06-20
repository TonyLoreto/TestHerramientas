# Python

## Configuración inicial de python

Primero necesitamos crear un entorno virtual, esto es porque algunos sistemas operativos desarrollaron parte de su software con una versión especifica de Python y para mantener compatibilidad no permite realizar actualizaciones o instalaciones de otras bibliotecas. Por ello disponemos de entornos virtuales donde se puede configurar que version de Python instalar así como las distribuciones o paquetes de bibliotecas.

Instalamos la herramienta que nos permite crear entornos virtuales, desde consola utilizamos el comando:
```console
root@Usuario:~# pip3 instal pipenv
```
El siguiente paso será crear nuestro entorno virtual, en *pythonversionX* sustituimos la *X* por la versión deseada y, en lugar de *nombredelentorno* el nombre que le queremos dar a nuestro entorno.

```console
root@Usuario:~# pythonversionX -m venv nombredelentorno
```
Una vez hecho esto podemos ingresar a nuestro entorno con el siguiente comando:
```console
root@Usuario:~# source nombredelentorno/bin/activate
```
El nombre de usuario de nuestra consola deberá cambiar a lo siguiente:
```console
nombredelentorno:~#
```
Listo!!! A partir de este punto puedes instalar las bibliotecas que requieras en tu entorno.

Cuando quieras salir del entorno solo escribe:
```console
root@Usuario:~# deactivate
```
