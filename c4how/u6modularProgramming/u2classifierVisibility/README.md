# [Visibilidad de Clasificadores](README.md)

* La visibilidad de las clases de un paquete es:


	+ Las clases declaradas ***public*** son **accesibles desde cualquier código exterior al paquete**
	
	
		- Si hay una **clase publica, entonces el nombre del fichero debe coincidir con el nombre de esa clase, y con extensión *.java***
		- En un fichero fuente puede haber varias declaraciones de clases, pero como máximo una de ellas puede ser *public*;
		
		
			* La recomendación es disponer los clasificadores en distintos ficheros, siendo excepcional y poco recomendado para alguna clase auxiliar
	
	+ Las clases NO declaradas *public* sólo son **accesibles solo desde el código de ese paquete** (tampoco desde sus subpaquetes); <br><br>

 
* *MTablero.java*

```JAVA
package pooa.ter.modelos;

public class MTablero {
 ...
}
```

* *CAbrir.java*



```JAVA
package pooa.ter.controladores;

public class CAbrir {
  ...
}
class CPoner {
  ...
}
class CMover {
  ...
}
```

---



[Anterior](../u1packageHierarchy/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3classifierImporting/README.md)
