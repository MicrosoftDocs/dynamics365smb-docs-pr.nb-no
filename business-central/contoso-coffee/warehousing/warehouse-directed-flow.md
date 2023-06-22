---
title: 'Mottak, plassering, flytting, plukking og levering i avansert lageroppsett med kontrollert lagerstyring'
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

# <a name="walkthrough-of-inbound-and-outbound-flow-in-advanced-warehouse-configuration-with-directed-put-away-and-pick" />Gjennomgang av inngående og utgående flyt i avansert lageroppsett med lagerstyring

Denne gjennomgangen vis hvordan du fullfører inngående og utgående flyter i konfigurasjonen Avansert: lagerstyring Hvis du vil ha mer informasjon, kan du se [Oversikt over ulike konfigurasjonsalternativer](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

## <a name="prerequisites" />Forutsetninger
Hvis du vil fullføre denne gjennomgangen, må du gjøre deg til lageransatt på lokasjonen *HVIT* ved å følge disse trinnene:  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageransatte**, og velg deretter den relaterte koblingen.  
2. Velg feltet **Bruker-ID**, og velg din egen brukerkonto på siden **Brukere**.  
3. Skriv inn KR.SAND i **Lokasjonskode**-feltet.  
4. Aktiver vekslebryteren **Standard**.


## <a name="scenario" />Scenario
Lagerlederen Ellen bruker funksjonaliteten for kryssoverføring og etterfyllings til å øke hastigheten på mottaks- og leveringstid.  

## <a name="steps" />Trinn

1. Opprett lagerlevering.  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 2.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
    2. Velg ordre for kunde 10000 for HVIT lokasjon. Eksternt ordrenr. er *W-1*. Bruk tilpasningsverktøyene hvis feltet **Eksternt ordrenr.** ikke vises. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](../../ui-personalization-user.md).
    3. Velg **Opprett lagerlevering**-handlingen for å opprette lagerlevering for valgt ordre.
    4.  Velg handlingen **Frigi** for å informere lageret at salgsleveringen er klar for lagerhåndtering.  

2. Definer hyller for varen for å styre hvor den plasseres 

    1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
    2.  Velg *WRB-1000*, og velg deretter handlingen **Hylleinnhold**.  
    3.  Velg handlingen **Ny**. Legg til to linjer. Bruk verktøyene for tilpassing hvis feltet **Hyllekode** ikke er synlig. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](../../ui-personalization-user.md). 
    
    |Vare|Lokasjonskode|Hyllekode|Fast|Måleenhet|
    |----------|----------|---------|---|------|  
    |WRB-1000|KR.SAND|A-05-0001|Ja|HANDLEKURV|  
    |WRB-1000|KR.SAND|A-05-0002|Ja|HANDLEKURV|

3. Opprett lagermottak.  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.  
    2. Velg ordre for leverandør 10000 for HVIT lokasjon. Leverandørordrenr. er *W-2*. Bruk tilpasningsverktøyene hvis feltet **Leverandørordrenr.** ikke vises. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](../../ui-personalization-user.md).
    3. Velg **Opprett lagermottak**-handlingen for å opprette lagermottak for valgt bestilling.


4. Kontroller om det er utgående ordrer som trenger mottatte varer, og bokfør mottak
    1. Velg handlingen **Beregn kryssoverføring**. Dette fyller ut en kolonne **Autoutfyll antall for kryssoverføring**.
    2. Angi 0 i feltet **Autoutfyll antall for kryssoverføring** på linjen med varen *WRB-1000* som du ikke planlegger å pakke på nytt i mottaksområdet.
    3. Velg handlingen **Bokfør mottak**.

5. Registrer lagerplasseringen
    1. Ved å bruke ikonet ![Lyspære som åpner funksjonen Fortell meg 5.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") angir du **Lagerplassering** og velger den relaterte koblingen.
    2. Finn lagerplasseringsdokumentet som opprettes fra lagermottaket, og åpne det
    3. På siden **Lagerplassering** gjennomgår du delen **Linjer**

    I denne fasen avsløres den logiske logikken for hyllekapasitet lagerplasseringslinjene har tre linjer for varen *WRB-1000*:
    - En Hent-linje for å flytte de mottatte antallene fra mottakshyllen (W-08-0001)
    - En Plasser-linje som flytter én POSE inn i en av de konfigurerte faste hyllene (W-05-0001)
    - En Plasser-linje som flytter en annen POSE inn i en annen fast hylle (W-05-0002). Dette er fordi én enkelt fast hylle ikke kan inneholde hele mottaksantallet.

    Siden denne plasseringen inneholder kryssoverføringslinjer, ser du tre linjer for varen *WRB-1001*:
    -  En Hent-linje for å flytte de mottatte antallene fra mottakshyllen (W-08-0001)
    -  En Plasser-linje for 2 til kryssoverføringshyllen
    -  En Plasser-linje for restantallet i lagringshyllen

    4. Velg handlingen **Registrer plassering**.


6. Definer en plukkhylle for varen for å styre hvor den plukkes fra 

    1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 6.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
    2.  Åpne lokasjonskortet *HVIT*.  
    3.  Velg **Hyller**-handlingen på **lokasjonskortet**
    4.  Velg hyllen *W-02-0001*, og velg deretter handlingen **Innhold**.  
    5.  Velg handlingen **Ny**.  
    6.  Aktiver vekslebryteren **Fast**.  
    7.  Angi **WRB-1000** i feltet *Varenr.*. 
    8.  I feltet **Min. antall** angir du *2*. 
    9.  I feltet **Maks antall** angir du *10*. 

    Bruk tilpasningsverktøyene hvis feltene **Min. antall** og **Maks antall** ikke vises. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](../../ui-personalization-user.md). 

