# [Tipo boolean](./README.md)

**Sintaxis:**

`<expresion>` ::= `<expresion>` `<operadorRelacional>` `<expresion>`

`<operadorRelacional>` ::= ( `==` | `!=` )

**Semántica:** dados dos valores de tipo `boolean`, devuelve un valor de tipo `boolean` correspondiente a la igualdad o no de los respectivos operadores

`==`, igualdad en valor; `!=`, desigualdad en valor;

```java
class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln(true == true); // true
        console.writeln(true != false); // true
    }
}
```
---

[Volver al nivel superior](../README.md)

[Siguiente sección: Tipo string](../u4stringType/README.md)
