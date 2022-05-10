---
title: Bokmerke kobling til en side eller rapport i rollesenteret
description: Ved hjelp av det nye bokmerkeikonet kan du legge til en handling som åpner en side eller en rapport fra navigasjonsmenyen i rollesenteret.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 833cc4aff2aefbd4ddd69fb340896ce5b3b90457
ms.sourcegitcommit: f9143302b8271f5924a027cacdf29dc37c95f4c6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2022
ms.locfileid: "8655205"
---
# <a name="bookmark-a-page-or-report-on-your-role-center"></a>Bokmerke en side eller rapport i rollesenteret
Ved hjelp av det nye bokmerkeikonet kan du legge til en handling som åpner en side eller en rapport fra navigasjonsmenyen i rollesenteret. Med bokmerker kan du komme raskt i kontakt med favorittinnhold eller forretningsoppgaver. Du legger til bokmerket fra målsiden eller rapporten, som betyr skjermbildet du vil at koblingen i rollesenteret skal åpne.

Ikonet for bokmerke vises i øvre høyre hjørne på en side og også i **Fortell meg**-vinduet hvor du effektivt kan sette bokmerke på flere sider eller rapporter. Hvis det allerede finnes et bokmerke for siden, er ikonet mørkt, og verktøytipet viser "Bokmerket".

## <a name="to-bookmark-the-target-page"></a>Slik bokmerker du målsiden
1. Åpne en side du vil ha en kobling for i rollesenteret.
2. Velg ![Bokmerke](media/ui_bookmark_icon.png "Bokmerke")-ikonet .

En handling navngitt etter siden er nå lagt til på navigasjonsmenyen i rollesenteret ditt.

## <a name="to-bookmark-the-target-report"></a>Slik bokmerker du målrapporten
1. Åpne en rapportforespørselsside du vil ha en kobling for i rollesenteret.
2. Velg ![Bokmerke](media/ui_bookmark_icon.png "Bokmerke")-ikonet .

En handling navngitt etter rapporten er nå lagt til på navigasjonsmenyen i rollesenteret ditt.

## <a name="to-bookmark-a-page-or-report-from-the-tell-me-window"></a>Slik bokmerker du en side eller rapport fra Fortell meg-vinduet
1. Åpne **Fortell meg**-vinduet, og angi for eksempel **Ordrer**.
2. Hold musepekeren over søkeresultatet for **Ordrer**-siden eller rapporten, og velg ![Bokmerke](media/ui_bookmark_icon.png "Bokmerke")-ikonet .

En handling navngitt etter siden eller rapporten er nå lagt til på navigasjonsmenyen i rollesenteret ditt.


## <a name="frequently-asked-questions"></a>Vanlige spørsmål  

- **Kan jeg omorganisere bokmerkene?**  
Ja. Du kan tilpasse rollesenteret og flytte handlinger til en mer optimal rekkefølge eller flytte dem til eksisterende grupper eller undergrupper.  
Finn ut hvordan du kan [Tilpasse arbeidsområdet](ui-personalization-user.md).

- **Hvordan fjerner jeg et bokmerke?**  
På målsiden eller i rapporten velger du bokmerkeikonet på nytt for å fjerne den aktuelle handlingen fra rollesenteret. Du kan også tilpasse rollesenteret og skjule handlinger midlertidig uten å fjerne dem fullstendig.

- **Hvor finner jeg bokmerkene?**  
Når du legger til et bokmerke på en side eller rapport, legges den nye handlingen til på den øverste navigasjonsmenyen på gjeldende startside (rollesenter). Hvis du har mange handlinger, må du kanskje aktivere **Mer**-knappen for å vise alle dem fordi den nye handlingen alltid legges til på slutten av disse handlingene.
<!-- Should we add a screenshot here? -->

- **Jeg har ikke et bokmerkeikon. Er noe galt?**  
Muligheten til å sette bokmerke på en side eller rapport er én av mange brukertilpasningsfunksjoner i Business Central. Hvis bokmerkeikonet ikke vises, er det sannsynlig at systemansvarlig har deaktivert tilpassing.

- **Hvorfor kan jeg ikke sette bokmerke på visse sider eller rapporter?**  
Ikke alle sider og rapporter kan bokmerkes. Når en side eller en rapport kjøres innenfor en spesiell kontekst som styres av forretningsprogrammet, vises ikke bokmerkeikonet. Sider som ikke finnes i **Fortell meg** -vinduet, men som startes fra andre steder, viser for eksempel ikke et bokmerkeikon. Rapportforespørselssider som bare brukes til å samle filtre uten å kjøre rapporten, viser heller ikke et bokmerkeikon.

  Se tekniske detaljer om [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) og [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

- **Når tilpassingen fjernes, fjernes også bokmerkene automatisk?**  
Ja. Bokmerker ligger på navigasjonsmenyen. Hvis du fjerner endringer av navigasjonsmenyen fra en hvilken som helst side, eller fjerner all tilpassinger i rollesenteret, fjernes alle de nye handlingene for godt.

- **Hvorfor fortsetter bokmerkeikonet med å angi at det fremdeles ikke er bokmerket?**  
Når du legger til et bokmerke, legges den nye handlingen til i navigasjonsmenyen i rollesenteret, og påfølgende besøk på siden eller rapporten viser et mørkt bokmerkeikon. Hvis du tilpasser rollesenteret og omorganiserer handlingene ved å flytte dem til grupper, vil bokmerkeikonet ikke lenger være mørkt, og du kan legge til et annet bokmerke på den samme siden eller rapporten. På denne måten kan du legge til flere handlinger på samme side eller rapport, og kategorisere dem i forskjellige grupper.

- **Hvorfor viser koblingen til en rapport en annen rapport?**  
Noen rapporter kan erstattes av andre rapporter etter at en utvidelse er brukt på Business Central. Når erstatningen forekommer, oppdateres ikke teksten i den nye handlingen, og navnet på den opprinnelige rapporten vil bli vist, men går til den nye rapporten. Hvis du vil korrigere teksten i den nye handlingen, kan du fjerne den nye handlingen og legge den til på nytt.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

- **Er bokmerking tilgjengelig for XML-porter?**  
Antall På dette tidspunktet er det ikke mulig å legge til handlinger i åpne XML-porter fra brukergrensesnittet.

- **Vil bokmerkene bli oversatt når jeg endrer språk i Business Central?**  
Når du legger til en ny handling, brukes oversatt tekst som var tilgjengelig på det tidspunktet, ved bokmerking. Hvis ny oversatt tekst legges til senere, vil ikke den nye handlingen inneholde de nyere oversettelsene.

- **Hvorfor kan jeg ikke legge til tekst på en side direkte etter at den er åpnet med bokmerket?**<br> Når en side er bokmerke, åpnes siden alltid i visningsmodus fra bokmerket, selv om den var i redigeringsmodus da den ble bokmerket. Hvis du velger **Gjør endringer på siden**-ikonet, ![Viser blyantikonet for redigering av siden.](media/edit-pencil.png) kan du legge til tekst i de redigerbare feltene.


## <a name="see-also"></a>Se også
[Tilpasse arbeidsområdet](ui-personalization-user.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]