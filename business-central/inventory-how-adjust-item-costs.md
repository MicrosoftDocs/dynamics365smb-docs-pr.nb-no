---
title: Justere kostnadene for varer manuelt
description: Du kan manuelt justere lagerverdien for en vare med lagermetoden FIFO eller Gjennomsnitt, når kostnadene på produkter endres.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 7ed2e9ebad96d29c9fc2d73e426b6e37f577f9b9
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441221"
---
# <a name="adjust-item-costs"></a>Justere varekost
Kostnaden for en vare (lagerverdien) som du kjøper og senere selger, kan endres i løpet av levetiden, for eksempel fordi en fraktkostnader er lagt til innkjøpskostnaden etter at du har solgt varen. Kostjustering er spesielt relevant i situasjoner der du selger varer før du fakturerer kjøpet av varene. Hvis du alltid vil vite riktig lagerverdi, må varekostnader derfor justeres regelmessig. Dette sikrer at salgs- og fortjenestestatistikk er oppdatert og at økonomiske KPI-er er riktige. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Kostjustering](design-details-cost-adjustment.md).

Som en regel er verdien i **Enhetskost**-feltet på varekortet basert på standardkost for varer med standard lagermetode. For varer med andre lagermetoder er den basert på beregning av tilgjengelig lagerbeholdning (fakturerte kostnader og forventede kostnader) delt på aktuell beholdning. Du finner flere opplysninger i [Forstå beregning av enhetskost](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

I [!INCLUDE[prod_short](includes/prod_short.md)] justeres varekostnader automatisk hver gang det oppstår en lagertransaksjon, for eksempel når du bokfører en kjøpsfaktura for en vare.

Du kan også bruke en funksjon til å justere kostnadene for en eller flere varer manuelt. Dette er nyttig, for eksempel når du vet at varekostnader er endret av andre grunner enn varetransaksjoner.

Varekost justeres med lagermetoden FIFO eller Gjennomsnitt, avhengig av hva du valgte i den assisterte oppsettsveiledningen **Konfigurere Mitt selskap** eller i feltet **Lagermetode** på varekortet. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).  

Hvis du bruker lagermetoden FIFO, er enhetskosten for en vare den faktiske verdien for alle mottak av varen. Lageret verdisettes basert på antakelsen om at de første varene som plasseres på lager, selges først.

Hvis du bruker lagermetoden Gjennomsnitt, blir enhetskosten for en vare beregnet som den gjennomsnittlige enhetskosten på hvert tidspunkt etter et kjøp. Lageret verdisettes basert på antakelsen om at alle beholdninger selges samtidig. For varer som bruker denne lagermetoden, kan du velge feltet **Enhetskost** på varekortet for å vise en historikk over transaksjoner som gjennomsnittskosten beregnes fra

Funksjonen for kostnadsjustering behandler bare verdiposter som ennå ikke er justert. Hvis funksjonen støter på en situasjon der endrede inngående kost må videresendes til tilknyttede utgående poster, opprettes det nye justeringsoppføringer, som er basert på informasjonen i de opprinnelige verdipostene, men som inneholder justeringsbeløpet. Funksjonen for kostnadsjustering bruker bokføringsdatoen for den opprinnelige verdiposten i justeringsposten hvis denne datoen ikke er i en lukket lagerperiode. I så tilfelle bruker programmet startdatoen for den neste åpne lagerperioden. Hvis lagerperioder ikke brukes, styrer datoen i feltet **Bokf. tillatt fra** på siden **Finansoppsett** når justeringsposten bokføres.

## <a name="to-adjust-item-costs-manually"></a>Justere varekost manuelt
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Juster kostverdi – vareposter**, og velg deretter den tilknyttede koblingen.
2. På siden **Juster kostverdi - vareposter** angir du hvilke varer du vil justere kostnader for.
3. Velg **OK**.

