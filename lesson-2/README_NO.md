[🇬🇧 English Version](README.md)

# Leksjon 2: Data, Filer og Digital Etteforsking

Denne leksjonen fokuserer på hvordan man håndterer data i Python ved å lese filer og analysere serverlogger for å oppdage dataangrep.

## 📂 Innhold

- **notebooks/**: Interaktive Jupyter Notebooks.
  - `Lesson_2_EN.ipynb`: Engelsk versjon.
  - `Lesson_2_NO.ipynb`: Norsk versjon.
- **slides/**: Presentasjonslysbilder.
  - `Lesson_2_EN_Slides.md`
  - `Lesson_2_NO_Slides.md`
- **data/**: Eksempel på loggfiler for analyse.
  - `server_logs.txt`: En simulert serverloggfil som inneholder normal trafikk og et brute-force-angrep.

## 🚀 Kom i gang

1.  **Åpne Notebook:** Åpne `notebooks/Lesson_2_NO.ipynb` i VS Code.
2.  **Sjekk Data:** Sørg for at du har tilgang til `data/server_logs.txt`. Notebooken er konfigurert til å se etter `../data/server_logs.txt`.
3.  **Kjør Cellene:** Følg instruksjonene for å lære hvordan du åpner, leser og analyserer filer.

## 🔍 Nøkkelkonsepter

-   **Fil-I/O:** `open()`, `read()`, `readlines()`.
-   **Streng-parsing:** `.split()`, `.strip()`.
-   **Ordbøker (Dictionaries):** Nøkkel-Verdi-par for å telle data.
-   **Logganalyse:** Identifisere mistenkelige mønstre (Brute Force).

## Læringsmål

Etter denne leksjonen skal eleven kunne:

- Lese en loggfil inn i Python og forklare hvorfor `with open(...)` er nyttig.
- Dele en logglinje opp i meningsfulle deler som IP-adresse og statuskode.
- Bruke en ordbok for å telle gjentatte hendelser.
- Forklare hvorfor gjentatte `401`-responser fra samme IP kan tyde på et brute-force-angrep.

## Rask egenkontroll

- Hva hjelper `with`-setningen oss med når vi jobber med filer?
- Hvorfor deler vi opp hver logglinje før vi analyserer den?
- Hvorfor kan mange mislykkede innlogginger fra én IP være mistenkelig?
