---
title: Bruke arbeidsflyter
description: Du kan opprette og bruke arbeidsflyter som kobler sammen forretningsprosessoppgaver som automatisk bokføring eller forespørsel om å gi godkjenning for nye poster.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: b7e6574567e07b42187d3e33cfbf7f99e13096f8
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077374"
---
# <a name="use-workflows"></a>Bruk arbeidsflyter

En arbeidsflyt er en sekvens av oppgaver som utløses av en handling, en betingelse eller en regel. Arbeidsflyter er vanligvis implementert for å integrere forretningslogikk i en organisasjon, for eksempel separasjon av oppgaver, innsamlingsprosesser eller for å øke tillit og ansvar.  

Arbeidsflytene er utformet for å opprette forespørsler om godkjenning av en ny verdi og beholde den gamle verdien i tilfelle forespørselen ikke godkjennes. Den nye verdien blir ikke implementert før den siste forespørselen er godkjent.  

Forretningslogikken kan være godkjenning av:

- Nye hoveddata som finanskonti, kunder, leverandører eller varer
- Endringer i felt i eksisterende poster med sensitive opplysninger, for eksempel **Leverandørs bankkontonr.** eller **Kundekredittgrense**
- Endringer i felt i eksisterende poster med forretningskritisk informasjon, for eksempel **Varesalgspriser**
- Nye brukere eller endringer i brukertillatelser
- Kjøpsdokumenter
- Salgsdokumenter
- Inngående dokumenter
- Finansjournaler før bokføring

Følgende illustrasjon viser et eksempel på en arbeidsflyt med sekvensiell godkjenning utløst av en bruker. Ved å utløse arbeidsflyten opprettes det en godkjenningsforespørsel for den første godkjenneren.  

![Bilde av en arbeidsflyt med sekvensiell godkjenning.](media/Workflows/approval-flow.png)

I dette eksemplet må forespørselen godkjennes av den første godkjenneren før forespørselen sendes til neste godkjenner. Hvis forespørselen ikke godkjennes av den første godkjenneren, går ikke forespørselen videre til neste godkjenner.  

Ruten som er hentet fra den første utløseren for arbeidsflyten, kan variere avhengig av godkjenningstypen.  

Illustrasjonen nedenfor viser en parallell godkjenning som utløses av brukeren. Ved å utløse arbeidsflyten sendes en forespørsel om godkjenning til alle godkjennerne samtidig.  

![Bilde av en arbeidsflyt med parallell godkjenning.](media/Workflows/approval-flow-2.png)

Arbeidsflyten godkjennes imidlertid ikke før alle forespørsler er godkjent av godkjennerne, som vist i følgende illustrasjon:  

![Bilde av en avvist arbeidsflyt med parallell godkjenning.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Det er ikke mulig å opprette en arbeidsflyt med flere godkjennere og forvente at hele arbeidsflyten godkjennes etter at den første forespørselen er godkjent. Alle forespørsler må godkjennes for at arbeidsflyten skal bli godkjent.

Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Det er også mulig å opprette samme arbeidsflyt mer enn én gang. Hver arbeidsflyt som utløses av en hendelse, bruker forskjellige filtre. Dette er nyttig hvis en godkjenningsforespørsel i én avdeling må godkjennes av én godkjenner, der godkjenningsforespørsler i andre avdelinger må godkjennes av en annen godkjenner. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.  

 Før du kan begynne å bruke arbeidsflyter, må du konfigurere brukere av arbeidsflyt, opprette arbeidsflytene, potensielt med foranstilt tilpasset kode, og angi hvordan brukere mottar varsler. Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidsflyter](across-set-up-workflows.md).  

> [!NOTE]  
> Vanlige arbeidsflyttrinn er om brukere som ber om godkjenning av oppgaver og godkjennere som godkjenner eller avviser forespørsler om godkjenning. Mange emner om hvordan du bruker arbeidsflyter, refererer derfor til godkjenninger.  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.  

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Angi at en arbeidsflyt skal starte når den første innpunkthendelsen oppstår.|[Aktivere arbeidsflyter](across-how-to-enable-workflows.md)|  
|Be om godkjenning for en oppgave, som godkjenner, godkjenn, avvis eller deleger godkjenning, og send eller vis godkjenningsmeldinger.|[Bruke arbeidsflyter for godkjenning](across-how-use-approval-workflows.md)|  
|Opprett trinn i arbeidsflyten som forhindrer at en bestemt oppføringstype brukes før en bestemt hendelse inntreffer, for eksempel at oppføringen er godkjent.|[Begrense og tillate bruk av en post](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|Vise forekomster av arbeidsflyttrinn med statusen Fullført.|[Vise arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md)|  
|Slette en arbeidsflyt du er sikker på ikke lenger vil bli brukt.|[Slette arbeidsflyter](across-how-to-delete-workflows.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Konfigurere arbeidsflyter](across-set-up-workflows.md)  
[Arbeidsflyt](across-workflow.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]