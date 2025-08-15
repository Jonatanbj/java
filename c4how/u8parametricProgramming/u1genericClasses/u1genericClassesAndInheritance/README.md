# [Clases genéricas y herencia](README.md)

| Caso | Ejemplo |
| :--- | :--- |
| **Una clase genérica puede heredar de otra clase genérica** | `java` `public` `class` `extends` `BoundedDispenser` |
| **Una clase genérica puede heredar de una clase no genérica** | `public` `class` `BoundedStack`<E> `implements` `Serializable`|
| **Una clase no genérica puede heredar de una clase genérica** | `public` `class` `IntBoundedStack` `extends` `BoundedStack``<Integer>` <br> `public` `final` `class` `Integer` `extends` `Number` `implements` `Comparable``<Integer>`


---


[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](../u2genericClassesLimitations/README.md)
