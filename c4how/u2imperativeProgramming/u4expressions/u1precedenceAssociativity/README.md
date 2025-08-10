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


<br>


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



![Tabla de Precedencia](/images/tablaPrecedencia.webp)

| Precedencia | Operador                          | Tipo                                                                 | Asociatividad       |
|-------------|-----------------------------------|----------------------------------------------------------------------|---------------------|
| 15          | ()<br>[]<br>.                     | Paréntesis<br>Subíndice de arreglo<br>Selección de miembro          | Izquierda a derecha |
| 14          | ++<br>--                          | Post-incremento unario<br>Post-decremento unario                    | Derecha a izquierda |
| 13          | ++<br>--<br>+<br>-<br>!<br>~<br>(tipo) | Pre-incremento unario<br>Pre-decremento unario<br>Más unario<br>Menos unario<br>Negación lógica unaria<br>Complemento bit a bit unario<br>Conversión de tipo unaria | Derecha a izquierda |
| 12          | *<br>/<br>%                       | Multiplicación<br>División<br>Módulo                                | Izquierda a derecha |
| 11          | +<br>-                            | Adición<br>Sustracción                                               | Izquierda a derecha |
| 10          | << <br>>><br>>>>                  | Desplazamiento a la izquierda<br>Desplazamiento a la derecha con signo<br>Desplazamiento a la derecha sin signo | Izquierda a derecha |
| 9           | <<br><=<br>><br>>=<br>instanceof  | Menor que<br>Menor o igual que<br>Mayor que<br>Mayor o igual que<br>Comparación de tipo (solo objetos) | Izquierda a derecha |
| 8           | ==<br>!=                          | Igualdad<br>Desigualdad                                              | Izquierda a derecha |
| 7           | &                                 | AND bit a bit                                                        | Izquierda a derecha |
| 6           | ^                                 | XOR bit a bit                                                        | Izquierda a derecha |
| 5           | \|                                | OR bit a bit                                                         | Izquierda a derecha |
| 4           | &&                                | AND lógico                                                           | Izquierda a derecha |
| 3           | \|\|                              | OR lógico                                                            | Izquierda a derecha |
| 2           | ? :                               | Condicional ternario                                                 | Derecha a izquierda |
| 1           | =<br>+=<br>-=<br>*=<br>/=<br>%=   | Asignación<br>Asignación con suma<br>Asignación con resta<br>Asignación con multiplicación<br>Asignación con división<br>Asignación con módulo | Derecha a izquierda |                         | Derecha a izquierda |

_Mayor número indica mayor precedencia._

---

[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](../u2parenthesisOperator/README.md)
