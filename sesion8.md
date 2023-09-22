<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


# Actividad: Ejecicios de métodos en Java

Implementar los siguientes métodos:

1. Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
2. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
3. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
4. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
5. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

# Solución

Se implementaron todos los métodos en una misma clase, y en el main se ejecuta cada unp, pidiendo al usuario por consola los argumentos para ejecutar los metodos. Adicionalmente se hizo en una misma clase para mostrar la versatilidad de los métodos.

```java
import java.util.Arrays;
import java.util.Scanner;

public class Actividad8 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // prueba del METODO1

        System.out.println("Ejercicio 1");
        System.out.println("Ingrese el primer valor: ");
        double valor1 = input.nextDouble();
        System.out.println("Ingrese el segundo valor: ");
        double valor2 = input.nextDouble();
        double mayor = numeroMayor(valor1, valor2);
        System.out.println("El numero mayor es " + mayor);
        System.out.println("--------------------------------");
        System.out.println("Ejercicio 2");

        // prueba del METODO2

        System.out.println("Ingrese una cadena de texto: ");
        input.nextLine();
        String string1 = input.nextLine();
        int vocales = numeroVocales(string1);
        System.out.println("El string tiene " + vocales + " vocales");
        System.out.println("--------------------------------");
        System.out.println("Ejercicio 3");

        // prueba del METODO3

        System.out.println("Ingrese una cadena de texto con mayusculas y minusculas: ");
        String string2 = input.nextLine();
        String cadena = convertirLetras(string2);
        System.out.println("La cadena con mayusculas y minusculas invertidas es: " + cadena);
        System.out.println("--------------------------------");
        System.out.println("Ejercicio 4");

        // prueba del METODO4

        System.out.println("Ingrese una oración: ");
        String string3 = input.nextLine();
        int palabras = contarPalabras(string3);
        System.out.println("El número de palabras del String es: " + palabras);
        System.out.println("--------------------------------");
        System.out.println("Ejercicio 5");

        // prueba del METODO5

        System.out.println("Ingrese una oración: ");
        String string4 = input.nextLine();
        String cadena2 = ordenaString(string4);
        System.out.println("Las palabras del string ordenadas alfebeticamente son: " + cadena2);
        System.out.println("--------------------------------");
    }

    // METODO 1: DEVOLVER EL NÚMERO MAYOR.
    public static double numeroMayor(double a, double b) {
        double mayor;
        if (a > b) {
            mayor = a;
        } else {
            mayor = b;
        }
        return mayor;
    }

    // METODO 2: DEVOLVER NUMERO DE VOCALES DE CADENA DE TEXTO.

    public static int numeroVocales(String a) {
        int vocales = 0;
        for (int i = 0; i < a.length(); i++) {
            char letra = a.charAt(i);
            String letraString = String.valueOf(letra);
            switch (letraString) {
                case "a":
                case "e":
                case "i":
                case "o":
                case "u":
                    vocales++;
                    break;
                default:
                    break;
            }
        }
        return vocales;
    }

    // METODO 3: Mayusculas/Minusculas
    public static String convertirLetras(String a) {
        String cadena = "";
        String letra;
        char caracter;

        for (int i = 0; i < a.length(); i++) {
            caracter = a.charAt(i);

            if (Character.isUpperCase(caracter)) {
                caracter = Character.toLowerCase(caracter);
            } else {
                caracter = Character.toUpperCase(caracter);
            }
            letra = String.valueOf(caracter);
            cadena += letra;

        }
        return cadena;
    }

    // METODO 4 : Número de palabras

    public static int contarPalabras(String a) {
        String[] palabras = a.split(" ");
        return palabras.length;
    }
    // METODO 5: Ordenar palabras alfabeticamente.
    public static String ordenaString(String a) {

        String[] palabras = a.split(" ");
        String cadena = "";
        Arrays.sort(palabras);
        for (String string : palabras) {
            cadena += string + " ";
        }
        return cadena;
    }

}

```





