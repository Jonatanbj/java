# [Operadores binarios](../u3binaryOperators/README.md)






## [Operadores Binarios Infijos Java ](../u3binaryOperators/README.md)

### Sintaxis


- *`<expresion>`*  **::=** *`<expresion>`* *`<operadorBinarioLogico>`* *`<expresion>`*  
- *`<operadorBinarioLogico>`*  **::=** **&&** **\|** **\|\|**

### Semántica


- **&&**  y-lógico  Devuelve la evaluación de la primera expresión, **no *true***, cuando **ambos operandos evalúan a cierto**
- **\|\|**  o-lógico  **Devuelve la evaluación de la primera expresión**, **no *true*** **cuando es cierto o, caso contrario, la evaluación de la segunda expresión cuando es cierta**
- ***false*** en casos contrarios |


```java
public class App {

    public static void main(String[] args) {
        Console console = new Console();

        console.writeln(false && false); // false
        console.writeln(false && true); // false
        console.writeln(true && false); // false
        console.writeln(true && true); // true

        console.writeln(false || false); // false
        console.writeln(false || true); // true
        console.writeln(true || false); // true
        console.writeln(true || true); // true
    }

}
```
---

[Anterior](../u2unaryOperators/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3charType/README.md)
