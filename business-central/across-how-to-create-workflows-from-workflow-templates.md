---
title: Opprette arbeidsflyter fra arbeidsflytmaler
description: 'Hvis du vil spare tid når du oppretter nye godkjenningsarbeidsflyter, kan du opprette ikke-redigerbare arbeidsflyter fra arbeidsflytmalen som inneholder MS.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: edupont
---
# <a name="create-workflows-from-workflow-templates"></a>Opprette arbeidsflyter fra arbeidsflytmaler

For å spare tid når du oppretter nye godkjenningsarbeidsflyter, kan du bruke arbeidsflytmaler.  

Arbeidsflytmaler er ikke-redigerbare arbeidsflyter som finnes i standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)]. Kodene for arbeidsflytmaler opprettet av Microsoft har prefikset MS-.  

En annen måte å raskt opprette en arbeidsflyt på er å importere en eksisterende arbeidsflyt som du har på en fil utenfor [!INCLUDE[prod_short](includes/prod_short.md)]. Finn ut mer under [Eksporter og importer arbeidsflyter](across-how-to-export-and-import-workflows.md).  

På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene. Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer. Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden. Finn ut mer under [Opprett arbeidsflyter](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template"></a>Slik oppretter du en arbeidsflyt fra arbeidsflytmaler

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny arbeidsflyt fra mal**. Siden **Arbeidsflytmaler** åpnes.  
3. Velg en arbeidsflytmal, og velg deretter **OK**.  

   **Arbeidsflyt**-siden åpnes for en ny arbeidsflyt som inneholder all informasjon for den valgte malen. Verdien i **Kode**-feltet utvides med for eksempel "-01" for å angi at dette er den første arbeidsflyten opprettet fra arbeidsflytmalen.  
4. Fortsett med å opprette arbeidsflyten ved å redigere de arbeidsflyttrinnene eller legge til nye trinn. Finn ut mer under [Opprett arbeidsflyter](across-how-to-create-workflows.md).  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Opprett godkjenningsarbeidsflyter](across-how-to-create-workflows.md)  
[Importer og eksporter godkjenningsarbeidsflyter](across-how-to-export-and-import-workflows.md)  
[Vis arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md)  
[Slett godkjenningsarbeidsflyter](across-how-to-delete-workflows.md)  
[Gjennomgang: Definer og bruk en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurer godkjenningsarbeidsflyter](across-set-up-workflows.md)  
[Bruk godkjenningsarbeidsflyter](across-use-workflows.md)  
[Arbeidsflyt](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
