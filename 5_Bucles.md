# Bucles


## Bucle For

### Iterando sobre un rango
~~~
for x in range(5):
    print(x)
~~~

### Iterando sobre un rango concreto
~~~
for x in range(3, 6):
    print(x)
~~~

# Iterando sobre un rango y salto
~~~
for x in range(3, 8, 2):
    print(x)
~~~

### Iterando sobre una lista

~~~
primes = [2, 3, 5, 7]
for prime in primes:
    print(prime)
~~~

### Iterando sobre una lista y un rango

~~~
primes = [2, 3, 5, 7]
for i,prime in enumerate(primes):
    print(prime)
~~~

### Iterando sobre dos listas

~~~
primes = [2, 3, 5, 7]
otros = [1,2,3,4]
for i,prime in zip(primes,otros):
    print(i,prime)
~~~

## Bucle While

Se repite las instrucciones mientra se cumpla una condición

~~~
count = 0
while count < 5:
    print(count)
    count += 1  # This is the same as count = count + 1
~~~

## Instrucción break

Nos lleva a la primera instrucción del For o While

~~~
count = 0
while True:
    print(count)
    count += 1
    if count >= 5:
        break

Prints out only odd numbers - 1,3,5,7,9

for x in range(10):
    # Check if x is even
    if x % 2 == 0:
        continue
    print(x)
~~~


