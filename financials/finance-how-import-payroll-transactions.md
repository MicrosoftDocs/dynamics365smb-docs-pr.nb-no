---
title: "Importere lønnstransaksjoner| Microsoft-dokumentasjon"
description: "Du administrerer lønn ved å importere og bokføre finanstransaksjoner fra lønnssystemet til Finans ved hjelp av en utvidelse for lønn, for eksempel Ceridian eller Quickbooks."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 06/16/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 45ac64abac2a604eb4f669dd3c246b59f05f4d31
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="import-payroll-transactions"></a>Importer lønnstransaksjoner
For å ta høyde for lønnsutbetalinger og relaterte transaksjoner, må du importere og bokføre finansielle transaksjoner som er utført av lønnssystemet til Finans. Hvis du vil gjøre dette, importerer du først filen som du mottar fra lønnssystemet til vinduet **Finanskladd**. Deretter tilordner du eksterne kontoer i lønnsfilen til de relevante finanskontiene. Til slutt kan du bokføre lønnstransaksjoner etter kontotilordningen.

> [!NOTE]  
>   Hvis du vil bruke denne funksjonaliteten, må det installeres og aktiveres en utvidelse for import av lønn. Utvidelsene for Ceridian lønn og Quickbooks Payroll-filimport er forhåndsinstallert i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Slik importerer du en lønnsfil
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. I den aktuelle finanskladden velger du handlingen **Importer lønnstransaksjoner**. Det åpnes en assistert oppsettsveiledning.
3. Følg trinnene i vinduet **Importer lønnstransaksjoner**.

    > [!TIP]  
>   I trinnet om hvordan du tilordner de eksterne lønnspostene til finanskontiene, vil tilordningene du gjør, bli husket neste gang de samme postene importeres. Dette vil spare deg tid siden du trenger ikke å fylle ut feltet **Kontonummer** i finanskladden hver gang du har importert gjentakende lønnstransaksjoner.   

    Når du velger **OK**-knappen i den assisterte oppsettsveiledningen, fylles vinduet **Finanskladd** med linjer som representerer transaksjoner der lønnsfilen inneholder og med de aktuelle kontoene som er forhåndsutfylt i **Finanskonto**-feltene i henhold til tilordninger som du har gjort i veiledningen.
4. Rediger eller bokfør kladdelinjene som for andre transaksjoner i Finans. Hvis du vil ha mer informasjon, kan du se [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  

