---
title: Konfigurere arbeidsflytbrukere | Microsoft-dokumentasjon
description: "Før du kan opprette arbeidsflyter, må du definere brukerne som deltar i arbeidsflyter. Det er for eksempel nødvendig å angi hvem som skal varsles om å utføre en handling på et arbeidsflyttrinn."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0fe05d44acd7fb163996e8a663adb309d229b203
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-workflow-users"></a>Konfigurere arbeidsflytbrukere
Før du kan opprette arbeidsflyter, må du definere brukerne som deltar i arbeidsflyter. Det er for eksempel nødvendig å angi hvem som skal varsles om å utføre en handling på et arbeidsflyttrinn.  

I vinduet **Brukergruppe for arbeidsflyt** kan du definere brukere under brukergrupper for arbeidsflyt, og du angir brukernes nummer i en prosessekvensen, for eksempel en godkjennerkjede.  

Arbeidsflytbrukere som fungerer som godkjenningsbrukere, både bestillere for godkjenning og godkjennere, må også først defineres i vinduet **Brukeroppsett for godkjenning**. Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
>  Du kan definere at en godkjenningsforespørsel ikke er godkjent før flere godkjennere i en godkjenningsrekke har godkjent den, ved å definere godkjennere i et hierarki. For godkjennertypen **Godkjenner** definerer du godkjennere i vinduet **Brukeroppsett for godkjenning**. For godkjennertype **Brukergruppe for arbeidsflyt** definerer du godkjennere i vinduet **Brukergrupper for arbeidsflyt** og definerer hierarkiet ved å tilordne trinnvise numre til hver enkelt godkjenner i feltet **Sekvensnr.** . Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md) og dette emnet.  
>   
>  Hvis du vil definere at en godkjenningsforespørsel ikke er godkjent før flere like godkjennere har godkjent den, uavhengig av et hierarki, kan du definere en flat arbeidsflyt-brukergruppe. For godkjennertype **Brukergruppe for arbeidsflyt** definerer du godkjennere i vinduet **Brukergrupper for arbeidsflyt** og tilordner samme nummer til hver enkelt godkjenner i **Sekvensnummer**. . Hvis du vil ha mer informasjon, kan du se dette emnet.  

### <a name="to-set-up-a-workflow-user"></a>Slik konfigurerer du en arbeidsflytbrukere  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Brukergrupper for arbeidsflyt**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Vinduet **Brukergruppe for arbeidsflyt** åpnes.  
3. I **Kode**-feltet angir du maksimalt 20 tegn for å identifisere arbeidsflyten.  
4. I **Beskrivelse**-feltet beskriver du arbeidsflyten.  
5. Fyll ut feltene på den første linjen som beskrevet i tabellen nedenfor, i hurtigfanen **Medlemmer i brukergrupper for arbeidsflyt**.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Brukernavn**|Angi brukeren som skal inngå i arbeidsflyter.<br /><br /> Brukeren må finnes i vinduet **Brukeroppsett**. Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).|  
    |**Sekvensnummer**|Angi rekkefølgen som arbeidsflytbrukeren deltar i en arbeidsflyt i forhold til andre brukere. Dette feltet kan for eksempel brukes til å angi når brukeren godkjenner i forhold til andre godkjennere når du bruker **Brukergruppe for arbeidsflyt**-alternativet i **Godkjennertype**-feltet på relaterte arbeidsflytsvar. **Tips!**  For å definere at en godkjenningsforespørsel ikke er godkjent før flere like godkjennere har godkjent den, uavhengig av et hierarki, kan du sette opp en flat brukergruppe for arbeidsflyt ved å tilordne samme sekvensnummeret til de aktuelle godkjennerne.|  
6. Gjenta trinn 5 for å legge til flere arbeidsflytbrukere for brukergruppen.  
7. Gjenta trinn 2 til 6 for å legge til flere brukergrupper for arbeidsflyt.  

## <a name="see-also"></a>Se også  
[Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md)   
[Konfigurere arbeidsflyter](across-set-up-workflows.md)   
[Bruke arbeidsflyter](across-use-workflows.md)   
[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Arbeidsflyt](across-workflow.md)   

