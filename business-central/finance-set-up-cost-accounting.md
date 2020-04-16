---
title: Definere kostregnskap | Microsoft-dokumentasjon
description: Før du begynner å arbeide med kostregnskap, må du utføre konfigurasjonsprosedyrer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: fc6195457d605da4d1558cf03a9ca4c42408a1d4
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182903"
---
# <a name="setting-up-cost-accounting"></a>Definere kostregnskap
Før du begynner å arbeide med kostregnskap, må du utføre konfigurasjonsprosedyrer.

## <a name="balances-between-cost-type-cost-center-and-cost-object"></a>Balanser mellom kosttype, kostsenter og kostobjekt
Når du definerer kostregnskap, må du kontrollere at alle poster tilordnes en kosttype i tillegg til et kostsenter eller et kostobjekt. Dette betyr at hver kostpost må ha en kosttype tilordnet og en kostsenterkode eller et kostobjekt tilordnet. Denne regelen sikrer at hver kostpost vises i kostsentrene eller kostobjektene, men aldri på begge steder.  

Ved å gjøre dette oppretter du følgende regnskapsformel:  

*Kosttypesaldo* = *Kostsentersaldo* + *Kostobjektsaldo*  

Når du skriver ut rapporter for oversikten over kosttyper, diagrammet med kostsentre og diagrammet med kostobjekter, kan du analysere dette forholdet.

## <a name="setting-up-cost-types"></a>Definere kosttyper
Diagrammet med kosttyper ligner på kontoplanen i finans. Du kan definere diagrammet med kosttyper på følgende måter:  

-   Strukturen i oversikten over kosttyper ligner på resultatregnskapskontiene i finanskontoplanen. Du kan deretter overføre finanskontoplanen til diagrammet med kosttyper. Du kan foreta alle nødvendige justeringer etter overføringen.  
-   Opprett et nytt kosttypediagram, eller legg til nye kosttyper i det eksisterende kosttypediagrammet. Du må opprette hver enkelt nye kosttype individuelt.  

### <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Slik overfører du finanskontoplanen til diagrammet med kosttyper:  
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Diagram med kosttyper**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Hent kosttyper fra kontoplan**. Klikk **Ja**-knappen i dialogboksen for å bekrefte overføringen. Funksjonen bruker kontoplanen til å opprette et diagram med kosttyper.  

    Diagrammet over kostnadstypene inneholder nå alle resultatkontiene i finans og inkluderer overskrifter og delsummer. Du kan endre diagrammet med kosttyper etter behov. Du kan for eksempel slette eksisterende kosttypeduplikater.  

    > [!IMPORTANT]  
    >  Funksjonen **Registrer kosttyper i kontoplan** oppdaterer forholdet mellom kontoplanen og oversikten over kosttyper. **Nr.** -feltet er fylt ut og bekreftet for å forsikre at hver finanskonto er relatert til bare én kostnadstype. Funksjonen kjøres automatisk før overføring av finansposter til kostregnskap.  

### <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Slik definerer du nye kosttyper på siden Diagram med kosttyper:  
1.  Åpne siden **Diagram med kosttyper** i redigeringsmodus.  
2.  Fyll ut feltene som beskrevet etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Du kan definere og vedlikeholde kostnadstyper på siden **Kosttypekort** eller **Diagram med kosttyper**. I denne fremgangsmåten definerer du nye kosttyper på siden **Diagram med kosttyper**.

3.  Når du har opprettet alle kosttyper, velger du **Rykk inn kosttyper**. Klikk **Ja**-knappen i dialogboksen.  
4.  Koble nye kosttypen til den tilsvarende kontoen i finans.  

    > [!IMPORTANT]  
    >  Hvis du har angitt definisjoner i feltene **Sammentelling** for linjetypen **Til-sum** før du kjører funksjonen **Rykk inn kosttyper**, må du angi definisjonene på nytt fordi funksjonen overskriver verdiene i alle **Til-sum**-felt.  

### <a name="to-update-cost-types"></a>Slik oppdaterer du kosttyper:  
1.  Velg på siden **Kostregnskapsoppsett** hvis du vil at diagrammet med kosttypene skal oppdateres automatisk når kontoplanen endres.  
2.  I feltet **Juster finanskonto** kan du velge blant følgende alternativer:  

- **Ingen justering** – Det gjøres ingen tilsvarende endring i diagrammet med kosttyper når du endrer kontoplanen.  
- **Automatisk** – en tilsvarende endring blir utført i diagrammet for kosttyper når du endrer kontoplanen.  
- **Spør** - Det vises en melding med spørsmål om du vil gjøre tilsvarende endring i diagrammet med kosttyper når du endrer kontoplanen.

## <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definere forholdet mellom kostnadstyper og finanskontoer
Forholdet mellom kosttypen og finanskontoen opprettes i kosttypen og finanskontoen.  

* Feltet **Finanskto. fra/til** i **Kosttype**-tabellen angir hvilke finanskontoer som tilhører en kostnadstype.  
* Feltet **Kosttypenr.** i kontoplanen angir hvilken kostnadstype en finanskontoer tilhører.  

