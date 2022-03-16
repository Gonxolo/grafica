# Instalación de python y librerias en Windows
=======

# Python Nativo

Si usted ya tenía Python instalado con Anaconda y tuvo problemas, seguramente se trata de un problema con las variables de entorno. En ese caso, usted querrá desinstalar Python en conjunto con Anaconda. Haga esto manualmente.

Ahora, deberá instalar Python para que se agregue a sus variables de entorno:
 
Descargar e instalar la última versión estable de Python para Windows desde https://www.python.org/downloads/windows/ segun el procesador de su computador (32 o 64 bits).

![Descarga](./captures/captura0.jpg)

Luego abra el ejecutable y realice la instalación, donde es importante que añada python al path, marcando la opción.  POR FAVOR NO OLVIDE ESTO. SI LO HACE ¡REINSTALE!

![path](./captures/captura1.jpg)

Una vez instalado, asegúrese de que python funciona. Abra alguna terminal de windows (windows-> buscar o ejecutar -> cmd). 

![cmd](./captures/captura8.jpg)


Luego escriba en la terminal

    python --version

Debería aparecer algo del estilo:

    Python 3.10.1
    
De ser asi significa que su instalacion de Python fue exitosa

Python instala de igual manera el paquete pip, que permite administrar e instalar otros paquetes fácilmente. Para comprobar su instalacion escriba:

    pip --version

Debería aparecer algo del estilo:

    pip 21.2.4 from C:\Python310\lib\site-packages\pip (python 3.10)

Lo importante de esto es que le muestre que existe alguna version de pip instalada, si la consola arroja error es posible que pip no este instalado, y para instalarlo se debe ejecutar el modulo get-pip.py (revisar el link https://www.liquidweb.com/kb/install-pip-windows/). Este módulo se puede ejecutar tal como se hacía en el curso de Introducción a la Programación, abriendo el IDLE y corriéndolo.

Ahora pip deberia estar instalado, por lo ahora se procedera a instalar los paquetes necesarios para utilizar en el curso, los cuales corresponden a:

- numpy
- scipy
- matplotlib
- pyopengl
- glfw
- ipython
- jupyter
- pillow

Antes de instalar las librerias crearemos primero un entorno virtual que contega los paquetes del curso, para esto ejecutaremos el siguiente comando idealmente en la carpeta donde guardara los contenidos de este curso:

    python -m venv python-cg
    
Una vez se termine de crear el entorno virtual lo activaremos en la linea de comandos con el comando

    python-cg\Scripts\activate.bat
    
O si se esta haciendo uso de PowerShell con el comando

    python-cg\Scripts\Activate.ps1

Ahora continuaremos con la instalacion de los paquetes, primero debemos asegurarnos de que estamos en el directorio que contiene el archivo `requirements.txt`, de ser asi, para instalar estos paquetes usaremos el comando:

    pip install -r requirements.txt

Que instalara todos los paquetes que se encuentran en el archivo en sus respectivas versiones, junto con algunos paquetes que son requeridos para hacer uso de los paquetes que deseamos instalar.
 
Y ahora se deberían poder correr todos los programas normalmente.
