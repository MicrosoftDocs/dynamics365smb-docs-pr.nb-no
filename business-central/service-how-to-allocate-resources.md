---
title: Tildele ressurser | Microsoft-dokumentasjon
description: Du kan endre årlig beløp i servicekontrakten eller kontrakttilbudet for å rette beløpet som skal faktureres hvert år.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 0238a5fc1799ba78616aeb08aa8d84e089094e6a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195012"
---
# <a name="allocate-resources"></a>Tildele ressurser
Det viktigste elementet innen service er personene som utfører servicen. Du kan definere [!INCLUDE[d365fin](includes/d365fin_md.md)] for å tildele de aktuelle personene til de aktuelle prosjektene. Tilordningen kan være basert på servicesoner der personene befinner seg, eller der servicen skjer. I tillegg kan du samle ressurser i grupper når du svarer på serviceforespørsler. Hvis du vil ha mer informasjon, kan du se [Definere ressurstildeling](service-how-setup-resource-allocation.md).

Du kan tildele ressurser, for eksempel teknikere, ved hjelp av feltet **Servicefordeling** eller fra en serviceordre. Du kan bruke ressursdisponering til å tildele ressurser til å utføre serviceoppgavene i ordrene eller tilbudene.

Du kan tildel den samme ressursen, for eksempel en tekniker eller ressursgruppe, til alle servicevarene i en serviceordre. Fordelingsposter opprettes for de andre servicevarene i ordren med samme ressursnummer og tildelingsdato som linjen du tildelte. De tildelte timene utgjør timene du har tildelt, fordelt på antall servicevarer i ordren. **Status**-feltet settes automatisk til **Aktiv** for alle postene som ble opprettet.

## <a name="to-see-an-overview-of-service-orders-and-service-quotes"></a>Slik får du oversikt over serviceordrer og -tilbud  
Det kan ofte være nødvendig å skaffe seg oversikt over serviceordre eller servicetilbud som oppfyller visse krav, slik at det kan utføres bestemte handlinger på dem, en etter en. Du kan for eksempel bli nødt til å tildele ressurser til serviceordrer som tilhører en bestemt kunde.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicefordeling**, og velg deretter den relaterte koblingen.  
2. I feltet **Dokumentfilter** velger du hvilken type dokument du vil se.
3. Hvis du ønsker en oversikt over dokumenter som har serviceoppgaver som en bestemt ressurs eller ressursgruppe er tildelt til, fyller du ut feltene **Ressursfilter** og **Ressursgruppefilter**, og trykker på Enter.  
4. Hvis du ønsker en oversikt over dokumenter med en bestemt responsdato, eller responsdato innen en bestemt tidsperiode, fyller du ut feltet **Responsdatofilter**, og trykker på **Enter**.  
5. Hvis du vil ha en oversikt over dokumenter med en bestemt tildelings- eller dokumentstatus, fyller du ut feltet **Tildelingsfilter/Statusfilter**, og trykker på **Enter**.  
6. Hvis du vil ha en oversikt over dokumenter som tilhører en bestemt kontrakt, kunde eller sone, fyller du ut feltet **Kontraktfilter/Kundefilter/Sonefilter**, og trykker på **Enter**.  
7. Velg en linje som er knyttet til en serviceordre eller et servicetilbud, og velg deretter handlingen **Vis dokument**.  

    **Serviceordre**- eller **Servicetilbud**-siden åpnes, og du kan arbeide med dokumentet. Hvis du vil gå tilbake til **Servicefordeling**-siden, velger du **OK**.

## <a name="to-allocate-a-resource-using-resource-or-resource-group-availability"></a>Slik tildeler du en ressurs ved hjelp av ressurs eller ressursgruppedisponering    
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicefordeling**, og velg deretter den relaterte koblingen.  
2. Velg serviceordren, og velg deretter handlingen **Ressurstildelinger**.  
3. Velg posten med serviceoppgaven som du vil tildele en ressurs til.  
4. Velg handlingen **Ressursdisponering** eller **Ress.grp.disponering**.  
5. På siden **Disponible ress. (service)** velger du **Vis matrise**.  
6. Velg en ressurs å tildele. Du kan basere utvalget på om ressursen er kompetent til oppgaven, om den holder til i kundesonen, og/eller om den er foretrukket av kunden.  
7. Angi en dato da ressursen har tilstrekkelig med disponible timer for oppgaven, og som er nær i tid til responsdatoen på serviceordren.  
8. I feltet **Ant. som skal tildeles** angir du antall timer ressursen skal tildeles til serviceoppgaven for.  
9. Velg **Tildele**-handlingen for å tildele den valgte ressursen på den valgte datoen.  

     **Status**-feltet settes automatisk til **Aktiv**.  

 Gjenta disse trinnene for hver enkelt dato som du vil tildele ressursen til serviceoppgaven.  