Disse to feltene er automatisk utfylt når du bruker funksjonen **Hent kosttyper fra kontoplan**.  

### <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Forhold mellom finanskontoer og kostnadstyper  
Det er et n:1-forhold mellom finanskonti og kosttyper. Flere finanskontoer kan tilhøre én kosttype, men hver finanskonto tilhører bare én kosttype. Tabellen nedenfor beskriver detaljene om forholdet.  

|Forbindelser|**Finanskto. fra/til**|**Kosttypenr.**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Én finanskonto for hver kosttype|Én finanskonto|En kosttype|  
|Flere finanskontoer for én kosttype.|Finanskontoområdet, for eksempel 7110–7193 for hver finanskonto|For hver finanskonto i området er det bare én kosttype|  
|Kosttyper uten tilsvarende finanskontoer|<Empty>||  
|Finanskonti der poster ikke overføres||<Empty>|  

### <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Kosttyper uten en relasjon til finans  
En kostnadstype kan ikke ha en relasjon til finanskontoer hvis én av følgende betingelser er oppfylt:  

* Kontoer for driftsregnskap, for eksempel beregnede renter og avskrivning, tar bare kostnader fra driftsregnskapet.  
* Hjelpekosttyper, for eksempel kosttypene 9901, 9902 og 9903 i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen, brukes som kredit- og debetkontoer for fordelinger.  
* Hjelpekontoen, 9920 i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen, inneholder faktiske avsetninger som viser differansen mellom kost og utgiftene fra Finans.

## <a name="setting-up-cost-centers"></a>Definere kostsentre
Kostsentre er avdelinger som er ansvarlig for kostnader og inntekter. Diagrammet med kostsentre ligner dimensjonsinformasjonen for finans. Du kan definere diagrammet med kostsentre på følgende måter:  

-   Overfør dimensjonsverdier i finans til diagrammet med kostsentre. Du kan foreta alle nødvendige justeringer etter overføringen.  
-   Opprett et nytt kostsenterdiagram som er uavhengig av finans, eller legg til et nytt kostsenter i et eksisterende kostsenterdiagram. Du må opprette hvert enkelt kostsenter individuelt.  

### <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Slik overfører du dimensjonsverdier i finans til diagrammet med kostsentre:  
1.  Angi en dimensjon som kostsenterdimensjon på siden **Oppdater kostregnskapsdimensjoner**. Det er bare verdier fra denne dimensjonen som overføres.  
2.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Diagram med kostsentre**, og velg deretter den relaterte koblingen.  
3.  I fanebladet **Handlinger**, under **Funksjoner** velger du **Hent kostsentre fra dimensjon** for å overføre dimensjonsverdier til kostsenterdiagrammet. Funksjonen overfører dimensjonsverdiene som du definerte i trinn 1.  

    > [!NOTE]  
    >  Du kan konfigurere feltet **Juster kostsenterdimensjon** slik at det definerer en enveissynkronisering av dimensjonsverdier fra finans til diagrammet med kostsentre. Du kan ikke definere en synkronisering av diagrammet med kostsentre til dimensjonsverdier fra finans.  

Diagrammet med kostsentre inneholder nå alle angitte dimensjonsverdier fra finans og inkluderer titler og delsummer.  

### <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a>Slik oppretter du nye kostsentre på siden Diagram med kostsentre:  
Du kan definere og vedlikeholde kostsentre i kortet **Kostsenterkort** eller på siden **Diagram med kostsentre**. I denne fremgangsmåten definerer sentre på siden **Diagram med kostsentre**.  

