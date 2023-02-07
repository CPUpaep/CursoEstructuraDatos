# Funciones y Procedimientos

Nos permiten desarrollar una parte del código que puede ser llamado en nuestra clase principal cuando lo necesitemos.

```cpp
int main(){

    proceso1();
    proceso2();

    proceso1();
    proceso3();
    return 0;
}
```

## Funciones
Son aquella partes del código que regresan un valor, este valor esperado tiene que estar declarado al inicio de la función.

Ejemplo : 
```cpp
int sumar(){
    int a = 1, b = 4;
    return a + b;
}

x = 23 - sumar();
//Output : 18
```
Se crea un función que regresa la suma de dos variables y que espera una variable int.

```cpp
char verificar(){
    char c = 'F';
    if(condicional == true){
        return 'V';
    }
    return 'F';
}
```

Se crea una funcion que espera una variable char. 

La función tiene que siempre retornar algo, en dado caso que la condicional no se cumpla, no se retornaria ningun valor.

## Procedimientos

Son aquella partes del código las cuales no retornan un valor, simplemente hacen un proceso.

Se declaran bajo la palabra reservada *void*.

```cpp
void decirHola(){
    cout<<"Hola";
}

void cribraErastotenes(){
    //Código para la criba
}
```

# Alcance de variables

## Variables Locales

Las variables locales sólo pueden ser accesibles dentro de la función o procedimiento en la cual fueron declaradas.


## Variables Globales

Las variables globales pueden ser utilizadas en cualquier función o procedimiento dentro de la clase.

## Ejemplo

```cpp

#include <bits/stdc++.h>

int a = 2; // Variable Global

void procedimiento(){
    int b = 3; // Variable Local
    a += b;
}

using namespace std;

int main(){
    int b = 10; // Variable Local
    procedimiento();
    a *= b;
    return 0;
}
```
# Parametros

Tanto los procedimientos como funciones pueden recibir valores para procesarlos.

```cpp
int formula(int x){
    return (x * 2) + 3;
}

int suma(int a, int b){
    return a + b;
}
```
## Paso de parametros

Como hemos visto, el paso de parámetros nos permite utilizar variables de manera dinámica en las funciones y procedimientos. 

Pero existen diferentes maneras de hacerlo.

### Valor

Genera una variable o una copia del valor registrado en esa variable.

```cpp
int f(int x){
    return x+1;
}

```

### Referencia

Da un alias a una variable que ya se encuentra en existencia por medio de ese alias.

En términos más sencillos, solo es darle otro nombre a la misma variable.

```cpp
int felipe = 10;
int &rafael = felipe;

rafael = 5;

cout<<felipe;
```

### Apuntadores

[Link aqui]()