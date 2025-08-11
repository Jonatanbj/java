# [Polimorfismo](README.md)

- #### [Formalización](u1formalization/README.md)
- #### [Polimorfismo vs sobrecarga](u2polymorphismVsOverloading/README.md)
- #### [Beneficios del Polimorfismo](u3polymorphismBenefits/README.md)

---
  **Introducción** <br><br> 

   - Término de origen griego que significa **"muchas formas"**. <br>
     * _Una persona puede pagar con tarjeta o con efectivo._
     + _Una empresa de transporte realiza ventas de billetes por ventanilla o a través de una máquina._
     + _Un sistema operativo imprime a través de drivers de impresora para cada modelo._
     + _Un navegador muestra textos, imágenes, videos, etc., con muy diversos formatos._
<br>

  + No se contempla que algo cambie de forma o sea de dos clases de cosas a la vez.
    + Una persona de ventanilla **NO** se convierte en máquina expendedora.
    + Una persona **NO** es a la vez una máquina expendedora.
    + Simplemente, un billete lo puede vender una persona o una máquina expendedora en cada momento que se vende un billete.

- A lo largo de la historia, en este mundo existe la jerarquía de personas: **mujeres** y **hombres**.  
  - Pero en ciertos momentos y en ciertos países, no existe polimorfismo: el lugar de una mujer no lo puede ocupar un hombre y el de un hombre no lo puede ocupar una mujer.  
  - Mientras que, en otros momentos u otros países, el lugar de una persona es indiferentemente ocupado por una mujer o un hombre.

```java
Person person;

// person = new Person(); // ERROR: Clase abstracta
person = new Woman();
person = new Man();

Woman woman;

// woman = new Person(); // ERROR: Clase abstracta
woman = new Woman();
// woman = new Man(); // ERROR: Clase no derivada de Woman

Man man;

// man = new Person(); // ERROR: Clase abstracta
// man = new Woman(); // ERROR: Clase no derivada de Man
man = new Man();
```

- Donde no se contempla que una mujer se convierta en hombre o un hombre en mujer.
- Ni se contempla que alguien sea mujer y hombre a la vez.
- Lo único que se contempla es que una referencia a `Person` apunte a un objeto de la clase `Woman` u `Man` en cada instante del tiempo.

**Definición**

- <span style="color:DodgerBlue">El polimorfismo</span> es una relajación del sistema de tipos, de tal manera que una referencia declarada de una clase (atributo, parámetro o declaración local o elemento de un vector) acepta la asignación de la dirección de un objeto de dicha clase o de alguna de sus clases derivadas (hija, nieta, …).

  - Por tanto:  
    - <span style="color:green">exige la existencia de una jerarquía de clasificación mediante relaciones de herencia</span>  
    - <span style="color:red">pero las jerarquías de clasificación NO exigen tratamientos polimórficos</span>

En un punto dado, existen listas, en otro punto, existen conjuntos y, en otro punto, pueden existir indiferentemente listas o conjuntos





```java
Set set;

// set = new List(); // ERROR: List no es una subclase de Set

set = new Set();

List list;

list = new List();

// list = new Set(); // ERROR: Set no es una subclase de List
```

- <span style="color:red">donde un objeto se crea de una clase y siempre será de esa clase</span> mientras que la referencia puede tener, en un momento dado, una dirección de un objeto lista o de un objeto conjunto.

- con la incorporación del <span style="color:red">polimorfismo</span>, tiene sentido declarar referencias a <span style="color:red">clases abstractas</span> con la intención de almacenar direcciones de objetos de <span style="color:red">clases concretas derivadas</span>, **NO** de <span style="color:red">clases abstractas que no son instanciables</span>.


**<span style="color:DodgerBlue">Comportamiento:</span>**

  - cuando <span style="color:DodgerBlue">se lanza un mensaje a un objeto a través de una referencia polimórfica se ejecuta el método prescrito en la clase del objeto que recibe el mensaje</span>, <span style="color:red">independientemente de la clase de la declaración de la referencia</span>.

```java
List list;
list = new List();
list.insertFirst(5); // con repetición
list = new Set();
list.insertFirst(5); // sin repetición
```

- **<span style="color:red">Limitación:</span>**

  - cuando <span style="color:dodgerBlue">se lanza un mensaje a un objeto a través de una referencia polimórfica, éste debe estar contemplado en el interfaz de clase de la que se declaró la referencia</span>, <span style="color:red">sin contemplar los posibles métodos añadidos en la clase del objeto apuntado</span>.

```java
List list1 = new Set();
List list2 = new Set();
...
Set set1 = new Set();
Set set2 = new Set();
set1.intersection(set2);
...
```


---




[Anterior](../u6inheritanceBenefits/README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u5objectOrientedProgramming/u7polymorphism/u1formalization/README.md)