7. Omorganiser lageret ved å flytte varer fra masselagringsområdet til plukkområdet, for å gi optimal plukktid.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 7.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Flytteforslag**, og velg deretter den relaterte koblingen
    2. Velg handlingen **Beregn etterfylling av hyller**. 

    Lagerforslaget med forslag om å flytte vare *WRB-1000* fra masselagring til plukkområde opprettes.

    3. Velg **Opprett flytting**-handling og bekreft for å opprette dokumentet.
    4.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 8.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerflyttinger** og velg den relaterte koblingen
    5.  Åpne lagerflyttingen du opprettet, se gjennom **Linjer**-delen

     Ved denne fasen vises anbrekksfunksjonaliteten. Det vil være fire linjer:
    - En linje for å ta den ene POSEN ut av masselagringshyllen
    - En linje for å plassere de 48 stykkene tilbake på lager i samme hylle. 
    - En linje for å ta 10 stykker ut av masselagringshyllen
    - En linje for å plassere 10 stykker i plukkhyllen

    6.  Velg handlingen **Registrer flytting**.

8. Opprett lagerplukk

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 9.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Plukkforslag**, og velg deretter den relaterte koblingen
    2. Velg handlingen **Hent lagerdokumenter**, velg linjen for ordren for kunde 10000, og velg deretter **OK** for å fylle ut forslagslinjene i henhold til det valgte dokumentet.

    3. Kontroller feltet **Ant. i kryssoverføringshylle**. 

    4. Velg handlingen **Opprett plukk**.
    5. Bekreft plukkinnstillingene som trengs, for eksempel aktiver vekslebryteren **Per fra-sone**. Velg **OK**-knappen.
    
    Du mottar en bekreftelsesmelding med plukknumrene. Det er to plukkinger som er plassert i kryssoverføringssonen, nærme leveringsområdet, og det vil være fornuftig å behandle dem separat.

9.  Registrer lagerplukk
    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 10.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplukk** og velg den relaterte koblingen.
    2. Finn plukkene du har opprettet, og åpne dem.
    3. Velg handlingen **Registrer plukk**.
    4. Gjenta for den andre plukkingen

10. Bokfør lagerleveringen
    
    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 11.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Lagerlevering**, og velg den relaterte koblingen.
    2. På siden Lagerplassering gjennomgår du delen **Linjer**. Når lagerplukket er registrert, blir lagerleveringen oppdatert med **Antall som skal leveres** fylt ut.
    3. Velg handlingen **Bokfør levering**.
    4. Bekreft **Levering**-alternativet.


## <a name="results" />Resultater
- det **bokførte lagermottaket** opprettes
- den **registrerte lagerplasseringen** opprettes    
- det **bokførte kjøpsmottaket** opprettes    
- **bestillingen** har **Mottatt antall** oppdatert for linjene som er mottatt
- den **registrerte lagerflyttingen** opprettes
- det **registrerte lagerplukket** opprettes
- den **bokførte lagerleveringen** opprettes
- den **bokførte følgeseddelen** opprettes
- **ordren** har **Antall levert** oppdatert for linjene som er levert
- **varelageret** økes med rest som ikke sendes ut



## <a name="see-also" />Se også
[Motta varer](../../warehouse-how-receive-items.md) 
[Utformingsdetaljer: Inngående lagerflyt](../../design-details-inbound-warehouse-flow.md) 
[Lever varer](../../warehouse-how-ship-items.md) 
[Plukk varer for lagerlevering](../../warehouse-how-to-pick-items-for-warehouse-shipment.md) 
[Utformingsdetaljer: Utgående lagerflyt](../../design-details-outbound-warehouse-flow.md) 
[Vis tilgjengeligheten av varer](../../inventory-how-availability-overview.md) 
