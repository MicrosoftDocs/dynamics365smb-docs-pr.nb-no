---
title: Definere kostobjekter | Microsoft-dokumentasjon
description: Lær hvordan du definerer kostobjekter, som ligner på dimensjonene i Finans.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: ae2ca5b4c6f63a004d42c2ae1ef9f0efa95dd02c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306031"
---
# <a name="set-up-cost-objects"></a>Definere kostobjekter
Kostobjekter er et selskaps prosjekter, produkter eller tjenester. Diagrammet med kostobjekter ligner dimensjonsinformasjonen for finans. Du kan definere diagrammet med kostobjekter på følgende måter:  

* Overfør dimensjonsverdier i finans til diagrammet med kostobjekter. Du kan foreta alle nødvendige justeringer etter overføringen.  
* Opprett et nytt kostobjektdiagram som er uavhengig av finans, eller legg til et nytt kostobjekt i et eksisterende kostobjektdiagram. Du må opprette hvert enkelt kostobjekt individuelt.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Slik overfører du dimensjonsverdier fra finans til diagrammet med kostobjekter:  
1.  Angi en dimensjon som kostobjektdimensjon på siden **Oppdatere KR-dimensjoner**. Det er bare verdier fra denne dimensjonen som overføres.  
2.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Diagram med kostobjekter**, og velg deretter den relaterte koblingen.  
3.  Velg **Hent kostobjekter fra dimensjon** for å overføre dimensjonsverdier til kostobjektdiagrammet. Funksjonen overfører dimensjonsverdiene som du definerte i trinn 1.  

    > [!NOTE]  
    >  Du kan konfigurere feltet **Juster kostobjektdimensjon** slik at det definerer en enveissynkronisering av dimensjonsverdier fra finans til diagrammet med kostobjekter. Du kan ikke definere en synkronisering av diagrammet med kostobjekter til dimensjonsverdier fra finans.  

Diagrammet med kostobjektene inneholder nå alle angitte dimensjonsverdier fra finans og inkluderer titler og delsummer.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Slik oppretter du nye kostobjekter på siden Diagram med kostobjekter:  
Du kan definere og vedlikeholde kostobjekter i kortet **Kostobjektkort** eller siden **Diagram med kostobjekter**. I denne fremgangsmåten definerer objekter på siden **Diagram med kostobjekter**.  

1.  Åpne siden **Diagram med kostobjekter** i redigeringsmodus.  
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
