# Especialización por adición







| **Atributos** | **Métodos** | **Constructores** |
| --- | --- | --- |
| 
* Los **atributos añadidos en la clase hija** tienen **las mismas reglas sintácticas y semánticas que en una clase que no sea derivada**


 | 
* Los **métodos añadidos en la clase hija** tienen **las mismas reglas sintácticas y semánticas que en una clase que no sea derivada**


	+ **excepto que NO tienen acceso a los atributos y métodos privados transmitidos desde la clase padre**, si no es **a través de los métodos públicos transmitidos desde la clase padre**
	
	
		- Esto **permite la contención del mantenimiento**, dado que, si se **modifica la implantación de la clase padre, no repercute sobre la implantación de la clase hija y se obtiene un mínimo acoplamiento** entre ambas clases



 | 


```
  class <Clase> extends <Base> {

    public <Clase>({ <parametro> }* ){
      super( { <expresion> }*);
      ...
    }
  }
```




* Mediante ***super***, donde debe ser la primera sentencia de los constructores de la clase derivada y sus argumentos deben coincidir en número y tipo con la lista de parámetros de algún constructor público o protegido de la clase padre


	+ Se puede omitir para el caso del constructor de la clase padre con una lista vacía de parámetros



 |







| **Implicaciones sobre los objetos** | *Ejemplo* |
| --- | --- |
| 
* Los **objetos de la clase padre NO sufren ninguna alteración** por la presencia de clases derivadas
* Los **objetos de la clase hija**:


	+ tienen todos los **atributos transmitidos desde la clase padre junto con los atributos añadidos en la clase hija**;
	+ responden a mensajes que corresponden con los **métodos públicos transmitidos desde la clase padre junto con los métodos públicos añadidos en la clase derivada**;



 | 

HerenciaExtencion2

 |








| **Aplicaciones** |
| --- |
| 
* List - [*Composición*](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a0_classes) - [Herencia](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a4_extends/Node.java): Node


 |  |  |






| 

lists

 |



##### Miembros protegidos








| 
**Cuando la clase padre no transmite los métodos públicos necesarios para manipular los atributos privados transmitidos desde la clase padre en los métodos añadidos en la clase hija**
 |
| 
* **Visibilidad publica** añadiendo dichos métodos públicos a la clase padre **NO es solución** puesto que **rompe el principio de encapsulación** ya que, para la implantación de una clase hija, los objetos de la clase padre dan a conocer más allá de lo que se les solicitaba previamente a la existencia de la clase derivada.


 | 
* **Visibilidad protegida (*protected*)**, donde los miembros (atributos y/o métodos) son **accesibles en la implantación de la clase y en cualquier clase derivada**.


 |
| 
* **Atributos protegidos** Dentro del cuerpo de los métodos de la clase derivada se tiene acceso a los atributos protegidos heredados, a los atributos añadidos, a los parámetros del método y a las declaraciones locales, **ley flexible de Demeter**


	+ Implicación: desbordamiento del mantenimiento dado que si se modifica la implantación de la clase padre SI repercute sobre la implantación de la clase hija y se obtiene un **máximo acoplamiento** entre ambas clases



 | 
* **Métodos *get/set* protegidos** son métodos para obtener el valor y asignar un valor a los atributos privados transmitidos desde la clase padre, **posibilitando cualquier manipulación por parte de la clase hija futura**;


	+ Implicación: contención del mantenimiento dado que si se modifica la implantación de la clase padre no repercute sobre la implantación de la clase hija y se obtiene un **mínimo acoplamiento** entre ambas clases



 |








| **Aplicaciones** |
| --- |
| 
* List - [*Herencia*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a4_extends/Node.java): Node - [Protected](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a4_extends_protected/Node.java): Node - [Protected Attributes](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a4_extends_protected_attributes/Node.java): Node!!!


 |  |



---

[Volver al nivel superior](../README.md)

[Siguiente sección: Miembros protegidos](../u2protectedMembers/README.md)
