# Clases

Como he mencionado anteriormente, las clases y los objetos sirven para crear tu propio tipo de datos (es decir, tipos de datos definidos por el usuario). Una clase es un tipo de dato definido por el usuario, y la crear instancias de una clase hace relación a la creación de objetos de ese tipo. Las clases y los objetos son considerados los principales bloques de desarrollo para Python, el cual es un lenguaje de programación orientado a objetos.

¿Cómo crearíamos una clase en Python? La estructura de clase más simple en Python luciría de la siguiente manera:
~~~
class ClassName:
    statements
~~~
Como puedes ver, la definición de una clase comienza con la palabra clave class, y className sería el nombre de la clase (identificador). Ten en cuenta que el nombre de la clase sigue las mismas reglas que los nombres de variables en Python, es decir, sólo pueden comenzar con una letra o un subrayado _, y sólo pueden contener letras, números o guiones bajos. Además, según PEP 8 (Guía de estilo para la programación en Python), se recomienda que los nombres de las clases estén capitalizadas.

Ahora vamos a definir una clase Person (persona), que por el momento no contendrá nada, excepto la declaración de pass. Según la documentación de Python:

La sentencia pass no hace nada. Puede ser utilizada cuando se requiere una sentencia sintácticamente pero programa no requiere acción alguna.
~~~
class Person:
    pass
~~~
Para crear una instancia (objeto) de esta clase, simplemente haremos lo siguiente:
~~~
jorge =  Person()
~~~
Esto significa que hemos creado un nuevo objeto jorge del tipo Person. Date cuenta que para crear un objeto solo debemos escribir el nombre de la clase, seguido de unos paréntesis.

Podemos identificar de qué clase es jorge, y qué espacio ocupa en la memoria escribiendo: print jorge. En ese caso, obtendrás algo similar a:
~~~
< __main__.Person instance at 0x109a1cb48 >
~~~
## Atributos

Los atributos son como propiedades que queremos añadir a la clase (tipo). Por ejemplo, para nuestra clase Person, vamos a añadir dos atributos: name y school, tal que así:
~~~
class Person:
    name = ''
    school = ''
~~~
Ahora, vamos a crear un nuevo objeto del tipo Person con más detalle, completando estos atributos que acabamos de añadir:
~~~
jorge = Person()
abder.name = 'Jorge'
abder.school = 'Universidad de la vida'
~~~
## Métodos

Los métodos son cómo funciones en Python, ya que se definen con la palabra clave def y cuentan con el mismo formato que las funciones. En nuestra clase, vamos a definir un método que imprima el nombre (name) y la escuela (school) de una persona (Person). La clase se verá de la siguiente manera:
~~~
class Person:
    name = ''
    school = ''
     
    def print_name(self):
        print self.name
         
    def print_school(self):
        print self.school
     
jorge = Person()
jorge.name = 'Jorge'
jorge.school = 'Universidad de la vida'
jorge.print_name()
jorge.print_school()
~~~
He mencionado anteriormente que los métodos son como funciones. Sin embargo, la principal diferencia es que los métodos necesitan tener un argumento convenientemente llamado self, que se refiere al objeto del método que está siendo llamado (es decir jorge). Date cuenta que en una llamada al método, no necesitamos pasar self como un argumento, Python se encargará de eso por nosotros.

Si no ponemos self como argumento en print_name(), Python arrojará un error tal que así:
~~~
Traceback (most recent call last):
  File "test.py", line 14, in 
    jorge.print_name()
TypeError: print_name() takes no arguments (1 given)
~~~
Por supuesto, puedes pasar más de un argumento al método. Vamos a hacer el proceso de imprimir el nombre y la escuela en un solo método, tal que así:
~~~
class Person:
    name = ''
    school = ''
     
    def print_information(self, name, school):
        print self.name
        print self.school
             
jorge = Person()
jorge.name = 'Jorge'
jorge.school = 'Universidad de la vida'
jorge.print_information(jorge.name, jorge.school)
~~~
Prueba y ejecuta el programa, ¿has obtenido el mismo resultado que en el ejemplo de antes?

## Inicialización

En la sección anterior, hemos inicializado name y school, dándoles un valor vacío ''. Pero hay una forma más elegante de inicializar variables con sus valores predeterminados. El inicializador es un método especial, con nombre __init__ (el método se considera especial y será tratado de forma especial, es por eso que tiene subrayados dobles al principio y al final).

Vamos a modificar el programa anterior para utilizar el inicializador. En este caso, el programa se verá como sigue:
~~~
class Person:
    def __init__(self, n, s):
        self.name = n
        self.school = s
     
    def print_name(self):
        print self.name
         
    def print_school(self):
        print self.school
     
jorge = Person('Jorge', 'Universidad de la vida')
 
jorge.print_name()
jorge.print_school()
~~~
Observa que el inicializador necesita dos argumentos. Por ejemplo, si no incluimos el argumento n en el inicializador, obtendremos el siguiente error:
~~~
Traceback (most recent call last):
  File "test.py", line 12, in < module >
    jorge = Person('Jorge', 'Universidad de la vida')
TypeError: __init__() takes exactly 2 arguments (3 given)
~~~
Resumiendo, con las clases serás capaz de crear tus propios tipos de datos, y con los objetos serás capaz de crear instancias de estos tipos de datos. Las cla