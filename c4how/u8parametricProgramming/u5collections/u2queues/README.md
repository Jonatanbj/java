# Colas






| 
* **Interfaz Queue<E>:** Las colas ordenan sus elementos según un orden determinado (normalmente FIFO, aunque no necesariamente):


 | 


```
boolean offer(E e)
E remove()
E poll()
E element()
E peek()
```


 |








|  | **Excepción** | **No excepción** |
| --- | --- | --- |
| 
**Inserción**
 | 
*add()*
 | 
*offer()*
 |
| 
**Extracción**
 | 
*remove()*
 | 
*poll()*
 |
| 
**Consulta**
 | 
*element()*
 | 
*peek()*
 |



* La única clase que implementa el ***interfaz Queue<E>*** es:










| 
* **Clase PriorityQueue<E>:** proporciona una implementación basada en prioridades que se establecen por el orden natural de sus elementos (según el interfaz *Comparable*) o por un comparador de elementos que se suministra a la cola en su construcción. Todas las claves deben implementar el interfaz *Comparable* (o ser aceptadas por su *Comparator*).


 | 


```
public PriorityQueue()
public PriorityQueue(int initialCapacity)
public PriorityQueue(int initialCapacity,
Comparator<? super E> comparator)
public PriorityQueue(Collection<? extends E> c)
public PriorityQueue(PriorityQueue<? extends E> c)
public PriorityQueue(SortedSet<? extends E> c)
```


 |
| 
* **Interfaz Deque<E>:** Son colas que permiten la inserción y extracción de elementos en ambos extremos (*double ended queue*).


 | 


```
void addFirst(E e)
void addLast(E e)
boolean offerFirst(E e)
boolean offerLast(E e)
E removeFirst()
E removeLast()
E pollFirst()
E pollLast()
E getFirst()
E getLast()
E peekFirst()
E peekLast()
boolean removeFirstOccurrence(Object o)
boolean removeLastOccurrence(Object o)
void push(E e)
E pop()
Iterator<E> descendingIterator()
```


 |



* Las clases que implementan el **interfaz Deque<E>** son:










| 
* **Clase LinkedList<E>:** Implementación mediante listas doblemente enlazadas.


 | 


```
public LinkedList()
public LinkedList(Collection<? extends E> c)
```


 |
| 
* **Clase ArrayDeque<E>:** Implementación mediante vectores autoajustables.


 | 


```
public ArrayDeque()
public ArrayDeque(Collection<? extends E> c)
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Conjuntos](../u3sets/README.md)
