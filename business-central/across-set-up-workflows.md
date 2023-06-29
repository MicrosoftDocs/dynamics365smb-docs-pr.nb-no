---
title: Konfigurer godkjenningsarbeidsflyter (inneholder video)
description: 'Definer arbeidsflyter, arbeidsflytbrukere og godkjenningsbrukere for å koble sammen systemoppgaver for forretningsprosesser som utføres av disse forskjellige brukerne.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: edupont
---
# <a name="set-up-approval-workflows"></a><a name="set-up-approval-workflows"></a>Konfigurere arbeidsflyter for godkjenning

Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn. Finn ut mer under [Bruk godkjenningsarbeidsflyter](across-use-workflows.md).

Før du begynner å bruke godkjenningsarbeidsflyter, må du konfigurere brukere av arbeidsflyt og godkjenning, angi hvordan brukere motta varsler om trinn i arbeidsflyten, og deretter opprette arbeidsflyter.

På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene. Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer. Du definerer arbeidsflyttrinn ved å fylle ut felter på arbeidsflytlinjer ved å bruke faste lister over verdier for hendelse og svar som representerer scenarioer som støttes av programkoden.

[!INCLUDE[workflow](includes/workflow.md)]

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til artiklene som beskriver dem.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Konfigurere arbeidsflytbrukere og brukergrupper.|[Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md)|  
|Konfigurere arbeidsflytbrukere som deltar i godkjenningsarbeidsflyter.|[Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md)|  
|Angi hvordan arbeidsflytbrukere blir varslet om arbeidsflyttrinn, herunder forespørsler om godkjenning.|[Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md)|  
|Angi om brukere blir varslet med e-post eller notat og hvor ofte varslene sendes.|[Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Tilpass innholdet i e-postvarslet ved å endre rapport 1320, E-postvarsling.|[Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)|  
|Definer en SMTP-server for å aktivere e-postkommunikasjon inn og ut av [!INCLUDE[prod_short](includes/prod_short.md)].|[Konfigurere e-post](admin-how-setup-email.md)|
|Angi de ulike trinnene i en arbeidsflyt ved å koble arbeidsflythendelser til arbeidsflytsvar.|[Opprett godkjenningsarbeidsflyter](across-how-to-create-workflows.md)|  
|Bruker arbeidsflytmaler til å opprette nye arbeidsflyter.|[Opprett godkjenningsarbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md)|  
|Del arbeidsflyter med andre [!INCLUDE[prod_short](includes/prod_short.md)]-databaser.|[Importer og eksporter godkjenningsarbeidsflyter](across-how-to-export-and-import-workflows.md)|  
|Lær hvordan du konfigurerer en arbeidsflyt for godkjenning av salgsdokumenter ved å følge en ende-til-ende-fremgangsmåte.|[Gjennomgang: Definer og bruk en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow"></a><a name="example-of-an-approval-workflow"></a>Eksempel på en godkjenningsarbeidsflyt

Denne videoen viser hvordan du konfigurerer en arbeidsflyt som krever at en bruker ber om en annens godkjenning før de kan endre informasjon om en eksisterende kunde eller opprette en ny kunde.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/create-workflows/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Bruk godkjenningsarbeidsflyter](across-use-workflows.md)  
[Arbeidsflyt](across-workflow.md)  
[Gjennomgang: Definer og bruk en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbeid med Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
