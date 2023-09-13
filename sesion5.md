<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


# Actividad 5: Ejercicios de bucles

Resolver los siguientes ejercicios:

## Ejercicios - while
1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.
2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.
## Ejercicios - do while
1. Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.
2. Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.
## Ejercicios - for
1. Imprimir los números impares del 1 al 50.
2. Imprimir los números primos del 1 al 100.

# Solución

## Ejercicios - while

### Ejercicio 1.

```java
import java.util.*;

public class Ejercicio1 {
	 public static void main(String[] args) {
		   Scanner input = new Scanner(System.in);
		        System.out.println("Ingrese un número: ");
		        int num=input.nextInt();
		        int i=1;
		        System.out.println("Tabla de multiplicar del número "+num);
		        while(i<=10){
		             int result=i*num;
		             System.out.println(num+"x"+i+"="+result);
		             i++;
		            
		        }
}
}

```
### Ejercicio 2.

```java
import java.util.Scanner;

public class Ejercicio2 {
	 public static void main(String[] args) {
		   Scanner input = new Scanner(System.in);
		        System.out.println("Ingrese una cadena de caracteres: ");
		        String num=input.next();
		        int i=num.length();
		        int contador=0;
		        int auxiliar =0;
		      
		       while(auxiliar<i){
		             char letter=num.charAt(auxiliar);
		            if(Character.isDigit(letter)) {
		            	 contador++;
		            	 
		            	 
		             }auxiliar++;
		             
		             
		            
		        }
		       System.out.println("La cadena tiene "+contador+" caracteres númericos");
}
}

```
## Ejercicios - do while

### Ejercicio 1.

```java
import java.util.Scanner;
public class Ejercicio3 {

	public static void main(String[] args) {
	
Scanner input = new Scanner(System.in);
int i=1;
double parar;
do {
System.out.println(i);
System.out.println("Si desea parar introduzca un número negativo, de lo contrario introduzca uno positivo.");
 parar=input.nextDouble();
 i++;
}while(parar>=0 || i>100);

	}
}

```
### Ejercicio 2.

```java
import java.util.Scanner;

public class Ejercicio4 {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		int i=1;
		double parar;
		do {	
			System.out.println("Introduzca un número para mostrar su tabla de multiplicar: ");
			int num=input.nextInt();
			while(i<11) {
				int result=i*num;
				System.out.println(num+"x"+i+" = "+result);
				i++;
				
			}
			
			i=1;
			
			
			System.out.println("Si desea continuar introduzca un numero DISTINTO de 0");
			parar=input.nextDouble();
			
			  
		}while(parar!=0);

			}

	}

```
## Ejercicios - for

### Ejercicio 1.

```java

public class Ejercicio5 {

	public static void main(String[] args) {
		for(int i=1;i<50;i+=2) {
			
				System.out.println(i);
			
		}

	}

}

```
### Ejercicio 2.

```java
import java.util.Scanner;

public class Ejercicio4 {

	public class Ejercicio6 {

	public static void main(String[] args) {
		boolean esprimo;
		for(int i=1;i<100;i++) {
			esprimo=true;
			for(int j=i-1;j>=2;j--) {
				if(i%j==0) {
					
				esprimo=false;
				break;
				
				}
				
				
				}//fin segundo for
			
			if(esprimo) {
				System.out.println(i);
				
			}
		}
	}

}

```






