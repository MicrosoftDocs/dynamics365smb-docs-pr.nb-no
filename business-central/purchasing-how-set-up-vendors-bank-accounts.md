---
title: Konfigurer leverandørbankkonto
description: 'Finn ut hvordan du knytter bankkontoer til leverandørkort i Business Central, inkludert kontaktinformasjon, SWIFT og IBAN-koder.'
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: article
ms.date: 07/04/2022
ms.author: bholtorf
ms.reviewer: bholtorf
---
# <a name="set-up-vendor-bank-accounts"></a>Konfigurer leverandørbankkontoer

På samme måte som du kan bruke bankkontoopplysninger på [!INCLUDE [prod_short](includes/prod_short.md)] til å holde oversikt over selskapets banktransaksjoner, kan du også angi bankdetaljer for leverandører. Bankkontodata for leverandører kan for eksempel forenkle betaling til leverandører når de kombineres med funksjonen [AMC Banking 365 Fundamentals-utvidelsen](ui-extensions-amc-banking.md) eller [Eksporter betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

## <a name="add-or-edit-a-vendor-bank-account"></a>Legg til eller rediger en leverandørbankkonto

[!INCLUDE [purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

> [!TIP]
> Du kan definere flere leverandørbankkontoer på siden **Liste over leverandørbankkonto**.

## <a name="set-up-a-preferred-vendor-bank-account"></a>Konfigurer en foretrukket leverandørbankkonto

Hvis en leverandør har en eller flere bankkontoer og du vil angi et foretrukket alternativ for betalingskladdelinjene, følger du denne fremgangsmåten:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Åpne kortet for leverandøren.
3. Velg standard leverandørbankkonto i feltet **Foretrukket bankkontokode** på hurtigfanen **Betalinger**.

## <a name="see-also"></a>Se også

[Definere kjøp](purchasing-setup-purchasing.md)  
[Registrer nye leverandører](purchasing-how-register-new-vendors.md)  
[Konfigurer bankkontoer](bank-how-setup-bank-accounts.md)  
[Bruk utvidelsen AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Konfigurer Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
