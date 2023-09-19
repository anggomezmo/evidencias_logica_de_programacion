<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


# Actividad: Ejecicios Array - ArrayList
## 1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.
#### Ejemplo Array
```java
import java.util.Arrays;

public class EjercicioArray {

    public static void main(String[] args) {
        // Crear un array de números enteros
        int[] numeros = {5, 2, 10, 7, 1};

        // Imprimir el array original
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Calcular la suma de los elementos del array
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
    }
}
```
### Ejemplo Array list

```java
import java.util.ArrayList; 
import java.util.Scanner;

public class AppNotas {

  public static void main(String[] args) {

    ArrayList<String> notas = new ArrayList<>();
    
    Scanner scan = new Scanner(System.in);

    while(true) {

      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      int opcion = scan.nextInt();

      if (opcion == 1) {
        agregarNota(notas, scan);  
      } else if (opcion == 2) {
        mostrarNotas(notas);
      } else {
        break;
      }

    }

  }

  public static void agregarNota(ArrayList<String> notas, Scanner scan) {
    
    System.out.println("Ingrese el titulo de la nota:");
    String titulo = scan.nextLine();
    
    System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();
    
    notas.add(titulo + " - " + contenido);

  }

  public static void mostrarNotas(ArrayList<String> notas) {

    for(String n : notas) {
      System.out.println(n);
    }

  }

}

```


## 2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.


# Solución.

##   Analisis del ejemplo Array:

#### - Parte 1 del programa.

El codigo comienza con la importación de la clase Array y la creación del método principal.
```java
import java.util.Arrays;
 public static void main(String[] args) {
 }
```
Dentro del metodo principal, se inicializa un array de números enteros.

```java
int[] numeros = {5, 2, 10, 7, 1};
```
Se utiliza un println para imrpimir los elementos del array. Para ello se utiliza de la clase Arraty el metodo toString, que nos da una representación en cadena de texto del array.

```java
System.out.println("Array original: " + Arrays.toString(numeros));
```


Luego se utilizará un ciclo for para calcular la suma de los elementos del array, y posteriormente mostrar su resultado.
Para ello se sigue con los siguientes pasos:

1. Se crea la variable de tipo entero "suma" para ir acumulando progresivamente la suma de los elementos del array.

```java
int suma = 0;
```


2.  Iniciar un ciclo for para iterar el array, para ello se inicializa la variable i en 0, y la condición de parada se da cuando el valor de i sea menor al número de elementos del array.

3. Dentro del for sumaremos a la variable "suma" que inicialmente es 0, el valor del elemento en la posición i (variable condicional del for) del array.
```java
for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }

```
Para cuando el for finaliza sólo queda enseñar el resultado de la suma. Para ellos imprimos el valor de la variable suma.

```java
 System.out.println("La suma de los elementos es: " + suma);
```

#### - Parte 2 del programa.

La segunda parte del programa toma nuestro array anteriormente creado y busca cual es el mayor elemento del mismo.

Para ello comenzamos creando una variable de tipo entero "maximo" que inicialmente tendra el valor del primer elemento del array.

```java
int maximo = numeros[0];
```
Posteriormente los pasos para hallar el máximo valor son:

1. Iniciar un ciclo for para iterar el array, para ello se inicializa la variable i en 1 (puesto que el primer valor del array ya lo tenemos almacenado como máximo temporal en la variable "maximo"), y la condición de parada se da cuando el valor de i sea menor al número de elementos del array.

2. Dentro del for verificaremos si el elemento en la posición i (variable iteradora) es mayor o no a nuestro máximo actual:
- En caso de serlo, nuestro máximo se actualizara al actual elemento iterado del array.

- En caso de no serlo, el for seguirá con la siguiente iteración manteniendo el máximo actual.
```java
for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
```
Para cuando el for finaliza sólo queda enseñar el máximo valor del array. Para ello imprimos el valor de la variable "maximo".

```java
System.out.println("El número más grande es: " + maximo);
```
#### - Parte 3 del programa.

La última parte del array consiste en ordenar los elementos del array de menor a mayor.

Para ello utilizamos el metodo sort de la clase Arrays que ordena de forma automatica los elementos del array.
```java
 Arrays.sort(numeros);
```
Por ultimo se utiliza un println para imrpimir los elementos del array ordenados. Para ello se utiliza de la clase Arrays el metodo toString, que nos da una representación en cadena de texto del array.

```java
System.out.println("Array original: " + Arrays.toString(numeros));
```

###   Analisis del ejemplo ArrayList:

El codigo comienza con la importación de la clase Array, la clase Scanner y la creación del método principal.
```java
import java.util.Arrays;
 public static void main(String[] args) {
 }
```
Primero se explicarán los metodos de la clase para entender mejor el funcionamiento del programa.

#### 1. Metodo agregarNota:

Este método recibe como argumentos el array notas, y el objeto scan de la clase Scanner.

```java
  public static void agregarNota(ArrayList<String> notas, Scanner scan) {

  }
```
Empieza mostrando un mensaje para ingresar el nombre de la nota, y lo almacena en la variable tipo Stting "titulo" inicializada por consola. 
```java
System.out.println("Ingrese el titulo de la nota:");
    String titulo = scan.nextLine();
```

De la misma forma se ingresa la nota en la variable de tipo String "contenido".

```java
System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();
```
Luego se agrega al array notas un elemento que contiene el titulo de la nota y su valor.

```java
System.out.println("Ingrese el contenido de la nota:");
    notas.add(titulo + " - " + contenido);
```

#### 1. Metodo mostrarNotas:

Este metodo recibe como parametros de entrada el array notas, y su función es imprimir las notas guardadas en el array.
```java
public static void mostrarNotas(ArrayList<String> notas) {
    }
```
Para ello se utiliza un for each que recorre el array notas y imprime el contenido del elemento n (variable iteradora).
```java
for(String n : notas) {
      System.out.println(n);
    }
```

##  2. Ejemplos de Array y Arraylist:

