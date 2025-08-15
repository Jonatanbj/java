# [Parámetros Comodines](README.md)

* [Código](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_listas/a5_parametrized) con error de compilación porque la clase *List<Double>* no es una subclase de *List<Number>* aunque *Double* sea una subclase de *Number*.

```java
List<Double> doubleList = new List<Double>();
List<Number> numberList = doubleList; // !!!ERROR
numberList.add(Integer.valueOf(3));
Double value = doubleList.get(0);
```
<br>

La razón es que si fuera así, entonces las siguientes sentencias harían que **pudiéramos copiar una referencia a un entero en una referencia a un doble, lo cual es incorrecto**.



* Los **parámetros de tipos comodines (*wildcards*) son parámetros sin nombre que pueden usarse para declarar tipos parametrizados de los atributos, argumentos, objetos locales y valores devueltos de métodos de cualquier clase, parametrizada o no**; y que representan únicamente que se trata de un **tipo cualquiera desconocido**.
  * Se representan mediante el **símbolo *?***.
  * Al ser **anónimos no pueden usarse para referirse a él** en el interior de la clase o método donde se declaran.
  * **Pueden limitarse como cualquier otro** parámetro de tipo.
  * Su principal utilidad consiste en que **relajan el sistema de tipos de Java de forma que resulta más fácil asignar instancias de tipos genéricos**.
<br>


* El [error de compilación no se produce](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_listas/a5_parametrized2) porque el uso del **parámetro comodín relaja el sistema de tipos**, de manera que las siguientes sentencias son correctas:
  * Sin embargo, usar el parámetro comodín impone que con la referencia no se puedan usar métodos de la clase parametrizada que pudieran producir una incompatibilidad de tipos 
  * pero sí se pueden usar métodos que no puedan producir incompatibilidad de tipos.

<br>

```java
List<Double> doubleList = new List<Double>();
// List<Number> numberList = doubleList; // !!!ERROR
//numberList.add(Integer.valueOf(3));
Double value = doubleList.get(0);

// Se podría omitir extends Number
List<? extends Number> numberList = doubleList;
//numberList.add(new Double(3)); // !!!ERROR
//Number numero = new Double(3);
//numberList.add(numero); // !!!ERROR
//Double x1 = numberList.get(0); // !!!ERROR

Number number = numberList.get(0);
String string = numberList.toString();
numberList.clear();
string = numberList.toString();
```


---


[Anterior](../u2boundedTypeParameters/README.md) | [Subir nivel](../README.md) | [Siguiente](../u4genericMethods/README.md)
