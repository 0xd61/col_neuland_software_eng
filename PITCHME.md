# Software Engineering
by Daniel Glinka
---

# Kontrollstrukturen

+++

- Abläufe steuern
- geben an, in welcher Reihenfolge und wie oft Anweisungen ausgeführt werden
- Bedingte Anweisungen
  - Code wird nur unter bestimmten Bedingungen ausgeführt
- Wiederholungsanweisungen
  - Code wird mehrfach ausgeführt
  
---

## Bedingte Anweisungen

- `if-else` Anweisung
  - Unterscheidet 2 Fälle (wenn "x", dann "y", _sonst "z"_)
- `switch` Anweisung
  - Unterscheided 3 oder mehr Fälle

+++

### if-else

```java
// Recap: Boolsche Ausdrücke ergeben immer true oder false (x == y, a <= b, etc.)
if(<boolescherAusdruck>) {
  // In diesen geklammerten Block kommen alle die Anweisungen hinein,
  // die abgearbeitet werden, wenn die Bedingung wahr ist.
}
else {
  // In diesen geklammerten Block kommen alle Anweisungen hinein,
  // die abgearbeitet werden, wenn die Bedingung falsch ist.
}
```

`else` ist optional. Wenn dieser Block nicht benötigt wird, kann man ihn komplett weg lassen.

+++

### switch

```java
switch(<Ausdruck>) {
  case <Konstante_1>:
    <Anweisungsblock_1>;
    break;
  case <Konstante_2>:
    <Anweisungsblock_2>;
    break;
  ...
  case <Konstante_n>:
    <Anweisungsblock_n>;
    break;
  default:
    <Anweisungsblock_sonst>;
}
```

`break` beendet die Ausführung der umgebenden Struktur sofort. Wird ein `break` vergessen, werden die nächsten Anweisungsblöcke bis zum nächsten `break` bzw. Ende der `switch`-Anweisung auch ausgeführt.

`default` beschreibt den "sonst"-Fall und ist optional. Allerdings ist es gute Praxis, immer einen `default` zu haben.

---

## Wiederhohlungsanweisungen (Schleifen)

+++

- `for`-Schleife
  - "Kopfgesteuerte"-Schleife
- `while`-Schleife
  - "Kopfgesteuerte"-Schleife
  - "Fußgestuerte"-Schleife

+++

### for-Schleife

```java
for(int i=1; i<10; i++) {
  // In diesen geklammerten Block kommen alle die Anweisungen hinein,
  // die wiederholt abgearbeitet werden sollen.
}
```

Eine Endlosschleife erhält man mit `for (;;){// Anweisungen}`. Dies ist allerdings in den meisten Fällen unerwünscht.

+++

### while-Schleife (Kopfgesteuert)

```java
int i = 0;
while(i<10) {
  // Anweisungen, die abgearbeitet werden sollen
  i++;
}
```

Eine Endlosschleife erhält man mit `while(true){// Anweisungen}`.

+++

### while-Schleife (Fußgesteuert)

```java
int i = 0;
do {
  // Anweisungen, die abgearbeitet werden sollen
  i++;
} while(i<10)
```

Eine Endlosschleife erhält man mit `do {// Anweisungen} while(true)`.

+++

`break` funktioniert auch bei allen Schleifen. Das bedeutet, bei einem `break` macht das Programm mit der nächsten Zeile außerhalb der Schleife weiter.

`continue` ist ein Schlüsselwort, das nur in Schleifen erlaubt ist. Bei `continue` wird der aktuelle Durchlauf beendet und ein "neuer" Durchlauf gestartet. Bei der `for`-Schleife wird "Aktualisierungs"-Anweisung noch ausgeführt.

---

## Übungen

+++

### Maximum bestimmen
