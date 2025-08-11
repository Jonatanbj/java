# [Limitaciones de la Herencia](README.md)


**Clases final**

- <span style="color:#b71c1c;">no permiten ningún tipo de herencia posterior,</span> por clases de la biblioteca estándar



```java
final class MiClaseFinal {
    // No se puede heredar de esta clase
}
```

**Enumerados**

- **<span style="color:#b71c1c;">NO** <span style="color:#b71c1c;"> pueden heredar de una clase por extensión,</span> son siempre `final`.
- **SÍ** pueden heredar de un interfaz por implementación.

**Metodos final**

- **<span style="color:#b71c1c;">No** <span style="color:#b71c1c;">permiten ningún tipo de redefinición posterior (por clases de la biblioteca estándar).

```java
class <clase> {
    ...
    final <metodo>
    ...
}
```
---


[Anterior](../u4inheritanceByImplementation/README.md) | [Subir nivel](../README.md) | [Siguiente](../u6inheritanceBenefits/README.md)
