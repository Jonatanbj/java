# [Tipo string](../u4stringType/README.md)


**Operadores binarios infijos, Java**

**Sintaxis:**

* `<expresion>` ::= `<expresion>` `<operadorRelacional>` `<expresion>`

* `<operadorRelacional>` ::= ( `==` | `!=` )

**Semántica:**

* dados dos `string`, devuelve un valor de tipo `boolean` correspondiente a la relación de cada operador según la exacta igualdad de la secuencia de caracteres

    * `==`, igualdad en valor; `!=`, desigualdad en valor;


```java
class App {

    public static void main(String[] args) {
        Console console = new Console();

        console.writeln("cadena" == "cadena"); // true
        console.writeln("cadena" != "cadena distinta"); // true 
    }
}
```

---

[Anterior](../u3booleanType/README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u2imperativeProgramming/u2simpleStatements/README.md)
