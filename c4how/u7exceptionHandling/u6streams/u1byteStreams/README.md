# Flujos de Bytes



![FlujoDeBytes](images/FlujoDeBytes.svg)




![FlujoDeBytes2](images/FlujoDeBytes2.svg)







| 


```
class InputStream {
  public abstract int read() throws IOException { ... }
  public int read(byte[] b) throws IOException { ... }
  public int read(byte[] b, int off, int len) throws IOException { ... }
  public long skip(long n) throws IOException { ... }
  public int available() throws IOException { ... }
  public void close() throws IOException { ... }
}
```


 | 


```
class OutputStream {
  public abstract void write(int b) throws IOException { ... }
  public void write(byte[] b) throws IOException { ... }
  public void write(byte[] b, int off, int len) throws IOException { ... }
  public void flush() throws IOException { ... }
  public void close() throws IOException { ... }
}
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Flujos de Caracteres](../u2characterStreams/README.md)


[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](../u2characterStreams/README.md)
