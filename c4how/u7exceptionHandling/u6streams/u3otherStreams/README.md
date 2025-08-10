# Otros Flujos






| **Flujos de conversión** |
| --- |
| 
* Las clases *InputStreamReader* permiten convertir bytes en caracteres


	+ Los objetos *InputStreamReader* reciben en su constructor un objeto *InputStream* que es capaz de leer bytes







```
public InputStreamReader(InputStream in)
```




* Los métodos read de *InputStreamReader* leen bytes de su *InputStream* y los convierten en caracteres


 | 
* Las clase *OuputStreamWriter* permite convertir caracteres en bytes


	+ Los objetos *OuputStreamWriter* reciben en su constructor un objeto *OutputStream* que es capaz de escribir bytes;







```
public OuputStreamWriter(OutputStream out)
```




* Los métodos write de *OutputStreamReader* convierten caracteres a bytes y los escriben en su *OutputStream*;


 |








| **Flujos de Datos** |
| --- |
| 
* Leer y escribir bytes y caracteres de texto es muy útil, pero a menudo se necesita transmitir **datos binarios de los tipos primitivos a través de un flujo**
* Los **interfaces *DataInput\_ y \_DataOutput*** declaran métodos que permiten leer y escribir datos en formato binario


 | 


```
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


 | 


```
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


 |







| **Varios flujos** |
| --- |
| 
* hay varios tipos de flujos que **definen comportamientos específicos, tanto en su modalidad de entrada como de salida**:


 |
| 
* los flujos de **tipo *Filter* aplican alguna operación de filtrado cuando leen o escriben datos utilizando otro flujo**


	+ un objeto *FilterReader* lee caracteres de otro objeto *Reader*, procesa los caracteres de alguna manera, y devuelve el resultado







```
protected FilterReader(Reader in)
```


 | 
* los flujos de **tipo *Piped* se diseñan en parejas, de forma que las escrituras que realiza un flujo de salida se pueden leer en otro flujo de entrada**






```
public PipedWriter(PipedReader snk) throws IOException
```


 |
| 
* los flujos de **tipo *Buffered* añaden almacenamiento intermedio en forma de *buffers*, de forma que las lecturas y escrituras no requieren acceder al sistema de ficheros en cada invocación**.


	+ Los flujos de caracteres de este tipo también proporcionan la **lectura y escritura de líneas de texto**,con retornos de línea







```
public BufferedReader(Reader in)
public BufferedWriter(Writer out)
```


 | 
* los llamados **flujos en memoria permiten usar estructuras de datos en memoria como fuente o destino de un flujo**:
* los **flujos *ByteArray*** usan un vector de byte,
* los **flujos *CharArray*** usan un vector de char,
* los **flujos *String*** usan objetos de la clase *String*;
* los **flujos de tipo *Print*** proporcionan los **métodos *print* y *println* que facilitan la escritura de valores de tipos primitivos y objetos en forma de texto legible**


	+ todos los flujos *Print* actúan como flujos *Filter*
	+ [***System.out* es un flujo *PrintStream***](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a1_interval/a2_statics/Console.java)



 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Ficheros](../u4files/README.md)


[Anterior](../u2characterStreams/README.md) | [Subir nivel](../README.md) | [Siguiente](../u4files/README.md)
