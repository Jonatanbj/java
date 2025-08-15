# [Clase Object](README.md)


* Toda clase "no derivada" explícitamente hereda implícitamente de la clase predefinida *Object*


	+ Proporciona un conjunto de **métodos comunes a todas las clases**, algunos de ellos susceptibles de ser redefinidos en cualquier clase de la manera oportuna.
	
	
		- además, métodos para la sincronización de programas concurrentes y para usar la reflexión


```java

class Object {
  public boolean equals(Object)
  public String toString()
  public int hashCode()
  protected Object clone()
  protected void finalize()
  ...
}
```


---

[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u5objectOrientedProgramming/u9inheritanceAndEnums/README.md)
