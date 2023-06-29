---
title: Importer lønnstransaksjoner
description: 'Du administrerer lønn ved å importere og bokføre finanstransaksjoner fra lønnssystemet til Finans ved hjelp av en utvidelse for lønn, for eksempel Ceridian.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Ceridian, Quickbooks, salary'
ms.search.form: '1660, 1661, 36601'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="importing-payroll-transactions"></a><a name="importing-payroll-transactions"></a>Importer av lønnstransaksjoner

For å ta høyde for lønnsutbetalinger og relaterte transaksjoner, må du importere og bokføre finansielle transaksjoner som er utført av lønnssystemet til Finans. Hvis du vil gjøre dette, importerer du først filen som du mottar fra lønnssystemet på siden **Finanskladd**. Deretter tilordner du eksterne kontoer i lønnsfilen til de relevante finanskontiene. Til slutt kan du bokføre lønnstransaksjoner etter kontotilordningen.

> [!NOTE]  
> Hvis du vil bruke denne funksjonaliteten, må det installeres og aktiveres en utvidelse for import av lønn. Utvidelsene for Ceridian lønn og Quickbooks Payroll-filimport er forhåndsinstallert i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a><a name="to-import-a-payroll-file"></a>Slik importerer du en lønnsfil

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. I den aktuelle finanskladden velger du handlingen **Importer lønnstransaksjoner**. Det åpnes en assistert oppsettsveiledning.
3. Følg trinnene på siden **Importer lønnstransaksjoner**.

    > [!TIP]  
    >   I trinnet om hvordan du tilordner de eksterne lønnspostene til finanskontiene, vil tilordningene du gjør, bli husket neste gang de samme postene importeres. Dette vil spare deg tid siden du trenger ikke å fylle ut feltet **Kontonummer** i finanskladden hver gang du har importert gjentakende lønnstransaksjoner.   

    Når du velger **OK**-knappen i den assisterte oppsettsveiledningen, fylles siden **Finanskladd** med linjer som representerer transaksjoner der lønnsfilen inneholder og med de aktuelle kontoene som er forhåndsutfylt i **Finanskonto**-feltene i henhold til tilordninger som du har gjort i veiledningen.
4. Rediger eller bokfør kladdelinjene som for andre transaksjoner i Finans. Hvis du vil ha mer informasjon, kan du se [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a><a name="see-also"></a>Se også

[Finans](finance.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
