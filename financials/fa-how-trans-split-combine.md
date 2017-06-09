---
title: "Overføre, dele opp eller kombinere aktiva| Microsoft-dokumentasjon"
description: "Beskriver hvordan du omklassifiserer et aktiva for å overføre, dele eller kombinere det med andre aktiva."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/29/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 50e1a8d7012394b4b3f710991f7d45ae244656c9
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-transfer-split-or-combine-fixed-assets"></a>Overføre, dele opp eller kombinere aktiva
Du bruker aktivareklassifiseringskladden til å overføre, dele opp og knytte sammen aktiva. Du kan vise eller skrive ut resultatene av aktivareklassifisering med rapporten **Aktiva - bokført verdi 02**.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Slik overfører du et aktiva til en annen avdeling:
Du må kanskje overføre et aktiva til en annen avdeling når for eksempel du plasserer et aktiva i produksjonsavdelingen mens aktivaet er under bygging, og deretter flytter det til administrasjonsavdelingen når det er ferdig.  

1. Definer et nytt aktiva. Angi den nye avdelingen i feltet **Avdelingskode**.
2. Tilordne et avskrivningstablå for aktiva til det nye aktivaet. Hvis du vil ha mer informasjon, se [Anskaffe aktiva](fa-how-acquire.md).
3. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivareklass.kladder**, og deretter velger du den beslektede koblingen.
4. Opprett en reklassifiseringskladd der **Aktivanr.**-feltet inneholder det originale aktivaet, og **Nytt aktivanr.**-feltet inneholder det nye aktivaet som skal flyttes.  
5. Velg handlingen **Reklassifiser**.

    To linjer opprettes nå i aktivafinanskladden ved hjelp av malen og kladden du oppgav for det angitte avskrivningstablået, i vinduet **Aktivakladdoppsett**. Se [Definere avskriving av aktiva](fa-how-setup-depreciation.md) for mer informasjon.
6. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivafinanskladder**, og deretter velger du den beslektede koblingen.    
7. I **Aktiva finanskladd**-vinduet velger du **Bokfør**-handlingen for å bokføre reklassifiseringen du utførte i trinn 4 og 5.

Hvis du har bokført en anskaffelseskost for ett aktiva, kan du bruke reklassifiseringskladden for aktiva til å dele anskaffelseskosten på flere aktiva.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Slik deler du et aktiva inn i tre aktiva:
Du kan dele ett aktiva i flere aktiva, for eksempel når du skal distribuere et aktiva på tre forskjellige avdelinger. Da kan du for eksempel overføre 25 prosent av anskaffelseskosten og avskrivningen for det originale aktivaet til et annet aktiva, og 45 prosent til et tredje aktiva. De resterende 30 prosent blir igjen i det opprinnelige aktivaet.

1. Definer to nye aktiva. Angi den nye avdelingen i feltet **Avdelingskode**.
2. Tilordne avskrivningstablåer for aktiva til de nye aktivaene. Hvis du vil ha mer informasjon, se [Anskaffe aktiva](fa-how-acquire.md).
3. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivareklass.kladder**, og deretter velger du den beslektede koblingen.
4. Opprett to reklassifiseringskladdelinjer, én for hvert nye aktiva.
5. På den første linjen angir du det andre aktivaet i **Nytt aktivanr.**-feltet og 25 i **Reklass.anskaff.kost %**-feltet.
6. På den andre linjen angir du det tredje aktivaet i **Nytt aktivanr.**-feltet og 40 i **Reklass.anskaff.kost %**-feltet.
7. På begge linjene merker du av for **Reklass.anskaffelseskost** og **Reklass.avskrivning**.   
8. Velg handlingen **Reklassifiser**.

    To linjer opprettes nå i aktivafinanskladden ved hjelp av malen og kladden du oppgav for det angitte avskrivningstablået, i vinduet **Aktivakladdoppsett**. Se [Definere avskriving av aktiva](fa-how-setup-depreciation.md) for mer informasjon.    
9. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivafinanskladder**, og deretter velger du den beslektede koblingen.
10. I **Aktiva finanskladd**-vinduet velger du **Bokfør**-handlingen for å bokføre reklassifiseringen du utførte i trinn 4 til 8.

## <a name="to-combine-two-fixed-assets-into-one"></a>Slik kombinerer du to aktiva til en:
Du kan kombinere flere aktiva til ett aktiva, for eksempel når du flytter distribuerte aktiva til én avdeling. Hvis du har bokført anskaffelseskostnader og avskrivning for aktivaet som skal flyttes, kombineres disse verdiene i ett aktiva.

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivareklass.kladder**, og deretter velger du den beslektede koblingen.
2. Opprett en reklassifiseringskladd der **Aktivanr.**-feltet inneholder aktivaet som skal flyttes/kombineres, og **Nytt aktivanr.**-feltet inneholder anleggsmidlet som det vil bli kombinert med.
3. La **Reklass.anskaff.kost %**-feltet stå tomt for å flytte/kombinere hele anskaffelseskosten.    
4. Merk av for **Reklass.anskaffelseskost** og **Reklass.avskrivning**.
5. I fanebladet **Handlinger** velger du **Reklassifiser**.

    To linjer opprettes nå i aktivafinanskladden ved hjelp av malen og kladden du oppgav for det angitte avskrivningstablået, i vinduet **Aktivakladdoppsett**. Se [Definere avskriving av aktiva](fa-how-setup-depreciation.md) for mer informasjon.   
6. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivafinanskladder**, og deretter velger du den beslektede koblingen.
7. I **Aktiva finanskladd**-vinduet velger du **Bokfør**-handlingen for å bokføre reklassifiseringen du utførte i trinn 2 til 5.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Slik viser du endret avskrivningstablåverdier på grunn av aktivareklassifisering:
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktiva - bokført verdi 02**, og deretter velger du den beslektede koblingen.
2. Fyll ut feltene etter behov.
3. Velg knappen **Skriv ut** eller **Forhåndsvisning**.  

## <a name="see-also"></a>Se også
[Anleggsmidler](fa-manage.md)  
[Definere aktiva](fa-setup.md)  
[Finans](finance.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

