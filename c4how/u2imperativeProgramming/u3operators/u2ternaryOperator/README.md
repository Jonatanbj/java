# Operador Ternario






| Operador ternario | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<expresion>* **::=** *<expresion>* **?** *<expresion>* **:** *<expresion>*

* **Semántica**:


	+ devuelve
	
	
		- **la evaluación del segundo argumento** **si** **la evaluación del primer argumento resulta cierto**
		- o **la evaluación del tercero argumento en caso contrario**



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa.a3\_operadores.a3\_ternario;

class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln(true ? "si / entonces / segundo / izquierda" 
                    : "no / en caso contrario / tercero / derecha "); // si / entonces / segundo / izquierda
        console.writeln(false ? -1 : +1); // 1
    }
}
```


 |








| **Aplicaciones** |
| --- |
| 
* [0-time/1-major/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/0-time.md#1-majorv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a1_major/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a1_major/v0_1/App.java)


 | 
* [3-numbers/5-changeCoins/v1](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#5-changecoinsv1) : [v1.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a5_changeCoins/v1_0/App.java)


 | 
* [0-time/2-sibilings/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/0-time.md#2-sibilingsv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a2_sibilings/v0_0/App.java)


 |
| 
* [3-numbers/3-even/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#3-evenv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a3_even/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a3_even/v0_1/App.java)


 | 
* [3-numbers/4-absoluteValue/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#4-absolutevaluev0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a4_absoluteValue/v0_0/App.java)


 |  |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Operadores de Acumulación](../u3compoundOperators/README.md)
