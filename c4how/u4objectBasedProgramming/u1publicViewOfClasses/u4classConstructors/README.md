# [Constructores de la Clase](/java/c4how/u4objectBasedProgramming/u1publicViewOfClasses/u4classConstructors/README.md)


* Son **métodos que reúnen las tareas de inicialización**, **no construyen**, y se lanzan implícimatemente en la construcción de objetos. Cumplen:


	+ no devuelven nada, ni **void**;
	+ deben coincidir su nombre con el de la clase;
	+ no se pueden lanzar mensajes que se correspondan con los constructores de la clase.\_

<br>

```java
class Interval {
  public Interval(double min, double max) {...}
  public Interval(double max) {...}
  public Interval() {...}
  public Interval(Interval interval) {...}
  public Interval(String string) {...}
  ...
}
```
---

[Anterior](../u3methodOverloading/README.md) | [Subir nivel](../README.md) | [Siguiente](../u5classDestructors//README.md)
