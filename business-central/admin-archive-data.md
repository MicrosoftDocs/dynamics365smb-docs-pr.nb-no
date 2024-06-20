---
title: Dataarkiv-utvidelsen
description: 'Når du arkiverer data, opprettes en lavkostnads sikkerhetskopi av postene.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 01/30/2023
ms.custom: bap-template
ms.search.form: 630
ms.service: dynamics-365-business-central
---

# <a name="the-data-archive-extension"></a>Dataarkiv-utvidelsen

Over tid vil bedriften samle en vesentlig mengde data, og som administrator kan det være lurt å ha en strategi for arkivering av data. Hvis du har store mengder data, kan du redusere hastigheten, for eksempel at det tar litt lengre tid å generere rapporter, eller til og med låse poster. I tillegg kan store mengder data føre til økte lagringskostnader.

Dataarkiv-utvidelsen inneholder et grunnleggende rammeverk for arkivering og sikkerhetskopiering av data som en del av datokomprimeringen. Datokomprimering konsoliderer relaterte poster til én post og sletter originalene. Finn ut mer under [Komprimer data med datokomprimering](admin-manage-documents.md#compress-data-with-date-compression). Det kan imidlertid være verdi i å beholde dataene, så i stedet for å slette dem, kan du arkivere dem til senere bruk.

## <a name="start-archiving-data"></a>Start arkivering av data

Utvidelsen er forhåndsinstallert og tilgjengelig i **Utvidelsesbehandling**, slik at du ikke trenger å gjøre noe for å komme i gang. Utvidelsen er også tilgjengelig på AppSource.

Dataarkivene vises på siden **Dataarkivliste**. Hvert arkiv kan inneholde data fra flere tabeller og kan inneholde opptil 10 000 poster. Hvis det er mer enn 10 000 poster i en tabell, blir det opprettet et annet arkiv for de neste 10 000 postene, og så videre. Hvis du for eksempel arkiverer 10 100 finansposter, oppretter Business Central et finanspostarkiv for de første 10 000 postene, og deretter et annet arkiv for de resterende 100 postene.

Når du har arkivert data, kan du utforske dem ved å bruke Microsoft Excel eller som en CSV-fil.

* Hvis du bruker alternativet Excel, vil arbeidsboken inneholde ett regneark for hver dataarkivtabell.
* Hvis du bruker alternativet for CSV, får du en ZIP-fil som inneholder én CSV-fil for hver dataarkivtabell.

> [!TIP]
> Alternativene for Excel og CSV gjør det enklere å bruke en annen app eller tjeneste til å flytte dataene til en annen plassering, for eksempel Azure Blob-lagring eller et analyseverktøy, for eksempel Microsoft Power BI.

Dataarkiv-utvidelsen brukes av følgende kjørsler for datokomprimering.

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

De arkiverte dataene lagres i tabellen for **Leietakermedier**. Vi anbefaler at du eksporterer gamle arkiver til for eksempel en CSV-fil og deretter sletter gamle arkivposter.

## <a name="see-also"></a>Se også

[Behandle lagring ved å slette dokumenter eller komprimere data](admin-manage-documents.md)
