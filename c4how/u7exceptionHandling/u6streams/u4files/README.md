# [Ficheros](README.md)


* los **flujos *File (FileInputStream, FileOutputStream, FileReader y FileWriter)*** permiten tratar a un **fichero como un flujo de entrada o de salida**;

  + Para crear un objeto, se usa un **constructor que recibe como argumento el nombre del fichero**;

**Ejemplo:**

```java
FileWriter outTxt = new FileWriter("salida.txt");
FileReader inTxt = new FileReader("entrada.txt");
FileOutputStream outDat = new FileOutputStream("salida.dat");
FileInputStream inDat = new FileInputStream("entrada.dat");
```

**Ficheros de texto**
 
* [Clase plantilla](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_itinerario/a5_excepciones/a1_writeText/App.java) para **escribir en un fichero de texto** se usa la **clase *PrintWriter***

```java
package es.usantatecla.a0\_itinerario.a5\_excepciones.a1\_writeText;

import java.io.IOException;
import java.io.PrintWriter;

class App {

  public static void main(String[] args) {
    PrintWriter out = null;
    try {
      out = new PrintWriter("./src/main/resources/fichero.txt");
      out.print(1);
      out.print(':');
      out.print(" juan = ");
      out.println(5.5);
      out.println(2 + ": jose = " + 7.2);
      Console.getInstance().writeln("Fichero generado");
    } catch (IOException ex) {
      Console.getInstance().writeln("IOException al escribir:" + ex.getMessage());
    } finally {
      if (out != null) {
        out.close();
      }
    }
  }
}
```


* [Clase plantilla](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_itinerario/a5_excepciones/a2_readText/App.java) para **leer de un fichero de texto** se usa la **clase *BufferedReader***



```java
package es.usantatecla.a0\_itinerario.a5\_excepciones.a2\_readText;

import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

class App {

  public static void main(String[] args) {
    BufferedReader in = null;
    try {
      in = new BufferedReader(new FileReader("./src/main/resources/fichero.txt"));
      String linea;
      while ((linea = in.readLine()) != null) {
        System.out.println(linea);
      }
    } catch (IOException ex) {
      System.out.println("IOException al leer: " + ex.getMessage());
    } finally {
      if (in != null) {
        try {
          in.close();
        } catch (IOException ex) {
          System.out.println("IOException al cerrar: " + ex.getMessage());
        }
      }
    }
  }
}
```


**Ficheros binarios** 

* [Clase plantilla](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/a0_itinerario/a5_excepciones/a3_writeBinary/App.java) para **escribir en un fichero binario** se usa la **clase *DataOutputStream***

```java
package es.usantatecla.a0\_itinerario.a5\_excepciones.a3\_writeBinary;

import java.io.DataOutputStream;
import java.io.FileOutputStream;
import java.io.IOException;

class App {

  public static void main(String[] args) {
    DataOutputStream out = null;
    try {
      out = new DataOutputStream(new FileOutputStream("./src/main/resources/fichero.dat"));
      out.writeInt(1);
      out.writeChar(':');
      out.writeUTF(" juan = ");
      out.writeDouble(5.5);
      Console.getInstance().writeln("Fichero generado");
    } catch (IOException ex) {
      System.out.println("IOException al escribir: " + ex.getMessage());
    } finally {
      if (out != null) {
        try {
          out.close();
        } catch (IOException ex) {
          System.out.println("IOException al cerrar: " + ex.getMessage());
        }
      }
    }
  }
}
```

* [Clase plantilla](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_itinerario/a5_excepciones/a4_readBinary/App.java) para **leer de un fichero binario** se usa la **clase *DataInputStream***


```java
package es.usantatecla.a0\_itinerario.a5\_excepciones.a4\_readBinary;

import java.io.DataInputStream;
import java.io.FileInputStream;
import java.io.IOException;

class App {

  public static void main(String[] args) {
    DataInputStream in = null;
    try {
      in = new DataInputStream(new FileInputStream("./src/main/resources/fichero.dat"));
      System.out.println(in.readInt() + String.valueOf(in.readChar()) +
          in.readUTF() + in.readDouble());
      System.out.println(in.readInt() + String.valueOf(in.readChar()) +
          in.readUTF() + in.readDouble());
    } catch (IOException ex) {
      System.out.println("IOException al leer: " + ex.getMessage());
    } finally {
      if (in != null) {
        try {
          in.close();
        } catch (IOException ex) {
          System.out.println("IOException al cerrar: " + ex.getMessage());
        }
      }
    }
  }
}
```

---


[Anterior](../u3otherStreams/README.md) | [Subir nivel](../README.md) | [Siguiente](../u5objectSerialization/README.md)
