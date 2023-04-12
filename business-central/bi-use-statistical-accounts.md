---
title: Bruk statistiske kontoer til å analysere ikke-transaksjonelle data
description: Beskriver hvordan du bruker statistiske kontoer som en annen datakilde for analysene.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/07/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, financial report'
ms.search.form: '2632, 2631, 2633, 2623, 2634'
---
# Analyser data med statistiske kontoer

Bruke statistiske kontoer til å supplere informasjon i finansrapporter. Med statistiske kontoer kan du legge til målinger basert på ikke-transaksjonelle data. Du legger til de ikke-transaksjonelle dataene som tallbaserte enheter, for eksempel:

* Antall ansatte
* Kvadratfot
* Antall kunder med forfalte kontoer

Du kan for eksempel måle omsetning eller kostnader basert på antall personer i en avdeling. Antall ansatte for avdelingen er enheten for den statistiske kontoen. Det følgende bildet viser et eksempel på en rapport som bruker en statistisk konto til å vise inntekter per ansatt.

:::image type="content" source="media/statistical account report example.png" alt-text="Eksempel på en rapport som inneholder data fra en statistisk konto.":::

Statistiske kontoer ligner på bokføring av kontoer basert på hvordan de fungerer. Transaksjoner som du bokfører, blir lagret ved hjelp av statistiske kontojournaler, slik at du kan bruke transaksjonene som data for finansrapporter. Hvis du vil finne ut mer om finansrapporter, kan du gå til [Klargjør Financial Reporting med finansdata og kontokategorier](bi-how-work-account-schedule.md). 

Det er et par viktige forskjeller mellom statistiske kontoer og bokføringskontoer. Statistiske kontoer er separate enheter og tas ikke med i rapporter for råbalanse. Du trenger heller ikke å balansere debet- og kreditbeløp når du bruker statistiske kontojournaler til å bokføre poster til en statistisk konto. Du bokfører bare beløpet.

## Konfigurer en statistisk konto

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Statistiske kontoer**, og velg deretter den relaterte koblingen.
1. Fyll ut feltene på hurtigfanen **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Bokføre beløp til en statistisk konto

1. Hvis du vil bokføre beløpene du vil følge opp, velger du handlingen **Statistisk kontojournal** på siden **Statistiske kontoer**.
1. Angi den siste datoen i bokføringsperioden du vil bokføre beløp for, i **Bokføringsdato**-feltet.
1. Valgfritt: Hvis du vil spore beløp for et bestemt dokument, angir du dokumentets ID i feltet **Dokumentnr.**.
1. I feltet **Statistisk kontonr.** velger du den statistiske kontoen du vil bokføre beløp på.
1. I feltet **Beskrivelse** skriver du en kort beskrivelse av hva du måler.  
1. Angi beløpet som skal bokføres, i feltet **Beløp**. 
1. Valgfritt: Hvis du vil ta med den statistiske kontoen i mer avanserte analyser, angir du dimensjoner i feltene **Avdelingskode** og **Customergroup-kode**. Hvis du vil ha mer informasjon om dimensjoner, kan du gå til [Analyser data per dimensjoner](bi-how-analyze-data-dimension.md).

## Bekreft statistiske kontobeløp

På siden **Statistiske kontoer** bruker du handlingen **Saldo for statistiske kontoer** til å bekrefte at de registrerte beløpene er riktige for hver periode.  

## Inkluder statistisk konto i en finansrapport

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
1. Opprett en ny finansrapport på en av følgende måter:
    1. Velg **Opprett** for å starte fra begynnelsen. Hvis du vil ha mer informasjon om hvordan du oppretter finansrapporter, går du til [Opprett en ny finansrapport](bi-how-work-account-schedule.md#create-a-new-financial-report).
    1. Hvis du vil bruke innstillinger fra en lignende rapport, velger du rapporten du vil kopiere og velger handlingen **Kopier finansrapport**. Du kan redigere innstillingene du kopierer i den nye rapporten.
1. Legg til statistisk konto:
    1. Hvis du starter fra bunnen av, velger du **Rediger raddefinisjon**-handling.
    1. Hvis du vil bruke en raddefinisjon fra en eksisterende rapport, velger du rapporten du vil kopiere fra, og velger handlingen **Kopier raddefinisjon**.
1. På siden **Raddefinisjon** i feltet **Radenr.** definerer du hvor raden skal vises i radsekvensen i rapporten.
1. I feltet **Beskrivelse** angir du tekst som angir hva du måler.
1. I **Sammentellingstype**-feltet velger du **Statistiske kontoer**.
1. I **Sammentelling**-feltet velger du en statistisk konto.
1. I **Radtype**-feltet velger du om du vil vise saldoen på bokføringsdatoen eller begynnelsen av bokføringsperioden, eller hvis du vil vise endringen i beløpet i perioden.
1. Fyll ut feltene som gjenstår. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Se også

[Finansforretningsanalyse](bi.md)  
[Finansrapporter og analyser i Business Central](finance-reports.md)