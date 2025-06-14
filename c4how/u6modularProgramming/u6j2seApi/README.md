# API de J2SE






| **Biblioteca estandar** (***[Application Programming Interface](https://docs.oracle.com/javase/8/docs/api/)***) |
| --- |
| 
* **[*java.lang*](https://docs.oracle.com/javase/8/docs/api/java/lang/package-summary.html)**: clases básicas del lenguaje, recubrimientos, …​ importado implícitamente por cualquier proyecto
* **[*java.util*](https://docs.oracle.com/javase/8/docs/api/java/util/package-summary.html)**: utilidades y estructuras de datos
* **[*java.time*](https://docs.oracle.com/javase/8/docs/api/java/time/package-summary.html)**: calendario, desaprobando *java.util.Calendar*, *java.util.Date*, …​
* **[*java.io*](https://docs.oracle.com/javase/8/docs/api/java/io/package-summary.html)**: acceso a ficheros
* ***java.awt, javax.swing***: interfaces gráficas de usuario
* ***java.net***: acceso a redes
* ***java.sql***: acceso a bases de datos
* …​


 | 

height32

 |
| 

height32

 | 

height32

 |
| 

height32

 | 

height32

 |







| [Clase *java.util.Random*](https://docs.oracle.com/javase/6/docs/api/java/util/Random.html) | *Ejemplo* |
| --- | --- |
| 
* implantación más eficiente y menos sesgada, más aleatoria, que *Math.random()*






```
Random() {}
Random(long seed) {}
int nextInt(int top)**(1)**
int nextInt()
long nextLong()
float nextFloat()
double nextDouble()
double nextGaussian()
boolean nextBoolean()
void nextBytes(byte[] bytes)
void setSeed(long seed)**(2)**
```






|  |  |
| --- | --- |
| **1** | genera valores de 0 a *top* |
| **2** | establece una semilla a partir de la cual generar los siguientes valores aleatorios, habitualmente alimentado con *System.currentTimeMillis()* |


 | 


```
package es.usantatecla.a0\_itinerario.a6\_packages.a2\_random;

import java.util.Random;

class App {

  public static void main(String[] args) {
    final int min = 3;
    final int max = 7;
    Random random = new Random();
    for (int i = 0; i < 10; i++) {
      Console.instance().writeln(min + random.nextInt(max - min + 1));
    }
    random = new Random(System.currentTimeMillis());
    Console.instance().writeln(random.nextInt());
    Console.instance().writeln(random.nextDouble());
  }

}
```


 |







| Clases de Expresiones Regulares | *Ejemplo* |
| --- | --- |
| 
* **[*java.util.regex.Pattern*](https://docs.oracle.com/javase/6/docs/api/java/util/regex/Pattern.html)**






```
static Pattern compile(String expReg)
Matcher matcher(String text)
```




* **[*java.util.regex.Matcher*](https://docs.oracle.com/javase/6/docs/api/java/util/regex/Matcher.html)**






```
boolean find()
String group()
int start()
int end()
String replaceAll(String text)
```


 | 


```
package es.usantatecla.a0\_itinerario.a6\_packages.a1\_regExp;

import java.util.regex.Matcher;
import java.util.regex.Pattern;

class App {

  public static void main(String[] args) {
    Pattern words = Pattern.compile("\\w+");
    final String TEXT = "Uno, dos, tres y cuatro.";
    Matcher matcher = words.matcher(TEXT);
    while (matcher.find()) {
      Console.instance().writeln(
        "\"" + matcher.group() + "\""
        + "(" + matcher.start() + 
        "-" + matcher.end() + ")");
    }
    Pattern separators = 
      Pattern.compile(
        "[\\s,.]+", Pattern.CASE_INSENSITIVE);
    Console.instance().writeln(
      separators.matcher(TEXT).replaceAll("\n"));
  }
}
```


 |







| Clases de Calendario | *Ejemplo* |
| --- | --- |
| 
* **[*java.time.LocalDateTime*](https://docs.oracle.com/javase/8/docs/api/java/time/package-summary.html)**






```
int getYear()
LocalDateTime plusYears(long years)
LocalDateTime minusYears(long years)
LocalDateTime withYear(int year)
Month getMonth()
int getMonthValue()
LocalDateTime plusMonths(long months)
LocalDateTime minusMonths(long months)
LocalDateTime withDayOfMonth(int dayOfMonth)
LocalDateTime withMonth(int month)
LocalDateTime plusWeeks(long weeks)
LocalDateTime minusWeeks(long weeks)
int getDayOfMonth()
DayOfWeek getDayOfWeek()
int getDayOfYear()
LocalDateTime plusDays(long days)
LocalDateTime minusDays(long days)
LocalDateTime withDayOfYear(int dayOfYear)
int getHour()
LocalDateTime plusHours(long hours)
LocalDateTime minusHours(long hours)
LocalDateTime withHour(int hour)
int getMinute()
LocalDateTime plusMinutes(long minutes)
LocalDateTime minusMinutes(long minutes)
LocalDateTime withMinute(int minute)
int getSecond()
LocalDateTime plusSeconds(long seconds)
LocalDateTime minusSeconds(long seconds)
LocalDateTime withSecond(int second)
int getNano()
LocalDateTime plusNanos(long nanos)
LocalDateTime minusNanos(long nanos)
LocalDateTime withNano(int nanoOfSecond)
LocalDateTime plus(long amountToAdd, TemporalUnit unit)
LocalDateTime minus(long amountToSubtract, TemporalUnit unit)
LocalDateTime plus(TemporalAmount amountToAdd)
LocalDateTime minus(TemporalAmount amountToSubtract)
LocalDateTime with(TemporalAdjuster adjuster)
LocalDateTime with(TemporalField field, long newValue)
long getLong(TemporalField field)
boolean isAfter(LocalDateTime other)
boolean isBefore(LocalDateTime other)
LocalDate toLocalDate()
LocalTime toLocalTime()
static LocalDateTime now()
static LocalDateTime now(Clock clock)
static LocalDateTime now(ZoneId zone)
static LocalDateTime of(LocalDate date, LocalTime time)
static LocalDateTime of(int year, Month month, int dayOfMonth, int hour, int minute)
static LocalDateTime of(int year, int month, int dayOfMonth, int hour, int minute)
static LocalDateTime of(int year, Month month, int dayOfMonth, int hour, int minute, int second)
static LocalDateTime of(int year, int month, int dayOfMonth, int hour, int minute, int second)
static LocalDateTime of(int year, Month month, int dayOfMonth, int hour, int minute, int second, int nanoOfSecond)
static LocalDateTime of(int year, int month, int dayOfMonth, int hour, int minute, int second, int nanoOfSecond)
static LocalDateTime parse(CharSequence text)
static LocalDateTime parse(CharSequence text, DateTimeFormatter formatter)
...
}

class LocalDate {
public int getYear()
...
}

class LocalTime {
public int getHour()
...
}
```




* **[*java.time.Month*](https://docs.oracle.com/javase/8/docs/api/java/time/Month.html)**






```
JANUARY
...
int	maxLength()
```




* **[*java.time.DayOfWeek*](https://docs.oracle.com/javase/8/docs/api/java/time/DayOfWeek.html)**
* **[*java.time.Period*](https://docs.oracle.com/javase/8/docs/api/java/time/Period.html)**
* **[*java.time.Duration*](https://docs.oracle.com/javase/8/docs/api/java/time/Duration.html)**
* **[*java.time.ZoneId*](https://docs.oracle.com/javase/8/docs/api/java/time/ZoneId.html)**
* **[*java.time.ZonedDateTime*](https://docs.oracle.com/javase/8/docs/api/java/time/ZonedDateTime.html)**
* **[*java.time.format.DateTimeFormatter*](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html)**
* **[*java.time.temporal.ChronoUnit*](https://docs.oracle.com/javase/8/docs/api/java/time/temporal/ChronoUnit.html)**
* **[*java.time.temporal.TemporalAdjusters*](https://docs.oracle.com/javase/8/docs/api/java/time/temporal/TemporalAdjusters.html)**


 | 


```
package es.usantatecla.a0\_itinerario.a6\_packages.a3\_localDateTime;

import java.time.Duration;
import java.time.LocalDate;
import java.time.LocalDateTime;
import java.time.LocalTime;
import java.time.Month;
import java.time.Period;
import java.time.ZoneId;
import java.time.ZonedDateTime;
import java.time.format.DateTimeFormatter;
import java.time.temporal.ChronoUnit;
import java.time.temporal.TemporalAdjusters;

class App {

  public static void main(String[] args) {
    trace(LocalDate.of(1, 2, 3));
    trace(LocalDate.of(1, Month.FEBRUARY, 3));
    trace(LocalDate.parse("0001-02-03"));

    trace(LocalTime.of(4, 5, 6));
    trace(LocalTime.of(4, 5));
    trace(LocalTime.parse("04:05:06"));
    trace(LocalTime.parse("04:05"));

    trace(LocalDateTime.parse("0001-02-03T04:05:06"));
    trace(LocalDateTime.parse("0001-02-03T04:05"));
    trace(LocalDateTime.of(LocalDate.parse("0001-02-03"), LocalTime.parse("04:05")));

    LocalDateTime now = LocalDateTime.now();
    trace("now in Paris: " + ZonedDateTime.of(now, ZoneId.of("Europe/Paris")));
    trace("now in Paris: " + ZonedDateTime.parse("0001-02-03T04:05:06+01:00[Europe/Paris]"));

    trace("now: " + now);
    trace("now: " + now.toLocalDate());
    trace("now: " + now.toLocalTime());
    trace("tomorrow: " + now.plusDays(1));
    trace("tomorrow: " + now.plus(Period.ofDays(1)));
    trace("tomorrow: " + now.plus(1, ChronoUnit.DAYS));
    trace("next year: " + now.plusYears(1));
    trace("hour ago: " + now.minusHours(1));
    trace("hour ago: " + now.minus(1, ChronoUnit.HOURS));
    trace("hour ago: " + now.minus(Duration.ofHours(1)));

    LocalDateTime tomorrow = now.plusDays(1);
    trace("horas: " + Duration.between(now, tomorrow).toHours());
    trace("horas: " + ChronoUnit.HOURS.between(now, tomorrow));
    trace("dias: " + Period.between(now.toLocalDate(), tomorrow.toLocalDate()).getDays());
    trace("dias: " + ChronoUnit.DAYS.between(now, tomorrow));

    trace("now-firstDayOfMonth: " + now.with(TemporalAdjusters.firstDayOfMonth()));
    trace("now-lastDayOfYear: " + now.with(TemporalAdjusters.lastDayOfYear()));
    trace("now-getDayOfWeek: " + now.getDayOfWeek());
    trace("now-getDayOfWeek: " + (now.getDayOfWeek().ordinal() + 1));
    trace("now-getDayOfMonth: " + now.getDayOfMonth());
    trace("now is before plus second: " + now.isBefore(now.plusSeconds(1)));
    trace("now is after minus second: " + now.isAfter(now.minusSeconds(1)));

    trace("now isLeapYear " + now.getYear() + "? " + LocalDate.now().isLeapYear());
    trace("2000 isLeapYear " + 2000 + "? " + LocalDate.of(2000, 2, 29).isLeapYear());
    trace("2001 isLeapYear " + 2001 + "? " + LocalDate.of(2001, 2, 28).isLeapYear());

    trace("now: " + now.format(DateTimeFormatter.ofPattern("yyyy/dd/MM")));
    trace("now: " + now.format(DateTimeFormatter.ofPattern("yyyy/MM/dd")));
    trace("now: " + now.format(DateTimeFormatter.ofPattern("yyyy/MM/dd - hh:mm:ss")));
    trace("now: " + now.format(DateTimeFormatter.ofPattern("yyyy/MM/dd - HH:mm")));
    trace("now: " + now.format(DateTimeFormatter.ofPattern("yyyy/MM ")));
  }

  private static void trace(Object object) {
    Console.instance().writeln(object);
  }

}
```


 |


---

[Volver al nivel superior](../README.md)

