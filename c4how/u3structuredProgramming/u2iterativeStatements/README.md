# [Sentencias Iterativas](../u2iterativeStatements/README.md)

* **Sintaxis**:

	+ *`<sentencia>`* **::=** *`<sentenciaIterativa>`*
	+ *`<sentenciaIterativa>`* **::=** *`<sentenciaWhile>`* **|** *`<sentenciaDoWhile>`* **|** *`<sentenciaFor>`*
	+ *`<sentenciaWhile>`* **::=** **while** **(** *`<expresion>`* **)** *`<sentencia>`*
	+ *`<sentenciaDoWhile>`* **::=** **do** **{** *`<sentencia>`* **}** **while** **(** *`<expresion>`* **)** **;**
	+ *`<sentenciaFor>`* **::=** **for** **(** **[** *`<sentenciaLet>`* **]** **[** *`<expresion>`* **]** **;** **[** *`<expresion>`* **]** **)** *`<sentencia>`*
<br><br>
* **Semántica**:

	+ **Sentencia *while***, mientras se evalúa la expresión a cierto, ejecuta la sentencia de 0 a n veces
	+ **Sentencia *do-while***, ejecuta la sentencia mientras se evalúa la expresión a cierto de 1 a n veces
	+ **Sentencia *for***,
	
	
		- se crean los índices de las sentencia let
		- mientras se evalua a cierto la primera expresión, se ejecuta la sentencia y se evalúa la segunda expresión
<br>

```java

public class App {

    public static void main(String[] args) {
        Console console = new Console();
        int x = 3;
        while (x > 0)
            x--;
        console.writeln(x); // 0

        do {
            x++;
        } while (x < 3);
        console.writeln(x); // 3

        for (int i = 0, j = 9; i < j; i++, j--)
            console.writeln(i + " - " + j); // 0 - 9 / 1 - 8 / 2 - 7 / 3 - 6 / 4 - 5
    }
}
```

| **Aplicaciones** |--- |--- |
| --- |--- |--- |
| [4-validation](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#4-validationv0) - [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a4_validation/v0_0/App.adoc)|[3-numbers/0-multiplicationTable/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#0-multiplicationtable) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a0_multiplicationTable/v0_0/App.java) - [v0.4](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a0_multiplicationTable/v0_4/App.java)|[3-numbers/9-factorial/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#9-factorialv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a9_factorial/v0_0/App.java)|


---



[Anterior](../u1conditionalStatements/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3sequentialStatement/README.md)
