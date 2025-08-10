# [Definición de constructores](./README.md)


* Reservado para las **tareas de inicialización de los atributos** del objeto, evitando la creación de objetos incosistentes


	+ A **falta de inicialización explícita**, **no recomendado**, se inicializan a **valores por defecto**, dependiendo de su tipo (*0* para tipos numéricos, *false* para el tipo *boolean*, caracter nulo para tipo *char* y *null* para referencias);

```java
class Interval

  private double min;
  private double max;

  public Interval(){
    min = 0;
    max = 0;
  }

  public Interval(double maximum){
    min = 0;
    max = maximum;
  }

  public Interval(double minimum, double maximum){
    min = minimum;
    max = maximum;
  }
  ...
```

---

[Volver al nivel superior](../README.md)

[Siguiente sección: Definición de metodos](../u3Definicióndemetodos/README.md)


[Anterior](../u1attributeDefinition/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3Definicióndemetodos/README.md)
