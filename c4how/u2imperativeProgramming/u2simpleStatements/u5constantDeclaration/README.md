# [Sentencia de Declaración de Constante](../u5constantDeclaration/README.md)






| Sentencia de Declaración de Constante | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *`<sentencia>`* **::=** **final** **(** **byte** **|** **short** **|** **int** **|** **long** **|** **float** **|** **double** **|** **char** **|** **boolean** **|** **String** **)** *`<identificador>` **=** `<expresion>`* **;**
<br><br>
* **Semántica**:


	+ referenciable desde las expresiones del ámbito de la declaración pero **no mutable!!!**



```java
class App {

    public static void main(String[] args) {
        Console console = new Console();
        final String CONSTANT = "constante";
        console.writeln("Esto es " + CONSTANT + "!!!"); // Esto es constante
        // CONSTANT = "mutacion"; Error!!!
    }
}
```





| **Aplicaciones** | --- | --- | --- | --- | --- |
| --- | --- | --- | --- | --- | --- | 
|* [2-texts/1-echo/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#1-echov0) : [*v0.1*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a1_echo/v0_1/App.java) - [v0.2](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a1_echo/v0_2/App.java) | * [2-texts/1-echo/v1](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#1-echov1) : [v1.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a1_echo/v1_0/App.java) | * [0-time/0-units/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/0-time.md#0-unitsv0) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a0_units/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a0_units/v0_1/App.java) - [v0.2](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a0_units/v0_2/App.java) |* [1-space/0-square/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/1-space.md#0-squarev0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a1_space/a0_square/v0_0/App.java) | * [3-numbers/1-intergerDivision/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#1-integerdivisionv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a1_integerDivision/v0_0/App.java) |  * [3-numbers/5-changeCoins/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#5-changecoinsv0) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a5_changeCoins/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a5_changeCoins/v0_1/App.java) |





---

[Volver al nivel superior](../README.md)
[Siguiente sección: Operadores ](/c4how/u2imperativeProgramming/u3operators/README.md)

