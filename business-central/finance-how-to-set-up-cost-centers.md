---
title: Definere kostsentre | Microsoft-dokumentasjon
description: Kostsentre er avdelinger som er ansvarlig for kostnader og inntekter. Diagrammet med kostsentre ligner dimensjonsinformasjonen for finans.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7362518cbade8132fb07f49e7b2e9be67c4bce29
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-cost-centers"></a>Definere kostsentre
Kostsentre er avdelinger som er ansvarlig for kostnader og inntekter. Diagrammet med kostsentre ligner dimensjonsinformasjonen for finans. Du kan definere diagrammet med kostsentre på følgende måter:  

-   Overfør dimensjonsverdier i finans til diagrammet med kostsentre. Du kan foreta alle nødvendige justeringer etter overføringen.  
-   Opprett et nytt kostsenterdiagram som er uavhengig av finans, eller legg til et nytt kostsenter i et eksisterende kostsenterdiagram. Du må opprette hvert enkelt kostsenter individuelt.  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Slik overfører du dimensjonsverdier i finans til diagrammet med kostsentre:  
1.  Angi en dimensjon som kostsenterdimensjon i vinduet **Oppdater kostregnskapsdimensjoner**. Det er bare verdier fra denne dimensjonen som overføres.  
2.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Diagram med kostsentre**, og velg deretter den relaterte koblingen.  
3.  I fanebladet **Handlinger**, under **Funksjoner** velger du **Hent kostsentre fra dimensjon** for å overføre dimensjonsverdier til kostsenterdiagrammet. Funksjonen overfører dimensjonsverdiene som du definerte i trinn 1.  

    > [!NOTE]  
    >  Du kan konfigurere feltet **Juster kostsenterdimensjon** slik at det definerer en enveissynkronisering av dimensjonsverdier fra finans til diagrammet med kostsentre. Du kan ikke definere en synkronisering av diagrammet med kostsentre til dimensjonsverdier fra finans.  

Diagrammet med kostsentre inneholder nå alle angitte dimensjonsverdier fra finans og inkluderer titler og delsummer.  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a>Slik oppretter du nye kostsentre i vinduet Diagram med kostsentre:  
Du kan definere og vedlikeholde kostsentre i kortet **Kostsenterkort** eller vinduet **Diagram med kostsentre**. I denne fremgangsmåten definerer sentre i vinduet **Diagram med kostsentre**.  

1. Åpne vinduet **Diagram med kostsentre** i redigeringsmodus.  
2. Angi kostsenterkoden i **Kode**-feltet. Alle kostsentre må ha en kode.  
3. Skriv inn navnet på kostsenteret i **Navn**-feltet.  
4. Velg rullegardinpilen i feltet **Linjetype** for å angi formålet med kostsenteret.  

    - For kostsentre av typen **Sum** må du fylle ut feltet **Sammentelling**. Bruk **eller**-operatoren, som er en loddrett linje (**&#124;**), til å angi områder for kostsentre.  
    - Når det gjelder kostsentre av linjetypen **Til-sum**, fylles dette feltet ut automatisk når du bruker innrykksfunksjonen.  
5.  Fyll ut feltene **Sorteringsrekkefølge** og **Kostundertype**.  
6.  Velg den neste tomme linjen for å opprette et nytt kostsenter, og gjenta deretter trinn 2 til 5.  
7.  Når du har definert alle kostsentrene, velger du **Rykk inn kostsentre**. Velg **Ja**-knappen.  

> [!IMPORTANT]  
>  Hvis du har angitt definisjoner i **Sammentelling**-feltene for **Til-sum**-kostsentre før du kjører innrykksfunksjonen, må du angi dem på nytt. Funksjonen overskriver verdiene i alle **Til-sum**-felt.  

## <a name="see-also"></a>Se også  
[Gjøre rede for kostnader](finance-manage-cost-accounting.md)  
[Definere kost.regnskap](finance-set-up-cost-accounting.md)   
[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md)   
[Om kostregnskap](finance-about-cost-accounting.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

