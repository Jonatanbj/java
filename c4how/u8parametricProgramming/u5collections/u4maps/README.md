# [Mapas](README.md)





* **Interfaz Map<K,V>:** Un mapa representa una colección de elementos formados por una clave y un valor. En un mapa no puede haber elementos con claves repetidas, cada clave puede tener un valor como máximo.

```java
boolean containsKey(Object key)
boolean containsValue(Object value)
V get(Object key)
V put(K key, V value)
V remove(Object key)
void putAll(Map<? extends K,? extends V> m)
Set<K> keySet()
Collection<V> values()
Set<Map.Entry<K,V>> entrySet()
```

Las clases que implementan este interfaz son:


* **Clase EnumMap<K extends Enum<K>,V>:** Implementación para usarse con claves de tipo enumerados. Las claves deben ser valores de enumerados. Proporcionan una representación muy compacta y eficiente basada en vectores. Los elementos se recorren según su orden natural.

```java
public EnumMap(Class<K> keyType)
public EnumMap(EnumMap<K,? extends V> m)
public EnumMap(Map<K,? extends V> m)
```


* **Clase HashMap<K,V>:** Implementación mediante una tabla hash. No garantiza ningún orden al iterar sobre el mapa.

```java
public HashMap()
public HashMap(int initialCapacity)
public HashMap(int initialCapacity, float loadFactor)
public HashMap(Map<? extends K,? extends V> m)
```


* **Clase LinkedHashMap<K,V>:** Implementación mediante una tabla hash y listas doblemente enlazadas. Los elementos se recorren en el orden de inserción de sus claves.

```java
public LinkedHashMap()
public LinkedHashMap(int initialCapacity)
public LinkedHashMap(int initialCapacity, float loadFactor)
public LinkedHashMap(Map<? extends K,? extends V> m)
public LinkedHashMap(int initialCapacity, float loadFactor,
     boolean accessOrder)
```



* **Clase WeakHashMap<K,V>:** Implementación mediante una tabla hash y claves débiles. Los elementos cuyas claves dejan de ser referenciadas se destruyen automáticamente.

```java
public WeakHashMap()
public WeakHashMap(int initialCapacity)
public WeakHashMap(int initialCapacity, float loadFactor)
public WeakHashMap(Map<? extends K,? extends V> m)
```



* **Clase IdentityHashMap<K,V>:** Implementación mediante una tabla hash y con comparación de claves y valores mediante == en lugar de equals.

```java
public IdentityHashMap()
public IdentityHashMap(int expectedMaxSize)
public IdentityHashMap(Map<? extends K,? extends V> m)
```



* **Interfaz SortedMap<K,V>:** Un mapa que proporciona un orden total sobre sus claves. El mapa se ordena según el orden natural de sus claves, o mediante un *Comparator* que se suministra al crear el mapa. Este orden se sigue al iterar sobre las colecciones que devuelve el mapa. Todas las claves deben implementar el interfaz *Comparable* (o ser aceptadas por su *Comparator*).

```java
Comparator<? super K> comparator()
SortedMap<K,V> subMap(K fromKey, K toKey)
SortedMap<K,V> headMap(K toKey)
SortedMap<K,V> tailMap(K fromKey)
K firstKey()
K lastKey()
Set<K> keySet()
```


* **Interfaz NavigableMap<K,V> (I):** Extiende *SortedMap<E>* para buscar un elemento menor, menor o igual, mayor o igual, y mayor que un cierto elemento dado, más otros métodos de búsqueda.

```java
Map.Entry<K,V> lowerEntry(K key)
K lowerKey(K key)
Map.Entry<K,V> floorEntry(K key)
K floorKey(K key)
Map.Entry<K,V> ceilingEntry(K key)
K ceilingKey(K key)
Map.Entry<K,V> higherEntry(K key)
K higherKey(K key)
Map.Entry<K,V> firstEntry()
Map.Entry<K,V> lastEntry()
Map.Entry<K,V> pollFirstEntry()
Map.Entry<K,V> pollLastEntry()
NavigableMap<K,V> descendingMap()
```


* **Interfaz NavigableMap<K,V> (II):**

```java
NavigableSet<K> navigableKeySet()
NavigableSet<K> descendingKeySet()
NavigableMap<K,V> subMap(K fromKey, boolean fromInclusive,
                         K toKey, boolean toInclusive)
NavigableMap<K,V> headMap(K toKey, boolean inclusive)
NavigableMap<K,V> tailMap(K fromKey, boolean inclusive)
* **Interfaz SortedMap<K,V>:** Un mapa que proporciona un orden total sobre sus claves. El mapa se ordena según el orden natural de sus claves, o mediante un *Comparator* que se suministra al crear el mapa. Este orden se sigue al iterar sobre las colecciones que devuelve el mapa. Todas las claves deben implementar el interfaz *Comparable* (o ser aceptadas por su *Comparator*).
```

La única clase que implementa el interfaz *NavigableMap<K,V>* es:  


* **Clase TreeMap<K,V>:** Implementación mediante un árbol, en la que los elementos se recorren según su orden natural (o en el orden que proporciona su *Comparator*).parator<? super K> comparator()
 toKey)

```java
public TreeMap()y)
public TreeMap(Comparator<? super K> comparator)
public TreeMap(Map<? extends K,? extends V> m)
public TreeMap(SortedMap<K,? extends V> m)et()
```


---

[Anterior](../u3sets/README.md) | [Subir nivel](../README.md) | [Siguiente](README.md)
