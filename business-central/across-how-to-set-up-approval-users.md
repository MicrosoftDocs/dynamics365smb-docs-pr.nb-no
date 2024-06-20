---
title: Konfigurere godkjenningsbrukere
description: 'Før du kan opprette arbeidsflyter som omfatter godkjenningstrinn, må du definere arbeidsflytbrukerne som er involvert i godkjenningsprosessen.'
author: brentholtorf
ms.topic: how-to
ms.devlang: al
ms.search.form: '663,'
ms.date: 05/31/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Konfigurer godkjenningsbrukere

Før du kan opprette arbeidsflyter som omfatter godkjenningstrinn, må du definere brukerne som er involvert i godkjenningsprosessene på siden **Brukeroppsett for godkjenning**. Du kan også angi beløpsgrenser for ulike typer forespørsler, definere erstatningsgodkjennere og definere meldinger.  

Når du har definert godkjenningsbrukere, kan du opprette arbeidsflytsvar for godkjenningsarbeidsflyter. Finn ut mer under [Opprett godkjenningsarbeidsflyter](across-how-to-create-workflows.md).  

> [!TIP]
> Du kan kreve at flere godkjennere reagere på en godkjenningsforespørsel, ved å opprette en gruppe godkjennere på siden **Brukergruppe for arbeidsflyt**. Finn ut mer under [Definer brukergrupper for arbeidsflyt](across-how-to-set-up-workflow-users.md).  

## Slik konfigurerer du godkjenningsbrukere

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukeroppsett for godkjenning**, og velg deretter den relaterte koblingen.  
2. Opprett en ny linje på siden **Brukeroppsett for godkjenning**, og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

   |Felt|Description|
   |-----|-----------|
   |**Bruker-ID**|Velg bruker-ID-en til personen involvert i godkjenningsprosessen.|
   |**Selger/innkjøper - kode**|Angi selger- eller innkjøperkoden som gjelder for brukerne.<br /><br /> Du fyller vanligvis ut feltet **Selger/innkjøper - kode** hvis selgeren eller innkjøperen som har ansvaret for kunden eller leverandøren, også er personen som må godkjenne en salgs- eller kjøpsforespørsel.|
   |**Godkjenner-ID**|Velg bruker-ID-en til personen som må godkjenne forespørsler fra personen du definerte i **Bruker-ID**-feltet.|
   |**Godkjenningsgrense salg**|Angi maksimalt salgsbeløp i lokal valuta (LV) som personen valgt i **Bruker-ID**-feltet, kan godkjenne.|
   |**Ubegrenset salgsgodkjenning**|Angi at personen identifiserte i **Bruker-ID**-feltet kan godkjenne alle salgsforespørsler uavhengig av beløpet.<br /><br /> Hvis du merker av her, kan du ikke fylle ut feltet **Godkjenningsgrense salg**.|
   |**Godkjenningsgrense kjøp**|Angi maksimumsbeløpet i LV som personen identifisert i **Bruker-ID**-feltet kan godkjenne.|
   |**Ubegrenset kjøpsgodkjenning**|Angi at personen identifiserte i **Bruker-ID**-feltet kan godkjenne alle kjøpsforespørsler uavhengig av beløpet.<br /><br /> Hvis du merker av her, kan du ikke fylle ut feltet **Godkjenningsgrense kjøp**.|
   |**Godkjenningsgrense forespørsel**|Angi maksimumsbeløpet i LV som personen identifisert i **Bruker-ID**-feltet kan godkjenne for forespørsler.<br /><br /> Hvis du vil bruke dette feltet, må du velge alternativet **Godkjennerkjede** i feltet **Godkjennergrensetype** på siden **Arbeidsflytsvar**.|
   |**Ubegrenset forespørselsgodkjenning**|Angi at personen identifiserte i **Bruker-ID**-feltet kan godkjenne alle forespørsler uavhengig av beløpet.<br /><br /> Hvis du merker av her, kan du ikke fylle ut feltet **Godkjenningsgrense forespørsel**.|
   |**Stedfortreder**|Velg bruker-ID-en til personen som må godkjenne forespørsler fra personen i identifisert i **Bruker-ID**-feltet, hvis brukeren i **Godkjenner-ID** ikke er tilgjengelig. <br /><br />**Obs!** Stedfortrederen kan enten være brukeren i **Stedfortreder**-feltet, den direkte godkjenneren eller godkjenningsadministratoren, i denne rekkefølgen. Finn ut mer under [Bruk godkjenningsarbeidsflyter](across-how-use-approval-workflows.md).|
   |**E-post**|Angi e-postadressen for personen i **Bruker-ID**-feltet.|
   |**Godkjenningsansvarlig**|Angi brukeren som har tillatelse til å fjerne blokkeringen av godkjenningsarbeidsflyt, som ved å delegere godkjenningsforespørsler til nye stedfortredere for godkjenning eller slette forfalte godkjenningsforespørsler.<br /><br />**Obs!** Det er bare én person som kan være godkjenningsansvarlig.|

3. Hvis du vil teste brukeroppsettet for godkjenning, velger du **Test av brukeroppsett for godkjenning**.  
4. Gjenta trinn 2 og 3 for alle personer som du vil definere som godkjenningsbrukere.  

Neste trinn er å angi hvordan du vil at [!INCLUDE [prod_short](includes/prod_short.md)] skal varsle personer om at en forespørsel venter på oppmerksomhet. Finn ut mer under [Konfigurering av godkjenningsarbeidsflytvarsler](across-setting-up-workflow-notifications.md).

## Se også

[Konfigurer arbeidsflytbrukere](across-how-to-set-up-workflow-users.md)  
[Konfigurer arbeidsflytvarsler](across-setting-up-workflow-notifications.md)  
[Opprett godkjenningsarbeidsflyter](across-how-to-create-workflows.md)  
[Konfigurer godkjenningsarbeidsflyter](across-set-up-workflows.md)  
[Gjennomgang: Definer og bruk en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbeidsflyt](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
