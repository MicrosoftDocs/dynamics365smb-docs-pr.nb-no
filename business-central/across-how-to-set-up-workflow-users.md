---
title: Konfigurere arbeidsflytbrukere
description: 'Før du kan opprette arbeidsflyter, må du definere brukerne som deltar i dem på siden Brukeroppsett for godkjenning.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 04/04/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Definer en sekvens med arbeidsflytbrukere

Før du kan opprette godkjenningsarbeidsflyter, må du definere brukerne som kan sende inn forespørsler og godkjennerne. Du kan for eksempel angi hvem som varsles om å utføre en handling på et arbeidsflyttrinn. Du setter opp arbeidsflytdeltakere på side **Brukeroppsett for godkjenning**. Finn ut mer under [Definer godkjenningsbrukere](across-how-to-set-up-approval-users.md).

På siden **Brukergrupper for arbeidsflyt** kan du angi hvor en deltaker skal engasjere seg i en godkjenningsarbeidsflyt ved å angi et nummer i feltet **Serienr.** . Du kan for eksempel angi at brukere skal inngå i en sekvensiell rekkefølge, for eksempel en kjede med godkjennere. Du kan også angi en flat liste over godkjennere ved å skrive inn samme nummer. I det siste tilfellet må bare én av godkjennerne godkjenne en forespørsel.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## Slik konfigurerer du en arbeidsflytbrukergruppe

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflytbrukergrupper**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Siden **Brukergruppe for arbeidsflyt** åpnes.  
3. I **Kode**-feltet angir du maksimalt 20 tegn for å identifisere arbeidsflyten.  
4. I **Beskrivelse**-feltet beskriver du arbeidsflyten.  
5. Fyll ut feltene på den første linjen som beskrevet i tabellen nedenfor, i hurtigfanen **Medlemmer i brukergrupper for arbeidsflyt**.  

   |Felt|Description|
   |-----|-----------|
   |**Brukernavn**|Angi brukeren som inngår i en arbeidsflyt.<br /><br /> Brukeren må finnes på siden **Brukeroppsett**. Finn ut mer under [Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md).|
   |**Sekvensnummer**|Angi rekkefølgen som arbeidsflytbrukeren deltar i en arbeidsflyt i forhold til andre brukere. Dette feltet kan angi for eksempel når brukeren godkjenner i forhold til andre godkjennere ved å konfigurere **Brukergruppe for arbeidsflyt**-alternativet i **Godkjennertype**-feltet på relaterte arbeidsflytsvar.|

   > [!NOTE]
   > Sekvensnumre er vanligvis sekvensielle for brukere i en arbeidsflytbrukergruppe. Flere brukere kan imidlertid ha samme sekvensnummer. Når det er tilfelle, må bare én av brukerne godkjenne en forespørsel før arbeidsflyten går til neste trinn. Hvis for eksempel bruker A og bruker B begge er nummer to i sekvensen, går arbeidsflyten til trinn tre når enten bruker A eller bruker B godkjenner forespørselen.
6. Gjenta trinn 5 for å legge til flere arbeidsflytbrukere for arbeidsflytbrukergruppen.  

## Se også

[Konfigurer godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Konfigurer godkjenningsarbeidsflyter](across-set-up-workflows.md)  
[Bruk godkjenningsarbeidsflyter](across-use-workflows.md)  
[Gjennomgang: Definer og bruk en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbeidsflyt](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
