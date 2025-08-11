# [Miembros protegidos](README.md)








**<span style="color:#ff4d4d;">Cuando la clase padre no transmite los métodos públicos necesarios para manipular los atributos privados transmitidos desde la clase padre en los métodos añadidos en la clase hija</span>**

* **Visibilidad publica** añadiendo dichos métodos públicos a la clase padre **NO es solución** puesto que **rompe el principio de encapsulación** ya que, para la implantación de una clase hija, los objetos de la clase padre dan a conocer más allá de lo que se les solicitaba previamente a la existencia de la clase derivada.


* **<span style="color:#ff4d4d;"Visibilidad protegida (*protected*)**, donde los miembros (atributos y/o métodos) son **accesibles en la implantación de la clase y en cualquier clase derivada**.

* **Atributos protegidos** Dentro del cuerpo de los métodos de la clase derivada se tiene acceso a los atributos protegidos heredados, a los atributos añadidos, a los parámetros del método y a las declaraciones locales, **ley flexible de Demeter**


	+ Implicación: <span style="color:#ff4d4d;">desbordamiento del mantenimiento dado que si se modifica la implantación de la clase padre SI repercute sobre la implantación de la clase hija y se obtiene un **máximo acoplamiento</span>** entre ambas clases


* **Métodos *get/set* protegidos** son métodos para obtener el valor y asignar un valor a los atributos privados transmitidos desde la clase padre, **posibilitando cualquier manipulación por parte de la clase hija futura**;


	+ Implicación: contención del mantenimiento dado que si se modifica la implantación de la clase padre no repercute sobre la implantación de la clase hija y se obtiene un **mínimo acoplamiento** entre ambas clases



| **Aplicaciones** |--- |
| --- |--- |
| * List - [*Herencia*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a4_extends/Node.java): Node - [Protected](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a4_extends_protected/Node.java): Node - [Protected Attributes](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a4_extends_protected_attributes/Node.java): Node!!! |  |


---

[Anterior](../u1specializationByAddition/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3specializationByRedefinition/README.md)
