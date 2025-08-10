# Conjuntos


* Representa una colección de elementos no repetidos. No añade ningún método nuevo a *Collection<E>*, sólo estipula ciertas restricciones en sus métodos;


* Las clases que implementan este interfaz son:










| 
* **Clase EnumSet<E extends Enum<E>>:** Los elementos del conjunto deben ser valores de enumerados. Proporcionan una representación muy compacta y eficiente. Los elementos se recorren según su orden natural. La clase es abstracta y sólo tiene métodos genéricos estáticos para crear los conjuntos.


 | 


```
public static <E extends Enum<E>> EnumSet<E>
noneOf(Class<E> elementType)
public static <E extends Enum<E>> EnumSet<E>
allOf(Class<E> elementType)
public static <E extends Enum<E>> EnumSet<E> copyOf(EnumSet<E> s)
public static <E extends Enum<E>> EnumSet<E> copyOf(Collection<E> c)
public static <E extends Enum<E>> EnumSet<E>
    complementOf(EnumSet<E> s)
public static <E extends Enum<E>> EnumSet<E> of(E e)
public static <E extends Enum<E>> EnumSet<E> of(E e1, E e2)
public static <E extends Enum<E>> EnumSet<E> of(E e1, E e2, E e3)
public static <E extends Enum<E>> EnumSet<E> of(E e1, E e2, E e3, E e4)
public static <E extends Enum<E>> EnumSet<E> of(E e1, E e2, E e3, E e4, E e5)
public static <E extends Enum<E>> EnumSet<E> of(E first, E... rest)
public static <E extends Enum<E>> EnumSet<E> range(E from, E to)
public EnumSet<E> clone()
```


 |
| 
* **Clase HashSet<E>:** Implementación mediante una tabla hash (realmente un *HashMap*). No garantiza ningún orden al iterar sobre el conjunto.


 | 


```
public HashSet()
public HashSet(int initialCapacity)
public HashSet(int initialCapacity, float loadFactor)
public HashSet(Collection<? extends E> c)
```


 |
| 
* **Clase LinkedHashSet<E>:#** Implementación mediante tabla hash y listas enlazadas (mediante *LinkedHashMap*), en la que los elementos se recorren en el mismo orden en el que se insertaron.


 | 


```
public LinkedHashSet()
public LinkedHashSet(int initialCapacity)
public LinkedHashSet(int initialCapacity, float loadFactor)
public LinkedHashSet(Collection<? extends E> c)
```


 |
| 
* **Interfaz SortedSet<E>:** Representa un conjunto que establece un orden total sobre sus elementos. Los elementos se ordenan por su orden natural (según el interfaz *Comparable*) o por un comparador de elementos que se suministra al conjunto en su construcción. Todas las claves deben implementar el interfaz *Comparable* (o ser aceptadas por su *Comparator*).


 | 


```
Comparator<? super E> comparator()
SortedSet<E> subSet(E fromElement, E toElement)
SortedSet<E> headSet(E toElement)
SortedSet<E> tailSet(E fromElement)
E first()
E last()
```


 |
| 
* **Interfaz NavigableSet<E>:** Extiende *SortedSet<E>* para buscar un elemento menor, menor o igual, mayor o igual, y mayor que un cierto elemento dado, más otros métodos de búsqueda.


 | 


```
E lower(E e)
E floor(E e)
E ceiling(E e)
E higher(E e)
E pollFirst()
E pollLast()
NavigableSet<E> descendingSet()
Iterator<E> descendingIterator()
NavigableSet<E> subSet(E fromElement, boolean fromInclusive,
E toElement, boolean toInclusive)
NavigableSet<E> headSet(E toElement, boolean inclusive)
NavigableSet<E> tailSet(E fromElement, boolean inclusive)
SortedSet<E> subSet(E fromElement, E toElement)
SortedSet<E> headSet(E toElement)
SortedSet<E> tailSet(E fromElement)
```


 |



* La única clase que implementa el interfaz *NavigableSet<E>* es:










| 
* **Clase TreeSet<E>:** Implementación mediante *TreeMap*, en la que los elementos se recorren según su orden natural.


 | 


```
public TreeSet()
public TreeSet(Comparator<? super E> comparator)
public TreeSet(Collection<? extends E> c)
public TreeSet(SortedSet<E> s)
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Mapas](../u4maps/README.md)


[Anterior](../u2queues/README.md) | [Subir nivel](../README.md) | [Siguiente](../u4maps/README.md)
