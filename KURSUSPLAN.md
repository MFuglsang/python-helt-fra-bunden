# Kursusplan - Python helt fra bunden

## Vision
Et progressivt Python-kursus for danske folkeskoleelever (7-9. klasse), der går fra absolut begynder til at kunne løse små programmeringsproblem selvstændigt.

---

## Samleoverblik: 9 Moduler i Progression

```
Module 01: Introduktion        (FÆRDIG ✅)
      ↓
Module 02: Variabler           (FÆRDIG ✅)
      ↓
Module 03: Betingelser         (FÆRDIG ✅)
      ↓
Module 04: Løkker              (FÆRDIG ✅)
      ↓
Module 05: Funktioner          (PLANLAGT 📋)
      ↓
Module 06: Lister & Tuples     (PLANLAGT 📋)
      ↓
Module 07: Dictionaries        (FÆRDIG ✅)
      ↓
Module 08: Tekstbehandling    (FÆRDIG ✅)
      ↓
Module 09: Projekt             (FÆRDIG ✅)
```

---

## Detaljeret Moduloversigt

### ✅ Module 01: Introduktion til Programmering

**Fil**: `01_Intro.ipynb`  
**Varighed**: 40 minutter  
**Niveau**: Absolut begynder

**Læringsmål**:
- Hvad er programmering?
- Hvordan bruger man Google Colab?
- Dit første Python program (`print()`)

**Indhold**:
- Hvad gør programmører?
- Ada Lovelace - den første programmør
- Colab brugerfladen (celler, afspilningsknap, output)
- Simpel `print()` funktion
- Lidt Python historie

**Opgaver**:
- Kør "Hej, Colab!" eksempel
- Ændre teksten i print statement
- Prøve `print()` med tal

**Forudsætninger**: Ingen

**Næste modul**: Variabler (hvordan gemmer vi information?)

---

### ✅ Module 02: Variabler

**Fil**: `02_variable.ipynb`  
**Varighed**: 50 minutter  
**Niveau**: Begynder

**Læringsmål**:
- Hvad er en variabel? (navngivet datakasse)
- 3 datatyper: Strings, Integers, Floats
- Oprette og ændre variabler
- Kombinere tekst (string concatenation)
- Grundlæggende aritmetik

**Indhold**:
1. **Variabler - grundkoncept**
   - Hvad er en variabel?
   - Analogi: Navngivet boks
   - `navn = 'Maria'`

2. **Datatyper**
   - **Strings** (tekst): `'Hej verden'`
   - **Integers** (hele tal): `42`
   - **Floats** (decimaler): `3.14`

3. **String operationer**
   - Sammensætning: `'Hej' + ' ' + 'verden'`
   - Længde: `len()`
   - `print()` med variabler

4. **Tal operationer**
   - Addition, subtraktion, multiplikation, division
   - `+`, `-`, `*`, `/`, `**` (potens), `//` (heltalsdivision)

5. **Blanding af variabler**
   - Hvordan man kombinerer tal og tekst
   - `str()` funktion for konvertering (introduktion)

**Opgaver**:
- Opret variabel med dit navn
- Kombinér fornavn og efternavn
- Beregn dage til sommerferie
- Print en sætning der bruger en variabel

**Fælles fejl**:
- Glemmer citationstegn omkring tekst
- Blanding af `+` for tekst vs. tal
- Brug af komma i stedet for punktum (Dansk vane)

**Forudsætninger**: Modul 01

**Næste modul**: Betingelser (hvordan tager computeren beslutninger?)

---

### ✅ Module 03: Betingelser (if/else)

**Fil**: `03_betingelser.ipynb`  
**Varighed**: 55 minutter  
**Niveau**: Begynder - Intermediate

**Læringsmål**:
- Hvad er en betingelse?
- Sammenligningsoperatorer: `>`, `<`, `==`, `!=`, `>=`, `<=`
- `if` statements
- `else` statements
- Indentation og struktur

**Indhold**:
1. **Hvad er en betingelse?**
   - Analogi: "Hvis det regner, tag paraply"
   - Hvordan computere tager beslutninger

2. **Sammenligningsoperatorer**
   - `>` (større end) og `<` (mindre end)
   - `==` (lig med) vs `=` (gemmer værdi)
   - `!=` (ikke lig med)
   - `>=` og `<=`

