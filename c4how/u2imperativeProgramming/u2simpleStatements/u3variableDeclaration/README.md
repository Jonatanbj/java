# Sentencia de Declaración de Variable






| Sentencia de Declaración de Variable | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<sentencia>* **::=** **(** **byte** **|** **short** **|** **int** **|** **long** **|** **float** **|** **double** **|** **char** **|** **String** **|** **boolean** **)** *<identificador> [ **=** <expresion> **];***
	+ *<identificador>* **::=** [ a - zA - Z\_$ ] [ a - zA - z0 - 9\_$ ]*
	
	
		- **distinto** de cualquier **otro identificador** del mismo ámbito y de cualquier **palabra reservada**: *const, let, if, for, function, new, …​*
		- **estilo**: ***camelCase***: palabras yuxtapuestas con la inicial en mayúsculas a partir de la segunda palabra

* **Semántica**:


	+ **Reserva de memoria** para
	
	
		- **almacenar un único valor**, y posteriormente,
		- **consultar su valor** si ha sido inicializada o asignada previamente y
		- **modificar su valor mediante la asignación del valor de la evalución de una expresión**,
		- **desde la línea de la declaración hasta el final del ámbito que encierra la declaración**



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa.a2\_sentenciasSimples.a3\_variable;

class App {

    public static void main(String[] args) {
        Console console = new Console();
        int identifier = 0;
        console.writeln("Valor actual ." + identifier + "."); // Valor actual .0.
        console.writeln("Valor siguiente ." + (identifier + 1) + "."); // Valor siguiente .1.
        console.writeln("Valor actual ." + identifier + "."); // Valor actual .0.
        int identifierWithoutInitialization;
        //console.writeln("." + identifierWithoutInitialization + "."); // Error
        byte code = 127;
        short age = -1000;
        long euros = 1234567890;
        float distance; // conversion
        double lighYear = 0.0234;
        char initial = 'A';
        boolean error = false;
    }
}
```


 |
| 
**Palabras Reservadas**
 |
| 

palabrasReservadas

 |








| **Aplicaciones** |
| --- |
| 
* [2-texts/0-regards/v3](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#0-regardsv3) : [*v3.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a0_regards/v3_0/App.java) - [v3.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a0_regards/v3_1/App.java)


 | 
* [2-texts/0-regards/v4](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#0-regardsv4) : [v4.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a0_regards/v4_0/App.java)


 | 
* [2-texts/1-echo/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#1-echov0) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a1_echo/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a1_echo/v0_1/App.java)


 |
| 
* [0-time/0-units/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/0-time.md#0-unitsv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a0_units/v0_0/App.java)


 |  |  |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Sentencia de Asignación](../u4assignmentStatement/README.md)
