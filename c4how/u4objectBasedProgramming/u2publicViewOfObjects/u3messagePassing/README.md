# [Paso de mensajes](/java/c4how/u4objectBasedProgramming/u2publicViewOfObjects/u3messagePassing/README.md)


**Sintaxis**

`<expressioin>`.`<methodName>`([`<expression>`{, `<expression>`})]

**Ejemplo** 

* *donde el método (sin contemplar constructores ni destructores) debe estar presente en la interfaz de la clase del objeto y la lista de expresiones debe coincidir en número y tipos a la lista de parámetros del método;*


```java
intervalo.longitud()
new Intervalo(-100, 100).longitud()
edades.partido(5)
años.incluye(88)
edades.interseccion(años)
...
```
---

[Anterior](../u2objectReference/README.md) | [Subir nivel](../README.md) | [Siguiente](../u4objectArrayCreation/README.md)
