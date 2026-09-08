# Stanislav Brysin
**AI Automation Engineer**

Python | n8n | API's | LLM-workflows | Testen | CI/CD | Datapipelines

[GitHub](https://github.com/BrysinSS) · [Portfolio](README.md)

## Profiel

Ik bouw automatiseringssystemen met Python, API's, n8n en LLM-integraties. Mijn nadruk ligt op deterministische verwerking, gestructureerde gegevens, testen en reproduceerbare pipelines. Ik heb ongeveer acht jaar zelfstandig een productiebedrijf geleid. Ik zoek een functie in automatisering of toegepaste AI in Nederland.

## Geselecteerde technische projecten

### AIVS — commercieel systeem voor AI-zichtbaarheidsaudits

- Een geautomatiseerde auditpipeline met acht fasen gebouwd, met specificaties, validatiepoorten en controles in elke fase.
- Deterministische extractie gecombineerd met LLM-redenering.
- Bewijsgerichte controles voor claims en Ed25519-attestatie van auditpakketten geïmplementeerd, waarbij aanwezigheid en verificatie van de handtekening afzonderlijk worden gerapporteerd.
- De privésuite geverifieerd: 4.308 geslaagd, 12 overgeslagen en 0 mislukte tests (4.320 verzameld; september 2026).
- Een audit in `strict_production` uitgevoerd met 27 Nederlandse zoekvragen en vier modelproviders: 108/108 geldige antwoorden en 0 niet-onderbouwde of verboden claims in het eindpakket.
- Rapportuitvoer in zes talen gebouwd; de gedocumenteerde productiecase mat Nederlands en leverde gevalideerde Nederlandse en Russische artefacten.

[Praktijkbeschrijving](portfolio/aivs-case-study/README.md) · [geanonimiseerd productievoorbeeld](portfolio/aivs-case-study/sample/README.md) · [testresultaat](portfolio/aivs-case-study/TESTING.md). De implementatie blijft privé; het openbare bewijs bevat meetresultaten, Stage H-validatie en herkomsthashes.

### AI Accountant Orchestra — transactieverwerking in Python

- Een deterministische, YAML-gestuurde Python-pipeline voor transacties gebouwd, met bronvalidatie, normalisatie, inclusieve filtering op kalenderkwartaal (`Qn-YYYY`), samenvattingen en een geconfigureerde btw-berekeningsdemonstratie.
- JSON- en Markdown-artefacten en geordende NDJSON-staplogs opgeleverd, met fail-fast-afhandeling van verplichte validatie, zichtbare foutartefacten en CLI-exitcodes voor succes, ongeldige invoer en uitvoeringsfouten.
- 37 geslaagde pytest-tests geverifieerd, inclusief end-to-end-scenario's voor succes en fouten; GitHub Actions voert de suite uit met Python 3.11 en 3.12.

### Onderzoeksautomatisering — Literature Parser en PDF Hunter

- Een n8n-workflow gebouwd voor het verzamelen en normaliseren van Crossref- en OpenAlex-metadata, met deduplicatie op DOI of titel.
- Een Python-tool gebouwd die PDF-links zoekt via officiële metadata-API's en documentendpoints, met expliciete bronprioriteit en gestructureerde CSV-uitvoer.
- De bestandsoverdracht, beperkingen van DOI-formaten en foutafhandeling gedocumenteerd.

## Ondernemersachtergrond

Ongeveer acht jaar zelfstandig een productiebedrijf geleid.

## Technische vaardigheden

Python, n8n, API's, YAML, gestructureerde gegevens, datapipelines, LLM-integraties, hybride deterministische/AI-workflows, pytest en GitHub Actions / CI. De openbare repositories tonen CI; een uitgerolde pipeline voor continuous delivery wordt niet geclaimd.

Ontwikkeltools: Claude Code en Codex voor AI-ondersteunde ontwikkeling.

## Aanvullingen voor dit concept — verwijderen voor verzending

Dit is een inhoudelijk concept, geen volledige loopbaanbeschrijving. Contactgegevens, datums, bedrijfsnaam, opleiding, woonplaats, werkvergunning en taalniveaus zijn niet aangeleverd. Er zijn geen taalniveaus toegevoegd of gewijzigd. Zie PORTFOLIO_REPORT.md voor de punten met NEEDS_USER_CONFIRMATION.
