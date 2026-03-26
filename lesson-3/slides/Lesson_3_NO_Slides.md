---
marp: true
theme: default
class: invert
---

# 🔐 Python + Datasikkerhet
## Leksjon 3: Kryptografi og hemmeligheter

---

# Agenda

1. **Funksjoner:** Skrive gjenbrukbar kode
2. **Hashing:** Enveisreisen
3. **Salting:** Overvinne Rainbow Tables
4. **Kryptering:** Låse og låse opp
5. **Prosjekt:** Bygge en passordbehandler

---

# 1. Funksjoner
Slutt å copypaste kode!

```python
def hils_paa(navn):
    return f"Hei, {navn}!"

print(hils_paa("Hacker"))
```

- **Definer** én gang (`def`)
- **Kall** mange ganger
- **Returner** en verdi

---

# 2. Hashing (Enveis)
En hashfunksjon gjør data om til et "fingeravtrykk".
**Du kan ikke reversere en hash.**

Bra for:
- Lagring av passord
- Sjekke filintegritet

**Den gylne regel:** ALDRI lagre passord i klartekst!

---

# 3. Salting
Hvis to brukere har passordet `passord123`, får de samme hash.
Hackere bruker **Rainbow Tables** for å slå opp disse vanlige hashene.

**Løsningen: Salting**
Legg til tilfeldig data (salt) til passordet før hashing.
`Hash(Salt + Passord)` = Unik Hash

---

# 4. Kryptering (Toveis)
I motsetning til hashing, er kryptering reversibelt... hvis du har **Nøkkelen**.

Vi bruker **Symmetrisk Kryptering** (Fernet):
- Én nøkkel for å låse (kryptere)
- Samme nøkkel for å låse opp (dekryptere)

---

# 5. Prosjekt: Passordbehandler
Vi skal bygge et script som:
1. Genererer en hemmelig nøkkel
2. Krypterer passordene dine
3. Lagrer dem i en fil
4. Dekrypterer dem når du trenger dem

---

# Ekte feiltrinn
- **LinkedIn (2012):** Brukte SHA-1 (rask) uten salt. Millioner av passord ble knekket.
- **RockYou (2009):** Lagret passord i klartekst. Komplett katastrofe.

**Konklusjon:** Meningsfull sikkerhet krever lag på lag (Hashing + Salting + Kryptering).
