# Software Engineering
by Daniel Glinka
---

# Variablen

- Platzhalter
- Programme dynamisch gestalten
- Reservierter Speicherbereich
- Bezeichner kann selbst gewählt werden

+++

## Aufbau

- Name (Bezeichner)
- Typ (interne Darstellung)
- (Adresse) (wo im Speicher)
- Wert (variabel)

+++

## Im Speicher

![Variable im Speicher](assets/img/Variablen_Speicher.png)

+++

## Konventionen

- sprechende Namen
- keine Umlaute
- in der Regel auf Englisch
- Programmiersprache spezifische Konventionen ([Java](https://www.oracle.com/technetwork/java/codeconventions-135099.html))
___

# Datentypen

+++

- Java ist eine streng typisierte Sprache
- Jede Variable hat genau einen Datentyp
- Ein festgelegter Datentyp kann nicht geändert werden
- Gibt an, wie die Daten gespeichert werden
- Legt Wertebereich fest

+++

```java
// Datentyp Integer (Ganzzahlen) => int
int x = 10;

// Datentyp String (Zeichenkette) => String
String x = "10";

int x = "10"; // ERROR!
int x = abc;  // ERROR!

int x = 25;   // x hat den Wert 25
x = 10;       // x hat den neuen Wert 10
x = "15";     // ERROR!
```
+++

## Wertebereich

boolean (1b) < byte (1B) < char (1B) < short (2B) < int (4B) < float (4B) long (8B) < double (8B)

```java
byte x = 127 // x hat den Wert 127
x = 128      // ERROR! => Overflow
```

+++

## Beispiel mit C

##### Code
```c
#include "stdio.h"
int main() {
  char x = 127;
  printf("x = %d\n", x);

  x = x + 1;
  printf("x = %d\n", x);

  return 0;
}
```

##### Output
```bash
x = 127
x = -128
```

+++

## Overflow in Binär

##### Zahlen in Binär (byte/char)
```
-128 = 1000 0000
-1   = 1000 0001 
 0   = 0000 0000
 1   = 0000 0001
 127 = 0111 1111
```
##### Rechnen in Binär
```
+ = Bitweises OR (|)

    0111 1111
  | 0000 0001 
  -----------
    1000 0000
```
