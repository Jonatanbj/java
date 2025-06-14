# Métodos privados






| 
* Sirve para la **reutilización de métodos en la codificación de otros métodos**


	+ dado que puede ser conveniente disponer de métodos, que **no han sido solicitados, para implementar otros métodos**, cabe la posibilidad de definir métodos de ámbito privado que sólo se pueden usar en la implementación de la clase:







```
class <class> {
   private <methodHeader> <sequentialSentence>
   private <methodHeader> <sequentialSentence>
   ...
}
```


 | 


```
public Interval shifted(double amount) {
   Interval interval = this.clone();
   interval.shift(amount);
   return interval;
}

private Interval clone() {
  return new Interval(this);
}
```


 |







| *Resumen de Implantación de Clases* |
| --- |
| 


```
package es.usantatecla.a0\_itinerario.a3\_basadaObjetos.a1\_clazz;

class Clazz {

    public int publicAtributte; // Desaconsejado
    private int privateAtributte;

    public Clazz(int value) {
        this.publicAtributte = 2;
        this.privateAtributte = value;
    }

    private Clazz() {
        this(3);
        // ...
    }

    public void publicInstnaceMethod() {
        Console console = new Console();
        console.writeln();
        console.writeln("publicInstnaceMethod : publicAtributte: " + this.publicAtributte);
        console.writeln("publicInstnaceMethod : privateAtributte: " + this.privateAtributte);
        this.privateInstanceMethod();
    }

    private void privateInstanceMethod() {
        Console console = new Console();
        console.writeln();
        console.writeln("privateInstnaceMethod : publicAtributte: " + this.publicAtributte);
        console.writeln("privateInstnaceMethod : privateAtributte: " + this.privateAtributte);
    }

}

class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln();
        Clazz object = new Clazz(0);
        console.writeln("main.publicAtributte: " + object.publicAtributte);
        // console.writeln("main.privateAtributte: " + object.privateAtributte);
        object.publicInstnaceMethod();
        // object.privateInstnaceMethod();
    }
}
```


 | 


```
package es.usantatecla.a0\_itinerario.a3\_basadaObjetos.a1\_method;

class X {
}

class Clazz {

    private int primitive;
    private int[] primitiveArray;
    private X object;
    private X[] objectArray;

    public void methodWithoutArguments() {
        // sentences
    }

    public void methodWitArguments(int primitive, int[] primitiveArray, X object, X[] objectArray) {
        // sentences
    }

    public void methodWitArguments(int primitive, int[] primitiveArray, X object) {
        // sentences
    }

    public void methodWitArguments(int[] primitiveArray, X object, X[] objectArray, int primitive) {
        // sentences
    }

    public int methodReturPrimitive() {
        // sentences
        return 0;
    }

    public int[] methodReturPrimitiveArray() {
        // sentences
        return new int[] {};
    }

    public X methodReturObject() {
        // sentences
        return new X();
    }

    public X[] methodReturObjectArray() {
        // sentences
        return new X[] {};
    }

}

class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln();
        Clazz object = new Clazz();
        object.methodWithoutArguments();
        object.methodWitArguments(0, new int[] {}, new X(), new X[] {});
        object.methodWitArguments(0, new int[] {}, new X());
        object.methodWitArguments(new int[] {}, new X(), new X[] {}, 0);
        X x = object.methodReturObject();
        X[] xs = object.methodReturObjectArray();
        int primitive = object.methodReturPrimitive();
        int[] primitiveArray = object.methodReturPrimitiveArray();
    }
}
```


 |








| **Aplicaciones** |
| --- |
| 
* Fraction - [*Fraction*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a1_classes/Fraction.java) - [*App*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a0_fraction/a1_classes/App.java)


 |  |  |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Aserciones](../u6assertions/README.md)
