---
title: Definere kostobjekter | Microsoft-dokumentasjon
description: "Lær hvordan du definerer kostobjekter, som ligner på dimensjonene i Finans."
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
ms.openlocfilehash: 3eb90611939dce2134d9413812918c2afb82c083
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-cost-objects"></a>Definere kostobjekter
Kostobjekter er et selskaps prosjekter, produkter eller tjenester. Diagrammet med kostobjekter ligner dimensjonsinformasjonen for finans. Du kan definere diagrammet med kostobjekter på følgende måter:  

* Overfør dimensjonsverdier i finans til diagrammet med kostobjekter. Du kan foreta alle nødvendige justeringer etter overføringen.  
* Opprett et nytt kostobjektdiagram som er uavhengig av finans, eller legg til et nytt kostobjekt i et eksisterende kostobjektdiagram. Du må opprette hvert enkelt kostobjekt individuelt.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Slik overfører du dimensjonsverdier fra finans til diagrammet med kostobjekter:  
1.  Angi en dimensjon som kostobjektdimensjon i vinduet **Oppdatere KR-dimensjoner**. Det er bare verdier fra denne dimensjonen som overføres.  
2.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Diagram med kostobjekter**, og velg deretter den relaterte koblingen.  
3.  Velg **Hent kostobjekter fra dimensjon** for å overføre dimensjonsverdier til kostobjektdiagrammet. Funksjonen overfører dimensjonsverdiene som du definerte i trinn 1.  

    > [!NOTE]  
    >  Du kan konfigurere feltet **Juster kostobjektdimensjon** slik at det definerer en enveissynkronisering av dimensjonsverdier fra finans til diagrammet med kostobjekter. Du kan ikke definere en synkronisering av diagrammet med kostobjekter til dimensjonsverdier fra finans.  

Diagrammet med kostobjektene inneholder nå alle angitte dimensjonsverdier fra finans og inkluderer titler og delsummer.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-window"></a>Slik oppretter du nye kostobjekter i vinduet Diagram med kostobjekter:  
Du kan definere og vedlikeholde kostobjekter i kortet **Kostobjektkort** eller vinduet **Diagram med kostobjekter**. I denne fremgangsmåten definerer objekter i vinduet **Diagram med kostobjekter**.  

1.  Åpne vinduet **Diagram med kostobjekter** i redigeringsmodus.  
2.  Angi kostobjektkoden i **Kode**-feltet. Alle kostobjekter må ha en kode.  
3.  Skriv inn kostobjektnavnet i **Navn**-feltet.  
4.  Velg rullegardinpilen i feltet **Linjetype** for å angi formålet med kostobjektet.  

    * Når det gjelder kostobjekter av linjetypen **Sum**, må du fylle ut feltet **Total fra/til**. Bruk **eller**-operatoren, som er en loddrett linje (**&#124;**), til å angi områder for kostobjekter.  
    * Når det gjelder kostobjekter av linjetypen **Til-sum**, fylles dette feltet ut automatisk når du bruker innrykksfunksjonen.  
5.  Fyll ut feltet **Sorteringsrekkefølge**.  
6.  Velg den neste tomme linjen for å opprette et nytt kostobjekt, og gjenta deretter trinn 2 til 5.  
7.  Når du har definert alle kostsentrene, velger du **Rykk inn kostobjekter**. Velg **Ja**-knappen.  

> [!IMPORTANT]  
>  Hvis du har angitt definisjoner i feltene **Total fra/til** for **Til-sum**-kostobjekter før du kjører innrykksfunksjonen, må du angi dem på nytt. Funksjonen overskriver verdiene i alle **Til-sum**-felt.  

## <a name="see-also"></a>Se også  
[Gjøre rede for kostnader](finance-manage-cost-accounting.md)  
[Definere kostsentre og kostobjekter for kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Balanser mellom kosttype, kostsenter og kostobjekt](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Definere kost.regnskap](finance-set-up-cost-accounting.md)   
[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md)   
[Om kostregnskap](finance-about-cost-accounting.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

