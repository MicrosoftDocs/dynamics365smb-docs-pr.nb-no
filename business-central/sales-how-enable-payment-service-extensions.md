---
title: Aktivere kundebetalinger gjennom betalingstjenester | Microsoft-dokumentasjon
description: Gjør det lettere for kundene å betale sine fakturaer ved å aktivere betalingstjenester.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5fa58c177629fdf386bca0ebfce2b668a55cbc8f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393352"
---
# <a name="enable-customer-payments-through-payment-services"></a>Aktivere kundebetalinger gjennom betalingstjenester
Som et alternativ til å samle inn betalinger via bankoverføring eller kredittkort, kan kundene betale via egne kontoer med betalingstjenester, som Microsoft Pay, PayPal eller WorldPay.  

Når du har aktivert en betalingstjeneste i [!INCLUDE[prod_short](includes/prod_short.md)], en kobling til tjenesten er tilgjengelig på salgsdokumenter som du sender via e-post til kundene dine. Kunder kan bruke koblingen for å gå til tjenesten og betale fakturaen, direkte fra salgsdokumentet. Hvis du ikke vil inkludere koblingen, for eksempel kan Hvis en kunde betaler kontant, du fjerne tjenesten fra fakturaen før bokføring.  

Tilleggene Microsoft Pay, PayPal Payments Standard og WorldPay Payments Standard er installert i [!INCLUDE[prod_short](includes/prod_short.md)] og er klar til å aktiveres.  

## <a name="to-enable-a-payment-service-in-prod_short"></a>Slik aktiverer du en betalingstjeneste i [!INCLUDE[prod_short](includes/prod_short.md)]
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Betalingstjenester**, og velg deretter den relaterte koblingen.  
2. På siden **Betalingstjenester** velger du handlingen **Ny**.  
3. Velg betalingstjenesten, og lukk deretter siden.  
4. På siden **Betalingstjenester** velger du handlingen **Oppsett**.  
5. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Lukk siden.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Velge en betalingstjeneste på en salgsfaktura
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. Åpne Salgsfaktura som du ønsker å betale ved hjelp av betalingstjenesten.  
3. I feltet **Betalingstjeneste** velger du betalingstjenesten.  

    > [!NOTE]  
    > Feltet **Betalingstjeneste** er bare tilgjengelig hvis du har aktivert betalingstjenesten.  

## <a name="see-also"></a>Se også  
[Sette opp salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]