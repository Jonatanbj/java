# [Literales](../u1literals/README.md)



### Sintaxis

- *`<literal>`** ::= `<valorNumerico>`  
- *`<valorNumerico>`** ::= `<parteEntera>` **[** `<parteDecimal>` **]** **[** `<exponente>` **]**  
- *`<parteEntera>`** ::= **[** `0b` **|** `0x` **]** `<signo>` `[0-9]+`  
- *`<parteDecimal>`** ::= `.` `[0-9]+`  
- *`<exponente>`** ::= `e` `<signo>` `[0-9]+`  
- *`<signo>`** ::= **[** `+` **|** `-` **]**

### Semántica

- Los prefijos **`0b`** y **`0x`** indican notación binaria y hexadecimal, respectivamente.  
- Todos los literales enteros serán de tipo **`int`**.  
- Todos los literales con decimales o notación científica serán de tipo **`double`**.



**Ejemplo** 

```JAVA
class App {

  public static void main(String[] args) {
    Console console = new Console();
    console.writeln(356); // 356
    console.writeln(-66); // -66
    console.writeln(34.45); // 34.45
    console.writeln(-2.343e-5); // -2.343E-5
    console.writeln(0); // 0
    console.writeln(-0); // 0
    console.writeln(-024); // -20
    console.writeln(0xA4); // 164
  }
``` 
---

[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](../u2unaryOperators/README.md)
