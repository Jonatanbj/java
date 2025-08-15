# [Limitaciones de las clases genéricas](README.md)






| Limitación | Ejemplo |
| :--- | :--- |
| **No se pueden encarnar clases genéricas con tipos primitivos** | `BoundedStack<int>` `intBoundedStack;` // ERROR |
| **No se pueden crear clases parametrizadas de excepciones** | `public` `class` `XException`<E> `extends` `Exception` { ... } // ERROR |
| **No pueden aparecer genéricos en las cláusulas *catch*** | `try` { ... } `catch` (E e) { ... } // ERROR|
| **No se pueden crear vectores de objetos de clases genéricas** | Ver ejemplo abajo. |

<!-- Ejemplo de código fuera de la tabla para evitar problemas de formato -->

<br>

```java
public class BoundedStack<E> {

    protected E[] elements;
    // ...

    public BoundedStack(int size) {
        // this.elements = new E[size]; // ERROR
        this.elements = (E[]) new Object[size]; // AVISO
        // ...
    }

}

// No permitido:
PilaAcotada<Integer>[] pilas = new PilaAcotada<Integer>[10]; // ERROR
// Permitido con advertencia:
PilaAcotada<Integer>[] pilas = new PilaAcotada[10];          // AVISO
```

<br>

---

[Volver al nivel superior](../README.md)



[Anterior](../u1genericClassesAndInheritance/README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u8parametricProgramming/u2boundedTypeParameters/README.md)
