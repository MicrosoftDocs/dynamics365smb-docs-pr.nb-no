---
title: Gjennomgang – Planlegge forsyninger manuelt | Microsoft-dokumentasjon
description: Denne gjennomgangen viser hvordan du planlegger forsyningsordrer for å dekke nytt behov. Du kan sette i gang forsyningsplanlegging med jevne mellomrom, for eksempel hver morgen eller hver mandag, eller når du blir varslet av salg eller produksjon, avhengig av behovstypen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c1ab3c48ae09b75ab9e54e0c9fe9afd49b833f09
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214681"
---
# <a name="walkthrough-planning-supplies-manually"></a>Gjennomgang: planlegge forsyninger manuelt

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Denne gjennomgangen viser hvordan du planlegger forsyningsordrer for å dekke nytt behov. Du kan sette i gang forsyningsplanlegging med jevne mellomrom, for eksempel hver morgen eller hver mandag, eller når du blir varslet av salg eller produksjon, avhengig av behovstypen. I denne gjennomgangen skal du bruke siden **Ordreplanlegging**, som er et enkelt verktøy for forsyningsplanlegging som er basert på manuell beslutningstaking i stedet for parameterbasert automatisk planlegging.  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen  
 Denne gjennomgangen tar for seg følgende oppgaver:  

-   Planlegging av en bestilling for produksjonskomponenter  
-   Planlegging av en overføringsordre for å dekke salgsbehov  
-   Planlegging av en produksjonsordre for en vare med flere nivåer  

## <a name="roles"></a>Roller  
 Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:  

-   Produksjonsplanlegger  
-   Innkjøper  
-   Ordrebehandler  

## <a name="prerequisites"></a>Forutsetninger  
 Før du begynner med denne gjennomgangen, må du installere [!INCLUDE[prod_short](includes/prod_short.md)]. Du må gjøre følgende endringer i databasen:  

-   Slett alle eksisterende ordrer for sykler.  
-   Opprett én ordre for ti sykler i ØST.  
-   Slett alle planlagte og fast planlagte produksjonsordrer. Ikke slett påbegynte ordrer med poster som allerede er bokført.  

 Som en regel bruker du de foreslåtte dataene i denne gjennomgangen siden disse dataene har de nødvendige postene.  

## <a name="story"></a>Hovedscenario  
 Martin, produksjonsplanleggeren i et lite produksjonsselskap, er i ferd med å planlegge produksjon og bestillinger for å dekke nytt salgsbehov.  

 Siden produktene har få stykklistenivåer og ordreflyten er relativt lav, bruker Martin siden **Ordreplanlegging** til å opprette forsyningsordrer manuelt, ett produktnivå om gangen.  

 I et mer sammensatt produksjonsmiljø brukes planleggingsforslaget til å planlegge forsyning basert på vareparametere, for eksempel periode for ny planlegging, sikkerhetsleveringstid, gjenbestillingspunkt og masseberegninger av konsolidert behov fra alle produktnivåer.  

## <a name="setting-up-the-sample-data"></a>Konfigurere eksempeldataene  
 Det standard demonstrasjonsselskapet CRONUS har for tiden et stort behov som ikke er planlagt. I løpet av de ulike planleggingsoppgavene i denne gjennomgangen må du avvike fra den realistiske forretningsflyten ved å ignorere behov med nære forfallsdatoer og i stedet bruke behov med senere forfall.  

## <a name="using-the-order-planning-page"></a>Bruke siden Ordreplanlegging  

Du får tilgang til **Ordreplanlegging**-siden fra flere ulike steder:  

-   Produksjon, Planlegging  
-   Salg og markedsføring, Ordrebehandling  
-   Kjøp, Planlegging  
-   I tillegg kan du åpne denne siden for en bestemt produksjonsordre ved å velge **Planlegging**-handlingen.

### <a name="to-use-the-order-planning-page"></a>Slik bruker du siden Ordreplanlegging:  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillingsplanlegging**, og velg deretter den relaterte koblingen.  

     Når siden **Ordreplanlegging** åpnes for første gang, må en plan beregnes for å vise det nye behovet siden det sist ble beregnet.  

