# [Referencia a un vector de referencias a objetos](./README.md)

| **Definición** | **Sintaxis** | **Ejemplo** |
| --- | --- | --- |
| Es una variable puntero que alberga la dirección de un vector de referencias a objetos de una clase. | ![referencia2](/images/Referencia2.jpg) <br><br> - **final** obliga a la inicialización y fija su valor para la referencia| Intervalo **[   ]** intervalos; <br><br> ![Intervalos](/images/EjemploReferencia2%20(2).jpg)|

<br>

```java
Intervalo[] intervalos = new Intervalo[10];
intervalos[0] = new Intervalo ();
intervalos[1] = intervalos[0].desplazados(1);
intervalos[intervalos.length-1] = new Intervalo(2,2);
Intervalo intervalo = intervalos[1];
intervalos = null;**(1)**
...
```
**1** *Se libera automáticamente toda la memoria de las referencias del vector y de cada objeto excepto del segundo intervalo porque nadie está apuntando a dichos elementos;*

---


[Anterior](../u4objectArrayCreation/README.md) | [Subir nivel](../README.md) | [Siguiente](/c4how/u4objectBasedProgramming/u3privateViewOfClasses/README.md)
