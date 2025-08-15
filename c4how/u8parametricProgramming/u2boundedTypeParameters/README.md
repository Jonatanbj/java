# [Parámetros Limitados](README.md)


 **Sintaxis:** 

* En la declaración de un **parámetro de tipo de una clase parametrizada se puede especificar una restricción que debe cumplir ese tipo**; estos parámetros de tipo se conocen como **parámetros de tipo limitados (*bounded*)**.


```java
class <clase><<parámetro> extends <tipoBase>,…> {
  ...
}
```

* donde se especifica que el **parámetro de tipo que se declara <parámetro> debe ser el tipo <tipoBase> o cualquier tipo derivado de él**;


	+ el **tipo base puede ser una clase o un interfaz**;
	+ se **pueden especificar más interfaces separándolos por *&***;
	+ el **tipo base puede estar, a su vez, parametrizado**.

 *Ejemplo* 
  
* por ejemplo, la clase Interval puede parametrizarse, pero con la restricción de que sus elementos sean [comparables](https://docs.oracle.com/javase/8/docs/api/java/lang/Comparable.html): [bounded](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/a5_units/a1_interval/a7_parametrized)


```java
interface Comparable<T> {
   int comparteTo(T o);
}
```

---


[Anterior](../u1genericClasses/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3wildcardParameters/README.md)
