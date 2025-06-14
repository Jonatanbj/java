# Operadores de Acumulación






| Operador de acumulación | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<sentencia>* **::=** *<expresion>* **;**
	+ *<expresion>* **::=** *<identificador>* *<operadorAcumulacion>* *<expresion>*
	+ *<operadorAcumulacion>* **::=** **+=** **|** **-=** **|** **\**=* **|** **\***=* **|** **/=** **|** **%=** **|** **&=** **|** **|=** **|** **^=** **|** **<⇐** **|** **>>=** **|** **>>>=**

* **Semántica**:


	+ Abreviatura de: *<identificador>* **=** *<identificador>* *<operador>* *<expresion>*
	+ **No recomendado como parte de otra expresión**, con **efectos laterales**, de tal forma que la evaluación de la nueva evaluación de la misma expresión arroja distintos resultados



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa.a3\_operadores.a4\_acumulador;

class App {

    public static void main(String[] args) {
        Console console = new Console();
        int x = 234;
        console.writeln(x += 2); // 236
        console.writeln(x -= 2); // 234
        console.writeln(x *= 2); // 468
        console.writeln(x /= 2); // 234
        console.writeln(x %= 7); // 3
        console.writeln(x |= 2); // 3
        console.writeln(x &= 2); // 2
        console.writeln(x ^= 3); // 1
        console.writeln(x <<= 2); // 4
        console.writeln(x >>= 2); // 1
        console.writeln(x >>>= 2); // 0
        console.writeln(x += 1 * 5); // 5
        console.writeln(x += 1 * 5); // 10
        console.writeln(x); // 10
    }
}
```


 |








| **Aplicaciones** |
| --- |
| 
* [4-numberingSystems/0-digits/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/4-numberingSystems.md#0-digitsv0) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a0_digits/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a0_digits/v0_1/App.java)


 | 
* [3-numbers/5-changeCoins/v1](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#5-changecoinsv1) : [*v1.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a5_changeCoins/v1_0/App.java) - [v1.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a5_changeCoins/v1_1/App.java)


 | 
* [4-numberingSystems/3-binaryToDecimal/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/4-numberingSystems.md#3-binaryToDecimalv0) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a3_binaryToDecimal/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a3_binaryToDecimal/v0_1/App.java)


 |
| 
* [4-numberingSystems/4-decimalToBinary/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/4-numberingSystems.md#4-decimaltobinaryv0) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a4_decimalToBinary/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a4_decimalToBinary/v0_1/App.java)


 |  |  |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Operadores de Incremento y Decremento](../u4incrementDecrementOperators/README.md)
