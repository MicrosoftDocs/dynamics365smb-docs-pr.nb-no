---
title: Opprett og konfigurer en Shopify-konto
description: Lær hvordan du får en Shopify-konto slik at du kan demonstrere arbeidsflyten for integrering av Shopify og Business Central.
ms.date: 03/04/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# <a name="create-and-set-up-a-shopify-account"></a>Opprett og konfigurer en Shopify-konto



Hvis du vurderer om du skal bruke Shopify som netthandelsløsning og trenger en Shopify-konto til å validere integrert arbeidsflyt, har du følgende alternativer:

- Skaff deg en prøveversjon. Dette er det typiske startpunktet for sluttbrukere.  
- Opprett utviklingsbutikker. Denne fremgangsmåten er for partnere som utfører regelmessige demoer, opplæringer og gir støtte.

## <a name="trial-end-user"></a>Prøveversjon (sluttbruker)

Gå til [Shopify-nettstedet](https://www.shopify.com), og bruk e-postkontoen for administratorkontoen til å registrere deg for en prøveversjon. Finn ut mer om hvordan du oppretter og tilpasser nettbutikken på [Shopify-hjelpesenteret](https://help.shopify.com/).

I **Shopify-administratoren** til den opprettede butikken bruker du følgende **innstillinger**:

- Velg en plan i [**Plan**](https://www.shopify.com/admin/settings/plan)-innstillingene for å teste betalingsprosessen.

- Vurder å aktivere koblingen *Vis påloggingskobling i overskriften til nettbutikk og kasse* i delen **Kontoer i nettbutikk og kasse** i [**Kundekonto**](https://www.shopify.com/admin/settings/customer_accounts)-innstillingene i **Shopify-administrator**.
- Vurder å velge *Ny kundekonto* i delen **Kontoer i nettbutikk og kasse** i Kundekonto-innstillingene.
- Vurder aktivering av *Selvbetjent retur* i delen **Nye kundekontoer** i Kundekonto-innstillingene.

- Aktiver testbetalinger. Du har to alternativer. Start ved å gå til [**Betalinger**](https://www.shopify.com/admin/settings/payments)-innstillinger:  
  1. *(for testing) falsk gateway*. Hvis du vil ha mer informasjon, kan du se [Aktiver falsk gateway for testing](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* i testmodus. Hvis du vil ha mer informasjon, kan du se [Test Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Deaktiver **Arkiver ordren automatisk** i delen **Ordrebehandling** i innstillingene [**Betaling**](https://www.shopify.com/admin/settings/checkout) i **Shopify-administratoren**.
- Vurder å velge alternativet *Selskapsnavn – valgfritt* i delen **Kundeinformasjon** i innstillingene for betaling.
- Aktiver alternativet **Vis tipsalternativer ved betaling** i delen **Tips** i innstillingene for betaling, hvis du planlegger å demonstrere tips.

> [!Important]  
> Husk å avslutte Shopify-prøveversjonen for å unngå betalinger.

## <a name="development-store"></a>Utviklingsbutikk

Begynn med å bli med i [Shopify-partnerprogrammet](https://help.shopify.com/partners/about). Etterpå bruker du **partnerinstrumentbordet** til å opprette utviklingsbutikken. Lære mer om [Opprett utviklingsbutikker](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Når du har opprettet butikken, i **Shopify-administratoren** til den opprettede butikken bruker du følgende **innstillinger**:

- Vurder å aktivere koblingen *Vis påloggingskobling i overskriften til nettbutikk og kasse* i delen **Kontoer i nettbutikk og kasse** i [**Kundekonto**](https://www.shopify.com/admin/settings/customer_accounts)-innstillingene i **Shopify-administrator**.
- Vurder å velge *Ny kundekonto* i delen **Kontoer i nettbutikk og kasse** i Kundekonto-innstillingene.
- Vurder aktivering av *Selvbetjent retur* i delen **Nye kundekontoer** i Kundekonto-innstillingene.
  
- Aktiver testbetalinger. Du har to alternativer. Start ved å gå til [**Betalinger**](https://www.shopify.com/admin/settings/payments)-innstillinger:  
  1. *(for testing) falsk gateway*. Hvis du vil ha mer informasjon, kan du se [Aktiver falsk gateway for testing](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* i testmodus. Finn ut mer under [Test Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).
     
- Deaktiver **Arkiver ordren automatisk** i delen **Ordrebehandling** i innstillingene [**Betaling**](https://www.shopify.com/admin/settings/checkout) i **Shopify-administratoren**.
- Vurder å velge alternativet *Selskapsnavn – valgfritt* i delen **Kundeinformasjon** i innstillingene for betaling.
- Hvis du planlegger å vise tips, må du aktivere alternativet **Vis tipsalternativer ved betaling** i delen **Tips** i innstillingene for betaling.


> [!Note]  
> Utviklingslagre er vanligvis passordbeskyttet. Når du prøver å åpne en bestemt side i nettbutikken fra [!INCLUDE [prod_short](../includes/prod_short.md)], for eksempel for å gå til et bestemt produkt eller en bestemt ordre, må du angi passordet. Når du tester, for å unngå å måtte skrive inn passordet, logger du deg på Shopify-administratoren og åpner butikken derfra. Du trenger ikke å angi passordet for butikken før du har lukket nettleseren eller økten utløper.  

## <a name="see-also"></a>Se også

[Kom i gang med Shopify-koblingen](get-started.md)  
[Gjennomgang: Konfigurer og bruk Shopify-koblingen](walkthrough-setting-up-and-using-shopify.md)
