---
title: Bærekraftskontoplan og -post
description: 'Finn ut hvordan du administrerer bærekraftskontoplan, kategorier og underkategorier og detaljer om bærekraftsposter.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Bærekraftskontoplan og finans

## Bærekraftskontoplan

Bærekraftskontoplanen danner den grunnleggende strukturerte listen som brukes til å registrere alle utslippsdata. Den fungerer som et rammeverk som kategoriserer og organiserer bærekraftskontoer basert på attributtene, for eksempel området eller andre grupperinger. Hver konto får vanligvis tilordnet en unik kode eller et unikt nummer for enkel referanse og sporing. Den har samme struktur som en tradisjonell kontoplan, men er spesialtilpasset for å overvåke bærekraftrelaterte data og måleverdier i en organisasjon.

Brukere kan legge til kategorier og underkategorier for bærekraftskonto for å definere hvordan systemet skal fungere. De kan dermed velge dedikerte utslipp de vil spore, utslippsfaktorer, formler og lignende konfigurasjoner.

> [!NOTE]
> Det finnes tre utslippsområder basert på standardene for klimagass:
>
> - **Utslipp i område 1** omfatter utslipp fra stasjonær og mobil forbrenning og fra utilsiktede flyktige utslipp.
> - **Utslipp i område 2** omfatter indirekte utslipp fra produksjonen av energi som kjøpes fra strømleverandører.
> - **Utslipp i område 3** omfatter et bredt spekter av utslipp, fra kjøpte varer og tjenester og kapitalvarer, via drivstoff- og energirelaterte aktiviteter, oppstrøms og nedstrøms transport, generert avfall, forretningsreiser og til pendling for ansatte og så videre.

Du kan gjøre følgende fra bærekraftskontoplanen:

- Vise rapporter som viser bærekraftsposter og saldoer.
- Åpne bærekraftskontokortet for å legge til eller endre innstillinger.
- Vis kategorien og underkategorien for kontoen. 
- Vis separate saldoer for hvert utslipp for én konto.
- Legg til én eller flere dimensjoner i hver konto, og angi dimensjonsfiltre.

Du kan legge til, endre eller slette bærekraftskontoer. For å unngå avvik kan du imidlertid ikke slette en bærekraftskonto hvis en eller flere poster er knyttet til den.

### Legg til eller endre kontoer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bærekraftskontoplan** og velg deretter den relaterte koblingen.
2. På siden **Bærekraftskontoplan** kan du åpne hver bærekraftskonto og deretter legge til eller endre innstillinger. Hold markøren over et felt for å lese en kort beskrivelse.

Når det gjelder kontoer av typen **Total** må du angi feltet **Sammentelling**.

Når det gjelder kontoer av typen **Til-sum**, angir innrykksfunksjonen **Sammentelling**-feltet automatisk. Etter at du har definert alle kontoene, velger du handlingen **Rykk inn bærekraftskontoplan** for å kjøre innrykksfunksjonen og angi **Sammentelling**-feltet.

> [!IMPORTANT]
> Innrykksfunksjonen skriver over verdien i alle felter for **Til-sum**-kontoer. Hvis du angav definisjoner i **Sammentelling**-feltet for **Til-sum**-kontoer før du kjørte innrykksfunksjonen, må du derfor angi dem på nytt etter at du har kjørt den.

### Slett kontoer

Du kan slette en bærekraftskonto. Du må imidlertid først kontrollere at ingen poster er knyttet til den. Business Central forhindrer deg fra å slette en bærekraftskonto hvis en eller flere poster er knyttet til den.

## Kontokategorier

Brukere må legge til en kategori i hver bærekraftskonto for å definere hvordan systemet skal fungere. De kan velge utslippsområder, dedikerte utslipp de vil spore, formler og lignende konfigurasjoner.

Hvis du vil se gjennom bærekraftskontokategorier, følger du denne fremgangsmåten:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bærekraftskontokategorier** og velg deretter den relaterte koblingen.
2. På siden **Bærekraftskontokategorier** kan du redigere den eksisterende listen eller opprette en ny kategori. Hvis du vil opprette en ny kategori, velger du handlingen **Ny**.
3. Angi feltene **Kode** og **Beskrivelse**.
4. Velg et av områdealternativene i feltet **Utslippsområde**.
5. Velg gassutslippene du vil spore. For øyeblikket er følgende alternativer tilgjengelige: **CO2**, **CH4** og **N2O**. Du kan velge enhver kombinasjon du vil spore, men du må velge minst ett utslipp.
6. Du kan velge beregningsgrunnlaget (formelen) du vil bruke i utslippsberegninger, i feltet **Beregningsgrunnlag**, hvis du ikke vet den nøyaktige utslippsmengden. Du kan velge et av følgende alternativer: **Drivstoff/elektrisitet**, **Avstand**, **Installasjon** eller **Egendefinert**.

    > [!NOTE]
    > Hvis settet med tilgjengelige formler i feltet **Beregningsgrunnlag** ikke er nok, kan du utvide feltet og legge til flere beregninger i systemet du vil bruke i bærekraftkladdene.

7. Hvis du valgte **Egendefinert** i feltet **Beregningsgrunnlag**, kan du konfigurere en egendefinert beskrivelse i feltet **Egendefinert verdi**.

Hvis du angir feltet **Beregningsgrunnlag**, forklarer tabellen nedenfor hvordan systemet beregner utslipp basert på alternativet du valgte. (I denne tabellen representerer *EF* representerer **Utslippsfaktor**-verdien du kan konfigurere på siden **Underkategori for bærekraftskonto**.)

