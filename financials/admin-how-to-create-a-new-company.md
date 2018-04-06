---
title: Opprette et nytt selskap | Microsoft-dokumentasjon
description: Bruke RapidStart Services-tabeller og -sider som er opprettet, uten at det finnes data for dem.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8c07b7c4e6b1c82004295a187184a6f3ccb4c7c7
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-new-company"></a>Opprett et nytt selskap.
Hvis du vil bruke RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], oppretter du først et nytt selskap du vil utføre en kundeimplementering for. Når du oppretter et nytt selskap, opprettes standard [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller og -sider, men de inneholder ingen data.

I tillegg kan du bruke bestemte oppsettsdata på selskapet etter at du har initialisert det. Informasjonen leveres i en konfigurasjonspakke, en .rapidstart-fil, som leverer innhold i et komprimert format.  

Eksempelkonfigurasjonspakker, inkludert lands-regionspesifikke filer, er inkludert i demonstrasjonsselskapet CRONUS. Følg disse fremgangsmåtene for å bruke eksempelkonfigurasjonspakken med et nytt selskap.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Bruke eksempelkonfigurasjonspakken BASICCONFIG  
1. Åpne demonstrasjonsselskapet Cronus Norge AS Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).
2. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Konfigurasjonspakker**, og velg deretter den relaterte koblingen.  
3. Velg BASICCONFIG-pakken fra listen, og velg deretter handlingen **Eksporter pakke**.  

Bruk følgende fremgangsmåte til å opprette et nytt selskap, og bruk BASICCONFIG-pakken som en del av prosessen.  

## <a name="to-create-a-new-company"></a>Slik oppretter du et nytt selskap:  
1. Opprett et nytt selskap. Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper i [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).
2. Fra rollesenteret for RapidStart Services-implementereren kan du nå importere konfigurasjonspakken som du eksporterte fra selskapet CRONUS Norge AS.

Når du har opprettet et nytt selskap, blir enkelte tabeller fylt ut automatisk, selv om ingen selskapsmal er brukt. Du kan for eksempel se gjennom standardkoder for bokføring og partitransaksjoner i **Kildekode**-vinduet. Hvis du bruker en lokal versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)], bør du se gjennom denne tabellen og vurdere eventuelle problemer på lokale språk.

## <a name="about-data-tables"></a>Om datatabeller
[!INCLUDE[d365fin](includes/d365fin_md.md)]-datatabeller leveres i to hovedtyper: Hoved- og Oppsett. Når du oppretter en firmakonfigurasjon, kan du bruke disse typene for å skape et fokus for konfigurasjonsstrategien.  

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

I tillegg til oppsettsdatatabeller har [!INCLUDE[d365fin](includes/d365fin_md.md)] også oppsettsdatatabeller med kjerneinformasjon om selskapet og dets forretningsprosesser. Tabellen nedenfor viser noen av dem.  

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

