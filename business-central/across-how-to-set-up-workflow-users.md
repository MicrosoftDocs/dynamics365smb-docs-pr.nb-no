---
title: Konfigurere arbeidsflytbrukere
description: Før du kan opprette arbeidsflyter, må du definere brukerne som deltar i dem på siden Arbeidsflytbrukergruppe.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 95730ff31c963695c94a64d36a8f980bddfbb72b
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530949"
---
# <a name="set-up-workflow-users"></a>Konfigurere arbeidsflytbrukere

Før du kan opprette arbeidsflyter, må du definere brukerne som deltar i arbeidsflyter. Det er for eksempel nødvendig å angi hvem som skal varsles om å utføre en handling på et arbeidsflyttrinn.  

På siden **Brukergruppe for arbeidsflyt** kan du definere brukere under brukergrupper for arbeidsflyt, og du angir brukernes nummer i en prosessekvensen, for eksempel en godkjennerkjede.  

Arbeidsflytbrukere som fungerer som godkjenningsbrukere, både bestillere for godkjenning og godkjennere, må også først defineres på siden **Brukeroppsett for godkjenning**. Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Du kan definere at en godkjenningsforespørsel ikke er godkjent før flere godkjennere i en godkjenningsrekke har godkjent den, ved å definere godkjennere i et hierarki. For godkjennertypen **Godkjenner** definerer du godkjennere på siden **Brukeroppsett for godkjenning**. For godkjennertype **Brukergruppe for arbeidsflyt** definerer du godkjennere på siden **Brukergrupper for arbeidsflyt** og definerer hierarkiet ved å tilordne trinnvise numre til hver enkelt godkjenner i feltet **Sekvensnr.** -feltet. Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md) og følgende del.  
>
> Hvis du vil definere at en godkjenningsforespørsel ikke er godkjent før flere like godkjennere har godkjent den, uavhengig av et hierarki, kan du definere en flat arbeidsflyt-brukergruppe. For godkjennertype **Brukergruppe for arbeidsflyt** definerer du godkjennere på siden **Brukergrupper for arbeidsflyt** og tilordner samme nummer til hver enkelt godkjenner i **Sekvensnummer**. -feltet. Hvis du vil ha mer informasjon, kan du se følgende avsnitt:  

## <a name="to-set-up-a-workflow-user"></a>Slik konfigurerer du en arbeidsflytbrukere

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflytbrukergrupper**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Siden **Brukergruppe for arbeidsflyt** åpnes.  
3. I **Kode**-feltet angir du maksimalt 20 tegn for å identifisere arbeidsflyten.  
4. I **Beskrivelse**-feltet beskriver du arbeidsflyten.  
5. Fyll ut feltene på den første linjen som beskrevet i tabellen nedenfor, i hurtigfanen **Medlemmer i brukergrupper for arbeidsflyt**.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Brukernavn**|Angi brukeren som skal inngå i arbeidsflyter.<br /><br /> Brukeren må finnes på siden **Brukeroppsett**. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).|  
    |**Sekvensnummer**|Angi rekkefølgen som arbeidsflytbrukeren deltar i en arbeidsflyt i forhold til andre brukere. Dette feltet kan for eksempel brukes til å angi når brukeren godkjenner i forhold til andre godkjennere når du bruker **Brukergruppe for arbeidsflyt**-alternativet i **Godkjennertype**-feltet på relaterte arbeidsflytsvar.<br /><br /> **Tips!** For å definere at en godkjenningsforespørsel som krever at flere like brukere har godkjent den, uavhengig av et hierarki, kan du sette opp en flat brukergruppe for arbeidsflyt ved å tilordne samme sekvensnummeret til de aktuelle godkjennerne.|  
6. Gjenta trinn 5 for å legge til flere arbeidsflytbrukere for brukergruppen.  
7. Gjenta trinn 2 til 6 for å legge til flere brukergrupper for arbeidsflyt.  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Konfigurer godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Konfigurere arbeidsflyter](across-set-up-workflows.md)  
[Bruke arbeidsflyter](across-use-workflows.md)  
[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbeidsflyt](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
