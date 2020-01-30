# Diccionarios

Es otro tipo de estructura de datos con la novedad que tiene un indice, en el se pueden almacenar todo tipo de datos

## Crear un Diccionario

~~~
phonebook = {}
phonebook["John"] = 938477566
phonebook["Jack"] = 938377264
phonebook["Jill"] = 947662781
print(phonebook)

~~~

Otra forma

~~~
nombres=['john','Jack','Jill']
telefonos=[939,939,940]
phonebook = {}

for nombre,telefono in zip(nombres,telefonos):
    phonebook[nombre] = telefono

print(phonebook)

~~~

diccionario dentro de un diccionario

~~~
nombres=['john','Jack','Jill']
telefonos=[939,939,940]
phonebook = {}

phonebook['casa'] = { 'nombres' = nombres.
                      'telefonos' = telefonos  }

print(phonebook['casa']

~~~

## Iterar sobre diccionarios

Sobre los datos

~~~
phonebook = {"John" : 938477566,"Jack" : 938377264,"Jill" : 947662781}
for name, number in phonebook.items():
    print("Phone number of %s is %d" % (name, number))
~~~

Sobre las claves

~~~
phonebook = {"John" : 938477566,"Jack" : 938377264,"Jill" : 947662781}
for name in phonebook.keys():
    print("Phone number of %s is %d" % (name, phonebook[name]))
~~~

## Borrando registros

~~~
phonebook = {
   "John" : 938477566,
   "Jack" : 938377264,
   "Jill" : 947662781
}
del phonebook["John"]
print(phonebook)
~~~

