# [Clases Abstractas](README.md)


**Clases Concretas**  

* Surgen de la descripción de los atributos y métodos que **definen el comportamiento de un cierto conjunto de objetos homogéneos**

**Clases Abstractas** 

* Son clases **NO instanciables** que surgen del factor común del código de otras clases con atributos comunes, métodos comunes y/o **cabeceras de métodos comunes sin definición**, pero **no pueden ser con visibilidad privada**


```java
abstract class <ClaseAbstracta> {
  ...
  public abstract void <métodoAbstracto>( <parametros> );
  protected abstract void <métodoAbstracto>( <parametros> );
  // private abstract void <métodoAbstracto>( <parametros> ); ERROR!!!
  ...
}
```


**Aplicaciones** 


* Dispenser - [*Sin herencia*](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_dispensers/a5_extends_a1_node) - [con herencia](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_dispensers/a5_extends_a2_dispenser)



![dispenser](/images/dispenser.svg)

 |







|  **Posibilidades:** |  |
| :--- | --- |
| - Una **clase abstracta puede ser hija de otra clase abstracta** porque se especializa (añadiendo atributos, métodos o redefiniendo métodos), pero **no necesariamente redefine todos los métodos abstractos heredados y/o puede añadir nuevos métodos abstractos**;  |  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Alumno](/images/Alumno.svg) | 
|  - una **clase abstracta puede ser hija de una clase concreta si en su especialización añade algún método abstracto** | ![persona](/images/persona.svg) |


**Posibilidades:**

* Un **método no abstracto de una clase abstracta puede definirse apoyándose en métodos abstractos** entendiendo que será un código que se transmite hasta clases concretas que redefinen los métodos abstractos;





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

```
abstract class Solido {
  private double densidad;
  public double peso() {
    return densidad * this.volumen();
  }
  public abstract double volumen();
}
```

---



[Anterior](../u2inheritanceByExtension/README.md) | [Subir nivel](../README.md) | [Siguiente](../u4inheritanceByImplementation/README.md)
