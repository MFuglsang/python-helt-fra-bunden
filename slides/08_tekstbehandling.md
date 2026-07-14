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

# Modul 08: Tekstbehandling ✂️

**Alle de smarte trix med strenge!**

---

## Bogstav-Størrelse

```python
tekst = 'Python'

tekst.upper()         # PYTHON
tekst.lower()         # python
tekst.capitalize()    # Python
tekst.title()         # Python (titel)
```

---

## Erstat Tekst

```python
sætning = 'Jeg holder af hunde fordi hunde er søde'

ny = sætning.replace('hunde', 'katte')
# Jeg holder af katte fordi katte er søde
```

---

## Fjern Mellemrum

```python
tekst = '   Hej verden   '

tekst.strip()    # Hej verden (begge sider)
tekst.lstrip()   # Hej verden    (venstre)
tekst.rstrip()   # Hej verden    (højre)
```

---

## Opdel Tekst med .split()

```python
sætning = 'Jeg holder af Python'
ord_liste = sætning.split()
# ['Jeg', 'holder', 'af', 'Python']

csv = 'Anna,Bert,Cecilia'
navne = csv.split(',')
# ['Anna', 'Bert', 'Cecilia']
```

---

## Sæt sammen med .join()

```python
ord_liste = ['Jeg', 'holder', 'af', 'Python']

# Fra liste til sætning
sætning = ' '.join(ord_liste)
# 'Jeg holder af Python'

# Med kommaer
csv = ','.join(['A', 'B', 'C'])
# 'A,B,C'
```

---

## Søg i Tekst

```python
tekst = 'Python er sjovt'

'Python' in tekst       # True
'Java' in tekst         # False
'sjovt' in tekst        # True
```

---

## Find Position

```python
tekst = 'Python er sjovt'

pos = tekst.find('sjovt')
# 11 (position hvor ordet starter)

hvis ord ikke findes:
tekst.find('Java')  # -1
```

---

## Start og Slutning

```python
email = 'anna@gmail.com'

email.startswith('anna')     # True
email.endswith('.com')       # True

fil = 'billede.jpg'
fil.endswith('.jpg')         # True
```

---

## String Indeksering

```python
ord = 'Python'

ord[0]       # 'P'
ord[-1]      # 'n'
ord[1:4]     # 'yth'
ord[:3]      # 'Pyt'
ord[3:]      # 'hon'
```

---

## Praktisk: Tæl Vocaler

```python
tekst = 'programmering'
vocaler = 'aeiouæøå'

tæller = 0
for bogstav in tekst:
    if bogstav in vocaler:
        tæller += 1

print('Vocaler:', tæller)  # 4
```

---

## Løkke gennem String

```python
for bogstav in 'Python':
    print(bogstav)
```

**Output:** P, y, t, h, o, n (hver på egen linje)

---

## Noter for Lærer

**Timing:** ~60 minutter

**Key koncept:** String-metoder = magt

**Vigtige pointer:**
- `.split()` = string til liste
- `.join()` = liste til string
- `in` = søgning
- String-metoder returnerer NEU string
