---
title: "Forslå leverandørbetalinger| Microsoft-dokumentasjon"
description: "Foreslå leverandørbetalinger"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 4b85fc783cdebb7c1d2e048315e48aee02a189fa
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-suggest-vendor-payments"></a>Foreslå leverandørbetalinger
I vinduet **Utbetalingskladd** kan du bruke kjørselen **Betalingsforslag – leverandør** til å foreslå betalingslinjer. Linjer for ting som betalinger som forfaller snart, eller betalinger der kontantrabatt er tilgjengelig, foreslås basert på innstillingene.

Hvis du vil dra nytte fullstendig foreslåtte linjene, må du prioritere leverandørene først. Hvis du vil ha mer informasjon, kan du se [Prioritere leverandører](purchasing-how-prioritize-vendors.md).  

Leverandørposter som ikke er **På vent**, er ikke inkludert.  

**Viktig:** Hvis du vil dra nytte av kontantrabatter og har angitt et disponibelt beløp, brukes beløpet:  

* Prioriter først forfalte leverandørposter i prioritetsrekkefølge.  
* Forfalte leverandørposter som ikke er prioritert.  
* Åpne leverandørposter som kvalifiserer for kontantrabatter, sortert etter leverandørnummer.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>Bruke funksjonen Betalingsforslag - leverandør
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Utbetalingskladder**, og deretter velger du den beslektede koblingen.  
2. Åpne den aktuelle kladden, og velg deretter handlingen **Betalingsforslag - leverandør**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Velg **OK**-knappen.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Sette inn forfallsdato som bokføringsdato på betalingskladdelinjer
Når du bruker kjørselen **Betalingsforslag - leverandør** til å opprette betalingslinjer for leverandørene, kan du fylle ut to spesialfelt for å sikre at de genererte linjene bruker forfallsdatoen til å beregne bokføringsdatoen. Disse feltene er **Beregn bokføringsdato fra forfallsdato for utligningsbilag** og **Forskyvning av forfallsdato for utligningsbilag**.  

**Viktig:** Du kan ikke bruke feltet **Beregn bokføringsdato fra forfallsdato for utligningsbilag** sammen med feltet **Søk etter kontantrabatter** eller feltet **Summer per leverandør**. Hvis bokføringsdatoen er basert på forfallsdatoen, kan det hende at enkelte kontantrabatter ikke beregnes på riktig måte, fordi bokføringsdatoen er etter kontantrabattdatoen.  

Hvis den beregnede bokføringsdatoen er passert, vil bokføringsdatoen også bli flyttet til arbeidsdatoen og det vil vises en advarsel.  

Du kan også opprette betalingslinjer manuelt ved å bruke forfallsdatoen til å beregne bokføringsdatoen. Når du bruker leverandørposter, kan du bruke den **Beregn bokføringsdato** til å oppdatere bokføringsdatoen på kladdelinjen med forfallsdatoen for den tilknyttede kjøpsfakturaen. Hvis du vil ha mer informasjon, kan du se [Utligne kjøpstransaksjoner manuelt](payables-how-apply-purchase-transactions-manually.md).  

**Merk:** Hvis kjøpsfakturaen er forfalt, vil bokføringsdatoen bli satt til arbeidsdatoen, og skriftfargen på linjen blir rød.  

## <a name="see-also"></a>Se også
[Administrere skyldige beløp](payables-manage-payables.md)  
[Foreta betalinger](payables-make-payments.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

