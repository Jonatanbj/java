# [Tipo string](../u4stringType/)


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


 |


---

[Volver al nivel superior](../README.md)

