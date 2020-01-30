# Funciones

Nos permite dividir nuestro código en distintos bloques y poderlo hacer mas funcional

## Creando una función

### funcion simple
~~~
def mi_primera_funcion():
    print("Hola he creado una función!")
~~~

consta de un nombre
de unos argumentos que van en el parentesis
del código de la función
el retorno de la función o nó

~~~
mi_primera_funcion()

Hola he creado una función!
~~~

### función con argumento

~~~
def mi_primera_funcion(mensaje='Hola he creado una función!'):
    print(mensaje)
~~~

### función con retorno

~~~
def mi_primera_funcion(mensaje='Hola he creado una función!'):
    return mensaje
~~~

### funciones y argumentos *args **kwargs

Muchos progrmadores utilizan los argumentos siguientes al llamar a una función. Se utilizan para pasar argumentos variables a la función.

args se utiliza para enviar una lista a la función
~~~
def test_var_args(f_arg, *argv):
    print "first normal arg:", f_arg
    for arg in argv:
        print "another arg through *argv :", arg

test_var_args('yasoob','python','eggs','test')
~~~

kwargs se utiliza cuando pasamos un diccionario

~~~
def greet_me(**kwargs):
    if kwargs is not None:
        for key, value in kwargs.items():
            print "%s == %s" %(key,value)
 
greet_me(name="yasoob")
name == yasoob
~~~
o bien

~~~
def test_args_kwargs(arg1, arg2, arg3):
    print "arg1:", arg1
    print "arg2:", arg2
    print "arg3:", arg3

args = ("two", 3,5)
test_args_kwargs(*args)
~~~
arg1: two
arg2: 3
arg3: 5


~~~
kwargs = {"arg3": 3, "arg2": "two","arg1":5}
test_args_kwargs(**kwargs)
~~~
arg1: 5
arg2: two
arg3: 3