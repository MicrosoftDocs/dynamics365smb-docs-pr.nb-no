---
title: Arbeide med ansvarssentre | Microsoft-dokumentasjon
description: Ansvarssentre gir mulighet til å håndtere administrative sentre. Et ansvarssenter kan være et kostsenter, et resultatsenter, et investeringssenter eller et annet administrativt senter som er definert av selskapet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/03/2020
ms.author: edupont
ms.openlocfilehash: cb9586e207f3eda516d11dd4f184351ff66ca4b2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749958"
---
# <a name="work-with-responsibility-centers"></a>Arbeide med ansvarssentre

Ansvarssentre gir mulighet til å håndtere administrative sentre. Et ansvarssenter kan være et kostsenter, et resultatsenter, et investeringssenter eller et annet administrativt senter som er definert av selskapet. Eksempler på ansvarssentre kan være et salgskontor, en innkjøpsavdeling for forskjellige lokasjoner, og et planleggingskontor ved et anlegg. Ved hjelp av denne funksjonaliteten kan selskaper for eksempel sette opp brukerspesifikke visninger av salgs- og kjøpsdokumenter knyttet til ett bestemt ansvarssenter.  

Bruk av flere lokasjoner sammen med ansvarssentre gir muligheten til å styre forretningsdriften på en mest mulig fleksibel, men likevel optimal måte.

Med flere lokasjoner kan selskaper styre lageret på flere lokasjoner ved hjelp av én database. To begreper, lokasjoner og lagerføringsenheter er hjørnesteinene i denne granulen. En lokasjon er definert som et sted som håndterer fysisk plassering og antall varer. Begrepet er bredt nok til å omfatte lokasjoner som fabrikker eller produksjonsanlegg, samt distribusjonssentre, lagre, utstillingslokaler og servicekjøretøyer. En lagerføringsenhet er definert som en vare i en bestemt lokasjon og/eller som en variant. Ved hjelp av lagerføringsenheter kan selskaper med flere lokasjoner legge til informasjon om etterfylling, adresser og noe bokføringsinformasjon på lokasjonsnivå. De har dermed mulighet til å etterfylle varianter av samme vare for hver lokasjon, i tillegg til å bestille varer til hver lokasjon på bakgrunn av lokasjonsspesifikk etterfyllingsinformasjon.  

## <a name="to-set-up-a-responsibility-center"></a>Slik definerer du ansvarssentre

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ansvarssentre**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Hvis du bruker ansvarssentre til å administrere selskapet, kan det være nyttig å ha et standard ansvarssenter for selskapet.
4. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Selskapsopplysninger**, og velg deretter den relaterte koblingen.
5. I feltet **Ansvarssenter** angir du en ansvarssenterkode.

Koden brukes i alle kjøps-, salgs og servicedokumenter hvis brukeren, kunden eller leverandøren ikke har noe standard ansvarssenter. I et hvilket som helst salgs-, kjøps- eller servicedokument kan du angi et annet ansvarssenter enn standard.

> [!NOTE]  
> Når du angir en kode for ansvarssenteret i et dokument, virker koden inn på adressen, dimensjonene og prisene i dokumentet.  

## <a name="to-assign-responsibility-centers-to-users"></a>Slik tilordner du ansvarssentre til brukere

Du kan lage et oppsett som gjør at brukerne bare kan hente dokumenter som er relevante for oppgavene de utfører i sine daglige rutiner. Brukerne er vanligvis tilknyttet ett ansvarssenter der de bare arbeider med dokumenter som gjelder bestemte moduler ved dette arbeidssenteret.  

Hvis du vil knytte ansvarssentre til bruker, kan du gjøre dette i tre moduler: Kjøp, Salg og Servicehåndtering.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukeroppsett**, og velg deretter den relaterte koblingen.  
2. På siden **Brukeroppsett** velger du brukeren du vil tilordne et ansvarssenter til. Hvis brukeren ikke er på oversikten, må du angi bruker-ID i feltet **Bruker-ID**.  
3. I feltet **Filter for ansv.senter - salg** angir du i hvilket ansvarssenter brukeren skal ha oppgaver som er knyttet til salg.  
4. I feltet **Filter for ansv.senter - kjøp** angir du i hvilket ansvarssenter brukeren skal ha oppgaver som er knyttet til innkjøp.  
5. I feltet **Filter for ansv.sent - service** angir du i hvilket ansvarssenter brukeren skal ha oppgaver som er knyttet til servicehåndtering.  

> [!NOTE]  
> Brukere kan vise bare de bokførte dokumentene som gjelder sitt eget ansvarssenter. De kan imidlertid vise alle postene og navigere til andre bokførte dokumenter fra postene.

## <a name="see-also"></a>Se også

[Definere lager](inventory-setup-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)
[Beholdning](inventory-manage-inventory.md)[Lagerstyring](warehouse-manage-warehouse.md)  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
