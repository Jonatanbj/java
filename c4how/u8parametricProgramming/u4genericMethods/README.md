# [Métodos Genéricos](README.md)




* Los métodos también se pueden parametrizar, tanto si están en una clase parametrizada como si no lo están.

	+ Para parametrizar un método se declaran los parámetros de tipo antes de la declaración del tipo del valor devuelto por el método.


`<acceso>` `<parámetro1,` `…,` `parámetroN>`
`<tipoDevuelto>` `<nombreMétodo>`(`<argumentos>`) {
	...
}


* Los **parámetros de tipo pueden usarse dentro del método parametrizado para declarar el tipo del valor devuelto por el método, de sus argumentos y de sus objetos locales**.
* Estos **parámetros de tipo (formales) se especifican posteriormente con un tipo concreto (actual) al invocar el método parametrizado**, lo que produce la encarnación del método.
* *Ejemplo*: [greaters](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_listas/a5_parametrized3)

---

**Aplicaciones**

* TicTacToe - [generics](https://github.com/USantaTecla-tech-java/src/tree/main/src/main/java/es/usantatecla/aX_ticTacToe/a9_generics)


---


[Anterior](../u3wildcardParameters/README.md) | [Subir nivel](../README.md) | [Siguiente](../u5collections/README.md)
