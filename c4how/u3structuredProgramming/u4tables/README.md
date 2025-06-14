# Tablas






| Creación | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<expresion>* **::=** **[** **new** *<tipo>* **[** **]** **+** **]** **{** **[** *<expresion>* **{** **,** *<expresion>* **}** **]** **}** **|** **new** *<tipo>* **[** *<expresion>* **]** **+** **[** **]** *****
	+ *<sentenciaFor>* **::=** **for** **(** *<tipo>* *<identificador>* **:** *<expresión>* **)** *<sentencia>*

* **Semántica**:


	+ El operador ***new*** es unario prefijo cuyos operandos son tipo de tablas y devuelve la **dirección de memoria donde se ha reservado el espacio para dicha tabla**
	
	
		- su nivel de precedencia es igual al de los operadores unarios.
		- donde el vector se crea con n elementos inicializados con 0, false o '\0' los tipos numéricos, lógicos o caracteres respectivamente o con los valores de la evaluación de las expresiones correspondientes
	
	+ Tipo de dato **estructurado/compuesto** que permite almacenar un conjunto de datos **bajo un mismo identificador**, tabla, vector, matriz, retícula, rejilla, …​ *array*
	
	
		- Cada uno de los **elementos** que componen un vector pueden ser de cualquier tipo:
		
		
			* **tipo primitivo**, *number, string, boolean, undefined*;
			* tipo estructurado/compuesto como los propios **arrays** pudiendo construir arrays de arrays de tipos primitivos, tablas bidimensionales, …​ arrays de arrays de …​ de tipos primitivos, **tablas n-dimensionales**
		
		- Recomendado que sea una **colección de elementos homogéneos, todos ellos del mismo tipo y de la misma naturaleza**: no combinar 5 contadores y un acumulador



 | 


```
package es.usantatecla.a0\_itinerario.a2\_estructurada.a4\_tablas.a1\_creacion;

class App {

    public static void main(String[] args) {
        Console console = new Console();
        for (int value : new int[] {}) {
            console.write(value); //
        }
        console.writeln();
        for (int value : new int[] { 1, 2, 3, 4, 5 }) {
            console.write(value + ", "); // 1, 2, 3, 4, 5,
        }
        console.writeln();
        for (String value : new String[] { "Java", "Javascript", "Scala" }) {
            console.write(value + ", "); // Javascript, Java, Scala
        }
        console.writeln();
        for (boolean value : new boolean[] { false, true }) {
            console.write(value + ", "); // false, true
        }
        console.writeln();
        boolean b = false;
        for (boolean x : new boolean[] { true, b, 5 + 6 > 5 - 6 }) {
            console.write(x + ", "); // true, false, true,
        }
        console.writeln();
        for (char[] vowels : new char[][] {
                { 'a', 'e', 'i', 'o', 'u' },
                { 'A', 'E', 'I', 'O', 'U' } }) {
            for (char vowel : vowels) {
                console.write(vowel + ", "); // a, e, i, o, u, A, E, I, O, U
            }
        }
        console.writeln();
        for (char[] row : new char[][] {
                { 'x', ' ', 'o' },
                { 'x', 'o', 'o' },
                { ' ', ' ', 'x' } }) {
            for (char token : row) {
                console.write(token + ", "); // x, ,o, x, o, o, , ,x
            }
        }
        console.writeln();
        for (int[][] tableData : new int[][][] {
                {
                        { 0, 0, 0 },
                        { 0, 0 },
                        { 0 } },
                {
                        {},
                        { 1, 2, 3, 4 } } }) {
            for (int[] row : tableData) {
                for (int value : row) {
                    console.write(value + ", "); // 0, 0, 0, 0, 0, 0, 1, 2, 3, 4
                }
            }
        }
        console.writeln();
        for (int value : new int[3 * 2]) {
            console.write(value + ", "); // 0, 0, 0, 0, 0, 0,
        }
        console.writeln();
        int length = 3;
        for (boolean[] row : new boolean[length - 1][2]) {
            for (boolean value : row) {
                console.write(value + ", "); // false, false, false, false,
            }
        }
        console.writeln();
        int[][] notIntsOnlyRows = new int[10][];
    }
}
```


 |







