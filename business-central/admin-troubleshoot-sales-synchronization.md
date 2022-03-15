---
title: Feilsøke synkroniseringsfeil
description: Dette emner gir veiledning for identifisering, feilsøking og løsning av synkroniseringsfeil.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: a7490c896daabd05ef0b0bb7d125e15963d83320
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381489"
---
# <a name="troubleshooting-synchronization-errors"></a>Feilsøke synkroniseringsfeil


Mange bevegelige deler er involvert i integrasjon av [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)], og noen ganger går det galt. I dette emnet omtales noen av de typiske feilene som oppstår, og det oppgis noen punkter for hvordan de skal løses.

Feil oppstår ofte enten på grunn av noe en bruker har gjort med koblede poster, eller fordi noe er galt med hvordan integrasjonen er konfigurert. Ved feil relatert til koblede poster kan brukere løse disse selv. Disse feilene skyldes handlinger som sletting av data i én bedriftsapp, men ikke i begge bedriftsappene, og påfølgende synkronisering. Hvis du vil ha mer informasjon, kan du se [Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md).

Feil som er relatert til hvordan integrasjonen er satt opp, må vanligvis håndteres av en administrator. Du kan se disse feilene på siden **Synkroniseringsfeil ved integrasjon**. 

Tabellen nedenfor inneholder eksempler på vanlige problemer:  

|Problem  |Løsning  |
|---------|---------|
|Tillatelsene og rollene som er tilordnet til integreringsbrukeren, er ikke riktige. | Denne feilen oppstår fra [!INCLUDE[prod_short](includes/cds_long_md.md)], og den inneholder ofte følgende tekst Hovedbruker (Id=\<user id>, type=8) mangler \<privilegeName>-rettigheten. Denne feilen oppstår fordi integreringsbrukeren mangler en rettighet som gir den tilgang til en enhet. Vanligvis oppstår denne feilen hvis du synkroniserer egendefinerte enheter, eller hvis du har en app installert i [!INCLUDE[prod_short](includes/cds_long_md.md)] som krever tillatelse til å få tilgang til andre [!INCLUDE[prod_short](includes/cds_long_md.md)]-enheter. Du kan løse denne feilen ved å tilordne tillatelsen til integreringsbrukeren i [!INCLUDE[prod_short](includes/cds_long_md.md)].<br><br> Du finner integreringsbrukernavnet på siden **Tilkoblingsoppsett for Dataverse**. Feilmeldingen vil gi navnet til tillatelsen, noe som kan hjelpe deg med å identifisere enheten du trenger tillatelse til. Du legger til den manglende rettigheten ved å logge deg på [!INCLUDE[prod_short](includes/cds_long_md.md)] med en administratorkonto og redigere sikkerhetsrollen som er tilordnet integreringsbrukeren. Hvis du vil ha mer informasjon, kan du se [Opprett eller rediger en sikkerhetsrolle for å administrere tilgang](/power-platform/admin/create-edit-security-role). |
|Du kobler til en post som bruker en annen post som ikke er kombinert. Det kan for eksempel være en kunde som ikke er kombinert med en valuta eller en vare som enheten ikke er kombinert for. | Du må først ha den avhengige posten, for eksempel en valuta eller enhet, og deretter forsøke du tilkoblingen på nytt. |

Nedenfor følger noen verktøy om synkroniseringsfeilsiden for integrasjon som kan hjelpe deg med å løse disse problemene manuelt.  

* Feltene **Kilde** og **Destinasjon** kan inneholde koblinger til raden der feilen ble funnet. Klikk på koblingen for å undersøke feilen.  
* Handlingene **Slett oppføringer eldre enn 7 dager** og **Slett alle oppføringer** rydder opp i listen. Vanligvis bruker du disse handlingene etter at du har løst årsaken til en feil som påvirker mange poster. Du må imidlertid være forsiktig. Disse handlingene kan slette feil som fremdeles er relevante.
* Handlingen **Vis feilkallstakk** viser informasjon som kan bidra til å identifisere årsaken til feilen. Hvis du ikke kan løse problemet selv og du vil sende en støtteforespørsel, tar du med informasjonen i støtteforespørselen.

## <a name="see-also"></a>Se også
[Integrere med Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Sette opp brukerkontoer for integrasjon med Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Sette opp en tilkobling til Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
