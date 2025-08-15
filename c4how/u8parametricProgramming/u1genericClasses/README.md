# [Clases Genéricas](README.md)

- #### [Clases genéricas y herencia](u1genericClassesAndInheritance/README.md)
- #### [Limitaciones de las clases genéricas](u2genericClassesLimitations/README.md)


---

**_Sintaxis_**

`class` `<ClaseGenerica>` <`<ParametroTipo1>`, ...,`<ParametroTipo2>`> {
  `private` `ParametroTipo1` `atributo;`
  `public` `ParametroTipo1` `metodo(ParametroTipo2` `parameter`) {
    ...
  }
 ...
}
...
`private` `<ClaseGenerica>`<`<Tipo1/Clasificador1>`, ...,`<Tipo2/Clasificador2>`> `objeto`
  = `new` `<ClaseGenerica>`<`<Tipo1/Clasificador1>`, ...,`<Tipo2/Clasificador2>`>(...)

<br>

- donde los **identificadores encerrados entre `<` y `>`** son los **parámetros de tipo**.
  - pueden usarse dentro de la **clase parametrizada** para declarar el tipo de sus **atributos**, los **argumentos** de sus métodos, o **objetos locales** de sus métodos.
  - se **especifican posteriormente con un tipo concreto** (actual) en la **instanciación** de un objeto de la clase parametrizada, o al declarar una **clase hija** de la clase parametrizada,  
    lo que produce la **encarnación de la clase parametrizada**, convirtiéndola en una **clase concreta** (proceso realizado en **tiempo de compilación**).
<br>
- **Dispensers** : [objects](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_dispensers/a8_parametrized/a1_object) – [generics](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_dispensers/a8_parametrized/a2_generic)

- **Map** : [iterator](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_dispensers/a8_parametrized/a4_map)

<br>

- Con esta solución **NO** es necesario convertir la dirección devuelta por el método **remove()** a una dirección de la clase concreta mediante el **operador de conversión de tipos (cast)**

- Al sacar un elemento **NO** existe la posibilidad de que se produzca un **error de conversión de tipos en tiempo de ejecución** al sacar los elementos, porque el error es **detectado en tiempo de compilación**, si se trata de meter elementos que no son de la **clase adecuada**.

 	

**_Ejemplo_**


```java
  try {
    BoundedQueue<Integer> boundedQueue = new BoundedQueue<Integer>(1);
    boundedQueue.add(2);
    // boundedQueue.add(new Fraction(1, 2)); No compila!!!
    int element = boundedQueue.remove();
    Console.getInstance().writeln(element);
  } catch (DispenserException e) {
    e.printStackTrace();
  }
```
<br>

* Por razones de compatibilidad con códigos anteriores a la **JDK 1.5**, está permitido el uso de las **clases parametrizadas** sin especificar sus parámetros, aunque el compilador genera un **aviso**

  * estas clases se denominan **tipos crudos** (*raw types*):

    * Se puede asignar una referencia de una **clase parametrizada** a un **tipo crudo**, y viceversa.

    * Una utilidad de los **tipos crudos** es poder crear vectores de **objetos** de **clases parametrizadas**, lo cual **Java** no permite en la actualidad;

<br>

```java
 BoundedQueue<Double> b0 = new BoundedQueue<Double>(10);
  b0.add(0.0);
  //b0.add(0); // Error!!!
  //b0.add(new Fraction(0,2)); // Error!!!
  Console.getInstance().writeln(""+b0.remove());
  BoundedQueue<Double> b1 = new BoundedQueue(10);
  b1.add(1.1);
  //b1.add(1); // Error!!!
  //b1.add(new Fraction(1,2)); // Error!!!
  Console.getInstance().writeln(""+b1.remove());
  BoundedQueue b2 = new BoundedQueue<Double>(10);
  b2.add(2.2);
  //b2.add(2); // Warning!!! y Error!!!
  //b2.add(new Fraction(2,2)); // Warning!!! y Error!!!
  Console.getInstance().writeln(""+b2.remove());
  BoundedQueue b3 = new BoundedQueue(10); // Integer!!!
  //b3.add(3.3); // Warning!!! y Error!!!
  b3.add(3);
  //b3.add(new Fraction(3,2)); // Warning!!! y Error!!!
  Console.getInstance().writeln(""+b3.remove());
  //BoundedQueue<Integer>[] a0 = new BoundedQueue<Integer>[3]; // Error!!!
  BoundedQueue<Integer>[] a0 = new BoundedQueue[3];
  for(BoundedQueue<Integer> boundedQueue : a0){
    boundedQueue = new BoundedQueue<>(5);
  }
```



---

[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u8parametricProgramming/u1genericClasses/u1genericClassesAndInheritance/README.md)
