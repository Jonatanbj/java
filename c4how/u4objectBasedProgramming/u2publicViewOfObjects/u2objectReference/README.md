# [Referencia a un objeto](/java/c4how/u4objectBasedProgramming/u2publicViewOfObjects/u2objectReference/README.md)


|  | **Sintaxis** |Ejemplo| 
| --- | --- | --- | 
| Es una variable puntero que alberga la dirección de un objeto de una clase.|![referencia](/images/Referencia%20(2).jpg) <br> - **final** obliga a la inicialización y fija su valor para la referencia|![ejemploreferencia](/images/EjemploReferencia%20(2).jpg)

**Operadores** 

* *`<referenciaO>` = `<direcciónO>`: asigna la dirección a la referencia siendo del mismo tipo;*
* *`<direcciónO-I>` == `<direcciónO-D>`: determina si dos direcciones a objetos de la misma clase son iguales;*
* *`<direcciónO-I>` != `<direcciónO-D>`: determina si dos direcciones a objetos de la misma clase son distintas;*

**Ejemplo:** 

```java
final Intervalo HORARIO = new Intervalo(7, 15);
Intervalo edades = new Intervalo(100);
Intervalo años;
años = edades;
boolean mismo = edades == años;
…
```
---

[Anterior](../u1objectCreation/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3messagePassing/README.md)
