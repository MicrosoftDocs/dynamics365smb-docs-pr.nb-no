---
title: Konfigurere godkjenningsbrukere | Microsoft-dokumentasjon
description: "Før du kan opprette arbeidsflyter som omfatter godkjenningstrinn, må du definere arbeidsflytbrukerne som er involvert i godkjenningsprosessen. I vinduet Brukeroppsett for godkjenning angir du også beløpsgrenser for bestemte typer forespørsler og definerer stedfortredende godkjennere som godkjenningsforespørsler delegeres til når den opprinnelige godkjenneren er borte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 98dab9ee1d3b6d717d6d7d999785080225592ee3
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-approval-users"></a>Konfigurere godkjenningsbrukere
Før du kan opprette arbeidsflyter som omfatter godkjenningstrinn, må du definere arbeidsflytbrukerne som er involvert i godkjenningsprosessen. I vinduet **Brukeroppsett for godkjenning** angir du også beløpsgrenser for bestemte typer forespørsler og definerer stedfortredende godkjennere som godkjenningsforespørsler delegeres til når den opprinnelige godkjenneren er borte.  

> [!NOTE]  
>  Godkjenningsbrukere, både bestillere for godkjenning og godkjennere, må først defineres som arbeidsflytbrukere i vinduet **Brukergruppe for arbeidsflyt**. Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md).  

 Når du har definert godkjenningsbrukere, kan du bruke installasjonsprogrammet til å opprette arbeidsflytsvar for godkjenningsarbeidsflyter. Hvis du vil ha mer informasjon, kan du se trinn 9 i [Opprette arbeidsflyter](across-how-to-create-workflows.md).  

> [!NOTE]  
>  Du kan definere at en godkjenningsforespørsel ikke er godkjent før flere godkjennere i en godkjenningsrekke har godkjent den, ved å definere godkjennere i et hierarki. For godkjennertypen **Godkjenner** definerer du godkjennere i vinduet **Brukeroppsett for godkjenning**. For godkjennertype **Brukergruppe for arbeidsflyt** definerer du godkjennere i vinduet **Brukergrupper for arbeidsflyt** og definerer hierarkiet ved å tilordne trinnvise numre til hver enkelt godkjenner i feltet **Sekvensnr.** . Hvis du vil ha mer informasjon, kan du se dette emnet og [Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md).  
>   
>  Hvis du vil definere at en godkjenningsforespørsel ikke er godkjent før flere like godkjennere har godkjent den, uavhengig av et hierarki, kan du definere en flat arbeidsflyt-brukergruppe. For godkjennertype **Brukergruppe for arbeidsflyt** definerer du godkjennere i vinduet **Brukergrupper for arbeidsflyt** og tilordner samme nummer til hver enkelt godkjenner i **Sekvensnummer**. . Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Slik konfigurerer du godkjenningsbrukere  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Brukeroppsett for godkjenning**, og velg deretter den relaterte koblingen.  
2. Opprett en ny linje i vinduet **Brukeroppsett for godkjenning**, og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Bruker-ID**|Velg bruker-IDen til brukeren som er involvert i godkjenningsprosessen.|  
    |**Selger/innkjøper - kode**|Angi selger- eller innkjøperkoden som gjelder for brukerne, i feltet **Selger/innkjøper - kode**.<br /><br /> Du fyller vanligvis ut feltet **Selger/innkjøper - kode** hvis selgeren eller innkjøperen som har ansvaret for kunden eller leverandøren, også er personen som må godkjenne den aktuelle salgs- eller kjøpsforespørselen.|  
    |**Godkjenner-ID**|Velg bruker-ID-en til brukeren som må godkjenne forespørsler fra brukeren i **Bruker-ID**-feltet.|  
    |**Godkjenningsgrense salg**|Angi maksimalt salgsbeløp i NOK som brukeren i **Bruker-ID**-feltet kan godkjenne.|  
    |**Ubegrenset salgsgodkjenning**|Angi at brukeren i **Bruker-ID**-feltet kan godkjenne alle salgsforespørsler uavhengig av beløp.<br /><br /> Hvis du merker av her, kan du ikke fylle ut feltet **Godkjenningsgrense salg**.|  
    |**Godkjenningsgrense kjøp**|Angi maksimalt kjøpsbeløp i NOK som brukeren i **Bruker-ID**-feltet kan godkjenne.|  
    |**Ubegrenset kjøpsgodkjenning**|Angi at brukeren i **Bruker-ID**-feltet kan godkjenne alle kjøpsforespørsler uavhengig av beløp.<br /><br /> Hvis du merker av her, kan du ikke fylle ut feltet **Godkjenningsgrense salg**.|  
    |**Godkjenningsgrense forespørsel**|Angi maksimumsbeløpet i NOK som brukeren i **Bruker-ID**-feltet kan godkjenne for forespørsler.<br /><br /> Hvis du vil bruke dette feltet, må du velge alternativet **Godkjennerkjede** i feltet **Godkjennergrensetype** i vinduet **Arbeidsflytsvar**.|  
    |**Ubegrenset forespørselsgodkjenning**|Angi at brukeren i **Bruker-ID**-feltet kan godkjenne alle kjøpstilbud uavhengig av beløp.<br /><br /> Hvis du merker av her, kan du ikke fylle ut feltet **Godkjenningsgrense forespørsel**.|  
    |**Stedfortreder**|Velg bruker-ID-en til brukeren som må godkjenne forespørsler fra brukeren i **Bruker-ID**-feltet, hvis brukeren i **Godkjenner-ID** ikke er tilgjengelig. **Obs!** Stedfortrederen kan enten være brukeren i **Stedfortreder**-feltet, den direkte godkjenneren eller godkjenningsadministratoren, i denne rekkefølgen. Hvis du vil ha mer informasjon, kan du se [Bruke godkjenningsarbeidsflyter](across-how-use-approval-workflows.md).|  
    |**E-post**|Angi e-postadressen for brukeren i **Bruker-ID**-feltet.|  
    |**Godkjenningsansvarlig**|Angi brukeren som har rettigheter til å fjerne blokkeringen av godkjenningsarbeidsflyter, for eksempel ved å delegere godkjenningsforespørsler til nye stedfortredere for godkjenning og slette forfalte godkjenningsforespørsler.|  

    > [!NOTE]  
    >  Virkemåten til **Godkjennergrensetype** gjelder bare for modulene der grensene kan defineres, nemlig salgs- og kjøpsgodkjenninger. Andre typer godkjenning der grensene ikke gjelder, fungerer alltid som beskrevet for alternativet **Direkte godkjenner**.  

3. Hvis du vil teste brukeroppsettet for godkjenning, velger du **Test av brukeroppsett for godkjenning**.  
4. Gjenta trinn 2 og 3 for alle brukerne som du vil definere som godkjenningsbrukere.  

## <a name="see-also"></a>Se også  
[Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md)   
[Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md)   
[Opprette arbeidsflyter](across-how-to-create-workflows.md)   
[Konfigurere arbeidsflyter](across-set-up-workflows.md)   
[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Arbeidsflyt](across-workflow.md)   

