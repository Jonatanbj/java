# [Especialización por redefinición](./README.md)


| **Especialización por redefinición** | **Diagrama** |
|:--------------------------------------|:--------------:|
| - Donde la **<span style="color:blue">cabecera del método es exactamente igual</span>** a la cabecera del método no privado de la clase padre, excepto su visibilidad, que puede ampliarse. **<span style="color:red">En caso contrario, sería sobrecarga y no redefinición</span>**<br><br>- Sus implicaciones son:<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - <span style="color:red">se anula la transmisión del método de la clase padre</span>;<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - los <span style="color:blue">objetos de la clase padre</span> responden al mensaje con el comportamiento dado en la clase padre;<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - los <span style="color:blue">objetos de la clase hija</span> responden al mensaje con el comportamiento dado en la clase hija; | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Diagrama de clases](/images/ListaCentinela.svg) |


**Aplicaciones** 
* SentinnelList - [*Redefinición*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a4_extends/SentinelList.java): por anulación
---

[Anterior](../u2protectedMembers/README.md) | [Subir nivel](../README.md) | [Siguiente](../u4superReference/README.md)
