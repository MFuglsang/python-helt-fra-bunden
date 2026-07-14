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

# Modul 06: Lister 📋

**Gem mange ting i én variabel!**

---

## Hvad er en Liste?

**Samling af mange data på samme sted**

```python
frugter = ['æble', 'banan', 'appelsin']
karakterer = [10, 7, 12, 4, 9]
```

**Notation:** `[]` kvadratiske parenteser

---

## Indeksering

```
liste = ['æble', 'banan', 'kirsebær']
index:    0       1         2

liste[0] → 'æble'
liste[1] → 'banan'
liste[2] → 'kirsebær'
liste[-1] → 'kirsebær' (sidste)
```

**Python tæller fra 0!**

---

## Løkke gennem Liste

```python
frugter = ['æble', 'banan', 'appelsin']

for frugt in frugter:
    print('Jeg holder af ' + frugt)
```

**Output:**
```
Jeg holder af æble
Jeg holder af banan
Jeg holder af appelsin
```

---

## Liste-Metoder

### .append() - Tilføj
```python
kurv = ['milk', 'brød']
kurv.append('smør')
# Nu: ['milk', 'brød', 'smør']
```

### .remove() - Fjern
```python
kurv.remove('milk')
# Nu: ['brød', 'smør']
```

---

## len() - Længde

```python
frugter = ['æble', 'banan', 'appelsin']
antal = len(frugter)
print(antal)  # 3
```

**Hvor mange elementer er der?**

---

## Slicing - Del af Liste

```python
liste = [0, 1, 2, 3, 4, 5]

liste[1:4]    # [1, 2, 3]
liste[:3]     # [0, 1, 2]
liste[2:]     # [2, 3, 4, 5]
liste[::2]    # [0, 2, 4]
```

---

## Tuples - Uforanderlige Lister

```python
punkt = (10, 20)
navn_og_alder = ('Anna', 12)

# Kan ikke ændre:
# punkt[0] = 5  ← FEJL!
```

**Tuples:** Når du IKKE vil ændre data

---

## Praktisk: Karakterer

```python
karakterer = [10, 7, 12, 4, 9]

# Sum
total = sum(karakterer)
print('Total:', total)  # 42

# Gennemsnit
gennemsnit = total / len(karakterer)
print('Gennemsnit:', gennemsnit)
```

---

## Noter for Lærer

**Timing:** ~60 minutter

**Key koncept:** Lister = samling af data

**Vigtige pointer:**
- Index starter fra 0
- `.append()` og `.remove()` ændrer listen
- Kan løkke gennem med `for`
- Tuples når du vil sikkerhed
