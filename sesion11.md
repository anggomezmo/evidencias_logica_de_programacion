<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


# Actividad: Ejercicios de Lógica de Programación

1. Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

2. Desarrollar un algoritmo que realice la conversión de binario a decimal.

# Solución

## 1.  Encontrar elementos repetidos de un array.

```java
import java.util.ArrayList;

public class App {public static void main(String[] args) {
    // Declaramos un conjunto de números enteros
    int[] numeros = {1, 2, 3, 5, 3, 4, 5, 2};
    ArrayList<Integer> repetidos= new ArrayList<>();
    // Creamos una variable para almacenar el número que aparece más de una vez
    int numeroRepetido = 0;

    // Recorremos el conjunto de números
    for (int i = 0; i < numeros.length; i++) {
        // Comprobamos si el número actual ya ha aparecido
        for (int j = 0; j < i; j++) {
            if (numeros[i] == numeros[j]) {
                // El número actual ya ha aparecido
                numeroRepetido = numeros[i];
                // Verificar si el elemento esta en el arraylist
                if(repetidos.contains(numeroRepetido)){
                    continue;
                }else{
                    repetidos.add(numeroRepetido);
                }
                
            }
        }
    }
    // Ordenar lista
    repetidos.sort(null);
    // Si el número repetido es distinto de 0, lo imprimimos
    if(repetidos.size()==0){
        System.out.println("No hay ningún elemento repetido");
    }
    
    else{ for (Integer numero : repetidos) {
        System.out.println("El número "+numero+" se encuentra repetido.");
        
    }}
   
}
}


```

- Para la implementaciónm de esta variación unicamente se creo un arraylist donde iran almacenados los números repetidos, el método para encontrar los números repetidos sigue siendo el mismo.
- Para el proceso de almacenamiento se verifica previamente si el elemento repetido ya está en la lista para no almacenarlo más de una vez.
- Finalmente tras obtener los números repetidos se ordena el arraylist y se imprimen sus elementos

## 2. Conversión de número binario a decimal

```java
import java.util.ArrayList;
import java.util.Scanner;


public class BinarioDecimal {
    public static void main(String[] args) {
    
    Scanner input = new Scanner(System.in);
    System.out.println("Ingrese un número en binario: ");
    String binario= input.nextLine();
    ArrayList<Double> potencias = new ArrayList<>();
    int digitos= binario.length();
    // Agregar potencias al arraylist
    for(int i=0;i<digitos;i++){
       
        potencias.add(Math.pow(2, i));
    }// Imvertimos binario para trabajar con mayor comodidad
    String binarioInvertido="";
    for ( int i=digitos-1; i>=0;i--){
        binarioInvertido+=binario.charAt(i);
        }
   double decimal=0;
    for (int i=0; i<digitos;i++){
       double digito = Double.parseDouble( String.valueOf(binarioInvertido.charAt(i)));
       decimal+= digito*potencias.get(i);
    }
    int numeroFinal= (int) decimal;
    System.out.println("El número "+binario+" en el sistema númerico decimal es igual a: "+numeroFinal);
    }
}
```
Este programa permite convertir un número del sistema binario ingresado por consola y devolverlo en sistema decimal.

- Primero se cuenta la cantidad de digitos que tiene el binario para calcular las respetivas potencias de de dos y almacenarlas en un ArrayList.

- Luego se invierte el número binario para trabajar en el mismo orden del ArrayList de potencias.

- Finalmente se hace la respectiva operación para cada digito, multiplicando por su potencia de dos correspondiente.

- Acumulamos estos resultados en una variable para dar con el resultado de cual es el valor de nuestro nuevo número.


