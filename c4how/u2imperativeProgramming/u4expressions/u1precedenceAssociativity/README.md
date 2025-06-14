# Precedencia y asociatividad






| Expresiones | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ combinación
	
	
		- de operandos (literales, identifcadores de variables y constantes)
		- y operadores (prefijos, infijos, sufijos y ternarios)

* **Semántica**:


	+ cuya evaluación devuelve un valor de tipo primitivo
	
	
		- un **operando ambiguo, entre dos operadores,** alimenta al operador de mayor nivel de **precedencia**
		- ante el mismo nivel de precedencia, alimenta al operador de la **asociatividad** establecida para ese nivel de precedencia
		- estas reglas **no determinan el orden de evaluación**



 | 


```
package es.usantatecla.a0\_itinerario.a1\_imperativa.a4\_expresiones.a1\_asociatividad;

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


 |




![tablaPrecedencia](images/tablaPrecedencia.webp)


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Operador Paréntesis](../u2parenthesisOperator/README.md)
