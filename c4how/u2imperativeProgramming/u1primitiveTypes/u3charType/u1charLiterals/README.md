# [Literales de tipo char](../u1charLiterals/README.md)

## Sintaxis


- **`<literal>` ::= `<valorCaracter>`** <br><br>

- **`<valorCaracter>` ::= `'` `<caracter>` `'`** &nbsp;|&nbsp; **`'\\'` `<caracter>` `'`** <br><br>

    - `<caracter>` son los caracteres imprimibles del código ASCII (espacio, letras, dígitos, símbolos de puntuación, …).<br>
    - Los caracteres "escapados" son aquellos que no son imprimibles (salto de línea, …) o tienen sobrecarga de significados (apóstrofe para comienzo de cadena, …) y deben precederse del carácter de escape: `'\n'`, `'\t'`, `'\"'`, `'\''`, `'\\'`.<br>
    - También se puede usar la notación Unicode: `'\uXXXX'` para caracteres de UTF-16 de Unicode, donde `X` es un valor hexadecimal (`0-9A-F`).<br> <br>

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

[Anterior: Boolean](/c4how/u2imperativeProgramming/u1primitiveTypes/u2booleanType/README.md)
[Siguiente: Literales String](/c4how/u2imperativeProgramming/u1primitiveTypes/u4stringLiterals/README.md)


[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](../README.md)
