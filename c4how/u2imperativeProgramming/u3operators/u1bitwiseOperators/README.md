# [Operadores de Bits](./README.md)

* **Sintaxis**:

	+ *`<expresion>`* **::=** *`<expresion>`* *`<operadorBit>`* *`<expresion>`*
	+ *`<operadorBit>`* **::=** **&** **|** **|** **|** **^** **|** **~** **|** **<<** **|** **>>** **|** **>>>**
<br><br>
* **Semántica**:

	+ **&**, y-lógico de bits;
	+ **|**, o-lógico de bits;
	+ **^**, o-lógico exclusivo de bits;
	+ **~**, negación de bits;
	+ **<<**, desplaza hacia la izquierda rellenando con ceros;
	+ **>>**, desplaza hacia la derecha rellenando con el más significativo;
	+ **>>>**, desplaza hacia la derecha rellenando con ceros


```java
class App {
    
    public static void main(String[] args) {
        Console console = new Console();
        console.writeln(~4); // -5
        console.writeln(4 & 8); // 0
        console.writeln(4
```

**Aplicaciones** 

* [4-numberingSystems/4-decimalToBinary/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/4-numberingSystems.md#4-decimaltobinaryv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a4_decimalToBinary/v0_0/App.java)
---
[Anterior](../README.md) | [Subir nivel](../README.md) | [Siguiente](../u2ternaryOperator/README.md)
