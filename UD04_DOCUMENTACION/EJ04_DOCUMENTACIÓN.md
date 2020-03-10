# PR04_DOCUMENTACIÓN



En esta unidad:

* Git y gitHub. Control de versiones. 
* Javadoc. Documentación
* Refactorización

## 1. Git y github. Control de versiones. 

### 1.1. git

​	Git](https://git-scm.com) es un sistema de control de versiones cuyo cometido es tener controlados los cambios que se producen en los ficheros. Para ello, podemos decir que cuando se lo indicamos va tomando [_fotografías_](https://git-scm.com/book/es/v1/Empezando-Fundamentos-de-Git) de los ficheros y nos muestra qué cosas han cambiado en los ficheros desde la anterior fotografía a la actual.



Tutorial de git en youtube: https://www.youtube.com/watch?v=j8CSUPIB8mA&list=PLvimn1Ins-43-1sXQmGZPWLjNjPyGNi0R

Lista de comandos de git: https://gist.github.com/dasdo/9ff71c5c0efa037441b6



#### Prácticas 

*  http://aprendeconalf.es/curso-git 

* Documentos:
  * TallerdeGit.pdf
  * git-cosfer-dia1.pdf
  * libro:  https://git-scm.com/book/es/v2 

* git con eclipse (youtube):  https://www.youtube.com/watch?v=zkfzIGJditA 

### 1.2. Github

GitHub es un sistema de gestión de proyectos y control de versiones de código, así como una plataforma de red social diseñada para desarrolladores. ¿Pero para qué se usa GitHub? Bueno, en general, permite trabajar en colaboración con otras personas de todo el mundo, planificar proyectos y realizar un seguimiento del trabajo.

[GitHub](https://github.com/) es también uno de los [repositorios online más grandes](https://octoverse.github.com/) de trabajo colaborativo en todo el mundo.





### 1.3. Markdown

 Markdown es un lenguaje de marcado que *facilita la aplicación de formato* a un texto empleando una serie de caracteres de una forma especial. En principio, fue pensado para elaborar textos cuyo destino iba a ser la web con más rapidez y sencillez que si estuviésemos empleando directamente HTML. Y si bien ese suele ser el mejor uso que podemos darle, también podemos emplearlo para cualquier tipo de texto, independientemente de cual vaya a ser su destino. 



#### Prácticas

 https://markdown.es/ 



## 2. Documentación

### **2.1. Introducción** 

Documentar un proyecto es algo fundamental de cara al mantenimiento posterior. Cuando se desarrolla una clase, es conveniente generar documentación lo suficientemente detallada sobre ella como para que otros programadores sean capaces de usarla sólo con su interfaz. No debe existir necesidad de estudiar su implementación del mismo modo que para manejar una clase del API de Java no es necesario conocer su código fuente.

Al documentar una clase es conveniente incluir:

·     Nombre de la clase

·     Descripción general (*brief*) 

·     Versión

·     Autores

·     Documentación de cada constructor o método (especialmente los declarados como públicos):

o  Nombre del constructor o método

o  Tipo de retorno

o  Nombres y tipos de parámetros (si hay)

o  Descripción general

o  Descripción de parámetros (si hay)

o  Descripción del valor que devuelve

### 2.2. Javadoc



[Javadoc](https://es.wikipedia.org/wiki/Javadoc) es una utilidad para la generación de documentación de APIs a partir de código fuente Java. Viene con el propio JDK de Java y el resultado de la documentación que se genera está en formato HTML.

A grandes rasgos, es el método estándar para documentar clases de Java. La mayoría de los IDEs lo utilizan para generar de forma automática documentación de las clases, aunque existen otras herramientas que aportan distintas funcionalidades, como [Doxygen](http://www.doxygen.nl).

Para que javadoc genere documentación automáticamente hay que cumplir ciertas reglas:

·     La documentación para javadoc ha de incluirse entre símbolos de comentario que han de empezar con una barra y doble asterisco, y terminar con un asterisco y barra simple.

/**
 \* Comentario para javadoc
 */

·     La ubicación le define a javadoc qué representa el comentario: 

o  si está justo ANTES de la declaración de clase se considerará un comentario de clase, 

o  si está justo ANTES de la declaración de un constructor o método se considerará un comentario de ese constructor o método.

·     Para indicar a javadoc lo que significan los comentarios incluidos se usan ciertas palabras reservadas (tags) precedidas por "@", dentro de los símbolos de comentario javadoc. Si no existe al menos una línea que comience con @ no se reconocerá el comentario para la documentación de la clase. [Listado JavaSE EN](https://docs.oracle.com/javase/8/docs/technotes/tools/unix/javadoc.html#CHDBEFIF)



#### Prácticas

 https://www.discoduroderoer.es/como-utilizar-javadoc/ 





## 3. Refactorización





### ¿En qué consiste refactorizar?

*Refactorizar es un concepto interesante: consiste en mejorar el código poco a poco. Me gusta definirlo con una frase que aparece en el libro: así como con el tiempo el software se deteriora poco a poco, la refactorización debería mejorar el código poco a poco, sin realizar grandes cambios.*

*Cuando uno tiene entre sus manos un programa que no está en muy buenas condiciones, lo primero que desea es rehacerlo todo desde cero. Esto no es ni una posición realista, porque no se suele poder asumir el coste de una demolición y posterior construcción, ni respetuosa con los que lo programaron: no solemos saber las circunstancias en las que fue hecho ni los condicionantes de las decisiones. Frente a este deseo de rehacer todo surge el concepto de refactorización, que anima a ir cambiando el código a pasos pequeños y seguros.* [Fuente](https://www.adictosaltrabajo.com/2015/09/28/repasando-los-clasicos-refactoring-de-martin-fowler/)

La refactorización de código es la reescritura de una funcionalidad manteniendo su interfaz. Esto significa que se reemplaza el código pero se mantienen sus precondiciones y poscondiciones, es decir, lo que se debe aportar y lo que se debe obtener del código, respectivamente.

El objetivo puede ser variado, pero suele involucrar estos aspectos:

* Mejorar la reusabilidad. Crear componentes reutilizables.
* Optimizar un componente en términos de rendimiento.
* Corregir bugs provenientes de diseños erróneos.
* Generalizarlo para otros propósitos o entornos. Por ejemplo, parte del código responsable del acceso a los datos se puede refactorizar utilizando un framework que haga la aplicación independiente del DMBS utilizado.
* Mejorar la legibilidad del código.


### Bad smells ([Malos olores](https://es.wikipedia.org/wiki/Hediondez_del_código))

Son aquellos *síntomas* que se pueden encontrar en el código y que indican que probablemente existan otros problemas más profundos en la calidad del código, de diseño, o de ambos. 


* [Listado de algunos bad smells frecuentes](https://blog.intive-fdv.com.ar/repaso-los-code-smells-mas-comunes/)

* [Otro listado de bad smells ED](http://entornos.codeandcoke.com/doku.php?id=apuntes:refactorizacion#bad_smells)

### Refactorización en eclipse

* [Intro básica](https://tutobasico.com/refactoring-eclipse/)

* [Refactorización ED](http://entornos.codeandcoke.com/doku.php?id=apuntes:refactorizacion#refactorizacion_de_eclipse)


```java
public class GeneraPrimos {

	public static int[] generarPrimos(int max) {
		int i, j;
		
		if (max >= 2) {
		
			// Declaraciones
			
			int dim = max + 1; // Tamaño del array
			boolean[] esPrimo = new boolean[dim];
			
			// Inicializar el array
			for (i = 0; i < dim; i++) {
				esPrimo[i] = true;
			}
				
			// Eliminar el 0 y el 1, que no son primos
			esPrimo[0] = esPrimo[1] = false;
			
			// Se hace la criba de los que son múltiplos de otros y por tanto, no primos
			for (i = 2; i < Math.sqrt(dim) + 1; i++) {
				if (esPrimo[i]) {
					
					// Eliminar los múltiplos de i
					for (j = 2 * i; j < dim; j += i)
						esPrimo[j] = false;
				}
			}

			// ¿Cuántos primos hay?
			int cuenta = 0;
			for (i = 0; i < dim; i++) {
				if (esPrimo[i])
					cuenta++;
			}

			// Rellenar el vector de números primos
			
			int[] primos = new int[cuenta];
			
			for (i = 0, j = 0; i < dim; i++) {
				if (esPrimo[i])
					primos[j++] = i;
			}
			return primos;
			
		} else { 
			
			// max < 2
			return new int[0]; // Vector vacío
		}
	}

}
```

```java
public class demo {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int primos[];
		int limite = 125;
		primos = GeneraPrimos.generarPrimos(limite);
		
		System.out.println("Lista de números primos entre 0 y "+limite);
		for (int i=0; i<primos.length; i++) {
			System.out.println(primos[i]);
		}
	}

}

```

* [Refactorización números primos](http://elvex.ugr.es/decsai/java/pdf/8B-Refactoring.pdf)
* [Solución Refactorización primos](http://elvex.ugr.es/decsai/java/pdf/8B-Refactoring.solution.pdf)

#### Prácticas



Aprenderás:

* Cambiar nombre de variables

* Renombrear o mover una clase

* Extraer un método

  