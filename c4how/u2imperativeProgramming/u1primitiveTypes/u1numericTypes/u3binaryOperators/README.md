# Operadores binarios






| **Categoría** | **Descripción** |
|---------------|-----------------|
| **Sintaxis**  | <ul><li><code>&lt;expresion&gt;</code> **::=** <code>&lt;expresion&gt;</code> <code>&lt;operadorAritmetico&gt;</code> <code>&lt;expresion&gt;</code></li><li><code>&lt;operadorAritmetico&gt;</code> **::=** <code>-</code> **|** <code>*</code> **|** <code>/</code> **|** <code>%</code></li></ul> |
| **Semántica** | <ul><li>Operan sobre valores numéricos del mismo tipo, y devuelven un valor del tipo de los operandos (menos <code>byte</code>, <code>short</code> y <code>char</code>, que devuelven <code>int</code>).</li><li><strong>+</strong>, suma</li><li><strong>-</strong>, resta</li><li><strong>*</strong>, multiplicación</li><li><strong>/</strong>, división</li><li><strong>%</strong>, módulo resto</li></ul> |


```java
class App {

  public static void main(String[] args) {
    Console console = new Console();
    console.writeln(4 + 5); // 9
    console.writeln(4 - 5); // -1
    console.writeln(4 * 5); // 20
    console.writeln(4 / 5); // 0.8
    console.writeln(4 % 5); // 4

    //console.writeln(4 / 0); // Exception
    //console.writeln(4 % 0); // Exception

    console.writeln(0.1e-7 + 1e7); // 1.000000000000001E7
    console.writeln(0.1e-8 + 1e8); // 1.0E8
    console.writeln(0.1 + 0.2); // 0.30000000000000004
  }
}
```


 |


---

[Volver al nivel superior](../README.md)

