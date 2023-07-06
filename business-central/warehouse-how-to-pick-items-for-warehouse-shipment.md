---
title: Plukke varer for lagerlevering
description: Lær mer om å bruke lagerplukkdokumenter til å opprette og behandle plukkinformasjon før du bokfører en lagerlevering.
author: bholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '7335, 7339, 7345,'
---
# <a name="pick-items-for-warehouse-shipment"></a><a name="pick-items-for-warehouse-shipment"></a><a name="pick-items-for-warehouse-shipment"></a>Plukke varer for lagerlevering

I [!INCLUDE[prod_short](includes/prod_short.md)] plukker og leverer du varer ved å bruke en av fire metoder, som beskrevet i tabellen nedenfor.

|Prinsipp|Utgående prosess|Plukk nødv.|Levering nødv.|Kompleksitetsnivå (Finn ut mer under [Oversikt over Warehouse Management](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bokføre plukking og levering fra ordrelinjen|||Ingen dedikert lageraktivitet.|  
|B|Bokføre plukking og levering fra et lagerplukkdokument|Slått på||Grunnleggende: ordre for ordre.|  
|U|Bokføre plukking og levering fra en lagerfølgeseddel||Slått på|Grunnleggende: konsolidert mottak/levering for flere ordrer.|  
|D|Bokføre plukking fra et lagerplukkdokument og bokføre leveringen fra en lagerfølgeseddel|Slått på|Slått på|Avansert|  

Finn ut mer under [Utgående lagerflyt](design-details-outbound-warehouse-flow.md).

Denne artikkelen refererer til metode D i tabellen. Hvis du vil finne ut mer om levering av varer, går du til [Lever varer](warehouse-how-ship-items.md).

Når en lokasjon er satt opp til å bruke plukkbehandling og lagerleveringsbehandling, kan du bruke plukkdokumentene til å opprette og behandle plukkopplysningene før du bokfører lagerleveringen.  

Du kan ikke opprette et lagerplukkdokument fra bunnen av. Plukk er en del av en arbeidsflyt der personen som behandler en ordre, oppretter dem på en push-måte, eller den lageransatte oppretter dem på en pull-måte:

- På push-måte der du bruker **Opprett plukk**-handlingen på siden **Lagerlevering**. Velg linjene som skal plukkes, og klargjør plukkingene ved å angi hvilke hyller det skal tas fra og hvilke det skal plasseres i, og hvor mange enheter som skal håndteres. Hyllene kan være forhåndsdefinert for lagerlokasjonen eller ressursen.
- I en pull-måte der du bruker **Frigi**-handlingen på siden **Lagerlevering** til å gjøre varene tilgjengelig for plukking. Deretter på siden **Plukkforslag** kan lageransatte bruke handlingen **Hent lagerdokumenter** til å hente tildelte plukkinger.

> [!NOTE]  
> Plukking for en lagerlevering av varer som er montert for en ordre følger samme fremgangsmåte som for vanlig lagerplukking for leveringer, som beskrevet i denne artikkelen. Antall plukklinjer for antallet som skal leveres, kan imidlertid være mange til én fordi du plukker komponentene, ikke den monterte varen.  
>
> Lagerplukklinjer opprettes for verdien i **Restantall**-feltet på linjene i monteringsordren som er knyttet til ordrelinjen som skal leveres. Alle komponentene er plukket i én handling. Finn ut mer under [Håndtere montere-til-ordre-varer i lagerleveringer](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).  
>  
> Hvis du vil finne ut mer plukking av komponenter for monteringsordrer, inkludert situasjoner der monteringsvarer ikke er knyttet til salgsforsendelse, går du til [Plukk for produksjon, montering eller prosjekter i avanserte lageroppsett](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a><a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a><a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Slik oppretter du plukkdokumenter i bulk med plukkforslaget

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Plukkforslag**, og velg deretter den relaterte koblingen.  

2. Velg handlingen **Hent lagerdokumenter**.  

    Oversikten tar med alle forsendelser som er frigitt for plukking, inkludert de som det allerede er opprettet plukkinstruksjoner for. Dokumenter med plukklinjer som er fullstendig plukket og registrert, blir ikke vist i denne oversikten.  
3. Velg de følgesedlene du vil forberede plukking for.

    > [!NOTE]  
    >  Hvis du prøver å velge en levering eller intern plukkdokument som du allerede har opprettet instruksjoner for alle linjene, får du en melding om at det ikke er noe å håndtere. Hvis du vil kombinere lagerplukkinstruksjoner som du allerede har opprettet, til én plukkinstruksjon, må du slette de individuelle plukkingene først.

4. Fyll ut feltet **Sorteringsmetode** for å sortere linjene.  

    > [!NOTE]  
    >  Måten linjene blir sortert på i forslaget, overføres ikke automatisk ved plukkinstruksen. Det finnes imidlertid de samme mulighetene for sortering og hylleprioritering. Du kan enkelt opprette linjeordren du planlegger i forslaget på nytt, når du oppretter plukkinstruksjonene eller sortering i plukkinstruksjonene.

5. Fyll ut feltet **Ant. som skal håndt.** eller manuelt, eller ved hjelp av **Autoutfyll ant som skal håndt.**-handlingen.  

    Siden viser antall som er tilgjengelig i kryssoverføringshyller. Denne informasjonen er nyttig når du skal planlegge arbeidsoppgaver i situasjoner for kryssoverføring. [!INCLUDE[prod_short](includes/prod_short.md)] foreslår alltid en plukking fra en kryssoverføringshylle først.
6. Rediger linjene om nødvendig. Du kan også slette linjene for gjør plukk mer effektiv. Hvis det for eksempel finnes flere linjer med varer som er i kryssoverføringshyller, er det mulig at du vil opprette en plukking for alle linjene. De kryssoverførte varene vil bli levert med andre varer på forsendelsen, og kryssoverføringshyllene vil ha plass til flere inngående varer.  

    > [!NOTE]  
    >  Hvis du sletter linjer, slettes de bare fra forslaget. De slettes ikke fra plukkvalglisten.  

7. Velg handlingen **Opprett plukk**. Siden **Opprett plukk** åpnes, der du kan legge til mer informasjon i plukkingen du oppretter. Angi hvordan du kombinerer plukklinjer i plukkdokumentene ved å velge ett av følgende alternativer.  

    |Alternativ|Beskrivelse|
    |-|-|
    |Per lager Dokument|Oppretter separate plukkdokumenter for forslagslinjer med samme lagerkildedokumentet.|
    |Per kund/levrd/lok|Opprett separate plukkdokumenter for hver kunde (ordrer), leverandør (bestillingsreturer) og lokasjon (overføringsordrer).|
    |Per vare|Opprett separate plukkdokumenter for hver vare i plukkforslaget.|
    |Per fra-sone|Opprett separate plukkdokumenter for hver sone du vil plukke varer fra.|
    |Per hylle|Opprett separate plukkdokumenter for hver hylle du vil plukke varer fra.|
    |Per forfallsdato|Opprett separate plukkdokumenter for kildedokumenter som har samme forfallsdato.|

    Angi hvordan plukkdokumentene skal opprettes, ved å velge blant følgende alternativer.

    |Alternativ|Beskrivelse|
    |-|-|
    |Maks Antall plukklinjer|Oppretter plukkdokumenter som ikke har flere enn det angitte antallet linjer i hvert dokument.|
    |Maks Antall plukkildedok.|Oppretter plukkdokumenter som hver for seg ikke dekker mer enn det angitte antallet kildedokumenter.|
    |Tilordnet bruker-ID|Oppretter plukkdokumenter bare for forslagslinjer som er tilordnet til den valgte lageransatte.|
    |Sorteringsmetode for plukklinjer|Velg fra de tilgjengelige alternativene for å sortere linjene plukkdokumentet som er opprettet.|
    |Angi anbrekksfilter|Skjuler midlertidige anbrekksplukklinjer når en større enhet konverteres til en mindre enhet og plukkes ferdig.|
    |Ikke fyll ut ant. som skal hnd|Lar feltet Ant. som skal håndt. være tomt i de opprettede plukklinjene.|
    |Skriv ut plukk|Skriver ut plukkdokumenter når de opprettes. Du kan også skrive ut fra de opprettede plukkdokumentene.|

8. Velg **OK**. [!INCLUDE [prod_short](includes/prod_short.md)] oppretter plukkingen i henhold til valgene dine.  

## <a name="to-pick-items-for-a-warehouse-shipment"></a><a name="to-pick-items-for-a-warehouse-shipment"></a><a name="to-pick-items-for-a-warehouse-shipment"></a>Plukke varer for en lagerlevering

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplukk** og velg den relaterte koblingen.  

    Hvis du skal arbeide med en bestem plukking, velger du plukkingen fra oversikten eller filtrerer oversikten for å finne plukkingene som er tilordnet spesielt til deg. Åpne kortet for plukkingen.  
2. Hvis feltet **Tildelt bruker-ID** er tomt, angir du om nødvendig ID-en for å identifisere deg selv.  
3. Plukke varene.  

    Hvis lageret er definert slik at hyller brukes, brukes varenes standardhyller til å foreslå hvor du skal ta varene fra. Instruksjonene inneholder minst to separate linjer for handlingene Hent og Plasser.  

    Hvis lageret er definert slik at lagerstyring brukes, brukes hylleprioriteringen til å beregne de beste hyllene å plukke fra. Disse hyllene foreslås på plukklinjene. Instruksjonene inneholder minst to separate linjer for handlingene Hent og Plasser.  

    * Den første linjen, med **Hent** i **Handlingstype**-feltet, angir hvor varene er plassert i plukkområdet. Hvis du leverer et stort antall varer på én leveringslinje, kan det hende at du må plukk varene i flere hyller, det finnes derfor en Hent-linje for hver hylle.
    * Den neste linjen, med **Plasser** i **Handlingstype**-feltet, viser hvor du må plassere varene i lageret. Du kan ikke endre sonen og hyllen på denne linjen.

    > [!NOTE]
    > Hvis du må plukke eller plassere varene for én linje i mer enn én hylle, for eksempel fordi den angitte hyllen er full, bruker du handlingen **Del linje** i hurtigfanen **Linjer**. Handlingen oppretter en linje der restantallet skal håndteres.

4. Når du har utført plukkingen og plassert varene i leveringsområdet eller leveringshyllen, velger du **Registrer plukk**-handlingen.  

Du kan nå hente varene til leveringssonen og bokføre leveringen, inkludert det relaterte kildedokumentet, på siden **Lagerlevering**. Finn ut mer under [Lever varer](warehouse-how-ship-items.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/pick-ship-items-warehouse/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