| Utslippstype | Beregningsgrunnlag | Formel | Merknad |
|---------------|------------------------|---------|---------|
| **Område 1** | | | |
| Stasjonær forbrenning | Drivstoff/elektrisitet | *Utslipp* = *Drivstoff* &times; *EF* | *Drivstoff* = mengde drivstoff som brukes til kjeler, varmeovner, termiske oksidanter og så videre |
| Mobil forbrenning | Drivstoff/elektrisitet | *Utslipp* = *Drivstoff* &times; *EF* | *Drivstoff* = mengde drivstoff som brukes til kjøretøy på vei eller utenfor vei, jernbane og så videre |
| | | *Utslipp* = *Avstand* &times; *EF* | *Avstand* = Kjørelengde for kjøretøy på vei eller utenfor vei, jernbane og så videre |
| Flyktige utslipp | Installasjon | *Utslipp* = *Installasjonsmultiplikator* &times; *Egendefinert mengde* &divide; 100 &times; *Tidsfaktor* | *Egendefinert mengde* = monteringstap, årlig lekkasjerate og så videre |
| **Område 2** | | | |
| Kraftleverandører | Drivstoff/elektrisitet | *Utslipp* = *Elektrisitet* &times; *EF* | *Drivstoff/elektrisitet* = Elektrisitetsmengde, dampmengde, varmeenhet og så videre |
| | Egendefinert | *Utslipp* = *Egendefinert mengde* &times; *EF* | *Egendefinert mengde* = termisk enhet, tonntime og så videre |
| **Område 3** | | | |
| Kjøpte varer og tjenester, og kapitalvarer | Egendefinert | *Utslipp* = *Egendefinert mengde* &times; *EF* | *Egendefinert mengde* = kostnad (finans) og så videre |
| Oppstrøms transport og distribusjon | Avstand | *Utslipp* = *Avstand* &times; *EF* | |
| | Avstand | *Utslipp* = *Avstand* &times; *Multiplikator* &times; *EF* | *Multiplikator* = Tonn last |
| Nedstrøms transport og distribusjon | Avstand | *Utslipp* = *Avstand* &times; *EF* | |
| | Avstand | *Utslipp* = *Avstand* &times; *Multiplikator* &times; *EF* | *Multiplikator* = Tonn last |
| Avfall generert i drift og sluttbehandling av solgte produkter | Egendefinert | *Utslipp* = *Egendefinert mengde* &times; *EF* | *Egendefinert mengde* = avfall |
| Forretningsreiser og pendling for ansatte | Avstand | *Utslipp* = *Avstand* &times; *EF* | *Avstand* = kjørelengde av brukt firmabil, leiebil, tog, fly og så videre |
| | Egendefinert | *Utslipp* = *Egendefinert mengde* &times; *EF* | *Egendefinert beløp* = hotellopphold |
| | Drivstoff/elektrisitet | *Utslipp* = *Drivstoff* &times; *EF* | *Drivstoff* = Mengde drivstoff brukt i firmabilen, leiebil og så videre |

## Kontounderkategori

Brukere må legge til en underkategori i hver bærekraftskonto. Denne underkategorien definerer utslippsfaktorene som brukes i formlene, basert på valget for utslippssporing i kategorien i bærekraftskontoen.

Hvis du vil se gjennom underkategorier i bærekraftskonto, følger du denne fremgangsmåten:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Underkategorier for bærekraftskonto** og velg deretter den relaterte koblingen. 
2. På siden **Underkategorier for bærekraftskonto** kan du redigere den eksisterende listen eller opprette en ny kategori. Hvis du vil opprette en ny kategori, velger du handlingen **Ny**.
3. Angi feltene **Kode** og **Beskrivelse**.
4. Basert på gassutslippene du vil spore i kategorien i bærekraftskontoen og koble denne underkategorien til, kan du også angi en eller flere utslippsfaktorer: 

    - **Utslippsfaktor CO2** – Utslippsfaktoren for utslipp av karbondioksid (CO<sub>2</sub>).
    - **Utslippsfaktor CH4** – Utslippsfaktoren for metanutslipp (CH<sub>4</sub>).
    - **Utslippsfaktor N2O** – Utslippsfaktoren for utslipp av lystgass (N<sub>2</sub>O).

5. Hvis underkategorien er relatert til fornybar energi, velger du feltet **Fornybar energi**.

> [!NOTE]
> Feltene **Importer data** og **Importer fra** er ment for potensiell integrering med eksterne systemer som brukes til å samle inn utslippsfaktorer. Disse feltene kan imidlertid som standard ikke brukes som en funksjon i **lanseringsbølge 1 i 2024**.

## Bærekraftsposter

Bærekraftspost lagrer historikken for alle bokførte bærekraftstransaksjoner og organiserer alle utslippsdata i henhold til bærekraftskontoplanen. Når en bruker bokfører bærekraftskladden, registreres alle viktige data der. Alle aktive rapporter genereres basert på bærekraftspostene.

Hvis du vil åpne denne posten for en bestemt konto, bruker du handlingen **Poster** på siden **Bærekraftskontoplan**. Hvis du vil åpne alle postene, velger du ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skrive inn **Bærekraftsposter** og velge den relaterte koblingen. Hold musepekeren over et felt for å lese en kort beskrivelse.

> [!IMPORTANT]
> Etter at du har bokført dataene i bærekraftsposten, kan du ikke slette den. Hvis du har gjort en feil, kan du bokføre en tilbakeføringstransaksjon som har de samme detaljene, men bruker negativt fortegn for mengden.

## Se også

[Finans](finance.md)  
[Oversikt over bærekraftsadministrasjon](finance-manage-sustainability.md)  
[Bærekraftsoppsett](finance-sustainability-setup.md)  
[Slik registrerer du utslipp](finance-sustainability-journal.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
