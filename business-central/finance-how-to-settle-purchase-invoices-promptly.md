---
title: Gjøre opp kjøpsfakturaer omgående
description: Hvis du må betale leverandøren kontant eller med sjekk, kan du utføre den nødvendige bokføringen når du bokfører selve fakturaen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: fb442c7b1e9e7bdcb727ca6de157657e370e254f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746844"
---
# <a name="settle-purchase-invoices-promptly"></a>Gjøre opp kjøpsfakturaer omgående

Hvis du må betale leverandøren kontant eller med sjekk, kan du bokføre betalingen når du bokfører selve fakturaen.  

> [!NOTE]  
> Hvis du vanligvis betaler kjøpsfakturaer kontant, med sjekk eller bankoverføring, er det lurt å definere en bestemt betalingsmåte med en motkonto, og angi denne betalingsmåten i feltet **Betalingsmåte** på leverandørkortet. Motkontonummeret settes automatisk inn i fakturahodet hver gang du oppretter en ny faktura. Hvis du vil ha mer informasjon, kan du se [Definere betalingsmåter](finance-payment-methods.md).  

## <a name="to-settle-purchase-invoices-promptly"></a>Slik gjør du opp kjøpsfakturaer omgående

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Hvis du vil betale enten med kontanter eller med giro, angir du nummeret på kassekontoen eller bankkontoen i feltet **Motkontonr.**.  

> [!IMPORTANT]  
> Feltene **Motkontotype** og **Motkontonr.** inngår ikke i standardoppsettet for fakturahodet. Hvis du vil bokføre betalingen av en faktura, må du kontakte en Microsoft-partner som kan legge til feltene via kode.  
>
> Denne tilpassingen er bare nødvendig hvis du ikke angir motkonti i betalingsmåtene som beskrevet ovenfor.

## <a name="see-also"></a>Se også

[Administrere skyldige beløp](payables-manage-payables.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]