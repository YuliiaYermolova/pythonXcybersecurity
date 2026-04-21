---
marp: true
theme: default
class: invert
---

# 🔐 Python + Cybersikkerhet
## Leksjon 1: Python Tenker Som en Hacker

---

# Agenda

1. **Tankesett:** Angriper vs. Forsvarer
2. **Oppsett:** Python & VS Code
3. **Grunnleggende:** Variabler, Løkker, & Lister
4. **Verktøy:** `requests`-biblioteket
5. **Rekognosering:** Lese HTTP-overskrifter (Headers)
6. **Angrep:** Introduksjon til XSS (Cross-Site Scripting)

---

# 🧠 Cybersikkerhets-tankesettet

<div class="columns">
<div>

### Angriperen ⚔️
- Trenger å finne **én** åpen dør.
- Leter etter mønstre og feil.
- "Hvordan kan jeg ødelegge dette?"

</div>
<div>

### Forsvareren 🛡️
- Må sikre **alle** dører.
- Må vite hvordan angriperen tenker.
- "Hvordan kan jeg fikse dette?"

</div>
</div>

---

# 🐍 Python Grunnleggende

### Variabler
Beholdere for å lagre dataverdier.

```python
target_url = "https://example.com"
port = 80
is_secure = False
```

### Lister
Ordnet samling av elementer.

```python
admin_pages = ["/admin", "/login", "/config"]
```

---

# 🔄 Løkker (Automatisering)

Hackere skriver ikke manuelt; de skripter!

```python
for side in admin_pages:
    print("Skanner: " + side)
```

**Utdata:**
```
Skanner: /admin
Skanner: /login
Skanner: /config
```

---

# 🌐 `requests`-biblioteket

Pythons måte å surfe på nettet.

```python
import requests

response = requests.get("https://example.com")

print(response.status_code) # 200 = OK, 404 = Ikke funnet
print(response.text)        # HTML-innholdet
```

---

# 🕵️ Lese HTTP-overskrifter (Headers)

Skjult metadata sendt av serveren.

**Viktige Sikkerhetsoverskrifter:**
- `Strict-Transport-Security`: Tvinger bruk av HTTPS
- `X-Frame-Options`: Hindrer at nettstedet legges i en iframe (Clickjacking)
- `Content-Security-Policy`: Begrenser hvor ressurser kan lastes fra og reduserer XSS-risiko

En manglende header er en grunn til å undersøke videre, ikke automatisk bevis på en feil.

---

# 💥 Introduksjon til XSS (Cross-Site Scripting)

Injisere ondsinnede skript i pålitelige nettsteder.

**Et rødt flagg:** `<script>`-tagger i brukerinndata.

En `<script>`-tag alene beviser ikke XSS. Det viktige er om angriperkontrollert input kan injiseres og kjøres.

```python
# Enkel Python-sjekk
if "<script>" in response.text:
    print("⚠️ Krever gjennomgang: <script>-mønster funnet.")
```

---

# 🎓 Oppsummering

- **Python** er et kraftig verktøy for automatisering.
- **Moduler** som `requests` lar oss samhandle med nettverket.
- **Sikkerhetsoverskrifter** er første forsvarslinje.
- **XSS**-sjekker starter ofte med enkle mønstre, men ekte verifisering krever kontekst.

**Neste gang:** Filer, Logger, og Digital Etterforskning!
