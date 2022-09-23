---
title: Plukking og levering i enkle lageroppsett
description: I Business Central kan de utgående prosessene for plukking og levering utføres på følgende fire måter avhengig av kompleksitetsnivået til lageret.
author: jill-kotel-andersson
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: baa47a48cf7813a704666cb130eddc0adc6f4923
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531948"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Gjennomgang: Plukking og levering i enkle lageroppsett

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

I [!INCLUDE[prod_short](includes/prod_short.md)] kan de utgående prosessene for plukking og levering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.  

|Prinsipp|Inngående prosess|Hyller|Plukking|Følgesedler|Kompleksitetsnivå (se [Designdetaljer: Lageroppsett](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokføre plukking og levering fra ordrelinjen|X|||2|  
|B|Bokføre plukking og levering fra et lagerplukkdokument||X||3|  
|L|Bokføre plukking og levering fra en lagerfølgeseddel|||X|4/5/6|  
|D|Bokføre plukking fra et lagerplukkdokument og bokføre leveringen fra en lagerfølgeseddel||X|X|4/5/6|  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Utgående lagerflyt](design-details-outbound-warehouse-flow.md).  

Følgende gjennomgangen demonstrerer metoden B i forrige tabell.  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen

I grunnleggende lageroppsett hvor lokasjonen er definert til å kreve plukkbehandling, men ikke leveringsbehandling, bruker du siden **Lagerplukk** til å registrere og bokføre plukkings- og leveringsopplysninger for de utgående kildedokumentene. Det utgående kildedokumentet kan være en ordre, en bestillingsretur, en utgående overføringsordre eller en produksjonsordre med komponentbehov.  

Denne gjennomgangen viser følgende oppgaver:  

- Definere SØR-plassering for lagerplukkinger.  
- Opprette en ordre for kunde 10000 for 30 Amsterdam-lamper.  
- Frigir ordren for lagerhåndtering.  
- Opprette et lagerplukk basert på et frigitt kildedokument.  
- Registrerer lagerflyttingen fra lageret og bokfører samtidig følgeseddelen for salgsordrekilden.  

## <a name="roles"></a>Roller

Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:  

- Lagerleder  
- Ordrebehandler  
- Lagermedarbeider  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a>Hovedscenario

Ellen, lagersjefen på CRONUS, setter opp SØR-lageret for grunnleggende plukkhåndtering der lagermedarbeidere behandler utgående ordrer individuelt. Ordrebehandleren Heidi oppretter en ordre for 30 enheter av varen 1928-S som skal leveres til kunde 10000 fra SØR-lageret. John, lagermedarbeideren, må kontrollere at forsendelsen klargjøres og leveres til kunden. John behandler alle involverte oppgaver på siden **Lagerplukk**, som peker automatisk til hyllene der 1928-S er lagret.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a>Definere hyllekodene

Når lokasjonen er definert, må du legge til to hyller.

#### <a name="to-setup-the-bin-codes"></a>Slik definerer du hyllekodene

1. Velg handlingen **Hyller**.
2. Opprett to hyller med kodene *S-01-0001* og *S-01-0002*.

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a>Opprette deg selv som en lageransatt på lokasjon SØR

For å kunne bruke denne funksjonaliteten må du legge deg selv til på lokasjonen som en lagerarbeider. 

#### <a name="to-make-yourself-a-warehouse-employee"></a>Slik oppretter du deg selv som en lageransatt

  1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg første.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageransatte**, og velg deretter den relaterte koblingen.  
  2. Velg feltet **Bruker-ID**, og velg din egen brukerkonto på siden **Lageransatte**.
  3. Velg SØR i feltet **Lokasjonskode**.  
  4. Velg feltet **Standard**, og velg deretter **Ja**-knappen.  

### <a name="making-item-1928-s-available"></a>Gjøre vare 1928-S tilgjengelig

For å gjøre varen 1928-S tilgjengelig på SØR-plasseringen følger du denne fremgangsmåten:  

  1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg andre.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varekladder** og velg den relaterte koblingen.  
  2. Åpne standardkladden, og opprett deretter to varekladdelinjer med følgende informasjon om arbeidsdatoen (23. januar).  

        |Posttype|Varenummer|Lokasjonskode|Hyllekode|Antall|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Oppjustering|1928-S|SØR|S-01-0001|20|  
        |Oppjustering|1928-S|SØR|S-01-0002|20|  

        Som standard er feltet **Hyllekode** på salgslinjen skjult, så du må vise den. Du må tilpasse siden for å gjøre dette. Hvis du vil ha mer informasjon, kan du se [Slik tilpasser du en side med Tilpasse-banneret](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

  3. Velg **Handlinger**, **Bokføring** og deretter **Bokfør**.  
  4. Velg **Ja**-knappen.  

## <a name="creating-the-sales-order"></a>Opprette ordren

Salgsordrer er den vanligste typen av utgående kildedokumenter.  

### <a name="to-create-the-sales-order"></a>Slik oppretter du ordren

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg tredje.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Opprett en ordre for kunde 10000 på arbeidsdatoen (23. januar) med følgende ordrelinje.  

    |Vare|Lokasjonskode|Antall|  
    |----|-------------|--------|  
    |1928-S|SØR|30|  

     Fortsett med å informere lageret om at ordren er klar for lagerhåndtering.  

4. Velg handlingen **Frigi**.  

    John fortsetter å plukke og leverer solgte varer.  

## <a name="picking-and-shipping-items"></a>Plukke og levere varer

På siden **Lagerplukk** kan du håndtere alle utgående lageraktiviteter for et bestemt kildedokument, for eksempel en ordre. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>Slik plukker og leverer du varer:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg fjerde.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplukk**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  

    Pass på at **Nr.** -feltet i hurtigfanen **Generelt** er fylt ut.
3. Velg feltet **Kildedokument**, og velg deretter **Ordre**.  
4. Velg feltet **Kildenr.**, velg linjen for salg til kunde 10000, og velg deretter **OK**-knappen.  

    Velg eventuelt **Hent kildedokument**-handlingen, og velg deretter ordren.  
5. Velg handlingen **Autoutfyll ant som skal håndt**.  

    Du kan også skrive inn 10 og 20 i de to lagerplukklinjene i feltet **Ant. som skal håndt.**.  
6. Velg **Bokfør**-handlingen, velg **Lever**, og velg deretter **OK**-knappen.  

    30 Amsterdam-lamper er nå registrert som plukket fra hyllene S-01-0001 og S-01-0002, og det opprettes en negativ varepost som gjenspeiler den bokførte følgeseddelen.  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Se også

[Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Plukke varer for lagerlevering](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Opprette grunnleggende lagre med operasjonsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Flytte komponenter til et operasjonsområde i enkle lageroppsett](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[Plukke for produksjon eller montering](warehouse-how-to-pick-for-production.md)  
[Flytte varer ad hoc i enkle lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Designdetaljer: Utgående lagerflyt](design-details-outbound-warehouse-flow.md)  
[Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
