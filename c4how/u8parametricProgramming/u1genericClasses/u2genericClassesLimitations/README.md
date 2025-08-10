# Limitaciones de las clases genéricas






|  | Ejemplo |
| --- | --- |
| 
* **No se pueden encarnar clases genéricas con tipos primitivos**


 | 


```
BoundedStack<int> intBoundedStack; // ERROR
```


 |
| 
* **No se pueden crear clases parametrizadas de excepciones**


 | 


```
public class XException<E> extends Exception { ... } // ERROR
```


 |
| 
* **No pueden aparecer genéricos en las cláusulas *catch***


 | 


```
try { ... } catch (E e) { ... } // ERROR
```


 |
| 
* **No se pueden crear vectores de objetos de clases genéricas**


 | 


```
public class BoundedStack<E> {

   protected E[] elements;
   ...
   public BoundedStack(int size) {
       this.elements = new E[size]; // ERROR
       this.elements = (E[]) new Object[size]; // AVISO
   ...
   }
}

PilaAcotada<Integer>[] pilas = new PilaAcotada<Integer>[10];        // ERROR
PilaAcotada<Integer>[] pilas = new PilaAcotada[10];                // AVISO
```


 |


---

[Volver al nivel superior](../README.md)



[Anterior](../u1genericClassesAndInheritance/README.md) | [Subir nivel](../README.md) | [Siguiente](../README.md)
