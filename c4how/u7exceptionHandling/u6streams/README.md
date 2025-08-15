# [Flujos](README.md)

- #### [Flujos de Bytes](u1byteStreams/README.md)
- #### [Flujos de Caracteres](u2characterStreams/README.md)
- #### [Otros Flujos](u3otherStreams/README.md)
- #### [Ficheros](u4files/README.md)
- #### [Serialización de Objetos](u5objectSerialization/README.md)
---
- **Los flujos**, *streams*, son objetos que representan secuencias ordenadas de datos que tienen una **fuente**, flujos de entrada, o un **destino**, flujos de salida;

  - Las clases de entrada/salida del paquete **java.io** se definen en términos de flujos, y permiten a los programadores abstraerse de los detalles específicos del sistema operativo al acceder a los recursos del sistema, tales como ficheros, teclado, líneas de comunicaciones, etc.;
<br>
- **Tipos de flujos en la biblioteca**:

  - **de entrada y salida de bytes**, cuyas clases abstractas de las que heredan todas las demás son **InputStream** y **OutputStream**

  - **de entrada y salida de caracteres**, cuyas clases abstractas de las que heredan todas las demás son **Reader** y **Writer**, donde un caracter Unicode puede estar formado por varios bytes

---

[Anterior](../u5exceptionClassification/README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u7exceptionHandling/u6streams/u1byteStreams/README.md)
