# [Cabecera de Métodos de la Clase](/java/c4how/u4objectBasedProgramming/u1publicViewOfClasses/u2methodSignatures/README.md)

**Sintaxis**

`public` `<tipo1>` `<nombreMetodo>` ( {`<tipo2>` `<parametro>`, ...} )

* el *tipo1* indica el **tipo del valor devuelto**, que puede ser:\_

	+ ***void***, nada, dado que el efecto será un cambio de estado en el objeto y/o sistema
	+ `<primitivo/Clase>`*, un valor de tipo primitivo o una referencia a un objeto de una clase
	+ `<primitivo/Clase>` **[ ]**, una referencia a un vector de valores de tipos primitivos o de referencias a objetos
	+ `<primitivo/Clase>` **[ ][ ]**, una referencia a una matriz de valores de tipos primitivos o de referencias a objetos
	+ …​

* el **nombre del método** debe comenzar con minúscula\_
* el *tipo2* puede ser igual que *tipo1* excepto\_ ***void***


	+ todos los **parámetros son pasados por valor**

```java
class Interval {
  public void shift(double shiftment) {...}
  public void adjust(Interval interval) {...}
  public double length() {...}
  public boolean includes(Interval interval) {...}
  public boolean equals(Interval interval) {...}
  public Interval symetric() {...}
  public Interval shifted(double shifment) {...}
  public Interval intersección(Interval interval) {...}
  public double[] values(int times) {...}
  public Interval[] split(int times) {...}
  ...
}
```
---

[Anterior](../u1className/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3methodOverloading/README.md)
