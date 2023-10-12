---
title: Kjørselen Betalingsforslag – leverandør
description: Du kan angi betalingsinnstillinger for leverandør for å få forslag til betalinger.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 09/07/2023
ms.custom: bap-template
---
# Betalingsforslag - leverandør

På siden **Utbetalingskladd** kan du bruke kjørselen **Betalingsforslag – leverandør** til å foreslå betalingslinjer. Basert på innstillingene dine foreslår [!INCLUDE [prod_short](includes/prod_short.md)] linjer for betalinger:

* Betalinger som snart forfaller
* Betalinger der en kontantrabatt er tilgjengelig

Hvis du vil dra nytte fullstendig av betalingsforslag, må du prioritere leverandørene først. Hvis du vil vite mer om prioritering av leverandører, kan du gå til [Prioriter leverandører](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Kjørselen utelater leverandørposter som er **Avvent**, eller som allerede er utlignet og har en verdi i feltet **Utlignings-ID**.  

> [!IMPORTANT]  
> Hvis du vil dra nytte av kontantrabatter og har angitt et disponibelt beløp, brukes beløpet til følgende:  
>
> * Prioriterte forfalte leverandørposter først i prioritetsrekkefølge.
> * Forfalte leverandørposter som ikke er prioritert.  
> * Åpne leverandørposter som kvalifiserer for kontantrabatter. Postene er ordnet etter leverandørnummer.  

## Bruke funksjonen Betalingsforslag - leverandør

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utbetalingskladder** og velg den relaterte koblingen.  
2. Åpne kladden, og velg deretter handlingen **Betalingsforslag – leverandør**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Velg **OK**.  

## Sette inn forfallsdato som bokføringsdato på betalingskladdelinjer

Når du bruker kjørselen **Betalingsforslag - leverandør** til å opprette betalingslinjer for leverandørene, kan du fylle ut to spesialfelt for å sikre at de genererte linjene bruker forfallsdatoen til å beregne bokføringsdatoen. Disse feltene er **Beregn bokføringsdato fra forfallsdato for utligningsbilag** og **Forskyvning av forfallsdato for utligningsbilag**.  

> [!IMPORTANT]  
> Du kan ikke bruke feltet **Beregn bokføringsdato fra forfallsdato for utligningsbilag** sammen med feltet **Søk etter kontantrabatter** eller feltet **Summer per leverandør**. Hvis bokføringsdatoen er basert på forfallsdatoen, kan det hende at enkelte kontantrabatter ikke beregnes på riktig måte, fordi bokføringsdatoen er etter kontantrabattdatoen.  

Hvis den beregnede bokføringsdatoen er passert, blir bokføringsdatoen også flyttet til arbeidsdatoen og det vises en advarsel.  

Du kan også opprette betalingslinjer manuelt ved å bruke forfallsdatoen til å beregne bokføringsdatoen. Når du bruker leverandørposter, kan du bruke den **Beregn bokføringsdato** til å oppdatere bokføringsdatoen på kladdelinjen med forfallsdatoen for den tilknyttede kjøpsfakturaen. Hvis du vil lære mer om denne manuelle prosessen, kan du gå til [Utlign kjøpstransaksjoner manuelt](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
> Hvis kjøpsfakturaen er forfalt, vil bokføringsdatoen bli satt til arbeidsdatoen, og skriftfargen på linjen blir rød.  

## Se også

[Administrere skyldige beløp](payables-manage-payables.md)  
[Utføre betalinger](payables-make-payments.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
