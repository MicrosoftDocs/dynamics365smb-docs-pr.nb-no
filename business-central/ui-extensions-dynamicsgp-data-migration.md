---
title: Overføre data fra Dynamics GP med utvidelsen for datamigrering | Microsoft-dokumentasjon
description: Bruk utvidelsen Dynamics GP-datamigrering til å overføre kunder, leverandører, lagervarer, finanskonti og åpne transaksjoner med skyldige beløp og tilgodehavender fra Dynamics GP til Business Central.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 01/16/2020
ms.author: edupont
ms.openlocfilehash: b05959eea09289db7878145347362786ab336de8
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992148"
---
# <a name="the-dynamics-gp-data-migration-extension"></a>Utvidelsen for Dynamics GP datamigrering 
Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, lagervarer, finanskonti og åpne transaksjoner med skyldige beløp og tilgodehavender fra Dynamics GP til [!INCLUDE[prodshort](includes/prodshort.md)]. Hvis virksomheten din bruker Dynamics GP i dag, kan du eksportere relevante poster og deretter åpne en assistert oppsettsveiledning for å legge til data i [!INCLUDE[prodshort](includes/prodshort.md)]. Overføringsutvidelsen fungerer for alle støttede versjoner av Microsoft Dynamics GP. Hvis du vil ha mer informasjon, kan du se [Imporere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md).

> [!NOTE]
>  Denne utvidelsen vil bli avskrevet i 15.3-oppdateringen. Vi anbefaler at brukere som vil overføre fra Dynamics GP, begynner å bruke veiviseren for **skyoverføring** i stedet. Utvidelsen for **skyoverføring** har mer robust funksjonalitet og henter flere data til Business Central fra Dynamics GP.

## <a name="exporting-data-from-dynamics-gp"></a>Eksportere data fra Dynamics GP
Du må ha eksportert noen av eller alle dine eksisterende kunder, leverandører, varer og finanskontoer til en fil ved hjelp av funksjonen for dataeksport i Dynamics GP. Når du velger å eksportere data, kan du velge følgende typer:

* Konto  
* Kunde  
* Element  
* Leverandør  

Når eksportertfilen er opprettet, får du en zip-fil som inneholder flere txt-filer som bestemmes av hva du valgte under eksporten av dataene.  Det vil også være flere txt-filer som genereres som inneholder støtteinformasjon som er nødvendig for oppsett i det nye [!INCLUDE[prodshort](includes/prodshort.md)]-selskapet.

Utvidelsen Dynamics GP-datamigrering automatisk tilordner de eksporterte dataene, slik at dataene er raskt tilgjengelige for deg i det nye selskapet i [!INCLUDE[prodshort](includes/prodshort.md)].

## <a name="whats-new-in-the-october-2018-release"></a>Hva er nytt i oktober 2018-utgivelsen

I denne versjonen har vi utvidet datamengden vi henter til [!INCLUDE[prodshort](includes/prodshort.md)] fra Dynamics GP.

I veiviseren for flytting, kan du nå velge hvordan du ønsker å overføre Dynamics GP-kontoplanen. Du kan overføre den eksisterende kontoplanen, eller du kan opprette en ny kontoplan basert på en eksisterende kontoplan.  

Hvis du vil bruke en eksisterende kontoplan, settes kontiene opp som hovedkontosegmentet fra Dynamics GP, og de ekstra segmentene defineres som dimensjoner i [!INCLUDE[prodshort](includes/prodshort.md)].  

Hvis du vil opprette en ny kontoplan, får du en ekstra kontoside i veiviseren, slik at du kan laste ned arbeidsboken, foreta de aktuelle endringene, og deretter importere arbeidsboken på nytt for å endre kontiene.  

Du må laste ned Excel-arbeidsboken og tilordne et nytt kontonummer for hvert kontonummer i Excel-regnearket. Hver konto må ha et eget nummer, ellers vil overføringen mislykkes. Når du har fullført tilordningen, kan du fortsette gjennom veiviseren for flytting ved å importere Excel-arbeidsboken som du nettopp har oppdatert. Veiviseren validerer at hver rad har et unikt kontonummer, og at ingen rader inneholder et tomt nytt kontonummeret.  

Med endringer i tilknytning til diagrammet med kontoalternativer vil du også se en endring av typen data som kommer inn i finanskladden for kontonumrene.  

- Hvis du vil bruke de eksisterende kontonumrene, vil vi overføre startsaldoen for hovedsegmentet (det nye kontonummeret) som et sammendrag av hovedkontonummeret på tidspunktet for overføringen.  
- Hvis du vil opprette nye kontonumre, vil vi overføre informasjonsoversikt for tilsvarende to regnskapsår basert på regnskapsperiodene du har definert i Dynamics GP.

I tidligere versjoner av [!INCLUDE[prodshort](includes/prodshort.md)] overførte veiviseren en sammendragstransaksjon for kunde-/everandørsaldoen i Dynamics GP. Nå overfører vi de detaljerte åpne transaksjonene for kunder og leverandører på tidspunktet for overføringen. Hva betyr dette? Hvis kunden har 3 utestående transaksjoner som er registrert i modulen Salg, gir veiviseren disse transaksjonene til [!INCLUDE[prodshort](includes/prodshort.md)] sammen med det utestående beløpet som dokumentbeløpet. Dette er det samme for Kjøp-modulen for leverandører.  

Lagervarer importeres med kostverdisettingsmetoden som ble valgt da selskapets oppsettsveiviser ble kjørt. Servicevarer tilordnes automatisk FIFO-verdisettingsmetoden. For øyeblikket overfører vi beholdningen for varene på overføringstidspunktet.  Dette antallet hentes inn i den tomme lokasjonen.  

Det siste alternativet i veiviseren for overføring av data for Dynamics GP, er muligheten til å angi et bokføringsalternativ. Denne innstillingen angir om du vil bokføre alle transaksjoner i finanskladdene automatisk så snart overføringen flytter dataene til [!INCLUDE[prodshort](includes/prodshort.md)], eller om du vil bokføre manuelt, slik at alle transaksjoner er plassert i kladder på Finanskladd-siden, slik at du kan verifisere informasjonen før du bokfører. Dette alternativet vises på siden med alternativer for Kontoplan.


## <a name="see-also"></a>Se også
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tilpasse [!INCLUDE[prodshort](includes/prodshort.md)] ved hjelp av utvidelser](ui-extensions.md)  
