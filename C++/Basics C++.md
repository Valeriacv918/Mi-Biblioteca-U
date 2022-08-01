# C++ Curso

## Incluir librerias
 #### 1.Incluir todas las librerías (CP)
```
#include <bits/stdc++.h>
```
 #### 2. Incluir librerías específicas (Forma correcta)
```
#include <iomanip>      // Manipulación del cout para mostrar los números con el formato que queramos
#include <vector>       //Usar vectores
#include <utility>      // Usar pares con vectores
#include <set>          //Usar sets
#include <algorithm>    //Usar sort

using namespace std;
```

## I/O 
Para introducir datos por teclado/pantalla
```
getline(cin, nombreVariable);   // Lee toda una línea del teclado(cin) y lo guarda en la variable que se le pasa.

cin>>variable;      // Lee la variable hasta el 1er espacio

while (cin >> num)  // Lee la entrada hasta que ya no haya mas por leer
```
Para imprimir datos

```
cout<< variable1<< variable2<< endl;     // Imprime la variable1, variable2 y hace un salto de linea

setprecision(numero_de_digitos);	        // imprime la cantidad de digitos que se coloque acá

cout << setprecision(4);
cout << 3.141596 << endl; // Mostrara por pantalla 3.142
```
 Configurando "cout << fixed", la orden"setprecision() pasa a referirse únicamente a las posiciones decimales (en lugar de al número de dígitos), incluso rellenará de ceros la parte decimal hasta llenar la cantidad de caracteres indicada.
 ```
 cout<< fixed; 	 indica que va a contar la cantidad de dígitos  decimales y redondea al numero de setprecision()
 cout << fixed;
 cout << setprecision(4);
 cout << 3.141596 << endl; // Mostrara por pantalla 3.1416
 ```

 Podemos referirnos en general a la anchura que ocupará una variable con setw(espacio_minimo_que_ocupa). Para hacerlo hay que indicar con qué carácter rellenar los espacios sobrantes mediante la instrucción setfill(letra_con_la_que_rellenar) (la letra debe ir entre comillas simples)

*Nota:* setw() indicará el número mínimo de caracteres que ha de ocupar la variable, incluyendo el punto decimal. Los espacios que falten hasta llegar a este número se añadirán a la izquierda.

Una vez se ha configurado setw() todos siguientes cout del código usarán ese formato.

 ```
 cout << setfill('*');
 cout << setprecision(7);
 cout << setw(1);
 cout << 3.141596 << endl; // Mostrara por pantalla 3.141596

 cout << setw(10);
 cout << 3.141596 << endl; // Mostrara por pantalla **3.141596 
```
O formatear el cout de la siguiente manera

```
cout << fixed << setprecision(5) << setw(10) << setfill('*') << 3.14 << endl; 
```

## Operadores y precedencia Mayor a menor

1. ()
2. Tipo de Variable
3. *, /, %
4. +, -
5. <<, >>
6. <=, >=, >, < 
7. ==, !=
8. and
9. or
10. =

## Tipos de Datos
#### 1. Int
#### 2. 
#### 3.
#### 4.Strings
```
string word = "hola";
```
```
cout << "Indica una posicion y la convertire en mayuscula: ";
cin >> posicion;
nombre[posicion] = nombre[posicion] - 32;
```
#### 5. char
```
char letra = 'A';
```
```
letra = letra - 32;     // convertir a mayuscula
```

## Referencias
Es una ubicación que le da permiso de cambiar el elemento que hay allí

Si quisiéramos que una función modificara una de la variables que le pasamos debemos poner un símbolo ampersand *(&)* antes del nombre de la variable en la definición de los parámetros de la función. 

De lo contrario la función crea una copia del elemento y no lo modifica

```
void funcion(vector<int> &nombre){

}
```

## Estructuras de Datos

#### Arreglos (Arrays)
```
    tipoDeDato nombreArreglo[longitudArreglo];
    nombreArreglo = { 6, 8, 7, 3, 2, 8, 9, 3 }; Dar arreglo definido.

```
Se accede igual que un arreglo

### Vectores
```
#include <vector>
```
Se declara:
```
vector < tipo_de_los_valores > nombre_de_la_variable( tamaño , valor_predeterminado(opcional));
```
*Métodos:*
- .size()
- push_back(valor) //Agregar al final valor
- pop_back()
- insert(valor, pos) 
- erase(pos) 
- sort(v.begin(), v.end())

#### sort
Como es evidente sort para poder ordenar va comparando elementos de dos en dos. La función de comparación es la que decide, para cada par de valores, cual de los dos debe ir primero en la ordenación. Esta función recibe dos valores y devuelve TRUE si el primero debe ir primero o FALSE si es el segundo el que debe ir primero
```
sort( <inicio_de_la_serie>, <final_de_la_serie>, <funcion_de_comparacion>(opcional));
```

### Matrices
```
vector<vector<int> > matriz(num_filas, vector<int> (num_columnas, valorPorDefault));

int matriz[num_filas][num_columnas]; // matriz de arrays
```

### Pairs
```
#include <utility>
```

```
pair < tipo_de_valor_primero, tipo_de_valor_segundo > nombre_de_la_variable( <primer_valor>, <segundo_valor> );
```
Ejemplo: 
```
pair<string, int> goleador;
cin >> goleador.first;
cin >> goleador.second;

```

### Set 
```
#include <set>
```
Crear un set
```
set < tipo_de_los_valores > nombre_de_la_variable;
```
Recorrer un set FALTA
```
for (string it : s_nombres) {
  cout << it << ", ";
}
```
*Métodos:*
- set.insert(element)
- set.size()
- set.count(element)        // Verifica si ese elemento pertenece al Conjunto
- set.erase(element)

### Map  
Asocia etiquetas a valores (cada etiqueta tiene un único valor asociado).
```
#include <map>
```
Declarar map
```
map < tipo_de_las_etiquetas , tipo_de_los_valores >;
```

Acceder a alguna llave de map 
```
nombreMap["key"] = "valor";
```

Recorrer map 
```
for (pair<string, string> it : nombreMap) {
  cout << it.first << " = " << it.second << endl;
}
```

*Métodos:*
nombreMap.erase("key");      // Borrar elemento
nombreMap.count()            //Para ver si existe

## Bits   
