# Serilización por defecto






| 
* en la serialización por defecto, todos los atributos que sean tipos primitivos o cadenas de texto se escriben con el formato usado en *DataOutputStream*;
* en la serialización por defecto, todos los campos que sean referencias a objetos deben ser, a su vez, serializables;
* si durante el proceso de serialización o deserialización se intenta almacenar o restaurar algún objeto no serializable, se eleva una excepción de la clase *NotSerializableException*;
* si durante la deserialización no se encuentra la clase de un objeto o no se puede cargar por otra razón, se eleva una excepción *ClassNotFoundException*;
* si una clase serializable es una subclase de otra clase no serializable, entonces los atributos de la superclase no son serializados;
* además, la superclase no serializable debe tener un constructor sin argumentos que sea accesible desde la subclase, para que la deserialización por defecto pueda inicializar los atributos de las superclase, en caso contrario se produce una excepción *InvalidClassException*;


 | 


```
import java.io.Serializable;
abstract class Persona implements Serializable {
      …
}
class Escuela {
  private void guardar() {
    ObjectOutputStream out = null;
    try {
        out = new ObjectOutputStream (new FileOutputStream("fichero.dat"));
        out.writeInt(numPersonas);
        for (int i = 0; i < numPersonas; i++) {
            out.writeObject(personas[i]);
               }
         } catch (IOException ex) {
            System.out.println("IOException al escribir: " +
                        ex.getMessage());
         } finally {
            if (out != null) {
                try {
                    out.close();
                } catch (IOException ex) {
                  System.out.println("IOException al cerrar: " +
                              ex.getMessage());
                }
            }
    }
}
private void restaurar() {
  personas = new Persona[100];
  numPersonas = 0;
  ObjectInputStream in = null;
  try {
    in = new ObjectInputStream (new FileInputStream("fichero.dat"));
    int total = in.readInt();
    for (int i = 0; i < total; i++) {
        personas[numPersonas] = (Persona) in.readObject();
        numPersonas++;
    }
  } catch (IOException ex) {
    System.out.println("IOException al leer: " +
            ex.getMessage());
  } catch (ClassNotFoundException ex) {
    System.out.println("ClassNotFoundException al leer: " +
            ex.getMessage());
  } finally {
    if (in != null) {
        try {
            in.close();
        } catch (IOException ex) {
            System.out.println("IOException al cerrar: " +
                ex.getMessage());
        }
    }
  }
}
```


 |
| 
* otra solución más sencilla es escribir y leer directamente el vector en el fichero, en lugar de hacerlo elemento a elemento:


 | 


```
class Escuela {
     private void guardar() {
         ObjectOutputStream out = null;
         try {
            out = new ObjectOutputStream (new
FileOutputStream("fichero.dat"));
            out.writeInt(numPersonas);
            out.writeObject(personas);
         } catch (IOException ex) {
             System.out.println("IOException al escribir: " +
                     ex.getMessage());
         } finally {
            if (out != null) {
                try {
                     out.close();
                } catch (IOException ex) {
                    System.out.println("IOException al cerrar: " +
                        ex.getMessage());
                }
         }
      }
}
private void restaurar() {
    numPersonas = 0;
    ObjectInputStream in = null;
    try {
        in = new ObjectInputStream (new FileInputStream("fichero.dat"));
        int total = in.readInt();
        personas = (Persona[]) in.readObject();
        numPersonas = total;
    } catch (IOException ex) {
        System.out.println("IOException al leer: " +
    ex.getMessage());
    } catch (ClassNotFoundException ex) {
        System.out.println("ClassNotFoundException al leer: " +
              ex.getMessage());
    } finally {
        if (in != null) {
            try {
                 in.close();
            } catch (IOException ex) {
                System.out.println("IOException al cerrar: " +
                     ex.getMessage());
            }
        }
    }
}
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Serialización personalizadas](../u2customSerialization/README.md)
