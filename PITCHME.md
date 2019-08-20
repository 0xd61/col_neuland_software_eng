# Software Engineering

## by Daniel Glinka

---

# Arrays

- [Referenz](https://processing.org/reference/Array.html)

+++

## Eigenschaften

- Datentyp
- Speichert eine Menge von Werten
- Elemente haben gleichen Datentyp
- Werte werden mittels Index abgeändert oder abgefragt
- Ein Index startet bei 0

+++

### Beispiel

```java
koordinaten[3] = wert;

wert = koordinaten[3];
```

+++

### Variabler Index

```java
for(int i=0; i < anzahlWerte; i++) {
  koordinaten[i] = initialerWert;
}
```

+++

## Deklaration/Speicher Allokierung

- Erstellt einen neuen Array
- Gibt den Datentyp des Arrays vor
- Anders als bei bisher bekannten Datentypen muss für Arrays Speicher
  reserviert/allokiert werden

+++

### Beispiel

```java
int[] koordinaten; // Deklaration

// Speicher Allokierung mit 15 Elementen
// Danach hat jedes der Elemente den Wert 0
koordinaten = new int[15];

int[] koordinaten = new int[15]; // alles in einem Schritt

// Deklaration und Allokierung mit festgelegten Werten
String[] farben = {"rot", "gelb", "grün"}
```

+++

## Dimensionen

- Arrays können mehrere Dimensionen haben
- z.B. Koordinaten mit x und y

```java
// Zweidimensionaler Array
int[][] koordinaten = new int[anzahlX][anzahlY]
```

+++

## Länge

- ein Array hat automatisch die Eigenschaft `length`

```java
int anzahlElemente = koordinaten.length;
```

---

# Übungen

+++

## Tankfüllung

Schreibe eine Funktion, die ein Array mit verschiedenen `int`-Werten übergeben
bekommt und daraus die durchschnittliche Anzahl an Kilometern zurückgibt, die
wir mit einer Tankfüllung fahren können.

```
[123, 134, 120, 122] -> 124.75
```

+++

###### Tipps

- Summiere alle Kilometer
- Berechne den Mittelwert (Summe / Anzahl der Werte)
- Achte auf die richtigen Datentypen

+++

###### Hilfe

```java
// Funktion zur Berechnung des durchschnittlichen Verbrauchs
// An die Funktion wird ein Array mit Integer-Werten übergeben,
// die die gefahrenen Kilometer bis zum nächsten Tankstopp
// enthalten. Die Funktion gibt den Durchschnittswert als
// Fließkommazahl zurück.

// Erstelle eine Funktion averageFuelComsumption welche den Array
// kilometersPerTankful als Parameter erhält
/* ... */

  // Initialisierung der Variablen averageConsumption und
  // sumKilometers für die Berechnung des Mittelwerts
  /*...*/

  // Summiere alle Kilometer
  /*...*/

  // Teile durch Gesamtzahl
  /*...*/

  // Rückgabe des Ergebnisses
  /*...*/

// Startpunkt des Hauptprogramms
// Hier wird die implementierte Funktion zu Demonstrations- und
// Testzwecken aufgerufen.

// Erstelle die Funktion setup, welche das Ergebnis der
// Funktion averageFuelComsumption in der Console ausgibt
/*...*/
```

+++

## Rückwärtsausgabe

Programmiere eine Funktion, welche Wörter rückwärts schreibt. Dabei soll ihr ein
Char-Array übergeben werden, welcher die Buchstaben rückwärts in der Konsole ausgiebt.

z.B. Hallo -> ollaH

+++

##### Tipps

- du kannst den Array rückwärts oder vorwärts durchgehen. Beim letzteren
  benötigst du wahrscheinlich eine Hilfsvariable.
- jeder Array hat eine `length` Variable ([Referenz](https://processing.org/reference/Array.html))

+++

##### Hilfe

```java
// Programmiere die Funktion printBackwards, welche keinen Rückgabewert
// hat und als Parameter einen char-Array erhält.
// Die Funktion soll den übergeben char-Array in der
// umgekehrten Reihenfolge in der Konsole ausgeben.
/*...*/

// Startpunkt des Hauptprogramms
// Hier wird die implementierte Funktion zu Demonstrations- und
// Testzwecken aufgerufen.
void setup() {
  // Char Array mit Test Daten
  char[] palindrom =
    {'r', 'e', 'i', 'b', 'n', 'i', 'e', 'e', 'i', 'n', 'b', 'i', 'e', 'r'};

  // Char Array mit Test Daten
  char[] test = {'H', 'a', 'l', 'l', 'o'};

  // Hier wird die Funktion printBackwards mit dem entsprechenden Parameter aufgerufen
  printBackwards(palindrom);
  printBackwards(test);
}
```
