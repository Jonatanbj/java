# [Serialización de Objetos](README.md)

- #### [Serilización por defecto](u1defaultSerialization/README.md)
- #### [Serialización personalizadas](u2customSerialization/README.md)
---

- resuelve el problema de almacenar en un fichero (o transmitir por una línea de comunicación, etc.) un **conjunto de objetos de distintas clases, posiblemente relacionados entre sí, y posteriormente restaurarlos de nuevo en la memoria de un programa,** de forma que se mantengan el mismo número de objetos, los mismos valores de sus atributos y las mismas relaciones entre ese conjunto de objetos que en la situación original

  - resolver este problema mediante ficheros de texto o binarios es complejo:
    - porque **los objetos tienen un tamaño variable** dependiendo de su clase,
    - porque **los datos de los objetos deberían almacenarse una sola vez** en el fichero,
    - porque **no se pueden almacenar y restaurar las referencias, ya que se corresponden con direcciones de memoria,** y al volver a cargar un objeto, éste ocupará una dirección de memoria diferente de la original;

![image055](/images/persona.svg) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![image055](/images/svg.png) 

**Flujos de Objetos**

- **La solución** consiste en **guardar en el fichero cada objeto** con un *“número de serie”* único;
  - Java proporciona los flujos de bytes **`ObjectOutputStream`** y **`ObjectInputStream`** para resolver automáticamente el problema de la **serialización de objetos**;
<br>
- **Al almacenar un objeto en el fichero**:
  - se **asocia un número de serie** a cada referencia,
  - al encontrar por primera vez una referencia, se **almacenan los datos del objeto** en el fichero y su número de serie,
  - las siguientes veces que se encuentre esa referencia, escribir **sólo el número de serie**;
<br>
- Para **almacenar (serializar)** los objetos se usa la clase **`ObjectOutputStream`**, que implementa el interfaz **`ObjectOutput`** que, a su vez, extiende el interfaz **`DataOutput`**, con lo que, además de poder escribir cualquier dato en formato binario, añade, entre otros, los siguientes métodos:

- que permiten serializar objetos en un flujo de **bytes**:

```java
public ObjectOutputStream(OutputStream out) throws IOException
public final void writeObject(Object obj) throws IOException
public void defaultWriteObject() throws IOException
```

- **Al restaurar un objeto del fichero**:
  - al restaurar por primera vez un objeto, se **crea**, se **inicializa con sus datos**, y se **recuerda la asociación** entre la nueva referencia y su número de serie,
  - al encontrar sólo su número de serie, **recuperar la referencia** de ese número de serie;

- Para **restaurar (deserializar)** los objetos se usa la clase **`ObjectInputStream`**, que implementa el interfaz **`ObjectInput`** que, a su vez, extiende el interfaz **`DataInput`**, con lo que, además de poder leer cualquier dato en formato binario, añade, entre otros, los siguientes métodos:

- **que permiten deserializar objetos desde un flujo de bytes**:

```java
public ObjectInputStream(InputStream in) throws IOException
public final Object readObject() throws IOException, ClassNotFoundException
public void defaultReadObject() throws IOException, ClassNotFoundException
```

---



[Anterior](../u4files/README.md) | [Subir nivel](../README.md) | [Siguiente](u1defaultSerialization/README.md)
