# Recursividad

Es el concepto de que una función o procedimiento se llame a si mismo.

Una función recursiva debe tener un caso base para terminar con la recursividad, de otra forma el ciclo será infinito.

Una de las utilidades de las estructuras de datos, es poder utilizar la memoria dinámica (No declarar el tamaño que vas a usar previamente).

Por lo cual el tener una función recursiva para recorrer nuestra estructura hasta llegar una condición de paro, es fundamental.

# Ejemplos

## Factorial

```cpp
int factorial(int n){
    if(n>=1){
        return n * factorial(n);
    }
    return 1;
}
```

## Fibonacci

```cpp
int fib(int n){
    if(n == 1 || n == 2){
        return 1;
    }
    return fib(n-1) + fib(n-2);
}
```

## Binario

```cpp
string binario = "";
void to_binary(int n){
    if(n!=0){
        to_binary(n/2);
        binario += str(n%2);
    }
}
```

## Minimo Comun Divisor

```cpp
```

## Exponente

```cpp
```