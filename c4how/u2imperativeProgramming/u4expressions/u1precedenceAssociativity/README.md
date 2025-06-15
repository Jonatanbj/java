# [Precedencia y asociatividad](../u1precedenceAssociativity/README.md)






* **Sintaxis**:


	+ combinación
	
	
		- de operandos (literales, identifcadores de variables y constantes)
		- y operadores (prefijos, infijos, sufijos y ternarios)
<br><br>
* **Semántica**:


	+ cuya evaluación devuelve un valor de tipo primitivo
	
	
		- un **operando ambiguo, entre dos operadores,** alimenta al operador de mayor nivel de **precedencia**
		- ante el mismo nivel de precedencia, alimenta al operador de la **asociatividad** establecida para ese nivel de precedencia
		- estas reglas **no determinan el orden de evaluación**


<br><br>


```java

class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln(100/2-1); // ¿100 o 49?
        console.writeln(4>=7 && 2==4 || 5<6); // ¿false o true?
        console.writeln(100/2/2); // ¿100 o 25?
        console.writeln(1-1-1); // ¿1 o -1?
        console.writeln(5 * 4+4 * 2); // ¿80 o 28?
        console.writeln(5+4 / 4+2); // ¿1 u 8?
    }
}
```

<br><br>
imnagen original 
# [TablaPrecedencia](images/tablaPrecedencia.webp)

| Precedencia | Operador                   | Tipo                                                                 | Asociatividad       |
|-------------|----------------------------|----------------------------------------------------------------------|---------------------|
| 15          | () [] .                    | Paréntesis, subíndice de arreglo, selección de miembro               | Izquierda a derecha |
| 14          | ++ --                      | Incremento y decremento postfijo                                     | Derecha a izquierda |
| 13          | ++ -- + - ! ~ (tipo)       | Prefijo, unario, conversión de tipo                                  | Derecha a izquierda |
| 12          | * / %                      | Multiplicación, división, módulo                                     | Izquierda a derecha |
| 11          | + -                        | Suma y resta                                                         | Izquierda a derecha |
| 10          | << >> >>>                  | Desplazamientos a nivel de bits                                      | Izquierda a derecha |
| 9           | < <= > >= instanceof       | Relacionales y prueba de tipo                                        | Izquierda a derecha |
| 8           | == !=                      | Igualdad y desigualdad                                               | Izquierda a derecha |
| 7           | &                          | AND a nivel de bits                                                  | Izquierda a derecha |
| 6           | ^                          | XOR a nivel de bits                                                  | Izquierda a derecha |
| 5           | \|                         | OR a nivel de bits                                                   | Izquierda a derecha |
| 4           | &&                         | AND lógico                                                           | Izquierda a derecha |
| 3           | \|\|                       | OR lógico                                                            | Izquierda a derecha |
| 2           | ? :                        | Condicional ternario                                                 | Derecha a izquierda |
| 1           | = += -= *= /= %=           | Asignación y asignaciones compuestas                                 | Derecha a izquierda |

_Mayor número indica mayor precedencia._


![tablaPrecedencia](images/tablaPrecedencia.webp)


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Operador Paréntesis](../u2parenthesisOperator/README.md)
