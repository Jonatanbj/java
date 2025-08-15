# [Elevación de Excepciones](README.md)

**Sentencia *throw*** 

* durante la ejecución de un método se puede **elevar una excepción, para indicar que se ha producido un error de ejecución debido a alguna razón, lo que provoca la finalización brusca de su contexto de ejecución**

* para elevar una excepción se debe usar la siguiente sentencia:
 `throw` `<expresión>`**`(1)`**

**1** <br> donde la expresión debe evaluar a una **referencia a *Throwable***
* en un mismo método se pueden elevar, de forma alternativa, varias excepciones


```java

public class App {

  public static void main(String[] args) {
    Console.getInstance().writeln("Antes");
    new FractionView().writeln(new Fraction(3, 0));
    Console.getInstance().writeln("Despues");
  }
  
}
```

* *Ejemplo*: [*Fraction.java*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a5_exceptions/a1_arithmetic/Fraction.java)


Antes 
`Exception in thread "main" java.lang.ArithmeticException:` **El denominador no puede ser 0**
  `at` `Fraccion`.`<init>(Fraccion.java:10)`
  `at` `Aplicacion.main(Aplicacion.java:6)`


```java
package es.usantatecla.a5\_units.a0\_fraction.a5\_exceptions.a2\_format;

public class App {

  public static void main(String[] args) {
    Console.getInstance().writeln("Antes");
    new FractionView().writeln(new Fraction("2/a3"));
    Console.getInstance().writeln("Despues");
  }
  
}
```
 
* *Ejemplo*: [*FractionScanner.java*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a5_exceptions/a2_format/FractionScanner.java)


Antes
`Exception` `in` `thread` `"main"` `java.lang.NumberFormatException:` Formato incorrecto
  `at` `Fraccion.<init>(Fraccion.java:17)`
  `at` `Aplicacion.main(Aplicacion.java:6)`


**Cláusula *throws***
* las **únicas excepciones comprobadas que puede elevar un método son aquéllas cuyas clases se declaran en su cabecera** mediante la siguiente cláusula:


`<modificador>` `<tipo1>` `<nombreMétodo>`({`<tipo2>` `<parametro>`, }+)
       `throws` {`<claseExcepción1>`,}+


* como ya hemos visto, un método puede elevar excepciones no comprobadas sin necesidad de declarar sus clases en la cabecera, aunque puede ser **conveniente por razones de documentación**


	+ *Ejemplo*: [*Fraction.java*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a5_exceptions/a3_throws/Fraction.java)


```java
class Fraction {
  ...
  public void read(String path) throws IOException {
  ...
    if (<error de apertura>) {
      throw new IOException("Error al leer el fichero " + path);
    }
    ...
  }
  ...
}
```

---



[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](../u2exceptionCatching/README.md)
