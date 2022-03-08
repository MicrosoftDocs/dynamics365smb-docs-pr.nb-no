---
title: Konfigurere en dokumentutvekslingstjeneste | Microsoft-dokumentasjon
description: Du bruker en ekstern tjenesteleverandør til å utveksle elektroniske dokumenter med handelspartnere.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 75880e3315933831bf20fa9c5e8ce6a1528b935e
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785099"
---
# <a name="set-up-a-document-exchange-service"></a>Konfigurere en dokumentutvekslingstjeneste
Du bruker en ekstern tjenesteleverandør til å utveksle elektroniske dokumenter med handelspartnere. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Slik konfigurerer du en dokumentutvekslingstjeneste:  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett av dokumentutvekslingstjeneste**, og velg deretter den relaterte koblingen.  
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
