---
title: 'Bruk én mva-kode i kladder [NO]'
description: 'I Norge kan du bruke funksjonen for én mva-kode i en kladd, slik at du kan bokføre mva ved hjelp av ett enkelt felt, Mva-kode.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '10602, 10697, 10698, 10604'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="use-one-vat-code-in-journals-in-norway" />Bruk én mva-kode i kladder i Norge

I Norge kan du bruke funksjonen for én mva-kode i en kladd, slik at du kan bokføre mva ved hjelp av ett enkelt felt, **Mva-kode**. Når én mva-kode er konfigurert, er dette en rask måte å fylle ut mva-felt som brukes ofte.  

For å angi mva-koden for bestillinger og ordrer, må de tilsvarende mva-bokføringsgruppene for firma og mva-bokføringsgruppene for varer defineres.  

Mva-satsen beregnes fra kombinasjonen av mva-firmabokføringsgrupper, kjøperinformasjon og mva-varebokføringsgrupper.  

## <a name="to-create-a-vat-code" />Slik oppretter du en mva-kode:

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Mva-koder** og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Angi opplysninger i feltet **Kode**, **Bokføringstype** og **Beskrivelse** for hver mva-kode.  
4.  Velg **OK**-knappen for å lukke siden **Mva-koder**.  

Fremgangsmåten nedenfor beskriver mva-bokføringsoppsettet.  

## <a name="to-set-up-vat-posting" />Slik definerer du mva-bokføring:

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Mva-bokføringsoppsett**, og velg deretter den relaterte koblingen.  
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

## <a name="see-also" />Se også
 [Norske mva-koder](norwegian-vat-codes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
