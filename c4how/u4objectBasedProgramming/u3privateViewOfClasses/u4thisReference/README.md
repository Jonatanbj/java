# [Referencia this](./README.md)


 
* **this** es una **referencia constante que guarda la dirección del objeto que recibe el mensaje correspondiente al método que se está definiendo**, implícitamente existe en todas las clases:

<br>

  `private final` `<class>` `this;`





* Sirve para **resolución de ambigüedades en la colisión** de parámetros o declaraciones locales con el mismo nombre que los atributos;
  * **Evita la multiplicidad de identificadores innecesarios**

 <br>

```java

public Interval(double min, double max) {
  this.min = min;
  this.max = max;
}
```
<br>

* Sirve para la **reutilización de contructores en la definición de otros constructores**, siendo la primera sentencia del constructor, mediante la sintaxis:

<br>

  `this` ( [ `<expression>` {, `<expression>` } ] );

<br>

```java
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
<br>

* Sirve para la **reutilización de métodos** en la codificación de otros métodos;

<br>

```java
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
---

[Anterior](../u3Definicióndemetodos/README.md) | [Subir nivel](../README.md) | [Siguiente](../u5privateMethods/README.md)
