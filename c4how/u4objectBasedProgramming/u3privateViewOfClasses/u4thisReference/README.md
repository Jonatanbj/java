# Referencia this






| 
* **this** es una **referencia constante que guarda la dirección del objeto que recibe el mensaje correspondiente al método que se está definiendo**, implícitamente existe en todas las clases:






```
  private final <class> this;
```




* Sirve para **resolución de ambigüedades en la colisión** de parámetros o declaraciones locales con el mismo nombre que los atributos;


	+ **Evita la multiplicidad de identificadores innecesarios**



 | 


```
public Interval(double min, double max) {
  this.min = min;
  this.max = max;
}
```


 |







| 
* Sirve para la **reutilización de contructores en la definición de otros constructores**, siendo la primera sentencia del constructor, mediante la sintaxis:






```
  this([ <expression> {, <expression> }]);
```


 | 


```
  public Interval() {
    this(0, 0);
}

  public Interval(double max) {
    this(0, max);
  }

  public Interval(Interval interval) {
    this(interval.min, interval.max);
  }
```


 |
| 
* Sirve para la **reutilización de métodos** en la codificación de otros métodos;


 | 


```
public boolean includes(Interval interval) {
  return this.includes(interval.min) &&
    this.includes(interval.max);
}

public void escale(double escale) {
  final double newHalfLength = this.length()/2 * escale;
  final double middlePoint = this.middlePoint();
  this.min = middlePoint - newHalfLength;
  tnis.max = middlePoint + newHalfLength;
}
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Métodos privados](../u5privateMethods/README.md)
