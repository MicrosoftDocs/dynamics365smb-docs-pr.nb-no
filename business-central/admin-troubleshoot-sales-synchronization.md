---
title: Feilsøke synkroniseringsfeil | Microsoft Docs
description: Gir veiledning for identifisering og løsing av synkroniseringsfeil.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 729a767c0cb4bb330a463e14c7eb6a4f8fd7d909
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304263"
---
# <a name="troubleshooting-synchronization-errors"></a>Feilsøke synkroniseringsfeil
Mange bevegelige deler er involvert i integrasjon av [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)], og noen ganger går det galt. I dette emnet omtales noen av de typiske feilene som oppstår, og det oppgis noen punkter for hvordan de skal løses.

Feil oppstår ofte enten på grunn av noe en bruker har gjort med koblede poster eller fordi noe er galt med hvordan integrasjonen er satt opp. Ved feil relatert til koblede poster kan brukere løse disse selv. Disse feilene skyldes handlinger som sletting av en post i én bedriftsapp, men ikke i begge bedriftsappene, og påfølgende synkronisering. Hvis du vil ha mer informasjon, kan du se [Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Feil som er relatert til hvordan integrasjonen er satt opp, må vanligvis håndteres av en administrator. Du kan se disse feilene på siden **Synkroniseringsfeil ved integrasjon**. Eksempler på noen vanlige problemer er:  
  
* Tillatelsene og rollene som er tilordnet til brukere, er ikke korrekte.  
* Administratorkontoen ble angitt som integrasjonsbrukeren.  
* Integrasjonsbrukerens passord er satt til å kreve en endring når brukeren logger seg på.  
* Valutakursene for valutaer er ikke angitt i én av appene.  
  
Du må løse feilene manuelt, men siden hjelper deg på noen måter. Eksempel:  

* Feltene **Kilde** og **Destinasjon** kan inneholde koblinger til posten der feilen ble funnet. Klikk på koblingen for å åpne posten og undersøke feilen.  
* Handlingene **Slett oppføringer eldre enn 7 dager** og **Slett alle oppføringer** rydder opp i listen. Vanligvis bruker du disse handlingene etter at du har løst årsaken til en feil som påvirker mange poster. Du må imidlertid være forsiktig. Disse handlingene kan slette feil som fremdeles er relevante.

## <a name="see-also"></a>Se også
[Integrere med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Sette opp brukerkontoer for integrasjon med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Sette opp en tilkobling til [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md)  