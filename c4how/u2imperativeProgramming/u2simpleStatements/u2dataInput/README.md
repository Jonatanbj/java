# [Entrada de Datos](../u2dataInput/README.md)

* **Sintaxis**:


  * `<expresion>` ::= **console.** **read**[red]**(** **Byte** **|** **Short** **|** **Int** **|** **Long** **|** **Float** **|** **Double** **|** **Char** **|** **Boolean** **|** **String** **)** **(** **[** *`<String>`* **]** **)**<br><br>

* **Semántica**: devuelve el valor del tipo correspondiente (numérico, carácter, lógico vs *string*) introducido por el usuario tras la interrumpción de la ejecución hasta que el usuario pulsa *enter* (introducir, no entrar!!!)


	+ El parámetro opcional indica el *string* que se mostrará antes de la entrada de datos para guiar al usuario


```java

class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln("El siguiente es " + console.readInt("Dame un número: ") + 1);
    }
}
```

| **Aplicaciones** | **Aplicaciones** |
| --- | --- | 
| * [2-texts/0-regards/v3](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#0-regardsv3) : [v3.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a0_regards/v3_0/App.java) | * [2-texts/1-echo/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#1-echov0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a1_echo/v0_0/App.java) |

---

[Anterior](../u1dataOutput/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3variableDeclaration/README.md)
