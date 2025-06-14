# Sobrecarga de Métodos de la Clase






| **Descripción** | **Ejemplo** |
| --- | --- |
| 
* Varios métodos pueden tener el mismo nombre con las siguientes restricciones:


	+ **si están en la misma clase**, deben **diferenciarse en el número o tipo de parámetros comparados dos a dos**;
	+ **si están en distintas clases**, no existe restricción;



 | 


```
class Interval {
  public Interval(double min, double max) {...}
  public Interval(double max) {...}
  public Interval() {...}
  public Interval(Interval interval) {...}
  public Interval(String string) {...}
  public boolean includes (double point) {...}
  public boolean includes (Interval interval) {...}
  public boolean isValid() {...}
  ...
}

class Coordinate {
  public boolean isValid ()
  ...
}
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Constructores de la Clase](../u4classConstructors/README.md)
