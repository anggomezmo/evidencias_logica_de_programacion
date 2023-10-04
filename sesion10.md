<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


# Actividad 10: Analisis de algoritmo

Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno



# Solución

## 1. Calcular el movimiento rectilíneo uniforme

El movimiento rectilíneo uniforme (MRU) es un tipo de movimiento en el cual un objeto se mueve en línea recta y a velocidad constante, es decir, su velocidad no cambia en el tiempo. En este tipo de movimiento, la trayectoria del objeto es una línea recta, por lo que su aceleración es cero.

Un ejemplo común de MRU es un automóvil que se desplaza en una carretera recta y mantiene una velocidad constante durante todo el trayecto. Otro ejemplo es una pelota que cae verticalmente al suelo sin ser afectada por la resistencia del aire.

El MRU es un movimiento importante en la física, ya que permite entender conceptos básicos como la velocidad, la distancia recorrida y el tiempo de desplazamiento. Además, es utilizado como base para otros tipos de movimiento más complejos, como el movimiento rectilíneo uniformemente acelerado (MRUA) y el movimiento circular uniforme (MCU).

A continuación el analisis del algoritmo desarrollado.

El algoritmo comienza con la importación de la libreria Scanner, para hacer uso de datos por entrada en la consola, la creación de la clase MRU, y el metodo main.
```java
import java.util.Scanner;

public class MRU {
   public static void main(String[] args) {

   }
```
Continua con la creación del objeto input de la clase ```scanner``` para usar datos ingresados por consola.

```java
 Scanner input = new Scanner(System.in);
```

Continua con la creación de las variables que se van a usar en el programa.


```java
  double velocidad, tiempo, distancia;
```
A continuación se usa el objeto input para pedir la velocidad y el tiempo, almacenandolos en una variable de tipo double.


```java
  System.out.print("Ingrese la velocidad en metros por segundo: ");
      velocidad = input.nextDouble();
      System.out.print("Ingrese el tiempo en segundos: ");
      tiempo = input.nextDouble();
```

Por ultimo se hace el calculo de la distancia recorrida y se muestra el resultado, haciendo uso de la velocidad y el tiempo. 

```java
// Calcula la distancia recorrida
      distancia = velocidad * tiempo;

      // Muestra el resultado en la consola
      System.out.printf("La distancia recorrida es de %.2f metros.", distancia);
```

# 2. Calcular la cantidad de materiales necesarios para construir una pared de ladrillos
Cálculo de la cantidad de materiales para la construcción: Este ejercicio consiste en calcular la cantidad de materiales necesarios para construir una estructura. Para ello, se debe tener en cuenta las dimensiones de la estructura y la cantidad de materiales necesarios por unidad de área o de volumen. Algunos ejemplos de cálculos de materiales son el cálculo de la cantidad de ladrillos n

A continuación el analisis del algoritmo desarrollado.



El algoritmo comienza con la importación de la libreria Scanner, para hacer uso de datos por entrada en la consola, la creación de la clase CantidadLadrillos, y el metodo main.
```java
import java.util.Scanner;

public class CantidadLadrillos {
   public static void main(String[] args) {

   }
```
Continua con la creación del objeto input de la clase ```scanner``` para usar datos ingresados por consola.
```java
 Scanner input = new Scanner(System.in);
```

Continua con la creación de las variables que se van a usar en el programa.


```java
  double largo, alto, ancho, areaPared, cantidadLadrillos, largoLadrillo, altoLadrillo, anchoLadrillo;
```

A continuación se hace uso del objeto input para la guardar en las variables anteriormente creadas los valores requeridos. Cabe destacar que a pesar de que las variables relacionadas al ancho del ladrillo y de la parred estan creadas, no tienen ningún tipo de impacto en el programa.

```java
System.out.print("Ingrese el largo de la pared en metros: ");
      largo = input.nextDouble();
      System.out.print("Ingrese el alto de la pared en metros: ");
      alto = input.nextDouble();
      System.out.print("Ingrese el ancho de la pared en metros: ");
      ancho = input.nextDouble();

      // Solicita las dimensiones del ladrillo
      System.out.print("Ingrese el largo del ladrillo en metros: ");
      largoLadrillo = input.nextDouble();
      System.out.print("Ingrese el alto del ladrillo en metros: ");
      altoLadrillo = input.nextDouble();
      System.out.print("Ingrese el ancho del ladrillo en metros: ");
      anchoLadrillo = input.nextDouble();
```
Continua con el calculo del area de la pared a partir de las medidas pedidas, y lo mismo con el ladrillo.

```java
 // Calcula el área de la pared y del ladrillo
      areaPared = largo * alto;
      double areaLadrillo = largoLadrillo * altoLadrillo;
```

Por ultimo haciendo uso del metodo ceil, que aproxima al proximo número mayor o igual a otro número, se hace el calculo para tener una aproximación casi exacta de cuantos ladrillos se necesitan para rellenar el muro.

```java
cantidadLadrillos = Math.ceil(areaPared / (areaLadrillo * ancho / anchoLadrillo));
      // Muestra el resultado en la consola
      System.out.printf("Para construir la pared se necesitan %.0f ladrillos.", cantidadLadrillos);
```





