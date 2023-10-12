---
title: Mottak og plassering i avansert lagerstyring
description: De inngående prosessene for mottak og plassering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# Gjennomgang: Mottak og plassering i avansert lageroppsett

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

I [!INCLUDE[prod_short](includes/prod_short.md)] blir mottak og plassering utført på av fire metoder, som beskrevet i tabellen nedenfor.

|Prinsipp|Inngående prosess|Krev kvitteringer|Krev plasseringer|Kompleksitetsnivå (Finn ut mer under [Oversikt over Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokføre mottak og plassering fra ordrelinjen|||Ingen dedikert lageraktivitet.|  
|B|Bokføre mottak og plassering fra et lagerplasseringsdokument||Slått på|Grunnleggende: ordre for ordre.|  
|U|Bokføre mottak og plassering fra et lagermottaksdokument|Slått på||Grunnleggende: konsolidert mottak/levering for flere ordrer.|  
|D|Bokføre mottak fra et lagermottaksdokument og bokføre plassering fra et lagerplasseringsdokument|Slått på|Slått på|Avansert|  

Finn ut mer under [Inngående lagerflyt](design-details-inbound-warehouse-flow.md).

Følgende gjennomgangen demonstrerer metoden D i forrige tabell.  

## Denne gjennomgangen

I avanserte lageroppsett hvor lokasjonen er definert for å kreve mottaksbehandling, i tillegg til plasseringsbehandling, bruker du siden **Lagermottak** til å registrere og bokføre mottaket av varer på flere inngående ordrer. Når lagermottaket bokføres, opprettes det ett eller flere lagerplasseringsdokumenter for å instruere lageransatte til å ta de mottatte varene og plassere dem på angitte steder i henhold til hylleoppsett eller i andre hyller. Varenes bestemte plasseringer registreres når plasseringen registreres. Det inngående kildedokument kan være en bestilling, en ordreretur, en inngående overføringsordre eller monterings- eller produksjonsordre med avgang som er klar til plassering. Hvis mottaket er opprettet fra en inngående ordre, kan det hentes ett inngående kildedokument for mottaket. Ved hjelp av denne metoden kan du registrere mange varer som kommer fra ulike inngående ordrer med én bekreftelse.  

Denne gjennomgangen viser følgende oppgaver:  

-   Konfigurere lokasjonen KR.SAND for mottak og plassering.  
-   Opprett og frigi to bestillinger for full lagerhåndtering.  
-   Opprett og bokfør et lagermottaksdokument for flere bestillingslinjer fra bestemte leverandører.  
-   Registrere en lagerplassering for de mottatte varene.  

## Roller

Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:  

-   Lagerleder  
-   Innkjøper  
-   Mottakspersonale  
-   Lagermedarbeider  

## Forutsetninger

For å fullføre denne gjennomgangen må du gjøre følgende:  

-   CRONUS installert.  
-   Slik gjør du deg til lageransatt på lokasjonen KR.SAND ved å følge disse trinnene:  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageransatte**, og velg deretter den relaterte koblingen.  
2.  Velg feltet **Bruker-ID**, og velg din egen brukerkonto på siden **Brukere**.  
3.  Skriv inn KR.SAND i **Lokasjonskode**-feltet.  
4.  Velg **Standard**- feltet.  

## Hovedscenario

Ellen, lagerlederen hos CRONUS, oppretter to bestillinger for tilbehørsvarer fra leverandørene 10000 og 20000 som skal leveres til lageret KR.SAND. Når leveringene ankommer lageret, bruker Sammy, som er ansvarlig for mottak av varer fra leverandør 10000 og 20000, et filter til å opprette mottakslinjer for bestillinger som kommer fra de to leverandørene. Sammy bokfører varene som mottatt på lageret i ett lagermottak og gjør varene tilgjengelig for salg eller andre behov. Lagermedarbeideren Joakim tar elementene fra mottakshyllen og plasserer dem. John plasserer alle enhetene i standardhyllene deres, bortsett fra 40 av 100 mottatte hengsler som plasseres i monteringsavdelingen ved å dele plasseringslinjen. Når John registrerer plasseringen, oppdateres hylleinnholdet og varene gjøres tilgjengelig for plukking fra lageret.  

## Se gjennom lokasjonsoppsettet KR.SAND

Oppsettet av siden **Lokasjonskort** definerer selskapets lagerflyter.  

### Slik går du gjennom lokasjonsoppsettet  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
2.  Åpne lokasjonskortet KR.SANd.  
3.  På hurtigfanen **Lager** legger du merke til at det er merket av for **Lagerstyring**.  

    Dette betyr at lokasjonen er definert for høyeste kompleksitetsnivå, noe som gjenspeiles av det faktum at det er merket av for alle avmerkingsboksene for lagerhåndtering på hurtigfanen.  

4.  På hurtigfanen **Hyller** legger du merke til at hyller er angitt i feltet **Hyllekode for mottak** og **Hyllekode for levering**.  

Dette betyr at når du oppretter et lagermottak, kopieres denne hyllekoden til hodet av lagermottaksdokumentet som standard og til linjene for de resulterende lagerplasseringene.  

## Opprette bestillingene

Bestillinger er den vanligste typen inngående kildedokument.  

### Slik oppretter du bestillinger  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Opprett en bestilling for leverandør 10000 på arbeidsdatoen (23. januar) med følgende bestillingslinjer.  

    |Vare|Lokasjonskode|Antall|  
    |----------|-------------------|--------------|  
    |70200|KR.SAND|100 STK|  
    |70201|KR.SAND|50 STK|  

    Fortsett med å varsle lageret om at bestillingen er klar for håndtering av lageret når leveringen ankommer.  

4.  Velg handlingen **Frigi**. Statusen endres fra Åpen til Frigitt.

    Fortsett med å opprette den andre bestillingen.  

5.  Velg handlingen **Ny**.  
6.  Opprett en bestilling for leverandør 20000 på arbeidsdatoen (23. januar) med følgende bestillingslinjer.  

    |Vare|Lokasjonskode|Antall|  
    |----------|-------------------|--------------|  
    |70100|KR.SAND|10 BOKS|  
    |70101|KR.SAND|12 BOKS|  

    Velg handlingen **Frigi**. Statusen endres fra Åpen til Frigitt.

    Leveringer av varer fra leverandørene 10000 og 20000 har kommet til lageret KR.SAND, og Sammy begynner å behandle kjøpsmottakene.  

## Motta varene

På siden **Lagermottak** kan du håndtere flere inngående ordrer for kildedokumenter, for eksempel en bestilling.  

### Slik mottar du varer  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagermottak** og velg den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Skriv inn KR.SAND i **Lokasjonskode**-feltet.  
4.  Velg **Handlinger** og deretter **Funksjoner** og velg **Bruk filtre til å hente k.dok.**-handlingen.  
5.  Skriv inn **TILBEHØR** i **Kode**-feltet.  
6.  Angi **Leverandør 10000 og 20000** i **Beskrivelse**-feltet.  
7.  Velg handlingen **Endre**.  
8.  I **Kjøp**-hurtigfanen i feltet **Filter for kjøp fra-levrdnr.** angir du **10000&#124;20000**.  
9. Velg handlingen **Kjør**. Lagermottaket er fylt ut med fire linjer som representerer bestillingslinjene for de angitte leverandørene. Feltet **Motta (antall)** er fylt ut, fordi du ikke merket av for **Ikke fyll ut ant. som skal hnd** på siden **Filtre for henting av kildedok**.  
10. Eventuelt, hvis du vil bruke et filter som beskrevet tidligere i denne delen, velger du **Hent kildedokument**-handlingen og velger deretter bestillinger fra de aktuelle leverandørene.  
11. Velg **Bokføring** og deretter **Bokfør mottak**-handlingen, og velg deretter **Ja**-knappen.  

    Det opprettes positive vareposter som gjenspeiler de bokførte kjøpsmottakene for tilbehør fra leverandør 10000 og 20000, og elementene er klare til å bli plassert i lageret fra mottakshyllen.  

## Plassere varene

På siden **Plassering** kan du håndtere plasseringer for et bestemt lagermottaksdokumentet som dekker flere kildedokumenter. Som for alle lageraktivitetsdokumenter er hvert element på lagerplasseringen er representert ved en Hent-linje og en Plasser-linje. I den følgende fremgangsmåten er hyllekoden på Hent-linjene den standard mottakshyllen på lokasjonen KR.SAND, W-08-0001.  


### Slik plasserer du varene  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Plasseringer** og velg den relaterte koblingen.  
2.  Velg det eneste lagerplasseringsdokumentet i listen, og deretter **Rediger**-handlingen.  

    Lagerplasseringsdokumentet åpnes med totalt åtte Hent- eller Plasser-linjer for de fire bestillingslinjene.

    Lagermedarbeideren får beskjed om at det trengs 40 hengsler i monteringsavdelingen, og fortsetter å dele den ene Plasser-linjen for å angi en andre Plasser-linje for hylle W-02-0001 i monteringsavdelingen hvor lagerarbeideren plasserer den delen av de mottatte hengslene.  

3.  Velg den andre linjen på siden **Plassering**, Plasser-linje for vare 70200.  
4.  Endre verdien fra 100 til 60 i feltet **Ant. som skal håndt.**.  
5.  På hurtigfanen **Linjer** velger du **Funksjoner**, og deretter **Del linje**. Det settes inn en ny linje for elementet 70200 med 40 i feltet **Ant. som skal håndt.**.  
6.  Skriv inn W-02-0001 i **Hyllekode**-feltet. **Sonekode**-feltet fylles ut automatisk.  

    Som standard er feltet **Sonekode** på salgslinjen skjult, så du må vise den. Du må tilpasse siden for å gjøre dette. Hvis du vil ha mer informasjon, kan du se [Slik tilpasser du en side med Tilpasse-banneret](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

    Fortsette med å registrere plasseringen.  

7.  Velg **Registrer plassering**-handlingen, og velg deretter **Ja**-knappen.  

    Mottatt tilbehør er nå plassert i varens standardhyller og 40 hengsler plasseres i monteringsavdelingen. De mottatte varene er nå tilgjengelig for plukking til interne behov, for eksempel monteringsordrer, eller til eksterne behov, for eksempel følgesedler.  

## Se også  
 [Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Flytte varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Designdetaljer: Inngående lagerflyt](design-details-inbound-warehouse-flow.md)   
 <!-- [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)    -->
 [Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