## <a name="to-make-general-changes-in-the-direct-unit-cost"></a>Slik gjør du generelle endringer i direkte enhetskost
Hvis du må endre direkte enhetskost for flere varer, kan du bruke kjørselen **Juster varekost/priser**.  

 Kjørselen endrer innholdet i **Salgspris**-feltet på varekortet. Innholdet endres på samme måte for alle varene eller for utvalgte varer. Kjørselen multipliserer verdien i feltet med en justeringsfaktor som du angir.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Juster varekost/priser**, og velg deretter den tilknyttede koblingen.  
2. I feltet **Juster felt** angir du hvilket vare- eller LFE-kortfelt du vil justere.  
3. Angi faktoren som verdien skal justeres med, i **Justeringsfaktor**-feltet. Angi for eksempel **1,5** for å øke verdien med 50 %.  
4. På hurtigfanen **Vare** definerer du filtre til å angi, for eksempel, hvilke varer kjørselen skal behandle.  
5. Velg **OK**.  

## <a name="understanding-unit-cost-calculation"></a>Forstå beregning av enhetskost
Som en regel er verdien i **Enhetskost**-feltet på varekortet basert på standardkost for varer med standard lagermetode. For varer med andre lagermetoder er den basert på beregning av tilgjengelig lagerbeholdning (fakturerte kostnader og forventede kostnader) delt på aktuell beholdning.  

 Hvordan innholdet i feltet **Lagermetode** påvirker beregningen av enhetskosten for kjøp og salg, er beskrevet mer inngående i delene nedenfor.  

## <a name="unit-cost-calculation-for-purchases"></a>Beregne enhetskost for kjøp  
 Når du kjøper varer, blir verdien i feltet **Siste kjøpspris/prod.kost** på varekortet kopiert til feltet **Direkte enhetskost** på en bestillingslinje eller til Enhetsbeløp-linjen på en varekladdelinje.  

 Det du velger i **Lagermetode**-feltet, har innvirkning på hvordan [!INCLUDE[prod_short](includes/prod_short.md)] beregner innholdet i **Enhetskost**-feltet på linjene.  

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Lagermetoden FIFO, LIFO, Serienummer eller Gjennomsnitt  
 [!INCLUDE[prod_short](includes/prod_short.md)] beregner innholdet i feltet **Enhetskost LV** på bestillingslinjen, eller innholdet i feltet **Enhetskost** på varekladdelinjen etter følgende formel:  

 Enhetskost (LV) = (Direkte enhetskost - (Rabattbeløp / Antall)) x (1 + Indirekte kost-% / 100) + Sats for indirekte kostnader  

### <a name="costing-method-standard"></a>Standard lagermetode  
 Feltet **Enhetskost (LV)** på bestillingslinjen eller feltet **Enhetskost** fylles ut på varekladdelinjen ved å kopiere verdien i feltet **Enhetskost** på varekortet. Ved å angi lagermetoden som Standard, er denne alltid basert på standardkosten.  

 Når du bokfører kjøpet, kopieres enhetskosten fra bestillingslinjen eller varekladdelinjen til kjøp/varefakturaposten, og den kan ses på varens postoversikt.  

### <a name="all-costing-methods"></a>Alle lagermetoder  
 Enhetskosten fra kildedokumentlinjen brukes til å beregne innholdet i feltet **Kostbeløp faktisk**, eller feltet **Kostbeløp forventet**, hvis det er aktuelt, som er tilknyttet denne vareposten, uavhengig av lagermetoden for varen.  

## <a name="unit-cost-calculation-for-sales"></a>Beregne enhetskost for salg  
 Når du selger varer, kopieres enhetskosten fra feltet Enhetskost på varekortet til salgslinjen eller varekladdelinjen.  

 Ved bokføring kopieres enhetskosten til salgsfakturaposten, og den kan dermed ses på varens postoversikt. [!INCLUDE[prod_short](includes/prod_short.md)] bruker enhetskosten til å beregne innholdet i feltet **Kostbeløp faktisk**, eller feltet **Kostbeløp forventet**, hvis det brukes, i verdiposten som er knyttet til denne vareposten.  

## <a name="see-also"></a>Se også
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Lager](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]