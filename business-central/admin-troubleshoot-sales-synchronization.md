---
title: Feilsøke synkroniseringsfeil | Microsoft Docs
description: Gir veiledning for identifisering og løsing av synkroniseringsfeil.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: bb3c0684d476fbba2a23a73dd821384d32afbbab
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777044"
---
# <a name="troubleshooting-synchronization-errors"></a>Feilsøke synkroniseringsfeil
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Mange bevegelige deler er involvert i integrasjon av [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)], og noen ganger går det galt. I dette emnet omtales noen av de typiske feilene som oppstår, og det oppgis noen punkter for hvordan de skal løses.

Feil oppstår ofte enten på grunn av noe en bruker har gjort med koblede poster, eller fordi noe er galt med hvordan integrasjonen er konfigurert. Ved feil relatert til koblede poster kan brukere løse disse selv. Disse feilene skyldes handlinger som sletting av data i én bedriftsapp, men ikke i begge bedriftsappene, og påfølgende synkronisering. Hvis du vil ha mer informasjon, kan du se [Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Eksempel
Denne videoen viser et eksempel på hvordan du feilsøker feil som skjedde under synkronisering med Sales. Prosessen vil være den samme for alle integreringer. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Feil som er relatert til hvordan integrasjonen er satt opp, må vanligvis håndteres av en administrator. Du kan se disse feilene på siden **Synkroniseringsfeil ved integrasjon**. Eksempler på noen vanlige problemer er:  
  
* Tillatelsene og rollene som er tilordnet til brukere, er ikke korrekte.  
* Administratorkontoen ble angitt som integrasjonsbrukeren.  
* Integrasjonsbrukerens passord er satt til å kreve en endring når brukeren logger seg på.  
* Valutakursene for valutaer er ikke angitt i én av appene.  
  
Du må løse feilene manuelt, men siden hjelper deg på noen måter. Eksempel:  

* Feltene **Kilde** og **Destinasjon** kan inneholde koblinger til raden der feilen ble funnet. Klikk på koblingen for å undersøke feilen.  
* Handlingene **Slett oppføringer eldre enn 7 dager** og **Slett alle oppføringer** rydder opp i listen. Vanligvis bruker du disse handlingene etter at du har løst årsaken til en feil som påvirker mange poster. Du må imidlertid være forsiktig. Disse handlingene kan slette feil som fremdeles er relevante.

Tidsangivelser av poster kan iblant forårsake konflikter. Tabellen CDS-integreringspost beholder tidsstemplene Siste synkronisering endret den og Siste CDS-synkronisering endret den for å få den siste integrasjonen gjort i begge retninger for en rad. Disse tidsstemplene sammenlignes med tidsstempler i Business Central sentraler og salgsposter. I Business Central er tidsstempelet i tabellen for integreringspost.

Du kan filtrere på poster som skal synkroniseres ved å sammenligne radtidsstempler i tabellen Tilordning for integreringstabell i feltene Filter for siste synkr.endr. og Filter for siste synkr.endr. i intgr.tab."

Feilmeldingen om konflikt Kan ikke oppdatere kundeposten fordi den har en senere endringsdato enn forretningsforbindelsesposten eller Kan ikke oppdatere forretningsforbindelsesposten fordi den har en senere endringsdato enn kundeposten kan vises hvis en rad har et tidsstempel som er større enn IntegrationTableMapping.Filter for siste synkr.endr., men den ikke er nyere enn tidsstempelet for salgsintegreringsposten. Det betyr at kilderaden ble synkronisert manuelt, og ikke av posten i jobbkøen. 

Konflikten oppstår fordi målraden også ble endret – radtidsstemplet er nyere enn tidsstempelet for salgsintegrasjonsposten. Målkontrollen skjer bare for toveis tabeller. 

Disse postene flyttes nå til siden "Hoppet over synkroniserte poster", som du åpner fra siden Tilkoblingsoppsett for Microsoft Dynamics i Business Central. Der kan du angi endringene du vil beholde, og deretter synkronisere postene på nytt.

## <a name="remove-couplings-between-records"></a>Fjerne koblinger mellom poster
Når noe går galt i integrasjonen din, og du må frakoble poster for å stoppe synkroniseringen av dem, kan du gjøre det for én eller flere poster om gangen. Du kan slette én eller flere poster fra listesider eller siden **Feil ved synkronisering av koblede data** ved å velge én eller flere linjer og velge **Slett kobling**. Du kan også fjerne alle koblingene for én eller flere tabelltilordninger på siden **Tilordninger for integreringstabell**. 

## <a name="see-also"></a>Se også
[Integrere med Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Sette opp brukerkontoer for integrasjon med Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Sette opp en tilkobling til Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]