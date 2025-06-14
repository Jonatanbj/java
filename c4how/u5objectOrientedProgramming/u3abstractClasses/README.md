# Clases Abstractas







| **Clases Concretas** | **Clases Abstractas** |  |
| --- | --- | --- |
| 
* Surgen de la descripción de los atributos y métodos que **definen el comportamiento de un cierto conjunto de objetos homogéneos**


 | 
* Son clases **NO instanciables** que surgen del factor común del código de otras clases con atributos comunes, métodos comunes y/o **cabeceras de métodos comunes sin definición**, pero **no pueden ser con visibilidad privada**


 | 


```
abstract class <ClaseAbstracta> {
  ...
  public abstract void <métodoAbstracto>( <parametros> );
  protected abstract void <métodoAbstracto>( <parametros> );
  // private abstract void <métodoAbstracto>( <parametros> ); ERROR!!!
  ...
}
```


 |








| **Aplicaciones** |
| --- |
| 
* Dispenser - [*Sin herencia*](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_dispensers/a5_extends_a1_node) - [con herencia](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_dispensers/a5_extends_a2_dispenser)


 |  |






| 

dispenser

 |







| - **Posibilidades:** |  |
| --- | --- |
| 
* una **clase abstracta puede ser hija de otra clase abstracta** porque se especializa (añadiendo atributos y/o métodos y/o redefiniendo métodos) pero **NO redefine todos los métodos abstractos transmitidos y/o añade algún método abstracto**;





Alumno

 | 
* una **clase abstracta puede ser hija de una clase concreta si en su especialización añade algún método abstracto**





persona

 |







| - **Posibilidades:** |  |
| --- | --- |
| 
* Un **método no abstracto de una clase abstracta puede definirse apoyándose en métodos abstractos** entendiendo que será un código que se transmite hasta clases concretas que redefinen los métodos abstractos;


 | 


```
class Cubo extends Solido {
  private double lado;
  public double volumen() {
    return Math.pow(lado, 3);
  }
}

class Esfera extends Solido {
  private double radio;
  public double volumen() {
    return 4.0 / 3.0 * Math.PI * Math.pow(radio, 3);
  }
}
```


 |
| 


```
abstract class Solido {
  private double densidad;
  public double peso() {
    return densidad * this.volumen();
  }
  public abstract double volumen();
}
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Herencia por Implementación](../u4inheritanceByImplementation/README.md)
