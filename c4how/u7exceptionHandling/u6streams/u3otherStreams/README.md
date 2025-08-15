# [Otros Flujos](README.md)

| **Flujos de conversión** | |
| :--- |:--- |
| - Las clases ***InputStreamReader*** permiten convertir bytes en caracteres <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - Los objetos ***InputStreamReader*** reciben en su constructor un objeto ***InputStream*** que es capaz de leer bytes <br><br> `public` `InputStreamReader(InputStream in)` <br> - Los métodos read de ***InputStreamReader*** leen bytes de su ***InputStream*** y los convierten en caracteres | - Las clase ***OuputStreamWriter*** permite convertir caracteres en bytes <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - Los objetos ***OuputStreamWriter*** reciben en su constructor un objeto ***OutputStream*** que es capaz de escribir bytes; <br> `public` `OuputStreamWriter(OutputStream out)` <br> - Los métodos write de ***OutputStreamReader*** convierten caracteres a bytes y los escriben en su ***OutputStream***;|

**Flujos de Datos**

* Leer y escribir bytes y caracteres de texto es muy útil, pero a menudo se necesita transmitir **datos binarios de los tipos primitivos a través de un flujo**
* Los **interfaces *DataInput\_ y \_DataOutput*** declaran métodos que permiten leer y escribir datos en formato binario

```java
interface DataInput {
  boolean readBoolean();
  char readChar();
  short readShort();
  int readInt();
  long readLong();
  float readFloat();
  double readDouble();
  String readUTF();
}
```

```java
interface DataOutput {
  writeBoolean(boolean);
  writeChar(char);
  writeShort(short);
  writeInt(int);
  writeLong(long);
  writeFloat(float);
  writeDouble(double);
  writeUTF(String);
}
```
<br>

**Varios flujos**

<br>

* hay varios tipos de flujos que **definen comportamientos específicos, tanto en su modalidad de entrada como de salida**:<

|         |            |
|---------|------------|
| •   los flujos de **tipo Filter aplican alguna operación de filtrado cuando leen o escriben datos utilizando otro flujo** <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • un objeto *FilterReader* lee caracteres de otro objeto *Reader*, procesa los caracteres de alguna manera, y devuelve el resultado<br><br>`java` `protected` `FilterReader(Reader in)` | • los flujos de **tipo Piped** se diseñan en parejas, de forma que las escrituras que realiza un flujo de salida se pueden leer en otro flujo de entrada<br><br>`java` `public` `PipedWriter(PipedReader snk)` `throws IOException<br>`                                  |
| • los flujos de **tipo Buffered añaden almacenamiento intermedio en forma de buffers, de forma que las lecturas y escrituras no requieren acceder al sistema de ficheros en cada invocación**<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • Los flujos de caracteres de este tipo también proporcionan la lectura y escritura de líneas de texto, con retornos de línea<br><br>`java` `public` `BufferedReader(Reader in)` `public` `BufferedWriter(Writer out)`| • los llamados **flujos en memoria** permiten usar estructuras de datos en memoria como fuente o destino de un flujo:<br>   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • los flujos **ByteArray** usan un vector de byte,<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   • los flujos **CharArray** usan un vector de char,<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • los flujos **String** usan objetos de la clase String;<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • los flujos de **tipo Print** proporcionan los métodos *print* y *println* que facilitan la escritura de valores de tipos primitivos y objetos en forma de texto legible   <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  •  todos los flujos Print actúan como flujos Filter  <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; •  **System.out es un flujo PrintStream** |



---


[Anterior](../u2characterStreams/README.md) | [Subir nivel](../README.md) | [Siguiente](../u4files/README.md)
