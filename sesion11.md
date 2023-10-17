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





