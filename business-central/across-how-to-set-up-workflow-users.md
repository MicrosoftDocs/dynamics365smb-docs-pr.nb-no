---
title: Konfigurere arbeidsflytbrukere
description: 'Før du kan opprette arbeidsflyter, må du definere brukerne som deltar i dem på siden Brukeroppsett for godkjenning.'
author: brentholtorf
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 05/31/2023
ms.author: bholtorf
---
# <a name="set-up-a-sequence-of-workflow-users"></a>Definer en sekvens med arbeidsflytbrukere

Før du kan opprette godkjenningsarbeidsflyter, må du definere brukerne som skal sende inn forespørsler og godkjennerne. Du kan for eksempel angi hvem som skal varsles om å utføre en handling på et arbeidsflyttrinn. Du setter opp arbeidsflytdeltakere på side **Brukeroppsett for godkjenning**. Finn ut mer under [Definer godkjenningsbrukere](across-how-to-set-up-approval-users.md).

På siden **Brukergrupper for arbeidsflyt** kan du angi hvor en deltaker skal engasjere seg i en godkjenningsarbeidsflyt ved å angi et nummer i feltet **Serienr.** . Du kan for eksempel angi at brukere skal inngå i en sekvensiell rekkefølge, for eksempel en kjede med godkjennere. Du kan også angi en flat liste over godkjennere ved å skrive inn samme nummer. I det siste tilfellet må bare én av godkjennerne godkjenne en forespørsel.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## <a name="to-set-up-a-workflow-user-group"></a>Slik konfigurerer du en arbeidsflytbrukergruppe

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflytbrukergrupper**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Siden **Brukergruppe for arbeidsflyt** åpnes.  
3. I **Kode**-feltet angir du maksimalt 20 tegn for å identifisere arbeidsflyten.  
4. I **Beskrivelse**-feltet beskriver du arbeidsflyten.  
5. Fyll ut feltene på den første linjen som beskrevet i tabellen nedenfor, i hurtigfanen **Medlemmer i brukergrupper for arbeidsflyt**.  

   |Felt|Description|
   |-----|-----------|
   |**Brukernavn**|Angi brukeren som skal inngå i en arbeidsflyt.<br /><br /> Brukeren må finnes på siden **Brukeroppsett**. Finn ut mer under [Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md).|
   |**Sekvensnummer**|Angi rekkefølgen som arbeidsflytbrukeren deltar i en arbeidsflyt i forhold til andre brukere. Dette feltet kan angi for eksempel når brukeren godkjenner i forhold til andre godkjennere ved å konfigurere **Brukergruppe for arbeidsflyt**-alternativet i **Godkjennertype**-feltet på relaterte arbeidsflytsvar.| 

6. Gjenta trinn 5 for å legge til flere arbeidsflytbrukere for arbeidsflytbrukergruppen.  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Konfigurer godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Konfigurer godkjenningsarbeidsflyter](across-set-up-workflows.md)  
[Bruk godkjenningsarbeidsflyter](across-use-workflows.md)  
[Gjennomgang: Definer og bruk en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbeidsflyt](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
