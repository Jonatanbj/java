# [Creación de vectores de objetos](/java/c4how/u4objectBasedProgramming/u2publicViewOfObjects/u4objectArrayCreation/README.md)

**new** es operador unario prefijo cuyo operando es un vector de referencias a objetos de una clase y devuelve la dirección de memoria donde se ha reservado el espacio para dicho vector; <br> ![Sinstaxisg](/images/SintaxisG.jpg) <br>
- donde la expresión debe ser de tipo entero y determina la longitud de referencias del vector inicializadas a **null**; 
 


**Ejemplo** 

```java
new Intervalo[100]
```

**Sintaxis h** 

new `<Clase>`[] {`<expresion>`,..., `<expresion>`} <br><br> 
- donde cada expresión debe ser una dirección a un objeto de la clase que inicializan las referencias del vector creado de longitud igual al número de expresiones;

**Ejemplo** 


```java
   Intervalo intervalo = new Intervalo();
new Intervalo[] {new Intervalo(), null, intervalo}
```

---


[Anterior](../u3messagePassing/README.md) | [Subir nivel](../README.md) | [Siguiente](../u5referenceArrayCreation/README.md)
