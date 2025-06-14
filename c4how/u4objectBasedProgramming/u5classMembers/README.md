# Miembros de Clase






| **Miembros de instancia** | **Miembros de clase o estáticos** |
| --- | --- |
| 
* Los miembros de instancia asumen los **aspectos, datos y operaciones, particulares/locales de/a cada objeto de la clase**


 | 
* Los miembros de clase o estáticos asumen los **aspectos, datos y operaciones, compartidos/globales por/a la comunidad de objetos de la clase**


 |
| 
* **atributos de instancia** presentes en cada uno de los objetos de la clase;


	+ Ej. *día, mes y año de una fecha concreta*
	+ si no hay objetos, no hay atributos de instancia;



 | 
* **atributos de clase** compartidos por la globalidad de objetos de la clase;


	+ Ej. *los nombres y duración de los meses de cualquier fecha, excepto en Febrero de años bisiestos, …​*
	+ si no hay objetos, **si** hay atributos de clase;



 |
| 
* **métodos de instancia** cuyos mensajes se lanzan sobre un objeto particular de la clase;


	+ Ej. *si es primavera, si una fecha concreta se encuentra en una año bisiesto, …​*
	+ si no hay objetos, no hay mensajes;



 | 
* **métodos de clase** cuyos mensajes NO se lanzan sobre un objetos particular;


	+ Ej. *si un año (de cualquier fecha, no de una fecha particular) es bisiesto*
	+ si no hay objetos, **si** se llama a métodos de clase, **no mensaje!!!**;



 |







| **Atributos estáticos** | **Métodos estáticos** |
| --- | --- |
| 
* caracterizados por la palabra reservada **static** tras su visibilidad;


 |
| 
* su **reserva de memoria e inicialización obligatoria** se realiza al principio de la ejecución del programa,


	+ en orden dentro de las declaraciones de la clase pero
	+ en desorden entre las distintas clases

* accesibles desde cualquier método, de instancia o estático, de la clase;
* la notación sintáctica para el acceso desde las expresiones:






```
    <Clase>.<atributosEstático>
```


 | 
* se permite el acceso a los atributos estáticos;
* **no se permite el acceso a *this* ni a los atributos de instancia**;
* la notación sintáctica para la invocación/llamada/ejecución del método estático como sentencia de los métodos:






```
  <Clase>.<metodoEstatico>([<argumento> { <argumento>, }])
```


 |








| **Aplicaciones** |
| --- |
| 
* [*Interval*](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/a5_units/a1_interval/a2_statics)


 | 
* [*Date*](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/a5_units/a3_date/a2_statics)


 |  |








| **Código estático** | **Sintaxis** | *Ejemplo* |
| --- | --- | --- |
| 
* sirve para la inicialización de los atributos estáticos cuando la expresión de inicialización no alcanza sus objetivos y requiere la ejecución de sentencias
* se ejecutan al comienzo de la ejecución del programa, secuencialmente dentro de cada fichero y en cualquier orden entre distintos ficheros


 | 


```
<atributoEstático>
static {
  <sentencia/declaración>
  …
  <sentencia/declaración>
}
```


 | 


```
private static int[] coeficientes = null;
static {
  // lectura del fichero “coeficientes.sys”
}
```


 |







| **Método *main*** | *Ejemplo* |
| --- | --- |
| 
* **Sintaxis**






```
public static void main(String[] args) { **(1)**
  ...
}
```






|  |  |
| --- | --- |
| **1** | método del que parte la ejecución, presente en las clases "principales" |


 | 


```
package es.usantatecla.a0\_itinerario.a3\_basadaObjetos.a4\_main;

class Clazz {

    private void exec(String[] args){

    }

    public static void main(String[] args){
        new Clazz().exec(args);
    }
}

class App {
    
    public static void main(String[] args){
        Console.instance().write("Eco!!!\njava App ");
        for(String current : args){
            Console.instance().writeln(current);
        }
        Console.instance().writeln();
    }
    
}
```


 |
| 
* **Ejecución**






```
c:\>java Clase param1 param2 **(1)**
```






|  |  |
| --- | --- |
| **1** | *args[0].equals("param1") && args[1].equals("param2")* |


 |







| **Clases de Utilidad** | *Clase* [*System*](https://docs.oracle.com/javase/7/docs/api/java/lang/System.html) |
| --- | --- |
| 
* son clases que reúnen un **conjunto cohesivo de métodos estáticos**, …​ cajón de-sastre dentro de la **librería o proyecto**


	+ **Suelen no ser instanciables** porque no responden al concepto habitual de clases de objetos
	
	
		- se consigue a través **constructores privados** que eviten la creación de objetos de esa clase de utilidad



 | 


```
public static void gc() {}**(1)**
public static void exit(int) {}**(2)**
public static long nanoTime() {}
public static long currentTimeMillis() {}
```






|  |  |
| --- | --- |
| **1** | *garbage collector*, invoca el recolector de basura que libera la memoria de todo objeto no referenciado; se llama automáticamente cuando el procesador está ocioso por interrupción de entrada/salida, …​ |
| **2** | invoca la salida incondicional del programa comunicando un código de error |


 |







| *Clase* [*Math*](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html) |
| --- |
| 


```
public static final double E;
public static final double PI;
public static double sin(double)
public static double cos(double)
public static double tan(double)
public static double asin(double)
public static double acos(double)
public static double atan(double)
public static double toRadians(double)
public static double toDegrees(double)
public static double exp(double)
public static double log(double)
public static double log10(double)
public static double sqrt(double)
public static double cbrt(double)
public static double IEEEremainder(double, double)
public static double ceil(double)
public static double floor(double)
public static double rint(double)
public static double atan2(double,double)
public static double pow(double,double)
public static int round(float)
public static long round(double)
public static double random()
public static int abs(int)
public static long abs(long)
public static float abs(float)
public static double abs(double)
public static int max(int, int)
public static long max(long, long)
...
```


 | 


```
public static float max(float, float)
public static double max(double,double)
public static int min(int, int)
public static long min(long, long)
public static float min(float, float)
public static double min(double,double)
public static double ulp(double)
public static float ulp(float)
public static double signum(double)
public static float signum(float)
public static double sinh(double)
public static double cosh(double)
public static double tanh(double)
public static double hypot(double,double)
public static double expm1(double)
public static double log1p(double)
public static double copySign(double,double)
public static float copySign(float, float)
public static int getExponent(float)
public static int getExponent(double)
public static double nextAfter(double,double)
public static float nextAfter(float,double)
public static double nextUp(double)
public static float nextUp(float)
public static double scalb(double, int)
public static float scalb(float, int)
...
```




* *Clase* [*StrictMathMath*](https://docs.oracle.com/javase/8/docs/api/java/lang/StrictMath.html): con la misma interfaz pública y una implementación independiente de la máquina, sin cálculos nativos, menos eficiente que *Math*, la cual es menos portable


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Clases de Recubrimiento](../u6wrapperClasses/README.md)
