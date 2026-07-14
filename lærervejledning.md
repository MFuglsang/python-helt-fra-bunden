# Lærervejledning - Python helt fra bunden

## Overblik over Kurset

**Målgruppe**: Elever i folkeskolen uden programmerings-erfaring  
**Format**: Google Colab (browser-baseret, ingen installation)  
**Varighed**: Ca. 9 moduler × 50-60 minutter = ~480 minutter (8 timer samlet)  
**Sproget**: Dansk

**Moduler dækket**: 01 ✅ 02 ✅ 03 ✅ 04 ✅ 05 ✅ 06 ✅ 07 ✅ 08 ✅ 09 ✅  

---

## Modul 01: Introduktion til Programmering

### Læringsmål
- Eleverne forstår hvad programmering er
- Eleverne kan navigere Google Colab
- Eleverne kan køre deres første Python-kode

### Timing
- **Intro (5 min)**: Hvad er programmering? Historien med Ada Lovelace
- **Colab tutorial (10 min)**: Eleverne lærer brugerfladen
- **Kodeeksempler (10 min)**: Eleverne kører eksempler
- **Egen eksperimenteren (10 min)**: Eleverne ændrer koden og ser hvad der sker
- **Afslutning (5 min)**: Recap og forberedelse til næste modul

**Total**: ~40 minutter

### Undervisningsstrategi

1. **Start med spørgsmål**: "Hvordan tror I at Minecraft bliver programmeret?"
   - Lad eleverne gætte
   - Svar: "Med hundredtusinder af linjer Python-kode!"

2. **Ada Lovelace story**: 
   - Første programmør, kvinde i 1800-tallet
   - "Vigtig pointe: Programmering var ikke altid kun for drenge!"

3. **Colab live-demo**: 
   - Vis først selv hvordan du navigerer
   - Så lader du eleverne gøre det samme

4. **"Hej, Colab!"-øvelsen**:
   - Super enkel - kan ikke gå galt
   - Bygger selvtillid

### Fælles Fejl og Løsninger

| Fejl | Symptom | Løsning |
|------|---------|--------|
| Eleverne ved ikke hvordan de kører koden | Kode virker ikke | Vis hvor afspilningsknappen er (▶) |
| Eleverne klikker print i stedet for at køre cellen | Intet sker | Gør det klart at man skal køre cellen, ikke trykke Windows print |
| Eleverne er nervøse for at ændre koden | De våger/eksperimenterer ikke | Sig: "I kan ikke ødelægge noget - I kan altid starte forfra!" |
| Eleverne ved ikke hvis de har gjort det rigtigt | Usikkerhed | Vis konsollen - "Se der! Det virker!" |

### Forberedelse til næste modul
- "Næste gang lærer vi om variabler - det er som biler hvor vi gemmer information"

---

## Modul 02: Variabler

### Læringsmål
- Eleverne forstår hvad en variabel er
- Eleverne kan oprette variabler
- Eleverne forstår 3 datatyper: tekst (string), hele tal (int), decimaltal (float)
- Eleverne kan kombinere tekst

### Timing
- **Intro (5 min)**: Hvad er en variabel? Analogi: "Navngivne biler"
- **String eksempler (10 min)**: Navn, tekst, kombinering
- **Integer eksempler (8 min)**: Hele tal, alder, beregning
- **Float eksempler (8 min)**: Decimaler, pris, præcision
- **Elevøvelser (15 min)**: Eleverne løser opgaver
- **Fælles gennemgang (5 min)**: Hvad lærte vi?

**Total**: ~50 minutter

### Undervisningsstrategi

1. **Visualisering**:
   ```
   Tegn på tavlen:
   
   [navn: 'Maria']  ← en variabel
   [alder: 12]
   [højde: 1.65]
   ```

2. **Live eksempel - lad eleverne være med**:
   - Spørg: "Hvad er dit navn?"
   - "OK, jeg gemmer det i en variabel"
   - `navn = 'Anders'`

