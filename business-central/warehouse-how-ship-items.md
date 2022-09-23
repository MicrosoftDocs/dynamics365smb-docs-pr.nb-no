---
title: Levere varer
description: Denne artikkelen beskriver hvordan du leverer varer fra lageret, avhengig av lagerkonfigurasjonen for leveringsbehandling.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7335, 7337, 7339, 7340, 7341, 7362, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: b66a0a0a4cad12c4f41c53569b0007c51e846de7
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531219"
---
# <a name="ship-items"></a>Levere varer

Når du leverer varer fra et lager som ikke er definert til lagerleveringsbehandling, må du ganske enkelt registrere leveringen i det relaterte forretningsdokumentet, for eksempel en ordre, serviceordre, bestillingsretur eller utgående overføringsordre.

Når du leverer varer fra et lager som er definert for lagerleveringsbehandling, kan du bare levere varer basert på kildedokumenter som andre enheter i selskapet har frigitt til lageret for behandling.

> [!NOTE]
> Hvis lageret bruker kryssoverføring og hyller for hver linje, kan du vise antall varer plassert i kryssoverføringshyllene. Programmet beregner disse antallene automatisk hver gang feltene på følgeseddelen oppdateres. Hvis dette er varer som gjelder for den leveringen du forbereder, kan du opprette en plukking for alle linjene, og deretter fullføre leveringen. Finn ut mer under [Kryssoverføringsvarer](warehouse-how-to-cross-dock-items.md).

## <a name="ship-items-with-a-sales-order"></a>Lever varer med en ordre

Fremgangsmåten nedenfor beskriver hvordan du leverer varer fra en ordre. Fremgangsmåten er lik for bestillingsreturer, serviceordrer og utgående overføringsordrer.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Åpne en eksisterende ordre eller opprett en ny. Finn ut mer under [Selg produkter](sales-how-sell-products.md).
3. I feltet **Levere (antall)** angir du det leverte antallet.

    Verdien i feltet **Levert ant.** oppdateres. Hvis dette er en delvis levering, vil verdien være mindre enn verdien i feltet **Antall**. Finn ut mer under [Behandle delvise leveringer](sales-how-send-partial-shipments.md).
4. Velg handlingen **Bokfør**.

> [!NOTE]
> Hvis organisasjonen ikke bruker ordrer, antar [!INCLUDE [prod_short](includes/prod_short.md)] at du har levert hele antallet når du bokfører salgsfakturaen. Hvis dette er i strid med hvordan organisasjonen arbeider, anbefaler vi at du bruker ordrer og registrerer leveringer som forklart i denne artikkelen.

## <a name="ship-items-with-a-warehouse-shipment"></a>Lever varer med en lagerlevering

Først oppretter du et leveringsdokument fra et forretningskildedokument. Deretter plukker du de angitte varene for leveringen.

### <a name="create-a-warehouse-shipment"></a>Opprett en lagerlevering

Vanligvis er det den ansatte som er ansvarlig for leveringer, som oppretter en lagerlevering. Følgende fremgangsmåte viser hvordan du oppretter leveringen manuelt i standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)]. Organisasjonen kan imidlertid ha automatisert en del av prosessen, for eksempel med bruk av håndholdte eller monterte skannere som støttes av eksterne leverandører.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerleveringer** og velg den relaterte koblingen.  
2. Velg **Ny**.  

    Fyll ut feltene på hurtigfanen **Generelt**. Når du mottar kildedokumentlinjer, kopieres noe av informasjonen til hver linje.  

    For et lager konfigurert med lagerstyring: Hvis lokasjonen har en standard sone og hylle for leveringer, fylles feltene **Sonekode** og **Hyllekode** ut automatisk, men du kan endre dem slik det passer.  

    > [!NOTE]  
    > Hvis du vil levere varer med andre lagerklassekoder enn lagerklassekoden til hyllen i feltet **Hyllekode** i dokumenthodet, må du slette innholdet i feltet **Hyllekode** før du henter kildedokumentlinjene for varene.  
