---
marp: true
theme: default
style: |
  section {
    font-family: 'Arial', sans-serif;
    background: #f5f5f5;
  }
  h1 {
    color: #2c3e50;
  }
  code {
    background: #fffacd;
    padding: 2px 6px;
    border-radius: 3px;
  }
  pre {
    background: #2c3e50;
    color: #ecf0f1;
    padding: 15px;
    border-radius: 5px;
  }
---

# Modul 05: Funktioner 🛠️

**Genbrugbar kode - dine egne kommandoer!**

---

## Hvad er en Funktion?

**En opskrift du kan bruge igen og igen**

```
Rigtig opskrift:
├─ Navn: "Lav smørrebrød"
├─ Input: brød, smør, pølse
└─ Output: lækker sandwich

Python-funktion:
def lav_smørrebrød():
    ...
```

---

## Simpel Funktion

```python
def hilsen():
    print('Hej verden!')

# Kald funktionen
hilsen()
hilsen()
hilsen()
```

**Output:** `Hej verden!` - tre gange!

---

## Funktion med Parameter

```python
def hilsen(navn):
    print('Hej ' + navn)

hilsen('Anna')    # Hej Anna
hilsen('Bert')    # Hej Bert
```

**Parameter:** Data vi sender til funktionen

---

## return Værdi

```python
def add(a, b):
    return a + b

resultat = add(5, 3)
print(resultat)  # 8
```

**return:** Giv værdi tilbage til kalderen

---

## Flere Parameters

```python
def beskrivelse(navn, alder, by):
    print(navn + ' er ' + str(alder) + ' år og bor i ' + by)

beskrivelse('Maria', 12, 'København')
```

---

## Funktion i Funktion

```python
def mult(a, b):
    return a * b

def double(n):
    return mult(n, 2)

print(double(5))  # 10
```

**Funktioner kan kalde andre funktioner!**

---

## Flowchart

```
  def funktions_navn(parameter):
    ↓
  Gør noget med parameter
    ↓
  return resultat
    ↓
  Returnerer til kalderen
```

---

## Eksempel: Areal af Cirkel

```python
import math

def areal_cirkel(radius):
    resultat = math.pi * radius * radius
    return resultat

areal = areal_cirkel(5)
print(areal)  # 78.5...
```

---

## Noter for Lærer

**Timing:** ~60 minutter

**Key koncept:** Funktioner = genbrugbar kode

**Vigtige pointer:**
- `def` definerer
- `()` kalder
- `return` giver resultat tilbage
- Parameters sender data ind