3. **Demonstration af fejl**:
   ```python
   # FEJL - mangler citationstegn
   navn = Maria
   # ERROR: NameError: name 'Maria' is not defined
   
   # KORREKT
   navn = 'Maria'
   ```
   
4. **String kombinering - sjovt eksempel**:
   ```python
   fornavn = 'Anna'
   efternavn = 'Jensen'
   fuldt_navn = fornavn + ' ' + efternavn
   print('Hej ' + fuldt_navn + '!')
   ```

### Fælles Fejl og Løsninger

| Fejl | Symptom | Løsning |
|------|---------|--------|
| Glemmer citationstegn omkring tekst | `NameError` | "Alt tekst skal være i citationstegn eller anførselstegn" |
| Bruger komma i stedet for punkt (Dansk vane) | `3,14` vises som fejl eller tolkes forkert | Påmind: "Python er fra USA - vi bruger punktum, ikke komma" |
| Blander `+` for tekst og `+` for tal | `'10' + '5'` giver `'105'` | Vis begge eksempler: tal vs tekst |
| Lagrer tal uden at være sikker på type | `alder = 13` (eller `13.0`?) | Sig: "For hele tal, skriv uden punktum. Hvis det skal være præcist, brug punktum" |
| Udskriver variabel uden `print()` | I Colab vises variablen, i Python intet | Påmind at bruge `print()` |

### Løsningsbeskrivelse af Øvelser

**Øvelse 1**: Lav en variabel med dit navn
```python
# Løsning
mit_navn = 'Jens'
print(mit_navn)
```

**Øvelse 2**: Kombinér to ord (yndlingsfarver)
```python
# Løsning
farve1 = 'blå'
farve2 = 'rød'
print('Mine yndlingsfarver er ' + farve1 + ' og ' + farve2)
# Output: Mine yndlingsfarver er blå og rød
```

**Øvelse 3**: Beregn noget med tal
```python
# Løsning
tal1 = 10
tal2 = 20
sum_tal = tal1 + tal2
print(sum_tal)  # Output: 30
```

### Forberedelse til næste modul
- "Næste modul handler om betingelser - det er når vi lader computeren tage beslutninger!"

---

## Modul 03: Betingelser (if/else)

### Læringsmål
- Eleverne forstår hvad en betingelse er
- Eleverne kan skrive `if` statements
- Eleverne kan bruge `else` for alternativer
- Eleverne forstår sammenligningsoperatorer (`>`, `<`, `==`)

### Timing
- **Intro (5 min)**: Hvad er en betingelse? "Hvis det regner, tager jeg paraply"
- **if eksempler (10 min)**: Simpel logik
- **else eksempler (10 min)**: To valg
- **Sammenligninger (10 min)**: `>`, `<`, `==`
- **Elevøvelser (15 min)**: Eleverne løser opgaver
- **Samlet demo (5 min)**: Eleverne kombinerer hvad de har lært

**Total**: ~55 minutter

### Undervisningsstrategi

1. **Real-world analogi**:
   ```
   Hvis temperatur < 0:
       Tag vinterjakke
   Ellers:
       Tag sommerkjole
   ```

2. **Visuel flowchart på tavlen**:
   ```
        Start
         |
        Er det varmt?
       /         \
      JA         NEJ
      |           |
   T-shirt    Jakke
      |           |
   [program afslutter]
   ```

3. **Live kodning med eleverne**:
   ```python
   alder = 12
   
   if alder >= 18:
       print('Du er voksen')
   else:
       print('Du er barn')
   ```
   
   Spørg: "Hvad sker der hvis alder = 20?"

4. **Interaktiv ændring**:
   - Lad eleverne foreslå andre aldre
   - Kør koden igen hver gang

### Sammenligningsoperatorer - Visualization

