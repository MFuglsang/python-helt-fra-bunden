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

# Modul 07: Ordbøger (Dictionaries) 📖

**Nøgle → Værdi!**

---

## Hvad er en Dictionary?

**Som en rigtig ordbog: ord → betydning**

```python
person = {
    'navn': 'Anna',
    'alder': 12,
    'by': 'København'
}
```

**Notation:** `{}` krøllede parenteser

---

## Opret Dictionary

```python
telefonbog = {
    'Anna': '40123456',
    'Bert': '40654321',
    'Cecilia': '40999999'
}
```

**Nøgle: værdi par**

---

## Adgang til Værdi

```python
person = {'navn': 'Anna', 'alder': 12}

print(person['navn'])    # Anna
print(person['alder'])   # 12
```

**Brug nøglen i [] for at få værdi**

---

## Tilføj og Ændrer

```python
person = {'navn': 'Anna'}

# Tilføj
person['email'] = 'anna@gmail.com'

# Ændrer
person['navn'] = 'AnnaFigure'

print(person)
```

---

## Slet

```python
person = {'navn': 'Anna', 'alder': 12}

del person['alder']

print(person)  # {'navn': 'Anna'}
```

---

## Løkke gennem Dictionary

```python
person = {'navn': 'Anna', 'alder': 12}

# Kun nøgler
for nøgle in person:
    print(nøgle)

# Nøgler OG værdier
for nøgle, værdi in person.items():
    print(nøgle + ': ' + str(værdi))
```

---

## .get() - Sikker Adgang

```python
person = {'navn': 'Anna'}

# FARLIGT
# print(person['email'])  ← FEJL!

# SIKKERT
email = person.get('email', 'ikke opgivet')
print(email)  # ikke opgivet
```

---

## Dictionary Metoder

```python
person = {'navn': 'Anna', 'alder': 12}

person.keys()      # ['navn', 'alder']
person.values()    # ['Anna', 12]
person.items()     # [('navn', 'Anna'), ('alder', 12)]
```

---

## Praktisk: Karakterbog

```python
karakterer = {
    'Anna': 10,
    'Bert': 7,
    'Cecilia': 12
}

for navn, karakter in karakterer.items():
    print(navn + ' har ' + str(karakter))
```

---

## Dictionary vs. Liste

```
LISTE (nummer):           DICTIONARY (navn):
liste[0] = først          dict['navn'] = værdi
liste[1] = anden          dict['alder'] = værdi
liste[2] = tredje

Når: ordre betyder noget  Når: søgning på navn
```

---

## Noter for Lærer

**Timing:** ~60 minutter

**Key koncept:** Dictionary = navn-værdi par

**Vigtige pointer:**
- `{}` for dictionary
- Nøgler skal være strenge (tekst)
- Brug `.get()` hvis usikker
- `.items()` for både nøgler og værdier
