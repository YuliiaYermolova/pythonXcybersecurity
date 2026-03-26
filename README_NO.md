[🇬🇧 English Version](README.md)

# Python + Datasikkerhet Kurs

Velkommen til kurset i Python + Datasikkerhet! Dette repositoriet inneholder alt kursmateriell, Jupyter notebooks og presentasjoner.

## Arbeidsflyt for Studenter

Følg disse stegene for å sette opp din egen kopi av kursmateriellet og holde det oppdatert etter hvert som nye leksjoner blir lagt ut.

### 1. Fork Repositoriet (Lag din kopi)
Først må du lage din egen kopi av dette repositoriet på GitHub.
1. Gå til hovedsiden for repositoriet: [https://github.com/Cha-IT/pythonXcybersecurity](https://github.com/Cha-IT/pythonXcybersecurity)
2. Klikk på **Fork**-knappen øverst i høyre hjørne.
3. Dette oppretter en kopi under din egen GitHub-konto.

### 2. Klon din Fork i VS Code (Last ned)
Nå skal du laste ned din kopi til din datamaskin.
1. Åpne **VS Code**.
2. Trykk `Ctrl+Shift+P` (eller `Cmd+Shift+P` på Mac) for å åpne Command Palette.
3. Skriv `Git: Clone` og velg det.
4. Lim inn URL-en til **DITT FORKEDE REPOSITORIE** (f.eks. `https://github.com/DITT_BRUKERNAVN/pythonXcybersecurity.git`).
5. Velg en mappe på din datamaskin hvor du vil lagre det.
6. Når du blir spurt, klikk **Open** for å åpne det nye repositoriet i VS Code.

### 3. Legg til Upstream Remote (Koble til lærerens)
For å få oppdateringer fra læreren (nye leksjoner), må du fortelle Git hvor det originale repositoriet er.
1. Åpne Terminalen i VS Code (`Ctrl+` ` eller `Terminal > New Terminal`).
2. Kjør følgende kommando nøyaktig:
   ```bash
   git remote add upstream https://github.com/Cha-IT/pythonXcybersecurity.git
   ```
3. For å sjekke at det virket, kjør:
   ```bash
   git remote -v
   ```
   Du skal nå se både `origin` (din fork) og `upstream` (lærerens repo).

### 4. Hvordan få oppdateringer (Nye leksjoner)
Når en ny leksjon er lagt ut, følger du disse stegene for å laste den ned til ditt prosjekt:

1. Åpne Terminalen i VS Code.
2. Kjør disse kommandoene:
   ```bash
   git fetch upstream
   git merge upstream/main
   ```
3. Dytt (push) oppdateringene til din egen GitHub fork:
   ```bash
   git push origin main
   ```

Nå har du de nyeste filene!

## Feilsøking
- **Merge Conflicts:** Hvis du har redigert en fil som også ble endret i oppdateringen, kan Git klage over en "konflikt". Siden du stort sett jobber i dine egne filer eller oversatte notebooks, bør ikke dette skje ofte. Hvis det skjer, vil VS Code hjelpe deg med å løse det.
- **Branch Navn:** Denne guiden antar at hoved-branchen heter `main`. Hvis den heter `master`, bytt ut `main` med `master` i kommandoene over.
- **Permission Denied:** Sørg for at du er logget inn på GitHub i VS Code.
