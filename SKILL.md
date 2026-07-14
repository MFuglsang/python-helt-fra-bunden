# Python helt fra bunden - Undervisnings- og Materialkonstruktionsskill

## Formål
Denne skill dokumenterer den pedagogiske tilgang, materialkonstruktion og tekniske opbygning af **Python helt fra bunden**-kurset. Skillet tjener som retningslinje for alle fremtidige udvidelser, materiale-udvikling og ændringer til kursuset.

---

## Del 1: Pædagogisk Tilgang

### Målgruppe
- **Elever i folkeskolen** (7.-9. klasse), ingen forudsætninger
- **Absolute begyndere** i programmering
- **Browser-baseret læring** (Google Colab)

### Grundlæggende Undervisningsprincipper

#### 1. **Narrativ og Kontekst**
- **Start med "hvorfor"**: Hver lektion introduceres med relevante eksempler fra elevernes verden
  - "Hvordan blir videospil lavet?" 
  - "Hvordan ved GPS'en, hvor du er?"
  - "Hvordan virker dine yndlingssociale medier?"
  
- **Fortæl historier**: Brug historiske referencer (Ada Lovelace, Guido van Rossum) for at humanisere programmering
- **Konkrete, visuelle eksempler**: Knyt begreber til ting eleverne kender

#### 2. **Progression: Fra Simpelt til Komplekst**
Kurset følger denne tilgang:
1. **Præsentation af koncept** → Hvad er det? Hvorfor skal vi vide det?
2. **Forklaring i enkel dansk** → Analogier og sammenligning med hverdagen
3. **Kodet eksempel** → Eleverne ser det i action
4. **Guidet øvelse** → Eleverne prøver selv med vejledning
5. **Selvstændig opgave** → Eleverne løser på egen hånd

#### 3. **"Det er OK at lave fejl"**
- Eksplicit besked om, at fejl er en normal del af læring
- Fejl skal tolkes som feedback, ikke som fejleslagne
- Vær venlig og opmuntrende i tonen

#### 4. **Inkluderende Tone**
- Sig "Hej fremtidige udviklere!" - velkomstsnak til alle
- Brug "vi", "lad os prøve", "sammen"
- Anerkend at programmering kan virke skummelt til at starte
- Validér elevernes indsats

#### 5. **Konkrete Kodeopgaver**
- Hver øvelse skal være løsbar inden for 2-3 minutter
- Øvelserne skal bygge direkte på det netop lærte
- Løsninger skal være rimelig korte (ikke 50 linjer kode per øvelse)

---

## Del 2: Materialkonstruktion

### Notebook-Struktur per Modul

Hver notebook følger dette mønster:

#### **A. Introduktion (Top of Notebook)**
```markdown
# [Modulnavn]

Kort introduktion til, hvad eleverne skal lære.
Hvilket koncept lærer vi?
Hvorfor er det vigtigt?

Eksempel: "I denne arbejdsbog vil du lære de helt grundlæggende byggesten i Python. 
Vi vil blande forklaringer med eksempler, og der vil være små opgaver, du selv kan løse. 
Husk, det er okay at lave fejl – det er sådan, vi lærer!"
```

#### **B. Lektionsblokke (Gentager mange gange)**

Hver blok består af:

1. **Markdown: Teori & Forklaring**
   ```markdown
   ## Emnenavn
   
   - Start med spørgsmål eller en tankevekkende påstand
   - Forklar koncept i hverdagssprog
   - Brug analogier ("En variabel er som en boks...")
   - Giv konkrete eksempler fra elevernes verden
   - Slip ikke for for meget detaljer (hele dokumentationen er på Python.org)
   ```

2. **Code Cell: Eksempel (Eleverne skal kunne køre det)**
   ```python
   # Kort kommentar om hvad eksemplet viser
   # Kommentarer skal vejlede eleverne gennem koden
   variabel = 'værdi'
   print(variabel)
   
   # Øvelse: Prøv at ændre 'værdi' til noget sølf og se hvad der sker
   ```

3. **Markdown: Øvelsesbeskrivelse (valgfrit)**
   - Markér øvelser med `**Øvelse:**`
   - Gør øvelsen meget konkret
   - Giv et eksempel på hvad output burde se ud ud

#### **C. Progressiv Vanskelighedsgrad**
```
Blok 1: Introeksempel (meget simpelt)
   ↓
Blok 2: Lille variation
   ↓
Blok 3: Kombinering af begreber
   ↓
Blok 4: Selvstændig problem-løsning
```

