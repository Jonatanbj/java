# Sentencia Secuencial






| Sentencia Secuencial | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<sentencia>* **::=** *<sentenciaSecuencial>*
	+ *<sentenciaSecuencial>* **::=** **{** **{** *<sentencia>* **}+** **}**

* **Semántica**:


	+ Su ejecución (espacio/tiempo) ejecuta secuencialmente las sentencias anidadas



 | 


```
package es.usantatecla.a0\_itinerario.a2\_estructurada.a3\_secuencial.a1\_sinVariables;

class App {

  public static void main(String[] args) {
    Console console = new Console();
    {
      console.writeln("- Inicio secuencial");
      {
        console.writeln(" - Inicio secuencial interno");
        {
          console.writeln(" - Hasta el infinito");
          console.writeln(" - y más allá ... no!");
        }
        console.writeln(" - Fin secuencial interno");
      }
      console.writeln("- Fin secuencial");
    }

    console.writeln("- Inicio secuencial");
    console.writeln(" - Inicio secuencial interno");
    console.writeln(" - Hasta el infinito");
    console.writeln(" - y más allá ... no!");
    console.writeln(" - Fin secuencial interno");
    console.writeln("- Fin secuencial");
  }
}
```


 |







| Ámbito de bloque | *java* |
| --- | --- |
| 
* Define un **ámbito léxico** (espacio) desde su apertura ({) hasta su cierre (})


	+ puede contener declaración de variables y constantes accesibles desde su declaración hasta el cierre del ámbito léxico
	+ pero dos variables **no pueden tener igual nombre en el mismo ámbito léxico**

* Reglas de **acceso a variables y/o constantes** desde las expresiones:


	+ una variable o constante mencionada, se busca en su ámbito léxico hacia atras, si no se encontrara, se busca en el ámbito léxico superior hacia atrás, recursivamente hasta encontrarla …​
	+ en caso contrario, se considerará como asignación o acceso desde una expresión a una **variable del ámbito global** creada en última instancia (sentencia *var*)
	+ Siempre de dentro hacia afuera!, según sus **ámbito léxico**, desde la apertura hasta su cierre
	+ Nunca desde fuera hacia dentro!!!, **ocultación de información**
	+ cuando termina la ejecución de la sentencia, **se destruyen todas las posibles variables y constantes creadas internamente**



 | 


```
package es.usantatecla.a0\_itinerario.a2\_estructurada.a3\_secuencial.a2\_conVariables;

class App {

  public static void main(String[] args) {
    Console console = new Console();
    int nivel0 = 100;
    console.writeln("---");
     // nivel2++;
     // console.writeln(nivel2);
     // nivel1++;
     // console.writeln(nivel1);
    nivel0++;
    console.writeln(nivel0); // 101
    
    {
      int nivel1 = 200;    
      console.writeln("---");
      // nivel2++;
      // console.writeln(nivel2);
      nivel1++;
      console.writeln(nivel1); // 201
      nivel0++;
      console.writeln(nivel0); // 102
    
      {
        int nivel2 = 300;
        console.writeln("---");
        nivel2++;
        console.writeln(nivel2); // 301
        nivel1++;
        console.writeln(nivel1); // 202
        nivel0++;
        console.writeln(nivel0); // 103
      }    
       console.writeln("---");
      // nivel2++;
      // console.writeln(nivel2);
      nivel1++;
      console.writeln(nivel1); // 203
      nivel0++;
      console.writeln(nivel0); // 104
    }
    console.writeln("---");
     // nivel2++;
     // console.writeln(nivel2);
     // nivel1++;
     // console.writeln(nivel1);
    nivel0++;
    console.writeln(nivel0); // 105
    
    {
      console.writeln("---");
     // nivel2++;
     // console.writeln(nivel2);
     // nivel1++;
     // console.writeln(nivel1);
      nivel0++;
      console.writeln(nivel0); // 106
    }    
  }
}
```


 |







| Ámbito de bloque | *java* |
| --- | --- |
| 
* Permite la ejecucuión alternativa o iterativa de varias sentencias


 | 


