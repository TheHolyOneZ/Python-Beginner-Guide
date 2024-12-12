### **Python-Anfängerkurs - Komplettes Handbuch**

#### **Inhaltsverzeichnis**

1. Einführung in Python
2. Grundlagen der Programmierung
3. Kontrollstrukturen
4. Funktionen
5. Datenstrukturen
6. Objektorientierte Programmierung (OOP)
7. Fehlerbehandlung
8. Dateien und Dateisystem
9. Module und Bibliotheken
10. Projekte und Anwendungen
11. Weiterführende Themen
12. Zusatzthemen: Reguläre Ausdrücke, Debugging, und Best Practices

---

### **1. Einführung in Python**

#### **Was ist Python?**

Python ist eine einfach zu erlernende, vielseitige und beliebte Programmiersprache. Sie wird in verschiedenen Bereichen eingesetzt, z. B. in der Webentwicklung, Datenanalyse, KI, Automatisierung und mehr.

#### **Vorteile von Python:**

- Leicht zu lesen und zu schreiben
- Umfangreiche Standardbibliothek
- Plattformübergreifend
- Aktive Community

#### **Installation von Python**

1. **Download**: Lade Python von [python.org](https://www.python.org/) herunter.
2. **Installation**: Folge den Anweisungen. Aktiviere „Add Python to PATH“.
3. **Prüfen**: Öffne das Terminal und gib `python --version` ein.

#### **IDE-Empfehlungen:**

- **VSCode**: Flexibel und anpassbar.
- **PyCharm**: Voll ausgestattet für Python.
- **Jupyter Notebook**: Für Datenanalyse und wissenschaftliches Rechnen.

**Erstes Programm:**

```python
print("Hallo Welt!")
```

---

### **2. Grundlagen der Programmierung**

#### **Variablen und Datentypen**

Variablen sind Speicher für Daten. Beispiele für Datentypen:

| Typ     | Beschreibung   | Beispiel        |
| ------- | -------------- | --------------- |
| Integer | Ganze Zahlen   | `42`            |
| Float   | Dezimalzahlen  | `3.14`          |
| String  | Text           | `'Hallo'`       |
| Boolean | Wahrheitswerte | `True`, `False` |

**Beispiel:**

```python
name = "Alice"  # String
alter = 25       # Integer
pi = 3.14        # Float
ist_student = True  # Boolean
print(f"Name: {name}, Alter: {alter}, Student: {ist_student}")
```

#### **Eingaben und Ausgaben**

- **Eingabe:** `input()`
- **Ausgabe:** `print()`

**Beispiel:**

```python
benutzername = input("Wie heißt du? ")
print(f"Hallo, {benutzername}!")
```

---

### **3. Kontrollstrukturen**

#### **Bedingungen (`if`, `elif`, `else`)**

**Beispiel:**

```python
zahl = int(input("Gib eine Zahl ein: "))
if zahl > 0:
    print("Die Zahl ist positiv.")
elif zahl < 0:
    print("Die Zahl ist negativ.")
else:
    print("Die Zahl ist null.")
```

#### **Schleifen**

- **`for`-Schleife:** Iteriert über eine Sequenz.
- **`while`-Schleife:** Wiederholt, solange eine Bedingung wahr ist.

**Beispiele:**

```python
# for-Schleife
for i in range(1, 6):
    print(f"Zahl: {i}")

# while-Schleife
x = 5
while x > 0:
    print(x)
    x -= 1
```

---

### **4. Funktionen**

#### **Definition von Funktionen**

**Beispiel:**

```python
def begruessung(name):
    print(f"Hallo {name}!")

begruessung("Anna")
```

#### **Rückgabewerte**

```python
def addiere(a, b):
    return a + b

resultat = addiere(5, 7)
print(f"Die Summe ist: {resultat}")
```

---

### **5. Datenstrukturen**

#### **Listen**

Listen sind geordnete Sammlungen.

**Beispiele:**

```python
zahlen = [1, 2, 3, 4, 5]
zahlen.append(6)  # Element hinzufügen
zahlen.remove(2)  # Element entfernen
print(zahlen)
```

#### **Wörterbücher (Dictionaries)**

**Beispiel:**

```python
student = {"name": "Lisa", "alter": 22}
print(student["name"])
```

---

### **6. Objektorientierte Programmierung (OOP)**

#### **Klassen und Objekte**

**Beispiel:**

```python
class Auto:
    def __init__(self, marke, modell):
        self.marke = marke
        self.modell = modell

    def beschreibung(self):
        return f"{self.marke} {self.modell}"

mein_auto = Auto("Tesla", "Model 3")
print(mein_auto.beschreibung())
```

---

### **7. Fehlerbehandlung**

#### **`try` und `except`**

**Beispiel:**

```python
try:
    zahl = int(input("Gib eine Zahl ein: "))
    print(f"Das Doppelte ist: {zahl * 2}")
except ValueError:
    print("Bitte eine gültige Zahl eingeben!")
```

---

### **8. Dateien und Dateisystem**

#### **Lesen und Schreiben von Dateien**

**Beispiel:**

```python
# Schreiben
with open("beispiel.txt", "w") as datei:
    datei.write("Hallo Datei!")

# Lesen
with open("beispiel.txt", "r") as datei:
    inhalt = datei.read()
    print(inhalt)
```

---

### **9. Projekte und Anwendungen**

#### **Projekt 1: Taschenrechner**

```python
def addiere(a, b):
    return a + b

def subtrahiere(a, b):
    return a - b

while True:
    print("1: Addieren, 2: Subtrahieren, 3: Beenden")
    auswahl = input("Wähle: ")
    if auswahl == "3":
        break
    zahl1 = float(input("Erste Zahl: "))
    zahl2 = float(input("Zweite Zahl: "))
    if auswahl == "1":
        print(addiere(zahl1, zahl2))
    elif auswahl == "2":
        print(subtrahiere(zahl1, zahl2))
```

#### **Projekt 2: Zahlenratespiel**

```python
import random
geheime_zahl = random.randint(1, 100)
while True:
    tipp = int(input("Rate die Zahl: "))
    if tipp < geheime_zahl:
        print("Zu niedrig!")
    elif tipp > geheime_zahl:
        print("Zu hoch!")
    else:
        print("Richtig!")
        break
```

---

### **10. Weiterführende Themen**

#### **Datenanalyse mit pandas und numpy**

- **pandas**: Eine Bibliothek zur Datenmanipulation und -analyse.
- **numpy**: Eine leistungsstarke Bibliothek für numerische Berechnungen.

**Beispiel:**

```python
import pandas as pd
import numpy as np

# Daten mit numpy erstellen
daten = np.random.rand(5, 3)

# Daten in pandas DataFrame umwandeln
df = pd.DataFrame(daten, columns=["A", "B", "C"])
print(df)
```

#### **Visualisierung mit matplotlib**

- **matplotlib**: Bibliothek zur Erstellung von Diagrammen und Visualisierungen.

**Beispiel:**

```python
import matplotlib.pyplot as plt

# Daten
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

# Diagramm erstellen
plt.plot(x, y, marker="o")
plt.title("Beispielplot")
plt.xlabel("x-Achse")
plt.ylabel("y-Achse")
plt.show()
```

#### **Webentwicklung mit Flask/Django**

- **Flask**: Ein leichtgewichtiges Webframework.
- **Django**: Ein vollständiges Webframework.

**Flask-Beispiel:**

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hallo, Welt!"

if __name__ == "__main__":
    app.run(debug=True)
```

#### **GUIs erstellen mit tkinter**

- **tkinter**: Eine Standardbibliothek zur Erstellung von grafischen Oberflächen.

**Beispiel:**

```python
import tkinter as tk

# Fenster erstellen
root = tk.Tk()
root.title("GUI Beispiel")

# Label hinzufügen
label = tk.Label(root, text="Hallo, GUI!")
label.pack()

# Button hinzufügen
button = tk.Button(root, text="Beenden", command=root.quit)
button.pack()

# Hauptloop starten
root.mainloop()
```

---

### **11. Zusatzthemen: Reguläre Ausdrücke, Debugging und Best Practices**

#### **Reguläre Ausdrücke (Regex)**

Reguläre Ausdrücke helfen bei der Verarbeitung von Textmustern.

**Beispiel:**

```python
import re

text = "Meine Telefonnummer ist 123-456-7890."
muster = r"\d{3}-\d{3}-\d{4}"
match = re.search(muster, text)
if match:
    print(f"Gefundene Nummer: {match.group()}")
```

#### **Debugging**

- Nutze `print()`-Anweisungen, um Variablen zu überprüfen.
- Verwende `pdb`, den Python-Debugger.

**Beispiel:**

```python
import pdb

x = 10
y = 0
pdb.set_trace()
result = x / y
```

#### **Best Practices**

- Schreibe klaren, gut dokumentierten Code.
- Nutze Versionskontrolle (z. B. Git).
- Schreibe Tests für deinen Code.

**Beispiel:**

```python
def quadrat(x):
    """Berechnet das Quadrat einer Zahl."""
    return x * x

assert quadrat(3) == 9
assert quadrat(-4) == 16
```

