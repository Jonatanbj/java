# Especialización por redefinición






| 
* Donde la **cabecera del método es exactamente igual a la cabecera del método no privado de la clase padre, excepto su visibilidad, que puede ampliarse**. **En caso contrario, sería sobrecarga y no redifinición**
* Sus implicaciones son:


	+ se **anula la transmisión del método de la clase padre**;
	+ los **objetos de la clase padre responden al mensaje con el comportamiento dado en la clase padre**;
	+ los **objetos de la clase hija responden al mensaje con el comportamiento dado en la clase hija**;



 | 

ListaCentinela

 |








| **Aplicaciones** |
| --- |
| 
* SentinnelList - [*Redefinición*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a4_extends/SentinelList.java): por anulación


 |  |



##### Referencia *super*







| 
* **super**, en la implantación de cualquier **clase derivada, es una referencia constante que guarda la dirección del objeto que recibe el mensaje correspondiente al método que se está redefiniendo, pero con el comportamiento de la clase padre**


	+ Su utilidad será para la **reutilización del método de la clase padre, anulado en la transmición, desde la redefinición del método de la clase hija**



 | 

Conjunto

 |








| **Aplicaciones** |
| --- |
| 
* Set - [*Redefinición*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a4_extends/Set.java): por refinamiento, Liskov?!?!


 |  |



---

[Volver al nivel superior](../README.md)

[Siguiente sección: Referencia super](../u4superReference/README.md)


[Anterior](../u2protectedMembers/README.md) | [Subir nivel](../README.md) | [Siguiente](../u4superReference/README.md)
