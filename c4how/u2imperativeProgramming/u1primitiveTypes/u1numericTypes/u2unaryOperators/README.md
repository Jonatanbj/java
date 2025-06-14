# Operadores unarios






| **Concepto**       | **Descripción**                                                                                                                                                                                                 |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sintaxis**        | + *<expresion>* **::=** *<operadorAritmeticoUnario>* *<expresion>*<br>+ *<operadorAritmeticoUnario* **::=** **-** **|** **+**                                                                                   |
| **Semántica**       | + Operan sobre valores numéricos del mismo tipo, y devuelven un valor del tipo de los operandos (menos *byte, short* y *char*, que devuelven *int*).<br>    - **+**, identidad, devuelve el mismo valor numérico dado.<br>    - **-**, opuesto, devuelve el valor con cambio de signo respecto al valor numérico dado. |


```jaVA
class App {

  public static void main(String[] args) {
    Console console = new Console();
    console.writeln(+ -5); // -5
    console.writeln(- -5); // 5
  }
}
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Operadores binarios](../u3binaryOperators/README.md)
