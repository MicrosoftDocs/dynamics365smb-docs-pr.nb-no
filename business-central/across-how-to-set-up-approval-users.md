---
title: Konfigurere godkjenningsbrukere
description: Før du kan opprette arbeidsflyter som omfatter godkjenningstrinn, må du definere arbeidsflytbrukerne som er involvert i godkjenningsprosessen. På siden Brukeroppsett for godkjenning angir du også beløpsgrenser for bestemte typer forespørsler og definerer stedfortredende godkjennere som godkjenningsforespørsler delegeres til når den opprinnelige godkjenneren er borte.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5eaa2daf8321adf65275bf4e0cd21ee1f4cb29fa
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787260"
---
# <a name="set-up-approval-users"></a>Konfigurere godkjenningsbrukere

Før du kan opprette arbeidsflyter som omfatter godkjenningstrinn, må du definere arbeidsflytbrukerne som er involvert i godkjenningsprosessen. På siden **Brukeroppsett for godkjenning** angir du også beløpsgrenser for bestemte typer forespørsler og definerer stedfortredende godkjennere som godkjenningsforespørsler delegeres til når den opprinnelige godkjenneren er borte.  

> [!NOTE]  
> Godkjenningsbrukere, både bestillere for godkjenning og godkjennere, må først defineres som arbeidsflytbrukere på siden **Brukergruppe for arbeidsflyt**. Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md).  

 Når du har definert godkjenningsbrukere, kan du bruke installasjonsprogrammet til å opprette arbeidsflytsvar for godkjenningsarbeidsflyter. Hvis du vil ha mer informasjon, kan du se trinn 9 i [Opprette arbeidsflyter](across-how-to-create-workflows.md).  

> [!NOTE]  
> Du kan definere at en godkjenningsforespørsel ikke er godkjent før flere godkjennere i en godkjenningsrekke har godkjent den, ved å definere godkjennere i et hierarki. For godkjennertypen **Godkjenner** definerer du godkjennere på siden **Brukeroppsett for godkjenning**. For godkjennertype **Brukergruppe for arbeidsflyt** definerer du godkjennere på siden **Brukergrupper for arbeidsflyt** og definerer hierarkiet ved å tilordne trinnvise numre til hver enkelt godkjenner i feltet **Sekvensnr.** . Hvis du vil ha mer informasjon, kan du se dette emnet og [Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md).  

## <a name="to-set-up-an-approval-user"></a>Slik konfigurerer du godkjenningsbrukere

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukeroppsett for godkjenning**, og velg deretter den relaterte koblingen.  
2. Opprett en ny linje på siden **Brukeroppsett for godkjenning**, og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Bruker-ID**|Velg bruker-IDen til brukeren som er involvert i godkjenningsprosessen.|  
    |**Selger/innkjøper - kode**|Angi selger- eller innkjøperkoden som gjelder for brukerne, i feltet **Selger/innkjøper - kode**.<br /><br /> Du fyller vanligvis ut feltet **Selger/innkjøper - kode** hvis selgeren eller innkjøperen som har ansvaret for kunden eller leverandøren, også er personen som må godkjenne den aktuelle salgs- eller kjøpsforespørselen.|  
    |**Godkjenner-ID**|Velg bruker-ID-en til brukeren som må godkjenne forespørsler fra brukeren i **Bruker-ID**-feltet.|  
    |**Godkjenningsgrense salg**|Angi maksimalt salgsbeløp i NOK som brukeren i **Bruker-ID**-feltet kan godkjenne.|  
    |**Ubegrenset salgsgodkjenning**|Angi at brukeren i **Bruker-ID**-feltet kan godkjenne alle salgsforespørsler uavhengig av beløp.<br /><br /> Hvis du merker av her, kan du ikke fylle ut feltet **Godkjenningsgrense salg**.|  
    |**Godkjenningsgrense kjøp**|Angi maksimalt kjøpsbeløp i NOK som brukeren i **Bruker-ID**-feltet kan godkjenne.|  
    |**Ubegrenset kjøpsgodkjenning**|Angi at brukeren i **Bruker-ID**-feltet kan godkjenne alle kjøpsforespørsler uavhengig av beløp.<br /><br /> Hvis du merker av her, kan du ikke fylle ut feltet **Godkjenningsgrense salg**.|  
    |**Godkjenningsgrense forespørsel**|Angi maksimumsbeløpet i NOK som brukeren i **Bruker-ID**-feltet kan godkjenne for forespørsler.<br /><br /> Hvis du vil bruke dette feltet, må du velge alternativet **Godkjennerkjede** i feltet **Godkjennergrensetype** på siden **Arbeidsflytsvar**.|  
    |**Ubegrenset forespørselsgodkjenning**|Angi at brukeren i **Bruker-ID**-feltet kan godkjenne alle kjøpstilbud uavhengig av beløp.<br /><br /> Hvis du merker av her, kan du ikke fylle ut feltet **Godkjenningsgrense forespørsel**.|  
    |**Stedfortreder**|Velg bruker-ID-en til brukeren som må godkjenne forespørsler fra brukeren i **Bruker-ID**-feltet, hvis brukeren i **Godkjenner-ID** ikke er tilgjengelig. <br /><br />**Obs!** Stedfortrederen kan enten være brukeren i **Stedfortreder**-feltet, den direkte godkjenneren eller godkjenningsadministratoren, i denne rekkefølgen. Hvis du vil ha mer informasjon, kan du se [Bruke godkjenningsarbeidsflyter](across-how-use-approval-workflows.md).|  
    |**E-post**|Angi e-postadressen for brukeren i **Bruker-ID**-feltet.|  
    |**Godkjenningsansvarlig**|Angi brukeren som har rettigheter til å fjerne blokkeringen av godkjenningsarbeidsflyter, for eksempel ved å delegere godkjenningsforespørsler til nye stedfortredere for godkjenning og slette forfalte godkjenningsforespørsler.|

    > [!Note]
    > Det er bare én person som kan være godkjenningsansvarlig.

3. Hvis du vil teste brukeroppsettet for godkjenning, velger du **Test av brukeroppsett for godkjenning**.  
4. Gjenta trinn 2 og 3 for alle brukerne som du vil definere som godkjenningsbrukere.  

## <a name="see-also"></a>Se også

[Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md)   
[Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md)   
[Opprette arbeidsflyter](across-how-to-create-workflows.md)   
[Konfigurere arbeidsflyter](across-set-up-workflows.md)   
[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Arbeidsflyt](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]