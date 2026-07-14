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

# Modul 03: Betingelser 🚦

**Computeren tager beslutninger!**

---

## Hvad er en Betingelse?

**Hvis noget er sandt, gør noget**

```
Hverdags-eksempel:
├─ Hvis det regner → tag paraply
├─ Hvis det er koldt → tag jakke
└─ Hvis det er varmt → tag T-shirt
```

---

## if Statement

```python
alder = 13

if alder >= 13:
    print('Du må kigge denne film')
```

**Flowchart:**
```
    Alder >= 13?
       ↙     ↘
      JA      NEJ
      ↓        ↓
  Tilladt   Nej tak
```

---

## if + else

```python
alder = 10

if alder >= 13:
    print('Du må kigge denne film')
else:
    print('Du er for ung')
```

**To valg:**
- Hvis alder >= 13: `print()` første
- Ellers: `print()` anden

---

## Sammenligningsoperatorer

```
>   større end          10 > 5 = True
<   mindre end           3 < 8 = True
==  lig med              5 == 5 = True
!=  ikke lig med         5 != 3 = True
>=  større eller lig    10 >= 10 = True
<=  mindre eller lig     3 <= 5 = True
```

**Vigtig:** `=` gemmer, `==` sammenligner!

---

## Praktisk Eksempel

```python
point = 85

if point >= 80:
    print('Du fik 10-taller!')
elif point >= 60:
    print('Du fik 7-taller')
else:
    print('Du skal øve mere')
```

---

## Visualisering

```
       Start
         ↓
    Point >= 80?
      ↙     ↘
     JA      NEJ
     ↓        ↓
   10-tall   >= 60?
             ↙    ↘
            JA    NEJ
            ↓      ↓
          7-tall  Øv mere
```

---

## Fælles Fejl 🐛

❌ Brug `=` i stedet for `==`
```python
if alder = 13:  # FEJL!
```

✅ Brug `==` til sammenligning
```python
if alder == 13:  # OK
```

---

## Interaktion

**Spørg eleverne:**
- "Hvad skal der ske hvis...?"
- "Hvad er andre betingelser i jeres liv?"
- "Kan vi kombinere flere betingelser?"

---

## Noter for Lærer

**Timing:** ~55 minutter

**Vigtigste koncept:** Computere kan tage beslutninger baseret på data

**Demonstration:**
- Tegn flowchart på tavlen
- Vis fejlen med `=` vs `==`
- Lad eleverne lave deres egne betingelser
