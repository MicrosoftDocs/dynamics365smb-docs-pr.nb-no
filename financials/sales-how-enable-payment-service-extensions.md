---
title: Aktivere kundebetalinger gjennom betalingstjenester | Microsoft-dokumentasjon
description: "Gjør det lettere for kundene å betale sine fakturaer ved å aktivere betalingstjenester."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c149949b939a551a14236c84f8ba7538fcb54bbe
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-customer-payments-through-payment-services"></a>Aktivere kundebetalinger gjennom betalingstjenester
Som et alternativ til å samle inn betalinger via bankoverføring eller kredittkort, kan kundene betale via egne kontoer med betalingstjenester, som Microsoft Pay, PayPal eller WorldPay.  

Når du har aktivert en betalingstjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)], en kobling til tjenesten er tilgjengelig på salgsdokumenter som du sender via e-post til kundene dine. Kunder kan bruke koblingen for å gå til tjenesten og betale fakturaen, direkte fra salgsdokumentet. Hvis du ikke vil inkludere koblingen, for eksempel kan Hvis en kunde betaler kontant, du fjerne tjenesten fra fakturaen før bokføring.  

Tilleggene Microsoft Pay, PayPal Payments Standard og WorldPay Payments Standard er installert i [!INCLUDE[d365fin](includes/d365fin_md.md)], og er klar til å aktivere.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Slik aktiverer du en betalingstjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Betalingstjenester**, og velg deretter den relaterte koblingen.  
2. I vinduet **Betalingstjenester** velger du handlingen **Ny**.  
3. Velg betalingstjenesten, og lukk deretter vinduet.  
4. I vinduet **Betalingstjenester** velger du handlingen **Oppsett**.  
5. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Lukk vinduet.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Velge en betalingstjeneste på en salgsfaktura
1. Velg handlingen **Salgsfakturaer** på Hjem-siden.  
2. Åpne Salgsfaktura som du ønsker å betale ved hjelp av betalingstjenesten.  
3. I feltet **Betalingstjeneste** velger du betalingstjenesten.  

    > [!NOTE]  
>   Feltet **Betalingstjeneste** er bare tilgjengelig hvis du har aktivert betalingstjenesten.  

## <a name="see-also"></a>Se også  
[Sette opp salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

