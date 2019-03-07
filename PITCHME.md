# Software Engineering
by Daniel Glinka
---

# Programmieren

+++

## Aufbau

- Abfolge von Anweisungen
- "Rezept"

+++

### Beispiel (Java)

```Java
nameAnweisung1();
nameAnweisung2(parameter);
nameAnweisung3(parameter1, parameter2);

nameAnweisung4(); nameAnweisung5(); 
```

+++

### Beispiel (Java)

```java
print("Hallo "); print("Welt!");

```
### Beispiel (Python)

```python
print("Hallo ")
print("Welt!")

```
+++

Alle Anweisungen findet man [hier](https://processing.org/reference/)

---

# Processing

+++

- Basiert auf Java
- [https://processing.org](https://processing.org/)
- [Referenz](https://processing.org/reference/)

+++

![Processing UI](assets/img/Processing_UI.png)

---

# Übungen

+++

## Weihnachtsbaum

Schreibe ein Programm, das das folgende Muster in der Konsole ausgibt:

```bash
      *
     ***
    *****
   *******
  *********
 ***********
*************
     ***
```

+++

##### Tipp:
- Es gibt 2 Anweisungen, mit denen Text in der Konsole ausgegeben wird.
- Sternchen und Leerzeichen helfen weiter ;-)

+++

## Perlenkette

Programmiere das angegebene Bild mithilfe der grafischen Grundelemente von Processing:

![Perlenkette](assets/img/Perlenkette.png)

+++

##### Tipp:
- Lies den Ellipsen Befehl in der Referenz nach
- Du kannst die Bildschirmgröße mit `size(x,y)` festlegen

+++

## Grafische Elemente

```java
// Die Größe des grafischen Ausgabefensters wird auf 450 Pixel
// in der Breite und 320 Pixel in der Höhe festgelegt.
// Die Hintergrundfarbe ist weiß.
size(450, 320);
background(255);

// Die grafischen Grundelemente im angegebenen Bild werden von links
// nach rechts gezeichnet. Dazu muss für jedes Element zuvor die
// Füllfarbe und Linienfarbe spezifiziert werden.

// Das rote Rechteck
stroke(255, 0, 0);         // Linienfarbe ist blau
fill(255, 0, 0);           // Füllfarbe ist blau
rect(10, 10, 100, 300);

// Der grüne Kreis
stroke(0, 255, 0);
fill(0, 255, 0);
ellipse(200, 160, 100, 100);

// Die blaue Linie
strokeWeight(10);          // Strichstärke auf 10 Pixel setzen
stroke(0, 0, 255);
line(310, 10, 310, 300);

// Das gelbe Dreieck
strokeWeight(1);
stroke(255, 255, 0);
fill(255, 255, 0);
triangle(400, 10,          // Punkt oben
         370, 310,         // Punkt unten links
         440, 310);        // Punkt unten rechts

```
+++

## Ghettoblaster

Programmiere in Processing die Zeichnung eines Ghettoblasters. Er soll in dieser Form gestaltet werden:

![Ghettoblaster](assets/img/Ghettoblaster.png)

+++

##### Tipp:
- Erstelle eine Skizze mit Koordinatensystem (Nullpunkt ist oben links)

## Ghettoblaster Lösung

```java
size(400, 400);
background(255);

// Henkel
// Schwarze Fläche mit Rundungen oben
stroke(0);
strokeWeight(5);
fill(0);
rect(75, 45, 250, 65, 15, 15, 0, 0);

// Weiße Fläche ohne Rundungen
noStroke();
fill(255);
rect(85, 65, 230, 50);

// Körper (300x100 Pixel groß)
stroke(0);
fill(217);
rect(50, 100, 300, 180, 15);

// Frequenzanzeiger
// graue Grundfläche (280x40 Pixel)
fill(89);
noStroke();
rect(60, 120, 280, 40, 10);

// oranges Display links
fill(219, 106, 28);
rect(80, 125, 60, 30);

// weiße Frequenzlinien rechts
stroke(255);
strokeCap(SQUARE);
strokeWeight(2);
line(160, 138, 320, 138);
line(160, 142, 320, 142);

// grauer Trenner darunter
stroke(89);
strokeWeight(4);
line(75, 170, 330, 170);

// Blaue Lautsprecherboxen
stroke(65, 91, 139);
fill(90, 126, 187);
strokeWeight(10);

// X-Mitte der Box
// = 300 (Breite)/2 + 50 (X-Startposition)
// = 200
// Linke X-Hälftenmitte also 300/4+50 = 125
// Y-Mitte der Box: 180/2+100=190
// Linke untere Y-Hälftenmitte: 180/4*3+100=235
ellipse(125, 225, 80, 80);
ellipse(275, 225, 80, 80);
```
