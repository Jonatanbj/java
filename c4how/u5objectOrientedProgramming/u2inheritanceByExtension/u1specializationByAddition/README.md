# [Especialización por adición](./README.md)







**Atributos**   

* Los **atributos añadidos en la clase hija** tienen **las mismas reglas sintácticas y semánticas que en una clase que no sea derivada**

**Métodos**

* Los **métodos añadidos en la clase hija** tienen **las mismas reglas sintácticas y semánticas que en una clase que no sea derivada**


	+ <span style="color:#b71c1c"> excepto que NO tienen acceso a los atributos y métodos privados transmitidos desde la clase padre,</span> si no es a través de los métodos públicos transmitidos desde la clase padre
	
	
		- Esto **permite la contención del mantenimiento**, dado que, si se **modifica la implantación de la clase padre, no repercute sobre la implantación de la clase hija y se obtiene un mínimo acoplamiento** entre ambas clases

 **Constructores** 



```java
  class <Clase> extends <Base> {

    public <Clase>({ <parametro> }* ){
      super( { <expresion> }*);
      ...
    }
  }
```

* Mediante ***super***, donde debe ser la primera sentencia de los constructores de la clase derivada y sus argumentos deben coincidir en número y tipo con la lista de parámetros de algún constructor público o protegido de la clase padre


	+ Se puede omitir para el caso del constructor de la clase padre con una lista vacía de parámetros



| **Implicaciones sobre los objetos** | *Ejemplo* |
| :--- | :---: |
| - Los **objetos de la clase padre NO sufren ninguna alteración** por la presencia de clases derivadas <br>- Los **objetos de la clase hija**: <br><br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - tienen todos los **atributos transmitidos desde la clase padre junto con los atributos añadidos en la clase hija**;<br><br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - o responden a mensajes que corresponden con los **métodos públicos transmitidos desde la clase padre junto con los métodos públicos añadidos en la clase derivada**; | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Herencia por extensión](/images/HerenciaExtencion2.svg)|




| **Aplicaciones** |--- |
| --- |--- |
| List - [*Composición*](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a0_classes) | - [Herencia](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a4_extends/Node.java): Node |

![Ver todas las imágenes relacionadas](/images/lists.svg)

[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](../u2protectedMembers/README.md)
