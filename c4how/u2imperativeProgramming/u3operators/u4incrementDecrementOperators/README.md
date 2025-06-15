# [Operadores de Incremento y Decremento](../u4incrementDecrementOperators/README.md)



* **Sintaxis**:


	+ *`<sentencia>`* **::=** *`<expresion>`* **;**
	+ *`<expresion>`* **::=** **(** *`<identificador>`* *`<operadorIncrementoDecremento>`* **|** *`<operadorIncrementoDecremento>`* *`<identificador>`* **)**
	+ *`<operadorIncrementoDecremento>`* **::=** **++** **|** **--**
<br><br>
* **Semántica**:


	+ Abreviatura de: *<identificador>* **=** *<identificador>* *<operador>* **(** 1 **|** -1 **)**
	+ pero la expresión devuelve el valor de la variable **incrementada/decrementada** o o el valor **previo al incremento/decremento** dependiendo de si el operador es prefijo o postfijo respectivamente, en cualquier caso **modifica el valor de la variable**
	+ **No recomendado** como parte de otra expresión, con **efectos laterales**

<br><br>

```java

class App {

    public static void main(String[] args) {
        Console console = new Console();
        int x= 100;
        console.writeln(x); // 100
        console.writeln(x++); // 100
        console.writeln(++x); // 102
        console.writeln(x--); // 102
        console.writeln(--x); // 100
        console.writeln(- -x); // 100
        console.writeln(+ +x); // 100
        console.writeln(++x*2); // 202
        console.writeln(++x*2); // 204
        console.writeln(x++*2); // 204
        console.writeln(x); // 103
    }
}
```

<br><br>




[Volver al nivel superior](../README.md)

[Siguiente sección: Operador Coma](../u5commaOperator/README.md)
