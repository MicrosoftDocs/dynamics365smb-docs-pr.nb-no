---
title: Bruke én mva-kode i kladder
description: I Norge kan du bruke funksjonen for én mva-kode i en kladd, slik at du kan bokføre mva ved hjelp av ett enkelt felt, Mva-kode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 5ca0bd097ee05819dd85f049cc3e9c5c2137fc84
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676696"
---
# <a name="use-one-vat-code-in-journals"></a>Bruke én mva-kode i kladder
I Norge kan du bruke funksjonen for én mva-kode i en kladd, slik at du kan bokføre mva ved hjelp av ett enkelt felt, **Mva-kode**. Når én mva-kode er konfigurert, er dette en rask måte å fylle ut mva-felt som brukes ofte.  

For å angi mva-koden for bestillinger og ordrer, må de tilsvarende mva-bokføringsgruppene for firma og mva-bokføringsgruppene for varer defineres.  

Mva-satsen beregnes fra kombinasjonen av mva-firmabokføringsgrupper, kjøperinformasjon og mva-varebokføringsgrupper.  

## <a name="to-create-a-vat-code"></a>Slik oppretter du en mva-kode:  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **VAT-koder**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Angi opplysninger i feltet **Kode**, **Bokføringstype** og **Beskrivelse** for hver mva-kode.  
4.  Velg **OK**-knappen for å lukke siden **Mva-koder**.  

 Fremgangsmåten nedenfor beskriver mva-bokføringsoppsettet.  

## <a name="to-set-up-vat-posting"></a>Slik definerer du mva-bokføring:  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Mva-bokføringsoppsett**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  I kortet **Mva-bokføringsoppsett** må du fylle ut følgende felt:  

    - **Mva-bokføringsgruppe - firma**  
    - **Mva-bokføringsgruppe - vare**  
    - **Mva-type**  
    - **Mva-prosent**  
    - **Utgående mva-konto**  
    - **Inngående mva-konto**  

4.  I feltet **Mva-kode** velger du en kode fra listen.  

Nå når du bokfører et dokument i finanskladden og lukker det, brukes informasjonen som er angitt i **Mva-bokføringsoppsett**-kortet.  

For eksempel: mva-satsen som er bokført i kladden, defineres av oppsettet du har angitt på **Mva-bokføringsoppsett**-siden.  

> [!NOTE]  
>  Feltet **Mva-kode** og **Motkonto-mva. - kode** er lagt til i kladden. **Motkonto-mva. - kode** er mva-koden som brukes til å beregne motkontoen.  
>   
>  Det gjøres ingen endringer i bokføringen.  

## <a name="see-also"></a>Se også  
 [Norske mva-koder](norwegian-vat-codes.md)
