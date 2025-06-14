# Entrada de Datos






| Entrada de datos | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<expresion>* **::=** **console.** **read**[red]**(** **Byte** **|** **Short** **|** **Int** **|** **Long** **|** **Float** **|** **Double** **|** **Char** **|** **Boolean** **|** **String** **)** **(** **[** *<String>* **]** **)**

* **Semántica**: devuelve el valor del tipo correspondiente (numérico, carácter, lógico vs *string*) introducido por el usuario tras la interrumpción de la ejecución hasta que el usuario pulsa *enter* (introducir, no entrar!!!)


	+ El parámetro opcional indica el *string* que se mostrará antes de la entrada de datos para guiar al usuario



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa.a2\_sentenciasSimples.a2\_entrada;

class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln("El siguiente es " + console.readInt("Dame un número: ") + 1);
    }
}
```


 |








| **Aplicaciones** |
| --- |
| 
* [2-texts/0-regards/v3](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#0-regardsv3) : [v3.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a0_regards/v3_0/App.java)


 | 
* [2-texts/1-echo/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#1-echov0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a1_echo/v0_0/App.java)


 |  |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Sentencia de Declaración de Variable](../u3variableDeclaration/README.md)
