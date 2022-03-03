---
title: Definere hovedkalendere
description: Du kan tilordne en hovedkalender til selskapet og forretningspartnerne, for å beregne leverings-og mottaksdatoer i henhold til virkedagene som er angitt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7600, 7601, 7602, 5703
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 25d15bfab1dac9cea52d9efdb30e5ed3c7cbb4a2
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141596"
---
# <a name="set-up-base-calendars"></a>Definere hovedkalendere

Du kan tilordne en hovedkalender til selskapet med forretningspartnere, for eksempel kunder, leverandører eller lokasjoner. Leverings- og mottaksdatoer i fremtidige ordrer, bestillinger, overføringsordrer og produksjonsordrelinjer beregnes i henhold til virkedagene som er angitt i kalenderen. Den største oppgaven med å definere en ny hovedkalender, er å angi og definere hvilke fridager som skal brukes.  

## <a name="to-set-up-a-base-calendar"></a>Slik definerer du en hovedkalender

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Hovedkalender**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Fyll ut **Kode**-feltet.  
4. Velg **Vedlikehold endringer i hovedkalender**.
5. På siden **Endringer i hovedkalender** bruker du feltet **Gjentakelsesintervall** til å merke en bestemt dato eller dag som en gjentakende fridag. Du kan velge **Årlig** eller **Ukentlig**.  

    Hvis du velger **Årlig**, må du også angi den aktuelle datoen i **Dato**-feltet.  

    Hvis du velger **Ukentlig**, må du også velge den aktuelle ukedagen i **Dag**-feltet. Hvis du lar feltet stå tomt, må du fylle ut **Dato**-feltet. **Dag**-feltet fylles ut automatisk.  

Når du oppretter en post, merkes det av for **Fridag**. Du kan velge å fjerne merket hvis du vil gjøre den til en virkedag.  
 Når du går tilbake til kortet for hovedkalenderen, ser du at postene du opprettet for fridager, er oppdatert. Disse postene vises nå i rødt, og **Fridag**-feltet er valgt.  

> [!NOTE]  
>  Når du oppretter en ny hovedkalender, kan du velge og kopiere linjer fra en eksisterende kalender. Det gjør du på den aktuelle **Endringer i hovedkalender**-siden.  

