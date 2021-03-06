Módulos

Crear un módulo en Python es tan sencillo como crear un script, sólo tenemos que añadir alguna función a un fichero con la extensión .py, por ejemplo saludos.py:
~~~
def saludar():
    print("Hola, te estoy saludando desde la función saludar() " \
            "del módulo saludos")
~~~
Luego ya podremos utilizarlo desde otro script,por ejemplo script.py, en el mismo directorio haciendo un import y el nombre del módulo:
~~~
import saludos

saludos.saludar()
~~~
También podemos importar funciones directamente, de esta forma ahorraríamos memoria. Podemos hacerlo utilizando la sintaxis from import:
~~~
from saludos import saludar

saludar()
~~~
Para importar todas las funciones con la sintaxis from import debemos poner un asterisco:
~~~
from saludos import *

saludar()
~~~
Dicho esto, a parte de funciones también podemos reutilizar clases:
~~~
class Saludo():
    def __init__(self):
        print("Hola, te estoy saludando desde el __init__ " \
                "de la clase Saludo")
~~~
Igual que antes, tendremos que llamar primero al módulo para referirnos a la clase:

import saludos

s = saludos.Saludo()

O cargar solo una clase con el from import:

from saludos import Saludo

s = Saludo()

El problema ocurre cuando queremos utilizar nuestro módulo desde un directorio distinto por ejemplo test/script.py.