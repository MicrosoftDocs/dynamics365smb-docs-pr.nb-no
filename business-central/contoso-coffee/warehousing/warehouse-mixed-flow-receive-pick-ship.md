---
title: 'Mottak, plassering, plukk og levering i blandet lageroppsett'
description: 'I Business Central kan de utgående prosessene utføres på ulike måter, avhengig av kompleksitetsnivået til lageret.'
author: andreipanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 04/01/2021
ms.author: andreipa
---

# <a name="walkthrough-of-inbound-and-outbound-flow-in-mixed-warehouse-configurations"></a>Gjennomgang av inngående og utgående flyt i blandede lageroppsett

Denne gjennomgangen viser hvordan du fullfører inngående og utgående flyter i blandet oppsett, der inngående flytlager er konfigurert som Grunnleggende: ordre for ordre og for utgående flyt Avansert oppsett brukes. Hvis du vil ha mer informasjon, kan du se [Oversikt over ulike konfigurasjonsalternativer](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites"></a>Forutsetninger
Hvis du vil fullføre denne gjennomgangen, må du gjøre deg til lageransatt på lokasjonen *GUL* ved å følge disse trinnene:  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageransatte**, og velg deretter den relaterte koblingen.  
2. Velg feltet **Bruker-ID**, og velg din egen brukerkonto på siden **Brukere**.  
3. Skriv inn *GUL* i feltet **Lokasjonskode**.  

## <a name="inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Inngående flyt: Mottak og plassering i grunnleggende lageroppsett

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan de inngående prosessene for mottak og plassering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.  

|Prinsipp|Inngående prosess|Hyller|Mottak|Plassering|Kompleksitetsnivå (se [Designdetaljer: Lageroppsett](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokføre mottak og plassering fra ordrelinjen|X|||2|  
|B|Bokføre mottak og plassering fra et lagerplasseringsdokument|||X|3|  
|L|Bokføre mottak og plassering fra et lagermottaksdokument||X||4/5/6|  
|D|Bokføre mottak fra et lagermottaksdokument og bokføre plassering fra et lagerplasseringsdokument||X|X|4/5/6|  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Inngående lagerflyt](../../design-details-inbound-warehouse-flow.md).  

Følgende gjennomgangen demonstrerer metoden C i forrige tabell.  

### <a name="scenario"></a>Scenario
Innkjøperen Alicia oppretter bestillinger for ulike brente bønner etter behov. Når kombinert levering ankommer til lageret, mottar og plasserer lagermedarbeideren John varene. Når John bokfører mottaket, bokføres varene som mottatt på lageret og tilgjengelig for salg eller andre behov.  

### <a name="steps"></a>Trinn
1. Definer siden **Lokasjonskort** for å definere selskapets inngående lagerflyter.  

    1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 2.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
    2.  Åpne lokasjonskortet *GUL*.  
    3.  Deaktiver vekslebryteren **Plassering nødv.**.  

2. Frigi bestillinger til lager.  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.  
    2. Velg ordrer for leverandør 10000 for GUL lokasjon. Leverandørordrenr. er *Y-1* og *Y-2*. Bruk tilpasningsverktøyene hvis feltet **Leverandørordrenr.** ikke vises. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](../../ui-personalization-user.md).
    3. Velg handlingen **Frigi** for å varsle lageret om at de valgte bestillingene er klare for håndtering av lageret når leveringen ankommer.  

3. Opprett lagermottaket for å motta og plassere de leverte varene
    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagermottak** og velg den relaterte koblingen.
    2. Velg handlingen **Opprett**
    3. På lagermottakssiden trykker du på ENTER for å få et lagermottaksnummer automatisk valgt
    4. Angi *lokasjonskoden* som **GUL**.
    5. Velg handlingen **Hent kildedokumenter ...**
    6. Velg tidligere frigitte bestillinger fra leverandør 10000, og velg **OK**.
        Linjene vil inneholde en ny oppføring for hver bestillingslinje.

4. Juster antall til mottak basert på mottatt antall og bokfør dokument
    1. Velg linje med varen *WRB-1000*.
    2. Velg *OVERRCPT10* i feltet **Overmottakskode**, og endre verdien i feltet **Motta (antall)** fra *100* til *110*.
    3. Velg linje med varen *WRB-1001* og 
    4. I den andre linjen endrer du verdien i feltet **Motta (antall)** fra *200* til *190*.
    5. Velg handlingen **Bokfør mottak**.

### <a name="results"></a>Resultater
 - de brente bønnene er nå registrert som plassert
 - det **bokførte lagermottaket** opprettes
 - det **bokførte kjøpsmottaket** opprettes
 - bestillingen har **Mottatt antall** oppdatert for linjene som er mottatt
 - **varelageret** økes med det valgte antallet
    

## <a name="outbound-flow-picking-and-shipping-in-advanced-warehouse-configurations"></a>Utgående flyt: Plukking og levering i avansert lageroppsett

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan de utgående prosessene for plukking og levering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.  

|Prinsipp|Inngående prosess|Hyller|Plukking|Følgesedler|Kompleksitetsnivå (se [Designdetaljer: Lageroppsett](../../design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokføre plukking og levering fra ordrelinjen|X|||2|  
|B|Bokføre plukking og levering fra et lagerplukkdokument||X||3|  
|L|Bokføre plukking og levering fra en lagerfølgeseddel|||X|4/5/6|  
|D|Bokføre plukking fra et lagerplukkdokument og bokføre leveringen fra en lagerfølgeseddel||X|X|4/5/6|  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Utgående lagerflyt](../../design-details-outbound-warehouse-flow.md).  

Følgende gjennomgangen demonstrerer metoden D i forrige tabell.

### <a name="scenario-1"></a>Scenario
Ordrebehandleren Susan oppretter ordrer for ulike brente bønner og sender den til lager. Siden alle ordrene kommer fra samme kunde, bestemmer lagerlederen Ellen at de skal sendes sammen. John, lagermedarbeideren, må kontrollere at forsendelsen klargjøres og leveres til kunden.

### <a name="steps-1"></a>Trinn
Dette er en fortsettelse av [Inngående flyt: Mottak og plassering i grunnleggende lageroppsett](#inbound-flow-receiving-and-putting-away-in-basic-warehouse-configurations).

1. Frigi ordrer til lager.  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 5.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
    2. Velg ordrer for kunde 10000 for GUL lokasjon. Eksterne ordrenumre er *Y-3*, *Y-4* og *Y-5*. Bruk tilpasningsverktøyene hvis feltet **Eksternt ordrenr.** ikke vises. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](../../ui-personalization-user.md).
    3. Velg handlingen **Frigi** for å informere lageret at de valgte ordrene er klare for lagerhåndtering.  

2. Slik leverer du varer  
    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 6.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerleveringer** og velg den relaterte koblingen.  
    2. Velg handlingen **Ny**.  
    3. Skriv inn *GUL* i feltet **Lokasjonskode**.  
    4. Velg handlingen **Bruk filtre til å hente k.dok...**.  
    5. Skriv inn **CUST10000** i **Kode**-feltet.  
    6. Angi **Kunde 10000** i **Beskrivelse**-feltet.  
    7. Velg handlingen **Endre**.  
    8. I **Salg**-hurtigfanen i feltet **Filter for Salg til-kundenr.** angir du *10000*.  
    9. Velg handlingen **Kjør**. 
    
    Lagerleveringen er fylt ut med fire linjer som representerer ordrelinjene for den angitte kunden. Feltet **Lever (antall)** er tomt, ettersom varene må plukkes først.

3. Opprett lagerplukkingen fra lagerleveringen
    1. Velg handlingen **Opprett plukk** på lagerleveringssiden.
    2. Bekreft de nødvendige innstillingene for plukk, velg for eksempel *Vare* i feltet **Sorteringsmetode for aktivitetslinje** for å gruppere samme varer sammen. Velg **OK**-knappen.
    3. Du mottar en bekreftelsesmelding med plukknummeret. 

4. Åpne lagerplukkingen
    1. Ved å bruke ikonet ![Lyspære som åpner funksjonen Fortell meg 7.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplukk** og velg den relaterte koblingen.
    2. Finn plukket du har opprettet, og åpne dem.
    3. Oppdater **Ant. som skal håndt.** om nødvendig.
    4. Velg handlingen **Registrer plukk**.
    5. Lagerplukkingen lukkes og fjernes hvis alle antallene håndteres.

5. Bokfør lagerleveringen
   1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 8.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerleveringer** og velg den relaterte koblingen.  
   2. Finn leveringen du opprettet tidligere, og åpne den.
    Merk at **Lever (antall)** er fylt ut.
    3. Du kan oppdatere **Bokføringsdato**, **Eksternt dokumentnr.**, **Transportørkode**, **Leveringsmåte** hvis det er nødvendig. Verdier som ikke er tomme, blir overført til kildedokumenter.
    4. Velg handlingen **Bokfør levering**.
    5. Bekreft **Levering**-alternativet.

### <a name="results-1"></a>Resultater
 - de brente bønnene er nå registrert som plukket 
 - det **registrerte lagerplukket** opprettes
 - den **bokførte lagerleveringen** opprettes
 - de tre **bokførte følgesedlene** er opprettet
 - ordren har **Antall levert** oppdatert for linjene som er levert
 - **varelageret** reduseres med det valgte antallet


## <a name="see-also"></a>Se også
[Motta varer](../../warehouse-how-receive-items.md)
[Definer grunnleggende lagre med operasjonsområder](../../warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)
[Utformingsdetaljer: Inngående lagerflyt](../../design-details-inbound-warehouse-flow.md)
[Lever varer](../../warehouse-how-ship-items.md)
[Plukk varer for lagerlevering](../../warehouse-how-to-pick-items-for-warehouse-shipment.md)
[Utformingsdetaljer: Utgående lagerflyt](../../design-details-outbound-warehouse-flow.md)
[Vis tilgjengeligheten til varer](../../inventory-how-availability-overview.md)
