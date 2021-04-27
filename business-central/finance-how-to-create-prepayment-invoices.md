---
title: Opprette forskuddsfakturaer | Microsoft-dokumentasjon
description: Lær hvordan du vil håndtere situasjoner der du eller leverandøren krever forskuddsbetaling.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 72a073fcde9ddf20df7c138ab544afb6719b93ce
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782166"
---
# <a name="create-prepayment-invoices"></a>Opprette forskuddsfakturaer

Hvis du krever at kundene skal betale før du leverer en ordre til dem, kan du bruke funksjonen for forskudd. Det samme gjelder hvis leverandøren krever at du sender betaling før de leverer en ordre til deg.  

Du kan starte betalingsprosessen når du oppretter en ordre eller bestilling. Hvis du har en standard forskuddsprosent for denne kunden eller leverandøren, vil det automatisk bli inkludert i den resulterende forskuddsfakturaen. Du kan også angi en forskuddsprosent for hele dokumentet.

Når du har opprettet en ordre eller bestilling, kan du opprette en forskuddsfaktura. Du kan bruke standardprosentene for hver salgslinje eller bestillingslinje, eller du kan justere beløpet etter behov. Du kan for eksempel angi et totalbeløp for hele ordren.  

Fremgangsmåten nedenfor beskriver hvordan du fakturerer et forskudd for en ordre. Trinnene er de samme for bestillinger.  

## <a name="to-create-a-prepayment-invoice"></a>Slik oppretter du en forskuddsfaktura:

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2. Opprett en ny ordre for den aktuelle kunden. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).  

    I hurtigfanen **Forskudd** angir feltet **Forskuddsprosent** prosenten som skal brukes til å beregne forskuddsbeløpet. Hvis det er angitt en standard forskuddsprosent på kundekortet, fylles feltet ut automatisk. Du kan endre prosenten. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Velg feltet **Komprimer forskudd** hvis du vil opprette linjer på forskuddsfakturaen som kombinerer linjer fra ordren, hvis:  

    - De har samme finanskonto for forskudd, som definert i det generelle bokføringsoppsettet.  
    - De har samme dimensjoner.  

    Hvis du vil definere en forskuddsfaktura med én linje for hver ordrelinje som har en forskuddsprosent, velger du ikke feltet **Komprimer forskudd**.  

    Forskuddsdatoen for forskuddet beregnes automatisk basert på verdien i feltet **Kode for betalingsbetingelser for forskudd**.

3. Fyll ut salgslinjene.  

    Hvis du har angitt en standard forskuddsprosent for kunden eller i hurtigfanen **Forskudd** for dette dokumentet, blir denne verdien kopiert til hver linje. Du kan endre verdien i **Forskuddsprosent**-feltet på linjen.  

4. Du kan vise det totale forskuddsbeløpet ved å velge **Statistikk**-handlingen.

    Hvis du vil justere det totale forskuddsbeløpet for ordren, kan du endre verdien i **Forskuddsbeløp**-feltet på **Ordrestatistikk**-siden.  

    Hvis feltet **Priser inkl. mva.** er valgt, kan du redigere feltet **Forskuddsbeløp inkl. mva**.  

    Hvis du endrer verdien i **Forskuddsbeløp**-feltet, blir beløpet fordelt proporsjonalt mellom alle linjene, unntatt de som har **0** i **Forskuddsprosent**-feltet.  

5. Hvis du vil skrive ut en testrapport før du bokfører forskuddsfakturaen, velger du **Forskuddsbetaling** og velger deretter **Testrapport for forskudd**.  
6. Hvis du vil bokføre forskuddsfakturaen, velger du **Forskuddsbetaling** og velger deretter **Bokfør forskuddsfaktura**.  

    Hvis du vil bokføre og skrive ut forskuddsfakturaen, velger du handlingen **Bokfør og skriv ut forskuddsfaktura**.  

Du kan utstede flere forskuddsfakturaer for ordren. Dette gjør du ved å øke forskuddsbeløpet på én eller flere linjer, justere dokumentdatoen om nødvendig, og bokføre forskuddsfakturaen. Det opprettes en ny faktura for differansen mellom forskuddsbeløpene som er fakturert hittil, og det nye forskuddsbeløpet.  

> [!NOTE]  
> Hvis du befinner deg i Nord-Amerika, kan du ikke endre forskuddsprosenten når den forskuddsbetalte fakturaen er bokført. Dette er ikke tillatt i Nord-Amerika-versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] fordi beregningen av merverdiavgift ellers blir feil.  

 Når du er klar til å bokføre resten av fakturaen, bokfører du den som en hvilken som helst annen faktura, og forskuddsbeløpet blir automatisk trukket fra forfallsbeløpet.  

## <a name="see-also"></a>Se også

[Fakturere forskuddsbetalinger](finance-invoice-prepayments.md)  
[Gjennomgang: konfigurere og fakturere salgsforskudd](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]