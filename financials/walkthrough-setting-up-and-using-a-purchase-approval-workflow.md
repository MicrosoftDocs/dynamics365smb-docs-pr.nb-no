---
title: "Gjennomgang – Definere og bruke en arbeidsflyt for kjøpsgodkjenning | Microsoft-dokumentasjon"
description: "Du kan automatisere prosessen med å godkjenne nye eller endrede poster, for eksempel dokumenter, kladdelinjer og kundekort, ved å opprette arbeidsflyter med trinnene for godkjenninger som er aktuelle. Før du oppretter arbeidsflyter for godkjenning, må du definere en godkjenner og stedfortredende godkjenner for hver bruker for godkjenning. Du kan også angi godkjenneres beløpsgrenser for å definere hvilke salgs- og kjøpsposter de er kvalifisert til å godkjenne. Forespørsler om godkjenning og andre meldinger kan sendes som e-post eller intern merknad. For hvert brukeroppsett for godkjenning kan du også definere når de mottar meldinger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 7ce4b45d740e50bba8256e72fcf43c70ea85922c
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning
Du kan automatisere prosessen med å godkjenne nye eller endrede poster, for eksempel dokumenter, kladdelinjer og kundekort, ved å opprette arbeidsflyter med trinnene for godkjenninger som er aktuelle. Før du oppretter arbeidsflyter for godkjenning, må du definere en godkjenner og stedfortredende godkjenner for hver bruker for godkjenning. Du kan også angi godkjenneres beløpsgrenser for å definere hvilke salgs- og kjøpsposter de er kvalifisert til å godkjenne. Forespørsler om godkjenning og andre meldinger kan sendes som e-post eller intern merknad. For hvert brukeroppsett for godkjenning kan du også definere når de mottar meldinger.  

 Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn. Hvis du vil ha mer informasjon, kan du se [Arbeidsflyt](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen  
Denne gjennomgangen tar for seg følgende oppgaver:  

-   Definere godkjenningsbrukere (inkl. definere en bruker i Windows og i [!INCLUDE[d365fin](includes/d365fin_md.md)]).  
-   Definere meldinger for godkjenningsbrukere.  
-   Endre og aktivere en godkjenningsarbeidsflyt.  
-   Starte jobbkøen som sender varslinger.  
-   Be om godkjenning av en bestilling, som Charlotte.  
-   Motta en varsling og deretter godkjenne forespørselen, som Stig.  

## <a name="prerequisites"></a>Forutsetninger  
For å fullføre denne gjennomgangen trenger du demonstrasjonsselskapet CRONUS Norge AS.

## <a name="story"></a>Hovedscenario  
Stig er en superbruker hos CRONUS på sin egen datamaskin.  

Han oppretter to godkjenningsbrukere. En er Charlotte som representerer en innkjøper. Den andre er ham selv som representerer Charlottes godkjenner. Stig gir selv ubegrensede rettigheter for kjøpsgodkjenning og angir at han skal motta meldinger ved internt notat så snart en relevant hendelse inntreffer. Til slutt oppretter Stig den nødvendige godkjenningsarbeidsflyten som en kopi av den eksisterende arbeidsflytmalen for arbeidsflyt for bestillingsgodkjenning, lar alle eksisterende hendelsesbetingelser og svaralternativer stå uendret, og aktiverer deretter arbeidsflyten.  

For å teste godkjenningsarbeidsflyten logger Stig seg først på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Charlotte, og ber deretter om godkjenning av en bestilling. Stig logger seg deretter på som seg selv, ser notatet i rollesenteret, følger koblingen til godkjenningsforespørselen for bestillingen, og godkjenner forespørselen.  

## <a name="setting-up-the-sample-data"></a>Konfigurere eksempeldataene  
Du må opprette en ny bruker på den lokale datamaskinen og i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å representere Charlotte som du senere skal velge som en godkjenningsbruker. Din egen brukerkonto vil representere Stig.  

### <a name="to-add-alicia-as-a-user-on-the-local-computer"></a>Slik legger du til Charlotte som en bruker på den lokale datamaskinen  

1.  Velg **Start**. I boksen **Søk i programmer og filer** skriver du **Rediger lokale brukere og grupper**. Velg deretter den relaterte koblingen.  
2.  Åpne mappen **Brukere**.  
3.  I fanebladet **Handlinger** velger du **Ny bruker**.  
4.  I **Brukernavn**-feltet skriver du inn Charlotte.  
5.  I feltene **Passord** og **Bekreft passord** skriver du inn et gyldig passord.  
6.  Fjern merket i avmerkingsboksen **Brukeren må endre passordet ved neste pålogging**.  
7.  Lukk vinduet **Lokale brukere og grupper**.  

### <a name="to-add-alicia-as-a-user-in-included365finincludesd365finmdmd"></a>Slik legger du til Charlotte som en bruker i [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Brukere**, og velg deretter den relaterte koblingen.  
2.  I **Windows-brukere**-vinduet i **Hjem**-fanen velger du **Ny** i **Ny**-gruppen.  
3.  I vinduet **Brukerkort** i **Brukernavn**-feltet angir du Charlotte.  
4.  Klikk AssistEdit-knappen i **Windows-brukernavn**-feltet.  
5.  I vinduet **Velg bruker eller gruppe** i feltet **Skriv inn objektnavnet som skal velges** angir du Charlotte, og deretter velger du **Kontroller navn**-knappen.  
6.  Når [DATAMASKINNAVN]CHARLOTTE vises i feltet, velger du **OK**-knappen.  
7.  I hurtigfanen **Brukertillatelsessett** i **Tillatelsessett**-feltet velger du **SUPER**.  
8.  I **Selskap**-feltet velger du **CRONUS International Ltd.**  
9. Velg **OK**-knappen.  

## <a name="setting-up-approval-users"></a>Definere godkjenningsbrukere  
Ved hjelp av Windows-brukeren som du nettopp opprettet, definerer du Charlotte som en godkjenningsbruker med deg selv som godkjenner. Sett opp godkjenningsrettigheter og angi hvordan og når du blir varslet om forespørsler om godkjenning.  

### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Slik definerer du deg selv og Charlotte som godkjenningsbrukere  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Brukeroppsett for godkjenning**, og velg deretter den relaterte koblingen.  
2.  Velg **Ny** under **Ny** i fanebladet **Hjem** i vinduet **Brukeroppsett for godkjenning**.  

    > [!NOTE]  
    >  Du må definere en godkjenner før du kan definere brukere som krever godkjenning fra denne godkjenneren. Du må derfor definere deg selv før du definerer Charlotte.  

3.  Definer to godkjenningsbrukere ved å fylle ut feltene som beskrevet i følgende tabell.  

    |Bruker-ID|Godkjenner-ID|Ubegrenset kjøpsgodkjenning|  
    |-------------|-----------------|---------------------------------|  
    |[DATAMASKINNAVN][DEG]||Valgt|  
    |[DATAMASKINNAVN]CHARLOTTE|[DATAMASKINNAVN][DEG]||  

## <a name="setting-up-notifications"></a>Definere varsler  
Angi hvordan og når du blir varslet om forespørsler om godkjenning.  

### <a name="to-set-up-how-and-when-you-are-notified"></a>Slik definerer du hvordan og når du blir varslet  
1.  I vinduet **Brukeroppsett for godkjenning** velger du linjen for deg selv, og deretter, i fanebladet **Hjem** i **Prosess**-gruppen, velger du **Meldingsoppsett**.  
2.  I feltet **Oppsett av varsling**i **Varslingstype**-feltet angir du **Godkjenning**.  
3.  Velg feltet **Varslingsmalkode**, og velg deretter **Avansert**-knappen.  
4.  Velg **Rediger liste** i **Behandle**-gruppen i fanen **Hjem** i **Varslingsmaler**-vinduet.  
5.  På linjen for GODKJENNING-malen i feltet **Varslingsmetode** angir du **Notat**.  
6.  Velg **OK**.  
7.  I **Oppsett av varsling**-vinduet i **Hjem**-fanen under **Prosess** velger du **Tidsplan for varsling**.  
8.  Velg **Umiddelbart** i **Forekomst**-feltet i vinduet **Tidsplan for varsling**.  
9. Velg **OK**.  

## <a name="creating-the-approval-workflow"></a>Opprette arbeidsflyten for godkjenning  
 Opprett arbeidsflyten for godkjenning av innkjøp ved å kopiere trinnene fra arbeidsflytmalen for arbeidsflyt for bestillingsgodkjenning. La de eksisterende trinnene i arbeidsflyten forblir uendret, og aktiver deretter arbeidsflyten.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Slik oppretter og aktiverer du en arbeidsflyt for bestillingsgodkjenning:  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2.  Velg **Opprett arbeidsflyt fra mal** under **Generelt** på fanebladet **Handlinger** i vinduet **Arbeidsflyter**.  
3.  Velg **Opprett arbeidsflyt fra mal** under **Generelt** på fanebladet **Handlinger**. Vinduet **Arbeidsflytmaler** åpnes.  
4.  Velg arbeidsflytmalen kalt Arbeidsflyt for bestillingsgodkjenning, og velg deretter **OK**.  

    **Arbeidsflyt**-vinduet åpnes for en ny arbeidsflyt som inneholder all informasjon for den valgte malen. Verdien i **Kode**-feltet utvides med "-01" for å angi at dette er den første arbeidsflyten som er opprettet fra arbeidsflytmalen Arbeidsflyt for bestillingsgodkjenning.  
5.  Merk av for **Aktivert** i hodet i **Arbeidsflyt**-vinduet.  

## <a name="starting-a-notification-job-queue"></a>Starte en jobbkø for varsel  
Kontroller at jobbkøen i installasjonen er definert til å håndtere arbeidsflytvarsler.  

### <a name="to-start-the-notify-job-queue"></a>Slik starter du jobbkøen VARSLE:  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Jobbkøer**, og velg deretter den relaterte koblingen.  
2.  I vinduet **Jobbkøer** velger du linjen for jobbkøen VARSLE, og deretter velger du **Start jobbkø** under **Prosess** på fanebladet **Hjem**.  

## <a name="using-the-approval-workflow"></a>Bruke arbeidsflyten for godkjenning  
Bruk den nye arbeidsflyten for bestillingsgodkjenning ved først å logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Charlotte for å be om godkjenning av en bestilling. Deretter logger du på som deg selv, viser notatet i rollesenteret, følger koblingen til forespørsel om godkjenning og godkjenner deretter forespørselen.  

For å logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] som forskjellige brukere bruker du funksjonen **Kjør som annen bruker**.  

