---
title: "Gjennomgang – Mottak og plassering i avansert lageroppsett | Microsoft-dokumentasjon"
description: "I Finance and Operations, Business edition kan de inngående prosessene for mottak og plassering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 991256bf2737297710d25f5a25854f4803185fc3
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Gjennomgang: Mottak og plassering i avansert lageroppsett
I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de inngående prosessene for mottak og plassering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.  

|Prinsipp|Inngående prosess|Hyller|Mottak|Plassering|Kompleksitetsnivå (se [Designdetaljer: Lageroppsett](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bokføre mottak og plassering fra ordrelinjen|X|||2|  
|B|Bokføre mottak og plassering fra et lagerplasseringsdokument|||X|3|  
|L|Bokføre mottak og plassering fra et lagermottaksdokument||X||4/5/6|  
|D|Bokføre mottak fra et lagermottaksdokument og bokføre plassering fra et lagerplasseringsdokument||X|X|4/5/6|  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Inngående lagerflyt](design-details-inbound-warehouse-flow.md).  

Følgende gjennomgangen demonstrerer metoden D i forrige tabell.  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen  
I avanserte lageroppsett hvor lokasjonen er definert for å kreve mottaksbehandling, i tillegg til plasseringsbehandling, bruker du vinduet **Lagermottak** til å registrere og bokføre mottaket av varer på flere inngående ordrer. Når lagermottaket bokføres, opprettes det ett eller flere lagerplasseringsdokumenter for å instruere lageransatte til å ta den mottatte varen og plassere dem på angitte steder i henhold til hylleoppsett eller i andre hyller. Varenes bestemte plasseringer registreres når plasseringen registreres. Det inngående kildedokument kan være en bestilling, en ordreretur, en inngående overføringsordre eller monterings- eller produksjonsordre med avgang som er klar til plassering. Hvis mottaket er opprettet fra en inngående ordre, kan det hentes ett inngående kildedokument for mottaket. Ved hjelp av denne metoden kan du registrere mange varer som kommer fra ulike inngående ordrer med én bekreftelse.  

Denne gjennomgangen viser følgende oppgaver.  

-   Konfigurere lokasjonen KR.SAND for mottak og plassering.  
-   Opprett og frigi to bestillinger for full lagerhåndtering.  
-   Opprett og bokfør et lagermottaksdokument for flere bestillingslinjer fra bestemte leverandører.  
-   Registrere en lagerplassering for de mottatte varene.  

## <a name="roles"></a>Roller  
Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:  

-   Lagerleder  
-   Innkjøper  
-   Mottakspersonale  
-   Lagermedarbeider  

## <a name="prerequisites"></a>Forutsetninger  
For å fullføre denne gjennomgangen må du gjøre følgende:  

-   Installere CRONUS Norge AS.  
-   Slik gjør du deg til lageransatt på lokasjonen KR.SAND ved å følge disse trinnene:  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lageransatte**, og velg deretter den relaterte koblingen.  
2.  Velg feltet **Bruker-ID**, og velg din egen brukerkonto i **Brukere**-vinduet.  
3.  Skriv inn KR.SAND i **Lokasjonskode**-feltet.  
4.  Velg **Standard**- feltet.  

## <a name="story"></a>Hovedscenario  
Ellen, lagerlederen hos CRONUS Norge AS, oppretter to bestillinger for tilbehørsvarer fra leverandørene 10000 og 20000 som skal leveres til lageret KR.SAND. Når leveringene ankommer lageret, bruker Sammy, som er ansvarlig for mottak av varer fra leverandør 10000 og 20000, et filter til å opprette mottakslinjer for bestillinger som kommer fra de to leverandørene. Sammy bokfører varene som mottatt på lageret i ett lagermottak og gjør varene tilgjengelig for salg eller andre behov. Lagermedarbeideren Joakim tar elementene fra mottakshyllen og plasserer dem. Han plasserer alle enhetene i standardhyllene deres, bortsett fra 40 av 100 mottatte hengsler som han plasserer i monteringsavdelingen ved å dele plasseringslinjen. Når John registrerer plasseringen, oppdateres hylleinnholdet og varene gjøres tilgjengelig for plukking fra lageret.  

## <a name="reviewing-the-white-location-setup"></a>Se gjennom lokasjonsoppsettet KR.SAND  
Oppsettet av vinduet **Lokasjonskort** definerer selskapets lagerflyter.  

### <a name="to-review-the-location-setup"></a>Slik går du gjennom lokasjonsoppsettet  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
2.  Åpne lokasjonskortet KR.SANd.  
3.  På hurtigfanen **Lager** legger du merke til at det er merket av for **Lagerstyring**.  

    Dette betyr at lokasjonen er definert for høyeste kompleksitetsnivå, noe som gjenspeiles av det faktum at det er merket av for alle avmerkingsboksene for lagerhåndtering på hurtigfanen.  

4.  På hurtigfanen **Hyller** legger du merke til at hyller er angitt i feltet **Hyllekode for mottak** og **Hyllekode for levering**.  

Dette betyr at når du oppretter et lagermottak, kopieres denne hyllekoden til hodet av lagermottaksdokumentet som standard og til linjene for de resulterende lagerplasseringene.  

## <a name="creating-the-purchase-orders"></a>Opprette bestillingene  
Bestillinger er den vanligste typen inngående kildedokument.  

### <a name="to-create-the-purchase-orders"></a>Slik oppretter du bestillinger  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bestillinger**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Opprett en bestilling for leverandør 10000 på arbeidsdatoen (23. januar) med følgende bestillingslinjer.  

    |Vare|Lokasjonskode|Antall|  
    |----------|-------------------|--------------|  
    |70200|KR.SAND|100 STK|  
    |70201|KR.SAND|50 STK|  

    Fortsett med å varsle lageret om at bestillingen er klar for håndtering av lageret når leveringen ankommer.  

4.  Velg handlingen **Frigi**.  

    Fortsett med å opprette den andre bestillingen.  

5.  Velg handlingen **Ny**.  
6.  Opprett en bestilling for leverandør 20000 på arbeidsdatoen med følgende bestillingslinjer.  

    |Vare|Lokasjonskode|Antall|  
    |----------|-------------------|--------------|  
    |70100|KR.SAND|10 BOKS|  
    |70101|KR.SAND|12 BOKS|  

    Velg handlingen **Frigi**.  

    Leveringer av varer fra leverandørene 10000 og 20000 har kommet til lageret KR.SAND, og Sammy begynner å behandle kjøpsmottakene.  

## <a name="receiving-the-items"></a>Motta varene  
I vinduet **Lagermottak** kan du håndtere flere inngående ordrer for kildedokumenter, for eksempel en bestilling.  

### <a name="to-receive-the-items"></a>Slik mottar du varer  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lagermottak**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Skriv inn KR.SAND i **Lokasjonskode**-feltet.  
4.  Velg handlingen **Bruk filtre til å hente k.dok...**.  
5.  Skriv inn **TILBEHØR** i **Kode**-feltet.  
6.  Angi **Leverandør 10000 og 20000** i **Beskrivelse**-feltet.  
7.  Velg handlingen **Endre**.  
8.  I **Kjøp**-hurtigfanen i feltet **Filter for kjøp fra-levrdnr.** angir du **10000&#124;20000**.  
9. Velg handlingen **Kjør**. Lagermottaket er fylt ut med fire linjer som representerer bestillingslinjene for de angitte leverandørene. Feltet **Motta (antall)** er fylt ut fordi du ikke merket av for **Ikke fyll ut ant. som skal hnd** i vinduet **Filtre for henting av kildedok**.  
10. Eventuelt, hvis du vil bruke et filter som beskrevet tidligere i denne delen, velger du **Hent kildedokument**-handlingen og velger deretter bestillinger fra de aktuelle leverandørene.  
11. Velg **Bokfør mottak**-handlingen, og velg deretter **Ja**-knappen.  

    Det opprettes positive vareposter som gjenspeiler de bokførte kjøpsmottakene for tilbehør fra leverandør 10000 og 20000, og elementene er klare til å bli plassert i lageret fra mottakshyllen.  

## <a name="putting-the-items-away"></a>Plassere varene  
I **Plassering**-vinduet kan du håndtere plasseringer for et bestemt lagermottaksdokumentet som dekker flere kildedokumenter. Som for alle lageraktivitetsdokumenter er hvert element på lagerplasseringen er representert ved en Hent-linje og en Plasser-linje. I den følgende fremgangsmåten er hyllekoden på Hent-linjene den standard mottakshyllen på lokasjonen KR.SAND, W-08-0001.  

### <a name="to-put-the-items-away"></a>Slik plasserer du varene  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Plassering**, og velg deretter den relaterte koblingen.  
2.  Velg det eneste lagerplasseringsdokumentet i listen, og deretter i fanebladet **Hjem**, i gruppen **Behandle**, velger du **Rediger**.  

    Lagerplasseringsdokumentet åpnes med totalt åtte Hent- eller Plasser-linjer for de fire bestillingslinjene.

    Lagermedarbeideren får beskjed om at det trengs 40 hengsler i monteringsavdelingen, og han fortsetter å dele den ene Plasser-linjen for å angi en andre Plasser-linje for hylle W-02-0001 i monteringsavdelingen hvor han plasserer den delen av de mottatte hengslene.  

3.  Velg den andre linjen i **Plassering**-vinduet, Plasser-linje for vare 70200.  
4.  Endre verdien fra 100 til 60 i feltet **Ant. som skal håndt.**.  
5.  På hurtigfanen **Linjer** velger du **Funksjoner**, og deretter **Del linje**. Det settes inn en ny linje for elementet 70200 med 40 i feltet **Ant. som skal håndt.**.  
6.  Skriv inn W-02-0001 i **Hyllekode**-feltet. **Sonekode**-feltet fylles ut automatisk.  

    Fortsette med å registrere plasseringen.  

7.  Velg **Registrer plassering**-handlingen, og velg deretter **Ja**-knappen.  

    Mottatt tilbehør er nå plassert i varens standardhyller og 40 hengsler plasseres i monteringsavdelingen. De mottatte varene er nå tilgjengelig for plukking til interne behov, for eksempel monteringsordrer, eller til eksterne behov, for eksempel følgesedler.  

## <a name="see-also"></a>Se også  
 [Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Flytte varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Designdetaljer: Inngående lagerflyt](design-details-inbound-warehouse-flow.md)   
 [Gjennomgang: Mottak og plassering i grunnleggende lageroppsett](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)   
 [Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)

