# [Tipo char](../u3charType/README.md)

## Literales de tipo char


- `<literal>` ::= `<valorCaracter>`
- `<valorCaracter>` ::= ' `<caracter>` ' | ' \ `<caracter>` '`

    - `<caracter>` son los caracteres imprimibles del código ASCII (espacio, letras, dígitos, símbolos de puntuación, …​).
    - Los caracteres "escapados" son aquellos que no son imprimibles (salto de línea, …​) o con sobrecarga de significados (apóstrofe para comienzo de cadena, …​) que deben precederse del carácter escape: `'\n'`, `'\t'`, …​ `'\\"'`, `'\''`, `'\\"'` y `'\\\\'`.

        - `\uXXXX` para caracteres de UTF-16 de Unicode.
        - Donde `X` será un valor hexadecimal: `[0-9A-F]`.


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

[Anterior](../u3binaryOperators/README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u2imperativeProgramming/u1primitiveTypes/u4stringLiterals/README.md)
