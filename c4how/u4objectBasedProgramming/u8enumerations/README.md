# Enumerados





| **Enumerados** | **Ejemplos** |
| --- | --- |
| - Son **clases** que limitan la creación de objetos a los enumerados explícitamente en la implementación de la clase. , <br> &nbsp;&nbsp;&nbsp;&nbsp; - La **única limitación** respecto a la implantación de una clase normal es que, si incorporan **constructores, deben ser privados** para evitar la creación de nuevos objetos distintos a los ofertados por la implementación. <br> &nbsp;&nbsp;&nbsp;&nbsp;  - Cada `<enumeradoX>` es implícitamente una referencia a un objeto de la clase con modificadores **public static final**. <br> &nbsp;&nbsp;&nbsp;&nbsp;  - La **sentencia `switch` acepta expresiones de clase enumerado** y, en tal caso, las posibles constantes de cada cláusula `case` serán las referencias a los objetos especificados en el enumerado.| - El enumerado/clase `Planeta` responsable de su posición, velocidad, etc., con únicamente 8 objetos mutables con atributos y métodos. <br>- El enumerado/clase `Mes` responsable de su número máximo de días (28, 30 o 31) y los literales en varios idiomas (“Enero”, “January”), con únicamente 12 objetos inmutables con atributos y métodos. <br>- El enumerado/clase `Color` responsable de nada, con únicamente 2 objetos inmutables (vacíos) sin atributos ni métodos.|


**Enumerado** 

```java
enum <Enumerado> {
  <enumerado1>[(<argumentos>)],
  ...
  <enumeradoN>[(<argumentos>)];

  <definiciónAtributos>

  private <Enumerado> ([<parametros>]) {
    ...
  }

  <definiciónMétodos>

  public void <metodo> () {
    ...
    switch(this){
      case <enumerado1>:
      case <enumerado2>:
      ...
        <sentencia>;
        break;
      default:
        <sentencia>;
    }
  }
}
```
**Clase con *static***  

```java
class <Enumerado> {
  public static final <Enumerado> <enumerado1> = new <Enumerado>([<argumentos>]);
  ...
  public static final <Enumerado> <enumeradoN> = new <Enumerado>([<argumentos>]);

  <definiciónAtributos>

  private <Enumerado> ([<parametros>]) {
    ...
  }

  <definiciónMétodos>

  public void <metodo> () {
    ...
    if(this == <enumerado1> || this== <enumerado2>) {
      <sentencia>;
    } else {
      <sentencia>;
    }
  }
}
```

**Métodos implícitos**  

* devuelve la **posición del enumerado** dentro de la secuencia expresada en la implementación
* devuelve el **identificador del enumerado**;
* devuelve un **vector de referencias con la dirección de todos los objetos enumerados**


	+ la **sentencia *for* acepta tablas de objetos enumerados en su formato iterador** como tablas de objetos de clases

**Sintaxis** 

```java
class <Enumerado> {
    public int ordinal()
    public String name()
    public static <Enumerado>[] values()
    ...
}

class App {
  public static void main(String[] args){
    Console console = new Console();
    for(<Enumerado> enum : <Enumerado>.values()) {
      console.writeln(
        "" + enum.ordinal() + ". " + enum.name());
    }
  }
}
```

| **Aplicaciones** |            |
| ---------------- |----------- |
| - [*Date*](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/a5_units/a3_date/a3_enums)| - [*TicTacToe*](https://github.com/USantaTecla-tech-java/game-ticTacToe/tree/master/domainModel/basic/src/main/java/usantatecla)| 

---


[Anterior](../u7stringsManipulation/README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u5objectOrientedProgramming/README.md)
