---
title: Konfigurere arbeidsflyter | Microsoft-dokumentasjon
description: Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6ff257a13a995b9617bdae9de98830f50e45edee
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879358"
---
# <a name="setting-up-workflows"></a>Konfigurere arbeidsflyter
Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn. Hvis du vil ha mer informasjon, kan du se [Bruke arbeidsflyter](across-use-workflows.md).  

 Før du begynner å bruke arbeidsflyter, må du konfigurere brukere av arbeidsflyt og godkjenning, angi hvordan brukere motta varsler om trinn i arbeidsflyten, og deretter opprette arbeidsflyter, potensielt med foranstilt tilpasset kode.  

 På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene. Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer. Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden.  

 Hvis et forretningsscenario krever en arbeidsflythendelse eller et arbeidsflytsvar som ikke støttes, må en Microsoft-partner implementere dem ved å tilpasse programkoden. Hvis du vil ha mer informasjon, kan du se [Gjennomgang: Implementering av nye arbeidsflythendelser og svar](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) i hjelpen for utviklere og IT-eksperter.

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.  

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Konfigurere arbeidsflytbrukere og brukergrupper.|[Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md)|  
|Konfigurere arbeidsflytbrukere som deltar i godkjenningsarbeidsflyter.|[Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md)|  
|Angi hvordan arbeidsflytbrukere blir varslet om arbeidsflyttrinn, herunder forespørsler om godkjenning.|[Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md)|  
|Angi om brukere blir varslet med e-post eller notat og hvor ofte varslene sendes.|[Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Tilpass innholdet i e-postvarslet ved å endre rapport 1320, E-postvarsling.|[Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)|  
|Definer en SMTP-server for å aktivere e-postkommunikasjon inn og ut av [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Konfigurere e-post](admin-how-setup-email.md)|
|Angi de ulike trinnene i en arbeidsflyt ved å koble arbeidsflythendelser til arbeidsflytsvar.|[Opprette arbeidsflyter](across-how-to-create-workflows.md)|  
|Bruker arbeidsflytmaler til å opprette nye arbeidsflyter.|[Opprette arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md)|  
|Del arbeidsflyter med andre [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser.|[Importere og eksportere arbeidsflyter](across-how-to-export-and-import-workflows.md)|  
|Lær hvordan du konfigurerer en arbeidsflyt for godkjenning av salgsdokumenter ved å følge en ende-til-ende-fremgangsmåte.|[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Legg til støtte for et forretningsscenario som krever nye arbeidsflythendelser eller svar ved å tilpasse programkoden.|[Gjennomgang: Implementering av nye arbeidsflythendelser og svar](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="see-also"></a>Se også  
 [Bruke arbeidsflyter](across-use-workflows.md)   
 [Arbeidsflyt](across-workflow.md)   
 [Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Arbeide med Business Central](ui-work-product.md)
