# Conversión de Tipos


| Concepto | Codigo UNICODE. | 
| --- | --- | 
| **Promoción:** transforman un dato de un tipo a otro con el mismo o mayor espacio en memoria para almacenar información; <br> <br> **Contracción :** Transforman un dato de un tipo a otro con menor espacio en memoria, lo que puede con llevar **posible pérdida de información**. <br> <br> **Conversión implícita:** Por promoción al combinar operandos de distinto tipo: <br>  + se convierte el de menor precisión al de mayor precisión. <br>   Por promoción al asignar un valor de tipo de menor precisión a una variable de mayor precisión. |  ![Descripción de la imagen](/images/conversion.png)  | 










| 
* **Sintaxis**:


	+ *`<expresion>`* **::=** **(** `<tipo>` **)** *`<expresion>`*
	+ \_`<tipo>` **::=** **byte** **|** **short** **|** **int** **|** **long** **|** **float** **|** **double** **|** **char** **|** **boolean**
<br><br>
* **Semántica**:


	+ por promoción o contracción a través del **operador de conversión de tipos** (*cast*), cuyo nivel de precedencia es el de los operadores unarios;



<br><br>


```java

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



---

[Volver al nivel superior](../README.md)
[Siguiente sección: Expresiones](/c4how/u2imperativeProgramming/u4expressions/README.md)
