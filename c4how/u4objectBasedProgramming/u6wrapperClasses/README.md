# Clases de Recubrimiento


**Clases de Recubrimiento**  
* Aglutinan funciones de conversión entre los tipos primitivos y las correspondientes cadenas de caracteres junto con algunas otras funciones auxiliares particulares de cada tipo primitivo.


	+ *Clase* [*Character*](https://docs.oracle.com/javase/8/docs/api/java/lang/Character.html)
	+ *Clase* [*Byte*](https://docs.oracle.com/javase/8/docs/api/java/lang/Byte.html)
	+ *Clase* [*Short*](https://docs.oracle.com/javase/8/docs/api/java/lang/Short.html)
	+ *Clase* [*Integer*](https://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html)
	+ *Clase* [*Long*](https://docs.oracle.com/javase/8/docs/api/java/lang/Long.html)
	+ *Clase* [*Float*](https://docs.oracle.com/javase/8/docs/api/java/lang/Float.html)
	+ *Clase* [*Double*](https://docs.oracle.com/javase/8/docs/api/java/lang/Double.html)
	+ *Clase* [*Boolean*](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)


***Clase*** [*Character*](https://docs.oracle.com/javase/8/docs/api/java/lang/Character.html) 
```java
class Character {
  Character(char)
  char charValue()
  int compareTo(Character)
  int hashCode()
  public static String toString(char)
  public static char[] toChars(int)
  public static boolean isLowerCase(char)
  public static boolean isUpperCase(char)
  public static boolean isTitleCase(char)
  public static boolean isDigit(char)
  public static boolean isDefined(char)
  public static boolean isLetter(char)
  public static boolean isLetterOrDigit(char)
  public static char toLowerCase(char)
  public static char toUpperCase(char)
  public static char toTitleCase(char)
  public static int getNumericValue(char)
  public static boolean isSpace(char)
  public static boolean isSpaceChar(char)
  public static boolean isWhitespace(char)
  ...
}
```


 **Clase** [*Integer*](https://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html) 


```java
class Integer {
  public static final int MIN_VALUE;
  public static final int MAX_VALUE;
  public static final int SIZE;
  public Integer(int)
  public Integer(String)
  public byte byteValue()
  public short shortValue()
  public int intValue()
  public long longValue()
  public float floatValue()
  public double doubleValue()
  public String toString()
  public int hashCode()
  public int compareTo(Integer)
  public static String toString(int, int)
  public static String toHexString(int)
  public static String toOctalString(int)
  public static String toBinaryString(int)
  public static String toString(int)
  public static int stringSize(int)
  public static int parseInt(String, int)
  public static int parseInt(String)
  public static Integer valueOf(String, int)
  public static Integer valueOf(String)
  public static Integer valueOf(int)
  public static Integer getInteger(String)
  public static Integer getInteger(String,int)
  public static Integer getInteger(String,Integer)
  public static Integer decode(String)
  public static void getChars(int, int, char[])
}
```

*Clase* [*Boolean*](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html) 


```java
class Boolean {
  public static Boolean FALSE
  public static Boolean TRUE
  public Boolean(boolean value)
  public Boolean(String s)
  public boolean booleanValue()
  public String toString()
  public boolean equals(Object obj)
  public int compareTo(Boolean b)
  public int hashCode()
  public static int compare(boolean x, boolean y)
  public static boolean getBoolean(String name)
  public static int hashCode(boolean value)
  public static boolean logicalAnd(boolean a, boolean b)
  public static boolean logicalOr(boolean a, boolean b)
  public static boolean logicalXor(boolean a, boolean b)
  public static boolean parseBoolean(String s)
  public static Boolean valueOf(boolean b)
  public static Boolean valueOf(String s)
  public static String toString(boolean b)
}
```
*Ejemplos*


```java
public Fecha(String cadena) {
  dia = Integer.parseInt(
    cadena.substring(0, cadena.indexOf("/")));
  cadena = cadena.substring(
    cadena.indexOf("/") + 1, cadena.length());
  mes = Integer.parseInt(
    cadena.substring(0, cadena.indexOf("/")));
  cadena = cadena.substring(
    cadena.indexOf("/") + 1, cadena.length());
  año = Integer.parseInt(cadena);
}

public String toString() {
  return dia + "/" + mes + "/" + año;
}
...
```

---



[Anterior](../u5classMembers/README.md) | [Subir nivel](../README.md) | [Siguiente](../u7stringsManipulation/README.md)
