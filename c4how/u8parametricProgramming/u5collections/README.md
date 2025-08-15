# [Colecciones](README.md)

- #### [Listas](u1lists/README.md)
- #### [Colas](u2queues/README.md)
- #### [Conjuntos](u3sets/README.md)
- #### [Mapas](u4maps/README.md)


---

Java proporciona en el paquete `java.util` un conjunto de clases para representar y manejar estructuras de datos.

* Antes de la aparición de la plataforma Java 2, sólo se disponía de un conjunto muy limitado de clases para las estructuras de datos más comunes: Vector, Stack, Hashtable, y el interfaz Enumeration para recorrer los elementos de estas clases.

* Java 2 incorpora un framework más completo inspirado en la librería STL de C++, pero manteniendo compatibles las clases heredadas de las versiones anteriores.
	

* Esta biblioteca de clases separa los interfaces de sus implementaciones, lo que proporciona mayor abstracción al usar la biblioteca, y facilita la extensibilidad de la misma.

* A partir de la JDK 1.5 las clases de la biblioteca son clases parametrizadas.

<br>

|  iterator |  collection |  map |
|---|---|---|
|![iterator](/images/Iterator.svg)|![collection](/images/Collection.svg)| ![map](/images/Map.svg)| 
||![collection2](/images/Collection2.svg)|![map2](/images/Map2.svg)|


<br>

`InterfazCollection<E>`: Es la raíz de la jerarquía de las clases de colecciones y proporciona los métodos comunes a todas ellas:

<br>

```java
int size()
boolean isEmpty()
boolean contains(Object o)
boolean containsAll(Collection<?> c)
Iterator<E> iterator()
Object[] toArray()
<T> T[] toArray(T[] a)
boolean add(E e)
boolean remove(Object o)
boolean addAll(Collection<? extends E> c)
boolean removeAll(Collection<?> c)
boolean retainAll(Collection<?> c)
void clear()
boolean equals(Object o)
int hashCode()
```

<br>

 `InterfazIterator<E>:` Permite recorrer los elementos de las clases de colecciones:

- donde el método `remove()` debe llamarse solo después de `next()`, y elimina de la colección el último elemento devuelto por este.
- no debe modificarse una colección mientras un iterador la recorre de ninguna otra manera que invocando `remove()` sobre ese iterador, ya que el comportamiento del iterador no está definido (la implementación actual produce una excepción `ConcurrentModificationException`).

<br>

```java
boolean hasNext()
E next()
void remove()
```




---


[Anterior](../u4genericMethods/README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u8parametricProgramming/u5collections/u1lists/README.md)
