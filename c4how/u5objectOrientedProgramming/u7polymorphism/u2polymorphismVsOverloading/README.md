# Polimorfismo vs sobrecarga







| **Sobrecarga** | *Ejemplos* |
| --- | --- |
| 
es un **enlace estático entre un mensaje y el método que se ejecuta**;
 | 


```
class A {
  public void m()
  public void m(A a)
  public void m(B b)
  public A m(B b, C c)
  public B m(A a, C c)
}
class B {
}
```


 | 


```
class C {
}
…

A a;
B b;
C c;
a.m(b, c).m();
b = a.m(a, c);
…
```


 |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Beneficios del Polimorfismo](../u3polymorphismBenefits/README.md)


[Anterior](../u1formalization/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3polymorphismBenefits/README.md)
