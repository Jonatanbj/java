# [Programación con Excepciones](README.md)

- #### [Elevación de Excepciones](u1exceptionThrowing/README.md)
- #### [Captura de Excepciones](u2exceptionCatching/README.md)
- #### [Delegación de Excepciones](u3exceptionDelegation/README.md)
- #### [Excepciones Polimorficas](u4polymorphicExceptions/README.md)
- #### [Clasificación de Excepciones](u5exceptionClassification/README.md)
- #### [Flujos](u6streams/README.md)




---
|      |       |
|-----------|-----
| • cuando se produce un **error de ejecución** en un programa, **se interrumpe bruscamente la ejecución secuencial de sus instrucciones**, es decir, no se ejecuta ninguna operación posterior a aquélla en la que se ha producido el error, y **se eleva o lanza una excepción que representa ese error**  | • por **defecto**, se muestra **por pantalla un informe del error producido**, pero esto es configurable por parte del programador con procesos para la recuperación del error |
| • las **excepciones**:<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • proporcionan una forma clara de indicar la existencia de posibles errores de ejecución, así como de comprobar la ocurrencia de dichos errores de ejecución sin oscurecer el código del programa <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • las excepciones se representan mediante **objetos de clases que pertenecen a la siguiente jerarquía**<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • cuando se produce una excepción **se crea un objeto de la clase adecuada, dependiendo del tipo de error producido**, que mantendrá la información sobre el error y proporcionará métodos para obtener dicha información, cosificación | ![Diagrama jerarquía](/images/Excepciones.svg)|
| • **Clase Throwable**:<br>o la raíz de la jerarquía de clasificación y, por tanto, es la **superclase de todas las excepciones**.<br>`public` `String` `toString() {}` (1)<br>`public` `void` `printStackTrace() {}` (2)<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `1` devuelve un **mensaje que informa** de la excepción<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; `2` imprime **por la salida estándar los métodos que estaban en la pila de ejecución** (llamadas anteriores a aquélla que produjo el error) cuando se produjo la excepción y la línea donde se produce la excepción. Es el comportamiento por **defecto** cuando no se maneja la excepción.             | • **Clase Error**:<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • representa las **excepciones graves que no deberían ser capturadas por un programa**<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; § `java.lang.VirtualMachineError` deriva de `java.lang.Error`<br><br>• **Clase Exception**:<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • representa las **excepciones normales que un programa podría capturar**  |
| • **Clase RuntimeException**:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • representa aquellas excepciones normales que **NO es necesario capturar en un programa**, se denominan **no comprobadas**<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;§ `java.lang.ArithmeticException` deriva de `java.lang.RuntimeException`, por división por cero | • **Clase IOException**:<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • el resto de clases que heredan de la clase **Exception** representan **aquellas excepciones que SI es necesario capturar en un programa**, estas excepciones se denominan **comprobadas** <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; § representan las excepciones comprobadas relacionadas con operaciones fallidas de entrada y salida <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;§ `java.io.FileNotFoundException` deriva de `java.io.IOException`, al tratar de abrir en modo lectura un fichero inexistente|   Gestión de excepciones      |    |

|Gestión de excepciones|Gestión de excepciones|
|--------|----------|
| • **elevar** la excepción: cuando una **biblioteca** o subsistema encuentra un error porque no se cumplen las condiciones de su uso<br><br>• **capturar** la excepción: cuando una **aplicación o biblioteca** usa un recurso (ficheros, comunicaciones, bibliotecas, ...) que puede dar problemas, hay que capturarlos para solventar esos problemas | • **delegar** la excepción:<br>  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; • cuando una aplicación o biblioteca usa un recurso (ficheros, comunicaciones, bibliotecas, ...) que pueden dar problemas, se **le comunica a quien corresponda para que los resuelva**<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;• cuando una aplicación o biblioteca usa un recurso (ficheros, comunicaciones, bibliotecas, ...) que pueden dar problemas, hay que capturarlos para **solventar en parte esos problemas y elevar otra excepción a quien corresponda para que resuelva el resto** |
                                                                                                                                                                                                               

---


[Anterior](../u6modularProgramming/README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u7exceptionHandling/u1exceptionThrowing/README.md)
