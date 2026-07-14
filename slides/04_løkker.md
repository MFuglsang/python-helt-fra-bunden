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

# Modul 04: Løkker 🔄

**Gentag kode uden at skrive det igen!**

---

## Hvad er en Løkke?

**Gør det samme mange gange**

```
Uden løkke (kedeligt):
print('*')
print('*')
print('*')
print('*')
print('*')

Med løkke (smart!):
for i in range(5):
    print('*')
```

---

## range() Funktion

```
range(5)      → 0, 1, 2, 3, 4
range(1, 6)   → 1, 2, 3, 4, 5
range(0, 10, 2) → 0, 2, 4, 6, 8
```

**Notation:**
- `range(stop)`
- `range(start, stop)`
- `range(start, stop, step)`

---

## for Løkke

```python
for i in range(5):
    print(i)
```

**Output:**
```
0
1
2
3
4
```

**I betyder:** "for hver værdi i range(5)"

---

## Tegn Mønstre

```python
# Pyramide
for i in range(1, 6):
    print('*' * i)
```

**Output:**
```
*
**
***
****
*****
```

---

## Kombinér med if

```python
for i in range(1, 11):
    if i % 2 == 0:
        print(str(i) + ' er lige')
```

**Output:** Finder alle lige tal 2-10

---

## Indentation - Vigtig! ⚠️

```python
for i in range(3):
    print('Denne køres 3 gange')  ← indentation!
    
print('Dette køres 1 gang')  ← uden indentation
```

**Regel:** Alt der skal gentages **skal være rykket ind**

---

## Flowchart

```
  for i in range(5):
    ↓
  i = 0? Gør blok
  i = 1? Gør blok
  i = 2? Gør blok
  i = 3? Gør blok
  i = 4? Gør blok
    ↓
  Færdig
```

---

## Øvelser

**1. Gangetabel**
```python
for i in range(1, 11):
    print(str(i) + ' * 5 = ' + str(i * 5))
```

**2. Trekant**
```python
for i in range(1, 6):
    print(i)
```

---

## Noter for Lærer

**Timing:** ~60 minutter

**Key koncept:** Løkker = automatisering

**Vigtige pointer:**
- range() starter fra 0 normalt
- Indentation er KRITISK
- Kombiner med if for filtrering