3. **if statements**
   - Syntaks og indentation
   - Hvad sker der hvis betingelsen er sand?
   - Hvad sker der hvis den er falsk?

4. **else statements**
   - To valg: if eller else
   - Flow og rækkefølge

5. **Kombinering**
   - Betingelser med variabler
   - Real-world eksempler

**Opgaver**:
- Tjek om tal er større end 10
- Bestem hvis du kan se en film (efter alder)
- Beregn karakterer baseret på point
- Vis forskellige beskederbased på bruger-input

**Fælles fejl**:
- `=` i stedet for `==`
- Glemmer kolon efter `if`
- Indentation-problemer
- Logik-fejl (altid true/false)

**Forudsætninger**: Modul 01-02

**Næste modul**: Løkker (hvordan repeterer man ting?)
---

### 📋 Module 07: Dictionaries (Ordbøger)

**Planlagt fil**: `07_dictionaries.ipynb`  
**Anslået varighed**: 60 minutter  
**Niveau**: Intermediate - Advanced

**Læringsmål**:
- Hvad er en dictionary?
- Nøgle-værdi par (key-value pairs)
- Adgang til værdier
- Tilføj, ændrer og slet værdier
- Løkker gennem dictionaries
- Dictionary metoder
- Hvornår bruger man dicts vs. lister?

**Indhold**:
1. **Hvad er en dictionary?**
   - Analogi: En rigtig ordbog (ord → betydning)
   - En rigtig telefonbog (navn → nummer)
   - `ordbog = {'nøgle': 'værdi', 'navn': 'Maria'}`
   - Anden datastruktur end lister
   - Bruger nøgler i stedet for indeks

2. **Opret en dictionary**
   - Syntaks: `{}`
   - Eksempel: `person = {'navn': 'Anna', 'alder': 12, 'by': 'København'}`
   - Tomme dicts: `{}`

3. **Adgang til værdier**
   - `.get()` metode
   - `dict[nøgle]` - hvis nøgle ikke eksisterer → fejl
   - `dict.get(nøgle, default)` - sikkert
   - Eksempel: `person['navn']` → 'Anna'

4. **Tilføj og ændrer værdier**
   - `dict[nøgle] = værdi`
   - Eksempel: `person['email'] = 'anna@mail.com'`
   - Ændrer eksisterende: `person['alder'] = 13`

5. **Slet værdier**
   - `del dict[nøgle]`
   - `.pop(nøgle)` - slet og få værdi tilbage
   - `.clear()` - slet alt

6. **Løkker gennem dictionaries**
   - `for nøgle in dict:`
   - `for nøgle, værdi in dict.items():`
   - `for værdi in dict.values():`
   - `for nøgle in dict.keys():`

7. **Dictionary metoder**
   - `.keys()` - alle nøgler
   - `.values()` - alle værdier
   - `.items()` - nøgle-værdi par
   - `.get(nøgle)` - få værdi sikker
   - `nøgle in dict` - tjek hvis nøgle eksisterer

8. **Praktiske eksempler**
   - Telefonbog (navn → nummer)
   - Karakterer (navn → karakter)
   - Inventar (item → antal)
   - Vejr (dag → temperatur)

9. **Dictionaries med lister**
   - Kombinering af data-strukturer
   - `{'navn': 'Anna', 'hobbyer': ['fodbold', 'tegning']}`

10. **Dictionaries vs. Lister**
    - Hvornår bruger man hvilken?
    - Lister: Når rækkefølge betyder noget, eller du har samme type data
    - Dicts: Når du vil finde data hurtigt via navn

**Opgaver**:
- Opret dictionary med dine yndlingsting (navn → beskrivelse)
- Lav en simpel telefonbog
- Tæl hvor mange gange hvert bogstav optræder (dictionary)
- Opret karakterliste (navn → karakter) og find bedste student
- Ændrer og tilføj til dictionary dynamisk
- Løkke og print alle værdier pent

**Fælles fejl**:
- Bruger lister når dict ville være bedre
- `dict[nøgle]` uden at tjekke hvis nøgle eksisterer (fejl)
- Forvirring mellem nøgler og værdier
- Blandede datatyper som nøgler (fungerer, men forvirrende)
- Glemmer at dictionaries ikke er sorterede (før Python 3.7)

**Forudsætninger**: Modul 01-06 (især Lister)

**Næste modul**: Tekstbehandling (praktisk brug)

---

