# [Operadores unarios](../u2unaryOperators/README.md)

### Sintaxis

- *`<expresion>`** ::= `<operadorAritmeticoUnario>` `<expresion>`
- *`<operadorAritmeticoUnario>`** ::= - | +

### Semántica

- **+**: Identidad. Devuelve el mismo valor numérico dado.
- **-**: Opuesto. Devuelve el valor con el signo cambiado respecto al valor numérico dado.

```jaVA
class App {

  public static void main(String[] args) {
    Console console = new Console();
    console.writeln(+ -5); // -5
    console.writeln(- -5); // 5
  }
}
```
---

[Anterior](../u1literals/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3binaryOperators/README.md)
