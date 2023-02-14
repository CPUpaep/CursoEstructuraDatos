# Apuntadores

## Definicion
Un puntero es una variable que
almacena la dirección de memoria de un
objeto.

## Representación Natural Variables

```cpp
int a = 5;
```
Crea una variable de tipo
entero de nombre a cuyo
valor sera igual a 5


```cpp
int &b = a;
```
Crea un variable de tipo entero de
nombre b cuya direccion de memoria
sera igual a la direccion de memoria de
la variable de nombre a

```cpp
int *c = &b;
```
Crea una variable de tipo
entero de nombre c cuyo
valor apuntura a la direccion
de memoria de la variable con
nombre b

```cpp
int d = *c;
```   
Crea una variable de tipo
entero de nombre d cuyo
valor sera aquello que apunte
la variable de nombre c

## Otras Referencias

[Low Learning Learning (19 de Junio,2022).
You will never ask about pointers again
after watching this video.](https://www.youtube.com/watch?v=2ybLD6_2gKM)