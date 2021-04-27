---
title: Plukke varer med lagerplukk | Microsoft-dokumentasjon
description: Hvis en lokasjon er definert til å kreve plukkbehandling, men ikke leveringsbehandling, bruker du lagerplukkdokumentene til å registrere og bokføre plukkings- og leveringsopplysninger for kildedokumentene.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7e8798f9581d3f0ae416a52bfdd53c7bb4893eab
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771707"
---
# <a name="pick-items-with-inventory-picks"></a>Plukke varer med lagerplukk

Når lokasjonen din er definert til å kreve plukkbehandling, men ikke leveringsbehandling, bruker du **Lagerplukk**-siden til å registrere og bokføre plukkings- og leveringsopplysninger for kildedokumentene. Det utgående kildedokument kan være en ordre, en bestillingsretur, en utgående overføringsordre eller en produksjonsordre som det skal plukkes komponenter til.

> [!NOTE]  
> Komponenter for monteringsordrer kan ikke plukkes eller bokføres med lagerplukk. Bruk i stedet siden **Lagerflytting**. Hvis du vil ha mer informasjon, kan du se [Flytte komponenter til et operasjonsområde i grunnleggende lagerstyring](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)
>
> Når du plukker og leverer salgslinjeantall som er montert til ordre, må du følge visse regler når du oppretter lagerplukklinjene. Hvis du vil ha mer informasjon, kan du se delen [Håndtere montere-til-ordre-varer med lagerplukk](#handling-assemble-to-order-items-with-inventory-picks).  

Du kan opprette lagerplukk på tre måter:  

- Opprett plukkingen i to trinn ved først å be om et lagerplukk ved å frigi kildedokumentet. Dette signaliserer til lageret at kildedokumentet er klart for plukking. Lagerplukket kan så opprettes på siden **Lagerplukk** basert på kildedokumentet.  
- Opprette lagerplukket direkte fra selve kildedokumentet  
- Du kan opprette lagerplukk for flere kildedokumenter samtidig ved hjelp av kjørselen.  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Be om et lagerplukk ved å frigi kildedokumentet

Når det gjelder ordrer, bestillingsreturer og utgående overføringsordrer, oppretter du lagerforespørselen ved å frigi ordren. Fremgangsmåten nedenfor beskriver hvordan dette gjøres fra en ordre.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.
2. Velg ordren som skal frigis, og velg deretter **Frigi**-handlingen.

Når det gjelder produksjonsordrer, oppretter du automatisk lagerforespørselen for plukking av komponenter, som kalles *trekk*, når produksjonsordrestatus endres til **Frigitt** eller når den frigitte produksjonsordren opprettes. Hvis du vil ha mer informasjon, kan du se [Plukke for produksjon eller montering](warehouse-how-to-pick-for-production.md).

Når lagerforespørselen er opprettet, kan lageransatte som er tilordnet arbeidet med å plukke varer, se at kildedokumentet er klart for plukking, og kan opprette nye plukkdokumenter basert på lagerforespørselen.  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Slik oppretter du et lagerplukk basert på kildedokumentet:

Nå som forespørselen er opprettet, kan den lageransatte opprette et nytt lagerplukk basert på det frigitte kildedokumentet.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerplukk**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
    Pass på at **Nr.** -feltet i hurtigfanen **Generelt** er fylt ut.
3. Velg hvilken type kildedokument du plukker for, i **Kildedokument**-feltet.  
4. Velg kildedokumentet i **Kildenr.**-feltet.  
5. Du kan også velge handlingen **Hent kildedokument** for å velge dokumentet fra en liste over utgående kildedokumenter som er klare for plukking på lokasjonen.  
6. Velg **OK**-knappen for å fylle ut plukklinjene i henhold til det valgte kildedokumentet.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Slik oppretter du et lagerplukk fra kildedokumentet

1. I kildedokumentet, som kan være en ordre, bestillingsretur, utgående overføringsordre eller produksjonsordre, velger du handlingen **Opprett lagerplassering/-plukking**.
2. Merk av for **Opprett lagerplukking**.  
3. Velg **OK**. Et nytt lagerplukk opprettes.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Slik oppretter du flere lagerplukk med en kjørsel:

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Opprett plassering/plukk for lager**, og velg deretter den relaterte koblingen.  
2. På hurtigfanen **Lagerforespørsel** bruker du filtrene **Kildedokumentet** og **Kildenr.** for å filtrere etter bestemte dokumenttyper eller dokumentnummerintervaller. Du kan for eksempel bare opprette plukk for ordrer.  
3. Merk av for **Opprett lagerplukking** på hurtigfanen **Alternativer**.
4. Velg **OK**. De angitte lagerplukkingene blir opprettet.

> [!NOTE]  
> Hvis du plukker og leverer salgslinjeantall som er montert til ordre, må du følge visse regler når du oppretter lagerplukklinjene. Hvis du vil ha mer informasjon, kan du se delen [Håndtere montere-til-ordre-varer med lagerplukk](#handling-assemble-to-order-items-with-inventory-picks).  
>
> I grunnleggende lageroppsett plukkes varer som er montert til ordrer, fra den relaterte ordren, som forklart i dette emnet. Hvis du vil ha mer informasjon, kan du se delen [Håndtere montere-til-ordre-varer med lagerplukk](#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="to-record-the-inventory-picks"></a>Slik registrerer du lagerplukk

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerplukk**, og velg deretter den relaterte koblingen.  
2. I **Hyllekode**-feltet på plukklinjene foreslås hyllen som varene skal plukkes fra, per varens standardhylle. Du kan endre hylle på denne siden hvis det er nødvendig.  
3. Utfør plukkingen, og angi opplysninger om det faktiske plasseringsantallet i feltet **Ant. som skal håndt**.

    Hvis varene for én linje må plukkes fra mer enn én hylle, for eksempel fordi de ikke er tilgjengelige i den angitte hyllen, bruker du funksjonen **Del linje** i hurtigfanen **Linjer**. Hvis du vil ha mer informasjon om deling av linjer, kan du se [Dele lageraktivitetslinjer](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Når du har utført plukkingen, velger du handlingen **Bokfør**.  

Bokføringsprosessen bokfører leveringen av kildedokumentlinjene som er plukket, eller bokfører forbruk når det gjelder produksjonsordrer. Hvis lokasjonen bruker hyller, oppretter bokføringen også lagerposter for bokføring av hylleantallendringer.  

## <a name="to-delete-inventory-pick-lines"></a>Slik sletter du lagerplukklinjer:

Hvis varer på lagerplukkingen ikke er tilgjengelige, kan du slette disse lagerplukklinjene etter bokføring og deretter slette lagerplukkdokumentet. Kildedokumentet, for eksempel en ordre eller en produksjonsordre, vil ha gjenværende varer som skal plukkes, som kan oppnås gjennom et nytt lagerplukk senere når varene blir tilgjengelige.  

> [!WARNING]  
> Denne prosessen kan ikke gjennomføres hvis serie-/partinumre er angitt i kildedokumentet. Hvis en ordrelinje for eksempel inneholder et serie-/partinummer, slettes denne varesporingsspesifikasjonen hvis du sletter en lagerplukklinje for serie-/partinummeret.  
>
> Hvis lagerplukklinjer har serie-/partinumre som ikke er tilgjengelige, må du ikke slette de aktuelle linjene. Du må i stedet endre **Ant. som skal håndt.**-feltet til null, bokføre faktiske plukk og så slette lagerplukkdokumentet. Dette sikrer at lagerplukklinjene for disse serie-/partinumrene kan gjenopprettes fra ordren senere.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Håndtere montere-til-ordre-varer med lagerplukk

**Lagerplukk**-siden brukes også til å plukke og levere for salg der varer må monteres før de kan leveres. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).

Varer som skal leveres er ikke fysisk til stede i en hylle før de er montert og bokført som avgang til en hylle i monteringsområdet. Dette betyr at plukking av monter-til-ordre-varer til levering følger en spesiell flyt. Lagermedarbeidere tar monteringsvarene fra en hylle til leveringssonen og bokfører deretter lagerplukkingen. Det bokførte lagerplukket bokfører deretter monteringsavgangen, komponentforbruket og følgeseddelen.

Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til å automatisk opprette en lagerflytting når lagerplukkingen for monteringsvaren opprettes. Hvis du vil aktivere dette, må du velge feltet **Opprett flyttinger automatisk** på siden **Monteringsoppsett**. Hvis du vil ha mer informasjon, kan du se [Flytte komponenter til et operasjonsområde i grunnleggende lagerstyring](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Lagerplukklinjer for salgsvarer opprettes på forskjellige måter avhengig av om ingen, noen eller alle salgslinjeantallene er montert til ordre.

Når du ved vanlig salg bruker lagerplukk til å bokføre levering av lagerantall, opprettes én lagerplukklinje for hver ordrelinje, eller flere hvis varen er plassert i forskjellige hyller. Denne plukklinjen er basert på antallet i **Levere (antall)**-feltet.

I montere-til-ordre-salg der hele antallet på ordrelinjen er montert til ordre, opprettes én lagerplukklinje for dette antallet. Dette betyr at verdien i feltet Antall å montere er det samme som verdien i feltet **Levere (antall)**. **Monter til ordre**-feltet er valgt på linjen.

Hvis en monteringsavgangsflyt er definert for lokasjonen, blir verdien i feltet **Hyllek. lev. fra m. til ordre** eller **Fra-Hyllekode for montering** satt inn (i denne rekkefølgen) i **Hyllekode-feltet på** lagerplukklinjen.

Hvis ingen hyllekode er angitt på ordrelinjen og ingen monteringsavgangsflyt er definert for lokasjonen, er **Hyllekode**-feltet på lagerplukklinjen tomt. Lagermedarbeideren må åpne **Hylleinnhold**-siden og velge hyllen der monteringsvarene er montert.

I kombinasjonsscenarier, der en del av antallet først må monteres og en annen del må plukkes fra lager, opprettes minst to lagerplukklinjer. Én plukklinje er til montere-til-ordre-antallet. Den andre plukklinjen avhenger av hvilke hyller som kan oppfylle det gjenværende antallet fra lageret. Hyllekoder på de to linjene er fylt ut på forskjellige måter som beskrevet for de to ulike salgstypene. Hvis du vil ha mer informasjon, kan du se delen "Kombinasjonsscenarier" i [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Se også

[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Gjennomgang: Plukking og levering i grunnleggende lageroppsett](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]