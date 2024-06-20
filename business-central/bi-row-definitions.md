---
title: Raddefinisjoner i finansrapportering
description: Beskriver hvordan raddefinisjoner i finansrapportering fungerer.
author: kennieNP
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# Raddefinisjoner i finansrapportering

Raddefinisjoner i finansrapporter gir et sted for beregninger som ikke kan utføres direkte i kontoplanen. Du kan for eksempel opprette delsummer for kontogrupper og deretter inkludere denne summen i andre totaler. Du kan også beregne mellomliggende trinn som ikke vises i sluttrapporten.

## Opprett eller rediger en raddefinisjon

Følg denne fremgangsmåten for opprette eller redigere en raddefinisjon:

1. På siden for **Finansrapporter** velger du den relevante finansrapporten, og deretter velger du handlingen **Rediger raddefinisjon**.
1. Velg handlingene **Sett inn finanskontoer**, **Sett inn CF-kontoer** og **Sett inn kostnadstyper** for å opprette en rad for hvert finanselement du vil analysere. Du kan for eksempel ha én rad for aktuelle aktiva og en annen rad for aktiva. For inspirasjon kan du se finansrapporter i demoselskapet CRONUS.

    > [!NOTE]
    > Feltet **Radnr.** viser de 10 første tegnene i en identifikator, for eksempel et kontonummer. Hvis du legger til elementer med identifikatorer som begynner med de samme ti tegnene, vil du ha duplikater fra felte **Radnr.** . Du kan om nødvendig redigere identifikatorer manuelt etter at du har satt inn elementene. De fullstendige identifikatorene vises i feltet **Sammentelling**.

> [!NOTE]
> Kolonnene som du definerer på hver linje i rapportdefinisjonen, representerer kolonner tre og oppover på siden **Finansrapport**. De to første kolonnene, **Radnr.** og **Beskrivelse**, er faste.  

## Innebygde raddefinisjoner

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder eksempler på raddefinisjoner som kan hjelpe deg med å komme raskt i gang med å konfigurere finansrapporter som passer dine behov.

<!-- update this when we release the new templates in 24.1
| Row definition code | Description | How to use this row definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 | 
-->

> [!NOTE]
> Eksempelfinansrapportene i [!INCLUDE[prod_short](includes/prod_short.md)] er ikke klare til bruk som standard. Avhengig av hvordan du definerer finanskontoer, dimensjoner, finanskontokategorier og budsjetter, må du justere rad- og kolonnedefinisjonene og finansrapportene som bruker dem, slik at de samsvarer med oppsettet.

## Bruk finanskontokategoriene til å endre oppsettet for regnskapsoppgjørene

Du kan bruke finanskontokategoriene til å endre oppsettet for regnskapsoppgjørene. Etter at du har definert kontokategoriene på siden **Finanskontokategorier** og du velger handlingen Generer kontoskjemaer, kan du for eksempel velge handlingen **Finansrapporter** og oppdatere de underliggende finansrapportene for kjernefinansrapporter. Neste gang du kjører en av disse rapportene, for eksempel **saldoutdrag**, legges nye totaler og underoppføringer til.

En annen fordel med å bruke finanskontokategorier fremfor de rå finanskontoene i raddefinisjonene, er at en endring i kontoplanstrukturen ikke påvirker finansrapportene.

> [!NOTE]
> Kontokategoriene på øverste nivå, for eksempel **Gjeld**-noden, er faste, og du kan ikke legge til dine egne. Du kan imidlertid slette og legge til kontokategorier på lavere nivåer og definere hvordan den tilhørende finansrapporten vises i rapporter.
>
> Du bør opprette og strukturere dine egne finanskontokategorier på lavere nivå fra bunnen av, om nødvendig i et hierarki, i stedet for å prøve å omorganisere de eksisterende. Du kan for eksempel omstrukturere **Gjeld**-noden slik at den inneholder en ny **Egenkapital**-node etterfulgt av nodene **Kortsiktig gjeld** og **Langsiktig gjeld**. Finn ut mer på [Tildel finanskontoer til kontokategorier](finance-general-ledger.md#account-categories).

## Anbefalte fremgangsmåter for arbeid med raddefinisjoner

Raddefinisjoner versjonskontrolleres ikke. Når du endrer en raddefinisjon, erstattes den gamle versjonen når endringen lagres i databasen. Listen nedenfor inneholder noen anbefalte fremgangsmåter for å arbeide med raddefinisjoner:

- Hvis du legger til raddefinisjoner, velger du en god kode og fyller ut beskrivelsesfeltet med en meningsfull tekst mens du fortsatt vet hva du bruker raddefinisjonen til. Denne informasjonen hjelper kollegene dine (og ditt fremtidige jeg) med å arbeide med finansrapportering og kanskje endre raddefinisjonen.
- Før du endrer en raddefinisjon, bør du vurdere å ta en kopi av den som en sikkerhetskopi, i tilfelle endringen ikke fungerer som forventet. Du kan enten bare kopiere definisjonen (gi den et bra navn), eller eksportere den. Hvis du vil finne ut mer, kan du gå til [Importer eller eksporter raddefinisjoner](#import-or-export-financial-reporting-row-definitions).
- Hvis du trenger en ny kopi av en definisjon som [!INCLUDE[prod_short](includes/prod_short.md)] gir, er det enkelt å opprette et nytt selskap som bare inneholder oppsettsdata. Deretter eksporterer du definisjonen og importerer den til selskapet der definisjonen trenger en oppdatering.

## Importer eller eksporter av raddefinisjoner for finansrapport

Du kan importere og eksportere raddefinisjoner for finansrapport som RapidStart-konfigurasjonspakker. Konfigurasjonspakker er for eksempel nyttig for deling av informasjon med andre selskaper. Pakken opprettes i en .rapidstart-fil, som komprimerer innholdet.

> [!NOTE]
> Når du importerer finansrapportering/raddefinisjoner, blir eksisterende poster med samme navn som de du importerer, erstattet med de nye definisjonene. Konfigurasjonspakken for en rapportdefinisjon overskriver ikke eksisterende rad- eller kolonnedefinisjoner som brukes i rapportdefinisjonen.

Hvis du vil importere eller eksportere finansrapportraddefinisjoner, gjør du følgende:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Raddefinisjoner**, og velg deretter den tilknyttede koblingen.
1. Velg raddefinisjonen, og velg deretter **Importer raddefinisjon** eller **Eksporter raddefinisjon**, avhengig av hva du vil gjøre.

## Se også

[Kolonnedefinisjoner i finansrapportering](bi-column-definitions.md)  
[Klargjør finansrapportering](bi-how-work-account-schedule.md)  
[Finansforretningsanalyse](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
