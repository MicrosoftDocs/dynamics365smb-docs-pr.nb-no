---
title: 'Mottak, plassering, plukk og levering i grunnleggende lageroppsett'
description: 'I Business Central kan de utgående prosessene utføres på ulike måter, avhengig av kompleksitetsnivået til lageret.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-basic-warehouse-configurations"></a>Gjennomgang av inngående og utgående flyt i grunnleggende lageroppsett

Denne gjennomgangen vis hvordan du fullfører inngående og utgående flyter i konfigurasjonen Grunnleggende: ordre for ordre Hvis du vil ha mer informasjon, kan du se [Oversikt over ulike konfigurasjonsalternativer](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Forutsetninger
Hvis du vil fullføre denne gjennomgangen, må du gjøre deg til lageransatt på lokasjonen *SØLV* ved å følge disse trinnene:  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageransatte**, og velg deretter den relaterte koblingen.  
2. Velg feltet **Bruker-ID**, og velg din egen brukerkonto på siden **Brukere**.  
3. Skriv inn *SØLV* i feltet **Lokasjonskode**.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Inngående flyt: Mottak og plassering i grunnleggende lageroppsett

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan de inngående prosessene for mottak og plassering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.  

|Prinsipp|Inngående prosess|Hyller|Mottak|Plassering|Kompleksitetsnivå (se [Designdetaljer: Lageroppsett](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokføre mottak og plassering fra ordrelinjen|X|||2|  
|B|Bokføre mottak og plassering fra et lagerplasseringsdokument|||X|3|  
|L|Bokføre mottak og plassering fra et lagermottaksdokument||X||4/5/6|  
|D|Bokføre mottak fra et lagermottaksdokument og bokføre plassering fra et lagerplasseringsdokument||X|X|4/5/6|  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Inngående lagerflyt](../../design-details-inbound-warehouse-flow.md).  

Følgende gjennomgangen demonstrerer metoden B i forrige tabell.  

### <a name="scenario"></a>Scenario
Innkjøperen Alicia oppretter en bestilling for ulike brente bønner. Når leveringen ankommer til lageret, plasserer lagermedarbeideren John varene i egnede hyller. Når John bokfører plasseringen, bokføres varene som mottatt på lager og er tilgjengelige for salg eller annet behov.  

### <a name="steps"></a>Trinn
1. Definer siden **Lokasjonskort** for å definere selskapets inngående lagerflyter.  

    1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 2.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
    2.  Åpne lokasjonskortet *SØLV*.  
    3.  Merk av for **Plassering nødv.**.  

2. Definer en standardhylle for varen for å styre hvor den plasseres

    1.  Velg **Hyller**-handlingen på **lokasjonskortet**
    2.  Merk den første raden, hylle *S-1-01*, og velg **Innhold**.  
    3.  Velg handlingen **Ny**.  
    4.  Velg feltene **Fast** og **Standard**.  
    5.  Angi **WRB-1000** i feltet *Varenr.*.  

3. Opprett bestillingen, som er den vanligste typen inngående kildedokument.  

    1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.  
    2.  Velg handlingen **Ny**.  
    3.  Opprett en bestilling for leverandør 10000 med følgende bestillingslinjer. Bruk verktøyene for tilpassing hvis feltet **Hyllekode** ikke er synlig. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](../../ui-personalization-user.md). 

    |Vare|Lokasjonskode|Hyllekode|Antall|  
    |----------|----------|---------|--------------|  
    |WRB-1000|SØLV|S-1-01|20|  
    |WRB-1001|SØLV||30|

    Hyllekoden i den første fylles opp i henhold til oppsett. Hyllekoden for den andre varen er tom, fordi den ikke har standardverdier. Behold det slik.  

    4.  Velg handlingen **Frigi** for å varsle lageret om at bestillingen er klar for håndtering av lageret når leveringen ankommer.  

4. Opprett **lagerplassering** for å motta og plassere de leverte varene  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplasseringer** og velg den relaterte koblingen.  
    2. Velg handlingen **Ny**. 
    3. Velg *SØLV* i feltet **Lokasjonskode**.
    4. Velg feltet **Kildedokument**, og velg deretter **Bestilling**.  
    5. Velg **Kildenr.**-feltet, velg linjen for kjøpet fra leverandør 10000, og velg **OK**-knappen for å fylle ut plasseringslinjene i henhold til det valgte kildedokumentet.

        Velg eventuelt **Hent kildedokument**-handlingen, og velg deretter bestillingen.  

5. Endre lagerplasseringen basert på faktisk plassering av varer, og bokfør dokument

    Når han plasserer varer i hyller, ser Johan at standardhyllen allerede inneholder noen varer, så han bestemmer seg for å bruke en annen hylle. John plasserer også andre varer i de neste hyllene, slik at det mottatte antallet ikke passer til kapasiteten.

    1. I den første linjen endrer du **Hyllekode** fra *S-1-01*, som ble kopiert fra bestillingen, til *S-1-02*. 
    2.  Angi 20 i feltet **Ant. som skal håndt.** på lagerplasseringslinjen med vare WBR-1000.  
    3. På den andre linjen angir du 20 i feltet **Ant. som skal håndt.** og velger deretter **Del linje**-handling. Det vises en ny linje som er en kopi av den opprinnelige linjen, bortsett fra at feltet **Ant. som skal håndt.** inneholder antallet du fjernet fra den opprinnelige linjen. 
    4. Fyll ut hyllekoder for varen WBR-1001:

    |Vare|Hyllekode|Antall|  
    |----------|-------------------|--------------|  
    |WRB-1001|S-1-03|20|  
    |WRB-1001|S-1-04|10|

    5.  Velg **Bokfør**-handlingen, velg **Motta og fakturer**, og velg deretter **OK**-knappen.  

### <a name="results"></a>Resultater
 - de brente bønnene er nå registrert som plassert i angitte hyller
 - den **bokførte lagerplasseringen** opprettes
 - det **bokførte kjøpsmottaket** opprettes
 - bestillingen har **Mottatt antall** oppdatert for linjene som er mottatt
 - **varelageret** økes med det valgte antallet
    

## <a name="outbound-flow-picking-and-shipping-in-basic-warehouse-configurations"></a>Utgående flyt: Plukking og levering i grunnleggende lageroppsett

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan de utgående prosessene for plukking og levering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.  

|Prinsipp|Inngående prosess|Hyller|Plukking|Følgesedler|Kompleksitetsnivå (se [Designdetaljer: Lageroppsett](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokføre plukking og levering fra ordrelinjen|X|||2|  
|B|Bokføre plukking og levering fra et lagerplukkdokument||X||3|  
|L|Bokføre plukking og levering fra en lagerfølgeseddel|||X|4/5/6|  
|D|Bokføre plukking fra et lagerplukkdokument og bokføre leveringen fra en lagerfølgeseddel||X|X|4/5/6|  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Utgående lagerflyt](../../design-details-outbound-warehouse-flow.md).  

Følgende gjennomgangen demonstrerer metoden B i forrige tabell.

### <a name="scenario-1"></a>Scenario
Ordrebehandleren Susan oppretter en ordre for ulike brente bønner og sender den til lager. John, lagermedarbeideren, må kontrollere at forsendelsen klargjøres og leveres til kunden. John behandler alle involverte oppgaver på siden **Lagerplukk**, som peker automatisk til hyllene der brente bønner er lagret.

### <a name="steps-1"></a>Trinn
Dette er en fortsettelse av [Inngående flyt: Mottak og plassering i grunnleggende lageroppsett](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Definer siden **Lokasjonskort** for å definere selskapets inngående lagerflyter.  

    1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 5.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
    2.  Åpne lokasjonskortet *SØLV*.  
    3.  Merk av for **Plukk nødv.**.  

2. Opprett ordren, som er den vanligste typen utgående kildedokument.  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 6.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
    2. Velg handlingen **Ny**.  
    3. Opprett en ordre for kunde 10000 med følgende ordrelinje.  

    |Vare|Lokasjonskode|Antall|  
    |----|-------------|--------|  
    |WRB-1000|SØLV|20|  
    |WRB-1001|SØLV|30|  

    Hyllekodene fylles automatisk ut med standardhyller.

    4. Velg handlingen **Opprett lagerplassering/-plukk**.
    5. Merk av for **Opprett lagerplukking**.  
    6. Velg **OK**-knappen. Et nytt lagerplukk opprettes.

3. Plukk og lever varer

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 7.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplukk**, og velg deretter den relaterte koblingen.  
    2. Velg lagerplukk for salg til kunde 10000
    
    Det opprettede lagerplukket ignorerte hyllen som er definert for varen *WRB-1000*, fordi den ikke inneholder lager og bruker en annen hylle. De andre linjene med varen *WRB-1001* ble automatisk delt for plukking fra flere hyller.
    
4. Velg handlingen **Autoutfyll ant som skal håndt**.  

5. Velg **Bokfør**-handlingen, velg **Lever**, og velg deretter **OK**-knappen.  

### <a name="results-1"></a>Resultater
 - de brente bønnene er nå registrert som plukket fra angitte hyller
 - den **bokførte lagerplukkingen** opprettes
 - den **bokførte følgeseddelen** opprettes
 - ordren har **Antall levert** oppdatert for linjene som er levert
 - **varelageret** reduseres med det valgte antallet


## <a name="see-also"></a>Se også
[Plasser varer med lagerplasseringer](../../warehouse-how-to-put-items-away-with-inventory-put-aways.md) 
[Definer grunnleggende lagre med operasjonsområder](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) 
[Utformingsdetaljer: Inngående lagerflyt](../../design-details-inbound-warehouse-flow.md) 
[Plukk varer med lagerplukk](../../warehouse-how-to-pick-items-with-inventory-picks.md) 
[Utformingsdetaljer: Utgående lagerflyt](../../design-details-outbound-warehouse-flow.md) 
[Vis tilgjengeligheten til varer](../../inventory-how-availability-overview.md) 
