# [Paquetes y Herencia](README.md)


* Un **método se puede redefinir en una clase derivada sólo si dicho método de la clase base es accesible desde la clase derivada**
	+ **Si el método no es accesible, el método de la clase derivada no redefine el método de la clase base, incluso aunque tenga la misma cabecera**

*Ejemplo:*

```java
package package1;

public class BaseClass {

  public void writeln() {
    this.privateMehtod();
    this.packageMethod();
    this.protectedMethod();
    this.publicMethod();
  }

  private void privateMehtod() {
    Console.getInstance().writeln( "privateMehtod of BaseClass");
  }

  void packageMethod() {
    Console.getInstance().writeln( "packageMethod of BaseClass");
  }

  protected void protectedMethod() {
    Console.getInstance().writeln( "protectedMethod of BaseClass");
  }

  public void publicMethod() {
    Console.getInstance().writeln( "publicMethod of BaseClass");
  }
```

```java
package app;

import package1.DerivatedClass;

class App {

  public static void main(String[] args) {
    new DerivatedClass().writeln();
  }
}
```

<br>

* Cuando se **invoca un método, el sistema tiene que considerar en tiempo de ejecución la accesibilidad de dicho método para decidir qué implementación del método se debe invocar**

*Ejemplo:* 


```java
package package2;

import package1.BaseClass;

public class DerivatedClass extends BaseClass {

    private void privateMehtod() {
    Console.getInstance().writeln( "privateMehtod of DerivatedClass");
  }

  void packageMethod() {
    Console.getInstance().writeln( "packageMethod of DerivatedClass");
  }

  protected void protectedMethod() {
    Console.getInstance().writeln( "protectedMethod of DerivatedClass");
  }

  public void publicMethod() {
    Console.getInstance().writeln( "publicMethod of DerivatedClass");
  }

}
```

```java
package app;

import package1.DerivatedClass;

class App {

  public static void main(String[] args) {
    new DerivatedClass().writeln();
  }
}
```
 | 
* al ejecutar su método principal, se produciría la siguiente salida por pantalla:


```java
privateMehtod of BaseClass
packageMethod of BaseClass
protectedMethod of DerivatedClass
publicMethod of DerivatedClass
```

| Aplicaciones |  |
| --- |--- |
| - Menús - [whitoutPackages](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_menu/a4_extends/a4_modelDynamicMenu) - [withPackages](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_menu/a5_package) | -  [TicTacToe](https://github.com/USantaTecla-0-domains/game-ticTacToe/tree/master/1.0.basic) - [Models](https://github.com/USantaTecla-tech-java/game-ticTacToe/tree/master/domainModel/basic/src/main/java/usantatecla) - [ModelsViews](https://github.com/USantaTecla-tech-java/game-ticTacToe/tree/master/documentView/basic/src/main/java/usantatecla)



---

[Anterior](../u4memberVisibility/README.md) | [Subir nivel](../README.md) | [Siguiente](../u6j2seApi/README.md)
