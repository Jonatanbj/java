# [Relación de Herencia](README.md)

- #### [Jerarquías de Clasificación](u1classificationHierarchies/README.md)

---

| **Transmisión**      | **Imagen**        |
|:---------------------|-------------------|
| - La herencia en todos los ámbitos (derecho, biología, ...) tiene connotaciones de transmisión <br> - En Programación Orientada a Objetos es la transmisión de todos los miembros (atributos y métodos públicos y privados) de una clase a otra. <br> - Terminología: <br> <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- clase base para la que transmite y clase derivada a la que recibe la transmisión <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- paralela a los árboles genealógicos: padre, hija, nieta ... <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- superclase y subclases en desuso | ![Transmisión en POO](/images/Transmision.svg)   |

<br> 

**Colaboración entre objetos**

- Las relaciones de **composición**, **asociación** y **dependencia** son relaciones binarias que devienen de la colaboración entre objetos: envío de mensajes entre objetos

- La relación de **herencia**:
  - es una relación binaria entre clases
  - si existe una relación de herencia, no es necesario que exista una colaboración entre los objetos de sus clases aunque tampoco lo impide
  - por tanto, los objetos de las clases de una relación de herencia son, a priori, independientes

- La clase **Persona** hereda de la clase **Animal**:
  - en una aplicación sobre la evolución de las especies, sus objetos no colaboran
  - en una aplicación para la gestión de una granja, sus objetos sí colaboran
<br> 

**Tipos de Relación de Herencia**

| Tipos de Relación de Herencia | Ejemplos |
|-------------------------------|----------|
|  **_Herencia simple:_** <br> cuando una clase derivada hereda de una única clase base. | ![Transmisión en POO](/images/HerenciaSimple.svg)   |
|  **_Herencia múltiple:_** <br> cuando una clase derivada hereda de varias clases base. | ![Transmisión en POO](/images/HerenciaMultiples.svg)|



---


[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](u1classificationHierarchies/README.md)