> [!NOTE]  
>  Det kan bare være **aktive** serviceordretildelingsposter med én ressurs eller ressursgruppe om gangen for en servicevare i en serviceordre.  

## <a name="to-allocate-a-resource-using-a-service-order"></a>Slik tildeler du en ressurs med en serviceordre  
Når du har opprettet og fylt ut en serviceordre eller et servicetilbud, kan du tildele ressurser, for eksempel teknikere, som skal utføre serviceoppgaver som er registrert som servicevarelinjer i dokumentet.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Velg serviceordren, og velg deretter **Rediger**.  
3. Velg servicevarelinjen som er knyttet til serviceoppgaven du vil tildele en ressurs til.  
4. Velg **Ressurstildelinger**.
5. På siden **Ressurstildelinger** velger du en tildelingspost som ikke er aktiv, med serviceoppgaven du vil tildele ressursen til. Hvis tildelingsposten ikke finnes, kan du opprette en ny ved å velge **Ny**.  
7. Angi serviceoppgaven ved å fylle ut feltet **Servicevarenr.** på samme linje.  
8. Velg ressursen i **Ressursnr.**-feltet. Hvis ressursen er medlem av en ressursgruppe, angis nummeret på ressursgruppen automatisk i feltet **Ressursgruppenr.**. .  
9. Fyll ut feltene **Tildelingsdato** og **Tildelte timer**. **Status**-feltet settes til **Aktiv**. Dette betyr at ressursen er tildelt til serviceoppgaven.  
10. Hvis du vil tildele ressursen til alle varene, kan du også velge **Tildel til alle servicevarer**.

> [!NOTE]  
>  Det kan bare være aktive tildelingsposter med én ressurs eller ressursgruppe om gangen for en servicevare i en serviceordre.

## <a name="to-reallocate-resources-on-a-service-order"></a>Slik tildeles ressurser på nytt for en serviceordre  
Du kan tildele ressurser på nytt direkte fra en serviceordre eller et servicetilbud mens du arbeider med den/det. Den opprinnelige posten finnes fremdeles, men statusen er oppdatert som følger:  

* Hvis servicen ble startet mens tildelingen var **Aktiv** (det vil si hvis reparasjonsstatusen til servicevaren i posten ble endret til **I arbeid**), endres tildelingsstatusen fra **Ny tildeling nødvendig** til **Ferdig**.  
* Hvis servicen ikke ble startet mens tildelingen var **Aktiv**, endres tildelingsstatusen fra **Ny tildeling nødvendig** til **Avbrutt**.  
* Hvis du tildeler en serviceordre på nytt, som du har konvertert fra et tilbud, endres alltid statusen til fordelingspostene som er registrert for tilbudet, til **Ferdig** når du tildeler servicevarene i serviceordren på nytt.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Åpne den aktuelle serviceordren.  
3. Velg servicevarelinjen som er knyttet til serviceoppgaven du vil tildele en ressurs til, og velg deretter handlingen **Ressurstildelinger**.  
4. På siden **Ressurstildelinger** velger du en tildelingspost med serviceoppgaven du vil tildele ressursen til på nytt. Velg den aktuelle ressursen i **Ressursnr.**-feltet. Dermed overskrives ressursnummeret som allerede finnes i feltet.  
5. Trykk Enter. Det vises en dialogboks med forespørsel om du vil tildele denne posten på nytt. Fyll eventuelt ut **Årsaksspor**-feltet, og velg **Ja**-knappen for å bekrefte den nye tildelingen.  
6. Fyll ut feltene **Tildelingsdato** og **Tildelte timer**. Posten inneholder nå den nye ressursen, og har statusen **Aktiv**.