### <a name="to-log-into-included365finincludesd365finmdmd-as-alicia"></a>Slik logger du på [!INCLUDE[d365fin](includes/d365fin_md.md)] som Charlotte:  

1.  For [!INCLUDE[d365fin](includes/d365fin_md.md)]-webklienten, på startknappen for websiden i leseren, trykker du Skift + høyreklikk, og velger deretter **Kjør som annen bruker**.  

    For Windows-klienten for [!INCLUDE[d365fin](includes/d365fin_md.md)], på startknappen for programmet, trykker du Skift + høyreklikk, og velger deretter **Kjør som annen bruker**.  

2.  I vinduet **Windows-sikkerhet** skriver du inn [DATAMASKINNAVN]CHARLOTTE og det påkrevde passordet.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Slik ber du om godkjenning av en bestilling som Charlotte:  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bestillinger**, og velg deretter den relaterte koblingen.  
2.  Velg linjen for åpen bestilling 104001, og velg deretter **Rediger** under **Behandle** i fanebladet **Hjem**.  
3.  I vinduet **Bestilling** på fanebladet **Handlinger** under **Godkjenning** velger du **Send godkjenningsforespørsel**.  

    Legg merke til at verdien i **Status**-feltet er endret til **Venter på godkjenning**.  

4.  Lukk [!INCLUDE[d365fin](includes/d365fin_md.md)].  

