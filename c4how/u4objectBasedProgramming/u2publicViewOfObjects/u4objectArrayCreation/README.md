# Creación de vectores de objetos







|  | **Sintaxis g** | **Ejemplo** |
| --- | --- | --- |
| 
**new** es operador unario prefijo cuyo operando es un vector de referencias a objetos de una clase y devuelve la dirección de memoria donde se ha reservado el espacio para dicho vector;
 | 

height32



* donde la expresión debe ser de tipo entero y determina la longitud de referencias del vector inicializadas a **null**;


 | 


```
new Intervalo[100]
```


 |







| **Sintaxis h** | **Ejemplo** |
| --- | --- |
| 


```
new <Clase>[] {<expresion>,..., <expresion>}
```




* donde cada expresión debe ser una dirección a un objeto de la clase que inicializan las referencias del vector creado de longitud igual al número de expresiones;


 | 


```
   Intervalo intervalo = new Intervalo();
new Intervalo[] {new Intervalo(), null, intervalo}
```





height32

 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Referencia a un vector de referencias a objetos](../u5referenceArrayCreation/README.md)