### 📋 Module 08: Tekstbehandling & Strings

**Planlagt fil**: `08_tekstbehandling.ipynb`
---

### 📋 Module 04: Løkker (for & while)

**Planlagt fil**: `04_løkker.ipynb`  
**Anslået varighed**: 60 minutter  
**Niveau**: Intermediate

**Læringsmål**:
- Hvad er en løkke? (Repetition)
- `for` løkker
- `while` løkker
- `range()` funktion
- Break og continue

**Indhold**:
1. **Hvad er en løkke?**
   - Analogi: Gentag samme handling mange gange
   - Hvorfor er det nyttigt?

2. **for løkker**
   - `for i in range(n):`
   - Løbe gennem tal
   - Løbe gennem strenge

3. **while løkker**
   - Gentag mens betingelse er sand
   - Forskel mellem `for` og `while`
   - Risiko for uendelige løkker

4. **range() funktion**
   - `range(5)` → 0,1,2,3,4
   - `range(1, 6)` → 1,2,3,4,5
   - `range(0, 10, 2)` → 0,2,4,6,8

5. **break og continue**
   - Stop løkken med `break`
   - Spring over iteration med `continue`

6. **Kombinering med if/else**
   - Hvad hvis vi kun vil udskrive visse tal?

**Opgaver**:
- Tegn 10 stjerner i en løkke
- Udskriv tabel (gangetabel)
- Find tal med specifikke egenskaber
- Simpelt spil (gæt mit tal - max 5 gæt)

**Fælles fejl**:
- Uendelige while-løkker
- Off-by-one fejl (range)
- Indentation i løkker
- Blandede `for` og `while`-begreber

**Forudsætninger**: Modul 01-03

**Næste modul**: Funktioner (hvordan genbruger man kode?)

---

### 📋 Module 05: Funktioner

**Planlagt fil**: `05_funktioner.ipynb`  
**Anslået varighed**: 60 minutter  
**Niveau**: Intermediate - Advanced

**Læringsmål**:
- Hvad er en funktion?
- Definere egne funktioner
- Parameters og return værdier
- Scope (lokale vs. globale variabler)
- Når skal man bruge funktioner?

**Indhold**:
1. **Hvad er en funktion?**
   - Analogi: En opskrift du kan gentage
   - Genbrugbar kode
   - Gør kode mere læselig

2. **Definere en funktion**
   - `def hej():`
   - Indentation
   - `return` statement

3. **Parameters**
   - Hvordan man sender data til en funktion
   - `def add(a, b):`
   - Default parametre: `def greet(name="Ven"):`

4. **Return værdier**
   - Få resultat tilbage fra funktion
   - Flere return værdier

5. **Eksempler**
   - `def areal_cirkel(radius):`
   - `def er_primtal(tal):`
   - `def omregn_temperaturer(celsius):`

6. **Best practices**
   - Gode navne på funktioner
   - Kommentarer og dokumentation
   - Hvornår skal jeg lave en funktion?

**Opgaver**:
- Lav funktion der beregner kvadrat
- Lav funktion der tjekker om tal er lige/ulige
- Lav funktion der gentager en streng N gange
- Kombinér funktioner (funktion der kalder anden funktion)

**Fælles fejl**:
- Glemmer `return`
- Scope-forvirring
- Parametrenavne svarer ikke
- For komplekse funktioner

**Forudsætninger**: Modul 01-04

**Næste modul**: Lister (hvordan gemmer man mange ting?)

---

### 📋 Module 06: Lister & Tuples

**Planlagt fil**: `06_lister.ipynb`  
**Anslået varighed**: 65 minutter  
**Niveau**: Intermediate - Advanced

**Læringsmål**:
- Lister og deres fordele
- Indeksering (adgang til elementerne)
- Loops gennem lister
- Listen operationer (append, remove, sort)
- Tuples (uforanderlige lister)

**Indhold**:
1. **Hvad er en liste?**
   - Gemmer mange værdier i én variabel
   - Analogi: En indkøbsliste
   - `liste = [1, 2, 3, 'hej', 3.14]`

2. **Indeksering**
   - Hvordan man adgang til elementer
   - `liste[0]`, `liste[1]`, `liste[-1]`
   - Off-by-one (0-indexering)

3. **Løkker gennem lister**
   - `for element in liste:`
   - Modificer elementer

