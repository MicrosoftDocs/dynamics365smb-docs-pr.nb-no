---
title: Konfigurere en dokumentutvekslingstjeneste
description: Du bruker en ekstern tjenesteleverandør til å utveksle elektroniske dokumenter med handelspartnere ved å bruke Oppsett av dokumentutvekslingstjeneste.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 357c48c6b7ed8e2d44316805bba04ff9236f0e9b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436301"
---
# <a name="set-up-a-document-exchange-service"></a>Konfigurere en dokumentutvekslingstjeneste
Du bruker en ekstern tjenesteleverandør til å utveksle elektroniske dokumenter med handelspartnere. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Slik konfigurerer du en dokumentutvekslingstjeneste:  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Oppsett av dokumentutvekslingstjeneste**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Brukeragent**|Skriv inn tekst som kan brukes til å identifisere firmaet i dokumentutvekslingsprosesser.|  
    |**ID for leietaker for dokumentutveksling**|Angi leietakeren i dokumentutvekslingstjenesten som representerer firmaet. Denne leveres av leverandøren av dokumentutvekslingstjenesten.|  
    |**Aktivert**|Angi om tjenesten er aktivert. **Obs!** Så snart du aktiverer tjenesten, opprettes minst to jobbkøposter for å behandle trafikken av elektroniske dokumenter inn og ut av [!INCLUDE[prod_short](includes/prod_short.md)]. Når du deaktiverer tjenesten, slettes jobbkøpostene.|  
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


[!INCLUDE[footer-include](includes/footer-banner.md)]