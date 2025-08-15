# [Jerarquía de Paquetes](README.md)


| **Nombres de paquetes** | *Ejemplos* |
| :--- | :--- |
| - Permite agrupar un conjunto de clases, interfaces y enumerados, junto con archivos de recursos (como textos, imágenes, sonidos, …​) en paquetes <br> <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Un paquete puede contener, a su vez, otros paquetes, lo que produce una **organización jerárquica** y debe situarse en un directorio del sistema operativo, de acuerdo a la jerarquía de paquetes, cuya raíz puede estar en cualquier directorio <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - Cada paquete tiene un nombre, que comienza por minúsculas y que corresponde con la jerarquía de directorios del sistema operativo <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - El nombre del paquete debe ser único (como los directorios dentro de un directorio), lo cual es problemático si puede usarse en cualquier lugar del mundo, en cuyo caso, la ruta del nombre de los paquetes deberían comenzar con un nombre de dominio de Internet de la institución de desarrollo, en orden inverso  <br> <br> `<paquete1>`.`<paquete2>`. ... .`<paqueteN>` |  pooa.util.pooa.ter.modelos <br><br>![pooa.util.pooa.ter.modelos](/images/Ejemplo.png)  es.upm.eui.lpsi.pooa.util <br><br> ![es.upm.eui.lpsi.pooa.util](/images/Ejemplo2.png) |


| **Declaración de paquete** | *Ejemplo* |
| --- | --- |
| - Para **añadir una clase, interface y/o enumerado a un paquete** (clasificadores), hay que situar su fichero fuente en el directorio del paquete y, en la primera línea del código (sin contar los comentarios), escribir la sentencia de declaración de paquete ***package***, para indicar que el clasificador pertenece a ese paquete <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - En un fichero fuente **sólo puede aparecer una declaración de paquete**<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - Si en un fichero fuente no se especifica ningún paquete, la clase pertenecerá a un paquete sin nombre por defecto; <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- § Esto puede ser útil en el caso de aplicaciones con pocas clases |  package `<paquete1>`.`<paquete2>`. ... `<paqueteN>`; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br><br> ![MTablero](/images/Ejemplo3.png)|


```java
  package pooa.ter.modelos;

  class MTablero {
    ...
  }
```

---


[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](../u2classifierVisibility/README.md)