```
>   betyder "større end"        10 > 5 = True
<   betyder "mindre end"         3 < 8 = True
==  betyder "lig med"            5 == 5 = True
!=  betyder "ikke lig med"       5 != 3 = True
>=  betyder "større end eller lig med"
<=  betyder "mindre end eller lig med"
```

### Fælles Fejl og Løsninger

| Fejl | Symptom | Løsning |
|------|---------|--------|
| Brug `=` i stedet for `==` i betingelse | `SyntaxError` eller uventet adfærd | "En `=` gemmer, to `==` sammenligner" |
| Glemmer kolon (`:`) efter `if` | `SyntaxError: expected ':'` | Påmind: "Hver `if` og `else` slutter med kolon" |
| Indentation galt (tekst under if uden indentation) | Koden køres ikke korrekt | Vis: "Koden UNDER `if` skal være rykket ind" |
| `elif` kendt fra engelsk - elever bruger det før du underviser det | `NameError: name 'elif' is not defined` (hvis de skriver det i en kommentar) eller det fungerer! | Hvis det virker, stor ros! Ellers: "Venter til næste modul" |
| Logik-fejl (eleverne skriver `if` som er altid true/false) | Betingelse fungerer ikke som tænkt | Spørg: "Hvad skal der være sandt her?" og arbejd baglæns |

### Løsningsbeskrivelse af Øvelser

**Øvelse 1**: Tjek om tal er større end 10
```python
# Løsning
tal = 15

if tal > 10:
    print('Tallet er større end 10')
else:
    print('Tallet er 10 eller mindre')
```

**Øvelse 2**: Tjek om alder giver adgang
```python
# Løsning
alder = 13

if alder >= 13:
    print('Du må kigge denne film')
else:
    print('Du er for ung til denne film')
```

**Øvelse 3**: Kombiner variabler med betingelser
```python
# Løsning
navn = 'Maria'
point = 85

if point >= 80:
    print(navn + ', du har fået 10-taller!')
else:
    print(navn + ', træn mere næste gang')
```

### Forberedelse til næste modul
- "Næste gang handler det om løkker - det er når vi gentager ting mange gange uden at skulle skrive det igen og igen!"

---

## Modul 04: Løkker (for & while)

### Læringsmål
- Eleverne forstår hvad en løkke er og hvorfor det er kraftfuldt
- Eleverne kan skrive `for` løkker med `range()`
- Eleverne kan kombinere løkker med `if` statements
- Eleverne forstår indentation inden i løkker

### Timing
- **Intro (5 min)**: Hvad er løkker? "Repetition uden at gentage koden"
- **range() eksempler (8 min)**: Tæl fra 0 til 10
- **for loop eksempler (10 min)**: Print tal, tegn mønstre
- **if + for kombinering (8 min)**: Kun visse tal
- **Elevøvelser (18 min)**: Stjerner, tabeller, mønstre
- **Samlet recap (5 min)**: Hvad lærte vi?

**Total**: ~60 minutter

### Undervisningsstrategi

1. **Visualisering af range()**:
   ```
   range(5) betyder: 0, 1, 2, 3, 4
   range(1, 6) betyder: 1, 2, 3, 4, 5
   range(0, 10, 2) betyder: 0, 2, 4, 6, 8
   ```

2. **"Tegn stjerner" øvelse**:
   ```python
   # Uden løkke (kedeligt):
   print('*')
   print('*')
   print('*')
   print('*')
   print('*')
   
   # Med løkke (kraftfuldt!):
   for i in range(5):
       print('*')
   ```
   Spørg: "Hvad hvis I skulle tegne 1000 stjerner?"

3. **Indentation visualisering**:
   - Vis at koden UNDER `for` skal være rykket ind
   - Tegn pile på tavlen der viser "denne kode hører til løkken"

### Fælles Fejl og Løsninger

