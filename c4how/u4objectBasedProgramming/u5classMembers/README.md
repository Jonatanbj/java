# [Miembros de Clase](../u5classMenbers/README.md)


| <span style="color:darkgreen"> Miembros de instancia </span> | <span style="color:darkred"> Miembros de clase o estáticos </span> |
| --- | --- |
| Los miembros de instancia asumen los **aspectos, datos y operaciones particulares/locales de/a cada objeto de la clase**. | Los miembros de clase o estáticos asumen los **aspectos, datos y operaciones compartidos/globales por/a la comunidad de objetos de la clase**. |
| **Atributos de instancia** presentes en cada uno de los objetos de la clase: <br> &nbsp;&nbsp;&nbsp;&nbsp;- Ejemplo: *día, mes y año de una fecha concreta*. <br> &nbsp;&nbsp;&nbsp;&nbsp;- Si no hay objetos, no hay atributos de instancia. | **Atributos de clase** compartidos por la globalidad de objetos de la clase: <br> &nbsp;&nbsp;&nbsp;&nbsp;- Ejemplo: *los nombres y duración de los meses de cualquier fecha, excepto en Febrero de años bisiestos*. <br> &nbsp;&nbsp;&nbsp;&nbsp;- Si no hay objetos, **sí** hay atributos de clase. |
| **Métodos de instancia** cuyos mensajes se lanzan sobre un objeto particular de la clase: <br> &nbsp;&nbsp;&nbsp;&nbsp;- Ejemplo: *si es primavera, si una fecha concreta se encuentra en un año bisiesto*. <br> &nbsp;&nbsp;&nbsp;&nbsp;- Si no hay objetos, no hay mensajes. | **Métodos de clase** cuyos mensajes **NO** se lanzan sobre un objeto particular: <br> &nbsp;&nbsp;&nbsp;&nbsp;- Ejemplo: *si un año (de cualquier fecha, no de una fecha particular) es bisiesto*. <br> &nbsp;&nbsp;&nbsp;&nbsp;- Si no hay objetos, **sí** se llama a métodos de clase, **no mensajes**. |

<br>

**Atributos y Métodos Estáticos:** caracterizados por la palabra reservada **static** tras su visibilidad;
<br>
|Atributos estáticos | Métodos estáticos |
| --- | --- |
|- su reserva de memoria e inicialización obligatoria se realiza al principio de la ejecución del programa,<br> &nbsp;&nbsp;&nbsp;&nbsp;  - o en orden dentro de las declaraciones de la clase pero<br> &nbsp;&nbsp;&nbsp;&nbsp; - o en desorden entre las distintas clases <br> - accesibles desde cualquier método, de instancia o estático, de la clase;<br> - la notación sintáctica para el acceso desde las expresiones: <br><br>`<Clase>`.`<atributosEstático>` |- se permite el acceso a los atributos estáticos;<br>- no se permite el acceso a this<br>- la notación sintáctica para la invocación/llamada/ejecución del método estático como sentencia de los métodos:<br>`<Clase>.<metodoEstatico>`([`<argumento>` { `<argumento>`, }])  | 

 **Aplicaciones** 

* [*Interval*](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/a5_units/a1_interval/a2_statics)

* [*Date*](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/a5_units/a3_date/a2_statics)


****Código estático****

- sirve para la inicialización de los atributos estáticos cuando la expresión de inicialización no alcanza sus objetivos y requiere la ejecución de sentencias

- se ejecutan al comienzo de la ejecución del programa, secuencialmente dentro de cada fichero y en cualquier orden entre distintos ficheros

**Sintaxis:**
```java
<atributoEstático>
static {
  <sentencia/declaración>
  …
  <sentencia/declaración>
}
```
**Ejemplo:**

```java
private static int[] coeficientes = null;
static {
  // lectura del fichero “coeficientes.sys”
}
```

---

**Método ***main*****

**Sintaxis:**
```java
public static void main(String[] args) {
  ...
}
```

> ⚠️ **Importante:** método del que parte la ejecución, presente en las clases "principales"


**Ejecución:**
```bash
c:\>java Clase param1 param2
```

En este caso, `args[0].equals("param1") && args[1].equals("param2")`.


**Ejemplo:**
```java
package es.usantatecla.a0_itinerario.a3_basadaObjetos.a4_main;

class Clazz {

    private void exec(String[] args) {
        // Implementación
    }

    public static void main(String[] args) {
        new Clazz().exec(args);
    }
}

class App {
    
    public static void main(String[] args) {
        Console.instance().write("Eco!!!\njava App ");
        for (String current : args) {
            Console.instance().writeln(current);
        }
        Console.instance().writeln();
    }
}
```

---

****Clases de Utilidad****

- son clases que reúnen un conjunto cohesivo de métodos estáticos, …​ cajón de-sastre dentro de la librería o proyecto

  - o    Suelen no ser instanciables porque no responden al concepto habitual de clases de objetos

    - se consigue a través constructores privados que eviten la creación de objetos de esa clase de utilidad

**Ejemplo:** Clase [System](https://docs.oracle.com/javase/7/docs/api/java/lang/System.html)
```java
public static void gc(); //(1º) Invoca el recolector de basura
public static void exit(int); //(2º) Salida incondicional del programa
public static long nanoTime();
public static long currentTimeMillis();
```
`1º:` garbage collector, invoca el recolector de basura que libera la memoria de todo objeto no referenciado; se llama automáticamente cuando el procesador está ocioso por interrupción de entrada/salida, …​ 
`2º:` invoca la salida incondicional del programa comunicando un código de error


**Ejemplo:** Clase [Math](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html)
```java
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
- **Clase StrictMathMath:** con la misma interfaz pública y una implementación independiente de la máquina, sin cálculos nativos, <span style="color:darkred">menos eficiente</span> que `Math`, la cual <span style="color:darkred">es menos portable</span>

---

[Anterior](../u4privateViewOfObjects/README.md) | [Subir nivel](../README.md) | [Siguiente](../u6wrapperClasses/README.md)