| Acceso a elementos | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<expresión>* **::=** *<expresión>* **[** *<expresión>* **]**
	+ *<expresión>* **::=** *<expresión>* **.length**

* **Semántica**:


	+ mediante la **indexación** del *array* dado por la primera expresión con la posición deseada a través de la segunda expresión entera comenzando por **0 para el primer elemento**
	+ mediante la propiedad ***length*** se accede a la cantidad del elementos del *array* dado por la expresión, **uno más del índice del último elemento porque empieza por 0**
	+ sentencias *for* especiales para *arrays*
	
	
		- donde la variable declarada tomará cada uno de los valores del *array* en el orden natural



 | 


```
package es.usantatecla.a0\_itinerario.a2\_estructurada.a4\_tablas.a2\_acceso;

class App {

    public static void main(String[] args) {
        Console console = new Console();
        console.writeln(new int[] { 1, 2, 3, 4, 5 }[0]); // 1
        console.writeln(new int[] { 1, 2, 3, 4, 5 }[4]); // 5
        //console.writeln(new int[] { 1, 2, 3, 4, 5 }[5]); // ERROR
        console.writeln(new String[][] { 
            { "a", "b", "c" }, 
            { "x", "y", "z" } }[0][0]); // a
        for(String value : new String[][] { 
            { "a", "b", "c" }, 
            { "x", "y", "z" } }[1]){
            console.write(value + ", "); // x, y, z,
        }
        console.writeln();
        console.writeln(new int[] { 0, 1, 2 }.length); // 3
        console.writeln(new String[][] { 
            { "a" }, 
            { "x", "y", "z" } }[0].length); // 1
        console.writeln(new String[][] { 
            { "a" }, 
            { "x", "y", "z" } }[1].length); // 3
        console.writeln(new String[][] { 
            { "a" }, 
            { "x", "y", "z" } }.length); // 2
    }
}
```


 |







| Referencias | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<sentencia>* **::=** **(** **byte** **|** **short** **|** **int** **|** **long** **|** **float** **|** **double** **|** **char** **|** **String** **|** **boolean** **)** **(** **[** **]** **)** **\+** *<identificador>* **[** **=** *<expresion>* *** [red]**]*

* **Semántica**:


	+ son variables/constantes declaradas no almacenan el valor compuesto del array, como ocurre con los tipos primitivos, sino que **almancenan la dirección/"referencia" a la memoria donde se almacenan los valores del tipo compuesto**



 | 


```
package es.usantatecla.a0\_itinerario.a2\_estructurada.a4\_tablas.a3\_referencia;

class App {

    public static void main(String[] args) {
        Console console = new Console();
        int[] array = new int[] { 1, 2, 3, 4, 5 };
        console.writeln(array[0]); // 1
        console.writeln(array[4]); // 5
        // console.writeln(array[5]); // ERROR!!!
        console.writeln(array.length); // 5

        int primitive1 = 1;
        int primitive2 = primitive1;
        console.writeln(primitive1); // 1
        console.writeln(primitive2); // 1
        primitive2 = 2;
        console.writeln(primitive1); // 1
        console.writeln(primitive2); // 2

        int[] array1 = new int[] { 1, 2, 3 };
        for(int value : array1) {
            console.write(value + ", "); // 1, 2, 3
        }
        console.writeln();
        int[] array2 = array1;
        for(int value : array2) {
            console.write(value + ", "); // 1, 2, 3
        }
        console.writeln();
        array1[1] = 666;
        for(int value : array1) {
            console.write(value + ", "); // 1, 666, 3
        }
        console.writeln();
        for(int value : array2) {
            console.write(value + ", "); // 1, 666, 3
        }
        console.writeln();
        console.writeln(array1 == array2); // true

        array1 = new int[] { 1, 666, 3 };
        for(int value : array1) {
            console.write(value + ", "); // 1, 666, 3
        }
        console.writeln();
        for(int value : array2) {
            console.write(value + ", "); // 1, 666, 3
        }
        console.writeln();
        console.writeln(array1 == array2); // false

        array2[1] = 0;
        for(int value : array1) {
            console.write(value + ", "); // 1, 666, 3
        }
        console.writeln();
        for(int value : array2) {
            console.write(value + ", "); // 1, 0, 3
        }
        console.writeln();
        console.writeln(array1 == array2); // false

        for (int value : array1) {
            console.write(value + ", "); // 1, 666, 3,
        }
        console.writeln();
        for (int i = 0; i < array1.length; i++) {
            console.writeln(i + ": " + array1[i] + ", "); // 0: 1, 1: 666, 2: 3,
        }
        console.writeln();
    }
}
```


 |







