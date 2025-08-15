# [Delegación de Excepciones](README.md)

**Delegación**  
* si el **método no captura una excepción, la propaga al método que lo invocó**


	+ si un método declara que eleva excepciones comprobadas, entonces **no necesita capturar esas clases de excepciones que declara**, cuando **invoca métodos que elevan esas mismas clases de excepciones**

* *Ejemplo*: [*App.java*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a5_exceptions/a7_nested/App.java)

<br>

```
Antes
Error aritmetico
java.lang.ArithmeticException: El denominador no puede ser 0
         at Fraccion.<init>(Fraccion.java:17)
         at Fraccion.crearFraccion(Fraccion.java:26)
         at Aplicacion.main(Aplicacion.java:14)
Fin
```

*Ejemplo* 

```java
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
    } catch (NumberFormatException ex) {
      Console.getInstance().writeln("Error de formato");
      ex.printStackTrace();
    }
    Console.getInstance().writeln("Fin");
  }

  public static Fraction createFraction(int numerator, int denominator) throws ArithmeticException {
    return new Fraction(numerator, denominator);
  }

}
```

---



[Anterior](../u2exceptionCatching/README.md) | [Subir nivel](../README.md) | [Siguiente](../u4polymorphicExceptions/README.md)
