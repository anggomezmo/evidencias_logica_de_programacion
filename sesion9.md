<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 


# Ejercicios de Lógica de Programación

## 1. Calculadora de la mediana

La mediana es un valor estadístico que se utiliza para describir el centro de un conjunto de datos. Es el valor que se encuentra justo en el medio de un conjunto de datos ordenados de menor a mayor. Es decir, la mediana divide el conjunto de datos en dos partes iguales, donde la mitad de los valores están por encima de la mediana y la otra mitad están por debajo de ella.

Mediana con números impares:

Supongamos este grupo de números: {3, 7, 4, 2, 8}

Ordenarlos de menor a mayor: {2, 3, 4, 7, 8} El número de elementos es impar (5 elementos), por lo que la mediana será el elemento central una vez ordenados. El elemento central es el número 4. Por lo tanto, la mediana de este grupo de números impares es 4.

Mediana con números pares:

Supongamos este otro grupo: {5, 12, 2, 11, 3, 9}

Ordenarlos de menor a mayor: {2, 3, 5, 9, 11, 12} El número de elementos es par (6 elementos), por lo que la mediana será el promedio de los 2 elementos centrales una vez ordenados. Los elementos centrales son el 5 y el 9. El promedio de 5 y 9 es (5 + 9) / 2 = 7 Por lo tanto, la mediana de este grupo de números pares es 7.

La mediana es el elemento central de un grupo ordenado cuando la cantidad de elementos es impar. Y es el promedio de los dos elementos centrales cuando la cantidad es par.

# Solución.

### Para Arrays.
```java
import java.util.Arrays;
public class Mediana {
    public static void main(String[] args)  {
      int[] array1 = {2, 4, 6, 8, 10, 12};
        int[] array2 = {2, 4, 6, 8, 10, 12, 14};
        Arrays.sort(array1);
        Arrays.sort(array2);
        int tamaño1 = array1.length;
        int tamaño2 = array2.length;
        String resultado1 = parImpar(tamaño1);
        String resultado2 = parImpar(tamaño2);
        double mediana1 = calcularMediana(array1, resultado1, tamaño1);
        double mediana2 = calcularMediana(array2, resultado2, tamaño2);
        System.out.println("La mediana del arreglo 1 es: " + mediana1);
        System.out.println("La mediana del arreglo 2 es: " + mediana2);
    }

    public static String parImpar(int numero) {
        if (numero % 2 == 0) {
            return "par";
        } else {
            return "impar";
        }

    }

    public static double calcularMediana(int[] arreglo, String pariedad, int tamaño) {
        if (pariedad == "par") {
            int posicion2 = tamaño / 2;
            int posicion1 = posicion2 - 1;
            int num1 = arreglo[posicion1];
            int num2 = arreglo[posicion2];
            double mediana = (num1 + num2) / 2;
            return mediana;
        } else {
            int posicion = tamaño / 2;
           double mediana = arreglo[posicion];
            return mediana;
        }

    }
}
```

### Para introducir datos por consola (Arraylist):

```java

import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;public class MedianaArraylist {
   public static void main(String[] args) throws Exception {
         Scanner input = new Scanner(System.in);
        ArrayList<Double> array = new ArrayList<>();
        boolean parar = false;
        while (parar == false) {

            System.out.println("Ingrese un numero");
            String numero = input.nextLine();
            if ("q".equals(numero)) {
                break;
            }
            double numero1 = Double.parseDouble(numero);

            array.add(numero1);

        }

        Collections.sort(array);
        int tamaño = array.size();
        String resultado = parImpar(tamaño);
        double mediana = calcularMediana(array, resultado, tamaño);
     
        System.out.println("La mediana del arreglo es: " + mediana);
      
    }

    public static String parImpar(int numero) {
        if (numero % 2 == 0) {
            return "par";
        } else {
            return "impar";
        }

    }

    public static double calcularMediana(ArrayList<Double> arreglo, String pariedad, int tamaño) {
        if (pariedad == "par") {
            int posicion2 = tamaño / 2;
            int posicion1 = posicion2 - 1;
            double num1 = arreglo.get(posicion1);
            double num2 = arreglo.get(posicion2);
            double mediana = (num1 + num2) / 2;
            return mediana;
        } else {
            int posicion = tamaño / 2;
            double mediana = arreglo.get(posicion);
            return mediana;
        }

    }
}

```




