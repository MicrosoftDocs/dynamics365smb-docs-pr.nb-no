---
title: Dataarkiv-utvidelsen
description: Når du arkiverer data, opprettes en lavkostnads sikkerhetskopi av postene.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 630
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 4070ff5658ad4aa976c181a3df377155080f1e3b
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012080"
---
# <a name="the-data-archive-extension"></a>Dataarkiv-utvidelsen
Over tid vil bedriften samle en vesentlig mengde data, og som administrator kan det være lurt å ha en strategi for arkivering av data. Hvis du har store mengder data, kan du redusere hastigheten, for eksempel at det tar litt lengre tid å generere rapporter, eller til og med låse poster. I tillegg kan store mengder data føre til økte lagringskostnader.

Dataarkiv-utvidelsen inneholder et grunnleggende rammeverk for arkivering og sikkerhetskopiering av data som en del av datokomprimeringen. Når du bruker datokomprimering, konsolideres relaterte poster til én oppføring, og originalene slettes. Hvis du vil ha mer informasjon, kan du se [Komprimer data med datokomprimering](admin-manage-documents.md#compress-data-with-date-compression). Det kan imidlertid være verdi i å beholde dataene, så i stedet for å slette dem, kan du arkivere dem til senere bruk.

## <a name="start-archiving-data"></a>Start arkivering av data
Utvidelsen er forhåndsinstallert og tilgjengelig i **Utvidelsesbehandling**, slik at du ikke trenger å gjøre noe for å komme i gang. Utvidelsen er også tilgjengelig på Microsoft AppSource. 

Dataarkivene vises på siden **Dataarkivliste**. Hvert arkiv kan inneholde data fra flere tabeller og kan inneholde opptil 10 000 poster. Hvis det er mer enn 10 000 poster i en tabell, blir det opprettet et annet arkiv for de neste 10 000 postene, og så videre. Hvis du for eksempel arkiverer 10 100 finansposter, oppretter Business Central et finanspostarkiv for de første 10 000 postene, og deretter et annet arkiv for de resterende 100 postene. 

Når du har arkivert data, kan du utforske dem ved å bruke Microsoft Excel eller som en CSV-fil.

* Hvis du bruker alternativet Excel, vil arbeidsboken inneholde ett regneark for hver dataarkivtabell.
* Hvis du bruker alternativet for CSV, får du en ZIP-fil med én CSV-fil for hver dataarkivtabell.

> [!TIP]
> Alternativene for Excel og CSV gjør det enklere å bruke en annen app eller tjeneste til å flytte dataene til en annen plassering, for eksempel Azure Blob-lagring eller analyseverktøy, for eksempel Microsoft Power BI.

Dataarkiv-utvidelsene brukes av følgende kjørsler for datokomprimering.

|Kjørsler  |
|---------|
|Datokomp. Varebudsjettposter |
|Datokomprim. bankkontopost |
|Datokomprimer kundeposter |
|Datokomprimer aktivaposter |
|Datokomprimer finansposter |
|Datokompr. forsikringspost |
|Datokompr. vedlikehold Finans |
|Datokompr. vedlikehold Finans |
|Datokomprimer ressursposter |
|Datokomprimer mva-poster |
|Datokompr. leverandørposter |
|Datokomprimer lager Poster |
|Datokomp. Budsjettposter |

Hvis du vil starte dataarkivering når du kjører en av kjørslene, kan du aktivere **Arkiver slettede poster**.

## <a name="storage-considerations"></a>Lagringshensyn
De arkiverte dataene lagres i tabellen for **Leietakermedier**. Denne tabellen er ikke inkludert når databasestørrelsen beregnes, i henhold til lisensvilkårene. I stedet telles den som fillagring. Vi anbefaler imidlertid at du eksporterer gamle arkiver til for eksempel en CSV-fil og deretter sletter gamle arkivposter.

## <a name="see-also"></a>Se også
[Behandle lagring ved å slette dokumenter eller komprimere data](admin-manage-documents.md)
