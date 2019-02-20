# Software Engineering
by Daniel Glinka
---
## Über mich

```Java
function setup() {
  string name = "daniel"
  int alter = 26
  string beruf = "software ingenieur"
  string twitter = "@k4itsh"
  string github = "github.com/kaitsh"
}
```

---
# Inhalte

+++

* Aufbau von Rechnern
  ** CPU
  ** RAM

* Wie rechnet eine CPU
  ** Bit/Byte
  ** ALU

+++

* Zeichencodierungen

+++

* Programmierung
  ** Variablen, Operatoren
  ** Kontrollstrukturen
  ** Funktionen
  ** Datenstrukturen

+++

* Vorschläge?

---

# Aufbau von Rechnern

+++

## Erwartungen an Computer

+++

* Datenverarbeitung
* Lösen von komplexen Aufgaben
* Ein/Ausgabe
* Betriebssystem ermöglicht Basisfunktionalitäten

+++

## Aufbau

+++

* CPU (Central Processing Unit) + FPU (Floating Point Unit)
* ROM (Read Only Memory)
* RAM (Random Access Memory)
* System-Bus
* Verschiedene Controller

+++

## CPU

+++
* Lädt Information/Befehle aus Hauptspeicher und führt sie aus
* Kontrolliert alle Aktionen

---

## Information - Daten

+++

* Information --> Abstraktion (Daniel Glinka)
* Daten --> Representation (01000100011000010110111001101001011001010110110000100000011001110110110001101001011011100110101101100001)

* Information = (Daten + Meta Data)

+++

## Bit

* Binary Digit
* Basiseinheit
* hat 2 Zustände (an - aus, 0 - 1, true - false, ...)

+++

## Bitstring

* Array von Bits
* Computer arbeitet ausschließlich mit Bitstrings
* 32 Bit Architektur, 64 Bit Architektur,... (bus width)

+++

## Bytes

* 1 Byte (B) = 8 Bit (b)

* File = langer byte string
* Datei mit 756 B = 6048 b

+++

| Name | Symbol | Wert               |
| ---- | -----  | ----               |
| kibi | Ki     | 1024^1 = 1 024     |
| mebi | Mi     | 1024^2 = 1 048 576 |
| gibi | Gi     | 1024^3 = ...       |
| tebi | Ti     | ...                |
| pebi | Pi     |                    |
| exbi | Ei     |                    |
| zebi | Zi     |                    |
| yobi | Yi     |                    |

+++

512 GB Festplatte => 512*10^9 Bytes, aber!
512 GB / 1024 / 1024 / 1024 = 476 GiBytes

---

## Boolsche Algebra

Wie rechnet eine CPU?
