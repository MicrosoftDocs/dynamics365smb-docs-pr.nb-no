---
title: Definere og bruke en arbeidsflyt for kjøpsgodkjenning
description: Du kan automatisere prosessen med å godkjenne nye eller endrede poster, for eksempel dokumenter, kladdelinjer og kundekort, ved å opprette arbeidsflyter med trinnene for godkjenninger som er aktuelle. Før du oppretter arbeidsflyter for godkjenning, må du definere en godkjenner og stedfortredende godkjenner for hver bruker for godkjenning. Du kan også angi godkjenneres beløpsgrenser for å definere hvilke salgs- og kjøpsposter de er kvalifisert til å godkjenne. Forespørsler om godkjenning og andre meldinger kan sendes som e-post eller intern merknad. For hvert brukeroppsett for godkjenning kan du også definere når de mottar meldinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/26/2021
ms.author: edupont
ms.openlocfilehash: 964e1dae3dc754198777c703a15c1ef0b6fe82a7
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110982"
---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning

Du kan automatisere prosessen med å godkjenne nye eller endrede poster, for eksempel dokumenter, kladdelinjer og kundekort, ved å opprette arbeidsflyter med trinnene for godkjenninger som er aktuelle. Før du oppretter arbeidsflyter for godkjenning, må du definere en godkjenner og stedfortredende godkjenner for hver bruker for godkjenning. Du kan også angi godkjenneres beløpsgrenser for å definere hvilke salgs- og kjøpsposter de er kvalifisert til å godkjenne. Forespørsler om godkjenning og andre meldinger kan sendes som e-post eller intern merknad. For hvert brukeroppsett for godkjenning kan du også definere når de mottar meldinger.

