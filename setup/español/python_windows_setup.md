# Instalación de python y librerias en Windows
=======

# Python Nativo (Recomendado)

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

Ahora continuaremos con la instalacion de los paquetes, para instalar estos paquetes usaremos el comando: 

    pip install numpy scipy matplotlib ipython jupyter pyopengl glfw pillow

Siempre es posible instalar cada librería por separado.
 
Y ahora se deberían poder correr todos los programas normalmente.


## Instalando Anaconda (No Recomendado)

⚠ Si no tiene ya instalado Anaconda prefiera seguir la instalacion de Python nativo. ⚠

Anaconda Distribution, permite administrar paquetes de python de manera similar a como se realiza en linux.

Primero descargue e instale anaconda python versión 3.8 en https://www.anaconda.com/products/individual#Downloads

![Descarga](./captures/captura3.jpg)

 Marque la segunda opción y termine la instalación


![instalacion](./captures/captura4.jpg)

Creando un environment
----------------------

Ahora necesita trabajar con la terminal de Anaconda "Anaconda Prompt" escribiendo en el buscador.

![buscador](./captures/captura5.jpg)

Donde se abrirá una terminal como la que se muestra

![terminal](./captures/captura6.jpg)


En dicha terminal creamos un environment ejecutando:

    conda create -n python-cg

Luego lo activamos con

    conda activate python-cg

Aparecerá (python-cg) al lado izquierdo de su prompt indicando que este es el environment activo. Puede volver al environment base con

    conda activate base

En cualquier momento, usted puede ver una lista con todos sus environments utilizando el comando:

    conda info --envs

Debiera ver una lista con 'base' y 'python-cg'.

Si comete algún error, puede eliminar un environment y todas sus librerias con

    conda remove --name python-cg --all

y luego realizar una nueva configuración.


Instalando las librerías necesarias
-----------------------------------

Regrese al environment python-cg, una vez ahí ejecute el siguiente comando para ver si está instalado pip:

    pip
    
Si no arroja error o no encontrado puede seguir, de lo contrario tiene que instalar pip con el comando:

    conda install pip
    
Ahora si puede instalar las librerías:

    pip install numpy scipy matplotlib pyopengl glfw ipython jupyter pillow imgui[glfw]

Es posible que se le pida actualizar algunas dependencias, ingrese 'y' para aceptar.