### Eksempel: Variabelmodulet

**Sektion 1 - Grundkoncept:**
```markdown
### Hvad er en variabel?

En variabel er som en navngivet boks, hvor vi kan gemme data...
```
↓ (kodet eksempel)
```python
navn = 'Maria'
print(navn)
# Øvelse: Ændre 'Maria' til dit eget navn
```

**Sektion 2 - Datatyper:**
```markdown
### Tekst (Strings)

Når vi vil gemme ord eller sætninger...
```
↓ (kodet eksempel med kombinering af strenge)
```python
fornavn = 'Anna'
efternavn = 'Jensen'
fuldt_navn = fornavn + ' ' + efternavn
print(fuldt_navn)
# Øvelse: Kombinér dine to yndlingsfarver
```

**Sektion 3 - Tal:**
```markdown
### Tal (Numbers)

Python kan arbejde med to slags tal...
```
↓ (kode med tal og beregninger)

---

## Del 3: Teknisk Opbygning

### Jupyter Notebook / Google Colab Format

#### **Filstruktur**
```
notebooks/
├── 01_Intro.ipynb
├── 02_variable.ipynb
├── 03_betingelser.ipynb
└── [fortsæt med samme mønster]
```

#### **Navngivning**
- `NN_emnenavn.ipynb` (f.eks. `04_løkker.ipynb`)
- Dansk navn (ikke engelsk) - det matcher elevernes verden
- Numerisk præfiks for rækkefølge

#### **Notebook-indstillinger (Metadata)**
- **Kernel**: Python 3.x
- **Google Colab kompatibilitet**: Sikr, at koden køres på standard Python 3 uden specielle biblioteker
- Ingen `!pip install` commands medmindre absolut nødvendigt

#### **Celle-struktur**

**Celle-typer:**
1. **Code cells** (skal være kørebare)
   - Kort, fokuseret kode
   - Velkommenteret
   - Eksempler før øvelser
   - Output skal være fornuftig

2. **Markdown cells** (forklaring)
   - Bruger standard Markdown
   - Headings (`##`, `###`) for struktur
   - Fedt (`**tekst**`) for vigtige koncepter
   - Kodekvoter (`` `variabel` ``) for syntaks

#### **Celle-længde**
- Markdown: Max 10-15 linjer før kodecelle
- Code: Max 20-30 linjer (ellers for overvældende)
- Regel: "En celle = en ide"

#### **Python Best Practices for Kurset**
- **Klart navn** på variabler: `fuldt_navn` (ikke `fn`)
- **Engelsk syntax** (Python er engelsk): `print()`, ikke `udskriv()`
- **Kommentarer på dansk**: `# Dette er min variabel`
- **Simple værktøjer**: Bare `print()`, ingen avancerede biblioteker i de første moduler
- **Input/Output klart**: Hvad indsender brugeren? Hvad får de ud?

#### **Google Colab Links**
Repository linkes via `githubtocolab.com`:

```markdown
### 01-Intro
https://githubtocolab.com/MFuglsang/python-helt-fra-bunden/blob/main/notebooks/01_Intro.ipynb
```

**Fordel**: Elever behøver ikke GitHub-konto; de klikker linket og får en Colab-kopi

---

## Del 4: Løsninger og Feedbackmateriale

### Løsningsstrukturer

#### **Option 1: Løsnings-Notebook (Anbefalet)**
```
notebooks/
├── 01_Intro.ipynb
├── 01_Intro_løsning.ipynb  ← Løsning med kommentarer
├── 02_variable.ipynb
└── 02_variable_løsning.ipynb
```

**Indhold i løsningsnotebook:**
- Samme struktur som øvelsesnotebook
- Løsninger vises med forklaring
- Kommentarer forklarer "hvorfor" denne løsning

#### **Option 2: Kommenterede Løsninger i Samme Notebook**
```python
# ØVELSE: Opret en variabel med dit navn
navn = 'Jens'  # LØSNING EKSEMPEL

# ØVELSE: Kombinér to ord
ord1 = 'Hej'
ord2 = 'verden'
resultat = ord1 + ' ' + ord2
print(resultat)  # Output: Hej verden
```

