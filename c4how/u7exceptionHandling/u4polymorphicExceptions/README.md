# Excepciones Polimorficas






| 
* cuando un método captura una excepción, **sólo se ejecuta la primera sentencia *catch* en la que la referencia de la excepción producida encaje en la clase de excepción declarada** en esa sentencia *catch*;
* *Ejemplo*: [*App.java*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a5_exceptions/a8_polymorphic/App.java)






```
Inicio
Antes
Error aritmetico : El denominador no puede ser 0
Fin
```


 | 


```
package es.usantatecla.a5\_units.a0\_fraction.a5\_exceptions.a8\_polymorphic;

public class App {

  public static void main(String[] args) {
    Console.getInstance().writeln("Inicio");
    try {
      Console.getInstance().writeln("Antes");
      new FractionView().writeln(App.createFraction(3, 0));
      Console.getInstance().writeln("Después");
    } catch (ArithmeticException ex) {
      Console.getInstance().writeln("Error aritmetico");
      ex.printStackTrace();
    } catch (Exception ex) {
      Console.getInstance().writeln("Error");
      ex.printStackTrace();
    }
    Console.getInstance().writeln("Fin");
  }

  public static Fraction createFraction(int numerator, int denominator) throws ArithmeticException {
    return new Fraction(numerator, denominator);
  }

}
```


 |
| 
* es un **error de compilación tratar de capturar una excepción en una sentencia *catch*, que ya ha sido capturada previamente** en otra sentencia *catch*;


	+ *Ejemplo*: [*App.java*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a5_exceptions/a9_polymorphic2/App.java)



 | 


```
package es.usantatecla.a5\_units.a0\_fraction.a5\_exceptions.a9\_polymorphic2;

public class App {

  public static void main(String[] args) {
    Console.getInstance().writeln("Inicio");
    try {
      Console.getInstance().writeln("Antes");
      new FractionView().writeln(App.createFraction("3/a2"));
      Console.getInstance().writeln("Después");
    } catch (Exception ex) {
      Console.getInstance().writeln("Error");
      ex.printStackTrace();
    } // catch (ArithmeticException ex) { Error compilación!!! Excepcion previamente capturada
      // Console.getInstance().writeln("Error aritmetico");
      // ex.printStackTrace();
    // } 
    Console.getInstance().writeln("Fin");
  }

  public static Fraction createFraction(String string) throws ArithmeticException, NumberFormatException {
    return new Fraction(string);
  }

}
```


 |







| 
* los **métodos pueden elevar excepciones de clases hijas de las declaradas** en su cabecera mediante la cláusula *throws*;
* los **métodos redefinidos** en una clase


	+ pueden **eliminar excepciones de la cláusula *throws* de su cabecera de aquéllas que estaban declaradas en la cabecera del método en su clase padre**
	+ pueden **sustituir excepciones en la cláusula *throws* de su cabecera por otros excepciones de sus clases hijas**;
	+ **NO** pueden **añadir nuevas excepciones en la cláusula *throws* de su cabecera respeto a aquéllas que estaban declaradas en la cabecera del método en su clase padre**



 | 


```
clase Base  {

  public void m() throws Exception { ... }

  public void n() throws Exception { ... }
}

class Derivada extends Base  {

  public void m() throws IOException {
    ...
    throw new FileSystemException() ;
    ...
  }

  public void n() {
    ...
  }
}
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Clasificación de Excepciones](../u5exceptionClassification/README.md)


[Anterior](../u3exceptionDelegation/README.md) | [Subir nivel](../README.md) | [Siguiente](../u5exceptionClassification/README.md)
