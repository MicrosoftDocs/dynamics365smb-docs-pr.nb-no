---
title: Overføre bankmidler
description: 'Du kan overføre beløp fra én bankkonto til en annen, inkludert ulike valutaer, ved å bokføre transaksjonen i finanskladden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bank account transfer, multiple currencies'
ms.search.form: 39
ms.date: 07/25/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="transfer-bank-funds"></a>Overføre bankmidler

Noen ganger må du kanskje overføre et beløp fra én bankkonto [!INCLUDE[prod_short](includes/prod_short.md)] til en annen. Hvis du vil gjøre dette, må du bokføre transaksjonen på **siden Finanskladder** . Oppgaven varierer avhengig av om bankkontoene bruker samme valuta eller forskjellige valutaer.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Bokføre en overføring mellom bankkonti med samme valutakode

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. På en av kladdelinjene fyller du ut feltet **Bokføringsdato** og **Bilagsnr.**.
3. Velg **Bankkonto** i **Kontotype**-feltet.
4. I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.
5. Angi beløpet som skal overføres i feltet **Beløp**.

    Du må deretter angi motkontoen. Hvis de relevante feltene ikke vises, velger du handlingen **Vis flere kolonner** for å vise alle tilgjengelige felter.
6. Velg **Bankkonto** i **Motkontotype**-feltet.
7. I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler til.
8. Bokfør kladden.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Slik bokfører du en overføring mellom bankkonti med ulike valutakoder

Hvis du vil overføre midler mellom bankkonti som bruker forskjellige valutaer, må du bokføre to linjer i finanskladden.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. Opprett to kladdelinjer, og fyll ut feltene **Bokføringsdato** og **Bilagsnr.**
3. På den første kladdelinje angir du **Bankkonto** i **Type**-feltet.
4. I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.
5. I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen med eller uten et minustegn.

    > [!TIP]
    > Et beløp uten et fortegn er et debetbeløp, og et beløp med et minustegn er et kreditbeløp.

    > [!NOTE]
    > Noen selskaper foretrekker å overføre mellom konti på separate kladdelinjer. Andre selskaper foretrekker å bokføre alt på én kladdelinje ved hjelp av en motkonto. Kontakt den lokale eksperten hvis du ikke er sikker på hva du skal gjøre.
    >
    > Hvis selskapet foretrekker å bruke en motkonto, setter du feltet **Motkontotype** til **Bankkonto** og feltet **Motkontonr.** til bankkontoen du vil overføre midlene til. Gå deretter videre til trinn 9 eller 10.
    >
    > Hvis selskapet foretrekker å bruke en separat kladdelinje, går du videre til neste trinn.
6. På den andre kladdelinje angir du **Bankkonto** i **Type**-feltet.
7. I feltet **Kontonr.** velger du bankkontoen du vil overføre midler til.
8. I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen med eller uten et minustegn.

    > [!TIP]
    > Et beløp uten et fortegn er et debetbeløp, og et beløp med et minustegn er et kreditbeløp.
9. Hvis valutakursene som brukes i kladden, ikke er de samme som valutakursene på siden **Valutakurser**, angir du en ny kladdelinje for agio eller disagio.  

    1. Angi **Finanskonto** i **Kontotype**-feltet.  

    2. Angi finanskontonummeret for agio eller disagio i **Kontonr.**-feltet.  

    3. Angi agio eller disagio i **Beløp**-feltet med eller uten et minustegn.

    > [!TIP]
    > Et beløp uten et fortegn er et debetbeløp, og et beløp med et minustegn er et kreditbeløp.
10. Bokfør kladden.

## <a name="see-also"></a>Se også

[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
