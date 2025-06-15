# [Literales de tipo char](../u1charLiterals/README.md)

## Sintaxis


- *\<literal>*  **::=** *\<valorCaracter>* <br><br>
- *\<valorCaracter>*  **::=** **'** *\<caracter>* **'** **\|** **'** **\\** *\<caracter>* **'** <br><br>

   * *<caracter>* son los caracteres imprimibles del código ASCII (espacio, letras, dígitos, símbolos de puntuación, …)<br><br>
   * los caracteres "escapados" son aquellos que no son imprimibles (salto de línea, …) o con sobrecarga de significados (apostrofe para comienzo de cadena, …) que deben precederse del caracter escape: '\n', '\t', …​ '\"', '\'', '\"' y '\\',<br><br>
      * *\uXXXX* para caracteres de UTF-16 de Unicode<br><br>
         * donde X será un valor hexadecimal: *[0-9AF]*

### Caracteres Escapados

Los caracteres "escapados" son aquellos que:
- No son imprimibles (salto de línea, …)
- Tienen sobrecarga de significados (apóstrofe para comienzo de cadena, …)
- Deben precederse del caracter escape

| Caracter Escapado | Descripción |Caracter Escapado | Descripción |
|-------------------|-------------|-------------------|-------------|
| `'\n'` | Salto de línea | `'\\'` | Barra invertida |
| `'\t'` | Tabulación |`'\''` | Apóstrofe |
| `'\"'` | Comillas dobles |






```java
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

