---
title: Tilordne brukertillatelser og opprette eller endre tillatelsessett | Microsoft-dokumentasjon
description: Beskriver hvordan du legger til Office 365-brukere i Financials og deretter tilordner tillatelser, tilgangsrettigheter og sikkerhetsinnstillinger.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 06/27/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a944a6135feeb81b32d1f7edcb823b9da89cd404
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-users-and-permissions"></a>Administrere brukere og tillatelser
For å legge til brukere i [!INCLUDE[d365fin](includes/d365fin_md.md)] må selskapets Office 365-administrator først opprette brukere i administrasjonssenteret for Office 365. For mer informasjon, se [Legge til brukere i Office 365 for bedrifter](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Når brukere er opprettet i Office 365, kan de importeres i **Brukere**-vinduet ved å velge handlingen **Hent brukere fra Office 365**. Brukere er tilordnet tillatelsessett avhengig av planen som er tilordnet til brukeren i Office 365.

Du kan deretter fortsette med å tildele tillatelser til brukere til å definere hvilke databaseobjekter, og dermed hvilke grensesnittelementer, de har tilgang til, og i som bedrifter.

Et tillatelsessett er en samling tillatelser for bestemte objekter i databasen. Alle brukere må være tilordnet ett eller flere tillatelsessett før de kan åpne [!INCLUDE[d365fin](includes/d365fin_md.md)]. Et antall forhåndsdefinerte tillatelsessett leveres som standard. Du kan bruke disse tillatelsessettene slik de allerede er definert, endre standardtillatelsessettene eller opprette flere egne tillatelsessett.

Du kan legge til brukere i grupper. Dette gjør det enklere å tilordne samme tillatelsessett til flere brukere.

Administratorer kan bruke vinduet **Brukeroppsett** til å definere hvor lenge angitte brukere skal kunne bokføre, og også angi om systemet skal logge hvor lenge brukere er logget på.

> [!NOTE]  
>   Denne funksjonen krever at opplevelsen er satt til Suite. Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Slik tilordner du tillatelser til en bruker til
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg brukeren du vil tilordne tillatelse til.
Eventuelle tillatelsessett som allerede er tilordnet til brukeren, vises i faktaboksen **Tillatelsessett**.
3. Velg handlingen **Rediger** for å åpne **Brukerkort**-vinduet.
4. På hurtigfanen **Brukertillatelsessett** fyller du ut feltene etter behov på en ny linje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Slik grupperer du brukere i brukergrupper
Du kan definere brukergrupper til å administrere tillatelsessett for grupper av brukere i firmaet. Du kan bruke en funksjon til å kopiere alle tillatelsessett fra en eksisterende brukergruppe til den nye brukergruppen. Medlemmene i brukergruppen kopieres ikke.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Brukergrupper**, og velg deretter den relaterte koblingen.
2. Du kan også gå til vinduet **Brukere** og velge handlingen **Brukergrupper**.
3. I vinduet **Brukergrupper** velger du en eksisterende brukergruppe du vil kopiere, og velg deretter **Kopier brukergruppe**.
4. I feltet **Ny brukergruppekode** angir du navnet på den nye brukergruppen, og velg deretter **OK**-knappen.

    Som et alternativ til å kopiere, kan du velge den nye handlingen til å opprette en ny linje for en tom brukergruppen, som du deretter fylle ut manuelt.
5. Til å legge til nye eller ekstra brukere i **Brukergruppe**-vinduet velger du **Brukergruppemedlemmer**-handlingen.
6. I vinduet **Brukergruppemedlemmer** på en ny linje, fyller du ut feltene etter behov ved å velge fra eksisterende brukere.
7. Til å legge til nye eller ekstra tillatelsessett, i **Brukergruppe**-vinduet velger du **Tillatelsessett for brukergruppe**.
8. I vinduet **Tillatelsessett for brukergruppe** på en ny linje, fyller du ut feltene etter behov ved å velge fra eksisterende tillatelsessett.

## <a name="to-create-or-modify-permission-sets"></a>Opprette eller endre tillatelsessett
Hvis de standard tillatelsessettene som følger med [!INCLUDE[d365fin](includes/d365fin_md.md)], ikke er tilstrekkelige eller aktuelle for din organisasjon, kan du opprette nye tillatelsessett. Og hvis de individuelle objekttillatelsene som definerer et tillatelsessett ikke er tilstrekkelige, kan du endre tillatelsessettet. Du kan opprette et tillatelsessett manuelt, eller du kan bruke en registrering funksjon som registrerer handlingene dine mens du navigerer gjennom et scenario og genererer deretter nødvendige tillatelsessettet.

### <a name="to-create-or-modify-permission-sets-manually"></a>Opprette eller endre tillatelsessett manuelt
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. I vinduet **Brukere** velger du handlingen **Tillatelsessett**.
3. I vinduet **Tillatelsessett** velger du handlingen **Ny**.
4. Fyll ut feltene etter behov på en ny linje.
5. Velg handlingen **Tillatelser**.
6. I vinduet **Tillatelser** fyller du ut feltene i overskriften etter behov.
7. På en ny linje, fyller du ut feltene fem for ulike tilgangstypene som er beskrevet i følgende tabell.

    |Alternativ|Beskrivelse|
    |------|-----------|
    |Tom|Angir at tillatelsestypen ikke gis for objektet.|
    |**Ja**|Angir at tillatelsestypen gis med direkte tilgang til objektet.|
    |**Indirekte**|Angir at tillatelsestypen gis med indirekte tilgang til objektet.|

    Indirekte tilgang til en tabell betyr at du kan ikke åpne tabellen og lese den, men du kan vise dataene i tabellen til et annet objekt, for eksempel en side, at du har direkte tilgang til. Hvis du vil ha mer informasjon, kan du se delen "Eksempel - indirekte tillatelse" i dette emnet.

8. I feltet **Sikkerhetsfilter** angir du et filter som du vil bruke på tillatelse ved å velge feltet du vil begrense tilgangen til en bruker.

    For eksempel hvis du vil opprette et sikkerhetsfilter slik at en bruker kan vise salg for bare med en bestemt selger, du velger feltnummeret for **Selgerkode**-feltet. Deretter, i feltet **Feltfilter**, du angir verdien for som du vil bruke til å begrense tilgangen. Hvis du vil begrense en brukers tilgang til bare Annette Hill salg, kan du for eksempel angi AH.
9. Gjenta trinn 7 og 8 for å legge til tillatelser for flere objekter i tillatelsessettet.

### <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Hvis du vil opprette eller endre tillatelsen angis ved makroregistreringen
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. I vinduet **Brukere** velger du handlingen **Tillatelsessett**.
3. I vinduet **Tillatelsessett** velger du handlingen **Ny**.
4. Fyll ut feltene etter behov på en ny linje.
5. Velg handlingen **Tillatelser**.
6. I vinduet **Tillatelser** velger du handlingen **Start**.

    En innspillingsprosess begynner for å fange opp alle handlinger i brukergrensesnittet.
7. Gå til de ulike vinduene og aktivitetene i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du vil at brukere med dette tillatelsessettet skal få tilgang til. Du må utføre oppgaver som du vil registrere tillatelser for.
8. Når du vil avslutte opptaket, gå tilbake til **Tillatelser**-vinduet, og velg deretter **Stopp**-handlingen.
9. Velg **Ja**-knappen for å legge til registrerte rettigheter til det nye tillatelsessettet.
10. Angi om brukere skal kunne sette inn, endre eller slette poster i tabeller som er registrert for hvert objekt i listen over registrerte. Se trinn 7 i "Opprette eller endre tillatelsessett manuelt".

### <a name="example---indirect-permission"></a>Eksempel - indirekte tillatelse
Du kan tilordne en indirekte tillatelse til å bruke et objekt, bare via et annet objekt.
En bruker kan for eksempel ha tillatelse til å kjøre kodeenhet 80, **Sales-Post**. Kodeenheten **Sales-Post** utfører mange oppgaver, inkludert å endre tabell 37, **salgslinjen**. Når du bokfører et salgsdokument, **Sales-Post**-kodeenheten, kontrollerer [!INCLUDE[d365fin](includes/d365fin_md.md)] om brukeren har tillatelse til å endre **Salgslinje**-tabellen. Hvis ikke kan ikke kodeenheten fullføre oppgavene, og brukeren får en feilmelding. Hvis dette er tilfelle, kjører kodeenheten uten problemer.

Brukeren trenger imidlertid ikke full tilgang til tabellen **Salgslinje** for å kunne kjøre kodeenheten. Hvis brukeren har indirekte tillatelse til **Salgslinje**-tabellen, kjører kodeenheten **Sales-Post** uten problemer. Når en bruker har indirekte tillatelse, kan vedkommende bare endre tabellen **Salgslinje** ved å kjøre kodeenheten **Sales-Post** eller et annet objekt som har tillatelse til å endre tabellen **Salgslinje**. Brukeren kan bare endre **Salgslinje**-tabellen når det gjøres fra moduler som støttes. Brukeren kan ikke kjøre funksjonen ved en feiltakelse eller med onde hensikter ved hjelp av andre metoder.

## <a name="to-set-up-user-time-constraints"></a>Slik definerer du tidsbegrensninger for brukere:
Administratorer kan definere hvor lenge angitte brukere skal kunne bokføre, og også angi om systemet skal logge hvor lenge brukere er logget på. Administratorer kan også tilordne ansvarssentre til brukere.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Brukeroppsett**, og velg deretter den relaterte koblingen.
2. I vinduet **Brukeroppsett** velger du handlingen **Ny**.
3. I feltet **Bruker-ID** angir du ID-en for en bruker eller velger feltet for å vise alle gjeldende Windows-brukere i systemet.
4. Fyll ut feltene etter behov.

## <a name="see-also"></a>Se også
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Oppsett og administrasjon i Dynamics 365 for Financials](admin-setup-and-administration.md)  
[Velkommen til [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

