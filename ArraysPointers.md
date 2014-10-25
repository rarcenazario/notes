* Repasar el pass by value de los arreglos en C++
* Completar el ejemplo de hallar el índice del mínimo valor
* Arreglos bidimensionales en C++
* Se guardan de forma row-major. En memoria las filas quedan contiguas. A = {{10,20,30},{15,25,35}}. 
* El cálculo que se realiza es $A_{base} + sizeof(type) * ( ri \times  QTYCOLS + ci)$ 
* Se debe siempre especificar al menos el número de columnas del arreglo
    ```cpp
    void xou(int A[][3],const int NUMROWS,  const int NUMCOLS ) {
        for (int r = 0; r < NUMROWS; r++) {
            for (int c = 0; c < NUMCOLS; c++) {
                cout << A[r][c] << "-";
            }
            cout << endl;
        }
    }
    ```

* arreglos de caracteres
    - char nombre[] = "caballo"; `c a b a  l l o `
    - No se puede nombre.length(), ni nombre.find(), etc.
    
* Ejemplo: Algoritmo para determinar si la diagonal principal de una matriz cuadrada de caracteres consiste de un mismo símbolo.
    ```
    Input: A, a square 2dim integer  array with C cols = R rows
    Output: true is the main diagonal consists all of the same number
    -----------------------------------------------------------------
    1. for i = 1 to R-1:
    2.    if A[0][0] != A[i][i]:
    3.         return false
    4. return true
    
    ```
    
* Todos los arreglos que hemos creado hasta ahora son de tipo estático (se quedan del mismo tamaño que fueron creados a través de la duración del programa).
    * `int A[10]`
    * A través del programa será de tamaño 10 y solo 10.
    

# Variables puntero!

* Repaso, el operador `&` antes de una variable.

* Un variable puntero (sencillo) es una variable que guarda dentro de si la dirección de memoria donde está guardado un valor.
   ```cpp
   int x;
   
   cout << x << endl;
   cout << &x << endl;
   ```
   
   ```cpp
   int x;
   x = 10;
   
   cout << x << endl;
   cout << &x << endl;
   ```
   
   ```cpp
   int x = 10;
   int *px;
   px = &x;
   
   
   cout << x << endl;
   cout << &x << endl;
   
   cout << px << endl;
   cout << *px << endl;
   ```
   
* El operador de desreferencia: se evalua interpretando el contenido de la variable como una dirección donde buscar un valor.

    ```cpp
    int A[] = {4, 9, 7, 3, 2};
    
    cout << A << endl;  // imprime la dir donde comienza el arreglo A
    cout << *A << endl; // imprime el elemento indice 0 del arreglo A 
    ```
