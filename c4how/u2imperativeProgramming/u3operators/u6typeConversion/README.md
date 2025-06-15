# Conversión de Tipos







| 
* **Promoción**: transforman un dato de un tipo a otro con el mismo o mayor espacio en memoria para almacenar información;
* **Contracción**: transforman un dato de un tipo a otro con menor espacio en memoria para almacenar información con la consecuente **posible pérdida de información**;


 | 

conversion

 | 
* **Conversión implícita**:


	+ por promoción cuando se combinan dos operandos de distinto tipo, se convierte el de menor precisión al de mayor precisión;
	+ por promoción cuando se asigna un valor de un tipo de menor precisión a una variable de mayor precisión;



 |







| - **Conversión explícita**: | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<expresion>* **::=** **(** <tipo> **)** *<expresion>*
	+ \_<tipo> **::=** **byte** **|** **short** **|** **int** **|** **long** **|** **float** **|** **double** **|** **char** **|** **boolean**

* **Semántica**:


	+ por promoción o contracción a través del **operador de conversión de tipos** (*cast*), cuyo nivel de precedencia es el de los operadores unarios;



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa.a3\_operadores.a2\_conversion;

class App {

    public static void main(String[] args) {
        Console console = new Console();
        byte id1 = 127;
        console.writeln(id1); // 127
        id1 = (byte) 128;
        console.writeln(id1); // -128
        short id2 = id1;
        console.writeln(id2); // -128
        int units = 13;
        console.writeln(units/2); // 6
        console.writeln((float) units/2); // 6.5
    }
}
```


 |


---

[Volver al nivel superior](../README.md)
[Operadores de Bits](u1bitwiseOperators/README.md)