2.  Velg **Beregn plan**-handlingen.  

     Planleggingssystemet analyserer eventuelt nytt behov som er introdusert, for eksempel nye salg, endrede salg eller produksjonsordrer.  

     Antallet som trengs for hver behovslinje, beregnes basert på totalt disponibelt antall. Denne beregningen utføres ordre for ordre. Dette betyr at ordren som inkluderer behovslinjen med den tidligste forfallsdatoen eller forsendelsesdatoen, beregnes først. Etter dette beregnes ytterligere behovslinjer i den samme ordren, uavhengig av forfallsdatoen eller forsendelsesdatoen.  

3.  Kontroller at siden **Ordreplanlegging** er maksimert, og at størrelsen på kolonnefeltene er endret slik at alle standard feltnavn vises.  

     Når beregningen er fullført, vises alt udekket behov som sammenslåtte (skjulte) ordrehodelinjer sortert etter tidligste behovsdato.  

     Legg merke til at CRONUS har flere ordrer med udekket behov. Hver planleggingslinje i fet representerer en ordre eller produksjonsordre, inkludert minst én line med utilstrekkelig disponibelt antall.  

4.  Velg filteret **Alle behov** i feltet **Vis behov som**.  

     Du kan bruke **Behovstype**-feltet til å velge hvilke ordretyper du vil vise.  

     Ordrer uten disponibilitetsproblemer vises ikke. Hvis det ikke finnes noen ordrer når en plan beregnes, får du en melding, og ingen planleggingslinjer vises.  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a>Planlegge en bestilling for å dekke komponentbehov  
 I denne fremgangsmåten oppretter du en bestilling for produksjonskomponenter det er behov for.  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a>Slik planlegger du en bestilling for å dekke et komponentbehov i produksjon:  

1.  Vis den første linjen (velg plussymbolet (+)).  
2.  Velg den første behovslinjen, med vare **LSU-15**, og velg deretter **Vis dokument**-handlingen.  
3.  Lukk den åpnede produksjonsordren for å gå tilbake til siden **Ordreplanlegging**.  
4.  Velg **Kjøp** i feltet **Etterfyllingssystem**.  

     Standardverdien er fra varekortet (eller LFE-kortet), men du kan endre den til ett av følgende alternativer:  

    -   **Kjøp** – for å opprette en bestilling.  
    -   **Overfør** – opprette en overføringsordre.  
    -   **Prod.ordre** – for å opprette en produksjonsordre.  

5.  Velg ett av følgende alternativer i henhold til det valgte etterfyllingssystemet, i **Forsyning fra**-feltet.  

    -   **Leverandør** – for kjøp  
    -   **Lokasjon** – For overføringer  

     Hvis du ikke fyller ut feltet, vises en feilmelding når du prøver å opprette forsyningsordrene.  

    > [!NOTE]  
    >  Hvis komponentene har et standard leverandørnummer angitt på varekortene, blir linjene forhåndsdefinert.  

6.  Velg feltet **Forsyning fra**.  
7.  Velg **Ny**-handlingen på siden **Vare/leverandør-katalog**, og velg deretter leverandør **30000**.  
8.  Velg **OK**-knappen for å gå tilbake til siden **Ordreplanlegging**.  
9. Kopier leverandør **30000** til de andre linjene for høyttalerkomponenter i denne produksjonsordren.  

     Du er nå klar til å opprette en bestilling.  

10. Velg handlingen **Lag bestillinger**. Siden **Lag forsyningsordrer** åpnes.  
11. På hurtigfanen **Ordreplanlegging**, i feltet **Lag ordrer for**, velger du alternativet **den aktive ordren**.  
12. Velg alternativet **Lag bestilling** i feltet **Opprett bestilling** på hurtigfanen **Alternativer**.  
13. Velg **OK**-knappen for å opprette en bestilling for alle komponentene i ordren.  

     Nå opprettes og lagres bestillingene som de siste bestillingene i bestillingsoversikten.  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a>Planlegge en overføringsordre for å dekke salgsbehov  
 I denne fremgangsmåten skal du planlegge for behov fra en ordre. Behovslinjer representerer salgslinjer, ikke komponentlinjer som i produksjonsbehov.  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a>Slik planlegger du en overføringsordre for å dekke salgsbehov:  

