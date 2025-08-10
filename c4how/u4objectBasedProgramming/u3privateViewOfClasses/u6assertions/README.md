# [Aserciones](./README.md)



| <font color="darkred">Error es una acción que produce un resultado incorrecto</font> | <font color="darkred">Defecto es la imperfección de un componente causado por un error</font> | <font color="darkred">Fallo es la manifestación visible de un defecto</font> |
:-------------------------------------------------------------|:-------------------------------------------------------------|:-------------------------------------------------------------|
| - Ej: un conductor analiza mal el contexto de la circulación <br> - Ej: un programador escribe mal una sentencia, incumpliendo reglas léxico/ sintáctico/ semánticas <br> - Ej: un programador diseña mal un algoritmo, produciendo un bucle infinito | - Ej: un conductor establece una velocidad, giro, ... inadecuados <br> - Ej: un programa produce una incompatibilidad de tipos entre un operador y un operando <br> - Ej: un programa con una condición en una sentencia iterativa infinita | - Ej: se produce un accidente <br> - Ej: el programa no compila <br> - Ej: el programa no responde |

## Tipos de Errores
* **Errores en Tiempo de Compilación** producidos por el incumplimiento de reglas:
  - reglas léxicas,
  - reglas sintácticas y/o
  - reglas semánticas del lenguaje fuerte o débilmente tipado;

<br>

* **Errores en Tiempo de Ejecución**
<br>

  * **Errores Lógicos** producidos por la lógica de un programa que no contempla todos los posibles situaciónes del sistema de información
    - Sentencias `assert` para pre-condiciones
    - Pruebas de software para post-condiciones
<br> 

  * **Errores Excepcionales** producidos por recursos (bibliotecas / frameworks para gestión de ficheros, comunicaciones, …​, arquitectura) fuera del ámbito del software que los maneja.
    - <font color="darkred"> Se gestionan con objetos de la clase Exception y la sentencia *try/catch/finally*</font>

## Contexto y Responsabilidades
 **Contexto** 
+ ciertos errores lógicos (ej.: un valor negativo para calcular un factorial, una referencia sin la dirección del objeto, …​) pueden ser un error lógico o excepcional <font color="darkblue">dependiendo del software en el que se está desarrollando:</font> 

 | **Aplicación** | **Biblioteca** |
|--------------|------------|
| - debe responsabilizarse de la detección y subsanación de los errores lógicos dentro de su ámbito durante el desarrollo. <br> - los errores en la entrada de datos del usuario no son errores del desarrollo y se solventan mediante la validación de la entrada de datos, sentencia iterativa hasta alcanzar la condición deseada | - NO puede responsabilizarse del uso indebido de los servicios prestados a las aplicaciones y NUNCA debe responsabilizarse de la subsanación de dichos errores. <br> - En estos casos, estos errores lógicos se considerarán excepcionales porque la causa del error está fuera de los límites del software de la biblioteca.|


* Ej. la función factorial contemplará:

  * pre-condiciones para verificar si la entrada es correcta (el argumento no es negativo) mediante

  * la sentencia assert en el código de producción

  * la elevación de una excepción en el código de producción

  * post-condiciones para verificar si la salida es correcta (n! = 1 si n = 0 si no n * (n-1)!) mediante la librería aseertThat en el código de pruebas




```java
class Interval {
  ...
  public Interval[] split(int times) {
    Interval[] intervals = new Interval[times];
    final double length = this.length() / times;
    final double min = this.min;
    final double max = min + length;
    for (int i = 0; i < times; i++) {
      intervals[i] = new Interval(min, max);
      min = max;
      max += length;
    }
    return intervals;
  }
  ...
}

class App {

  public static void main(String[] args){
    Console console = new Console();
    Interval interval = new Interval();
    interval.read();
    int times = console.readInt("¿Partir en cuántas veces? ");
    Interval[] intervals = interval.split(times);
  }
}
```
* cuando se solicita el número de veces, si el usuario introduce un valor negativo, se produce un error de ejecución, se muestra por pantalla un informe del error producido (reserva de un vector cuyo tamaño es negativo), y finaliza la ejecución del programa


```java
Introduce el minimo: 1
Introduce el maximo: 5
Veces: -1
Exception in thread "main" java.lang.NegativeArraySizeException
        at Intervalo.valores (Intervalo.java:141)
        at Aplicacion.main (Aplicacion.java:7)
```
#### <font color="darkred">Programación defensiva</font>

