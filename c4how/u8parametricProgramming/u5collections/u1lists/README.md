# [Listas](README.md)



* **Interfaz List<E>:** Representa una secuencia de elementos que ocupan una cierta posición en la colección, en la que puede haber elementos repetidos.

```java
E get(int index)
E set(int index, E element)
void add(int index, E element)
E remove(int index)
int indexOf(Object o)
int lastIndexOf(Object o)
ListIterator<E> listIterator()
ListIterator<E> listIterator(int index)
List<E> subList(int fromIndex, int toIndex)
boolean addAll(int index, Collection<? extends E> c)
```

* **Interfaz ListIterator<E>:** Recorre los elementos de una lista:

```java
boolean hasPrevious()
E previous()
int nextIndex()
int previousIndex()
void add(E e)
void set(E e)
```

- El método *remove()* debe llamarse sólo después de *next()* o *previous()*, y elimina de la colección el último elemento devuelto por éstos.
- *add()* inserta justo antes del elemento que se obtendría con *next()* y justo después del elemento que se obtendría con *previous()*.
- *set()* reemplaza el último elemento devuelto por *next*() o *previous()*, y sólo puede invocarse si después de estas operaciones no se ha invocado *add()* o *set()*.

  * Las clases que implementan el interfaz List<E> son:

* **Clase ArrayList<E>:** Proporciona una implementación basada en vectores de elementos que autoajustan su tamaño según se añaden elementos.

```java
public ArrayList()
public ArrayList(int initialCapacity)
public ArrayList(Collection<? extends E> c)
public void trimToSize()
public void ensureCapacity(int minCapacity)
```

* **Clase LinkedList<E>:** Utiliza listas doblemente enlazadas; además implementa el **interfaz Deque<E>**, por lo que puede usarse para tratar con colas (se verá más adelante).

```java
public LinkedList()
public LinkedList(Collection<? extends E> c)
```

* **Clase Vector<E>:** También usa vectores autoajustables, y se mantiene por razones de compatibilidad con código heredado; además está sincronizada para evitar accesos concurrentes, lo que conlleva un cierto sobrecoste adicional.

```java
public Vector()
public Vector(int initialCapacity)
public Vector(int initialCapacity, int capacityIncrement)
public Vector(Collection<? extends E> c)
public void copyInto(Object[] anArray)
public void trimToSize()
public void ensureCapacity(int minCapacity)
public void setSize(int newSize)
public int capacity()
public Enumeration<E> elements()
public int indexOf(Object o, int index)
public int lastIndexOf(Object o, int index)
public E elementAt(int index)
public E firstElement()
public E lastElement()
public void setElementAt(E obj, int index)
public void removeElementAt(int index)
public void insertElementAt(E obj, int index)
public void addElement(E obj)
public boolean removeElement(Object obj)
public void removeAllElements()
```

* **Stack<E>:** Representa una pila LIFO.

```java
public Stack()
public E push(E item)
public E pop()
public E peek()
public boolean empty()
public int search(Object o)
```


---


[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](../u2queues/README.md)
