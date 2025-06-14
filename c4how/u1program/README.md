# Programa


| | |
|---|---|
| • Un **programa** se compone de **paquetes** que se componen de otros paquetes y **clases**, bajo el **paradigma de la programación modular**<br>&nbsp;&nbsp;&nbsp;&nbsp;• cada clase reúne **atributos** presentes en todas sus instancias, que pueden ser de **tipo primitivo** o de alguna clase junto con sus **métodos**<br>&nbsp;&nbsp;&nbsp;&nbsp;• cada método reúne parámetros y un conjunto de sentencias:<br>&nbsp;&nbsp;&nbsp;&nbsp;• crear dato, **sentencias de declaración de variables/constantes**<br>&nbsp;&nbsp;&nbsp;&nbsp;• modificar datos, **sentencias de asignación**, **entrada** y **salida**<br>&nbsp;&nbsp;&nbsp;&nbsp;• eliminar datos, asociados a los **ámbitos** de los métodos<br>&nbsp;&nbsp;&nbsp;&nbsp;• consultar datos, mediante **referencias** desde las **expresiones**<br><br>• Las sentencias contienen **expresiones** que pueden ser<br>&nbsp;&nbsp;&nbsp;&nbsp;• **expresiones simples** mediante la **mención** de los datos o **literales**<br>&nbsp;&nbsp;&nbsp;&nbsp;• **expresiones compuestas** mediante la combinación de **operadores** | ![como](images/como.svg) |
| • Las sentencias pueden ser **compuestas**, bajo el **paradigma de la programación estructurada**<br>&nbsp;&nbsp;&nbsp;&nbsp;• **sentencia secuencial**, para la creación de ámbitos anidados en el ámbito del progrma,<br>&nbsp;&nbsp;&nbsp;&nbsp;• **sentencia alternativa**, para alternar la ejecución de sentencias,<br>&nbsp;&nbsp;&nbsp;&nbsp;• **sentencia iterativa**, para repetir la ejecución de sentencias.<br>&nbsp;&nbsp;&nbsp;&nbsp;• **sentencias con excepciones**, para elevar, capturalas y delegarlas. | • Los datos, **constantes** o **variables**, pueden ser de **tipo**<br>&nbsp;&nbsp;&nbsp;&nbsp;• **primitivo**, para átomos de información sin propiedades e inmutables<br>&nbsp;&nbsp;&nbsp;&nbsp;• **array**, para colecciones compuestas de datos homogéneas<br>&nbsp;&nbsp;&nbsp;&nbsp;• **objetos**, para colecciones compuestas de datos heterogéneas bajo el **paradigma de la programación orientada a objetos** |



| **Programa** | ***java*** |
|---|---|
| • **Sintaxis**:<br>&nbsp;&nbsp;&nbsp;&nbsp;• *\<sentencia\>* **::=** *\<sentenciaSalida\>*<br>&nbsp;&nbsp;&nbsp;&nbsp;• *\<sentenciaSalida\>* **::=** **console.writeln^** **([<expresion\> ])** **;**<br>&nbsp;&nbsp;&nbsp;&nbsp;• *\<expresion\>* **::=** *\<literal\>*<br>&nbsp;&nbsp;&nbsp;&nbsp;• *\<literal\>* **::=** *\<cadenaCaracteres\>*<br><br>• **Semántica**:<br>&nbsp;&nbsp;&nbsp;&nbsp;• Se ejecutan secuencialmente de arriba a abajo todas las sentencias<br><br>• ***Advertencia***:<br>&nbsp;&nbsp;&nbsp;&nbsp;• *Las ocho primeras líneas y dos últimas se explilcarán en los sucesivos apartados de este documento!!!*<br>&nbsp;&nbsp;&nbsp;&nbsp;• *Todos los códigos deben ir acompañandos en carpeta "utils" el fichero:* [utils/Console.java](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/utils/Console.java) | ```package es.usantatecla.a0_itinerario.a0_programa.v0;

class App {
    
    public static void main(String[] args) {
        Console console = new Console();
        console.writeln("Hola Mundo !!!");
        console.writeln();
        console.writeln("Adios Mundo !!!");
    }
}```

## **Comentarios** | ***java***

| **Comentarios** | ***java*** |
|---|---|
| • **Sintaxis**:<br>&nbsp;&nbsp;&nbsp;&nbsp;• *\<comnetario\>* **::=** **//** *\<caracter\>* **\*** *\<saltoLinea\>*<br>&nbsp;&nbsp;&nbsp;&nbsp;• *\<comnetario\>* **::=** **/\*** *\<caracter\>* **\*** **\*/**<br>&nbsp;&nbsp;&nbsp;&nbsp;• Válidos entre la secuencia de valores, operadores, identificadores, …​ **nunca dentro de éstos!!!**<br>&nbsp;&nbsp;&nbsp;&nbsp;• **Invalidos si anidan dentro de comentarios del mismo o distinto tipo**<br><br>• **Semántica**:<br>&nbsp;&nbsp;&nbsp;&nbsp;• No se ejecutan los caracteres internos al comentraio<br>&nbsp;&nbsp;&nbsp;&nbsp;• **No recomendados**, *clean code* | ```java<br>package es.usantatecla.a0_itinerario.a0_programa.v1;<br><br>class App {<br><br>  public static void main(String[] args) {<br>    Console console = new Console();<br>    console.writeln(/* aquí es raro, raro, ...*/"Hola Mundo !!!");<br>    // gestorIO.writeln(); Dead Code!!!<br>    // típico comentario innecesario<br>    console.writeln("Adios Mundo !!!");<br>  }<br>}<br>``` |

---

[Volver al nivel superior](../README.md)

[Siguiente sección: Programación Imperativa](../u2imperativeProgramming/README.md)
