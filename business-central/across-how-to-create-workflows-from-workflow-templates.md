---
title: Opprette arbeidsflyter fra arbeidsflytmaler | Microsoft-dokumentasjon
description: For å spare tid når du oppretter nye arbeidsflyter, kan du opprette arbeidsflyter fra arbeidsflytmaler.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2540632936a502cd1873c7db34733f5dd83db4b9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775850"
---
# <a name="create-workflows-from-workflow-templates"></a>Opprette arbeidsflyter fra arbeidsflytmaler
For å spare tid når du oppretter nye arbeidsflyter, kan du opprette arbeidsflyter fra arbeidsflytmaler.  

 Arbeidsflytmaler er ikke-redigerbare arbeidsflyter som finnes i den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)]. Kodene for arbeidsflytmaler som er lagt inn av Microsoft, har prefikset "MS-".  

 En annen måte å raskt opprette en arbeidsflyt på er å importere en eksisterende arbeidsflyt som du har på en fil utenfor [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Importere og eksportere arbeidsflyter](across-how-to-export-and-import-workflows.md).  

På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene. Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer. Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden. Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Slik oppretter du en arbeidsflyt fra arbeidsflytmaler  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Opprett arbeidsflyt fra mal**. Siden **Arbeidsflytmaler** åpnes.  
3.  Velg en arbeidsflytmal, og velg deretter **OK**.  

     **Arbeidsflyt**-siden åpnes for en ny arbeidsflyt som inneholder all informasjon for den valgte malen. Verdien i **Kode**-feltet utvides med for eksempel "-01" for å angi at dette er den første arbeidsflyten som er opprettet fra arbeidsflytmalen.  
4.  Fortsett med å opprette arbeidsflyten ved å redigere de arbeidsflyttrinnene eller legge til nye trinn. Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Se også  
 [Opprette arbeidsflyter](across-how-to-create-workflows.md)   
 [Importere og eksportere arbeidsflyter](across-how-to-export-and-import-workflows.md)   
 [Vise arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md)   
 [Slette arbeidsflyter](across-how-to-delete-workflows.md)   
 [Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Konfigurere arbeidsflyter](across-set-up-workflows.md)   
 [Bruke arbeidsflyter](across-use-workflows.md)   
 [Arbeidsflyt](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]