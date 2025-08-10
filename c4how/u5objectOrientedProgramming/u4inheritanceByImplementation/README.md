# Herencia por Implementación






| **Interfaces** | **Ejemplo** |
| --- | --- |
| 
* Son **clases abstractas puras** que no contienen ningún atributo ni la definición de ningún método, **sólo contienen métodos abstractos**.


	+ puede ser base de clases u otros interfaces.
	+ donde todos los métodos del interfaz son públicos.



 | 


```
interface <interfazBase> {
    <cabeceraMetodo1>;
    …
    <cabeceraMetodoN>;
}

[abstract] class <claseDerivada> implements <interfazBase> {
    …
}

interface <interfazDerivado> extends <interfazBase> {
    …
}
```


 |








| **Aplicaciones** |
| --- |
| 
* Dispenser - [*herencia*](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_dispensers/a5_extends_a2_dispenser) - [interfaces](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_dispensers/a6_interfaces)


 |  |







| 
* **Una interfaz**


	+ **NO puede heredar de una clase de ninguna manera**
	+ **SI puede heredar de otro interfaz por extensión**

* **Una clase**


	+ **SI puede heredar de una clase por extensión**
	+ **SI puede heredar de varios interfaces por implementación**

* **Herencia mútiple**
* **La herencia por extensión NO la permite**


	+ **la herencia por implementación SI la permite**



 | 


```
class <claseDerivada>
  extends <claseBase>
  implements <interfaz1>, …, <interfazN> {
  …
}
interface <interfazDerivado>
  extends <interfaz1>, …, <interfazN> {
  …
}
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Limitaciones de la Herencia](../u5inheritanceLimitations/README.md)


[Anterior](../u3abstractClasses/README.md) | [Subir nivel](../README.md) | [Siguiente](../u5inheritanceLimitations/README.md)
