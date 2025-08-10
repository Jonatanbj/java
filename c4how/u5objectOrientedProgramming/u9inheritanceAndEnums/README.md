# Herencia y Enumerados






| *Sin enumerados* | *Con enumerados* |
| --- | --- |
| 


```
package es.usantatecla.a0\_itinerario.a4\_orientadoObjetos.a6\_enums.a1\_inherits;

abstract class Enum {
    public static Enum OBJECT_1 = new Object_1("OBJECT\_1");
    public static Enum OBJECT_2 = new Object_2("OBJECT\_2");
    public static Enum OBJECT_3 = new Object_3("OBJECT\_3");

    public static Enum[] values() {
        return new Enum[] { Enum.OBJECT_1, Enum.OBJECT_2, Enum.OBJECT_3 };
    }

    private String name;

    protected Enum(String name) {
        this.name = name;
    }

    public String name() {
        return this.name;
    }

    public void transmitedMethod() {
        Console.instance().writeln("General");
    }

    public abstract void redefinedMethod();

    public static void main(String[] args) {
        for (Enum current : Enum.values()) {
            current.transmitedMethod();
            current.redefinedMethod();
            // if (current == Enum.OBJECT\_3){
            // current.addedMethod();
            // }
        }
        // Enum.OBJECT\_3.addedMethod();
    }
}

class Object\_1 extends Enum {

    protected Object_1(String name) {
        super(name);
    }

    public void redefinedMethod() {
        Console.instance().writeln(this.name());
    }
}

class Object\_2 extends Enum {

    protected Object_2(String name) {
        super(name);
    }

    public void redefinedMethod() {
        Console.instance().writeln(this.name());
    }

    public void transmitedMethod() {
        Console.instance().writeln("Particular");
    }
}

class Object\_3 extends Enum {

    protected Object_3(String name) {
        super(name);
    }

    public void redefinedMethod() {
        Console.instance().writeln(this.name());
    }

    public void addedMethod() {
        Console.instance().writeln("addedMethod");
    }

}
```


 | 


```
package es.usantatecla.a0\_itinerario.a4\_orientadoObjetos.a6\_enums.a2\_enums;

enum Enum {
    OBJECT_1 {
        public void redefinedMethod() {
            Console.instance().writeln(OBJECT_1.name());
        }

    },
    OBJECT_2 {
        public void redefinedMethod() {
            Console.instance().writeln(OBJECT_2.name());
        }

        public void transmitedMethod() {
            Console.instance().writeln("Particular");
        }
    },
    OBJECT_3 {
        public void redefinedMethod() {
            Console.instance().writeln(OBJECT_3.name());
            this.addedMethod();
        }

        public void addedMethod() {
            Console.instance().writeln("addedMethod");
        }
    };

    public void transmitedMethod() {
        Console.instance().writeln("General");
    }

    public abstract void redefinedMethod();

    public static void main(String[] args){
        for(Enum current : Enum.values()){
            current.transmitedMethod();
            current.redefinedMethod();
            // if (current == Enum.OBJECT\_3){
            // current.addedMethod();
            // }
        }
        // Enum.OBJECT\_3.addedMethod();
    }
}
```


 |








| **Aplicaciones** |
| --- |
| 
* Language - [*sin herencia*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a3_date/a3_enums/Language.java) - [con herencia](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a3_date/a4_inherits/Language.java)


 | 
* Month - [*sin herencia*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a3_date/a4_inherits/Month.java) - [con herencia](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a3_date/a3_enums/Month.java)


 |  |


---

[Volver al nivel superior](../README.md)



[Anterior](../u7polymorphism/README.md) | [Subir nivel](../README.md) | [Siguiente](../README.md)