3. Velg handlingen **Hent kildedokumenter**. Siden **Kildedokumenter** åpnes.

    Fra en ny eller åpen lagerlevering kan du bruke siden **Filtre for henting av kildedok** til å hente linjene i det frigitte kildedokument som definerer hvilke varer som skal leveres.

    1. Velg handlingen **Bruk filtre til å hente k.dok...**.  
    2. Hvis du vil definere et nytt filter, angir du en beskrivende kode i feltet **Kode** og velger deretter handlingen **Endre**.  
    3. Definer typen kildedokumentlinjer som du vil hente, ved å fylle ut de relevante filterfeltene.  
    4. Velg handlingen **Kjør**.  

    Alle frigitte kildedokumentlinjer som oppfyller filterkriteriene, settes nå inn på siden **Lagerlevering** der du aktiverte filterfunksjonen.  

    Filterkombinasjonene du definerer, lagres på siden **Filtre for henting av kildedok** til neste gang du trenger dem. Du kan opprette et ubegrenset antall filterkombinasjoner. Du kan når som helst endre kriteriene ved å velge handlingen **Endre**.

4. Velg kildedokumentene som du vil levere varer for, og velg deretter **OK**.  

Linjene i kildedokumentet vises på siden **Lagerlevering**. Feltet **Levere (antall)** er fylt ut med antall utestående for hver linje, men du kan endre antallet slik det er nødvendig. Hvis du sletter innholdet i feltet **Hyllekode** i hurtigfanen **Generelt** før du henter linjene, må du fylle ut riktig hyllekode på hver leveringslinje.  

> [!NOTE]  
> Du kan ikke levere flere varer enn det som er angitt i feltet **Restantall** på kildedokumentlinjen. Hvis du vil levere flere varer, må du hente et annet kildedokument som inneholder en linje for den samme varen.  

Når du har de linjene du vil levere, kan du starte prosessen som sender linjene til lageransatte for plukking.

### <a name="pick-and-ship"></a>Plukk og lever

Vanligvis er det en lagermedarbeider som er ansvarlig for plukking, som oppretter et plukkdokument eller åpner et allerede opprettet plukkdokument.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerleveringer** og velg den relaterte koblingen.
2. Velg lagerlevringen som du vil plukke for, og velg deretter **Opprett plukk**-handlingen.
3. Fyll ut feltene på forespørselssiden, og velg deretter **OK**. Det angitte lagerplukkdokumentet opprettes.

    Du kan også åpne et eksisterende lagerplukkdokument.
4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Plukking** og velger den relaterte koblingen. Velg plukkingen du vil arbeide med.

    Hvis lageret definert for bruk av hyller, så er plukklinjene konvertert til linjer for henting og plassering.

    Hvis du bruker lagerstyring, kan du sortere linjene, tildele en ansatt til plukkingen, definere et anbrekksfilter, og plukke og skrive ut plukkinstruksjonene.

5. Utfør den faktiske plukkingen av varer, og plasser dem i den angitte leveringshyllen eller i leveringsområdet hvis du ikke har hyller.
6. Velg handlingen **Registrer plukk**.

    Feltet **Levere (antall)** og feltet **Dokumentstatus** i hodet for leveringsdokumentet oppdateres. Varene du har plukket, er ikke lenger tilgjengelige for andre ordrer for plukking eller for interne operasjoner.
7. Skriv ut leveringsdokumentene, forbered leveringspakkene og bokfør deretter leveringen.

Hvis du vil vite mer informasjon om hvordan du plukker for lagerlevering, kan du se [Plukk varer for lagerlevering](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Du kan også bruke plukkforslaget til å gjøre flere plukkinstruksjoner om til én instruksjon (for flere leveringer), og derved forbedre effektiviteten for plukkingen i lageret. Finn ut mer under [Planlegg plukk i forslag](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Hvis du venter på at en bestemt vare skal ankomme lageret og du bruker kryssoverføringsfunksjonalitet, så beregner [!INCLUDE[prod_short](includes/prod_short.md)] antallet for varen som er i kryssoverføringshyllen på hver følgeseddel- eller plukkforslagslinje. Dette feltet oppdateres hver gang du går ut av eller åpner følgeseddelen eller forslaget. Finn ut mer under [Kryssoverføringsvarer](warehouse-how-to-cross-dock-items.md).

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/ship-invoice-items-dynamics-365-business-central/).

## <a name="see-also"></a>Se også

[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
