# Objetos Valor






| 
* En el caso de que los atributos sean **constantes, puede postergarse la inicialización obligatoria al cuerpo de todos los constructores**.


	+ Una vez inicializadas, ya no es posible la asignación de nuevos valores.



 | 


```
class Person  {
  public final short ADULT = 18;
  private short age;
  private final int DNI;

  public Person(int dni) {
    age = 0;
    DNI = dni;
  }
  ...
}
```


 |








| **Aplicaciones** |
| --- |
| 
* Fraction - [*Fraction*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a3_values/Fraction.java) - [*FractionView*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a3_values/FractionView.java) - [*App*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a3_values/App.java)


 |  |  |


---

[Volver al nivel superior](../README.md)