| Modificación de elementos | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<sentAsignacion>* **::=** *<expresión>* **[** *<expresión>* **]** = *<expresión>* **;**

* **Semántica**:


	+ mediante la asignación del valor de la evaluación de una expresión (3), en la posición indexada mediante el valor entero de la expresión (2) del *array* dado por la primera expresión (1)



 | 


```
package es.usantatecla.a0\_itinerario.a2\_estructurada.a4\_tablas.a4\_modificacion;

class App {

  public static void main(String[] args) {
    Console console = new Console();
    int[][] bidimensional = new int[][] {
        { 1, 2, 3 },
        { 0 },
        { 9, 8, 7 }
    };
    int[] temp = bidimensional[0];
    bidimensional[0] = bidimensional[1];
    bidimensional[1] = bidimensional[2];
    bidimensional[2] = temp;
    for(int[] unidimensional : bidimensional){
      for(int atom : unidimensional){
        console.writeln(atom);
      }
    }
  }
}
```


 |







| Valor ***null*** | *java* |
| --- | --- |
| 
* **Sintaxis**:


	+ *<literal>* **::=** **null**

* **Semántica**:


	+ la dirección ***null*** es el valor de **aquella dirección donde no hay valores**



 | 


```
package es.usantatecla.a0\_itinerario.a2\_estructurada.a4\_tablas.a5\_null;

class App {

  public static void main(String[] args) {
    Console console = new Console();
    int[][] array = new int[][] { { 1, 666, 3 }, null, { 0 } };
    for (int[] row : array) {
      if (row != null) {
        for (int value : row) {
          console.writeln(value + ", "); // 1, 666, 3, 0
        }
      }
    }
    array[2] = null;
    array[1] = array[0];
    for (int[] row : array) {
      if (row != null) {
        for (int value : row) {
          console.writeln(value + ", "); // 1, 666, 3, 1, 666, 3, 
        }
      }
    }
  }
}
```


 |








| **Aplicaciones** |
| --- |
| 
* [3-numbers/5-changeCoins/v1](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/3-numbers.md#5-changecoinsv1) : [*v1.1*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a5_changeCoins/v1_1/App.java) - [v1.2](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a3_numbers/a5_changeCoins/v1_2/App.java)


 | 
* [1-space/2-triangle/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/1-space.md#2-trianglev0) : [*v0.2*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a1_space/a2_triangle/v0_2/App.java) - [v0.3](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a1_space/a2_triangle/v0_3/App.java)


 | 
* [4-numberingSystems/0-digits/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/4-numberingSystems.md#0-digits) : [*v0.1*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a0_digits/v0_1/App.java) - [v0.2](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a4_numberingSystems/a0_digits/v0_2/App.java)


 |
| 
* [6-collections/3-matrixTranspose/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/6-collections.md#3-matrixtranspose) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a6_collections/a3_matrixTranspose/v0_0/App.java)


 | 
* [1-interval4-split](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/5-units.md#1-interval4-split) : [split](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a5_units/a1_interval/scenarios/split/App.java)


 |  |


---

[Volver al nivel superior](../README.md)

