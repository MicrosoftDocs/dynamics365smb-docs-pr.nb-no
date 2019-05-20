---
title: Opprette nummerserier | Microsoft-dokumentasjon
description: Finn ut hvordan du definerer nummerserier som tilordner unike ID-koder til konti og dokumenter i Business Central.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a650bb8dec324e94801da828d7e967b514ae3ca1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251380"
---
# <a name="create-number-series"></a>Opprette nummerserier
For hvert selskap som opprettes, må du tilordne unike identifikasjonskoder til elementer som for eksempel hovedbokkontoer, kunde- og leverandørkontoer, fakturaer og andre dokumenter. Nummerering er ikke bare viktig for identifikasjonsformål. Med et godt utformet nummereringssystem er det enklere å styre og analysere selskapet, og antall feil som forekommer ved dataregistrering reduseres.

> [!NOTE]  
>   Vi anbefaler at du bruker de samme nummerseriekodene som er oppført på siden **Nummerserieliste** i demoselskapet CRONUS. Koder som *P-INV+* gir kanskje ikke umiddelbar mening for deg, men [!INCLUDE[d365fin](includes/d365fin_md.md)] har en rekke standardinnstillinger som avhenger av disse nummerseriekodene.

Et nummereringssystem lager du ved å opprette én eller flere koder for hver hoveddatatype eller dokumenttype. Du kan for eksempel opprette én kode for å nummerere kunder, en annen kode for å nummerere salgsfakturaer, og enda en kode for å nummerere dokumenter i finanskladder. Når du har opprettet en kode, må du opprette minst én nummerserielinje. Nummerserielinjen inneholder informasjon som for eksempel første og siste nummer i serien, samt startdato. Du kan opprettet mer enn én nummerserielinje per nummerseriekode, med ulik startdato for hver linje. Seriene brukes i rekkefølge, og hver serie starter på sin respektive startdato.

Du setter vanligvis opp i nummerserien automatisk skal sette inn neste nummer i rekken på nye kort eller dokumenter du oppretter. Men kan du også definere en nummerserie som tillater at du angir det nye nummeret manuelt. Du angir dette med avmerkingsboksen **Manuelle nr.**

Hvis du vil bruke mer enn én nummerseriekode for én type hoveddata - det vil si hvis du for eksempel vil bruke ulike nummerserier for ulike varekategorier - kan du bruke nummerserieforbindelser.

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Virkemåte for feltet Nr. i dokumenter og kort
På salgs-, kjøps- og overføringsdokumenter og på alle kort kan **Nr.** fylles ut automatisk fra en nummerserie eller manuelt, og det kan settes opp til å være usynlig.

**Nr.** -feltet kan fylles ut på tre måter:

1. Hvis det bare finnes én nummerserie for dokumenttypen eller kortet, der det er merket av for **Standardnr.** og ikke merket av for **Manuelle nr.**, fylles feltet ut automatisk med neste nummer i serien, og feltet **Nr.** vises ikke.

    > [!NOTE]  
    > Hvis nummerserien ikke fungerer, for eksempel fordi den er tom for numre, vil feltet **Nr.** vises, og du kan angi et nummer manuelt eller løse problemene på siden **Nummerserieliste**.

2. Hvis det finnes flere nummerserier for dokumenttypen eller kortet, og det ikke er merket av for **Standardnr.** for den tilordnede nummerserien, er feltet **Nr.** synlig, og du kan slå opp **Nummerserieliste**-siden og velge nummerserien du vil bruke. Det neste nummeret i serien settes deretter inn i feltet **Nr.** .

3. Hvis du ikke har definert en nummerserie for typen dokument eller kort, eller hvis det er merket av for **Manuelle nr.** for nummerserien, vises feltet **Nr.** og du må angi et nummer manuelt. Du kan angi opptil 20 tegn, både tall og bokstaver.

Når du åpner et nytt dokument eller kort som det finnes en nummerserie for, åpnes den aktuelle **Oppsett for nummerserie**-siden, slik at du kan definere en nummerserie for denne dokumenttypen eller dette kortet før du går videre med andre dataregistreringer.

> [!NOTE]  
> Hvis du vil aktivere manuell nummerering på for eksempel nye varekort som er opprettet med en dataoverføring som har skjult **Nr.** som standard, går du til siden **Lageroppsett** og velger **Varenr.**-feltet for å åpne og angi den relaterte nummerserien til **Manuelle nr.**.

## <a name="to-create-a-new-number-series"></a>Opprette en ny nummerserie
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Nummerserie**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov på den nye linjen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-where-a-number-series-is-used"></a>Slik definerer du der det brukes en nummerserie
Følgende fremgangsmåte viser hvordan du angir nummerseriene for Salg-området. Trinnene er de samme for andre områder.
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Salg**, og velg deretter den relaterte koblingen.
2. På siden **Salg** på hurtigfanen **Nummerserie** velger du ønsket nummerserie for hvert salgskort eller dokument.

Det valgte nummeret skal nå brukes til å fylle ut feltet **Nr.** på kortet eller det aktuelle dokumentet, i henhold til innstillingene du gjorde på nummerserielinjen.

## <a name="to-create-relationships-between-number-series"></a>Slik oppretter du forbindelser mellom nummerserier
Hvis du har opprettet mer enn én nummerseriekode for den samme typen grunnleggende opplysninger eller transaksjoner, kan du opprette forbindelser mellom kodene. Denne funksjonen kan hjelpe deg med å velge mellom koder når du bruker et nummer.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Nummerserie**, og velg deretter den relaterte koblingen.
2. Velg linjen med nummerserien du vil opprette forbindelser for, og velg deretter **Forbindelser**.
3. I **Seriekode**-feltet angir du koden for nummerserien du vil knytte til serien du valgte i trinn 2.
4. Legg til en linje for hver kode du vil knytte til den valgte nummerserien.
5. Lukk siden.

Når du så registrerer noe som trenger et nummer, kan du bruke forbindelsene du har opprettet til å velge mellom nummerseriene som er koblet til hverandre.

## <a name="see-also"></a>Se også
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
