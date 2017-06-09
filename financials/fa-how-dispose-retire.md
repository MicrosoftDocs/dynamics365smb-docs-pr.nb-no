---
title: Avhende eller trekke tilbake aktiva| Microsoft-dokumentasjon
description: Beskriver hvordan du selger eller trekker tilbake et aktivum.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 28e4a67ae3df82a2860ced1b971ee41975c8d578
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-dispose-of-or-retire-fixed-assets"></a>Avhende eller trekke tilbake aktiva
Når du selger eller på annen måte avhender et aktiva, må salgsverdien bokføres for å beregne og registrere tap eller vinning. En salgspost må være den siste posten som bokføres for et aktiva. Du kan bokføre mer enn én salgspost for aktiva som er delvis solgt. Summen av alle bokførte salgsbeløp må være et kreditbeløp.  

**Merk:** Hvis du bytter ut et aktiva med et annet, må du registrere både salget av det gamle aktivaet og innkjøpet av det nye (anskaffelsen). Hvis du vil ha mer informasjon, se [Anskaffe aktiva](fa-how-acquire.md).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Slik bokfører du et salg fra aktivafinanskladden:
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivafinanskladder**, og deretter velger du den beslektede koblingen.  
2. Opprett en innledende kladdelinje, og fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. I feltet **Aktivabokf.type** velger du **Salg**.  
4. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for salgsbokføring.  

    **Merk:** Trinn 4 fungerer bare hvis du har definert følgende: I vinduet **Kort for bokf.grp.- aktiva** for bokføringsgruppen for aktivaet, inneholder **Konto for salg**-feltet finansdebetkontoen og **Motkonto for salg**-feltet inneholder finanskontoen du vil bokføre motposter for oppskrivning til. Hvis du vil ha mer informasjon, kan du se "Definere bokføringsgrupper for aktiva" i [Definere generell aktivainformasjon](fa-how-setup-general.md).  
5. Velg handlingen **Bokfør**.  

    Hvis du selger eller på avhender deler av et aktiva, må du dele opp aktivaet før du kan registrere salgstransaksjonen. Hvis du vil ha mer informasjon, se [Overføre, dele opp eller kombinere aktiva](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Slik viser du salgsposter
Når du selger eller avhender et aktiva, bokføres salgsverdien til finans der du kan se resultatet.  

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktiva**, og deretter velger du den beslektede koblingen.  
2. Velg aktivaet du vil vise poster for, og velg deretter **Avskrivningstablåer**.  
3. Velg avskrivningstablået du vil vise poster for, og velg deretter **Poster**.  
4. Velg en linje med **Salg** i **Bokføringskategori, aktiva**-feltet, og velg deretter **Naviger**.  
5. I **Naviger**-vinduet velger du finanspostlinjen og deretter **Vis**.  

**Finansposter**-vinduet åpnes der du kan se postene som er resultat av salgsbokføringen.  

## <a name="see-also"></a>Se også
[Anleggsmidler](fa-manage.md)  
[Definere aktiva](fa-setup.md)  
[Finans](finance.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

