---
title: Motta varer
description: Denne artikkelen er en oversikt over ulike måter å motta varer på i et lager med lagermottak.
author: brentholtorf
ms.author: bholtorf
ms.topic: how-to
ms.date: 09/02/2022
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008'
---
# <a name="receive-items-with-warehouse-receipts"></a><a name="receive-items-with-warehouse-receipts"></a>Motta varer med et lagermottak

I [!INCLUDE[prod_short](includes/prod_short.md)] mottar du varer og plasserer dem ved å bruke en av fire metoder, som beskrevet i tabellen nedenfor.

|Prinsipp|Inngående prosess|Krev kvitteringer|Krev plasseringer|Kompleksitetsnivå (Finn ut mer under [Oversikt over Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokføre mottak og plassering fra ordrelinjen|||Ingen dedikert lageraktivitet.|  
|B|Bokføre mottak og plassering fra et lagerplasseringsdokument||Slått på|Grunnleggende: ordre for ordre.|  
|U|Bokføre mottak og plassering fra et lagermottaksdokument|Slått på||Grunnleggende: konsolidert mottak/levering for flere ordrer.|  
|D|Bokføre mottak fra et lagermottaksdokument og bokføre plassering fra et lagerplasseringsdokument|Slått på|Slått på|Avansert|  

Hvis du vil ha mer informasjon om hvordan du håndterer inngående varer, går du til [Inngående lagerflyt](design-details-inbound-warehouse-flow.md).

Følgende artikkel refererer til metode C og D i forrige tabell.

## <a name="receive-items-with-a-warehouse-receipt"></a><a name="receive-items-with-a-warehouse-receipt"></a>Motta varer med et lagermottak

Når varene ankommer et lager som er definert til å behandle lagermottak, må du hente linjene i kildedokumentet som utløste mottaket. Hvis du bruker hyller, kan du enten godta standardhyllen eller angi hyllen som varene skal plasseres i. Det siste kan være nødvendig når du mottar en vare for første gang. Deretter må du angi antall varer du har mottatt, og bokføre mottaket.  

Du kan opprette lagermottak på en av to måter:

* På en push-måte, når arbeid gjøres på ordre-for-ordre-basis. Velg handlingen **Opprett lagermottak** i kildedokumentet, for eksempel en bestilling, ordreretur eller overføringsordre, for å opprette et lagermottak for ett kildedokument.
* I en pull-måte, der du bruker handlingen **Frigi** i kildedokumentet, for eksempel en bestilling, ordreretur eller overføringsordre til å frigi dokumentet til lageret. En lageransatt oppretter et **lagermottak** for et eller flere frigitte kildedokumenter. Følgende fremgangsmåte forklarer hvordan du oppretter et lagermottak på en pull-måte. Følgende fremgangsmåte forklarer hvordan du oppretter et lagermottak på en pull-måte.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagermottak** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**.  

    Fyll ut feltet **Lokasjonskode** på hurtigfanen **Generelt**. Når du mottar kildedokumentlinjer, kopieres noe av informasjonen til hver linje.

    For en lokasjon som krever hyller, fyller du feltet **Hyllekode**. [!INCLUDE[prod_short](includes/prod_short.md)] kan legge til hyllekoden for deg, avhengig av oppsettet. Finn ut mer under [Sone- og hyllekoder](warehouse-how-receive-items.md#zone-and-bin-codes).  

3. Du kan hente kildedokumentet på to måter:

    1. Velg handlingen **Hent kildedokumenter**. Siden **Kildedokumenter – inngående** åpnes. Her kan du velge et eller flere kildedokumenter som er frigitt til lageret, som krever mottak.
    2. Velg handlingen **Bruk filtre til å hente k.dok...**. Siden **Filtre for å hente kildedokumenter – inngående** åpnes. Her kan du velge kildedokumentfilter og kjøre det. Alle frigitte kildedokumentlinjer som oppfyller filterkriteriene, legges til på siden **Lagermottak**. Finn ut mer under [Bruke filtre til å hente kildedokumenter](warehouse-how-receive-items.md#how-to-use-filters-to-get-source-documents).

4. Sett antallet som skal mottas.

    Feltet **Motta (antall)** inneholder antall utestående for hver linje, men du kan endre antallet slik det er nødvendig. 

    Når du skal angi verdien i **Motta (antall)**-feltet på alle linjene til null, velger du handlingen **Slett antall som skal mottas**. Det kan for eksempel være nyttig å sette antallene til null hvis du bruker en strekkodeskanner til å oppdatere de mottatte antallene. Hvis du vil legge til restantallet fra kildedokumentet igjen, velger du handlingen **Autoutfyll ant som skal mottas**.  

    I et lagermottaksdokument der det mottatte antallet er høyere enn bestilt, angir du det faktiske mottatte antallet i feltet **Motta (antall)**. Hvis økningen er innenfor toleransen som er angitt av en tildelt overmottakskode, oppdateres feltet **Antall overmottak** til å vise antallet som verdien i feltet **Aantall** er overskredet med. Hvis økningen er over toleransen, er ikke overmottak tillatt.

5. Bokfør lagermottaket. Antallsfeltene oppdateres i kildedokumentene, og varene legges til i beholdningen.  

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

    > [!TIP]
    > Hvis du bruker lagerplassering, som refererer til metode D i tabellen i begynnelsen av denne artikkelen, mottas varene, men de kan ikke plukkes før de er plassert. Hvis du vil lære mer om hvordan du plasserer varer, går du til [Plasser varer med lagerplasseringer](warehouse-how-to-put-items-away-with-warehouse-put-aways.md).
    >
    > Du kan også vurdere å bruke handlingen **Bokfør og skriv ut**. Handlingen bokfører mottak og skriver det ut som en plasseringsinstruksjon som viser hvor varen skal plasseres.

    > [!NOTE]  
    > Hvis lageret bruker kryssoverføring, kan du kontrollere om du kan kryssoverføre varer uten å plassere dem. Hvis du vil finne ut mer om kryssoverføring, går du til [Kryssoverfør varer](warehouse-how-to-cross-dock-items.md).

## <a name="how-to-use-filters-to-get-source-documents"></a><a name="how-to-use-filters-to-get-source-documents"></a>Bruke filtre til å hente kildedokumenter

Fra et lagermottak kan du bruke siden **Filtre for henting av kildedokumenter** til å hente linjene i det frigitte kildedokument som angir varer som skal mottas.

1. I lagermottaket velger du handlingen **Bruk filtre til å hente k.dok.**.
2. Hvis du vil definere et nytt filter, angir du en beskrivende kode i feltet **Kode** og velger deretter handlingen **Endre**.

    Siden **Filterkort for kildedokument – inngående** vises.

3. Bruk filtre til å definere hvilken type kildedokumentlinjer som skal hentes. Du kan for eksempel velge ulike typer kildedokumenter, for eksempel bestillinger eller overføringsordrer.
4. Velg **Kjør**.  

Alle frigitte kildedokumentlinjer som oppfyller filterkriteriene, legges til på siden **Lagermottak** der du aktiverte filtrene.

Du kan opprette et ubegrenset antall filterkombinasjoner. Filtrer lagres på siden **Filtre for henting av kildedok**, og de er tilgjengelige neste gang du trenger dem. Du kan når som helst endre kriteriene ved å velge handlingen **Endre**.

## <a name="zone-and-bin-codes"></a><a name="zone-and-bin-codes"></a>Sone- og hyllekoder

Hvis du vil motta varer med andre lagerklassekoder enn lagerklassekoden til hyllen i feltet **Hyllekode** i dokumenthodet, må du fjerne feltet **Hyllekode** fra hodet før du henter kildedokumentlinjene for varene.  
<!-- TBD, table with comparison of various options-->

Hvis hyller er obligatoriske for lokasjon, legges sone- og hyllekoder til i lagermottaksdokumenter på følgende måte:

* For avanserte oppsett som bruker lagerstyring, bruker [!INCLUDE [prod_short](includes/prod_short.md)] mottakshyllekoden på siden **Lokasjonskort** for lokasjonen. Hvis det ikke er angitt noen mottakshyllekode, angis ingen hylle. Hvis varen og mottakshyllene ikke samsvarer, er koden for mottakshyllen tom.
* Hvis det er angitt en mottakshyllekode i andre konfigurasjoner, bruker [!INCLUDE [prod_short](includes/prod_short.md)] hyllekoden fra kildedokumentet.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a>Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
