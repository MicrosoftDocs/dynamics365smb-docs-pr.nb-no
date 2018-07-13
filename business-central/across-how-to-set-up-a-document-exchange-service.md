---
title: Konfigurere en dokumentutvekslingstjeneste | Microsoft-dokumentasjon
description: "Du bruker en ekstern tjenesteleverandør til å utveksle elektroniske dokumenter med handelspartnere."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 06/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 0e57f02f1689de12e75595a26c489eeda68a4b89
ms.contentlocale: nb-no
ms.lasthandoff: 06/11/2018

---
# <a name="set-up-a-document-exchange-service"></a>Konfigurere en dokumentutvekslingstjeneste
Du bruker en ekstern tjenesteleverandør til å utveksle elektroniske dokumenter med handelspartnere. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Slik konfigurerer du en dokumentutvekslingstjeneste:  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Oppsett av dokumentutvekslingstjeneste**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Brukeragent**|Skriv inn tekst som kan brukes til å identifisere firmaet i dokumentutvekslingsprosesser.|  
    |**ID for leietaker for dokumentutveksling**|Angi leietakeren i dokumentutvekslingstjenesten som representerer firmaet. Denne leveres av leverandøren av dokumentutvekslingstjenesten.|  
    |**Aktivert**|Angi om tjenesten er aktivert. **Obs!** Så snart du aktiverer tjenesten, opprettes minst to jobbkøposter for å behandle trafikken av elektroniske dokumenter inn og ut av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Når du deaktiverer tjenesten, slettes jobbkøpostene.|  
    |**Nettadresse for registrering**|Angi nettsiden der du registrerer deg for dokumentutvekslingstjenesten.|  
    |**Nettadresse for tjeneste**|Angi adressen til dokumentutvekslingstjenesten, som vil bli kalt når du sender og mottar elektroniske dokumenter.|  
    |**Nettadresse for pålogging**|Angi påloggingssiden for dokumentutvekslingstjenesten, som er nettsiden der du skriver inn firmaets brukernavn og passord for å logge på tjenesten.|  
    |**Forbrukernøkkel**|Skriv inn den tretrinns OAuth-nøkkelen for forbrukernøkkelen. Denne leveres av leverandøren av dokumentutvekslingstjenesten.|  
    |**Forbrukerhemmelighet**|Angi hemmeligheten som beskytter forbrukernøkkelen. Denne leveres av leverandøren av dokumentutvekslingstjenesten.|  
    |**Token**|Skriv inn den tretrinns OAuth-nøkkelen for tokenet. Denne leveres av leverandøren av dokumentutvekslingstjenesten.|  
    |**Tokenhemmelighet**|Angi hemmeligheten som beskytter tokenet. Denne leveres av leverandøren av dokumentutvekslingstjenesten.|  

    > [!NOTE]  
    > Påloggingsdataene krypteres automatisk.

## <a name="see-also"></a>Se også  
[Definere datautveksling](across-set-up-data-exchange.md)  
[Utveksle data elektronisk](across-data-exchange.md)

