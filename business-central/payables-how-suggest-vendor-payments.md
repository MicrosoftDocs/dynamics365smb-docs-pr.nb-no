---
title: Kjørselen Betalingsforslag – leverandør
description: 'Du kan angi innstillinger for leverandørbetaling for å få forslag for betalinger som snart forfaller, eller der en rabatt er tilgjengelig.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: 256
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="suggest-vendor-payments"></a><a name="suggest-vendor-payments"></a>Betalingsforslag - leverandør

På siden **Utbetalingskladd** kan du bruke kjørselen **Betalingsforslag – leverandør** til å foreslå betalingslinjer. Linjer for betalinger som forfaller snart, eller betalinger der kontantrabatt er tilgjengelig, foreslås basert på innstillingene.

Hvis du vil dra nytte fullstendig av betalingsforslag, må du prioritere leverandørene først. Hvis du vil ha mer informasjon, kan du se [Prioritere leverandører](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Leverandørposter som er merket med **Avvent** tas ikke med i kjørselen.  

> [!IMPORTANT]  
>   Hvis du vil dra nytte av kontantrabatter og har angitt et disponibelt beløp, brukes beløpet til følgende:  
    * Prioriterte forfalte leverandørposter først i prioritetsrekkefølge.   
    * Forfalte leverandørposter som ikke er prioritert.  
    * Åpne leverandørposter som kvalifiserer for kontantrabatter, sortert etter leverandørnummer.  

## <a name="to-use-the-suggest-vendor-payments-function"></a><a name="to-use-the-suggest-vendor-payments-function"></a>Bruke funksjonen Betalingsforslag - leverandør

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utbetalingskladder** og velg den relaterte koblingen.  
2. Åpne den aktuelle kladden, og velg deretter handlingen **Betalingsforslag - leverandør**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Velg **OK**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Sette inn forfallsdato som bokføringsdato på betalingskladdelinjer

Når du bruker kjørselen **Betalingsforslag - leverandør** til å opprette betalingslinjer for leverandørene, kan du fylle ut to spesialfelt for å sikre at de genererte linjene bruker forfallsdatoen til å beregne bokføringsdatoen. Disse feltene er **Beregn bokføringsdato fra forfallsdato for utligningsbilag** og **Forskyvning av forfallsdato for utligningsbilag**.  

> [!IMPORTANT]  
>   Du kan ikke bruke feltet **Beregn bokføringsdato fra forfallsdato for utligningsbilag** sammen med feltet **Søk etter kontantrabatter** eller feltet **Summer per leverandør**. Hvis bokføringsdatoen er basert på forfallsdatoen, kan det hende at enkelte kontantrabatter ikke beregnes på riktig måte, fordi bokføringsdatoen er etter kontantrabattdatoen.  

Hvis den beregnede bokføringsdatoen er passert, vil bokføringsdatoen også bli flyttet til arbeidsdatoen og det vil vises en advarsel.  

Du kan også opprette betalingslinjer manuelt ved å bruke forfallsdatoen til å beregne bokføringsdatoen. Når du bruker leverandørposter, kan du bruke den **Beregn bokføringsdato** til å oppdatere bokføringsdatoen på kladdelinjen med forfallsdatoen for den tilknyttede kjøpsfakturaen. Hvis du vil ha mer informasjon, kan du se [Utligne kjøpstransaksjoner manuelt](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Hvis kjøpsfakturaen er forfalt, vil bokføringsdatoen bli satt til arbeidsdatoen, og skriftfargen på linjen blir rød.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/suggest-vendor-payments-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Administrere skyldige beløp](payables-manage-payables.md)  
[Utføre betalinger](payables-make-payments.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
