---
title: Opprette forskuddsfakturaer | Microsoft-dokumentasjon
description: "Lær hvordan du vil håndtere situasjoner der du eller leverandøren krever forskuddsbetaling."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 314732d3f622aede09342d7246e28b4a910d08d9
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="create-prepayment-invoices"></a>Opprette forskuddsfakturaer
Hvis du krever at kundene skal betale før du leverer en ordre til dem, eller hvis leverandøren krever at du betaler før de leverer en ordre til deg, kan du bruke funksjonaliteten for forskudd.  

Når du har opprettet en ordre eller bestilling, kan du opprette en forskuddsfaktura. Du kan bruke standardprosentene for hver salgslinje eller bestillingslinje, eller du kan justere beløpet etter behov. Du kan for eksempel angi et totalbeløp for hele ordren.  

Fremgangsmåten nedenfor beskriver hvordan du fakturerer et forskudd for en ordre. Trinnene er de samme for bestillinger.  

## <a name="to-create-a-prepayment-invoice"></a>Slik oppretter du en forskuddsfaktura:  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2. Opprett en ny ordre. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).  

    På hurtigfanen **Forskudd** fylles **Forskuddsprosent**-feltet ut automatisk hvis det er angitt en standard forskuddsprosent på kundekortet. Du kan endre innholdet i feltet. Forskuddsprosenten kopieres bare fra hodet til linjer som ikke kopierer standard forskuddsprosent fra varen.  

    Hvis feltet **Komprimer forskudd** er valgt, kombineres linjene på fakturaen hvis følgende er tilfelle:  
    - De har samme finanskonto for forskudd, som definert i det generelle bokføringsoppsettet.  
    - De har samme dimensjoner.  

    La feltet stå tomt hvis du vil definere en forskuddsfaktura med én linje for hver ordrelinje som har en forskuddsprosent.  

3. Fyll ut salgslinjene.  

    Hvis det er definert standard forskuddsprosenter for varene, kopieres de automatisk til **Forskuddsprosent**-feltet på linjen. Ellers kopieres forskuddsprosenten fra hodet. Du kan endre verdien i **Forskuddsprosent**-feltet på linjen.  
4. Hvis du vil bruke én forskuddsprosent på hele ordren, endrer du **Forskuddsprosent**-feltet på hodet etter at du har fylt ut linjene.  
5. Du kan vise det totale forskuddsbeløpet ved å velge **Statistikk**-handlingen.

    Hvis du vil justere det totale forskuddsbeløpet for ordren, kan du endre verdien i **Forskuddsbeløp**-feltet i **Ordrestatistikk**-vinduet.  

    Hvis feltet **Priser inkl. mva.** er valgt, kan du redigere feltet **Forskuddsbeløp inkl. mva**.  

    Hvis du endrer verdien i **Forskuddsbeløp**-feltet, blir beløpet fordelt proporsjonalt mellom alle linjene, unntatt de som har **0** i **Forskuddsprosent**-feltet.  
6. Hvis du vil skrive ut en testrapport før du bokfører forskuddsfakturaen, velger du **Forskuddsbetaling** og velger deretter **Testrapport for forskudd**.  
7. Hvis du vil bokføre forskuddsfakturaen, velger du **Forskuddsbetaling** og velger deretter **Bokfør forskuddsfaktura**.  

    Hvis du vil bokføre og skrive ut forskuddsfakturaen, velger du handlingen **Bokfør og skriv ut forskuddsfaktura**.  

Du kan utstede flere forskuddsfakturaer for ordren. Dette gjør du ved å øke forskuddsbeløpet på én eller flere linjer, justere dokumentdatoen om nødvendig, og bokføre forskuddsfakturaen. Det opprettes en ny faktura for differansen mellom forskuddsbeløpene som er fakturert hittil, og det nye forskuddsbeløpet.  

> [!NOTE]  
>  Hvis du befinner deg i Nord-Amerika, kan du ikke endre forskuddsprosenten når den forskuddsbetalte fakturaen er bokført. Dette er ikke tillatt i Nord-Amerika-versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] fordi beregningen av merverdiavgift ellers blir feil.  

 Når du er klar til å bokføre resten av fakturaen, bokfører du den som en hvilken som helst annen faktura, og forskuddsbeløpet blir automatisk trukket fra forfallsbeløpet.  

## <a name="see-also"></a>Se også  
[Fakturere forskuddsbetalinger](finance-invoice-prepayments.md)  
[Gjennomgang: konfigurere og fakturere salgsforskudd](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

