---
title: Avhende eller trekke tilbake aktiva
description: 'Når du selger eller på annen måte avhender et aktiva, må salgsverdien bokføres for å beregne og registrere tap eller vinning.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.search.form: '5628, 5610, 5611, 5629, 5633'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="dispose-of-or-retire-fixed-assets" />Avhending eller tilbaketrekking av aktiva

Når du selger eller på annen måte avhender et aktiva, må salgsverdien bokføres for å beregne og registrere tap eller vinning. En salgspost må være den siste posten som bokføres for et aktiva. Du kan bokføre mer enn én salgspost for aktiva som er delvis solgt. Summen av alle bokførte salgsbeløp må være et kreditbeløp.  

> [!NOTE]  
> Hvis du bytter ut et aktivum med et annet, må du registrere både salget av det gamle aktivumet (salg) og innkjøpet av det nye (anskaffelse). Hvis du vil ha mer informasjon, kan du se [Anskaffe aktiva](fa-how-acquire.md).  

Følgende fremgangsmåte forutsetter at du allerede har konfigurert de aktuelle bokføringsgruppene på siden **Bokf. grupper-aktiva**. Hvis du vil ha mer informasjon, kan du se [Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal" />Slik bokfører du et salg fra aktivafinanskladden:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Aktivafinanskladder** og velger den relaterte koblingen.  
2. Opprett en innledende kladdelinje, og fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. I feltet **Aktivabokf.type** velger du **Salg**.  
4. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for salgsbokføring.  

    > [!NOTE]  
    >  Trinn 4 fungerer bare hvis du har definert følgende: På siden **Kort for bokf.grp.- aktiva** for bokføringsgruppen for aktivumet, inneholder feltet **Konto for salg** finansdebetkontoen, og feltet **Motkonto for salg** inneholder finanskontoen du vil bokføre motposter for oppskrivning til. Hvis du vil ha mer informasjon, kan du se [Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Velg handlingen **Bokfør**.  

Hvis du selger eller på avhender deler av et aktiva, må du dele opp aktivaet før du kan registrere salgstransaksjonen. Hvis du vil ha mer informasjon, kan du se [Overføre, dele opp eller kombinere aktiva](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries" />Slik viser du salgsposter

Når du selger eller avhender et aktiva, bokføres salgsverdien til finans der du kan se resultatet.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.  
2. Velg aktivaet du vil vise poster for, og velg deretter **Avskrivningstablåer**.  
3. Velg avskrivningstablået du vil vise poster for, og velg deretter **Poster**.  
4. Velg en linje med **Salg** i **Bokføringskategori, aktiva**-feltet, og velg deretter **Søk etter poster**.  
5. På **Søk etter poster**-siden velger du finanspostlinjen og deretter **Vis relaterte poster**.  

**Finansposter**-siden åpnes der du kan se postene som er resultat av salgsbokføringen.  

## <a name="see-related-microsoft-training" />Se relatert [Microsoft-opplæring](/training/modules/dispose-fixed-assets/)

## <a name="see-also" />Se også

[Aktiva](fa-manage.md)  
[Definer aktiva](fa-setup.md)  
[Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Søk etter poster](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
