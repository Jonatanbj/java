# Constructores de la Clase






| **Descripción** | **Ejemplo** |
| --- | --- |
| 
* Son **métodos que reúnen las tareas de inicialización**, **no construyen**, y se lanzan implícimatemente en la construcción de objetos. Cumplen:


	+ no devuelven nada, ni **void**;
	+ deben coincidir su nombre con el de la clase;
	+ no se pueden lanzar mensajes que se correspondan con los constructores de la clase.\_



 | 


```
class Interval {
  public Interval(double min, double max) {...}
  public Interval(double max) {...}
  public Interval() {...}
  public Interval(Interval interval) {...}
  public Interval(String string) {...}
  ...
}
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Destructores de la Clase](../u5classDestructors/README.md)
