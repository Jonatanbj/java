# [Herencia por extensión](README.md)

- #### [Especialización por adición](u1specializationByAddition/README.md)
- #### [Miembros protegidos](u2protectedMembers/README.md)
- #### [Especialización por redefinición](u3specializationByRedefinition/README.md)
- #### [Referencia super](u4superReference/README.md)

---

**_Sintaxis_**
+ Mediante la palabra reservada extends

    + **<span style="color:darkred">No permite herencia múltiple.</span>**



```java
class ClaseDerivada extends ClaseBase {
    // miembros y métodos adicionales
}
```

**_Ejemplo_**


	
```java
class Abuela {
  ...
}

class Padre extends Abuela {
  ...
}

class Hija extends Padre {
  ...
}
```

---


[Anterior](../u1inheritanceRelationship/u1classificationHierarchies/README.md) | [Subir nivel](../README.md) | [Siguiente](u1specializationByAddition/README.md)