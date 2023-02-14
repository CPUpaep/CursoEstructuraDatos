# Estructuras

Un struct es una forma de organizar variables elementales en un sola variable usando la abstracción.

Ejemplo


```cpp
    struct nombreEstructura{
        //atributos
    };
```

```cpp
    struct Punto{
        int x;
        int y;
    };
```

```cpp
    struct Punto{
        string nombre;
        int x = 0;
        int y = 0;
        int z;
    };

    struct Punto p1;
    p1.z = 8;
    cout<<p1.x<<" "<<p1.y<<" "<<p1.z;
```

## Conjuntos de Struct
Como si fuera otra variable, podemos hacer un arreglo, una matriz o cualquier otra estructura de dato de tipo Struct

```cpp
    Puntos puntos[3];
    Punto p;

    for(int i = 0; i<3;i++){
        cin>>puntos[i].x>>puntos[i].y;
    }

    for(int i = 0; i<3;i++){
        p = puntos[i];
        cout<<p.x<<p.y;
    }   
```

## Estucturas Anidadas

Un struct puede contener dentro otro struct

```cpp
struct Libro{
    string editorial;
    string nombre;
    int anio;
};

struct Bibloteca{
    string nombre;
    Libros libros[100];
};
```

## Funciones dentro de struct

```cpp

struct Punto{
    int x,y;

    void mostrar(){
        cout<<x<<" "<<y<<"\n";
    }

    int suma(){
        return x + y;
    }
};

int main(){
    Punto p;
    p.x = 5;
    p.y = 3;

    p.mostrar();
    cout<<p.suma();

    return 0;
}
```

# Contructores
Un constructor es una funcion que solo se utiliza 1 vez y se utiliza para crear  y incializar un struct.

La sobrecarga de metodos te permite tener una funcion o procedimiento con el mismo nombre, siempre y cuando la cantidad y tipo de atributos sea diferente.

```cpp

struct Punto{
    int x,y;

    Punto(){
        x = y = 0;
    }

    Punto(int dato){
        x = y = dato;
    }

     Punto(int a,int b){
        x = a;
        y = b;
    }
};

int main(){
    Punto p1 = Punto();
    Punto p2 = Punto(23);
    Punto p3 = Punto(2,3);

    return 0;
}
```


# Struct con Punteros

```cpp
struct Punto{
    int x;
    int y;
};

int main(){
    Punto p1;
    Punto *p2 = &p1;

    p1.x = 3;
    p2->y = 6;

    cout<<p2->x << " "<<p1.y;

    return 0;
}

Output: 3 6
```

## Nodos

```cpp
struct Nodo{
   int data;
   Nodo *next;

   Nodo(int d){
       data = data;
       next = NULL;
   }
};

int main(){
    Nodo n1 = Nodo(2);
    Nodo n2 = Nodo(4);

    n1.next = &n2;

    cout<<n1.data << " "<<n1.next->data;

    return 0;
}

Output: 2->4
```