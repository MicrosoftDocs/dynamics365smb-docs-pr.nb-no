---
title: Eksportere og importere arbeidsflyter | Microsoft-dokumentasjon
description: "For å overføre arbeidsflyter til andre [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser, for eksempel for å spare tid når du oppretter nye arbeidsflyter, kan du eksportere og importere arbeidsflyter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8126d3850103819e885d9d131ca3074f1b7cfda1
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-export-and-import-workflows"></a>Importere og eksportere arbeidsflyter
For å overføre arbeidsflyter til andre [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser, for eksempel for å spare tid når du oppretter nye arbeidsflyter, kan du eksportere og importere arbeidsflyter.  

 En annen måte å raskt opprette arbeidsflyter på er å opprette arbeidsflyter fra arbeidsflytmaler. Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md).  

 I **Arbeidsflyt**-vinduet oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene. Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer. Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden. Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Slik eksporterer du en arbeidsflyt  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2.  Velg en arbeidsflyt, og velg deretter **Eksporter til fil**.  
3.  Klikk **Lagre** i vinduet **Eksporter fil**.  
4.  I **Eksport**-vinduet velger du en filplassering, og deretter velger du **Lagre**-knappen.  

## <a name="to-import-a-workflow"></a>Slik importerer du en arbeidsflyt  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Importer fra fil**.  
3.  I **Import**-vinduet velger du XML-filen som inneholder arbeidsflyten, og deretter velger du **Åpne**-knappen.  

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

