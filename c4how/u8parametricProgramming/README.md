# [Programación Parametrizada](README.md)

- #### [Clases Genéricas](u1genericClasses/README.md)
- #### [Parámetros Limitados](u2boundedTypeParameters/README.md)
- #### [Parámetros Comodines](u3wildcardParameters/README.md)
- #### [Métodos Genéricos](u4genericMethods/README.md)
- #### [Colecciones](u5collections/README.md)

---

  - **Se desea definir clases** cuyos atributos puedan ser de **cualquier clase**, y para definir métodos que puedan recibir **argumentos** y devolver **resultados** de cualquier clase.  
    - Una posible solución sería declarando los atributos de estas clases y los argumentos de estos métodos con el **tipo más débil posible**, por ejemplo, `Object`.  
      - Con esta solución es necesario convertir la dirección devuelta por el método `remove()`, que es de la clase `Object`, a una dirección de la clase concreta mediante el **operador de conversión de tipos** (*cast*).  
      - Al sacar un elemento existe la posibilidad de que se produzca un **error de conversión de tipos en tiempo de ejecución** al sacar los elementos, que **no es detectado en tiempo de compilación**, si los objetos que se meten en la pila son de distinta clase de la que se espera que sean al sacarlos. <br>
+ **Genericos**
<br>

  - Estos problemas se pueden resolver mediante la **declaración de una clase parametrizada**, que permita declarar la clase de los elementos de la pila como un **parámetro de tipo**.  
    - A partir de la **JDK 1.5** se pueden declarar **clases, interfaces y métodos parametrizados**, mediante los **parámetros de tipo** (también llamados **variables de tipo**).  
    - Las clases parametrizadas se denominan **clases genéricas**; y los métodos parametrizados se denominan **métodos genéricos**.  
    - **Ventajas**:
      - proporcionan una **comprobación estricta de tipos en tiempo de compilación**;
      - su uso **no necesita comprobación de tipos en tiempo de ejecución**;
      - producen **código más robusto** y, en consecuencia, aumentan la **facilidad de mantenimiento** de los programas.

- **Dispensers:** [fractions](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_dispensers/a7_modular) - [objects]()



```java
---
9: 1
10: 0
Exception in thread "main" java.lang.ClassCastException: class es.usantatecla.aX_dispensers.a8_parametrized.a1_object.utils.Fraction cannot be cast to class java.lang.Integer (es.usantatecla.aX_dispensers.a8_parametrized.a1_object.utils.Fraction is in unnamed module of loader 'app'; java.lang.Integer is in module java.base of loader 'bootstrap')
        at es.usantatecla.aX_dispensers.a8_parametrized.a1_object.App.main(App.java:49)
```


---


[Anterior](/c4how/u7exceptionHandling/u6streams/u5objectSerialization/u2customSerialization/README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u8parametricProgramming/u1genericClasses/README.md)