#### **Option 3: Udvidet Lærervejledning**
Se [Lærervejledning](#lærervejledning)

### Lærervejledning

Dokumentet `lærervejledning.md` skal indeholde:

1. **Modul-oversigt**: Hvad lærer eleverne hver dag?
2. **Timing**: Hvor lang tid tager hver modul?
3. **Fælles fejl**: Hvad får eleverne ofte galt? Hvordan hjælper man?
4. **Differentiering**: Hvordan hjælper man eleverne, der er hurtige? Langsomme?
5. **Løsninger**: Kort oversigt over løsninger til alle øvelser
6. **Tips til lærer**: Hvordan præsenterer man bedst?

Eksempel:
```markdown
# Lærervejledning - Python helt fra bunden

## Modul 02: Variable

### Hvad lærer eleverne?
- Hvad en variabel er
- Tre datatyper: strenge, hele tal, decimaltal
- Hvordan man kombinerer strenge

### Timing
- 45 minutter for hele modulet
- 10 min: Intro & første eksempel
- 20 min: Eleverne koder eksempler
- 15 min: Fælles diskussion af løsninger

### Fælles fejl
**Fejl 1**: Elever glemmer citationstegn omkring tekst
```python
navn = Morten  # FEJL - Python tror Morten er en variabel
navn = 'Morten'  # KORREKT
```
**Løsning**: Sig "Alt tekst skal være i citationstegn"

**Fejl 2**: Blanding af + for addition og + for tekstkombinering
```python
10 + 5  # = 15 (tal)
'10' + '5'  # = '105' (tekst!)
```
**Løsning**: Vis både eksempler side-om-side
```

---

## Del 5: Udvidelse af Kurset - Checkliste

Når du tilføjer et nyt modul, følg denne checklist:

- [ ] **Navngivning**: `NN_emnenavn.ipynb` (dansk navn)
- [ ] **Introduktion**: Korteste mulig forklaring + "hvorfor"
- [ ] **Progression**: Mindst 3 eksempler + øvelser
- [ ] **Tone**: Venlig, inkluderende, "vi" ikke "I"
- [ ] **Kode**: Kort, kommenteret, kørebare eksempler
- [ ] **Øvelser**: "Øvelse:" mærkat + konkrete instrukser
- [ ] **Fejlhåndtering**: Giv eksempler på "fejl du måske laver"
- [ ] **Link**: Tilføj til README.md med githubtocolab link
- [ ] **Løsning**: Lav løsningsnotebook eller lærerguide
- [ ] **Lærervejledning**: Opdater `lærervejledning.md`

---

## Del 6: Værktøjer og Setup

### Elever
- **Ingenting at installere** - Google Colab er browser-baseret
- **GitHub-konto**: Ikke påkrævet (githubtocolab handles det)
- **Browser**: Moderne browser (Chrome, Firefox, Safari)

### Instruktører
- **GitHub repo**: `MFuglsang/python-helt-fra-bunden`
- **Jupyter**: Lokalt, eller brug Colab direkte
- **Versionskontrol**: Git til at holde styr på ændringer
- **Format**: Jupyter `.ipynb` filer (ikke `.md` eller `.py`)

### Kvalitetskontrol Før Udgave
1. Kør alle kodeceller lokalt - sikr at de virker
2. Tjek at links til Colab virker
3. Læs teksten for stavefejl og klarhed
4. Spørg: "Ville en 12-årig uden kodeerfaringer forstå det?"

---

## Del 7: Eksempler på God Konstruktion

### ✅ God Markdown
```markdown
## Hvad er en løkke?

Forestil dig, at du skal tegne 100 stjerner. Du kunne tegne hver en enkeltvis... 
eller du kunne sige: "Gentag dette 100 gange!"

En løkke er præcis det - en måde at få computeren til at gentage en opgave mange gange.
```

### ✅ God Kodecelle
```python
# Eksempel: Udskriv tallene 1-5
for tal in range(1, 6):
    print(tal)

# Øvelse: Ændre range(1,6) til range(1,10) - hvad sker der?
```

### ❌ Dårlig Konstruktion
```python
# Meget kompleks kode uden forklaring
import numpy as np
x = np.linspace(0, 10, 1000)
y = np.sin(x)
plt.plot(x, y)
```
**Problem**: Elever har ingen ide om hvad der sker

---

## Dokumentversion

**Skill Version**: 1.0  
**Opdateret**: 2026-07-14  
**Forfatter**: Python helt fra bunden team  
**Python Version**: 3.9+

---

## Spørgsmål?

Hvis du er usikker på noget, følg disse retningslinjer:
1. "Ville en 12-årig uden kodeerfaringer forstå det?"
2. "Kan eleverne selv køre denne kode på 2 minutter?"
3. "Er tonen venlig og opmuntrende?"

Hvis ja til alle tre = du er på rette vej! ✅