| Fejl | Symptom | Løsning |
|------|---------|--------|
| Glemmer kolon efter `for` | `SyntaxError` | Påmind: "Hver løkke slutter med kolon" |
| Indentation galt | Løkken køres kun én gang | "Alt DER SKAL gentages skal være rykket ind" |
| Off-by-one fejl i range() | `range(5)` giver 0-4, elever forventede 0-5 | "range(5) betyder 5 tal starter fra 0" |
| `for i in i:` eller anden variabl-forvirring | Kan fungere eller give fejl | Påmind: `i` er variablen der ændres hver gang |
| Prøver at ændre løkke-variablen indenfor løkken | Mønstre virker ikke som forventet | "Løkken kontrollerer `i`, du kan ikke ændre det" |

### Løsningsbeskrivelse af Øvelser

**Øvelse 1**: Tegn 10 stjerner
```python
for i in range(10):
    print('*')
```

**Øvelse 2**: Gangetabel
```python
for i in range(1, 11):
    print(str(i) + ' * 5 = ' + str(i * 5))
```

**Øvelse 3**: Find ulige tal fra 1-10
```python
for i in range(1, 11):
    if i % 2 == 1:
        print(str(i) + ' er ulige')
```

**Øvelse 4**: Tegn trekant
```python
for i in range(1, 6):
    print('*' * i)
```

### Forberedelse til næste modul
- "Næste modul er funktioner - det er som at lave dine egne kommandoer som computeren kan udføre"

---

## Modul 05: Funktioner

### Læringsmål
- Eleverne forstår hvad en funktion er
- Eleverne kan definere simple funktioner
- Eleverne kan give funktioner parameters
- Eleverne forstår `return` værdier

### Timing
- **Intro (5 min)**: Hvad er funktioner? "Genbrugbar kode du kan kalde"
- **def eksempler (10 min)**: Simpel funktion uden parameter
- **Parameters (10 min)**: Sending data til funktionen
- **return værdier (8 min)**: Få data tilbage
- **Kombinering (10 min)**: Funktioner der kalder funktioner
- **Elevøvelser (15 min)**: Lav egne funktioner
- **Recap (2 min)**

**Total**: ~60 minutter

### Undervisningsstrategi

1. **Analogi**: "En funktion er som en opskrift"
   ```
   Opskrift: "Lav smørrebrød"
     Input: hvedebrød, smør, rullepølse
     Output: lækker sandwich
   ```

2. **Live demonstration**:
   ```python
   # Definere
   def hilsen():
       print('Hej verden!')
   
   # Kalde
   hilsen()  # Dette gør noget!
   ```

3. **Parameters - visuelt**:
   ```python
   def hilsen(navn):
       print('Hej ' + navn)
   
   hilsen('Anna')    # Output: Hej Anna
   hilsen('Bert')    # Output: Hej Bert
   ```

4. **return - vigtig pointe**:
   ```python
   # Funktion der giver resultat tilbage
   def add(a, b):
       return a + b
   
   resultat = add(5, 3)  # resultat = 8
   ```

### Fælles Fejl og Løsninger

| Fejl | Symptom | Løsning |
|------|---------|--------|
| Glemmer `return` | Funktion returnerer `None` | "Hvis du vil have værdi tilbage, brug `return`" |
| Scope-forvirring (variabel defineret inden i funktion, brugt uden for) | `NameError` | "Variabler in funktioner lever kun i funktionen" |
| Kalder funktion uden parenteser | Intet sker | "Du skal skrive `()` når du kalder funktionen" |
| Parameter-navn stemmer ikke | `NameError` | "De navne du bruger når du kalder skal stemme" |
| Indentation galt inden i funktion | Kode bliver ikke del af funktion | "Alt under `def` skal være rykket ind" |

### Løsningsbeskrivelse af Øvelser

**Øvelse 1**: Lav funktion der printer navn
```python
def print_navn(navn):
    print('Hej ' + navn)

print_navn('Maria')
```

**Øvelse 2**: Funktion der returnerer værdi
```python
def multiply(a, b):
    return a * b

resultat = multiply(4, 5)
print(resultat)
```

