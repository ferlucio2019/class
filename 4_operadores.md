# Operadores 

## Aritméticos

los operadores son ( + - * / % ** )

~~~
numero = 1 + 2*2 /4.0

numero = numero % 2

numero = numero**2

print (numero)
~~~

## Operadores con Cadenas

~~~
cadena = 'hola ' +  'Mundo'

print (cadena)

print (cadena *10)

~~~
## Operadores con listas

~~~

print([2,2] + [3,3])

print([2]*10)

~~~

## Formateando cadenas

### tipo 1

Podemos modificar una cadena mediante los operadores de cadena

~~~
%s - String (or any object with a string representation, like numbers)

%d - Integers

%f - Floating point numbers

%.<number of digits>f - Floating point numbers with a fixed amount of digits to the right of the dot.

%x/%X - Integers in hex representation (lowercase/uppercase)

~~~

Alguna operaciones son:

~~~
mundo = 'Mundo'
print('Hola %s' % mundo)
~~~

### Tipo 2
o bien

~~~

mundo = 'Mundo'
print('Hola {}'.format(mundo))

~~~

## Operadores Booleanos

~~~
name = "John"
age = 23
if name == "John" and age == 23:
    print("Your name is John, and you are also 23 years old.")

if name == "John" or name == "Rick":
    print("Your name is either John or Rick.")
~~~

## Operador IN

~~~
name = "John"
if name in ["John", "Rick"]:
    print("Your name is either John or Rick.")
~~~


## Operador IS

~~~
x = [1,2,3]
y = [1,2,3]
print(x == y) # Prints out True
print(x is y) # Prints out False
~~~

## Operador NOT

~~~
print(not False) # Prints out True
print((not False) == (False)) # Prints out False
~~~
