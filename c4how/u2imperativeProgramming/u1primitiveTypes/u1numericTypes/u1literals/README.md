# [Literales](../u1literals/README.md)






| **Aspecto**   | **Descripción**                                                                                                                                                                                                                                                                                                                                                   |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sintaxis**  | - *<literal>* **::=** *<valorNumerico>* <br> - *<valorNumerico>* **::=** *<parteEntera>* **[** *<parteDecimal>* **]** **[** *<exponente>* **]** <br> - *<parteEntera>* **::=** **[** **0b** **|** **0x** **]** <br> - *<signo>* **[0.9]** **+** <br> - *<parteDecimal>* **::=** **.[0.9]** **+** <br> - *<exponente>* **::=** **e** *<signo>* **[0-9]** **+** <br> - *<signo>* **::=** **[** **+** **|** **-** **]** |
| **Semántica** | - Prefijos **0b** y **0x** son respectivamente para notación binaria y hexadecimal. <br> - Todos los literales enteros serán de tipo ***int***. <br> - Todos los literales con decimales o notación científica serán de tipo ***double***.



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

[Volver al nivel superior](../README.md)

[Siguiente sección: Operadores unarios](../u2unaryOperators/README.md)
