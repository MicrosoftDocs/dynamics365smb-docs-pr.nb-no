---
title: Opprette et prosjektkort for et prosjekt og angi oppgaver
description: For et nytt prosjekt oppretter du et prosjektkort som inneholder prosjektoppgaver og planleggingslinjer, slik at det blir enklere å administrere fremdrift og budsjett.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management, task
ms.search.form: 88, 1001, 1002, 1003, 1004, 1005, 1006, 1007
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 88da1794619da0fce6001d70482a021d8efbe8cf
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973313"
---
# <a name="create-jobs"></a>Opprette prosjekter
Når du starter et nytt prosjekt, må du opprette et prosjektkort med integrerte prosjektoppgaver og prosjektplanleggingslinjer, strukturert i to lag.  

Det første laget består av prosjektoppgaver. Du må opprette minst én prosjektoppgave per prosjekt fordi all postering refererer til en prosjektoppgave. Ved å ha minst én prosjektoppgave i prosjektet kan du definere planleggingslinjer og bokføre forbruket i prosjektet.

Det andre laget består av prosjektplanleggingslinjer, som angir den detaljerte bruken av ressurser, varer og ulike finansutgifter.

Lagstrukturen gjør det mulig å dele prosjektet inn i mindre oppgaver, slik at du kan bruke mer spesifikke detaljer i budsjettering, tilbud og registrering. I tillegg gir den deg innsikt i hvordan et prosjekt pågår. Du kan for eksempel spore om du innfrir angitte milepæler, eller er på vei til å innfri budsjettforventningene.

> [!TIP]
> Velg **Nytt prosjekt**-handlingen i rollesenteret **Prosjektleder** for å starte en assistert oppsettveiledning som veileder deg gjennom trinnene for å opprette et prosjekt med integrerte oppgaver og planleggingslinjer. Følgende prosedyre beskriver hvordan du utfører trinnene manuelt. For et eksempel på hvordan du oppretter et prosjekt manuelt, kan du se [Video: Opprette et prosjekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

## <a name="to-create-a-job-card"></a>Slik oppretter du et prosjektkort
Du oppretter et prosjektkort og deretter prosjektoppgavelinjer og prosjektplanleggingslinjer for prosjektet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil angi prosjektet med informasjon om andre prosjekter, kan du velge handlingen **Kopier prosjekt**, fylle ut feltene etter behov, og deretter velge **OK**-knappen.

> [!NOTE]  
>   Hvis du bruker timelister for prosjektet, må du også angi en person med ansvar for disse. Denne personen kan godkjenne timelister for ansattoppgavene som er knyttet til jobben. Hvis du vil ha mer informasjon, kan du se [Definere timelister](projects-how-setup-time-sheets.md).

## <a name="to-create-tasks-for-a-job"></a>Slik oppretter du oppgaver for et prosjekt:
En viktig del av å opprette et prosjekt er å angi de ulike oppgavene i prosjektet. Dette gjør du ved å legge til nye linjer i hurtigfanen **Oppgaver** på siden **Prosjektkort** med én oppgave per linje. Hvert prosjekt må ha minst én oppgave.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.
2. Åpne prosjektkortet for det aktuelle prosjektet.
3. På hurtigfanen **Oppgaver** fyller du ut feltene etter behov på en ny linje.
4. Hvis du vil rykke inn oppgaver og opprette et hierarki, velger du handlingen **Oppgaver**, og deretter velger du handlingen **Rykk inn prosjektoppgaver**.
5. Gjenta trinn 3 og 4 for alle oppgavene som er nødvendige for prosjektet.
6. Hvis du vil angi prosjektoppgavene med informasjon om andre prosjektoppgaver, kan du velge handlingen **Kopier prosjektoppgaver fra**, fylle ut feltene etter behov, og deretter velge **OK**-knappen.

## <a name="to-create-planning-lines-for-a-job"></a>Slik oppretter du planleggingslinjer for et prosjekt
Du kan tilpasse dine nye prosjektoppgaver på prosjektplanleggingslinjer. En planleggingslinje kan brukes til å registrere informasjon du vil spore for et prosjekt. Du kan bruke planleggingslinjer til å legge til informasjon, for eksempel hvilke ressurser som kreves, eller til å registrere hvilke varer som trengs for å utføre prosjektet. Du kan for eksempel opprette en oppgave for å innhente kundens godkjenning for et prosjekt. Denne oppgaven kan du knytte til planleggingslinjer for varer eller andre elementer, for eksempel møter med kunden og tilordning av en ressurs.  

En prosjektplanleggingslinje kan være én av følgende typer.  

| Type | Beskrivelse |
| --- | --- |
| **Budsjett** |Angir beregnet forbruk og kost for prosjektet, vanligvis i et prosjekt basert på tid og materialer. Planleggingslinjer av denne typen kan ikke faktureres. |
| **Fakturerbar** |Angir beregnet fakturering av kunden, vanligvis i et prosjekt basert på fast pris. |
| **Både Budsjett og Fakturerbar** |Angir budsjettert forbruk lik det som skal faktureres. |

**Merk**. Etter hvert som du angir informasjon på prosjektplanleggingslinjer, fylles kostinformasjon automatisk ut. Kost, pris og rabatt for ressurser og varer er i utgangspunktet basert på for eksempel informasjonen som er definert på ressurs- og varekortene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.
2. Åpne et aktuelt prosjektkort.
3. Velg en prosjektoppgave der feltet **Prosjektoppgavetype** inneholder **Bokføring**, og velg deretter handlingen **Prosjektplanleggingslinjer**.  
4. På siden **Prosjektplanleggingslinjer** på en ny linje fyller du ut feltene etter behov.
5. Gjenta trinn 3 og 4 for alle planleggingslinjene du trenger for prosjektoppgaven.

## <a name="see-also"></a>Se også

[Prosjektstyring](projects-manage-projects.md)  
[Video: Opprette et prosjekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]