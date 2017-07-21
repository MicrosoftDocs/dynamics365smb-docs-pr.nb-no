---
title: Opprete nummerserier | Microsoft-dokumentasjon
description: Finn ut hvordan du definerer nummerserier som tilordner unike ID-koder til konti og dokumenter i Dynamics 365 for Financials.
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7cc119c5879400adf63e468259a2c3a275b71cca
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create-number-series"></a>Opprette nummerserier
For hvert selskap som opprettes, må du tilordne unike identifikasjonskoder til elementer som for eksempel hovedbokkontoer, kunde- og leverandørkontoer, fakturaer og andre dokumenter. Nummerering er ikke bare viktig for identifikasjonsformål. Med et godt utformet nummereringssystem er det enklere å styre og analysere selskapet, og antall feil som forekommer ved dataregistrering reduseres.

> [!NOTE]  
>   Vi anbefaler at du bruker de samme nummerseriekodene som er oppført i vinduet **Nummerserieliste** i demonstrasjonsselskapet CRONUS. Koder som *P-INV+* gir kanskje ikke umiddelbar mening for deg, men [!INCLUDE[d365fin](includes/d365fin_md.md)] har en rekke standardinnstillinger som avhenger av disse nummerseriekodene.

Et nummereringssystem lager du ved å opprette én eller flere koder for hver hoveddatatype eller dokumenttype. Du kan for eksempel opprette én kode for å nummerere kunder, en annen kode for å nummerere salgsfakturaer, og enda en kode for å nummerere dokumenter i finanskladder. Når du har opprettet en kode, må du opprette minst én nummerserielinje. Nummerserielinjen inneholder informasjon som for eksempel første og siste nummer i serien, samt startdato. Du kan opprettet mer enn én nummerserielinje per nummerseriekode, med ulik startdato for hver linje. Seriene brukes i rekkefølge, og hver serie starter på sin respektive startdato.

Du setter vanligvis opp i nummerserien automatisk skal sette inn neste nummer i rekken på nye kort eller dokumenter du oppretter. Men kan du også definere en nummerserie som tillater at du angir det nye nummeret manuelt. Du angir dette med avmerkingsboksen **Manuelle nr.** .

Hvis du vil bruke mer enn én nummerseriekode for én type hoveddata - det vil si hvis du for eksempel vil bruke ulike nummerserier for ulike varekategorier - kan du bruke nummerserieforbindelser.

## <a name="to-create-a-new-number-series"></a>Opprette en ny nummerserie
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Nummerserie**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov på den nye linjen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Tips**: Hvis du vil tillate manuell angivelse av et nummer på nytt kort eller dokumenter, fjerner du merket for en **Standardnr.** og merker av for  **Manuelle nr.** .

Nå når du oppretter et nytt kort eller et dokument som er konfigurert til å bruke den aktuelle nummerserien, kan du manuelt fylle ut feltet **Nr.** med enhver verdi.  

## <a name="to-set-up-where-a-number-series-is-used"></a>Slik definerer du der det brukes en nummerserie
Følgende fremgangsmåte viser hvordan du angir nummerseriene for Salg-området. Trinnene er de samme for andre områder.
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Salg**, og velg deretter den relaterte koblingen.
2. I **Salg**-vinduet på hurtigfanen **Nummerserie** velger du ønsket nummerserie for hvert salgskort eller dokument.

Det valgte nummeret skal nå brukes til å fylle ut feltet **Nr.** på kortet eller det aktuelle dokumentet, i henhold til innstillingene du gjorde på nummerserielinjen.

## <a name="to-create-relationships-between-number-series"></a>Slik oppretter du forbindelser mellom nummerserier
Hvis du har opprettet mer enn én nummerseriekode for den samme typen grunnleggende opplysninger eller transaksjoner, kan du opprette forbindelser mellom kodene. Denne funksjonen kan hjelpe deg med å velge mellom koder når du bruker et nummer.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Nummerserie**, og velg deretter den relaterte koblingen.
2. Velg linjen med nummerserien du vil opprette forbindelser for, og velg deretter **Forbindelser**.
3. I **Seriekode**-feltet angir du koden for nummerserien du vil knytte til serien du valgte i trinn 2.
4. Legg til en linje for hver kode du vil knytte til den valgte nummerserien.
5. Lukk vinduet.

Når du så registrerer noe som trenger et nummer, kan du bruke forbindelsene du har opprettet til å velge mellom nummerseriene som er koblet til hverandre.

## <a name="see-also"></a>Se også
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

