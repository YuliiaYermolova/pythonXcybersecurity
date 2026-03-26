---
marp: true
theme: default
class: invert
---

# 🔐 Python + Cybersikkerhet
## Leksjon 2: Data, Filer og Digital Etterforskning

---

# Agenda

1.  **Prosess:** Digital Etterforskning ("Hva skjedde?")
2.  **Inndata:** Lese Filer i Python
3.  **Data:** Parsing av Strenger & Lister
4.  **Logikk:** Ordbøker (Dictionaries) & Telling
5.  **Utdata:** Identifisere et Angrep

---

# 🕵️ Digital Etterforskning

Når et system er hacket, gjetter vi ikke. Vi ser etter **bevis**.

**Bevis finnes vanligvis i logger.**

En **Logg** er en fil der en server skriver ned hva den gjør.
> "10:00 - Bruker 'Admin' logget inn."
> "10:05 - Bruker 'Hacker' feilet passord."

---

# 📂 Lese Filer

Python gjør det enkelt å åpne filer.

```python
# 'with'-blokken håndterer automatisk lukking av filen
with open("logger.txt", "r") as file:
    innhold = file.read()
    print(innhold)
```

- `"r"` = Lese-modus
- `"w"` = Skrive-modus (Overskriver!)
- `"a"` = Legge til på slutten 

---

# ✂️ Parsing av Strenger

Logger er bare lange strenger med tekst. Vi må kutte dem opp.

**`.split()`-metoden:**

```python
linje = "192.168.1.5 - GET /index.html"
deler = linje.split(" - ")
# Resultat: ["192.168.1.5", "GET /index.html"]

ip = deler[0]
handling = deler[1]
```

---

# 📚 Ordbøker (Nøkkel-Verdi-par)

Hvis vi vil telle hvor mange ganger en IP dukker opp, er en **Liste** vanskelig å bruke.
En **Dictionary** (ordbok) er som en ekte ordbok: Du slår opp et ord (Nøkkel) for å få en definisjon (Verdi).

```python
# Nøkkel: IP-adresse, Verdi: Antall
tellinger = {
    "192.168.1.1": 5,
    "10.0.0.5": 120
}

# Hente ut data
print(tellinger["10.0.0.5"]) # Skriver ut 120
```

---

# ⚔️ Angrepsmønsteret: Brute Force

**Brute Force:** Prøve hvert eneste mulige passord til ett virker.

**Logg-signaturen:**
1.  Samme IP-adresse...
2.  Prøver å `POST /login`...
3.  Får `401 Unauthorized`-feil...
4.  ...**Hundrevis** av ganger i minuttet.

---

# 🎓 Oppsummering

- **Etterforskning** handler om å lese historien (logger).
- **Filer** åpnes med `open()` og leses vanligvis med løkker.
- **Parsing** gjør tekst til data (`.split()`).
- **Ordbøker** hjelper oss å telle og gruppere data.
- **Brute Force**-angrep er høylytte og lette å se i logger!

**Neste Leksjon:** Kryptering og Hemmeligheter!
