# [Sentencia de Asignación](../u4assignmentStatement/README.md)

* **Sintaxis**:

	+ *`<expresion>`* **::=** *`<identificador>`* **=** *`<expresion>`* **;**
<br><br>
* **Semántica**:

	+ como "sentencia", asigna/ actualiza/ "iguala", …​, *set, move, :=*, …​, con **efecto lateral**: asignando a la variable identificada a la izquierda el resultado de la evaluacíon de la expresión **con restricción al tipo de la variable, lenguaje con sistema de tipos estático!!!**
	+ como operador, **devuelve**, el **valor recién asignado** a la variable

		- **No recomendado como parte de otra expresión**


```java

class App {

    public static void main(String[] args) {
        Console console = new Console();
        int x;
        int y;
        int z = -1;
        x = y = z;
        console.writeln(x); // -1
        x = 0;
        console.writeln(x); // 0
        x = x + 1;
        console.writeln(x); // 1
        console.writeln(x + 1); // 2
        console.writeln(x); // 1
        console.writeln(x = x + 1); // 2
        console.writeln(x); // 2
    }
}
```
<br>

| **Aplicaciones** |--- | --- | 
| --- | --- | --- | 
| * [3-numbers/5-changeCoins/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#5-changecoinsv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a5_changeCoins/v0_0/App.java) - [v0.01](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a5_changeCoins/v0_01/App.java) | * [4-numberingSystems/0-digits/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/4-numberingSystems.md#0-digitsv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a0_digits/v0_0/App.java) | * [4-numberingSystems/3-binaryToDecimal/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/4-numberingSystems.md#3-binaryToDecimalv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a3_binaryToDecimal/v0_0/App.java) | 




---

[Anterior](../u3variableDeclaration/README.md) | [Subir nivel](../README.md) | [Siguiente](../u5constantDeclaration/README.md)
