# [Operador Paréntesis](../u2parenthesisOperator/)

* **Sintaxis**:


	+ *`<expresion>`* **::=** **(** *`<expresión>`* **)**
<br><br>
* **Semántica**:


	+ devuelve la evaluación de la expresión anidada


<br><br>

```java
class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln(100/(2-1)); // ¿100 o 49?
        console.writeln(4>=7 && (2==4 || 5<6)); // ¿false o true?
        console.writeln(100/(2/2)); // ¿100 o 25?
        console.writeln(1-(1-1)); // ¿1 o -1?
        console.writeln(5 * (4+4) * 2); // ¿80 o 28?
        console.writeln((5+4) / (4+2)); // ¿1 u 8?
    }
}
```

<br><br>







| **Aplicaciones** |     |      |      |
| --- |---|---|---|
| [0-time/2-sibilings/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/0-time.md#2-sibilingsv0) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a2_sibilings/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a2_sibilings/v0_1/App.java) |[3-numbers/1-intergerDivision/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#1-integerdivisionv0) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a1_integerDivision/v0_0/App.java) - [v0.05](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a1_integerDivision/v0_05/App.java)|[3-numbers/2-percentage/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#2-percentagev0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a2_percentage/v0_0/App.java)|[3-numbers/3-even/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#3-evenv0) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a3_even/v0_0/App.java) - [v0.05](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a3_even/v0_05/App.java)|
| [3-numbers/4-absoluteValue/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#4-absolutevaluev0) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a4_absoluteValue/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a4_absoluteValue/v0_1/App.java) - [v0.2](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a4_absoluteValue/v0_2/App.java)|[1-space/0-square/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/1-space.md#0-squarev0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a1_space/a0_square/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a1_space/a0_square/v0_1/App.java)|[1-space/1-rectangle/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/1-space.md#1-rectanglev0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a1_space/a1_rectangle/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a1_space/a1_rectangle/v0_1/App.java)|[1-space/2-triangle/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/1-space.md#2-trianglev0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a1_space/a2_triangle/v0_0/App.java)|



---

[Volver al nivel superior](../README.md)



[Anterior](../u1precedenceAssociativity/README.md) | [Subir nivel](../README.md) | [Siguiente](../README.md)