> [!NOTE]
> I tillegg til arbeidsflytfunksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] kan du bruke Power Automate til å definere arbeidsflyter for hendelser i [!INCLUDE[prod_short](includes/prod_short.md)]. Legg merke til at selv om de er to separate arbeidsflytsystemer, legges en flytmal som du oppretter med Power Automate, til i listen over arbeidsflytmaler i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, se [Bruke Business Central i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md).  

 Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn. Hvis du vil ha mer informasjon, kan du se [Arbeidsflyt](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen

Denne gjennomgangen tar for seg følgende oppgaver:  

- Definere godkjenningsbrukere  
- Definere meldinger for godkjenningsbrukere  
- Endre og aktivere en godkjenningsarbeidsflyt  
- Be om godkjenning av en bestilling, som Charlotte  
- Motta en varsling og deretter godkjenne forespørselen, som Stig  

## <a name="story"></a>Hovedscenario

Stig er en superbruker ved CRONUS. Han oppretter to godkjenningsbrukere. En er Charlotte som representerer en innkjøper. Den andre er ham selv som representerer Charlottes godkjenner. Stig gir selv ubegrensede rettigheter for kjøpsgodkjenning og angir at han skal motta meldinger ved internt notat så snart en relevant hendelse inntreffer. Til slutt oppretter Stig den nødvendige godkjenningsarbeidsflyten som en kopi av den eksisterende arbeidsflytmalen for arbeidsflyt for bestillingsgodkjenning, lar alle eksisterende hendelsesbetingelser og svaralternativer stå uendret, og aktiverer deretter arbeidsflyten.  

For å teste godkjenningsarbeidsflyten logger Stig seg først på [!INCLUDE[prod_short](includes/prod_short.md)] som Charlotte, og ber deretter om godkjenning av en bestilling. Stig logger seg deretter på som seg selv, ser notatet i rollesenteret, følger koblingen til godkjenningsforespørselen for bestillingen, og godkjenner forespørselen.  

## <a name="users"></a>Brukere

Før du kan definere godkjenningsbrukere og varslingsmetode, må du kontrollere at det finnes to brukere i [!INCLUDE[prod_short](includes/prod_short.md)]: én bruker representerer Charlotte. Den andre brukeren, deg selv, representerer Stig. Hvis du vil ha mer informasjon, se [Opprette brukere i henhold til lisenser](ui-how-users-permissions.md).

### <a name="setting-up-approval-users"></a>Definere godkjenningsbrukere

Når du er logget på som deg selv, definer Charlotte som godkjenningsbruker med deg selv om godkjenner. Sett opp godkjenningsrettigheter og angi hvordan og når du blir varslet om forespørsler om godkjenning.  

#### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Slik definerer du deg selv og Charlotte som godkjenningsbrukere

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukeroppsett for godkjenning**, og velg deretter den relaterte koblingen.  
2. På siden **Brukeroppsett for godkjenning** velger du handlingen **Ny**.  

    > [!NOTE]  
    >  Du må definere en godkjenner før du kan definere brukere som krever godkjenning fra denne godkjenneren. Du må derfor definere deg selv før du definerer Charlotte.  

3. Definer to godkjenningsbrukere ved å fylle ut feltene som beskrevet i følgende tabell.  

    |Bruker-ID|Godkjenner-ID|Ubegrenset kjøpsgodkjenning|  
    |-------------|-----------------|---------------------------------|  
    |DU||Valgt|  
    |CHARLOTTE|DU||  

### <a name="setting-up-notifications"></a>Definere varsler

I denne gjennomgangen varsles brukeren med et internt varsel om forespørsler som må godkjennes. Godkjenningsvarsel kan også være via e-post, og du kan legge til et trinn for arbeidsflytsvar som varsler avsenderen når en forespørsel godkjennes eller avslås. Hvis du vil ha mer informasjon, kan du se [Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### <a name="to-set-up-how-and-when-you-are-notified"></a>Slik definerer du hvordan og når du blir varslet

1. På siden **Brukeroppsett for godkjenning** velger du linjen for deg selv og deretter handlingen **Oppsett av varsling**.  
2. I feltet **Oppsett av varsling** på siden **Varslingstype** velger du **Godkjenning**.  
3. I feltet **Varslingsmetode** velger du **Bemerkning**.  
4. På siden **Oppsett av varsling** velger du handlingen **Tidsplan for varsling**.  
5. Velg **Umiddelbart** i **Gjentakelse**-feltet på siden **Tidsplan for varsling**.  

## <a name="creating-the-approval-workflow"></a>Opprette arbeidsflyten for godkjenning

Opprett arbeidsflyten for godkjenning av innkjøp ved å kopiere trinnene fra arbeidsflytmalen **Arbeidsflyt for bestillingsgodkjenning**. La de eksisterende trinnene i arbeidsflyten forblir uendret, og aktiver deretter arbeidsflyten.  

> [!TIP]
> Du kan eventuelt legge til et trinn for arbeidsflytsvar for å varsle avsenderen når forespørselen er godkjent eller avvist. Hvis du vil ha mer informasjon, kan du se [Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md).

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Slik oppretter og aktiverer du en arbeidsflyt for bestillingsgodkjenning:

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2. På siden **Arbeidsflyter** velger du **Handlinger**, velger **Ny** og velger handlingen **Ny arbeidsflyt fra mal**.  
3. På siden **Arbeidsflytmaler** velger du arbeidsflytmalen kalt **Arbeidsflyt for bestillingsgodkjenning**.  

    **Arbeidsflyt**-siden åpnes for en ny arbeidsflyt som inneholder all informasjon for den valgte malen. Verdien i **Kode**-feltet utvides med *-01* for å angi at dette er den første arbeidsflyten som er opprettet fra arbeidsflytmalen **Arbeidsflyt for bestillingsgodkjenning**.  
4. Merk av for **Aktivert** i hodet på **Arbeidsflyt**-siden.  

## <a name="using-the-approval-workflow"></a>Bruke arbeidsflyten for godkjenning

Bruk den nye arbeidsflyten for bestillingsgodkjenning ved først å logge på [!INCLUDE[prod_short](includes/prod_short.md)] som Charlotte for å be om godkjenning av en bestilling. Deretter logger du på som deg selv, viser notatet i rollesenteret, følger koblingen til forespørsel om godkjenning og godkjenner deretter forespørselen.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Slik ber du om godkjenning av en bestilling som Charlotte:

1. Logg på som Charlotte.
2. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.  
3. Velg linjen for å åpne bestilling 106001.  
4. På siden **Bestilling** velger du **Handlinger**, **Be om godkjenning** og deretter velger du handlingen **Send godkjenningsforespørsel**.  

Legg merke til at verdien i **Status**-feltet er endret til **Venter på godkjenning**.  

### <a name="to-approve-the-purchase-order-as-sean"></a>Slik godkjenner du bestillingen som Stig:

1. Logg på som Stig.
2. I området **Selvbetjening** i rollesenteret velger du flisen **Forespørsler å godkjenne**.
3. På siden **Forespørsler å godkjenne** velger du linjen for bestillingen ved Charlotte, og deretter velger du **Godkjenn**-handlingen.  

Verdien i **Status**-feltet i Charlottes bestilling endres til **Frigitt**.  

Du har nå definert og testet en enkel godkjenningsarbeidsflyt basert på de to første trinnene av arbeidsflyten Arbeidsflyt for bestillingsgodkjenning. Du kan enkelt utvide denne arbeidsflyten til å postere Charlottes bestilling automatisk når Stig godkjenner den. Hvis du vil gjøre dette, må du aktivere arbeidsflyten Arbeidsflyt for kjøpsfaktura, der svaret på en frigitt kjøpsfaktura, er å bokføre den. Først må du endre betingelsen for hendelsen i det første arbeidsflyttrinnet fra (kjøp) **Faktura** til **Ordre**.  

Den generiske versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] inneholder mange arbeidsflytmaler for scenarioer som støttes av programkoden. De fleste av disse er for arbeidsflyter for godkjenning.  

Du kan definere variasjoner i arbeidsflyter ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden. Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).  

Hvis et forretningsscenario krever en arbeidsflythendelse eller et arbeidsflytsvar som ikke støttes, må en Microsoft-partner implementere dem via kode, eller du kan konfigurere en arbeidsflyt ved å bruke Power Automate. Hvis du vil ha mer informasjon, kan du se [Bruke [!INCLUDE[prod_short](includes/prod_short.md)] i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md) eller [Hendelse i AL](/dynamics365/business-central/dev-itpro/developer/devenv-events-in-al) i hjelpen for utviklere.

## <a name="see-also"></a>Se også

[Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md)  
[Opprette arbeidsflyter](across-how-to-create-workflows.md)  
[Bruke arbeidsflyter for godkjenning](across-how-use-approval-workflows.md)  
[Arbeidsflyt](across-workflow.md)  
[Bruke Business Central i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]