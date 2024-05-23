---
title: Opprett arbeidsflyter fra arbeidsflytmaler
description: 'For å spare tid når du oppretter nye arbeidsflytprosesser for godkjenning, kan du opprette arbeidsflytprosesser fra arbeidsflytmaler.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Opprett arbeidsflyt fra arbeidsflytmaler

På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å opprette en serie med arbeidsflyttrinn på linjene. Hvert trinn består av en arbeidsflythendelse (når hendelse), endret av hendelsesbetingelsene (ved betingelse), og et arbeidsflytsvar (så svar), endret av svaralternativer. Feltene på arbeidsflytlinjer gir faste lister av verdier for hendelse og svar som representerer scenarioene som [!INCLUDE [prod_short](includes/prod_short.md)] støtter. Finn ut mer under [Opprett arbeidsflyter](across-how-to-create-workflows.md).

For å spare deg tid når du oppretter arbeidsflyter for godkjenning, tilbyr [!INCLUDE [prod_short](includes/prod_short.md)] arbeidsflytmaler. Malene er tilgjengelige på siden **Arbeidsflytmaler**. Du kan bruke malene som de er, eller tilpasse dem etter dine behov. Kodene for arbeidsflytmalene fra Microsoft har prefikset **MS-**.

[!INCLUDE [workflow-next-step](includes/workflow-next-step.md)]

Hvis du endrer en arbeidsflytmal, men senere angrer på endringen, bruker du handlingen **Tilbakestill Microsoft-maler** for å gå tilbake til den opprinnelige innstillingen for arbeidsflyten.

> [!CAUTION]
> Handlingen **Tilbakestill Microsoft-maler** tilbakestiller alle Microsoft-arbeidsflytmalene. Du kan ikke tilbakestille én enkelt mal.  

En annen måte å opprette en arbeidsflyt raskt på, er å importere den, for eksempel hvis du eksporterte den fra en annen forekomst av [!INCLUDE[prod_short](includes/prod_short.md)]. Finn ut mer under [Eksporter og importer arbeidsflyter](across-how-to-export-and-import-workflows.md).  

## Slik oppretter du en arbeidsflyt fra arbeidsflytmaler

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny arbeidsflyt fra mal**. Siden **Arbeidsflytmaler** åpnes.  
3. Velg en arbeidsflytmal, og velg deretter **OK**.  

   **Arbeidsflyt**-siden åpnes for en ny arbeidsflyt som inneholder all informasjon for den valgte malen. Verdien i **Kode**-feltet utvides med for eksempel "-01" for å angi at dette er den første arbeidsflyten opprettet fra arbeidsflytmalen.  
4. Hvis du vil tilpasse arbeidsflyten, kan du redigere arbeidsflyttrinnene eller legge til nye trinn. Finn ut mer under [Opprett arbeidsflyter](across-how-to-create-workflows.md).  

## Se også

[Opprett arbeidsflyter for godkjenning](across-how-to-create-workflows.md)  
[Eksporter og importer arbeidsflyter for godkjenning](across-how-to-export-and-import-workflows.md)  
[Vis arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md)  
[Slett godkjenningsarbeidsflyter](across-how-to-delete-workflows.md)  
[Gjennomgang: Definer og bruk en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurer godkjenningsarbeidsflyter](across-set-up-workflows.md)  
[Bruk godkjenningsarbeidsflyter](across-use-workflows.md)  
[Arbeidsflyt](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