**Øvelse 3**: Funktion der tæller i løkke
```python
def tæl(n):
    for i in range(n):
        print(i)

tæl(5)
```

### Forberedelse til næste modul
- "Næste modul handler om lister - når du skal gemme MANGE ting på samme tid"

---

## Modul 06: Lister & Tuples

### Læringsmål
- Eleverne forstår hvad en liste er
- Eleverne kan adgang til elementer med indeks
- Eleverne kan løkke gennem lister
- Eleverne kender liste-metoder (`.append()`, `.remove()`)

### Timing
- **Intro (5 min)**: Hvad er liste? "Mange ting i én variabel"
- **Opret og indeks (10 min)**: Hvordan adgang til element
- **Løkker gennem lister (8 min)**: `for element in liste:`
- **Liste-metoder (10 min)**: `.append()`, `.remove()`, `.sort()`
- **Praktiske eksempler (10 min)**: Indkøbsliste, karakterer
- **Elevøvelser (15 min)**
- **Recap (2 min)**

**Total**: ~60 minutter

### Undervisningsstrategi

1. **Indeks visualisering**:
   ```
   liste = ['æble', 'banan', 'kirsebær', 'drue']
   index:    0       1         2          3
   
   liste[0] → 'æble'
   liste[2] → 'kirsebær'
   liste[-1] → 'drue' (sidste element)
   ```

2. **Demonstration af `.append()`**:
   ```python
   kurv = ['milk', 'brød']
   print(kurv)  # ['milk', 'brød']
   
   kurv.append('ost')
   print(kurv)  # ['milk', 'brød', 'ost']
   ```

3. **Løkke gennem lister**:
   ```python
   frugter = ['æble', 'banan', 'appelsin']
   
   for frugt in frugter:
       print('Jeg holder af ' + frugt)
   ```

### Fælles Fejl og Løsninger

| Fejl | Symptom | Løsning |
|------|---------|--------|
| Starter tælling fra 1 i stedet for 0 | `IndexError` når de gætter position | "Python tæller fra 0, ikke 1" |
| Blander `.append()` med assignment | `liste.append([1,2,3])` i stedet for værdi | "`.append()` tilføjer EN ting, ikke en liste" |
| Ændrer liste mens man løkker gennem den | Resultaterne virker mærkelige | "Ikke ændrer liste når du løkker igennem den" |
| Prøver at få element der ikke eksisterer | `IndexError: list index out of range` | "Tjek længden af listen først med `len()`" |

### Løsningsbeskrivelse af Øvelser

**Øvelse 1**: Opret liste og print elementer
```python
dyr = ['hund', 'kat', 'fugl']
print(dyr[0])
print(dyr[-1])
```

**Øvelse 2**: Løkke gennem liste
```python
karakterer = [10, 7, 12, 4, 9]

for karakter in karakterer:
    print('Karakter: ' + str(karakter))
```

**Øvelse 3**: Tilføj og fjern elementer
```python
shoppingliste = ['milk', 'brød', 'æbler']
shoppingliste.append('smør')
shoppingliste.remove('æbler')
print(shoppingliste)
```

### Forberedelse til næste modul
- "Næste modul er ordbøger - de er som lister men bedre når du skal søge på navn i stedet for nummer"

---

## Modul 07: Dictionaries (Ordbøger)

### Læringsmål
- Eleverne forstår nøgle-værdi par
- Eleverne kan create og adgang til dictionaries
- Eleverne kan tilføje, ændre, og slette elementer
- Eleverne kan løkke gennem dictionaries

### Timing
- **Intro (5 min)**: Hvad er dictionary? "Navn til værdi"
- **Opret og adgang (10 min)**: Syntaks og `.get()`
- **Ændring og sletning (8 min)**: Tilføj nye, opdater, slet
- **Løkker (10 min)**: `.items()`, `.keys()`, `.values()`
- **Praktiske eksempler (10 min)**: Telefonbog, karakterer
- **Elevøvelser (15 min)**
- **Recap (2 min)**

