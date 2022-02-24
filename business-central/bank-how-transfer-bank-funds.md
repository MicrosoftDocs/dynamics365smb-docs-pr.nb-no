---
title: Overføre bankkapital| Microsoft-dokumentasjon
description: Du kan overføre beløp fra én bankkonto til en annen, inkludert ulike valutaer, ved å bokføre transaksjonen i finanskladden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: a21cabaf2f3edc9e8f1f261a9f9169c3cb611b61
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186215"
---
# <a name="transfer-bank-funds"></a>Overføre bankkapital
Noen ganger har du behov for å overføre av et beløp fra én konto til en annen i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil gjøre dette, må du bokføre transaksjonen på siden **Finanskladd**. Oppgaven varierer avhengig av om bankkontoene bruker samme valuta eller forskjellige valutaer.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Bokføre en overføring mellom bankkonti med samme valutakode
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladd**, og velg deretter den relaterte koblingen.
2. På en av kladdelinjene fyller du ut feltet **Bokføringsdato** og **Bilagsnr.**.
3. Velg **Bankkonto** i **Kontotype**-feltet.
4. I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.
5. Angi beløpet som skal overføres i feltet **Beløp**.
6. Velg handlingen **Vis flere kolonner** for å vise alle tilgjengelige felt.
7. Velg **Bankkonto** i **Motkontotype**-feltet.
8. I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler til.
9. Bokfør kladden.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Slik bokfører du en overføring mellom bankkonti med ulike valutakoder
Hvis du vil overføre midler mellom bankkonti som bruker forskjellige valutaer, må du bokføre to linjer i finanskladden.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladd**, og velg deretter den relaterte koblingen.
2. Opprett to kladdelinjer, og fyll ut feltene **Bokføringsdato** og **Bilagsnr.**
3. På den første kladdelinje angir du **Bankkonto** i **Type**-feltet.
4. I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.
5. I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen. Angi kreditbeløp med minus som fortegn. Angi debetbeløp uten minus som fortegn.
6. Velg **Bankkonto** i **Motkontotype**-feltet.
7. I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler til.
8. På den andre kladdelinje angir du **Bankkonto** i **Type**-feltet.
9. I feltet **Kontonr.** velger du bankkontoen du vil overføre midler til.
10. I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen. Angi kreditbeløp med minus som fortegn. Angi debetbeløp uten minus som fortegn.
11. Velg **Bankkonto** i **Motkontotype**-feltet.  
12. I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler fra.

    > [!NOTE]  
    > Hvis valutakursene som brukes i kladden, ikke er de samme som valutakursene på siden **Valutakurser**, angir du en tredje linje for agio/disagio. Angi **Finanskonto** i **Kontotype**-feltet. Angi finanskontonummeret for agio eller disagio i **Kontonr.**-feltet. Angi agio eller disagio i **Beløp**-feltet med eller uten et minustegn for henholdsvis kredit og debet.
13. Bokfør kladden.

## <a name="see-also"></a>Se også
[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
