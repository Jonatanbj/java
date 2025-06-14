# Referencia a un objeto







|  | **Sintaxis** | **Ejemplo** |
| --- | --- | --- |
| 
Es una variable puntero que alberga la dirección de un objeto de una clase.
 | 

height32



* **final** obliga a la inicialización y fija su valor para la referencia


 | 

height32

 |







| **Operadores** | **Ejemplo:** |
| --- | --- |
| 
* *<referenciaO> = <direcciónO>: asigna la dirección a la referencia siendo del mismo tipo;*
* *<direcciónO-I> == <direcciónO-D>: determina si dos direcciones a objetos de la misma clase son iguales;*
* *<direcciónO-I> != <direcciónO-D>: determina si dos direcciones a objetos de la misma clase son distintas;*


 | 


```
final Intervalo HORARIO = new Intervalo(7, 15);
Intervalo edades = new Intervalo(100);
Intervalo años;
años = edades;
boolean mismo = edades == años;
…
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Paso de mensajes](../u3messagePassing/README.md)
