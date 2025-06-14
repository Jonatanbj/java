# Cadenas de Caracteres







| **Definición** | **Constantes, inmutables** | **Variables, mutables** |
| --- | --- | --- |
| 
* Son **secuencias de caracteres de cualquier longitud**, incluso **secuencia vacía**


 | 
* cuyos caracteres no varían tras la creación


	+ Implementadas bajo la clase **String** sin contemplar métodos que modifiquen el estado del objeto.
	+ *Ej. El nombre de una persona, de un mes, de una universidad, de un proyecto, …​*



 | 
* cuyos caracteres sí varían tras la creación


	+ Implementadas bajo las clases **StringBuffer** (con sincronización en concurrencia) y **StringBuilder** (sin) con métodos que contemplan la modificación del objeto
	+ *Ej. Membrete de una carta, párrafo de aviso, clausula de contrato, …​*



 |







| *Clase* [*String*](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html) |
| --- |
| 


```
public String()
public String(String)
public String(char[])
public String(char[], int, int)
public String(int[], int, int)
public String(byte[], int, int, int)
public String(byte[], int)
public String(byte[], int, int)
public String(byte[])
public String(StringBuffer)
public String(StringBuilder)
public int length()
public boolean isEmpty()
public char charAt(int)
public byte[] getBytes()
public char[] toCharArray()
public String toString()
public void getChars(int, int, char[], int)
public void getBytes(int, int, byte[], int)

public CharSequence subSequence(int,int)
public String substring(int)
public String substring(int, int)

public int hashCode()
public int indexOf(String)
public int indexOf(String, int)
public int indexOf(int)
public int indexOf(int, int)
public int lastIndexOf(String)
public int lastIndexOf(String, int)
public int lastIndexOf(int)
public int lastIndexOf(int, int)
```


 | 


```
public int codePointAt(int)
public int codePointBefore(int)
public int codePointCount(int, int)
public int offsetByCodePoints(int, int)

public boolean equals(Object)
public boolean equalsIgnoreCase(String)
public boolean contentEquals(StringBuffer)
public boolean matches(String)
public boolean regionMatches(int,String, int, int)
public boolean regionMatches(boolean,int, String,int, int)
public boolean startsWith(String, int)
public boolean startsWith(String)
public boolean endsWith(String)
public int compareTo(String)
public int compareToIgnoreCase(String)
public String[] split(String)
public String[] split(String, int)

public String concat(String)
public String replace(char, char)
public String replaceFirst(String, String)
public String replaceAll(String, String)
public String toLowerCase()
public String toUpperCase()
public String trim()
```


 |
| 


```
void getBytes(int srcBegin, int srcEnd,
  byte[] dst, int dstBegin)
```


 | 


```
void getChars(int srcBegin, int srcEnd,
  char[] dst, int dstBegin)
```


 |
| 


```
public static String valueOf(char)
public static String valueOf(int)
public static String valueOf(long)
public static String valueOf(char[])
public static String copyValueOf(char[])
```


 | 


```
public static String valueOf(float)
public static String valueOf(double)
public static String valueOf(boolean)
public static String valueOf(char[], int, int)
public static String copyValueOf(char[],int, int)
```


 |







| *Clases* [*StringBuffer*](https://docs.oracle.com/javase/7/docs/api/java/lang/StringBuffer.html) y [*StringBuilder*](https://docs.oracle.com/javase/7/docs/api/java/lang/StringBuilder.html) |
| --- |
| 


```
public StringBuffer()
public StringBuffer(int)
public StringBuffer(String)
public StringBuffer(CharSequence)

public int length()
public char charAt(int)
public String substring(int)
public String substring(int, int)
public CharSequence subSequence(int,int)
public String toString()

public int indexOf(String)
public int indexOf(String, int)
public int lastIndexOf(String)
public int lastIndexOf(String, int)

public int codePointAt(int)
public int codePointBefore(int)
public int codePointCount(int, int)
public int offsetByCodePoints(int, int)

public int capacity()
public void ensureCapacity(int)
public void setLength(int)
public void trimToSize()
public void getChars(int, int, char[], int)
```


 | 


```
public StringBuffer append(String)
public StringBuffer append(StringBuffer)
public StringBuffer append(char[])
public StringBuffer append(char[], int, int)
public StringBuffer append(boolean)
public StringBuffer append(char)
public StringBuffer append(int)
public StringBuffer appendCodePoint(int)
public StringBuffer append(long)
public StringBuffer append(float)
public StringBuffer append(double)

public StringBuffer insert(int, char[], int,int)
public StringBuffer insert(int, String)
public StringBuffer insert(int, char[])
public StringBuffer insert(int, boolean)
public StringBuffer insert(int, char)
public StringBuffer insert(int, int)
public StringBuffer insert(int, long)
public StringBuffer insert(int, float)
public StringBuffer insert(int, double)

public StringBuffer delete(int, int)
public StringBuffer deleteCharAt(int)

public void setCharAt(int, char)
public StringBuffer replace(int, int, String)
public StringBuffer reverse()
...
```


 |







| **Literales *String*** | *Ejemplos* |
| --- | --- |
| 
* es la única clase cuyos objetos pueden presentarse en forma literal;
* su formato es una secuencia de caracteres de cualquier longitud encerrados entre dobles comillas






```
"<caracter>..."
```




* son objetos de la clase **String** cuya evaluación devuelve la dirección del objeto al que representan;
* además, es la única clase que disfruta de un operador (**+**) para la concatenación de cadenas de caracteres y combinado con cualquier tipo.


 | 


```
int longitud = "caracteres".length();
String cadena = new String("caracteres");
boolean falso = cadena == "caracteres";
boolean cierto = cadena.equals("caracteres");
boolean tambien = "caracteres".equals(cadena);
StringBuffer buffer = new StringBuffer(cadena);
buffer.insert(0, "de ").insert(0, "cadena ");
boolean si = ("cadena de " + cadena).
    contentEquals(buffer);
String serie = (0+1)+", "+(1+1)+","+(2+1)+".";
```


 |








| **Aplicaciones** |
| --- |
| 
* [3-initials/v0.0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#3-initialsv0) - [*v0.0*](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a3_initials/v0_0/App.java) - [v1.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a3_initials/v1_0/App.java)


 | 
* [2-texts/2-morseTranlator/v0](https://github.com/USantaTecla-0-domains/0-simpleDomains/blob/master/docs/2-texts.md#2-morsetranlator) : [v0.0](https://github.com/USantaTecla-tech-java/src/blob/main/src/main/java/es/usantatecla/a2_texts/a2_morseTranslator/v0_0/App.java)


 |  |


---

[Volver al nivel superior](../README.md)

[Siguiente sección: Enumerados](../u8enumerations/README.md)
