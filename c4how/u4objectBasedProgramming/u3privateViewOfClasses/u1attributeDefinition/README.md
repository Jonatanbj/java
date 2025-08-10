# [Definición de atributos](../README.md)

* Se **declaran variables y/o constantes de tipos primitivos, referencias a objetos o vectores** de éstos
* anteponiendo la palabra **private**

   + En <span style="color: darkred;">cualquier punto de la implementación</span> de la clase pero lo lógico es <span style="color: green;">al principio de la declaración de la clase</span>

```java
class <class> {
   private <declaration>
   private <declaration>
   ...
}
```

```java
class Interval {
   private double min;
   private double max;
}
```
---

[Anterior](./README.md) | [Subir nivel](../README.md) | [Siguiente](../u2constructorDefinition/README.md)
