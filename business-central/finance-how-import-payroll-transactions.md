---
title: Importere lønnstransaksjoner| Microsoft-dokumentasjon
description: Du administrerer lønn ved å importere og bokføre finanstransaksjoner fra lønnssystemet til Finans ved hjelp av en utvidelse for lønn, for eksempel Ceridian eller Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b2bd2408152cac52be5e2b22e6568600ceeb96f6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781584"
---
# <a name="import-payroll-transactions"></a>Importer lønnstransaksjoner
For å ta høyde for lønnsutbetalinger og relaterte transaksjoner, må du importere og bokføre finansielle transaksjoner som er utført av lønnssystemet til Finans. Hvis du vil gjøre dette, importerer du først filen som du mottar fra lønnssystemet på siden **Finanskladd**. Deretter tilordner du eksterne kontoer i lønnsfilen til de relevante finanskontiene. Til slutt kan du bokføre lønnstransaksjoner etter kontotilordningen.

> [!NOTE]  
>   Hvis du vil bruke denne funksjonaliteten, må det installeres og aktiveres en utvidelse for import av lønn. Utvidelsene for Ceridian lønn og Quickbooks Payroll-filimport er forhåndsinstallert i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Slik importerer du en lønnsfil
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. I den aktuelle finanskladden velger du handlingen **Importer lønnstransaksjoner**. Det åpnes en assistert oppsettsveiledning.
3. Følg trinnene på siden **Importer lønnstransaksjoner**.

    > [!TIP]  
    >   I trinnet om hvordan du tilordner de eksterne lønnspostene til finanskontiene, vil tilordningene du gjør, bli husket neste gang de samme postene importeres. Dette vil spare deg tid siden du trenger ikke å fylle ut feltet **Kontonummer** i finanskladden hver gang du har importert gjentakende lønnstransaksjoner.   

    Når du velger **OK**-knappen i den assisterte oppsettsveiledningen, fylles siden **Finanskladd** med linjer som representerer transaksjoner der lønnsfilen inneholder og med de aktuelle kontoene som er forhåndsutfylt i **Finanskonto**-feltene i henhold til tilordninger som du har gjort i veiledningen.
4. Rediger eller bokfør kladdelinjene som for andre transaksjoner i Finans. Hvis du vil ha mer informasjon, kan du se [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]