[🇬🇧 English Version](README.md)

# Leksjon 3: Kryptografi og hemmeligheter i kode

## Oversikt
I denne leksjonen skal vi utforske hvordan vi beskytter data ved hjelp av Python. Vi beveger oss utover enkle skript og lærer om **funksjoner** og **moduler** for å bygge gjenbrukbar kode. Deretter dykker vi ned i **kryptografi**, lærer forskjellen på hashing og kryptering, og bygger en enkel pedagogisk passordbehandler.

## Agenda
1.  **Leksegjennomgang:** Ordbokangrep og Salting
2.  **Python Power-Up:** Funksjoner og Moduler
3.  **Hashing:** Enveisgater (MD5, SHA-256)
4.  **Kryptering:** Låse og låse opp med `cryptography`
5.  **Prosjekt:** Bygge en passordbehandler
6.  **Ekte feiltrinn:** LinkedIn & RockYou

## Oppsett
Du trenger `cryptography`-biblioteket for denne leksjonen.
```bash
pip install cryptography
```

## Filer
- `notebooks/`: Interaktive Jupyter notebooks for leksjonen.
- `slides/`: Presentasjonslysbilder.
- `generated/`: (Opprettes under leksjonen) Krypterte passordfiler.

## Læringsmål

Etter denne leksjonen skal eleven kunne:

- Forklare forskjellen mellom hashing og kryptering.
- Forklare hvorfor salt er viktig ved lagring av passord.
- Beskrive hvorfor MD5 ikke er egnet for sikker passordlagring.
- Lage små gjenbrukbare funksjoner for å kryptere og hente data.

## Viktig merknad

- Passordbehandleren i denne leksjonen er en pedagogisk demo. En ekte passordbehandler trenger også sikker nøkkellagring, autentisering og bedre feilhåndtering.