4. **Liste-metoder**
   - `.append()` - tilføj element
   - `.remove()` - fjern element
   - `.pop()` - fjern og få tilbage
   - `.sort()` - sorter
   - `.reverse()` - omvendt rækkefølge
   - `.index()` - find position
   - `.count()` - tæl forekomster

5. **Liste-slicing**
   - `liste[1:3]` - del af liste
   - `liste[:5]` - fra start til index 5
   - `liste[::2]` - hver anden element

6. **Tuples**
   - Uforanderlige lister
   - `tuple = (1, 2, 3)`
   - Hvornår bruger man tuples?

7. **Nesting**
   - Lister i lister
   - `[[1, 2], [3, 4]]`

**Opgaver**:
- Opret liste med dine yndlingsspil
- Øg/formindsk tal i liste ved loop
- Sorter karakterer fra lavest til højest
- Find gennemsnit af tal i liste
- Spil: Gæt min tanke (liste-baseret)

**Fælles fejl**:
- Glemmer at lister starter med index 0
- Forveksler `.append()` med at tildele
- Modifikation af liste mens man looper
- Tuples vs. lister

**Forudsætninger**: Modul 01-05

**Næste modul**: Tekstbehandling (praktisk anvendelse)

---

### 📋 Module 07: Tekstbehandling & Strings

**Planlagt fil**: `07_tekstbehandling.ipynb`  
**Anslået varighed**: 55 minutter  
**Niveau**: Intermediate

**Læringsmål**:
- Avancerede string-operationer
- `.split()` og `.join()`
- `.upper()`, `.lower()`, `.capitalize()`
- String indeksering og slicing
- Simpel parsing og analyse

**Indhold**:
1. **String metoder**
   - `.upper()`, `.lower()`
   - `.capitalize()`, `.title()`
   - `.replace()` - erstat tekst
   - `.strip()` - fjern mellemrum

2. **Split og join**
   - `"a,b,c".split(",")`
   - `" ".join(liste)`
   - Praktisk parsing

3. **String indeksering**
   - `string[0]`, `string[-1]`
   - `string[1:5]`
   - Løkke gennem tegn

4. **Find og søg**
   - `"hej" in "hej verden"` → True
   - `.find()` - position af substring
   - `.startswith()`, `.endswith()`

5. **Praktiske eksempler**
   - Tel hvor mange gange ordet "the" optræder
   - Tjek emailer
   - Simpel tekstanalyse

**Opgaver**:
- Konverter navn til stort/småt
- Tæl vocaler i en sætning
- Find alle ord som starter med "A"
- Analyser tekst-længde
- Simpel passwordvalidering

**Fælles fejl**:
- Strings er uforanderlige (kan ikke ændre på plads)
- `.split()` returnerer liste
- Spacing-problemer

**Forudsætninger**: Modul 01-07

**Næste modul**: Projekt (anvend alt du har lært)

---

### 📋 Module 09: Projekt - Lav Dit Eget Spil

---

**Planlagt fil**: `09_projekt.ipynb`  
**Anslået varighed**: 90 minutter  
**Niveau**: Advanced

**Læringsmål**:
- Kombinere alle koncepter
- Løse problem selvstændigt
- Debugging
- Dokumentation

**Indhold**:

Eleverne skal vælge **ét** projekt fra listen:

1. **Projekt A: Gæt Mit Tal**
   - Computer tænker på et tal 1-100
   - Elev gætter, får hint
   - Tæller gæt

2. **Projekt B: Hangman**
   - Computer har et hemmeligt ord
   - Elev gætter bogstaver
   - Viser progress
   - Win/lose betingelser

3. **Projekt C: Simpel Quiz**
   - 5 spørgsmål med multiple choice
   - Tæller rigtige svar
   - Giver karakter
   - Vis resultat

4. **Projekt D: Tekst-Analyser**
   - Elev indsætter tekst
   - Programmet teller: ord, tegn, sætninger
   - Finder længeste ord
   - Tæller vocaler

5. **Projekt E: Egen Idé**
   - Eleverne foreslår selv
   - Skal bruge mindst 3 af ens lærte koncepter

**Krav til projekt**:
- Mindst ét `for` eller `while` loop
- Mindst ét `if/else` statement
- Mindst én variabel-liste
- Mindst én funktion
- Fungerer uden fejl
- Kommentarer i koden

