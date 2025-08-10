# Serialización personalizadas






|  | **Ejemplos** |
| --- | --- |
| 
* en ciertas ocasiones es necesario personalizar el mecanismo de serialización por defecto de Java; por ejemplo:
* ciertos atributos de los objetos de la clase no deben serializarse porque contienen información redundante o que no tiene sentido después del proceso (por ejemplo, enlaces de listas, referencias de ficheros abiertos, ventanas, etc.);
* ciertos atributos de los objetos de la clase no implementan el interfaz *Serializable*, por lo que no deben serializarse mediante el mecanismo por defecto, sino que deben ser esos objetos los que deben responsabilizar almacenar y restaurar sus atributos;
* una clase es una subclase de otra clase no serializable, y también se debe responsabilizar de almacenar y restaurar sus atributos heredados;
* para indicar que algún atributo de una clase no debe ser serializado por el mecanismo por defecto, se añade a la declaración del atributo el modificador transient;


 | 


```
import pooa.util.Lista; // NO SERIALIZABLE
class AlumnoDinamico extends Persona {
      private transient Lista profesores = new Lista(); // NO
SERIALIZABLE
      private int numProfesores = 0;
      …
}
```


 |
| 
* cuando no se desea usar el mecanismo de serialización por defecto para una clase, se deben definir los siguientes métodos, respetando exactamente sus cabeceras:


 | 


```
private void readObject(ObjectInputStream in)
  throws IOException, ClassNotFoundException
private void writeObject(ObjectOutputStream out)
  throws IOException
```


 |
| 
* en cuyo caso, los objetos de la clase no se serializan ni deserializan por el mecanismo por defecto, sino que:


	+ en la serialización se invoca al método *writeObject* para que el objeto haga el proceso de la manera oportuna;
	+ en la deserialización, sólo se crea el objeto de la clase, y se invoca el método *readObject* para que el objeto haga el proceso;



 | 


```
import pooa.util.Lista; // NO SERIALIZABLE
class AlumnoDinamico extends Persona {
      private float nota = 0.1f;
      private transient Lista profesores = new Lista(); // NO
SERIALIZABLE
      …
      private void writeObject(ObjectOutputStream out)
              throws IOException {
         out.defaultWriteObject();
         out.writeInt(profesores.size());
         Iterador iterador = profesores.iterador();
         while (iterador.hasNext()) {
            Profesor profesor = (Profesor) iterador.next();
            out.writeObject(profesor);
         }
     }
private void readObject(ObjectInputStream in)
         throws IOException, ClassNotFoundException {
     in.defaultReadObject();
     profesores = new Lista();
     int numProfesores = in.readInt();
     for (int i = 0; i < numProfesores; i++) {
         Profesor profesor = (Profesor) in.readObject();
         profesores.add(profesor);
     }
}
```


 |


---

[Volver al nivel superior](../README.md)



[Anterior](../u1defaultSerialization/README.md) | [Subir nivel](../README.md) | [Siguiente](../README.md)
