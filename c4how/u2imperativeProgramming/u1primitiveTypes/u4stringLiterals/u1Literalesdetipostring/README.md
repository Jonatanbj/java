# [Literales de tipo string](../u1Literalesdetipostring/)



`<cadenaCaracteres>` **::=** **(** **"** **|** **'** **)**   `<caracter>` **(** **"** **|** **'** **)**
* donde
   * las comillas simples o compuestas de apertura y cierre deben ser iguales y distintas de cualquier caracter interior
   * `<caracter>` es
      * cualquiera caracter ASCII (espacio, letras, dígitos, símbolos de puntuación, …)
      * excluyendo aquellos no imprimibles (salto de línea, …) o con significado (comienzo de cadena, …) que deben precederse del caracter escape: \n, \t, …​ \", \', \" y \\ (tabla),
      * *\uXXXX* para caracteres de UTF-16 de Unicode
      * *\xXX* para caracteres de ASCII / ISO 8859-1 (Latin-1)
      * *\u{XXXXXX}* para caracteres de UTF-32
      * en todos los casos anteriores, X será un valor hexadecimal: *0, …, 9, A, …​, F*
* `<cadenaCaracteres>` **::=**  ( `<caracter>` **| ${** `<expresion>` } ) * 
   * para **plantillas literales**, cadenas literales que habilitan el uso de expresiones incrustadas
   * con los mismos caracteres que las cadenas anteriores pero sin necesidad de caracter de escape para las comillas, ni saltos de línea, …<br><br>

```java
class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln("cadena de caracteres con comillas dobles"); // cadena de caracteres con comillas dobles
        console.writeln("cadena de caracteres con comillas dobles 'con comillas simples' dentro"); // cadena de caracteres con comillas dobles 'con comillas simples' dentro
        console.writeln("cadena de caracteres\ncon salto de línea y \ttabulador"); // cadena de caracteres
        // con salto de línea y    tabulador
        console.writeln("Qué \"incomodo\" usar comillas con 'quit'!!!"); // Qué "comodo" usar comillas con normalidad sin 'escaparlas'!!!
        console.writeln(""); //  
        console.writeln("1"); // 1
        console.writeln("123"); // 123
        console.writeln("TRUE."); // TRUE.
        console.writeln("false"); // false
        
        console.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit.\n"+
        "Donec rhoncus sollicitudin enim vitae tempor.\n"+
        "Nullam dui lorem, vulputate varius sapien ac, malesuada dictum metus.\n"+
        "...");
    }

}

```


[Volver al nivel superior](../README.md)

[Siguiente sección: Operador de Concatenación](../u2concatenationOperator/README.md)
