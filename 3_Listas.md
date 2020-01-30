# Listas


Lista es algo parecido a un array o matriz que nos permite almacenar variables. Tiene otra utilidad que es iterable, es decir que nos permite recorrer la lista utilizando cada uno de sus elementos.

Puede tener elementos tipo caracter o numerico o listas dentro de la lista.

# Manipulando una Lista

Creo una lista
~~~
mylist = []

pasos = [1,2,3,4,5]

dias = ["Lunes", "Martes", "Miércoles", "Jueves", "Viernes", "Sábado", "Domingo"]

print (lista)
~~~

Con la propiedad append añado elementos a la lista
~~~
mylist.append(1)
mylist.append(2)
mylist.append(3)

print (mylist)
~~~
Con del puedo borrar elementos de la lista
~~~
del mylist[1]

print mylist
~~~

Visualizo la lista

~~~
print(mylist)
~~~

Puedo visualizar cada uno de los elementos 
~~~
print(mylist[0]) # prints 1
print(mylist[1]) # prints 2
print(mylist[2]) # prints 3

~~~

Seleccionar parte de una lista

~~~
print(dias[1:4]) # Se extrae una lista con los valores 1, 2 y 3

['Martes', 'Miércoles', 'Jueves']

print(dias[4:5]) # Se extrae una lista con el valor 4
['Viernes']

print(dias[4:4]) # Se extrae una lista vacía
[]
~~~



# Iteración de la lista

Recorrer una lista

~~~
for dia in dias:
    print(dia)
~~~


# Elementos en una lista

~~~
if 'lunes' in dias:
    print ('lunes está en días')

if 'saturno' not in dias:
    print ('lunes está en días')

~~~

# iterar listas en una lista

~~~
print([dia for dia in dias if dia |='Domingo' :]

print([ x*2 for x in range(1,10)])
~~~
