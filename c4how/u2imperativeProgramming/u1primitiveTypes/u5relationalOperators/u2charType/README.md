# [Tipo char](../u2charType/README.md)




**Sintaxis:**

- `<expresion>` ::= `<expresion>` `<operadorRelacional>` `<expresion>`

- `<operadorRelacional>` ::= ( `==` | `!=` )

**Semántica:** dados dos `char`, devuelve un valor de tipo `boolean` correspondiente a la relación de cada operador según la exacta igualdad de los caracteres

- `==`, igualdad en valor; `!=`, desigualdad en valor;



```java

class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln('a'); // a
        console.writeln('1'); // 1
        console.writeln(' '); // 
        console.writeln('*'); // *
        console.writeln('\n'); // (salto de línea)
        console.writeln('\u3333'); // ?
    }

}
```


 |



---

[Volver al nivel superior](../README.md)

[Siguiente sección: Tipo boolean](../u3booleanType/README.md)
