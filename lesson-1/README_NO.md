[🇬🇧 English Version](README.md)

# Leksjon 1: Python tenker som en hacker

Denne mappen inneholder alt undervisningsmateriell for den første leksjonen i kurset Python + Datasikkerhet.

## 📂 Innhold

- **notebooks/**: Interaktive Jupyter Notebooks for studenter.
  - `Lesson_1_EN.ipynb`: Engelsk versjon.
  - `Lesson_1_NO.ipynb`: Norsk versjon.
- **slides/**: Presentasjonslysbilder for instruktøren.
  - `Lesson_1_EN_Slides.md`: Engelske lysbilder.
  - `Lesson_1_NO_Slides.md`: Norske lysbilder.
- `requirements.txt`: Python-avhengigheter som trengs for leksjonen.
- `lesson-plan.md`: Den opprinnelige leksjonsplanen.

## Læringsmål

Etter denne leksjonen skal eleven kunne:

- Forklare hva `requests.get()` gjør og hva et HTTP-svar inneholder.
- Gjenkjenne viktige sikkerhetsoverskrifter som `X-Frame-Options`, `Strict-Transport-Security` og `Content-Security-Policy`.
- Bruke variabler, lister og løkker for å automatisere en enkel websjekk.
- Forklare hvorfor en manglende header eller et `<script>`-mønster er et spor som må undersøkes videre, ikke automatisk bevis på en sårbarhet.

## Viktig merknad

- Notebooken bruker `verify=False` kun i en kontrollert lab/demo-sammenheng. I virkelige systemer skal sertifikatproblemer løses, ikke ignoreres.

## 🚀 Kom i gang

### Forutsetninger

1.  **Installer Python:** Last ned og installer Python fra [python.org](https://www.python.org/).
2.  **Installer VS Code:** Last ned fra [code.visualstudio.com](https://code.visualstudio.com/).
3.  **Utvidelser:** Installer følgende utvidelser i VS Code:
    -   **Python** (Microsoft)
    -   **Jupyter** (Microsoft)
    -   **Marp for VS Code** (Marp Team) - *Valgfritt, for å vise lysbilder som presentasjon.*

### Installasjon

Åpne en terminal i denne mappen og kjør:

```bash
pip install -r requirements.txt
```

### Kjøre leksjonen

1.  Åpne `notebooks/Lesson_1_NO.ipynb` (eller EN) i VS Code.
2.  Velg Python-kjernen (øverst til høyre).
3.  Kjør kodeceller ved å bruke `Shift + Enter`.

### Vise presentasjon

1.  Åpne `slides/Lesson_1_NO_Slides.md`.
2.  Klikk på "Open Preview to the Side"-ikonet (øverst til høyre).
3.  For å presentere, klikk på Marp-ikonet i verktøylinjen og velg "Toggle Marp Preview" eller eksporter til PDF/HTML.
