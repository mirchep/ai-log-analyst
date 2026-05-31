# AI Log Analyst

## AI-Assisted Windows Security Log Analysis with Python

### Cilj projekta

Primarni cilj projekta je **učenje novih tehnologija kroz praktičan rad**, a ne izrada proizvoda pod svaku cijenu.

Kroz projekat želim naučiti:

* Python
* Obradu logova
* Analizu sigurnosnih događaja
* AI integraciju
* Git i GitHub workflow
* Izradu dashboarda

Potencijalni bonus cilj je priprema materijala za buduće konferencijsko predavanje.

---

# Definicija projekta

Naziv repozitorija:

```text
ai-log-analyst
```

Opis projekta:

```text
AI-Assisted Windows Security Log Analysis with Python
```

---

# Kreiranje Git repozitorija

Otvoren je lokalni Git repozitorij.

Inicijalizacija:

```bash
git init
```

Konfiguracija korisnika:

```bash
git config --global user.name "Mirche P"
git config --global user.email "email@example.com"
```

Provjera konfiguracije:

```bash
git config --global --list
```

---

# Struktura projekta

Trenutna struktura:

```text
ai-log-analyst/
│
├── logs/
├── src/
├── docs/
├── tests/
├── README.md
└── .gitignore
```

## Objašnjenje foldera

### logs/

Sadrži log fajlove za analizu.

Primjeri:

```text
security.csv
sample.evtx
iis.log
```

---

### src/

Sadrži sav Python kod.

Primjeri budućih fajlova:

```text
main.py
parser.py
detector.py
reporter.py
```

---

### docs/

Dokumentacija projekta.

---

### tests/

Automatski testovi.

---

# Važna Git napomena

**Git ne prati prazne foldere.**

Ako folder ne sadrži nijedan fajl, neće biti uključen u commit.

Zbog toga su u prvom commit-u sačuvani samo:

```text
README.md
.gitignore
```

---

# Prvi commit

Dodavanje fajlova:

```bash
git add .
```

Kreiranje prvog commit-a:

```bash
git commit -m "Initial project structure"
```

Provjera statusa:

```bash
git status
```

Rezultat:

```text
nothing to commit, working tree clean
```

To znači da je repozitorij ispravno postavljen.

---

# Naučene lekcije

## Git

* `git init`
* `git add`
* `git commit`
* `git status`
* `git log --oneline`

---

## Python

Prvi program:

```python
print("AI Log Analyst")
```

Pokretanje:

```bash
python src/main.py
```

---

## Rad sa putanjama

Koristiti:

```python
from pathlib import Path
```

umjesto hardkodiranih relativnih putanja.

Primjer:

```python
base_dir = Path(__file__).parent.parent
log_file = base_dir / "logs" / "security.csv"
```

---

## Važna razlika

### Radni direktorij (cwd)

```python
Path.cwd()
```

predstavlja direktorij iz kojeg je program pokrenut.

### Lokacija skripta

```python
Path(__file__)
```

predstavlja lokaciju Python fajla.

Ova razlika je bila uzrok greške:

```text
FileNotFoundError
```

prilikom otvaranja CSV fajla.

---

# Plan za prvu sedmicu

## Faza 1

Napraviti:

```text
src/main.py
```

i uspješno ga pokrenuti.

---

## Faza 2

Napraviti:

```text
logs/security.csv
```

sa testnim podacima.

---

## Faza 3

Napisati funkcionalnost za:

* učitavanje CSV fajla
* brojanje zapisa
* prikaz osnovne statistike

---

# Dugoročni plan razvoja

## Verzija 0.1

CSV parser

## Verzija 0.2

Brojanje događaja

## Verzija 0.3

Detekcija brute-force napada

## Verzija 0.4

Podrška za EVTX fajlove

## Verzija 0.5

AI analiza incidenata

## Verzija 0.6

Streamlit dashboard

---

# Ključna ideja projekta

Ne pokušavati odmah napraviti SOC sistem.

Prvo naučiti:

* obradu podataka
* Python ekosistem
* sigurnosnu analitiku
* AI integraciju

korak po korak, kroz stvaran projekat.

---

# Trenutni status

Završeno:

* Git repozitorij
* GitHub repozitorij
* Osnovna struktura projekta
* Prvi Python program
* Prvi CSV dataset
* Rad sa pathlib putanjama

Sljedeći korak:

**Izrada većeg i realističnijeg Windows Security log dataseta (200+ događaja) i razvoj prvog parsera za analizu događaja.**