## <a name="to-reallocate-a-resource-using-the-dispatch-board"></a>Slik tildeler du en ressurs på nytt ved bruk av servicefordeling  
Hvis ressursene som er tildelt til en serviceoppgave, ikke kan fullføre arbeidet, betyr det at denne serviceoppgaven trenger ny tildeling. Vanligvis tildeler du ressurser på nytt til en serviceoppgave med **Servicefordeling**.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicefordeling**, og velg deretter den relaterte koblingen.  
2. I feltet **Tildelingsfilter** velger du **Ny tildeling nødvendig**. Siden **Servicefordeling** viser nå en liste over serviceordrer som omfatter serviceoppgaver som trenger ny tildeling.  
3. Velg den relevatne serviceordren, og velg deretter handlingen **Ressurstildelinger**. **Ressurstildelinger**-siden åpnes.  
4. Velg tildelingsposten med serviceoppgaven som du vil tildele en ressurs til på nytt.  
5. Velg den aktuelle ressursen i **Ressursnr.**-feltet. Dermed overskrives ressursnummeret som allerede finnes i feltet.  
6. Trykk Enter. Dialogboksen **Årsaker til ny tildeling av post** åpnes, der du blir spurt om du vil tildele denne posten på nytt. Fyll eventuelt ut **Årsaksspor**-feltet, og velg **Ja**-knappen for å bekrefte den nye tildelingen.  
7.  Fyll ut feltene **Tildelingsdato** og **Tildelte timer**. Posten inneholder nå den nye ressursen, og har statusen **Aktiv**.  

    > [!NOTE]  
    >  Den gamle posten finnes fremdeles, men oppdateres på følgende måter:  
    >   
    >  * Hvis servicen ble startet mens tildelingen var **Aktiv** (det vil si hvis reparasjonsstatusen til servicevaren i posten ble endret til **I arbeid**), endres tildelingsstatusen fra **Ny tildeling nødvendig** til **Ferdig**.  
    > * Hvis servicen ikke var startet mens tildelingen var **Aktiv**, endres tildelingsstatusen fra **Ny tildeling nødvendig** til **Avbrutt**.  
    > * Hvis du tildeler en serviceordre på nytt, som du har konvertert fra et tilbud, endres alltid statusen til fordelingspostene som er registrert for tilbudet, til **Ferdig** når du tildeler servicevarene i serviceordren på nytt.  

## <a name="to-register-resource-hours"></a>Slik registrerer du ressurstimer  
Når du arbeider med servicevarer i serviceordrer, må du registrere ressurstimene som brukes på servicen. Følgende fremgangsmåte viser hvordan du registrerer ressurstimene på siden **Servicevareskjema**.  

Du kan bruke samme fremgangsmåte til å registrere timene på siden **Servicelinjer**, som du kan åpne fra siden Serviceordre. Åpne det relevante servicekortet, og velg deretter handlingen **Servicelinjer**.  

Hvis den samme ressursen kan brukes på alle servicevarene i serviceordren, kan du registrere samlede ressurstimer for bare én servicevare, og deretter dele ressurslinjen for å tilordne ressurstimene til de andre servicevarene.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceoppgaver**, og velg deretter den relaterte koblingen.
2. Velg linjen som inneholder den aktuelle servicevaren, og velg deretter handlingen **Arbeidsordre**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-resource-to-all-service-items-in-an-order"></a>Slik tildeler du en ressurs til alle servicevarer i en ordre
Hvis den samme ressursen, for eksempel en tekniker, kan brukes på alle servicevarene i serviceordren, kan du registrere samlede ressurstimer for bare én servicevare, og deretter dele ressurslinjen for å fordele ressurstimene på ressurslinjene for de andre servicevarene.  

Følgende fremgangsmåte viser hvordan du deler ressurslinjer på siden **Servicefakturalinjer**.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Åpne den aktuelle serviceordren.  
3. På hurtigfanen **Linjer** velger du handlingen **Servicelinjer**. Siden **Servicelinjer** åpnes.  
4. Velg ressurslinjen du vil dele. Innholdet i feltet **Antall** fordeles mellom alle servicevarene i ordren.  
5. Velg handlingen **Del ressurslinje**. Velg **Ja** for å bekrefte.  

    Ressurslinjer for de andre servicevarene i ordren opprettes med samme ressursnummer som linjen du delte. Antallet er antallet for linjen du deler fordelt på antall servicevarer i ordren.  

## <a name="to-cancel-an-allocation"></a>Slik kansellerer du en tildeling  
Du kan kansellere ressurstildelinger for serviceoppgaver uten å tildele oppgavene på nytt.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicefordeling**, og velg deretter den relaterte koblingen.  
2. Velg serviceordren, og velg deretter handlingen **Ressurstildelinger**.  
3. Velg tildelingsposten med serviceoppgaven som du vil avbryte tildeling for.  
4. Velg handlingen **Kanseller tildeling**.  
5. Velg det aktuelle årsakssporet i feltet **Årsaksspor**.  
6. Velg **Ja** for å bekrefte kanselleringen.  

    > [!NOTE]  
    > Alternativet **Ny tildeling nødvendig** velges automatisk i **Status**-feltet Hvis reparasjonsstatusen til servicevaren i posten er **Første**, endres reparasjonsstatusen til **Henvist**, det vil si at ingen service er påbegynt. Hvis reparasjonsstatusen er **I arbeid**, endres den til **Delvis vedlikeholdt**, det vil si at deler av servicen er fullført.

## <a name="see-also"></a>Se også
[Definere ressurstildeling](service-how-setup-resource-allocation.md)  
[Tildelingsstatus og reparasjonsstatus](service-allocation-status-and-repair-status.md)  
