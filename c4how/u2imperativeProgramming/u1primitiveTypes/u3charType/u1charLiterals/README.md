# Literales de tipo char






| char | *java* |
| --- | --- |
| 
* *<literal>* **::=** *<valorCaracter>*
* <valorCaracter> **::=** **'** *<caracter>* **'** **|** **'** **\** *<caracter>* **'**


	+ *<caracter>* son los caracteres imprimibles del código [ASCII](https://cs.stanford.edu/people/miles/iso8859.html) (espacio, letras, dígitos, símbolos de puntuación, …​)
	+ los caracteres "escapados" son aquellos que no son imprimibles (salto de línea, …​) o con sobrecarga de significados (apostrofe para comienzo de cadena, …​) que deben precederse del caracter escape: '\n', '\t', …​ '\"', '\'', '\"' y '\\',
	
	
		- *\uXXXX* para caracteres de [UTF-16 de Unicode](https://asecuritysite.com/coding/asc2)
		
		
			* donde X será un valor hexadecimal: *[0-9AF]*



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa.a1\_tipos.a4\_char.a1\_valores;

class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln('a'); // a
        console.writeln('1'); // 1
        console.writeln(' '); // 
        console.writeln('*'); // *
        console.writeln('\n'); // (salto de línea)
        console.writeln('\u3333'); // ?
    }

}
```


 |


---

[Volver al nivel superior](../README.md)

