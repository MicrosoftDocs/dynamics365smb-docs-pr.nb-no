---
title: Klassifisere datasensitivitet
description: Du må angi hvilken type opplysninger du lagrer om personer slik at du kan svare på forespørsler fra dataemner.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/01/2020
ms.openlocfilehash: f93e4a5757039c8598ba73112d1059dbb61406f5
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378676"
---
# <a name="classifying-data-sensitivity"></a>Klassifisere datasensitivitet
Hvis du vil klassifisere feltene som inneholder sensitive opplysninger eller personopplysninger, kan en Microsoft-partner angi ```DataClassification```-egenskapen for felt. Dette krever tilgang til databasetabellene via utviklingsmiljø eller ved å kjøre et Windows PowerShell-skript. Hvis du vil ha mer informasjon, kan du se [Klassifisere data](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data).  

Du kan som kunde legge til et sekundært klassifiseringsnivå ved å angi sensitivitetsnivåer for opplysninger du lagrer i standardfelt eller egendefinerte felt. Klassifisering av datasensitivitet sikrer at du vet hvor personopplysninger lagres i systemet, og dette gjør det lettere å svare på forespørsler fra dataemner. For eksempel hvis en kontakt eller kunden ber deg om å eksportere personopplysningene. Hvis du vil ha mer informasjon, kan du se [Svare på forespørsler om personopplysninger](admin-responding-to-requests-about-personal-data.md).

> [!Important]
> Microsoft leverer denne funksjonen for klassifisering av datasensitivitet for å gjøre den enklere for deg. Det er ditt ansvar å klassifisere dataene riktig og samsvare med lover og regler som gjelder for deg. Microsoft fraskriver seg alt ansvar for eventuelle krav knyttet til klassifiseringen av dataene.  

Tabellen nedenfor beskriver nivåene for datasensitivitet som du kan tilordne.

|Sensitivitet|Description|
|----|----|
|Sensitiv | Informasjon om et dataemnets rase eller etnisk opprinnelse, politiske meninger, religiøse trosretninger, deltakelse i fagforeninger, fysiske eller mentale helse, seksualitet eller detaljer om kriminelle handlinger. |
|Personlig | Informasjon som kan brukes til å identifisere et dataemne, enten direkte eller sammen med andre data eller annen informasjon.|
|Konfidensielt | Forretningsdata du bruker for regnskap eller andre forretningsformål og ikke vil vise til andre enheter. Dette kan for eksempel inneholde finansposter.|
|Normal | Generelle data som ikke tilhører andre kategorier.|

## <a name="how-do-i-classify-my-data"></a>Hvordan klassifiserer jeg dataene?
Klassifisering av sensitiviteten til av ett og ett felt for et stort antall felt ville tatt lang tid. For å bidra til å øke hastigheten på prosessen kan vi tilby verktøy du kan bruke til masseklassifisering av sensitiviteten til felt og deretter finjustere klassifiseringer for spesifikke felt. Du finner verktøy i dataklassifiseringsforslaget, som er tilgjengelig i rollesenteret for på Administrasjon av brukere, brukergrupper og tillatelser. Du må være en systemansvarlig for å bruke forslaget.

> [!Important]
> Når du åpner dataklassifiseringsforslaget for første gang, vil det være tomt. Du må kjøre veiledningen for dataklassifisering for å generere en liste over feltene. Du starter veiledningen ved å velge handlingen **Konfigurer dataklassifiseringer**.

Dataklassifiseringsforslag lar deg for eksempel gjøre følgende:  

* Bruke veiledningen for dataklassifisering til å eksportere felt til et Excel-regneark der du kan masseklassifisere dem. Bruk av Excel-regnearket er spesielt nyttig hvis du samarbeider med en Microsoft-partnere. Når du har oppdatert regnearket, kan du bruke veiledningen for å importere og ta i bruk klassifiseringene. Du kan også bruke veiledningen for å klassifisere feltene manuelt.  
* Velg et felt, og filtrer deretter listen for å finne lignende felt som sannsynligvis tilhøre samme klassifisering som feltet søket er basert på.  
* Undersøk et felt ved å vise innholdet.  

> [!Tip]
> Vi har definert eksempler på sensitivitetsklassifiseringer for tabellene og feltene i demonstrasjonsselskapet Cronus. Du kan bruke disse klassifiseringer som inspirasjon når du klassifisere dine egne tabeller og felt.

## <a name="see-also"></a>Se også

[Klassifisere data](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]