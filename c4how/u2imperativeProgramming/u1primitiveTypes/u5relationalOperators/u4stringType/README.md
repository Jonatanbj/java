# Tipo string






| Operadores binarios infijos, | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<expresion>* **::=** *<expresion> <operadorRelacional> <expresion>*
	+ *<operadorRelacional>* **::=** **(** **==** **|** **!=** **)**

* **Semántica**:


	+ dados dos *string*, devuelve un valor de tipo *boolean* correspondiente a la relación de cada operador según la exacta **igualdad** de la secuencia de caracteres
	
	
		- **==**, igualdad en valor;
		*****!=*, desigualdad en valor;



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa.a1\_tipos.a4\_relacional.a1\_string;

class App {

    public static void main(String[] args) {
        Console console = new Console();

        console.writeln("cadena" == "cadena"); // true
        console.writeln("cadena" != "cadena distinta"); // true 
    }
}
```


 |


---

[Volver al nivel superior](../README.md)

