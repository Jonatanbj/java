# [Polimorfismo vs sobrecarga](README.md)


**Sobrecarga:** es un **enlace estático entre un mensaje y el método que se ejecuta**;

*Ejemplos:*
```java
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


```java
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

---




[Anterior](../u1formalization/README.md) | [Subir nivel](../README.md) | [Siguiente](../u3polymorphismBenefits/README.md)
