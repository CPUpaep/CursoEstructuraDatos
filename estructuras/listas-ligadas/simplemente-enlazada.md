# Simplemente Enlazada

```cpp
#include <bits/stdc++.h>

using namespace std;


struct Nodo{
int dato;
Nodo *next;

Nodo(int d){
dato = d;
next = NULL;
}
};

struct Lista{
Nodo *inicio;

Lista(){
inicio = NULL;
}

void agregarInicio(int num){
Nodo *n = new Nodo(num);
n->next = inicio;
inicio = n;
}

void agregarFinal(int num){
Nodo *n = new Nodo(num);
Nodo *aux = inicio;

while(aux->next != NULL){
aux = aux->next;
}
aux->next = n;
}

void eliminarInicio(){
Nodo *aux = inicio;
inicio = inicio->next;
delete aux;
}

void eliminarFinal(){

}

bool estaVacia(){
if(inicio == NULL){
return true;
}
return false;
}

void mostrar(){
Nodo *aux = inicio;

while(aux != NULL){
cout<<aux->dato <<" -> ";
aux = aux->next;
}
cout<<"\n";

}

};


int main(){

Lista *numeros = new Lista();

numeros->agregarInicio(1);
numeros->agregarInicio(2);
numeros->agregarInicio(3);
numeros->agregarInicio(4);
numeros->agregarInicio(5);
numeros->agregarInicio(6);

numeros->agregarFinal(-1);
numeros->agregarFinal(-2);
numeros->agregarFinal(-3);
numeros->agregarFinal(-4);
numeros->agregarFinal(-5);

numeros->mostrar();
numeros->eliminarInicio();
numeros->mostrar();

return 0;
}
--

```
