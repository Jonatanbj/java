# Tipo boolean


##### Valores de tipo *boolean*







| boolean | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<literal>* **::=** *<valorLogico>*
	+ *<valorLogico>* **::=** **true** **|** **false**

* **Semántica**:


	+ correspondientes con cierto y false respectivamente



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa. a1\_tipos.a3\_boolean.a1\_valores;

public class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln(true); // true
        console.writeln(false); // false
    }
}
```


 |




##### Operadores unarios







| operador unario prefijo | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<expresion>* **::=** **!** *<expresion>*

* **Semántica**:


	+ **!**, negación lógica, el opuesto



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa.a1\_tipos.a3\_boolean.a2\_unarios;

public class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln(!false); // true
        console.writeln(!true); // false
    }
}
```


 |




##### Operadores binarios







| operadores binarios infijos | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<expresion>* **::=** *<expresion>* *<operadorBinarioLogico>* *<expresion>*
	+ *<operadorBinarioLogico>* **::=** **&&** **|** **||**

* **Semántica**:


	+ **&&**, y-lógico: devuelve la evaluación de la primera expresión, **no *true***, cuando **ambos operandos son evalúan a cierto**
	+ **||** , o-lógico: **devuelve la evaluación de la primera expresión**, **no *true*** **cuando es cierto o, caso contrario, la evaluación de la segunda expresión cuando es cierta**
	+ ***false*** en casos contrarios



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa.a1\_tipos.a3\_boolean.a3\_binarios;

public class App {

    public static void main(String[] args) {
        Console console = new Console();

        console.writeln(false && false); // false
        console.writeln(false && true); // false
        console.writeln(true && false); // false
        console.writeln(true && true); // true

        console.writeln(false || false); // false
        console.writeln(false || true); // true
        console.writeln(true || false); // true
        console.writeln(true || true); // true
    }

}
```


 |



---

[Volver al nivel superior](../README.md)

[Siguiente sección: Tipo string](../u4stringType/README.md)
