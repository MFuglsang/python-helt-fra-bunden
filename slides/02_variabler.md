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

# Modul 02: Variabler 📦

**Hvordan gemmer vi information?**

---

## Hvad er en Variabel?

En **navngivet "biler"** hvor vi gemmer data

```
┌─────────────────┐
│ navn: 'Maria'   │ ← variabel med værdi
└─────────────────┘

┌─────────────────┐
│ alder: 12       │ ← anden variabel
└─────────────────┘
```

---

## Opret en Variabel

```python
navn = 'Maria'
alder = 12
højde = 1.65
```

**Betyder:**
- `navn` gemmer teksten `'Maria'`
- `alder` gemmer tallet `12`
- `højde` gemmer decimaltallet `1.65`

---

## Tre Datatyper

### String (tekst)
```python
navn = 'Anna'
farve = 'blå'
```
**Husk:** Altid i citationstegn!

### Integer (helt tal)
```python
alder = 12
point = 100
```

### Float (decimaltal)
```python
højde = 1.65
pris = 49.99
```

---

## Kombinér Tekst

```python
fornavn = 'Anna'
efternavn = 'Jensen'
fuldt_navn = fornavn + ' ' + efternavn

print('Hej ' + fuldt_navn)
```

**Output:** `Hej Anna Jensen`

---

## Fælles Fejl 🐛

❌ Glemmer citationstegn
```python
navn = Maria  # FEJL!
```

✅ Skriver det rigtigt
```python
navn = 'Maria'  # OK
```

---

## Interaktion

**Spørg eleverne:**
- "Hvad skal I gemme i en variabel?"
- "Hvad er forskellige mellem tekst og tal?"
- "Kan vi kombinere ord?"

**Lad dem lave deres eget eksempel!**

---

## Noter for Lærer

**Timing:** ~50 minutter

**Key koncept:** Variabler = gemiing af data

**Demonstration:**
- Tegn på tavlen hvordan variabler virker
- Vis feilen når man glemmer citationstegn
- Lad eleverne ændre værdier og se hvad sker
