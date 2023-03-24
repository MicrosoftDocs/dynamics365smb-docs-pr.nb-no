---
title: Angi rapportoppsettet
description: 'Lær hvordan du angir oppsettet som brukes i en rapport, når du forhåndsviser og skriver ut.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 08/12/2022
ms.author: jswymer
---
# Definer oppsettet som brukes av en rapport

> **GJELDER:** Business Central online, Business Central on-premises (2022 lanseringsbølge 1 og senere). For tidligere versjoner går du [hit](ui-how-change-layout-currently-used-report.md).

Et rapportoppsett bestemmer utseendet på en rapport. Den kontrollerer hvilke datafelter i et rapportdatasett som vises, hvordan de er ordnet, stiler med mer. En rapport kan ha mer enn ett oppsett, som du deretter kan bytte mellom etter behov.

Når det er flere selskaper i programmet, blir oppsettene satt på per firma-basis. Slik at den samme rapporten i ett selskap kan ha et annet oppsett i et annet selskap.

## Kom i gang

Det finnes noen få måter å angi hvilket oppsett en rapport bruker. Du kan få fordeler på hver måte, avhengig av hva du er på jakt etter: 

- Fra rapportforespørselssiden

  Når du setter opp en rapport som skal kjøres, inneholder rapportforespørselssiden feltet **Rapportoppsett** som viser nåværende standardoppsett som brukes i rapporten. Du kan bruke dette feltet til å bytte midlertidig til et annet tilgjengelig oppsett som rapporten kjører. Etter at du har kjørt rapporten, går oppsettet tilbake til standardoppsettet på nytt. Hvis du vil ha mer informasjon, kan du se [Kjør og skriv ut rapporter](ui-work-report.md#switching-the-report-layout).

- Fra siden **Rapportoppsettsvalg**

  Siden **Valg av rapportoppsett** viser en liste over alle rapporter. Denne siden angir det gjeldende standardoppsettet for en rapport. Den lar deg definere oppsett i forskjellige selskaper uten å måtte bytte ut selskapet du arbeider med.

- Fra siden **Rapportoppsett** Siden **Rapportoppsett** viser alle tilgjengelige oppsett for hver rapport i det gjeldende selskapet. Det brukes også til å angi standardoppsett for rapporter. Det er enkelt å finne et bestemt oppsett ved å sortere eller filtrere listen. Når du har funnet oppsettet, kan du angi det for en rapport med et enkelt valg.

  > [!NOTE]
  > Du kan ikke bruke **Rapportoppsett**-siden for Word- og RDLC-oppsett som ble opprettet ved hjelp av den eldre funksjonen **Egendefinerte oppsett**. Du ser faktisk ikke at disse egendefinerte oppsettene vises på siden **Rapportoppsett**. For disse oppsettene kan du bare angi dem ved hjelp av siden **Valg av rapportoppsett**.

## Angi oppsettet fra Rapportoppsett

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Finn oppsettet i listen, merk det, og velg deretter **Angi standard**-handling øverst på siden.

## Angi oppsettet fra Valg av rapportoppsett-siden

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.
  
   Siden viser alle rapportene som er tilgjengelige for selskapet som er angitt i feltet **Selskap** øverst på siden. Feltet **Oppsettsbeskrivelse** angir oppsettet som brukes i rapporten for øyeblikket.
2. Sett feltet **Selskap** øverst på siden til selskapet som inkluderer rapporten.
3. Finn og merk rapporten i listen, og gjør deretter et av følgende:

   - Hvis oppsettet du vil bytte til er en annen type enn gjeldende oppsett, velger du feltet **Oppsettstype**, og deretter velger du typen oppsett du vil angi for rapporten. 
   - Hvis oppsettet du vil bytte til, er samme type som gjeldende oppsett, velger du **Velg oppsett**-handlingen øverst.

4. På siden **Rapportoppsett** velger du oppsett, og deretter velger du **OK**.

## Gå tilbake til det opprinnelige standardoppsettet

Rapporter er utformet for å bruke et oppsett som standard. Du kan gå tilbake til det opprinnelige standardoppsettet fra side for **Valg av rapportoppsett**. Bare merk rapporten, og velg deretter **Gjenopprett standardvalg**-handling øverst på siden.

## Se relatert [Microsoft-opplæring](/training/modules/change-documents-dynamics-365-business-central/index)

## Se også

[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
