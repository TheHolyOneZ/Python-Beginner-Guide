# **Python-Leitfaden 2024**

## Inhaltsverzeichnis
1. [Interaktive Beispiele](#interaktive-beispiele)
2. [Praxisanwendungen](#praxisanwendungen)
3. [Übungsaufgaben](#übungsaufgaben)
4. [Häufige Fehler](#häufige-fehler)
5. [Moderne Python-Funktionen](#moderne-python-funktionen)
6. [Testen](#testen)
7. [Entwicklungsumgebung](#entwicklungsumgebung)
8. [Versionskontrolle](#versionskontrolle)
9. [Optimierung](#optimierung)

## Interaktive Beispiele


py.md
def interaktives_beispiel():
    name = input("Gib deinen Namen ein: ")
    print(f"Hallo {name}, lass uns gemeinsam Python lernen!")

# Direktes Ausführen zum Testen
if __name__ == "__main__":
    interaktives_beispiel()


interactive.py
## Praxisanwendungen

### Einkaufswagen-Beispiel


py.md
def einkaufswagen_beispiel():
    warenkorb = []
    preise = {
        "apfel": 0.50,
        "banane": 0.30,
        "orange": 0.60
    }
    
    while True:
        artikel = input("Artikel hinzufügen (oder 'fertig' zum Bezahlen): ")
        if artikel == "fertig":
            break
        warenkorb.append(artikel)
        
    gesamt = sum(preise[artikel] for artikel in warenkorb)
    print(f"Gesamtbetrag: {gesamt:.2f}€")


shopping.py
## Übungsaufgaben

### Aufgabe 1: Palindrom-Prüfer
Erstelle eine Funktion, die prüft, ob ein Wort ein Palindrom ist.

### Aufgabe 2: Banksystem
Implementiere ein einfaches Banksystem mit OOP.

### Aufgabe 3: Aufgabenliste
Erstelle einen Kommandozeilen-Aufgabenmanager.

## Häufige Fehler

### 1. Veränderbare Standardargumente


py.md
# Falsch
def funktion(liste=[]):
    liste.append(1)
    return liste

# Richtig
def funktion(liste=None):
    if liste is None:
        liste = []
    liste.append(1)
    return liste


mistakes.py
## Moderne Python-Funktionen


py.md
# Typ-Hinweise
def begrüßung(name: str) -> str:
    return f"Hallo {name}"

# Walrus-Operator
def beispiel_walrus():
    if (n := len([1, 2, 3])) > 2:
        print(f"Liste hat {n} Elemente")


modern.py
## Entwicklungsumgebung

### Virtuelle Umgebung einrichten


py.md
python -m venv umgebung


source umgebung/bin/activate  # Unix


umgebung\Scripts\activate  # Windows


### Paketverwaltung


py.md
pip install -r anforderungen.txt


## Versionskontrolle


py.md
git init


git add .


git commit -m "Erste Python-Projekt Einrichtung"


## Optimierung


py.md
from timeit import timeit
from typing import List

def optimierungs_beispiel():
    # Vergleich: Listenerstellung
    zahlen: List[int] = list(range(1000))
    
    def mit_schleife():
        quadrate = []
        for n in zahlen:
            quadrate.append(n ** 2)
            
    def mit_listenverständnis():
        quadrate = [n ** 2 for n in zahlen]
        
    # Zeitmessung
    schleifenzeit = timeit(mit_schleife, number=1000)
    verständniszeit = timeit(mit_listenverständnis, number=1000)
    
    print(f"Schleife: {schleifenzeit:.4f} Sekunden")
    print(f"Listenverständnis: {verständniszeit:.4f} Sekunden")