1. Åpne siden **Diagram med kostsentre** i redigeringsmodus.  
2. Angi kostsenterkoden i **Kode**-feltet. Alle kostsentre må ha en kode.  
3. Skriv inn navnet på kostsenteret i **Navn**-feltet.  
4. Velg rullegardinpilen i feltet **Linjetype** for å angi formålet med kostsenteret.  

    - For kostsentre av typen **Sum** må du fylle ut feltet **Sammentelling**. Bruk **eller**-operatoren, som er en loddrett linje (**&#124;**), til å angi områder for kostsentre.  
    - Når det gjelder kostsentre av linjetypen **Til-sum**, fylles dette feltet ut automatisk når du bruker innrykksfunksjonen.  
5.  Fyll ut feltene **Sorteringsrekkefølge** og **Kostundertype**.  
6.  Velg den neste tomme linjen for å opprette et nytt kostsenter, og gjenta deretter trinn 2 til 5.  
7.  Når du har definert alle kostsentrene, velger du **Rykk inn kostsentre**. Velg **Ja**-knappen.  

> [!IMPORTANT]  
>  Hvis du har angitt definisjoner i **Sammentelling**-feltene for **Til-sum**-kostsentre før du kjører innrykksfunksjonen, må du angi dem på nytt. Funksjonen overskriver verdiene i alle **Til-sum**-felt.

## <a name="setting-up-cost-objects"></a>Definere kostobjekter
Kostobjekter er et selskaps prosjekter, produkter eller tjenester. Diagrammet med kostobjekter ligner dimensjonsinformasjonen for finans. Du kan definere diagrammet med kostobjekter på følgende måter:  

* Overfør dimensjonsverdier i finans til diagrammet med kostobjekter. Du kan foreta alle nødvendige justeringer etter overføringen.  
* Opprett et nytt kostobjektdiagram som er uavhengig av finans, eller legg til et nytt kostobjekt i et eksisterende kostobjektdiagram. Du må opprette hvert enkelt kostobjekt individuelt.  

### <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Slik overfører du dimensjonsverdier fra finans til diagrammet med kostobjekter:  
1.  Angi en dimensjon som kostobjektdimensjon på siden **Oppdatere KR-dimensjoner**. Det er bare verdier fra denne dimensjonen som overføres.  
2.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Diagram med kostobjekter**, og velg deretter den relaterte koblingen.  
3.  Velg **Hent kostobjekter fra dimensjon** for å overføre dimensjonsverdier til kostobjektdiagrammet. Funksjonen overfører dimensjonsverdiene som du definerte i trinn 1.  

    > [!NOTE]  
    >  Du kan konfigurere feltet **Juster kostobjektdimensjon** slik at det definerer en enveissynkronisering av dimensjonsverdier fra finans til diagrammet med kostobjekter. Du kan ikke definere en synkronisering av diagrammet med kostobjekter til dimensjonsverdier fra finans.  

Diagrammet med kostobjektene inneholder nå alle angitte dimensjonsverdier fra finans og inkluderer titler og delsummer.  

### <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Slik oppretter du nye kostobjekter på siden Diagram med kostobjekter:  
Du kan definere og vedlikeholde kostobjekter i kortet **Kostobjektkort** eller siden **Diagram med kostobjekter**. I denne fremgangsmåten definerer objekter på siden **Diagram med kostobjekter**.  

1.  Åpne siden **Diagram med kostobjekter** i redigeringsmodus.  
2.  Angi kostobjektkoden i **Kode**-feltet. Alle kostobjekter må ha en kode.  
3.  Skriv inn kostobjektnavnet i **Navn**-feltet.  
4.  Velg rullegardinpilen i feltet **Linjetype** for å angi formålet med kostobjektet.  

    * Når det gjelder kostobjekter av linjetypen **Sum**, må du fylle ut feltet **Total fra/til**. Bruk **eller**-operatoren, som er en loddrett linje (**&#124;**), til å angi områder for kostobjekter.  
    * Når det gjelder kostobjekter av linjetypen **Til-sum**, fylles dette feltet ut automatisk når du bruker innrykksfunksjonen.  
5.  Fyll ut feltet **Sorteringsrekkefølge**.  
6.  Velg den neste tomme linjen for å opprette et nytt kostobjekt, og gjenta deretter trinn 2 til 5.  
7.  Når du har definert alle kostsentrene, velger du **Rykk inn kostobjekter**. Velg **Ja**-knappen.  

> [!IMPORTANT]  
>  Hvis du har angitt definisjoner i feltene **Total fra/til** for **Til-sum**-kostobjekter før du kjører innrykksfunksjonen, må du angi dem på nytt. Funksjonen overskriver verdiene i alle **Til-sum**-felt.

## <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definere kostsentre og kostobjekter for kontoplanen
Du kan automatisk overføre utgifts- og inntektspostene fra finans til kostregnskap enten for hver finansbokføring eller sammen med en kjørsel. Når du foretar overføringen, overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] bare postene som allerede er koblet til et kostsenter eller et kostobjekt. Hvis du vil opprette en meningsfull overføring, må du kontrollere at kostsentre og kostobjekter er riktig definert.  

### <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Definere standard dimensjonsverdier for finanskontoer  
For hver finanskonto kan du definere standarddimensjonsverdier i **Standarddimensjon**-tabellen. Eksempelet nedenfor viser hvordan du definerer at det alltid skal finnes et kostsenter for AVDELING, men aldri et kostobjekt for PROSJEKT, ved bokføring til en finanskonto.  

|**Dimensjonskode**|**Verdibokføring**|  
|------------------------------------------|-----------------------------------------|  
|Avdeling|Obligatorisk kode|  
|Prosjekt|Ingen kode|  

### <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definere dimensjonsverdier for indirekte kostnader og direkte kostnader  
 Du kan overføre indirekte kostnader til et kostsenter og direkte kostnader til et kostobjekt. Følgende tabell viser den optimale kombinasjonen av dimensjonsoppsettsverdier.  

|Overfør til|Kostsenterbokføring|Bokføring av kostobjekt|  
|-----------------|-------------------------|-------------------------|  
|Kostsenter|Obligatorisk kode|Ingen kode|  
|Kostobjekt|Ingen kode|Obligatorisk kode|  

> [!NOTE]  
>  For å sørge for at det forhåndsdefinerte kostsenteret og kostobjekt som du setter opp i finans, overføres automatisk til kostregnskapet, kan du merke av for **Kontroller finansbokføringer** på siden Kostregnskapsoppsett.

## <a name="see-also"></a>Se også  
[Gjøre rede for kostnader](finance-manage-cost-accounting.md)  
[Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md)   
[Definere og fordele kostnader](finance-define-and-allocate-costs.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
