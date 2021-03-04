---
title: Eksportere og importere arbeidsflyter | Microsoft-dokumentasjon
description: For å overføre arbeidsflyter til andre Business Central-databaser, for eksempel for å spare tid når du oppretter nye arbeidsflyter, kan du eksportere og importere arbeidsflyter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4d11bc57066c0124bcb004894ed6b2c9dc4b812e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754770"
---
# <a name="export-and-import-workflows"></a>Importere og eksportere arbeidsflyter
For å overføre arbeidsflyter til andre [!INCLUDE[prod_short](includes/prod_short.md)]-databaser, for eksempel for å spare tid når du oppretter nye arbeidsflyter, kan du eksportere og importere arbeidsflyter.  

 En annen måte å raskt opprette arbeidsflyter på er å opprette arbeidsflyter fra arbeidsflytmaler. Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md).  

 På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene. Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer. Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden. Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Slik eksporterer du en arbeidsflyt  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2.  Velg en arbeidsflyt, og velg deretter **Eksporter til fil**.  
3.  Velg **Lagre** på siden **Eksporter fil**.  
4.  På **Eksport**-siden velger du en filplassering, og deretter velger du **Lagre**-knappen.  

## <a name="to-import-a-workflow"></a>Slik importerer du en arbeidsflyt  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Importer fra fil**.  
3.  På **Import**-siden velger du XML-filen som inneholder arbeidsflyten, og deretter velger du **Åpne**-knappen.  

> [!CAUTION]  
>  Hvis arbeidsflytkoden allerede finnes i databasen, overskrives arbeidsflyttrinnene med trinnene i den importerte arbeidsflyten.  

## <a name="see-also"></a>Se også  
 [Opprette arbeidsflyter](across-how-to-create-workflows.md)   
 [Opprette arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md)   
 [Vise arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md)   
 [Slette arbeidsflyter](across-how-to-delete-workflows.md)   
 [Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Konfigurere arbeidsflyter](across-set-up-workflows.md)   
 [Bruke arbeidsflyter](across-use-workflows.md)   
 [Arbeidsflyt](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]