1.  Flytt pekeren til planleggingslinjen for ordrenummer **2008**.  
2.  Vis linjen, og flytt pekeren til behovslinjen.  

     Ordrenummer **2008** er for ti høyttalere, varen **LS-120**, som er bestilt av Pedersen Kontorutstyr AS.  

     Definert etterfyllingssystem og standardleverandør for varen vises.  

    > [!NOTE]  
    >  Det er fire informasjonsfelt nederst på siden. I feltet **Tidligste tilgjengelige dato** blir de ti stykkene som trengs, tilgjengelige på en inngående forsyningsordre ni dager senere enn gjeldende forfallsdato. Hvis dette blir for sent for kunden, viser feltet **Tilgjengelig for overføring** at 13 stykker av varen er tilgjengelig på en annen lokasjon. Det er aktuelt å planlegge for denne varebeholdningen.  

3.  Velg feltet **Tilgjengelig for overføring** for å åpne siden **Hent alternativ forsyning**.  
4.  Velg **OK**-knappen for å bestille de ti varene som er tilgjengelige.  

    > [!NOTE]  
    >  På behovslinjen er det foreslåtte kjøpet erstattet med en en overføring fra lokasjonen HOVED. Funksjonen **Lag bestillinger** oppretter en overføringsordre fra HOVED til den etterspurte lokasjonen. **Erstatning finnes**-feltet fungerer på samme måte.  

5.  Velg handlingen **Lag bestillinger**. Siden **Lag forsyningsordrer** åpnes.  
6.  På hurtigfanen **Ordreplanlegging**, i feltet **Lag ordrer for**, velger du alternativet **Den aktive ordren**.  
7.  Velg alternativet **Lag overføringsordrer** i feltet **Opprett overføringsordre** på hurtigfanen **Alternativer**.  
8.  Velg **OK**-knappen for å opprette overføringsordren som skal forsyne ordren.  

     Overføringsordren er nå opprettet og lagret i oversikten som den siste ordren i oversikten over åpne overføringsordrer.  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a>Planlegge en produksjonsordre med flere nivåer for å dekke et salgsbehov  
 I denne fremgangsmåten skal du planlegge å dekke salgsbehov for en produsert vare med flere produktnivåer, der hvert nivå skaper et avhengig produksjonsbehov.  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a>Slik planlegger du produksjon med flere nivåer for å dekke salgsbehov:  

1.  Merk planleggingslinjen med salgsbehov for ordrenummer **1001**, opprettet tidligere som nødvendige data.  

     Denne behovslinjen er en salgslinje, men varen har **Prod.ordre** som definert etterfyllingssystem. Begynn med å legge til en ekstra ringeklokke i komponentbehovet for hver sykkel.  

2.  Velg handlingen **Komponenter** for å åpne **Planleggingskomponenter**-siden.  
3.  På linjen med varen ringeklokke endrer du **Antall per**-feltet fra **1** til **2**.  
4.  Vurder planleggingsalternativene på siden **Ordreplanlegging**. I dette tilfellet har du ingen alternative forsyningsmuligheter, ingen overføring, erstatning eller senere levering. Du må opprette den foreslåtte forsyningsordren – en produksjonsordre.  
5.  Velg **Lag ordre**-handlingen for å opprette produksjonsordren.  

     Legg merke til at planleggingslinjen for ordre **1001** på siden **Ordreplanlegging** ikke lenger finnes, og at det opprinnelige salgsbehovet er dekket.  

6.  Lukk siden **Ordreplanlegging**.  

     Nå kunne du ha valgt å fortsette i denne visningen og fylle ut alle planleggingsoppgavene. I stedet skal du nå ta på deg rollen som produksjonsplanlegger ved å gå til produksjonsordren du nettopp opprettet, og åpne siden **Ordreplanlegging**.  

 Som produksjonsplanlegger må du nå planlegge en bestemt produksjonsordre.  