**Total**: ~60 minutter

### Undervisningsstrategi

1. **Ordbog-analogi**:
   ```
   Rigtig ordbog:
   "hund" → "Et husdyr med fire ben"
   "bil" → "Et køretøj med hjul"
   
   Python dictionary:
   {'hund': 'dyr', 'bil': 'køretøj'}
   ```

2. **Nøgle-værdi visualisering**:
   ```
   person = {
       'navn': 'Anna',      ← nøgle: værdi
       'alder': 12,         ← nøgle: værdi
       'by': 'København'    ← nøgle: værdi
   }
   ```

3. **Praktisk eksempel - Telefonbog**:
   ```python
   telefon = {'Anna': '40123456', 'Bert': '40654321'}
   print(telefon['Anna'])  # Output: 40123456
   ```

### Fælles Fejl og Løsninger

| Fejl | Symptom | Løsning |
|------|---------|--------|
| Glemmer citationstegn på nøgle | `NameError` eller `KeyError` | "Nøgler skal være strenge i citationstegn" |
| Bruger `[key]` uden at tjekke hvis det eksisterer | `KeyError` | "Brug `.get()` hvis du er usikker" |
| Blander dictionary-syntaks med liste-syntaks | Fejl eller mærkelig adfærd | "Dictionaries bruger `{}`, lister bruger `[]`" |
| Løkker bare gennem nøgler, ikke værdier | Output er kun nøgler | "Brug `.items()` hvis du vil have både" |

### Løsningsbeskrivelse af Øvelser

**Øvelse 1**: Opret dictionary
```python
person = {'navn': 'Anna', 'alder': 12, 'by': 'København'}
print(person['navn'])
```

**Øvelse 2**: Tilføj og ændrer
```python
person['email'] = 'anna@gmail.com'
person['alder'] = 13
print(person)
```

**Øvelse 3**: Løkke gennem items
```python
for nøgle, værdi in person.items():
    print(nøgle + ': ' + str(værdi))
```

### Forberedelse til næste modul
- "Næste modul handler om tekstbehandling - alle de smarte trix du kan gøre med strenge"

---

## Modul 08: Tekstbehandling (String Metoder)

### Læringsmål
- Eleverne kan bruge `.upper()`, `.lower()`, `.replace()`
- Eleverne kan `.split()` og `.join()`
- Eleverne kan søge i tekst med `in` og `.find()`
- Eleverne kan arbejde med string indeksering

### Timing
- **Intro (5 min)**: Hvad kan vi gøre med tekst?
- **Bogstav-størrelse (8 min)**: `.upper()`, `.lower()`, `.capitalize()`
- **Erstat og fjern mellemrum (8 min)**: `.replace()`, `.strip()`
- **Opdel og sæt sammen (10 min)**: `.split()`, `.join()`
- **Søge i tekst (8 min)**: `in`, `.find()`, `.startswith()`
- **String indeks (8 min)**: `[0]`, `[-1]`, slicing
- **Elevøvelser (15 min)**
- **Recap (2 min)**

**Total**: ~60 minutter

### Undervisningsstrategi

1. **Metodekatalog på tavlen**:
   ```
   .upper()     → gør alt STORT
   .lower()     → gør alt småt
   .replace()   → bytt ord
   .split()     → lav liste af ord
   .join()      → lav tekst fra liste
   ```

2. **`.split()` og `.join()` er vigtigst**:
   ```python
   # Split: fra tekst til liste
   tekst = "A,B,C"
   liste = tekst.split(',')  # ['A', 'B', 'C']
   
   # Join: fra liste til tekst
   nye_tekst = '-'.join(liste)  # 'A-B-C'
   ```

