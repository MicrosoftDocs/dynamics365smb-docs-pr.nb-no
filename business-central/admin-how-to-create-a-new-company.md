---
title: Opprett et nytt selskap med konfigurasjonspakker
description: Bruk RapidStart Services-tabeller og -sider til å opprette et nytt selskap som du vil utføre en kundeimplementering for.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 2d75c136fdd0dcf2891468d722008ab0bf183cbb
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512415"
---
# <a name="create-a-new-company-based-on-configuration-packages"></a>Opprett et nytt selskap basert på konfigurasjonspakker

Hvis du vil bruke RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], oppretter du først et nytt selskap du vil utføre en kundeimplementering for. Når du oppretter et nytt selskap, opprettes standard [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller og -sider, men de inneholder ingen data.

I tillegg kan du bruke bestemte oppsettsdata på selskapet etter at du har initialisert det. Informasjonen leveres i en konfigurasjonspakke, en .rapidstart-fil, som leverer innhold i et komprimert format.  

Eksempelkonfigurasjonspakker, inkludert lands-regionspesifikke filer, er inkludert i demoselskapet CRONUS. Følg disse fremgangsmåtene for å bruke eksempelkonfigurasjonspakken med et nytt selskap.  

## <a name="to-use-the-sample-configuration-packages"></a>Bruk eksempelkonfigurasjonspakkene

1. Åpne CRONUS-demoselskapet. Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).  
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konfigurasjonspakker**, og velg deretter den relaterte koblingen.  
3. Velg den relevante pakken fra listen, og velg deretter handlingen **Eksporter pakke**.  

Bruk følgende fremgangsmåte til å opprette et nytt selskap, og bruk konfigurasjonspakken som en del av prosessen.  

## <a name="to-create-a-new-company"></a>Slik oppretter du et nytt selskap:

1. Opprett et nytt selskap. Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konfigurasjonspakker**, og velg deretter den relaterte koblingen.  
3. Velg handlingen **Importer pakke**, og angi .rapidstart-filen du vil importere.  

Når du har opprettet et nytt selskap, blir enkelte tabeller fylt ut automatisk, selv om ingen selskapsmal er brukt. Du kan for eksempel se gjennom standardkoder for bokføring og partitransaksjoner på **Kildekode**-siden. Hvis du bruker en lokal versjon av [!INCLUDE[prod_short](includes/prod_short.md)], bør du se gjennom denne tabellen og vurdere eventuelle problemer på lokale språk.

## <a name="about-data-tables"></a>Om datatabeller

[!INCLUDE[prod_short](includes/prod_short.md)]-datatabeller leveres i to hovedtyper: Hoved- og Oppsett. Når du oppretter en firmakonfigurasjon, kan du bruke disse typene for å skape et fokus for konfigurasjonsstrategien.  

### <a name="master-data-tables"></a>Hoveddatatabeller

Tabellen nedenfor viser noen av hoveddatatabellene. Når du initialiserer et nytt selskap, er disse tabellene tomme.  

|Tabellnr.|Tabellnavn|  
|-------------------|--------------------|  
|15|Finanskonto|  
|18|Kunde|  
|23|Leverandør|  
|27|Element|  
|5050|Kontakt|  

### <a name="setup-data-tables"></a>Oppsettsdatatabeller

Tabellen nedenfor viser noen av oppsettsdatatabellene, der du henter oppsettsinformasjon i konfigurasjonsspørreskjemaet. Disse tabellene inneholder grunnlagsinformasjon når selskapet opprettes.  

|Tabellnr.|Tabellnavn|  
|-------------------|--------------------|  
|98|Finansoppsett|  
|311|Salgsoppsett|  
|312|Kjøpsoppsett|  
|313|Lageroppsett|  

I tillegg til oppsettsdatatabeller har [!INCLUDE[prod_short](includes/prod_short.md)] også oppsettsdatatabeller med kjerneinformasjon om selskapet og dets forretningsprosesser. Tabellen nedenfor viser noen av dem.  

|Tabellnr.|Tabellnavn|  
|-------------------|--------------------|  
|3|Betalingsbetingelser|  
|4|Valuta|  
|6|Kundeprisgrupper|  
|5700|Lagerføringsenhet|

## <a name="see-also"></a>Se også

[Bruke konfigurasjoner for nye selskaper](admin-apply-configuration-to-new-companies.md)  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]