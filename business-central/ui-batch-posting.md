---
title: Bokføre flere dokumenter samtidig | Microsoft Docs
description: I stedet for å bokføre enkeltdokumenter én etter én, kan du velge flere dokumenter som ikke er bokført, i en liste for massebokføring, enten det er for umiddelbar bokføring eller planlagt, for eksempel på slutten av dagen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d26b98bac791bca2dc910f010c135fe187d6abff
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773633"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Bokføre flere dokumenter samtidig

I stedet for å bokføre enkeltdokumenter én etter én, kan du velge flere dokumenter som ikke er bokført, i en liste for umiddelbar bokføring eller massebokføring i henhold til en tidsplan, for eksempel på slutten av dagen. Dette kan være nyttig hvis bare en arbeidsleder kan bokføre dokumenter som er opprettet av andre brukere, eller for å unngå problemer med systemytelse ved bokføring i arbeidstiden.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Bokføre flere bestillinger umiddelbart

Fremgangsmåten nedenfor forklarer hvordan du bokfører flere bestillinger umiddelbart. Trinnene er lignende for alle kjøps- og salgsdokumenter.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. På **Bestilling**-siden fortsetter du for å velge alle bestillinger som skal bokføres:
3. I **Nr.** -feltet velger du de tre loddrette prikkene for å åpne hurtigmenyen, og deretter velger du handlingen **Velg flere**.
4. Merk av i boksen for alle linjene som representerer ordrer du vil bokføre samtidig.
5. Velg handlingen **Bokføring**, og velg deretter handlingen **Bokfør**.
6. Velg **Ja** i bekreftelsesmeldingen.

## <a name="to-batch-post-multiple-purchase-orders"></a>Massebokføre flere bestillinger

Fremgangsmåten nedenfor forklarer hvordan du massebokfører bestillinger. Trinnene er de samme for alle kjøps- og salgsdokumenter der handlingen **Massebokfør** er tilgjengelig.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.  
2. På **Bestilling**-siden fortsetter du for å velge alle bestillinger som skal bokføres:
3. I **Nr.** -feltet velger du de tre loddrette prikkene for å åpne hurtigmenyen, og deretter velger du handlingen **Velg flere**.
4. Merk av i boksen for alle linjene som representerer ordrer du vil bokføre samtidig.
5. Velg handlingen **Bokføring**, og velg deretter handlingen **Massebokfør**.
6. På siden **Bestillinger - massebokfør** fyller du ut resten av feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Velg **OK**-knappen.
8. Hvis du vil vise potensielle problemer som oppstod under massebokføring av dokumenter, åpner du siden **Feilmeldingsregister**.

> [!NOTE]
> Bokføring av flere dokumenter kan ta litt tid og blokkere andre brukere. Vurder å aktivere bokføring i bakgrunnen. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

## <a name="to-set-up-background-posting-with-job-queues"></a>Konfigurere bokføring i bakgrunnen med jobbkøer
Jobbkøer er et effektivt verktøy til å planlegge kjøring av forretningsprosesser i bakgrunnen, for eksempel når flere brukere prøver å bokføre ordrer, men bare én kan behandles om gangen.  

Fremgangsmåten nedenfor forklarer hvordan du konfigurerer ordrebokføring i bakgrunnen. Trinnene er de samme for kjøp.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.
2. På siden **Salgsoppsett** merker du av for **Bokfør med jobbkø**.
3. Velg feltet **Kategorikode for jobbkø**, og angi deretter koden **SALGSBOKF**.

    > [!NOTE]
    > Noen av jobbene endrer samme data og bør ikke kjøres samtidig, fordi dette kan forårsake konflikter. Bakgrunnsjobber for salgsdokumenter vil for eksempel prøve å endre de samme dataene samtidig. Jobbkøkategorier bidrar til å forhindre denne typen konflikter ved å sørge for at et annet prosjekt som tilhører samme jobbkøkategori, ikke blir kjørt før den er ferdig. Et prosjekt som for eksempel tilhører en jobbkøkategori for salg, vil vente til alle andre salgsrelaterte jobber er utført. Du angir en jobbkøkategori på hurtigfanen **Bakgrunnsbokføring** på siden **Salgsoppsett**.
    >
    > [!INCLUDE[prod_short](includes/prod_short.md)] gir jobbkøkategorier for salg, kjøp og finansbokføring. Vi anbefaler at én av disse eller en du oppretter, alltid angis. Hvis det oppstår feil på grunn av konflikter, kan du vurdere å definere en kategori for all bakgrunnsbokføring av salg, kjøp og finans.

    Hvis du også vil at salgsdokumenter skal skrives ut når de bokføres, merker du av for **Bokfør og skriv ut med jobbkø** på siden **Salgsoppsett**.  
    Hvis du velger **PDF** i feltet **Rapportutdatatype**, vil bokførte bestillinger være tilgjengelige i delen **Rapportinnboks** i rollesenteret.

    > [!IMPORTANT]  
    > Hvis du konfigurerer en jobb som bokfører og skriver ut dokumenter, og skriveren viser en dialogboks, for eksempel en forespørsel om legitimasjon eller en advarsel om lavt skriverblekk, blir dokumentet bokført, men ikke skrevet ut. Den tilsvarende jobbkøposten blir til slutt tidsavbrutt, og **Status**-feltet settes til **Feil**. Vi anbefaler derfor at du ikke bruker et skriveroppsett som krever samhandling med visningen av dialogbokser for skriveren i forbindelse med bakgrunnsbokføring.

    Neste gang du bokfører salgsdokumenter, oppretter [!INCLUDE [prod_short](includes/prod_short.md)] automatisk en jobbkøpost for hvert dokument og kjører jobbene i bakgrunnen, én etter én.