3. **Søgning visualisering**:
   ```python
   tekst = "Python er sjovt"
   
   'Python' in tekst          # True
   'Java' in tekst            # False
   tekst.find('sjovt')        # Position 11
   ```

### Fælles Fejl og Løsninger

| Fejl | Symptom | Løsning |
|------|---------|--------|
| Glemmer at metoder returnerer nyt string | `tekst.upper()` uden at gemme resultatet | "Gem resultatet i en variabel: `tekst = tekst.upper()`" |
| Blander `.split()` og `.join()` | Fejl i brug | "`.split()` = tekst til liste, `.join()` = liste til tekst" |
| Bruger `.join()` forkert | `liste.join(',')` | "Skal være `,`.join(liste), ikke omvendt!" |
| Case-sensitivity problem | Søgning finder ikke da store/små bogstaver er forskellige | "Brug `.lower()` før søgning hvis du vil være usikker" |
| Tries to modify string directly | `string[0] = 'X'` | "Strings kan ikke ændres. Lav ny string i stedet" |

### Løsningsbeskrivelse af Øvelser

**Øvelse 1**: Konverter navn
```python
navn = '  anna jensen  '
navn = navn.strip().upper()
print(navn)  # ANNA JENSEN
```

**Øvelse 2**: Tæl ord
```python
tekst = 'Python er sjovt og nyttigt'
ord = tekst.split()
print(len(ord))  # 5
```

**Øvelse 3**: Find længeste ord
```python
tekst = 'Den hurtige brune ræv springer'
ord = tekst.split()
længste = ord[0]
for o in ord:
    if len(o) > len(længste):
        længste = o
print(længste)
```

### Forberedelse til næste modul
- "Næste modul er det store projekt - her kombinerer du ALT du har lært!"

---

## Modul 09: Dit Eget Projekt

### Læringsmål
- Eleverne kan kombinere alle koncepter
- Eleverne kan løse problemer selvstændigt
- Eleverne kan debugge selv
- Eleverne få selvtillid til at lave egne programmer

### Timing
- **Intro (10 min)**: Præsenter de 5 projekt-muligheder
- **Valg (5 min)**: Eleverne vælger projekt
- **Planificering (10 min)**: Skitsering og pseudokode
- **Implementation (40 min)**: Eleverne koder
- **Testing (10 min)**: Eleverne tester deres program
- **Fejlfinding (10 min)**: Hvis noget ikke virker
- **Afslutning (15 min)**: Præsentation af resultater

**Total**: ~90 minutter (kan være fordelt over flere sessioner)

### Undervisningsstrategi

1. **Pre-projekt motivering**:
   - "I har nu lært alt det vigtige!"
   - "Nu viser I hvad I kan"
   - "Der er ingen rigtig måde at gøre det på"

2. **Vejledning for hver projekt**:
   
   **A: Gæt mit tal**
   - Simplest - god til usikre elever
   - Fokus på: `while` løkke, `if/else`, tilfældig tal
   
   **B: Hangman**
   - Medium - sjovt spil-format
   - Fokus på: strenge, lister, løkker gennem streng
   
   **C: Quiz**
   - Medium - pædagogisk
   - Fokus på: dictionaries, løkke gennem dict, tæller
   
   **D: Tekst-Analyser**
   - Medium - praktisk
   - Fokus på: string-metoder, løkker, funktioner
   
   **E: Egen idé**
   - Sværeste - men mest sjovt for kreative elever
   - Fokus på: egenindsats, kreativitet

3. **Fejlfinding-strategi**:
   - "Hvad siger fejlmeddelelsen?"
   - "Hvor sker fejlen?"
   - "Print() for at se hvad der sker"
   - "Har jeg stavfel i variabelnavne?"

### Checkpoint under arbejde

Gå rundt og spørg:
- "Hvad prøver dit program?"
- "Virker det som forventet?"
- "Hvad mangler?"

Giv små hints uden at løse det:
- "Prøv at print() variablen"
- "Har du glemt indentation?"
- "Hvad skal der ske her?"