* si se trata de una aplicación, la solución NO es que el método compruebe la corrección de su argumento y que, en el caso de que no sea correcto, gestione el error acoplándose con un mensaje a la consola, …​:
```java
class Interval {
  ...
  public Interval[] split(int times) {
    if (times < 0) {
      new Console().writeln("El numero de veces debe ser positivo");
      return null;
    }
    Interval[] intervals = new Interval[times];
    final double length = this.length() / times;
    final double min = this.min;
    final double max = min + length;
    for (int i = 0; i < times; i++) {
      intervals[i] = new Interval(min, max);
      min = max;
      max += length;
    }
    return intervals;
  }
}
```
* si se trata de una aplicación, la solución NO es que el método compruebe la corrección de su argumento y que, en el caso de que no sea correcto, devuelva una valor que indique que hay un error:
```java
class Interval {
  ...
  public Interval[] split(int times) {
    if (times < 0) {
      return null;
    }
    Interval[] intervals = new Interval[times];
    final double length = this.length() / times;
    final double min = this.min;
    final double max = min + length;
    for (int i = 0; i < times; i++) {
      intervals[i] = new Interval(min, max);
      min = max;
      max += length;
    }
    return intervals;
  }
}
```
**<font color="darkred"> Falta de cohesión</font>**
```java
class App {

  public static void main(String[] args){
    Console console = new Console();
    Interval interval = new Interval();
    interval.read();
    Interval[] intervals;
    do {
      int times = console.readInt("¿Partir en cuántas veces? ");
      intervalos = intervalo.troceado(veces);
    } while (intervalos != null);
  }
}
```
**<font color="darkgreen">Validación de datos</font>**

- si se trata de una aplicación, la solución es que, al leer el argumento, se valide su corrección y que, en el caso de que no sea correcto, no se invoque al método y se comunique y requiera de nuevo al usuario:

```java 
class App {
 
  public static void main(String[] args){
    Console console = new Console();
    Interval interval = new Interval();
    int times;
    do {
      times = console.readInt("¿Partir en cuántas veces? ");
      if (times <= 0) {
         console.writeln("El numero de veces debe ser positivo");
      }
    } while (times <= 0);
    Interval[] intervals = interval.split(times);
  }
}
```

**Sentencia assert**


- Sintaxis

`assert` `<expresión1>` [ : `<expresión2>` ];

- Cada **aserción contiene una expresión lógica** (`<expresión1>`) que se supone cierta cuando se ejecute la sentencia

  - <font color="darkred">En caso contrario, el sistema finaliza la ejecución</font> del programa y avisa del defecto detectado

  - o    opcionalmente, se puede acompañar de una cadena de caracteres (`<expresión2>`) para detallar el error detectado <br><br>
  
-  La experiencia ha demostrado que escribir aserciones es una de las formas más rápidas y efectivas para detectar y corregir errores lógicos en desarrollo, Diseño por Contrato<br>

   - o si se desea comprobar en el método la corrección de su argumento, debe incluirse una aserción como **pre-condiciones**

   - <font color="darkgreen">o las aserciones permiten eliminar estas comprobaciones automáticamente en la ejecución del código de producción para evitar la finalización abrupta del programa en fase de explotación</font>




```java
class App {

  public static void main(String[] args){
    Console console = new Console();
    Interval interval = new Interval();
    int times;
    do {
      times = console.readInt("¿Partir en cuántas veces? ");
      if (times <= 0) {
         console.writeln("El numero de veces debe ser positivo");
      }
    } while (times <= 0);
    Interval[] intervals = interval.split(times);
  }
}
```

* <font color="darkred"> si se está desarrollando una biblioteca, entonces sí que deberemos responsabilizarnos de comprobar los argumentos que se reciben en los métodos, porque están fuera del ámbito de la biblioteca, junto con la consiguiente gestión de excepciones para comunicar de la situación al error:</font>

``` java
class Interval {
  ...
  public Interval[] split(int times) throws Exception {
    if (times < 0) {
      throw new Exception("El numero de veces no es positivo")
    }

    Interval[] intervals = new Interval[times];
    final double length = this.length() / times;
    final double min = this.min;
    final double max = min + length;
    for (int i = 0; i < times; i++) {
      intervals[i] = new Interval(min, max);
      min = max;
      max += length;
    }
    return intervals;
  }
} 
```
<br>

``` java
class App {

  public static void main(String[] args){
    Console console = new Console();
    Interval interval = new Interval();
    int times;
    ...
    try {
      Interval[] intervals = interval.split(times);
      ...
    } catch (Exception ex){
      // gestión de error
    }
  }
}
```

 **Aplicaciones** 

* Fraction - [*Fraction*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a3_asserts/Fraction.java) - [*App*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a3_asserts/App.java)

---

[Anterior](../u5privateMethods/README.md) | [Subir nivel](../README.md) | [Siguiente](../u7valueObjects/README.md)
