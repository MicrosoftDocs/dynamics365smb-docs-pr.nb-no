---
title: Opprette et prosjektkort for et prosjekt og angi oppgaver
description: 'For et nytt prosjekt oppretter du et prosjektkort som inneholder prosjektoppgaver og planleggingslinjer, slik at det blir enklere å administrere fremdrift og budsjett.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/03/2022
ms.author: bholtorf
---
# <a name="create-jobs"></a>Opprette prosjekter

Når du starter et nytt prosjekt, må du opprette et prosjektkort med integrerte prosjektoppgaver og prosjektplanleggingslinjer, strukturert i to lag.  

Det første laget består av prosjektoppgaver. Du må opprette minst én prosjektoppgave per prosjekt fordi all postering refererer til en prosjektoppgave. Ved å ha minst én prosjektoppgave i prosjektet kan du definere planleggingslinjer og bokføre forbruket i prosjektet.

Det andre laget består av prosjektplanleggingslinjer, som angir den detaljerte bruken av ressurser, varer og ulike finansutgifter.

Lagstrukturen gjør det mulig å dele prosjektet inn i mindre oppgaver, slik at du kan bruke mer spesifikke detaljer i budsjettering, tilbud og registrering. I tillegg gir den deg innsikt i hvordan et prosjekt pågår. Du kan for eksempel spore om du innfrir angitte milepæler, eller er på vei til å innfri budsjettforventningene.

> [!TIP]
> Velg **Nytt prosjekt**-handlingen i rollesenteret **Prosjektleder** for å starte en assistert oppsettveiledning som veileder deg gjennom trinnene for å opprette et prosjekt med integrerte oppgaver og planleggingslinjer. Følgende prosedyre beskriver hvordan du utfører trinnene manuelt. For et eksempel på hvordan du oppretter et prosjekt manuelt, kan du se [Video: Opprette et prosjekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

Av og til er det en del av den som mottar en tjeneste, forskjellig fra parten som betaler regningen. På **Prosjekter**-siden kan du angi kunden som skal dra nytte av prosjektet i **Salg til**-feltene, og parten til å fakturere i **Faktura til**-feltene. Du kan også angi følgende informasjon: 

* Hvor arbeidet vil skje ved å velge fra en liste over lever til-adresser for kunden.
* Legg til informasjon om eksterne referanser for å forenkle kommunikasjon med prosjektet.
* Overskriv standard regnskapsbetingelsene for prosjektet.

## <a name="to-create-a-job-card"></a>Slik oppretter du et prosjektkort

Du oppretter et prosjektkort og deretter prosjektoppgavelinjer og prosjektplanleggingslinjer for prosjektet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil angi prosjektet med informasjon om andre prosjekter, kan du velge handlingen **Kopier prosjekt**, fylle ut feltene etter behov, og deretter velge **OK**-knappen.

> [!NOTE]  
> Hvis du bruker timelister for prosjektet, må du også angi en person med ansvar for disse. Denne personen kan godkjenne timelister for ansattoppgavene som er knyttet til jobben. Hvis du vil ha mer informasjon, kan du se [Definer timelister](projects-how-setup-time-sheets.md).

Du kan eventuelt merke handlinger på prosjektet som sperret, ved hjelp av feltet **Sperret**. tabellen nedenfor beskriver effekten av alternativene for dette feltet.

|Alternativ  |Description  |
|---------|---------|
|Tom |Alle handlinger er tillatt.|
|Bokføring    |Du kan arbeide med planleggingslinjer, men prosjektet er sperret for bokføring. Hvis du velger dette alternativet, kan du ikke bokføre forbruk eller salg i prosjektet.|
|Alle  |Alle handlinger er sperret.|

## <a name="to-create-tasks-for-a-job"></a>Slik oppretter du oppgaver for et prosjekt:

En viktig del av å opprette et prosjekt er å angi de ulike oppgavene i prosjektet. Du angir oppgaver ved å opprette én linje per oppgave på hurtigfanen **Oppgaver** på siden **Prosjektkort**. Hvert prosjekt må ha minst én oppgave.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.
2. Åpne prosjektkortet for det aktuelle prosjektet.
3. På hurtigfanen **Oppgaver** fyller du ut feltene etter behov på en ny linje.
4. Hvis du vil rykke inn oppgaver og opprette et hierarki, velger du handlingen **Oppgaver**, og deretter velger du handlingen **Rykk inn prosjektoppgaver**.
5. Gjenta trinn 3 og 4 for alle oppgavene som er nødvendige for prosjektet.
6. Hvis du vil angi prosjektoppgavene med informasjon om andre prosjektoppgaver, kan du velge handlingen **Kopier prosjektoppgaver fra**, fylle ut feltene etter behov, og deretter velge **OK**-knappen.

## <a name="to-create-planning-lines-for-a-job"></a>Slik oppretter du planleggingslinjer for et prosjekt

Du kan tilpasse dine nye prosjektoppgaver på prosjektplanleggingslinjer. En planleggingslinje kan registrere informasjonen du vil spore for et prosjekt. Du kan for eksempel spore hvilke ressurser jobben krever, eller hvilke varer som er nødvendige. Du har for eksempel en oppgave å få en kunde til å godkjenne en jobb. Du knytter oppgaven til planleggingslinjer for varer eller andre elementer, for eksempel møter med kunden og tildeling av en ressurs.  

En prosjektplanleggingslinje kan være én av følgende typer.  

| Type | Beskrivelse |
| --- | --- |
| **Budsjett** |Angir beregnet forbruk og kost for prosjektet, vanligvis i et prosjekt basert på tid og materialer. Planleggingslinjer av denne typen kan ikke faktureres. |
| **Fakturerbar** |Angir beregnet fakturering av kunden, vanligvis i et prosjekt basert på fast pris. |
| **Både Budsjett og Fakturerbar** |Angir budsjettert forbruk lik det som skal faktureres. |

> [!NOTE]
> Mens du angir informasjon på prosjektplanleggingslinjer, fylles kostinformasjon automatisk ut. Kost, pris og rabatt for ressurser og varer er basert på for eksempel informasjonen som er definert fra ressurs- og varekortene. 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.
2. Åpne et aktuelt prosjektkort.
3. Velg en prosjektoppgave der feltet **Prosjektoppgavetype** inneholder **Bokføring**, og velg deretter handlingen **Prosjektplanleggingslinjer**.  
4. På siden **Prosjektplanleggingslinjer** på en ny linje fyller du ut feltene etter behov.
5. Gjenta trinn 3 og 4 for alle planleggingslinjene du trenger for prosjektoppgaven.

## <a name="see-also"></a>Se også

[Prosjektstyring](projects-manage-projects.md)  
[Video: Opprett et prosjekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
