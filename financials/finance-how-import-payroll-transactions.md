---
title: "Importere lønnstransaksjoner| Microsoft-dokumentasjon"
description: "Beskriver hvordan du importerer lønnsutbetalinger og relaterte transaksjoner fra lønnssystemet til finans."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 03/24/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8d7ee87a80b4de2bc90086c188e5a53291c52683
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-import-payroll-transactions"></a>Lese inn lønnstransaksjoner
For å ta høyde for lønnsutbetalinger og relaterte transaksjoner, må du importere og bokføre finansielle transaksjoner som er utført av lønnssystemet til Finans. Hvis du vil gjøre dette, importerer du først filen som du mottar fra lønnssystemet til vinduet **Finanskladd**. Deretter tilordner du eksterne kontoer i lønnsfilen til de relevante finanskontiene. Til slutt kan du bokføre lønnstransaksjoner etter kontotilordningen.

**Merk**: Hvis du vil bruke denne funksjonaliteten, må det installeres og aktiveres en utvidelse for import av lønn. Utvidelsene for Ceridian lønn og Quickbooks Payroll-filimport er forhåndsinstallert i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Slik importerer du en lønnsfil
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Finanskladder**, og deretter velger du den beslektede koblingen.
2. I den aktuelle finanskladden velger du handlingen **Importer lønnstransaksjoner**. Det åpnes en assistert oppsettsveiledning.
3. Følg trinnene i vinduet **Importer lønnstransaksjoner**.

    **Tips**: I trinnet om hvordan du tilordner de eksterne lønnspostene til dine finanskonti, vil tilordningene du gjør bli husket neste gang de samme postene importeres. Dette vil bidra til at du sparer tid siden du ikke behøver å fylle ut i **Kontonummer** -feltet i finanskladden hver gang du har importert regelmessig lønnstransaksjoner.   

    Når du velger **OK**-knappen i den assisterte oppsettsveiledningen, fylles vinduet **Finanskladd** med linjer som representerer transaksjoner der lønnsfilen inneholder og med de aktuelle kontoene som er forhåndsutfylt i **Finanskonto**-feltene i henhold til tilordninger som du har gjort i veiledningen.
4. Rediger eller bokfør kladdelinjene som for andre transaksjoner i Finans. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).   

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av tillegg] (ui-extensions.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  

