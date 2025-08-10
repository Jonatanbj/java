# [Tipo numerico](../u1numericType/README.md)

**Sintaxis:**

- `<expresion>` ::= `<expresion>` `<operadorRelacional>` `<expresion>`

- `<operadorRelacional>` ::= ( `==` | `!=` | `<` | `⇐` | `>` | `>=` )

**Semántica:** dados dos valores del mismo tipo numérico, devuelve un valor de tipo boolean correspondiente a la relación de cada operador según el orden de los números reales

- `==`, igualdad en valor; `!=`, desigualdad en valor; `<`, menor; `⇐`, menor o igual; `>`, mayor; `>=`, mayor o igual

```java

class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln(5 == 5);  // true
        console.writeln(5 != 6); // true
        console.writeln(5 < 6); // true
        console.writeln(5 <= 5); // true
        console.writeln(5 > 4); // true
        console.writeln(5 >= 5); // true
    }
}
```
---
[Anterior](../u1numericType/README.md) | [Subir nivel](../README.md) | [Siguiente](../u2charType/README.md)
