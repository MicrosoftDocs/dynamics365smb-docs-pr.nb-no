---
title: Arbeid med ansvarssentre
description: Ansvarssenter som administrative sentre hjelper selskaper med å sette opp brukerspesifikke visninger av salgs- og kjøpsdokumenter eksklusivt til hvert senter.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 5714, 5715
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: e551b7810bba9e75320ca11a2126b15f3b91d812
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521991"
---
# <a name="work-with-responsibility-centers"></a>Arbeide med ansvarssentre

Ansvarssentre gir mulighet til å håndtere administrative sentre. Et ansvarssenter kan være et kostsenter, et resultatsenter, et investeringssenter eller et annet administrativt senter som er definert av selskapet. Eksempler på ansvarssentre kan være et salgskontor, en innkjøpsavdeling for forskjellige lokasjoner, og et planleggingskontor ved et anlegg. Ved hjelp av denne funksjonaliteten kan selskaper for eksempel sette opp brukerspesifikke visninger av salgs- og kjøpsdokumenter knyttet til ett bestemt ansvarssenter.  

Bruk av flere lokasjoner sammen med ansvarssentre gir muligheten til å styre forretningsdriften på en mest mulig fleksibel, men likevel optimal måte.

Med flere lokasjoner kan selskaper styre lageret på flere lokasjoner ved hjelp av én database. To begreper, lokasjoner og lagerføringsenheter er hjørnesteinene i denne granulen. En lokasjon er definert som et sted som håndterer fysisk plassering og antall varer. Begrepet er bredt nok til å omfatte lokasjoner som fabrikker eller produksjonsanlegg, samt distribusjonssentre, lagre, utstillingslokaler og servicekjøretøyer. En lagerføringsenhet er definert som en vare i en bestemt lokasjon og/eller som en variant. Ved hjelp av lagerføringsenheter kan selskaper med flere lokasjoner legge til informasjon om etterfylling, adresser og noe bokføringsinformasjon på lokasjonsnivå. De har dermed mulighet til å etterfylle varianter av samme vare for hver lokasjon, i tillegg til å bestille varer til hver lokasjon på bakgrunn av lokasjonsspesifikk etterfyllingsinformasjon.  

## <a name="to-set-up-a-responsibility-center"></a>Slik definerer du ansvarssentre

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ansvarssentre** og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Hvis du bruker ansvarssentre til å administrere selskapet, kan det være nyttig å ha et standard ansvarssenter for selskapet.
4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Selskapsopplysninger**, og velg deretter den relaterte koblingen.
5. I feltet **Ansvarssenter** angir du en ansvarssenterkode.

Koden brukes i alle kjøps-, salgs og servicedokumenter hvis brukeren, kunden eller leverandøren ikke har noe standard ansvarssenter. I et hvilket som helst salgs-, kjøps- eller servicedokument kan du angi et annet ansvarssenter enn standard.

> [!NOTE]  
> Når du angir en kode for ansvarssenteret i et dokument, virker koden inn på adressen, dimensjonene og prisene i dokumentet.  

## <a name="to-assign-responsibility-centers-to-users"></a>Slik tilordner du ansvarssentre til brukere

Du kan lage et oppsett som gjør at brukerne bare kan hente dokumenter som er relevante for oppgavene de utfører i sine daglige rutiner. Brukerne er vanligvis tilknyttet ett ansvarssenter der de bare arbeider med dokumenter som gjelder bestemte moduler ved dette arbeidssenteret.  

Hvis du vil knytte ansvarssentre til bruker, kan du gjøre dette i tre moduler: Kjøp, Salg og Servicehåndtering.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukeroppsett** og velg den relaterte koblingen.  
2. På siden **Brukeroppsett** velger du brukeren du vil tilordne et ansvarssenter til. Hvis brukeren ikke er på oversikten, må du angi bruker-ID i feltet **Bruker-ID**.  
3. I feltet **Filter for ansv.senter - salg** angir du i hvilket ansvarssenter brukeren skal ha oppgaver som er knyttet til salg.  
4. I feltet **Filter for ansv.senter - kjøp** angir du i hvilket ansvarssenter brukeren skal ha oppgaver som er knyttet til innkjøp.  
5. I feltet **Filter for ansv.sent - service** angir du i hvilket ansvarssenter brukeren skal ha oppgaver som er knyttet til servicehåndtering.  

> [!NOTE]  
> Brukere kan vise bare de bokførte dokumentene som gjelder sitt eget ansvarssenter. De kan imidlertid vise alle postene og navigere til andre bokførte dokumenter fra postene.

## <a name="see-also"></a>Se også

[Definere lager](inventory-setup-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]