### <a name="to-plan-a-specific-production-order"></a>Slik planlegger du en bestemt produksjonsordre:  

1.  Åpne produksjonsordren **101001**, for ti sykler, som du nettopp opprettet med funksjonen **Lag bestillinger**.  
2.  Åpne siden **Prod.ordrekomponenter** for å kontrollere at den ekstra ringeklokken gjenspeiles på produksjonsordren.  
3.  Velg handlingen **Planlegging**.  

     Siden **Ordreplanlegging** åpnes i en visning som alltid er filtrert etter bestemte produksjonsbehov. Salgsbehov vises ikke. Du må beregne en plan før du kan vise ytterligere behov.  

4.  Velg **Beregn plan**-handlingen.  

     Legg merke til at fire nye produksjonsordrer vises som ikke-planlagt produksjonsbehov som er hentet fra ordre **101001**. De nye linjene representerer produksjonsbehov fra delmonteringene som må opprettes for å produsere ordren.  

5.  Velg **Utvid alle**-handlingen for å få en oversikt over alt produksjonsbehov for de to produksjonsordrene.  

     For å gi tilleggsinformasjon om behovslinjene kan du legge til feltene **Behovsmengde** og **Disponibel behovsmengde** i visningen.  

     Nå må du forsyne ti av hver komponent.  

     Merk at fire av behovslinjene har Prod.ordre. fra etterfyllingssystemet. Disse fire delmonteringene representerer sykkelens andre produktnivå.  

     Standardinnstillingene for etterfylling er allerede fylt ut, og du kan begynne å lage bestillinger.  

6.  Velg handlingen **Lag bestillinger**.  

     Før du velger **OK**-knappen, må du legge merke til teksten i hurtigfanen **Ordreplanlegging**. Denne teksten er viktig fordi du vet at sykkelen har flere produserte komponenter, delmonteringer, som kan være etterspurt når du oppretter denne produksjonsordren.  

7.  Velg alternativet **Alle linjer** i feltet **Lag ordrer for** på siden **Lag forsyningsordrer**, og klikk deretter **OK** for å opprette produksjonsordrer for det andre produktnivået i ordren.  

     Merk at produksjonsbehovet på øverste nivå for produksjonsordren 101001 ikke lenger finnes. Dette betyr at det er planlagt for det opprinnelige produksjonsbehovet for delmonteringer.  

     På siden **Ordreplanlegging** beregner du en plan på nytt for å planlegge sykkelstrukturen.  

8.  Velg **Beregn plan**-handlingen for å beregne planen på nytt i henhold til instruksjonene i den innebygde hjelpeteksten.  

     De to nye linjene representerer ytterligere produksjonsbehov hentet fra delmonteringene som ble planlagt i forrige trinn. Det blir foreslått at du lager to produksjonsordrer for å forsyne hjulnavene, én for ti fornav og én for ti baknav.  

9. Velg **Utvid alle**-handlingen for å få en oversikt over alt behov for de to produksjonsordrene.  

     Den foreslåtte forsyningsplanen angir at i alt fire bestillinger blir opprettet for komponentene. Du bestemmer deg for å lage de foreslåtte bestillingene.  

10. Velg handlingen **Lag bestillinger**.  
11. Velg alternativet **Alle linjer** i feltet **Lag ordrer for**, og klikk deretter **OK**. Kontroller om det finnes ytterligere behov for produksjonen av den overordnede varen, sykkelen, som selges i ordre 1001.  
12. Velg **Beregn plan**-handlingen.  

     Meldingen angir at alle nødvendige varer nå er forsynt. Kontroller de fast planlagte produksjonsordrene som opprettes.  

13. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Fast planlagte prod.ordrer**, og velg deretter den relaterte koblingen.  

     Se gjennom hvordan start- og sluttidspunkt for individuelle ordrer planlegges i henhold til produktstrukturen, på siden **Fast planlagte prod.ordrer**. Komponentene på laveste nivå produseres først. Derfor må du planlegge ordrer med flere nivåer slik det er demonstrert i denne arbeidsflyten for planlegging.  

## <a name="see-also"></a>Se også  
 [Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]