---
title: Gjøre opp kjøpsfakturaer omgående | Microsoft-dokumentasjon
description: Hvis du må betale leverandøren kontant eller med sjekk, kan du utføre den nødvendige bokføringen når du bokfører selve fakturaen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: d187398fe615574785a17b4a7eb122b7a18c557e
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879683"
---
# <a name="settle-purchase-invoices-promptly"></a>Gjøre opp kjøpsfakturaer omgående
Hvis du må betale leverandøren kontant eller med sjekk, kan du bokføre betalingen når du bokfører selve fakturaen.  

### <a name="to-settle-purchase-invoices-promptly"></a>Slik gjør du opp kjøpsfakturaer omgående  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3.  Hvis du vil betale enten med kontanter eller med giro, angir du nummeret på kassekontoen eller bankkontoen i feltet **Motkontonr.**.  

> [!IMPORTANT]  
>  Feltene **Motkontotype** og **Motkontonr.** inngår ikke i standardoppsettet for fakturahodet. Hvis du vil bokføre betalingen av en faktura, må du først sette dem inn ved hjelp av designfunksjonene.  

> [!NOTE]  
>  Hvis du vanligvis betaler kjøpsfakturaer kontant, er det lurt å definere en bestemt betalingsmåte med en motkonto, og angi denne betalingsmåten i feltet **Betalingsmåte** på leverandørkortet. Motkontonummeret settes automatisk inn i fakturahodet hver gang du oppretter en ny faktura.  

## <a name="see-also"></a>Se også  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