4. Hvis du vil kontrollere at jobbkøen fungerer som forventet, bokfører du en ordre. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).
    Ordren blir nå lagt til i en dedikert jobbkø, som definerer når dokumentene bokføres. 

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Slik viser du status fra et salgs- eller kjøpsdokument
Hvis jobbkøen ikke kan bokføre ordren, endres statusen til **Feil**, og ordren legges til i listen over ordrer som brukeren må håndtere manuelt.
1. Fra dokumentet du har prøvd å bokføre med bakgrunnsbokføring, velger du feltet **Jobbkøstatus**, som inneholder **Feil**.
2. Les feilmeldingen og løs problemet.

Du kan også se på siden **Loggposter for jobbkø** om ordren ble bokført. Hvis du vil ha mer informasjon, se [Vise status eller feil i jobbkøen](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Opprette en jobbkøpost for massebokføring av ordrer

Du kan også utsette bokføringer til når det passer for organisasjonen. I din virksomhet kan det for eksempel være fornuftig å kjøre visse rutiner etter at det meste av dagens dataregistrering er gjort. Du kan oppnå dette ved å angi at jobbkøen skal kjøre ulike massebokføringspostrapporter, for eksempel rapportene **Massebokfør ordrer**, **Salgsfakturaer - massebokfør** og lignende rapporter. [!INCLUDE[prod_short](includes/prod_short.md)] støtter ordrebokføring i bakgrunnen for alle salgs-, kjøps- og servicedokumenter.

Følgende fremgangsmåte viser hvordan du konfigurerer rapporten **Massebokfør ordrer** slik at ordrer bokføres automatisk kl. 16:00 på ukedager.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Poster i jobbkø**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. I feltet **Objekttype som skal kjøres** velger du **Rapport**.  
4. I feltet **Objekt-ID som skal kjøres** velger du 296, **Massebokfør ordrer**.

   Du kan også bruke følgende rapporter:
  
   * 900 **Massebokfør monteringsordrer**
   * 497 **Kjøpsfakturaer - massebokfør**
   * 496 **Bestillinger - massebokfør**
   * 498 **Kjøpskr.notaer - massebokfør**
   * 6665 **Massebokfør bestillingsreturer**
   * 298 **Salgskr.notaer - massebokfør**
   * 297 **Salgsfakturaer - massebokfør**
   * 296 **Massebokfør ordrer**
   * 6655 **Massebokfør ordrereturer**
   * 6005 **Massebokfør salgskreditnotaer (service)**
   * 6004 **Massebokfør servicefakturaer**
   * 6001 **Massebokfør serviceordrer**

5. Merk av for **Rapportforespørselsside**.
6. På forepørselssiden **Massebokfør ordrer** må du definere hva som skal tas med ved automatisk bokføring av ordrer, og deretter velge **OK**-knappen.

    > [!IMPORTANT]
    > Husk å angi strenge filtre. Ellers bokfører [!INCLUDE [prod_short](includes/prod_short.md)] alle dokumenter, selv om de ikke er klare. Vurder å definere et filter i **Status**-feltet for verdien *Frigitt* og et filter for **Bokføringsdato**-feltet for verdien *..i dag*. Hvis du vil ha mer informasjon, kan du se [Sortere, søke etter og filtrere](ui-enter-criteria-filters.md).
7. Merk av i alle bokser fra **Kjør på mandager** til **Kjør på fredager**.
8. I feltet **Starttidspunkt** angir du 16:00.
9. Velg **Sett status til Klar**-handlingen.

Ordrer som er innenfor definerte filtre, blir nå bokført hver ukedag kl. 16:00.


## <a name="see-also"></a>Se også

[Bokføre dokumenter og kladder](ui-post-documents-journals.md)  
[Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)  
[Redigere bokførte dokumenter](across-edit-posted-document.md)  
[Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]