# Sentencias Alternativas






| Sentencia Alternativa | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<sentencia>* **::=** *<sentenciaAlternativa>* **|** *<sentenciaAlternativaMultiple>*
	+ *<sentenciaAlternativa>* **::=** **if (** *<expresion>* **)** *<sentencia>* **[** **else** *<sentencia>* **]** **;**

* *<sentenciaAlternativaMultiple>* **::=** **switch (** *<expresion>* **) {** **{** **case** *<literal>* **:** **{** *<sentencia>* **|** **break;** **}** **}** **[** **default:** **{** *<sentencia>* **|** **break;** **}** **]** **}** **;**
* **Semántica**:


	+ **Sentencia alternativa**, si se cumple la condición, ejecuta la sentencia
	+ **Sentencia alternativa compuesta**, si se cumple la condicion, ejecuta la primera sentencia, en caso contrario la segunda sentencia
	+ **Sentencia alternativa múltiple**, con ramas restringidas a casos concretos de valores, ejecuta desde la igualdad con la evaluación de la expresión hasta el final de la sentencia
	
	
		- **break**, termina la ejecución de la sentencia (p.e.: *for, …​*)
		
		
			* **No recomendado en ninguna otra situación**



 | 


```
package es.usantatecla.a0\_itinerario.a2\_estructurada.a1\_alternativa;

class App {
    
    public static void main(String[] args) {
        Console console = new Console();
        int x = 0;

        if (x>=0)
            x++;
        console.writeln(x); // 1
                    
        if (x>1)
            x++;
        else
            x--;
        console.writeln(x); // 0
        
        switch(x){
            case 3:
                console.writeln("esperado"); // 
                break;
            case 2:
                console.writeln("vulgar"); // 
            case 0:
            case 1:
                console.writeln("mágico"); // mágico
                break;
            default:
                console.writeln("otro"); // 
        }
    }
}
```


 |








| **Aplicaciones** |
| --- |
| 
* [0-time/2-sibilings/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/0-time.md#2-sibilingsv0) : [*v0.1*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a2_sibilings/v0_1/App.java) - [v0.2](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a2_sibilings/v0_2/App.java)


 | 
* [3-numbers/3-even/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#3-even) : [*v0.05*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a3_even/v0_05/App.java) - [v0.2](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a3_even/v0_2/App.java) - [v0.3](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a3_even/v0_3/App.java) - [v0.4](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a3_even/v0_4/App.java)


 | 
* [3-numbers/4-absoluteValue/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#4-absolutevalue) : [*v0.2*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a4_absoluteValue/v0_2/App.java) - [v0.3](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a4_absoluteValue/v0_3/App.java)


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Sentencias Iterativas](../u2iterativeStatements/README.md)