> [!IMPORTANT]  
>  En hvilken som helst basiskalender som er definert for leverandøren eller lokasjonen, påvirker hvordan datoene beregnes og avrundes til virkedager.
Angir en datoformel for tiden det tar å etterfylle varen. Det brukes til å beregne feltet **Planlagt mottaksdato** hvis det beregner fremover, og feltet **Ordredato** hvis det beregner bakover. Se [Beregning av leveringstid](across-how-to-assign-base-calendars.md#lead-time-calculation).

## <a name="lead-time-calculation"></a>Beregning av leveringstid

En hvilken som helst basiskalender som er definert for leverandøren eller lokasjonen, påvirker hvordan datoene beregnes og avrundes til virkedager. De to datofeltene i bestillingslinjer beregnes på samme måte som følger under forskjellige betingelser.

|Retning for beregning|Leverandørkalender er definert|Leverandørkalender er ikke definert|
|---------------------|-----------------------|---------------------------|
|Fremover|planlagt mottaksdato = bestillingsdato + leveringstid for leverandør (ifølge leverandørkalenderen og avrundet til påfølgende arbeidsdag, først i leverandørkalenderen og deretter i lokasjonskalenderen)|planlagt mottaksdato = bestillingsdato - leveringstid for leverandør (ifølge lokasjonskalenderen)|
|Bakover|bestillingsdato = planlagt mottaksdato - leveringstid for leverandør (ifølge leverandørkalenderen og avrundet til forrige arbeidsdag, først i leverandørkalenderen og deretter i lokasjonens kalender)|bestillingsdato = planlagt mottaksdato - leveringstid for leverandør (ifølge lokasjonskalenderen)|

> [!NOTE]
> I tillegg til beregning av leveringstid som påvirker planlagt mottaksdato og ordredato, som vist i tabellen over, kan lagerhåndteringstid og sikkerhetsleveringstid legges til i formlene for å fylle ut verdien i feltet **Forventet mottaksdato** slik: planlagt mottaksdato + sikkerhetsleveringstid + inngående lagerhåndteringstid = forventet mottaksdato.

> [!Important]
> Hvis lokasjonen bruker en helt annen kalender enn leverandørene gjør, er det viktig at du definerer spesifikke kalendere for disse leverandørene, slik at du kan beregne optimale leveringstider for leverandørene. Hvis du vil ha informasjon om hvordan du definerer leverandørkalendere, kan du se [Slik tilordner du en hovedkalender](across-how-to-assign-base-calendars.md#to-assign-a-base-calendar).

Innholdet i feltet **Beregning av leveringstid** kopieres fra varekortet eller LFE-kortet hvis leveringstiden er definert for varen, eller på siden **Leverandørens varekatalog** hvis leveringstiden er definert for leverandøren.

## <a name="to-customize-a-calendar"></a>Slik tilpasser du en kalender
Hovedoppgaven med å tilpasse en hovedkalender for selskapet, eller selskapets forretningspartner, er å angi eventuelle endringer i statusen for arbeids- eller fridager.

Mens for eksempel en hovedkalender vanligvis viser alle lørdager som fridager, kan den egendefinerte kalenderen for en bestemt lokasjon vise alle lørdager i november og desember frem til jul, som virkedager.

Følgende prosedyre bruker lokasjonen som eksempel. Merk at du på dette tidspunktet allerede har tilordnet en hovedkalender til lokasjonen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.
2. Åpne lokasjonen du vil oppdatere, og velg deretter feltet **Egendefinert kalender**. Merk at en kalender må velges i feltet **Hovedkalenderkode**.
3. På siden **Egendefinerte kalenderposter** som åpnes, velger du **Vedlikehold endringer i egendefinert kalender**.
4. I vinduet **Endringer i egendefinert kalender** legger du til linjer for egendefinerte kalenderposter.

    Når du oppretter en linje, merkes det av for **Fridag**. Du kan fjerne merket hvis du vil endre statusen til en virkedag.

    Du kan bruke feltet **Gjentakelsesintervall** til å angi en bestemt dato eller dag som en gjentakende fridag. Du kan velge **Årlig** eller **Ukentlig**.

    Hvis du velger **Årlig**, må du også angi den aktuelle datoen i **Dato**-feltet. Hvis du velger **Ukentlig**, må du også velge den aktuelle ukedagen i **Dag**-feltet. Hvis du lar feltet stå tomt, må du fylle ut **Dato**-feltet. **Dag**-feltet fylles deretter ut automatisk. Dette kan være nyttig hvis du for eksempel vil merke en enkelt dag som fridag eller virkedag.

5. Velg **OK**.

På siden **Egendefinerte kalenderposter** ser du at datopostene er oppdatert med endringene du gjorde.

På lokasjonskortet, ser du at det står **Ja** i feltet **Egendefinert kalender**, som betyr at det er opprettet en egendefinert kalender.

> [!Important]
> Hvis du ikke fyller ut **Lokasjonskode**-feltet på en ordrelinje, brukes selskapets kalender.


Hvis du ikke fyller ut **Transportørkode**-feltet på en ordrelinje, brukes selskapets kalender.

> [!NOTE]  
> Hvis du foretar endringer i en hovedkalender med endringer i den egendefinerte kalenderen, oppdateres alle egendefinerte kalendere automatisk.

## <a name="to-assign-a-base-calendar"></a>Slik tilordner du en hovedkalender  
I følgende fremgangsmåte planlegges leveringsdatoer på ordrelinjer for en kunde som et eksempel.

Hovedkalendere er tilordnet til ditt eget selskap, dine kunder, leverandører, plasseringer og transportører som vist nedenfor:  

-   På **Selskapsopplysninger**- og **Kunde**-kortene tilordnes hovedkalenderen på hurtigfanen **Levering**.  
-   På **Leverandør**-kortet er hovedkalenderen tilordnet på hurtigfanen **Mottak**.  
-   På **Lokasjon**-kortet er hovedkalenderen tilordnet på hurtigfanen **Lager**.  
-   På **Transportører**-siden tilordnes hovedkalenderen på **Transportørservice**-siden.  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.  
2.  Åpne **Kunde**-kortet som du vil tilordne en hovedkalender for.  
3.  På hurtigfanen **Levering**, i **Hovedkalenderkode**-feltet, velger du hovedkalenderen som du vil tilordne.  

> [!IMPORTANT]  
>  -   Hvis du ikke tilordner en hovedkalender til et selskap, beregnes alle datoene som virkedager.  
> -   Hvis du angir en tom lokasjon eller ordrelinje, beregnes alle datoer som virkedager.  
> -   En hvilken som helst basiskalender som er definert for leverandøren eller lokasjonen, påvirker hvordan datoene beregnes og avrundes til virkedager.

> [!NOTE]  
>  Før du kan opprette egendefinerte kalenderposter, må du først tilordne selskapet en hovedkalender.  

## <a name="see-also"></a>Se også
[Innkjøp](purchasing-manage-purchasing.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]