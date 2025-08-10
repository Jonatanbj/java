# [Definición de metodos](./README.md)

* En cualquier punto de la implementación de la clase, **se define el cuerpo de las cabeceras de los métodos acompañándolos de una sentencia secuencial** que contiene las declaraciones locales y sentencias que se consideren oportunas


	+ dentro del cuerpo del método se tiene **acceso a los atributos, los parámetros del método y a las declaraciones locales** desde las expresiones de la anidación jerárquica de sentencias
	+ la **notación punto** para el paso de mensajes sirve también para acceder a los atributos de un objeto de la misma clase

```java
clase <class> {
  public <methodHeader> <sequentialSentence>
  public <methodHeader> <sequentialSentence>
  ...
}
```

```java
class Interval {
  private double min;
  private double max;

  public void shift (double amount) {
    min += amount;
    max += amount;
  }

  public Interval(Interval interval){
    min = interval.min;
    max = interval.max;
  }

  public boolean equals(Intervalo interval) {
    return min == interval.min && max == interval.max;
  }
  ...
```
<br>
  
* si el **tipo devuelto** no es\_ **void**, se determinará el valor devuelto por el método con la siguiente sentencia:

<br>


  `return` `<expression>`;

<br>

```java
public double length() {
  return max - min;
}

public boolean includes(double point) {
  return min <= point && point <= max;
}

public boolean valid() {
  return min <= max;
}
```
---

[Anterior](../u2constructorDefinition/README.md) | [Subir nivel](../README.md) | [Siguiente](../u4thisReference/README.md)
