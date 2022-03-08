---
title: Plukke varer for lagerlevering | Microsoft-dokumentasjon
description: Når lokasjonen er satt opp til å bruke plukkbehandling og i tillegg lagerleveringsbehandling, kan du bruke plukkdokumentene til å opprette og behandle plukkopplysningene før lagerleveringen bokføres.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d35c6dec3eee09ec72a09325dcc527c18dc9b8c4
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876682"
---
# <a name="pick-items-for-warehouse-shipment"></a>Plukke varer for lagerlevering
Når lokasjonen er satt opp til å bruke plukkbehandling og i tillegg lagerleveringsbehandling, kan du bruke plukkdokumentene til å opprette og behandle plukkopplysningene før lagerleveringen bokføres.  

Du kan ikke opprette et lagerplukkdokument fra grunnen av fordi en plukkaktivitet alltid er en del av en arbeidsflyt, enten i et pull- eller push-scenario.  

Du kan opprette lagerplukkdokumenter på en hentemåte ved å åpne et tomt lagerleveringsdokument, finne kildedokumenter som er frigitt for levering og deretter opprette lagerplukklinjer for disse leveringene. Du kan bruke funksjonene **Hent kildedokumenter** eller **Bruk filter til å hente kildedokumenter** for å finne kildedokumenter som er klare for levering.

Du kan også bruke siden **Plukkforslag** til å hente og opprette plukklinjer i satsvis modus. Hvis du vil ha mer informasjon, kan du se [Planlegge plukkinger i forslaget](warehouse-how-to-plan-picks-in-worksheets.md)  

Du kan også opprette lagerplukkdokumenter på en push-måte på siden **Lagerlevering** ved å velge **Opprett plukk**.  

> [!NOTE]  
>  Plukking for lagerlevering av varer som er montert til ordren som leveres følger samme fremgangsmåte som for vanlig lagerplukking for levering, som beskrevet i dette emnet. Antall plukklinjer per antall som skal leveres, kan imidlertid være mange til én fordi du plukker komponentene, ikke monteringsvaren.  
>   
>  Lagerplukklinjene opprettes for verdien i **Restantall**-feltet på linjene i monteringsordren som er knyttet til ordrelinjen som skal leveres. Dette sikrer at alle komponentene er plukket i én handling.  
>   
>  Hvis du vil ha mer informasjon, kan du se delen Håndtere montere-til-ordre-varer i lagerleveringer.  
>   
>  Hvis du vil ha informasjon om plukking av komponenter for monteringsordrer generelt, inkludert situasjoner der monteringsvaren ikke forfaller på en følgeseddel, kan du se [Plukke for produksjon eller montering](warehouse-how-to-pick-for-production.md).  

## <a name="to-pick-items-for-warehouse-shipment"></a>Plukke varer for lagerlevering  
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Plukking**, og velg deretter den relaterte koblingen.  

    Hvis du skal arbeide med en bestem plukking, velger du plukkingen fra oversikten eller filtrerer oversikten for å finne plukkingene som er tilordnet spesielt til deg. Åpne kortet for plukkingen.  
2.  Hvis feltet **Tilordnet bruker-ID** er tomt, angir du om nødvendig IDen for å identifisere deg selv.  
3.  Utfør den faktiske plukkingen av varer.  

    Hvis lageret er definert slik at hyller brukes, brukes varenes standardhyller til å foreslå hvor du skal ta varene fra. Instruksjonene blir vist som to separate linjer, minst én for hver handlingstype, Hent og Plasser.  

    Hvis lageret er definert slik at lagerstyring brukes, brukes hylleprioriteringen til å beregne de beste hyllene å plukke fra, og disse hyllene foreslås deretter på plukklinjene. Instruksjonene blir vist som to separate linjer, minst én for hver handlingstype, Hent og Plasser.  

4.  Når du har utført plukkingen og plassert varene i leveringsområdet eller leveringshyllen, velger du **Registrer plukk**-handlingen.  

Personen som er ansvarlig for leveringen, kan nå hente varene til leveringssonen og bokføre leveringen, inkludert det relaterte kildedokumentet, på siden **Lagerlevering**. Hvis du vil ha mer informasjon, kan du se [Levere varer](warehouse-how-ship-items.md).   

I tillegg til å plukke for kildedokumenter, som beskrives i dette emnet, kan du hente og plassere varer mellom hyller uten å referere til kildedokumenter. Hvis du vil ha mer informasjon, kan du se [Plukke og plassere uten et kildedokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md).  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Håndtere montere-til-ordre-varer i lagerleveringer
I montere-til-ordre-scenarier brukes feltet **Levere (antall)** på lagerleveringslinjer til å registrere hvor mange enheter som monteres. Det angitte antallet bokføres deretter som monteringsavgang når lagerleveringen er bokført.

Når det gjelder andre lagerfølgeseddellinjer, er verdien i feltet **Levere (antall)** null fra starten.

Når medarbeidere som er ansvarlige for montering, er ferdige med monteringen av deler av eller hele montere-til-ordre-antallet, registrerer de dette i feltet **Levere (antall)** på lagerleveringslinjen, og velger deretter handlingen **Bokfør følgeseddel**. Resultatet er at den tilsvarende monteringsavgangen bokføres, inkludert komponentforbruket. En følgeseddel for antallet som er postert for salgsordren.

Fra monteringsordren kan du velge **Monter til ordre – lagerfølgeseddellinje** for å få tilgang til lagerfølgeseddellinjen. Dette er praktisk for medarbeidere som vanligvis ikke bruker siden **Lagerlevering**.

Når lagerleveringen er bokført, oppdateres forskjellige felt på ordrelinjen for å vise fremdrift i lageret. Følgende felt oppdateres også for å vise hvor mange montere-til-ordre-antall som foreløpig ikke er montert og levert:

- **Restantall for ATO-lager**
- **Restantall for ATO-lager (lagerenhet)**

> [!NOTE]
> I kombinasjonsscenarier, der en del av antallet først må monteres og en annen del må leveres fra lager, opprettes to lagerleveringslinjer. Én er for montere-til-ordre-antallet og én er for varebeholdningen.

> I dette tilfellet håndteres montere-til-ordre-antallet som beskrevet i dette emnet, og lagerantallet håndteres som alle andre vanlige lagerleveringslinjer. Hvis du vil ha mer informasjon om Kombinasjonsscenarier, kan du se [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
