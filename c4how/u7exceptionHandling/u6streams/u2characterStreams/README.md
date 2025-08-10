# Flujos de Caracteres



![FlujoDeCaracteres.svg](images/FlujoDeCaracteres.svg.png)




![FlujoDeCaracteres2](images/FlujoDeCaracteres2.svg)







| 


```
class Reader {
  public int read() throws IOException
  public int read(char[] cbuf) throws IOException
  public abstract int read(char[] cbuf, int off, int len) throws IOException
  public long skip(long n) throws IOException
  public boolean ready() throws IOException
  public abstract void close() throws IOException
}
```


 | 


```
class Writer {
  public void write(int c) throws IOException { ... }
  public void write(char[] cbuf) throws IOException { ... }
  public abstract void write(char[] cbuf, int off, int len) throws IOException { ... }
  public void write(String str) throws IOException { ... }
  public void write(String str, int off, int len) throws IOException { ... }
  public Writer append(char c) throws IOException { ... }
  public Writer append(CharSequence csq) throws IOException { ... }
  public Writer append(CharSequence csq, int start, int end) throws IOException { ... }
  public abstract void flush() throws IOException { ... }
  public abstract void close() throws IOException { ... }
}
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Otros Flujos](../u3otherStreams/README.md)


[Anterior](../u1byteStreams/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3otherStreams/README.md)
