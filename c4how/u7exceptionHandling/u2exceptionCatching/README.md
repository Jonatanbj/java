# [Captura de Excepciones](README.md)

| **Excepciones no comprobadas** | **Excepciones no comprobadas** | **Excepciones comprobadas**  |
| :--- | :--- | :--- |
| - elevadas por un método **pueden ser capturadas** en ese mismo método o en cualquier método que, directa o indirectamente, lo haya invocado | - si un método invoca otro método que eleva excepciones no comprobadas **no es necesario que las capture**, pero, en el caso de que se produzca la excepción, si ningún método captura la excepción, el **programa termina bruscamente** |- si un método invoca otro método que eleva excepciones comprobadas, entonces es **obligatorio que el método que invoca al otro capture** dichas excepciones|

<br>

**Sentencia *try/catch/finally*** 

* para capturar una excepción se debe usar la siguiente sentencia, donde se pueden **omitir la claúsula *catch* o *finally*, pero no ambas**:

<br>

```java
try {
     <sentencia1>
     ...
     <sentenciaN>
}
[
   catch (<declaraciónExcepción1>) {
     <sentencia11>
     ...
     <sentencia1N1>
}
...
   catch (<declaraciónExcepciónM>) {
    ...
}
]
[ finally {
  ...
} ]
```
<br>

* **Bloque *try***:


	+ indica las sentencias en cuya ejecución **se desea capturar una excepción**, en el caso de que ésta se produzca
	+ cuando se produce una excepción en alguna de sus sentencias, **se interrumpe bruscamente su ejecución** <br><br>

* **Bloque *catch***:


	+ especifican las **sentencias a ejecutar cuando se produzca una excepción** dentro del bloque try
	+ se debe especificar la **clase de excepción que queremos capturar** mediante la declaración de una excepción de esa clase
	+ opcionalmente, se pueden especificar **distintos bloques catch, para indicar distintos tratamientos** para distintas clases de excepciones
	+ es un error especificar más de un bloque catch para una misma clase de excepción;<br><br>

* **Bloque *finally***:


	+ **se ejecuta siempre**, después de la ejecución de *try/catch*
	+ sirve para **ejecutar un cierto código independientemente** de si se produce o no la excepción, si se captura o no, o de cualquier otra circunstancia;
	+ se suele usar para garantizar la **liberación de recursos**, por ejemplo, cerrar ficheros archivos abiertos, puertos de comunicaciones, etc.



<br>

 *Ejemplo*  

```java
package es.usantatecla.a5\_units.a0\_fraction.a5\_exceptions.a4\_catch;

public class App {

  public static void main(String[] args) {
    Console.getInstance().writeln("Inicio");
    try {
      Console.getInstance().writeln("Antes");
      new FractionView().writeln(new Fraction(3, 0));
      Console.getInstance().writeln("Después");
    } catch (ArithmeticException ex) {
      Console.getInstance().writeln("Error aritmetico");
      ex.printStackTrace();
    }
    Console.getInstance().writeln("Fin");
  }

}
```

<br>

 *Ejecución*

* *Ejemplo*: [*App.java*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a5_exceptions/a4_catch/App.java)



Inicio
Antes
Error aritmetico
`java.lang.ArithmeticException:` El denominador no puede ser 0
      `at` `Fraccion.<init>(Fraccion.java:10)`
      `at` `Aplicacion.main(Aplicacion.java:10)`
Fin


 *Ejemplo*  

```java
package es.usantatecla.a5\_units.a0\_fraction.a5\_exceptions.a5\_catchsFirst;

public class App {

  public static void main(String[] args) {
    Console.getInstance().writeln("Inicio");
    try {
      Console.getInstance().writeln("Antes");
      new FractionView().writeln(new Fraction("3/0"));
      Console.getInstance().writeln("Después");
    } catch (ArithmeticException ex) {
      Console.getInstance().writeln("Error aritmetico");
      ex.printStackTrace();
    } catch (NumberFormatException ex) {
      Console.getInstance().writeln("Error de formato");
      ex.printStackTrace();
    }
    Console.getInstance().writeln("Fin");
  }

}
```
 *Ejecución*
* *Ejemplo*: [*App.java*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a5_exceptions/a5_catchsFirst/App.java)


```
Inicio
Antes
Error aritmetico: El denominador no puede ser 0
Fin
```


 *Ejemplo*  

```java
package es.usantatecla.a5\_units.a0\_fraction.a5\_exceptions.a6\_catchsSecond;

public class App {

  public static void main(String[] args) {
    Console.getInstance().writeln("Inicio");
    try {
      Console.getInstance().writeln("Antes");
      new FractionView().writeln(new Fraction("3/a2"));
      Console.getInstance().writeln("Después");
    } catch (ArithmeticException ex) {
      Console.getInstance().writeln("Error aritmetico");
      ex.printStackTrace();
    } catch (NumberFormatException ex) {
      Console.getInstance().writeln("Error de formato");
      ex.printStackTrace();
    }
    Console.getInstance().writeln("Fin");
  }

}
```

 *Ejecución*| 
* *Ejemplo*: [*App.java*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a5_exceptions/a6_catchsSecond/App.java)



```
Inicio
Antes
Error de formato: Formato incorrecto
Fin
```

---


[Anterior](../u1exceptionThrowing/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3exceptionDelegation/README.md)
