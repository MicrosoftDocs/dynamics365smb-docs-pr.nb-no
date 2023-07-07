---
title: Bruk av arbeidsflyter for godkjenning
description: Du kan opprette og bruke arbeidsflyter for å koble sammen forretningsprosessoppgaver som automatisk bokføring eller forespørsel om å gi godkjenning for nye poster.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '1500, 1501, 1503, 1504, 1505'
ms.date: 09/13/2022
ms.author: edupont
---
# <a name="use-approval-workflows"></a>Bruke arbeidsflyter for godkjenning

En arbeidsflyt er en sekvens av oppgaver som utløses av en handling, en betingelse eller en regel. Arbeidsflyter er vanligvis implementert for å integrere forretningslogikk i en organisasjon, for eksempel separasjon av oppgaver, innsamlingsprosesser eller for å bruke anbefalte fremgangsmåter.

Arbeidsflytene kan være utformet for å opprette forespørsler om godkjenning av en postfeltendring og beholde de gamle dataene i tilfelle forespørselen ikke godkjennes. Den nye verdien blir ikke implementert før den siste forespørselen er godkjent.

Forretningslogikken kan være godkjenningen av:

- Nye hoveddata som finanskontoer, kunder, leverandører eller varer.
- Endringer i felter i eksisterende poster med sensitive opplysninger, for eksempel **Leverandørs bankkontonr.** eller **Kundekredittgrense**.
- Endringer i felter i eksisterende poster med forretningskritisk informasjon, for eksempel **Varesalgspriser**.
- Nye brukere eller endringer i brukertillatelser.
- Kjøpsdokumenter.
- Salgsdokumenter.
- Inngående dokumenter.
- Finansjournaler før bokføring.

Følgende illustrasjon er et eksempel på en arbeidsflyt med sekvensiell godkjenning utløst av en bruker. Ved å utløse arbeidsflyten opprettes det en godkjenningsforespørsel for den første godkjenneren.  

![Bilde av en arbeidsflyt med sekvensiell godkjenning.](media/Workflows/approval-flow.png)

Du ser i illustrasjonen ovenfor hvordan forespørselen må godkjennes av den første godkjenneren før den sendes til neste. Hvis forespørselen ikke godkjennes av den første godkjenneren, går ikke forespørselen videre til neste.

Ruten som er hentet fra den første utløseren for arbeidsflyten, kan variere avhengig av godkjenningstypen.  

Illustrasjonen nedenfor viser en parallell godkjenning som utløses av brukeren. En parallell godkjenning betyr at forespørsel om godkjenning sendes til alle godkjennerne samtidig.  

![Bilde av en arbeidsflyt med parallell godkjenning.](media/Workflows/approval-flow-2.png)

Arbeidsflyten er imidlertid ikke fullført før alle forespørsler er godkjent, som vist i følgende illustrasjon:  

![Bilde av en avvist arbeidsflyt med parallell godkjenning.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> For en arbeidsflyt med flere godkjennere må alle godkjennerne godkjenne hvert trinn før arbeidsflyten kan flyttes fremover til neste hendelse. Godkjenning fra bare én godkjenner flytter ikke arbeidsflyten fremover.

Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Det er også mulig å opprette samme arbeidsflyt mer enn én gang. Hver arbeidsflyt kan utløses av en hendelse ved å bruke forskjellige filtre. Dette er nyttig hvis en godkjenningsforespørsel for én avdeling må godkjennes av én godkjenner, mens godkjenningsforespørsler for andre avdelinger må godkjennes av en annen godkjenner. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.  

Før du kan begynne å bruke arbeidsflyter, må du konfigurere brukere av arbeidsflyt, opprette arbeidsflytene (potensielt med kodetilpasning først), og angi hvordan brukere mottar varsler. Finn ut mer under [Definer arbeidsflyter](across-set-up-workflows.md).

> [!NOTE]  
> Vanlige arbeidsflyttrinn omfatter brukere som ber om godkjenning av oppgaver og godkjennere som godkjenner eller avviser forespørsler om godkjenning. Derfor henviser mange emner om hvordan du bruker arbeidsflyter, til godkjenninger.  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til artiklene som beskriver dem.  

| **Hvis du vil** | **Se** |
|--|--|
| Definer en arbeidsflyt skal starte når den første innpunkthendelsen oppstår. | [Aktiver godkjenningsarbeidsflyter](across-how-to-enable-workflows.md) |
| Be om godkjenning for en oppgave, som godkjenner, godkjenn, avvis eller deleger godkjenning, og send eller vis godkjenningsmeldinger. | [Bruk arbeidsflyter for godkjenning](across-how-use-approval-workflows.md) |
| Opprett trinn i arbeidsflyten som forhindrer at en bestemt oppføringstype brukes før en bestemt hendelse inntreffer, for eksempel godkjenning av oppføringen. | [Begrense og tillate bruk av en post](across-how-to-restrict-and-allow-usage-of-a-record.md) |
| Vise forekomster av arbeidsflyttrinn med statusen **Fullført**. | [Vis arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md) |
| Slett en arbeidsflyt som ikke lenger blir brukt. | [Slett godkjenningsarbeidsflyter](across-how-to-delete-workflows.md) |

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Konfigurer godkjenningsarbeidsflyter](across-set-up-workflows.md)  
[Arbeidsflyt](across-workflow.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
