---
title: "Gjennomgang – Plukking og levering i enkle lageroppsett | Microsoft-dokumentasjon"
description: "I Dynamics 365 kan de utgående prosessene for plukking og levering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 2ef41d6b1d224c016da4663d3059717c11611d92
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Gjennomgang: Plukking og levering i enkle lageroppsett
I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de utgående prosessene for plukking og levering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.  

|Prinsipp|Inngående prosess|Hyller|Plukking|Følgesedler|Kompleksitetsnivå (se [Designdetaljer: Lageroppsett](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokføre plukking og levering fra ordrelinjen|X|||2|  
|B|Bokføre plukking og levering fra et lagerplukkdokument||X||3|  
|L|Bokføre plukking og levering fra en lagerfølgeseddel|||X|4/5/6|  
|D|Bokføre plukking fra et lagerplukkdokument og bokføre leveringen fra en lagerfølgeseddel||X|X|4/5/6|  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Utgående lagerflyt](design-details-outbound-warehouse-flow.md).  

Følgende gjennomgangen demonstrerer metoden B i forrige tabell.  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen  
I grunnleggende lageroppsett hvor lokasjonen er definert til å kreve plukkbehandling, men ikke leveringsbehandling, bruker du vinduet **Lagerplukk** til å registrere og bokføre plukkings- og leveringsopplysninger for de utgående kildedokumentene. Det utgående kildedokumentet kan være en ordre, en bestillingsretur, en utgående overføringsordre eller en produksjonsordre med komponentbehov.  

Denne gjennomgangen viser følgende oppgaver:  

-   Definere SØLV-plassering for lagerplukkinger.  
-   Opprette en ordre for kunde 10000 for 30 høyttalere.  
-   Frigir ordren for lagerhåndtering.  
-   Opprette et lagerplukk basert på et frigitt kildedokument.  
-   Registrerer lagerflyttingen fra lageret og bokfører samtidig følgeseddelen for salgsordrekilden.  

## <a name="roles"></a>Roller  
Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:  

-   Lagerleder  
-   Ordrebehandler  
-   Lagermedarbeider  

## <a name="prerequisites"></a>Forutsetninger  
For å fullføre denne gjennomgangen må du gjøre følgende:  

-   Installere CRONUS Norge AS.  
-   Gjør deg til lageransatt på lokasjonen SØLV ved å følge disse trinnene:  

    1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lageransatte**, og velg deretter den relaterte koblingen.  
    2.  Velg feltet **Bruker-ID**, og velg din egen brukerkonto i **Brukere**-vinduet.  
    3.  Skriv inn SØLV i feltet **Lokasjonskode**.  
    4.  Velg **Standard**- feltet.  

-   Gjør elementet LS-81 tilgjengelig på SØLV-plasseringen ved å følge disse trinnene:  

    1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varekladder**, og velg deretter den relaterte koblingen.  
    2.  Åpne standardkladden, og opprett deretter to varekladdelinjer med følgende informasjon om arbeidsdatoen (23. januar).  

        |Posttype|Varenummer|Lokasjonskode|Hyllekode|Antall|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Oppjustering|LS-81|SØLV|S-01-0001 **Obs!**  Varens standardhylle i CRONUS|20|  
        |Oppjustering|LS-81|SØLV|S-01-0002|20|  

    3.  Velg **Bokfør**-handlingen, og velg deretter **Ja**-knappen.  

## <a name="story"></a>Hovedscenario  
Ellen, lagersjefen i CRONUS, setter opp SØLV-lageret for grunnleggende plukkhåndtering der lagermedarbeidere behandler utgående ordrer individuelt. Ordrebehandleren Heidi oppretter en ordre for 30 enheter av varen LS-81 som skal leveres til kunde 10000 fra SØLV-lageret. John, lagermedarbeideren, må kontrollere at forsendelsen klargjøres og leveres til kunden. John behandler alle involverte oppgaver i vinduet **Lagerplukk**, som peker automatisk til hyllene der LS-81 er lagret.  

## <a name="setting-up-the-location"></a>Definere plassering  
Oppsettet av vinduet **Lokasjonskort** definerer selskapets lagerflyter.  

### <a name="to-set-up-the-location"></a>Slik definerer du lokasjonen:  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
2.  Åpne lokasjonskortet SØLV.  
3.  Merk av for **Plukk nødv.**.  

## <a name="creating-the-sales-order"></a>Opprette ordren  
Salgsordrer er den vanligste typen av utgående kildedokumenter.  

### <a name="to-create-the-sales-order"></a>Slik oppretter du ordren  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Opprett en ordre for kunde 10000 på arbeidsdatoen (23. januar) med følgende ordrelinje.  

    |Vare|Lokasjonskode|Antall|  
    |----------|-------------------|--------------|  
    |LS_81|SØLV|30|  

     Fortsett med å informere lageret om at ordren er klar for lagerhåndtering.  

4.  Velg handlingen **Frigi**.  

    John fortsetter å plukke og leverer solgte varer.  

## <a name="picking-and-shipping-items"></a>Plukke og levere varer  
I vinduet **Lagerplukk** kan du håndtere alle utgående lageraktiviteter for et bestemt kildedokument, for eksempel en ordre.  

### <a name="to-pick-and-ship-items"></a>Slik plukker og leverer du varer:  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lagerplukk**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Velg feltet **Kildedokument**, og velg deretter **Ordre**.  
4.  Velg feltet **Kildenr.**, velg linjen for salg til kunde 10000, og velg deretter **OK**-knappen.  

    Velg eventuelt **Hent kildedokument**-handlingen, og velg deretter ordren.  
5.  Velg handlingen **Autoutfyll ant som skal håndt**.  

    Du kan også skrive inn 10 og 30 i de to lagerplukklinjene i feltet **Ant. som skal håndt.**.  
6.  Velg **Bokfør**-handlingen, velg **Lever**, og velg deretter **OK**-knappen.  

    30 høyttalere er nå registrert som plukket fra hyllene S-01-0001 og S-01-0002, og det opprettes en negativ varepost som gjenspeiler den bokførte følgeseddelen.  

## <a name="see-also"></a>Se også  
 [Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md)   
 [Plukke varer for lagerlevering](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Opprette grunnleggende lagre med operasjonsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Flytte komponenter til et operasjonsområde i enkle lageroppsett](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Plukke for produksjon eller montering](warehouse-how-to-pick-for-production.md)   
 [Flytte varer ad hoc i enkle lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Designdetaljer: Utgående lagerflyt](design-details-outbound-warehouse-flow.md)   
 [Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

