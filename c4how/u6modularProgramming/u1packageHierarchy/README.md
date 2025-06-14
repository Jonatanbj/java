# Jerarquía de Paquetes






| **Nombres de paquetes** | *Ejemplos* |
| --- | --- |
| 
* Permite agrupar un conjunto de clases, interfaces y enumerados, junto con archivos de recursos (como textos, imágenes, sonidos, …​) en paquetes


	+ Un paquete puede contener, a su vez, otros paquetes, lo que produce una **organización jerárquica** y debe situarse en un directorio del sistema operativo, de acuerdo a la jerarquía de paquetes, cuya raíz puede estar en cualquier directorio
	+ Cada paquete tiene un nombre, que comienza por minúsculas y que corresponde con la jerarquía de directorios del sistema operativo
	+ El nombre del paquete debe ser único (como los directorios dentro de un directorio), lo cual es problemático si puede usarse en cualquier lugar del mundo, en cuyo caso, la ruta del nombre de los paquetes deberían comenzar con un nombre de dominio de Internet de la institución de desarrollo, en orden inverso







```
  <paquete1>.<paquete2>. ... .<paqueteN>
```


 | 


```
  pooa.util
  pooa.ter.modelos
```


 |
| 

height32

 |
| 


```
  es.upm.eui.lpsi.pooa.util
```


 |
| 

height32

 |







| **Declaración de paquete** | *Ejemplo* |
| --- | --- |
| 
* Para **añadir una clase, interface y/o enumerado a un paquete** (clasificadores), hay que situar su fichero fuente en el directorio del paquete y, en la primera línea del código (sin contar los comentarios), escribir la sentencia de declaración de paquete ***package***, para indicar que el clasificador pertenece a ese paquete


	+ En un fichero fuente **sólo puede aparecer una declaración de paquete**
	+ Si en un fichero fuente no se especifica ningún paquete, la clase pertenecerá a un paquete sin nombre por defecto;
	
	
		- Esto puede ser útil en el caso de aplicaciones con pocas clases



 | 


```
 package <paquete1>.<paquete2>. ... <paqueteN>;
```


 |
| 

height32

 |
| 


```
  package pooa.ter.modelos;

  class MTablero {
    ...
  }
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Visibilidad de Clasificadores](../u2classifierVisibility/README.md)
