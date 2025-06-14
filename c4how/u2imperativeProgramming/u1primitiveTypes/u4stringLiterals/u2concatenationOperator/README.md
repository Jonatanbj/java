# Operador de Concatenación






| Concatenación | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<expresion>* **::=** *<expresion> **+** <expresion>*

* **Semántica**:


	+ **+**, operador binario que, dados dos *string*, **devuelve otra cadena de caracteres con los primeros caracteres iguales al primer *string* y los últimos caracteres iguales a los del segundo *string***



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa.a1\_tipos.a2\_string.a2\_concatenacion;

class App {

  public static void main(String[] args) {
    Console console = new Console();
    console.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit.\n" +
        "Donec rhoncus sollicitudin enim vitae tempor.\n" +
        "Nullam dui lorem, vulputate varius sapien ac, malesuada dictum metus.\n" +
        "...");
    console.writeln("1" + "2" + "3" + "..."); // 123...
    console.writeln(535 + " * " + 723 + " = " + 535 * 723 + "."); // 535 * 723 = 386805.
  }
}
```


 |


---

[Volver al nivel superior](../README.md)

