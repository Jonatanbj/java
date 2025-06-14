# Aserciones







| 
* **Error** es una acción que produce un resultado incorrecto


 | 
* **Defecto** es la imperfección de un componente causado por un error


 | 
* **Fallo** es la manifestación visible de un defecto


 |
| 
* *Ej. un conductor analiza mal el contexto de la circulación*
* *Ej. un programador escribe mal una sentencia, incumpliendo reglas léxico/ sintáctico/ semánticas*
* *Ej. un programador diseña mal un algoritmo, produciendo un bucle infinito*


 | 
* *Ej. un conductor establece una velocidad, giro, …​ inadecuados*
* *Ej. un programa produce una incompatibilidad de tipos entre un operador y un operando*
* *Ej. un programa con una condición en una sentencia iterativa infinita*


 | 
* *Ej. se produce un accidente*
* *Ej. el programa no compila*
* *Ej. el programa no responde*


 |








| **Tipos de Errores** |
| --- |
| 
* ***Errores en Tiempo de Compilación*** producidos por el incumplimiento de las


	+ reglas léxicas,
	+ reglas sintácticas y/o
	+ reglas semánticas del lenguaje fuerte o débilmente tipado;



 | 
* **Errores en Tiempo de Ejecución**


 |
| 
* **Errores Lógicos** producidos por la lógica de un programa que no contempla todos los posibles situaciónes del sistema de información


	+ Se **gestionan con sentencias *assert*** para las pre-condiciones
	+ Se **gestionan con pruebas del software** para las post-condiciones



 | 
* **Errores Excepcionales** producidos por recursos (bibliotecas / *frameworks* para gestión de ficheros, comunicaciones, …​, arquitectura) fuera del ámbito del software que los maneja.


	+ Se **gestionan con objetos de la clase *Exception* y la sentencia *try/catch/finally***



 |








| **Contexto** | **Aplicación** | **Biblioteca** |
| --- | --- | --- |
| 
* ciertos errores lógicos (ej.: un valor negativo para calcular un factorial, una referencia sin la dirección del objeto, …​) pueden ser un error lógico o excepcional **dependiendo del software en el que se está desarrollando**:


 | 
* **debe responsabilizarse de la detección y subsanación de los errores lógicos dentro de su ámbito** durante el desarrollo.


	+ los **errores en la entrada de datos del usuario** **no son errores del desarrollo** y se solventan mediante la **validación de la entrada de datos, sentencia iterativa hasta alcanzar la condición deseada**



 | 
* **NO puede responsabilizarse del uso indebido de los servicios prestados a las aplicaciones y NUNCA debe responsabilizarse de la subsanación de dichos errores**.


	+ En estos casos, estos **errores lógicos se considerarán excepcionales** porque la causa del error está **fuera de los límites del software** de la biblioteca.



 |
| 
*Ej. la función factorial contemplará:*
 |
| 
* *pre-condiciones para verificar si la entrada es correcta (el argumento no es negativo) mediante*


 |
| 
* *la sentencia assert en el código de producción*


 | 
* *la elevación de una excepción en el código de producción*


 |
| 
* *post-condiciones para verificar si la salida es correcta (n! = 1 si n = 0 si no n * (n-1)!) mediante la librería aseertThat en el código de pruebas*


 |







| 


```
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


 | 
* *cuando se solicita el número de veces, si el usuario introduce un valor negativo, se produce un error de ejecución, se muestra por pantalla un informe del error producido (reserva de un vector cuyo tamaño es negativo), y finaliza la ejecución del programa*






```
Introduce el minimo: 1
Introduce el maximo: 5
Veces: -1
Exception in thread "main" java.lang.NegativeArraySizeException
        at Intervalo.valores (Intervalo.java:141)
        at Aplicacion.main (Aplicacion.java:7)
```


 |







| **Programación defensiva** |
| --- |
| 
* *si se trata de una aplicación, la solución NO es que el método compruebe la corrección de su argumento y que, en el **caso de que no sea correcto, gestione el error acoplándose con un mensaje a la consola, …​***:


 | 


```
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


 |
| 
* *si se trata de una aplicación, la solución NO es que el método compruebe la corrección de su argumento y que, en el **caso de que no sea correcto, devuelva una valor que indique que hay un error***:


 | 


```
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


 |








| **Falta de cohesión** | **Validación de datos** |
| --- | --- |
| 


```
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


 | 
* *si se trata de una aplicación, la solución es que, al leer el argumento, se **valide** su corrección y que, en el caso de que no sea correcto, **no se invoque al método** y se comunique y requiera de nuevo al usuario*:


 | 


```
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


 |







| **Sentencia *assert*** | *Ejemplo* |
| --- | --- |
| 
* **Sintaxis**






```
  assert <expresión1> [ : <expresión2> ] ;
```




* Cada **aserción contiene una expresión lógica** (<expresión1>) que se **supone cierta** cuando se ejecute la sentencia


	+ **en caso contrario, el sistema finaliza la ejecución** del programa y avisa del defecto detectado
	+ opcionalmente, se puede acompañar de una cadena de caracteres (<expresión2>) para detallar el error detectado

* La experiencia ha demostrado que escribir aserciones es una de las formas más rápidas y efectivas para detectar y corregir errores lógicos en desarrollo, **Diseño por Contrato**


	+ si se desea comprobar en el método la corrección de su argumento, debe incluirse una aserción como **pre-condiciones**
	+ las aserciones permiten eliminar estas comprobaciones automáticamente en la ejecución del código de producción para evitar la finalización abrupta del programa en fase de explotación



 | 


```
class Interval {
  ...
  public Interval[] split(int times) {
    assert times > 0 : "El numero de veces no es positivo";

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


 |








| 
* *si se está desarrollando una biblioteca, entonces sí que deberemos responsabilizarnos de comprobar los argumentos que se reciben en los métodos, porque están fuera del ámbito de la biblioteca, junto con la consiguiente gestión de excepciones para comunicar de la situación al error*:


 | 


```
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


 | 


```
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


 |








| **Aplicaciones** |
| --- |
| 
* Fraction - [*Fraction*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a3_asserts/Fraction.java) - [*App*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a3_asserts/App.java)


 |  |  |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Objetos Valor](../u7valueObjects/README.md)
