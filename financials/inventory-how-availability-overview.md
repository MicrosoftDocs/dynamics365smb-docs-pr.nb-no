---
title: "Få en oversikt over tilgjengelighet| Microsoft-dokumentasjon"
description: "Beskriver hvordan du viser tilgjengeligheten av varer på tvers av lokasjoner per salg eller kjøpshendelser etter en tidsperiode, eller ved varens posisjon i en monteringsstykkliste."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 03/28/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 47071e5e325de8a31663b8d5a59d1ce93e5d0111
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-get-an-availability-overview"></a>Få en oversikt over tilgjengelighet
Fra konteksten for en forretningsoppgave kan du få avansert informasjon om når og hvor en vare er tilgjengelig, for eksempel når du snakker med en kunde om en leveringsdato.

Du kan vise tilgjengeligheten for alle varer per lokasjon, og du kan vise tilgjengeligheten av hver vare etter hendelse, periode eller lokasjon. En hendelse er alle planlagte varetransaksjoner, for eksempel en følgeseddel eller mottak av inngående overføring.

**Merk**: Tilgjengelighetsvisninger etter lokasjon krever at du har beholdning på mer enn én lokasjon. Hvis du vil ha mer informasjon, kan du se [Definere lokasjoner](inventory-how-setup-locations.md).

I [Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] vises tilgjengelighetstallene i to forskjellige felt, hver med en forskjellig definisjon:

* **Beholdning**-feltet viser det faktiske antallet i dag i henhold til bokførte vareposter.
* Feltet **Beregnet disponibel beholdning** beregnes og viser antallet på lager pluss planlagte mottak minus bruttobehov. (I [Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] inkluderer planlagte mottak antall bestillinger og inngående overføringsordrer. Bruttobehov inkluderer antall på salgsordrer og utgående overføringsordrer.)

**Tips**: Beregnet disponibel saldo er spesielt relevant å vise i vinduene **Varetilgjengelighet per periode** og **Varetilgjengelighet per hendelse** fordi de inneholder datodimensjonen.  

**Merk**: Fremgangsmåtene nedenfor viser hvordan du viser avansert informasjon om tilgjengelighet fra varelisten og varekortet. Du har også tilgang til informasjon fra salgsdokumentlinjer for varen på linjen. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Slik viser du tilgjengeligheten for en vare i henhold til når den blir mottatt eller levert
Du viser tilgjengeligheten for en vare i henhold til planlagte varetransaksjoner i vinduet **Tilgjengelighet per hendelse**.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Varer**, og deretter velger du den beslektede koblingen.
2. Åpne kortet for en vare som du vil vise varetilgjengelighet for.
3. Velg handlingen **Varetilgjengelighet per**, og velg deretter **Hendelse**-handlingen.

    Vinduet **Varetilgjengelighet per hendelse** viser hvordan lagerantall for varen vil utvikle seg over tid i henhold til planlagte hendelser for levering og mottak. Vinduet gir en konsentrert visning som viser én linje med akkumulert informasjon per tidsintervall hvor lagerantallet endres. Tidsintervaller som det ikke har oppstått noen hendelser i, vises ikke. Du kan utvide hver linje for å vise detaljer om hendelsen eller hendelsene som forårsaket det akkumulerte antallet på linjen.
4. Velg verdien i feltet **Beregnet disponibel beholdning** for å vise vareposter eller åpne dokumenter som utgjør verdien.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Slik viser du tilgjengeligheten for en vare i forskjellige perioder
Du viser tilgjengeligheten for en vare over tid for bestemte tidsperioder i vinduet **Varetilgjengelighet per periode**.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Varer**, og deretter velger du den beslektede koblingen.
2. Åpne kortet for en vare som du vil vise varetilgjengelighet for.
3. Velg handlingen **Varetilgjengelighet per**, og velg deretter **Periode**-handlingen.

    Vinduet **Varetilgjengelighet per periode** viser hvordan lagerantallet for varen vil utvikler seg over tid, vist for en periode som du velger, for eksempel dag, uke eller kvartal.
4. Velg verdien i feltet **Beregnet disponibel beholdning** for å vise vareposter eller åpne dokumenter som utgjør verdien.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Slik viser du tilgjengeligheten for en vare på lokasjonene der den er lagret
Du viser tilgjengeligheten for en vare på de forskjellige lokasjonene der den er lagret, i vinduet **Varetilgjengelighet per lokasjon**.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Varer**, og deretter velger du den beslektede koblingen.
2. Åpne kortet for en vare som du vil vise varetilgjengelighet for.
3. Velg handlingen **Varetilgjengelighet per**, og velg deretter **Lokasjon**-handlingen.

    Vinduet **Varetilgjengelighet per lokasjon** viser hvordan lagerantallet for varen vil utvikle seg i fremtiden, vist for hver lokasjon der den er lagret.
