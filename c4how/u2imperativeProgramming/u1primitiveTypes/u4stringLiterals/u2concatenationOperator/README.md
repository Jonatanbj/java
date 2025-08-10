# [Operador de Concatenación](../u2concatenationOperator/README.md)


**Sintaxis:**

  * `<expresion>` ::= `<expresion>` + `<expresion>`

**Semántica:**

  * +, operador binario que, dados dos string, devuelve otra cadena de caracteres con los primeros caracteres iguales al primer string y los últimos caracteres iguales a los del segundo string

```java
class App {

  public static void main(String[] args) {
    Console console = new Console();
    console.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit.\n" +
        "Donec rhoncus sollicitudin enim vitae tempor.\n" +
        "Nullam dui lorem, vulputate varius sapien ac, malesuada dictum metus.\n" +
        "...");
    console.writeln("1" + "2" + "3" + "..."); // 123...
    console.writeln(535 + " * " + 723 + " = " + 535 * 723 + "."); // 535 * 723 = 386805.
  }
}
```
---

[Anterior](../u1Literalesdetipostring/README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u2imperativeProgramming/u1primitiveTypes/u5relationalOperators/README.md)
