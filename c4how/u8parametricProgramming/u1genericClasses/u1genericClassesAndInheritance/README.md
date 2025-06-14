# Clases genéricas y herencia






|  | Ejemplo |
| --- | --- |
| 
* **Una clase genérica puede heredar de otra clase genérica**


 | 


```
public class BoundedStack<E> extends BoundedDispenser<E>
```


 |
| 
* **Una clase genérica puede heredar de una clase no genérica**


 | 


```
public class BoundedStack<E> implements Serializable
```


 |
| 
* **Una clase no genérica puede heredar de una clase genérica**


 | 


```
public class IntBoundedStack extends BoundedStack<Integer>
public final class Integer extends Number implements Comparable<Integer>
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Limitaciones de las clases genéricas](../u2genericClassesLimitations/README.md)