4. Velg verdien i feltet **Disponibel beholdning** for å vise vareposter som utgjør verdien.
5. Velg verdien i feltet **Beregnet disponibel beholdning** for å vise vareposter eller åpne dokumenter som utgjør verdien.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Slik viser du tilgjengeligheten for alle varer på lokasjonen der de er lagret
Du kan vise tilgjengeligheten til alle varer på tvers av alle lokasjoner i vinduet **Varer per lokasjon**.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Varer**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Varer per lokasjon**.

    Vinduet **Varer per lokasjon** vises for alle varer hvor mange som er tilgjengelig på hver lokasjon.
3. Velg verdien i feltet **Disponibel beholdning** for å vise vareposter som utgjør verdien.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-boms"></a>Vise tilgjengeligheten til en vare etter bruk i monteringsstykklister
Hvis det finnes en vare i monteringsstykklister, enten som en overordnet vare eller som en komponent, kan du se hvor mange enheter av varen som er påkrevd i vinduet **Varetilgjengelighet per stykklistenivå**. Vinduet viser hvor mange enheter av en overordnet vare du kan lage basert på tilgjengeligheten av underordnede varer på underliggende linjer. Varene som har en monteringsstykkliste, vises i vinduet som en linje som kan skjules. Du kan utvide denne linjen for å se de underliggende komponentene og delmonteringer på lavere nivå med sine egne stykklister.

Du kan bruke vinduet for å finne ut om du kan oppfylle en ordre for en vare på en angitt dato. Du gjør dette ved å se på varens gjeldende tilgjengelighet og antallene som kan leveres av varens komponenter. Du kan også bruke vinduet til å identifisere flaskehalser i relaterte monteringsstykklister.

På hver linje i vinduet for både overordnede og underordnede varer angir følgende nøkkelfelt tilgjengelighetstall. Du kan bruke disse tallene for å bekrefte hvor mange enheter av en overordnet vare du kan levere hvis du starter den relaterte monteringsprosessen.

|Felt|Beskrivelse|
|------|-----------|
|**Kan lage overordnet**|Viser hvor mange enheter av en hvilken som helst delmontering i toppvaren du kan lage. Feltet angir hvor mange umiddelbare overordnede enheter du kan montere. Verdien er basert på tilgjengeligheten av varen på linjen.|
|**Kan lage toppvare**|Viser hvor mange enheter av toppvaren du kan lage. Feltet angir hvor mange enheter av stykklistevaren på øverste linje som du kan montere. Verdien er basert på tilgjengeligheten av varen på linjen.|

Vinduet **Varetilgjengelighet per stykklistenivå** viser informasjon for varen på kortet eller dokumentlinjen som vinduet er åpnet for. Varen vises alltid på øverste linje. Du kan vise informasjon for andre varer eller for alle varer ved å endre verdien i feltet **Varefilter**.

**Merk**: Som standard viser tilgjengelighetsfigurer på linjene den totale tilgjengeligheten for alle varene under den øverste varen. Disse tallene vises i feltet **Disponibelt antall**, og fokus er på toppvaren. Informasjon om hvor mange halvfabrikater du kan lage, kan imidlertid være skjevt. For å få en realistisk indikasjon om hvor mange av de viste delmonteringene du kan lage, må du fjerne merket for **Vis samlet tilgjengelighet** og deretter se tallet i feltet **Kan lage overordnet**.

Feltet **Flaskehals** angir hvilken vare i stykklistestrukturen som hindrer deg i å opprette et større antall enn antallet som vises i feltet **Kan lage toppvare**. Flaskehalsen kan for eksempel være en innkjøpt komponent med forventet mottaksdato som er for sen til å lage ekstra enheter av toppvaren etter datoen i feltet **Trengs innen dato**.

## <a name="see-also"></a>Se også
[Håndtere lager](inventory-manage-inventory.md)  
[Arbeide med stykklister](inventory-how-work-BOMs.md)    
[Definere lokasjoner](inventory-how-setup-locations.md)  
[Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md)  
[Selge produkter](sales-how-sell-products.md)      
[Forsyningskjede](madeira-supply-chain.md)  
[Arbeide med Financials](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