**Opgaver**:
- Vælg projekt
- Lav skitse / plan
- Skriv pseudokode
- Implementer
- Test og debug
- Tilføj kommentarer

**Evaluering**:
- Virker det?
- Bruger eleverne de lærte koncepter?
- Er koden læselig?
- Dokumentation tilstede?

**Forudsætninger**: Modul 01-08 (alle moduler)

---

## Tidsplan: Anbefalet Undervisning

### Scenario 1: 10 ugers kursus (1x time per uge)
```
Uge 1-2: Modul 01-02 (Intro + Variabler)
Uge 3-4: Modul 03 (Betingelser)
Uge 5-6: Modul 04 (Løkker)
Uge 7-8: Modul 05 (Funktioner)
Uge 9: Modul 06 (Lister)
Uge 10: Start på Modul 07 (Dictionaries)
(Modul 08-09 kan være valgfrit/ekstra)
```

### Scenario 2: 14 ugers kursus (1x time per uge)
```
Uge 1-2: Modul 01-02
Uge 3-4: Modul 03
Uge 5-6: Modul 04
Uge 7-8: Modul 05
Uge 9-10: Modul 06
Uge 11-12: Modul 07 (Dictionaries)
Uge 13: Modul 08 (Tekstbehandling)
Uge 14: Start på Modul 09 (projekt)
```

### Scenario 3: Intensivt kursus (4x timer på tværs af 1 uge)
```
Mandag: Modul 01-02
Tirsdag: Modul 03-04
Onsdag: Modul 05-06-07 (Dictionaries)
Torsdag: Modul 08-09 (projekt start)
Fredag: Projekt afslutning + præsentation
```

---

## Differentiering - Hvad hvis elever er på forskellige niveauer?

### Hurtige Elever
- **Ekstra udfordringer** i hver modul
  - Modul 03: Kan du lave `elif`?
  - Modul 04: Kan du lave nestet loops?
  - Modul 05: Kan du lave rekursion?
  - Modul 07: Kan du lave nested dictionaries?
  
- **Ekstra projekter**
  - Lav din egen hangman variant
  - Lav et avanceret spil
  - Lav en "quizbuilder" der læser fra liste
  - Lav en database-lignende struktur med dicts og lister

### Langsomme Elever
- **Simplificere**
  - Færre øvelser, mere eksempler
  - Længere tid per modul
  - Fokuser på: print(), variabler, if/else
  
- **One-on-one hjælp**
  - Trin-for-trin gennemgang
  - Pair programming med klassekammerat
  - Færre nye koncepter per session

### Elever der er hjemmeskrivere
- Levér video-tutorialer
- Fokuser på interaktive øvelser i Colab
- Mindre synkront arbejde

---

## Evalueringsmuligheder

### For Each Modul
- Kan eleverne løse 3 øvelser med >70% rigtigt?
- Kan de forklare koncept til en anden?

### Efter Projekt (Modul 08)
- **Funktionel**: Virker projektet?
- **Kodekvalitet**: Er koden læselig med kommentarer?
- **Koncepter**: Bruger de ≥3 ting de har lært?
- **Problem-løsning**: Kunne de debugge selv?

---

## Ressourcer & Links

- **Officiel Python Dokumentation**: https://docs.python.org/3/
- **Google Colab**: https://colab.research.google.com/
- **GitHub Repo**: https://github.com/MFuglsang/python-helt-fra-bunden/
- **W3Schools Python**: https://www.w3schools.com/python/

---

## Næste Trin: Udvikling

### Prioritet 1 (Essentiel)
- [x] Færdiggør Modul 04 (Løkker) ✅
- [ ] Færdiggør Modul 05 (Funktioner) 🚀

### Prioritet 2 (Vigtig)
- [ ] Færdiggør Modul 06 (Lister)
- [ ] Færdiggør Modul 07 (Tekstbehandling)

### Prioritet 3 (Nice-to-have)
- [ ] Færdiggør Modul 08 (Projekt)
- [ ] Lav løsningsmateriale for alle
- [ ] Lav video-tutorials

---

## Version & History

**Version**: 1.2  
**Dato**: 2026-07-14  
**Status**: Planlagt  
**Færdige Moduler**: 01, 02, 03, 04  
**Moduler Under Udvikling**: 05  
**Moduler Planlagt**: 06, 07, 08, 09  

**Seneste ændring**: Modul 04 (Løkker) færdiggjort
