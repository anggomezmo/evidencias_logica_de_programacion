<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


# Actividad 4: Ejercicios de control de flujo con expresiones compuestas

```java
// Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;
```
Con la información anterior, implementa los siguientes ejercicios:

1. Determinar si el estudiante es mayor de edad y tiene un estado activo.
2. Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
3. Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
4. Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
5. Mostrar toda la información del estudiante si está matriculado en el Cesde.
6. Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
7. Determinar la cantidad de beca que recibe el estudiante según su promedio:
- 0.0 - 3.4: El estudiante no recibe beca.
- 3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
- 4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
- 4.5 - 5.0: El estudiante recibe una beca completa.

# Solución.

En el siguiente programa se encuentran los 7 ejercicios solicitados y los 3 adicionales inventados.

```java
public class Trabajo4 {
	  public static void main(String[] args) {
	        // Variables de tipo String
	        String nombre = "Juan Pérez";
	        String apellido = "González";
	        String identificación = "1000000001";
	        String correo = "juan.perez@ejemplo.com";
	        String carrera = "Desarrollo de Software";
	        String universidad = "Cesde";
	// Variable de tipo int
	        int edad = 20;
	// Variable de tipo boolean
	        boolean esActivo = true;
	        boolean becado = false;
	// Variable de tipo char
	        char género = 'M';
	// Variable de tipo double
	        double promedio = 4.5;
	// Variable de tipo int
	        int semestre = 2;

	        System.out.println("EJERCICIO 1.");
	        System.out.println("Determinar si el estudiante es mayor de edad y tiene un estado activo.");
	        if (edad >= 18) {

	            System.out.println("El estudiante es mayor de edad");
	            if (esActivo) {
	                System.out.println("El estudiante es activo");
	            } else {
	                System.out.println("El estudiante no es activo");
	            }
	        } else {
	            System.out.println("El estudiante no es mayor de edad");
	            if (esActivo) {
	                System.out.println("El estudiante es activo");
	            } else {
	                System.out.println("El estudiante no es activo");
	            }
	        }

	        System.out.println("------------------------------------------");
	        System.out.println("EJERCICIO 2.");
	        System.out.println("Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.");

	        if (becado) {
	            System.out.println("El estudiante es becado");
	        } else {
	            System.out.println("El estudiante no es becado");
	        }
	        if (carrera == "Desarrollo de Software") {
	            System.out.println("El estudiante estudia desarrollo de software");
	        } else {
	            System.out.println("El estudiante no estudia desarrollo de software");
	        }

	        System.out.println("------------------------------------------");

	        System.out.println("EJERCICIO 3.");
	        System.out.println("Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.");

	        if (semestre == 3 && esActivo == true) {
	            System.out.println("El estudiante es activo y esta en su ultimo semestre");

	        } else {
	            System.out.println("El estudiante no es activo o no esta en su ultimo semestre");
	        }
	        System.out.println("------------------------------------------");

	        System.out.println("EJERCICIO 4.");
	        System.out.println("Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.");

	        if (carrera == "Desarrollo de Software" && promedio >= 4.0) {
	            System.out.println("El estudiante estudia desarrollo de software y tiene un promedio superior a 4");
	        } else {
	            System.out.println("El estudiante no estudia desarrollo de software o no tiene un promedio superior a 4");
	        }

	        System.out.println("------------------------------------------");
	        System.out.println("EJERCICIO 5.");
	        System.out.println("Mostrar toda la información del estudiante si está matriculado en el Cesde..");

	        if (universidad == "Cesde") {

	            System.out.println("nombre: " + nombre);
	            System.out.println("apellido: " + apellido);
	            System.out.println("identificación: " + identificación);
	            System.out.println("carrera: " + carrera);
	            System.out.println("universidad: " + universidad);

	        }
	        System.out.println("------------------------------------------");
	        System.out.println("EJERCICIO 6.");
	        System.out.println("Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.");

	        if (universidad == "Cesde" && promedio >= 4.0 && esActivo) {
	            System.out.println("El estudiante ganó una beca porque cumple los requisitos");

	        } else {
	            System.out.println("Una o varias de las condiciones no se cumple por lo que no ganó la beca");
	            }
	            System.out.println("------------------------------------------");
	            System.out.println("EJERCICIO 7.");
	            System.out.println("Determinar la cantidad de beca que recibe el estudiante según su promedio:\n"
	                    + "0.0 - 3.4: El estudiante no recibe beca.\n"
	                    + "3.5 - 3.9: El estudiante recibe una beca parcial del 25%.\n"
	                    + "4.0 - 4.4: El estudiante recibe una beca parcial del 50%.\n"
	                    + "4.5 - 5.0: El estudiante recibe una beca completa.");
	            System.out.println("");
	            if (promedio>=0 && promedio<=3.4) {
	                System.out.println("El estudiante no recibe beca");
	                
	            }
	            else if (promedio>=3.5 && promedio<=3.9) {
	                System.out.println("El estudiante recibe una beca parcial del 25%");
	                
	            }else if (promedio>=4.0 && promedio<=4.4) {
	                System.out.println("El estudiante recibe una beca parcial del 50%");
	                
	            }else{
	                System.out.println("El estudiante recibe una beca completa.");
	                System.out.println("------------------------------------------");
	                
	                System.out.println("EJERCICIO 8.");
	    	        System.out.println("Determinar el genero del estudiante: ");  
	    	        
	    	        if(Character.toString(género).matches("M")) {
	    	        	System.out.println("El estudiante es hombre");
	    	        	
	    	        	
	    	        }else {
	    	        	System.out.println("El estudiante es mujer");
	    	        }
	                
	    	        System.out.println("------------------------------------------");
		            System.out.println("EJERCICIO 9.");
		            System.out.println("Determinar si el estudiante es hombre y tiene más de 18 años");
		            
	    	        if(Character.toString(género).matches("M")) {
	    	        	
	    	        	if(edad>18) {
	    	        		System.out.println("El estudiantes es hombre y mayor de 18");
	    	        	}
	    	        	
	    	        }else {
	    	        	System.out.println("El estudiante no es hombre o no es mayor de "
	    	        			+ "18");
	    	        	
	    	        }
	    	        System.out.println("------------------------------------------");
	    	        
	    	        System.out.println("EJERCICIO 10.");
		            System.out.println("Determinar si el estudiante es Juan Pérez: ");
		            if(nombre=="Juan Pérez") {
		            	System.out.println("El estudiantes es Juan Pérez");
		            }
		            else {
		            	System.out.println("El estudiantes no es Juan Pérez");
		            }
		            	
	            }
	            
	        

	    }

}
```





