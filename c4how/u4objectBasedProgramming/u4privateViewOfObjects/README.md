# Vista Privada de los Objetos






| **Desencadenamiento de instanciaciones** | **Desencadenamiento de mensajes** |
| --- | --- |
| 
* se **crea un objeto** (instancia):


	+ por lo que, se crean los atributos definidos en la clase;
	+ por lo que, se ejecuta la inicialización de los atributos con posibles **creaciones de nuevos objetos**;
	+ por lo que, se ejecuta el constructor en la creación del objeto con posibles **creaciones de nuevos objetos**;
	+ Donde, **recursivamente**, pueden crear nuevos objetos de otras clases hasta llegar, de esta manera, a la creación de objetos que se basan directamente en tipos primitivos.



 | 
* se **lanza un mensaje** a un objeto:


	+ por lo que se crean las declaraciones locales con su inicialización y se ejecuta el cuerpo del método correspondiente
	+ por lo que se pueden **lanzar nuevos mensajes** a objetos que sean atributos de su clase, a objetos que sean argumentos del mensaje o a objetos que se crean en su ejecución
	+ Donde, **recursivamente**, pueden lanzar nuevos mensajes en la definición de sus respectivos métodos hasta llegar, de esta
	manera, a la definición de métodos que se basan directamente en tipos primitivos.



 |
| 


```
class Person {
  ...
  private MedicalRecord medicalRecord;
  private AcademicRecord academicRecord;
  ...

  public Person(...) {
    ...
    this.medicalRecord = new MedicalRecord();
    this.academicRecord = new AcademicRecord();
    ...
  }
}

class MedicalRecord {
  ...
}

class AcademicRecord {
  ...
}
```


 | 


```
class Person {
  ...

  public boolean isAdult() {
    return this.age > Person.ADULT;
  }

  public void writeln() {
    ...
    new Console.writeln("Age: " + this.age + (this.isAdult() ? " (adult)" : ""));
    this.medicalRecord.writeln();
    this.academicRecord.writeln();
  }

}
```


 |








| 
* el **desencadenamiento de instanciaciones puede provocar un desencadenamiento de mensajes** a través de la ejecución de los constructores que pueden lanzar mensajes;


 | 


```
public Intervalo(Intervalo intervalo) {
  this(intervalo.minimo, intervalo.maximo);
}

private Intervalo copia() {
  return new Intervalo(this);
}
```


 | 
* el **desencadenamiento de mensajes puede provocar un desencadenamiento de instanciaciones** a través de la creación de objetos en la definición de los métodos.


 |








| **Aplicaciones** |
| --- |
| 
* [*ServicesContract*](https://github.com/USantaTecla-tech-java/src/tree/cdf6862fac6b5bc6bba3652b857050a11c2efada/src/main/java/es/usantatecla/aX_managers/services/a1_classes)


 | 
* [*List*](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_listas/a1_basic/a0_classes)


 |  |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Miembros de Clase](../u5classMembers/README.md)
