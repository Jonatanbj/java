
# [Operadores unarios](../u2unaryOperators/README.md)

| **Aspecto**   | **Descripción**|
|---------------|----------------|
| **Sintaxis**  | `<expresion>` **::=** `<operadorAritmeticoUnario>` `<expresion>`<br>`<operadorAritmeticoUnario>` *::= -* +`                                                                   |
| **Semántica** | Operan sobre valores numéricos del mismo tipo, y devuelven un valor del tipo de los operandos (excepto `byte`, `short` y `char`, que devuelven `int`).               |
| **Operadores**| `+` (identidad): Devuelve el mismo valor numérico dado.<br>`-` (opuesto): Devuelve el valor con cambio de signo respecto al valor numérico dado.                     |

```java
class App {

  public static void main(String[] args) {
    Console console = new Console();
    console.writeln(+ -5); // -5
    console.writeln(- -5); // 5
  }
}
```
---

[Anterior](../u1booleanValues/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3binaryOperators/README.md)