```
package es.usantatecla.a0\_itinerario.a2\_estructurada.a3\_secuencial.a4\_agrupacion;

class App {

  public static void main(String[] args) {
    Console console = new Console();
    int x = 3;
    while (x > 0) {
      console.write(x + ", "); // 3, 2, 1,
      x--;
    }
    console.writeln(x + "."); // 0.
    
    do {
      console.write(x + ", "); // 0, 1, 2,
      x++;
    } while (x < 3);
    console.writeln(x + "."); // 3.
    
    for (int i = 0; i < x; i++){
      console.write(i + ": "); 
      console.write(x + ", "); 
    }
    console.writeln(); // 0: 3, 1: 3, 2: 3,
    
    for (int i = x; 0 < i; i--){
      console.write(i + ": "); 
      console.write(x + ", "); 
    }
    console.writeln(); // 3: 3, 2: 3, 1: 3,
  }
}
```


 |








| **Aplicaciones** |
| --- |
| 
* [3-sumTimes/v0.0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/0-time.md#3-sumtimesv00) - [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a0_time/a3_sumTimes/v0_0/App.java)


 | 
* [1-space/2-triangle/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/1-space.md#2-trianglev0) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a1_space/a2_triangle/v0_0/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a1_space/a2_triangle/v0_1/App.java) - [v0.2](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a1_space/a2_triangle/v0_2/App.java)


 | 
* [2-texts/1-echo/v1](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#1-echov1) : [*v1.1*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a1_echo/v1_1/App.java) - [v1.2](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a1_echo/v1_2/App.java)


 |
| 
* [3-numbers/0-multiplicationTable/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#0-multiplicationtable) : [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a0_multiplicationTable/v0_4/App.java) - [v0.1](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a0_multiplicationTable/v0_1/App.java) - [v0.2](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a0_multiplicationTable/v0_2/App.java) - [v0.3](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a0_multiplicationTable/v0_3/App.java) - [v0.4](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a0_multiplicationTable/v0_4/App.java)


 | 
* [3-numbers/6-prime/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#6-prime) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a6_prime/v0_0/App.java)


 | 
* [3-numbers/6-prime/v1](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#6-primev1) : [v1.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a6_prime/v1_0/App.java)


 |
| 
* [3-numbers/6-prime/v2](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#6-primev2) : [v2.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a6_prime/v2_0/App.java)


 | 
* [3-numbers/7-perfect/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#7-perfectv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a7_perfect/v0_0/App.java)


 | 
* [3-numbers/8-friends/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#8-friendsv0) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a8_friends/v0_0/App.java)


 |
| 
* [3-numbers/8-friends/v1](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#8-friendsv1) : [v1.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a8_friends/v1_0/App.java)


 | 
* [3-numbers/10-fibonacci/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#10-fibonacci) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a10_fibonacci/v0_0/App.java)


 | 
* [3-numbers/11-power/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#11-power) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a11_power/v0_0/App.java)


 |
| 
* [4-numberingSystems/0-digits/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/4-numberingSystems.md#0-digits) : [*v0.2*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a0_digits/v0_2/App.java) - [v0.3](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a0_digits/v0_3/App.java)


 | 
* [4-numberingSystems/3-binaryToDecimal/v1](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/4-numberingSystems.md#3-binaryToDecimalv1) : [*v0.1*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a3_binaryToDecimal/v0_0/App.java) - [v1.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a3_binaryToDecimal/v1_0/App.java)


 | 
* [4-numberingSystems/4-decimalToBinary/v1](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/4-numberingSystems.md#4-decimaltobinaryv1) : [*v0.1*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a4_decimalToBinary/v0_1/App.java) - [v1.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a4_decimalToBinary/v1_0/App.java)


 |
| 
* [1-interval6-isintersected](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/5-units.md#1-interval6-isintersected) : [isIntersected](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a1_interval/scenarios/isIntersected/App.java)


 |  |  |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Tablas](../u4tables/README.md)