### Fælles Fejl ved Projekter

| Fejl | Symptom | Løsning |
|------|---------|--------|
| Programmet virker ikke fra start | Eleverne ved ikke hvor de skal starte | Begynd med `print()` - få bare output |
| Uendelig løkke | Program fryser | "Betingelsen bliver aldrig falsk - tjek den" |
| Input-problemer | Input er string, ikke tal | "Husk `int(input())` hvis det skal være tal" |
| Manglende indentation | Logik virker ikke | "Tegn pile på hvad der hører til løkken" |
| For komplekst | Eleverne mister overblikket | "Start simpelt, lav det mere komplekst senere" |

### Løsningsbeskrivelse (Template)

For hver projekt er der template i notebooken. Eleverne skal:
1. Læse template
2. Forstå hvad der skal ske
3. Implementere selv
4. Teste

Du som lærer skal give hints, ikke løsningen!

### Efter-projekt aktiviteter

- **Præsentation**: Eleverne viser deres program
- **Demonstration**: De kører det live
- **Spørgsmål**: "Hvad var det sværeste?"
- **Applaus**: "Flot arbejde!"

---

## Tips til Undervisning Generelt

### Before Session
- [ ] Test alle kodeceller selv - sikr de virker
- [ ] Åbn notebooken i Colab selv, så du kender dens layout
- [ ] Find 2-3 ekstra eksempler som inspiration
- [ ] Forbered rebus/aktiviteter hvis klassen virker uengageret

### Under Session
- **Være tålmodig med langsomme eleverne**
  - Nogle læser ikke siden ordentlig - vis dem præcis hvad de skal klikke
  - Nogle har dårlig internet - accepter det
  
- **Celebrer små wins**
  - "Woah, jeres first program virker!" 
  - Det bygger selvtillid
  
- **Spørg altid**: "Hvad tror I vil ske?"
  - Før I kører koden
  - Det gør dem til aktive tænkere
  
- **Tillad eksperimentering**
  - "I kan ikke ødelægge noget"
  - "Hvad hvis du ændrer det tal?"
  
- **Differentier**
  - Hurtige elever: "Kan du kombinere to `if` statements?"
  - Langsomme elever: "Kan du bare ændre navnet fra Maria til dig selv?"

### After Session
- [ ] Spørg: "Hvad var det sværeste?"
- [ ] Svar på alle spørgsmål, selv hvis du ikke ved svaret ("Det finder vi ud af næste gang!")
- [ ] Giv hjemmelektier som optionalt for de interesserede

---

## Udfordringer med Specifikke Elever

### "Jeg forstår det ikke"
**Løsning:**
1. Ikke personligt - programmering er abstrakt
2. Spørg: "Hvad forstår du ikke præcist?"
3. Tegn det på tavlen
4. Giv et meget konkret eksempel fra deres liv

### "Jeg får en fejl"
**Løsning:**
1. Læs fejlmeddelelsen *sammen* med dem
2. Fejlmeddelelser er dine venner - de fortæller hvad der er galt
3. Få dem til selv at gætte hvad der mangler

### "Det er kedeligt"
**Løsning:**
1. Spørg hvad de synes ville være sjovere
2. Gør det mere personligt (deres navne, deres interesser)
3. Udfordring: "Kan du lave noget mere komplekst?"

---

## Ressourcer

- **Python Dokumentation**: https://docs.python.org/3/
- **Google Colab**: https://colab.research.google.com/
- **GitHub-repo**: https://github.com/MFuglsang/python-helt-fra-bunden/

---

## Ændringer til Denne Guide

Når du opdager nye fælles fejl eller gode undervisnings-tricks, skal du:
1. Tilføje dem til denne guide
2. Dele dem på GitHub-repoet så andre lærere profiterer

**Senest opdateret**: 2026-07-14 (Alle 9 moduler komplet)

