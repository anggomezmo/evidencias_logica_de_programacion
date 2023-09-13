<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 


# Actividad 3: Ejercicios de operaciones básicas en Java. :computer: :coffee: 
1. Suma y multiplicación: Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.

2. Resta y división: Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.

3. Operaciones combinadas: Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.

4. Operaciones con decimales: Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.

5. Incremento y decremento: Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.

6. Operador de asignación compuesta: Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.

7. Operadores lógicos: Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.

8. Operador ternario: Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.

# Solución.

## Ejercicio 1.

```java
 package Ejercicios;
import java.util.Scanner;
public class Ejercicio1 {
	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
			System.out.println("Ingrese el primer valor: ");
		int numero1= input.nextInt();
		System.out.println("Ingrese el segundo valor: ");
		int numero2= input.nextInt();
		
		int multipliacion= numero1*numero2;
		int suma= numero1+numero2;
		System.out.println("La suma de los valores es: "+suma);
		System.out.println("La multuplicacion es: "+ multipliacion);
		input.close();
	}
}
```

## Ejercicio 2.

```java
package Ejercicios;
import java.util.Scanner;
public class Ejercicio2 {
	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
			System.out.println("Ingrese el primer valor: ");
		int numero1= input.nextInt();
		System.out.println("Ingrese el segundo valor: ");
		int numero2= input.nextInt();
		
		double division= numero1/numero2;
		int resta= numero1-numero2;
		System.out.println("La division de los valores es: "+division);
		System.out.println("El valor de la resta es: "+ resta);
		input.close();
	}
}

```

## Ejercicio 3.

```java
package Ejercicios;
import java.util.Scanner;
public class Ejercicio3 {
	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		System.out.println("Ingrese el primer valor: ");
		int numero1= input.nextInt();
		System.out.println("Ingrese el segundo valor: ");
		int numero2= input.nextInt();
		System.out.println("Ingrese el tercer valor: ");
		int numero3= input.nextInt();
		
		int suma= numero1+numero2+numero3;
		int multiplicacion= numero1*numero2;
		double resultado=multiplicacion/numero3;
		System.out.println("La suma de los valores es: "+suma);
		System.out.println("El valor de la multiplicación entre el numero 1 y 2 es: "+ multiplicacion);
		System.out.println("El valor de la division entre el resultado anterior y el numero 3 es: "+ resultado);
		input.close();
	}
}


```

## Ejercicio 4.

```java
package Ejercicios;

import java.util.Scanner;

public class Ejercicio4 {
	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		System.out.println("Ingrese el primer valor: ");
		double numero1= input.nextDouble();
		System.out.println("Ingrese el segundo valor: ");
		double numero2= input.nextDouble();
	
		double suma= numero1+numero2;
		double resta= numero1-numero2;
		double multiplicacion= numero1*numero2;
		double division= numero1/numero2;
		System.out.println("La suma de los valores es: "+suma);
		System.out.println("La resta de los valores es: "+resta);
		System.out.println("La multiplicacion de los valores es: "+multiplicacion);
		System.out.println("La division de los valores es: "+division);
		
		input.close();
	}
}

```

## Ejercicio 5.

```java
package Ejercicios;

public class Ejercicio5 {
	public static void main(String[] args) {
		
		int valor=8;
		int incremento=valor+1;
		System.out.println("El valor incrementado es: "+incremento);
		int decremento=valor-1;
		System.out.println("El valor decrecido es: "+ decremento);
	}
}

```

## Ejercicio 6.

```java
package Ejercicios;

public class Ejercicio6 {
public static void main(String[] args) {
		
		int valor=8;
		valor+=5;
		System.out.println("El valor incrementado es: "+valor);
		
	}
}

```

## Ejercicio 7.

```java
package Ejercicios;

import java.util.Scanner;

public class Ejercicio7 {
	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		System.out.println("Ingrese el primer valor booleano: ");
		boolean numero1= input.nextBoolean();
		
		System.out.println("Ingrese el segundo valor booleano: ");
		boolean numero2= input.nextBoolean();
		boolean AND=numero1 && numero2;
		boolean OR=numero1 || numero2;
		boolean NOT1=!numero1;
		boolean NOT2=!numero2;
		System.out.println("La operación logica AND da como resultado: "+AND);
		System.out.println("La operación logica OR da como resultado:"+OR);
		System.out.println("La negación del primer valor es: "+NOT1);
		System.out.println("La negación del segundo valor es: "+NOT2);
		
		input.close();
	}
}


```

## Ejercicio 8.

```java
package Ejercicios;

import java.util.Scanner;

public class Ejercicio8 {
	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		System.out.println("Ingrese un valor: ");
		int numero= input.nextInt();
		String mensaje=(numero>=0) ? "El número es positivo":"El número es negativo";
		System.out.println(mensaje);
		input.close();
	}
}


```