### <a name="to-approve-the-purchase-order-as-sean"></a>Slik godkjenner du bestillingen som Stig:  

1.  Åpne [!INCLUDE[d365fin](includes/d365fin_md.md)] på vanlig måte. Programmet åpnes med deg som bruker.  
2.  I rollesenteret i **Mine varsler**-vinduet ser du etter et nytt notat fra Charlotte.  

    > [!NOTE]  
    >  Selv om regelmessigheten for varsling er satt til **Umiddelbart**, kommer notatet omtrent ett minutt etter at Charlotte har sendt forespørselen om godkjenning. Dette skyldes standard regelmessighetshyppighet for jobbkøfunksjonen.  

3.  Når notatet vises i **Mine varsler**-vinduet, velger du verdien **Godkjenningspost: XX, XX** i **Side**-feltet. Vinduet **Forespørsler å godkjenne** åpnes med Charlottes forespørsel for bestillingen uthevet.  
4.  Velg **Godkjenn** under **Prosess** på fanebladet **Hjem** i **Forespørsler å godkjenne**-vinduet.  

    Verdien i **Status**-feltet i Charlottes bestilling endres til **Frigitt**.  

Du har nå definert og testet en enkel godkjenningsarbeidsflyt basert på de to første trinnene av arbeidsflyten Arbeidsflyt for bestillingsgodkjenning. Du kan enkelt utvide denne arbeidsflyten til å postere Charlottes bestilling automatisk når Stig godkjenner den. Hvis du vil gjøre dette, må du aktivere arbeidsflyten Arbeidsflyt for kjøpsfaktura, der svaret på en frigitt kjøpsfaktura, er å bokføre den. Først må du endre betingelsen for hendelsen i det første arbeidsflyttrinnet fra (kjøp) **Faktura** til **Ordre**.  

Den generiske versjonen [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder mange arbeidsflytmaler for scenarier som støttes av programkoden. De fleste av disse er for arbeidsflyter for godkjenning. Hvis du vil ha mer informasjon, kan du se Arbeidsflytmaler.  

Du kan definere variasjoner i arbeidsflyter ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden. Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).  

Hvis et forretningsscenario krever en arbeidsflythendelse eller et arbeidsflytsvar som ikke støttes, må en Microsoft-partner implementere dem ved å tilpasse programkoden. Hvis du vil ha mer informasjon, kan du se [Gjennomgang: Implementering av nye arbeidsflythendelser og svar](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) i hjelpen for utviklere og IT-eksperter.  

## <a name="see-also"></a>Se også  
[Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md)   
[Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md)   
[Opprette arbeidsflyter](across-how-to-create-workflows.md)   
[Bruke arbeidsflyter for godkjenning](across-how-use-approval-workflows.md)   
[Arbeidsflyt](across-workflow.md)

