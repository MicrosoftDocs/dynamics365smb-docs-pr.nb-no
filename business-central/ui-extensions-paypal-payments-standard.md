---
title: Bruke PayPal Payments Standard-utvidelsen
description: Denne artikkelen beskriver hvordan du bruker standardutvidelsen til å gjøre det mulig for kunder å betale med PayPal.
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '1070, 1071, 1073, 1074'
ms.date: 07/09/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# PayPal Payments Standard-utvidelsen

Utvidelsen PayPal Payments Standard kan hjelpe deg med å øke kundeservicenivået ved å gjøre det enklere for kundene å betale regningene sine.

Som et alternativ til å samle inn betalinger via bankoverføring eller kreditt kort, kan kundene betale via sin PayPal konto. Når du sender en salgsfaktura i e-post, er det en PayPal-kobling i brødteksten i e-posten og i det vedlagte PDF-dokumentet. Hvis kunden velger opprette en kobling, åpnes servicesiden for PayPal kontoen som viser betalingsdetaljene. Kunden kan deretter betale fakturaen på samme måte som andre PayPal-betalinger.

PayPal Payments Standard-tjenesten gir følgende fordeler:

* Kundebetalinger kommer raskere inn på bankkontoen din.
* Kunder har flere måter å betale fakturaer på.
* PayPal tilbyr en pålitelig betalingstjeneste, som kunder som foretrekker i stedet for å angi opplysninger om kredittkort på nettsteder.
* PayPal tilbyr flere måter for å håndtere betalinger, inkludert behandling av kredittkortbetaling, PayPal-kontoer og andre kilder.
* PayPal-kobling kan legges til automatisk i salgsdokumenter eller manuelt av brukeren.
* PayPal Payments Standard-tjenesten omfatter ikke månedlige avgifter eller etableringsgebyrer.
* Fordi det er en utvidelse kan du enkelt aktivere PayPal Payments Standard-tjenesten når og hvis bedriften din har bruk for den.  

Hvis du vil vite mer om hvordan du konfigurerer utvidelsen, kan du gå til [Aktivere kundebetaling gjennom PayPal](sales-how-enable-payment-service-extensions.md).

## Registrere betalinger automatisk for bedriftskonti

[!INCLUDE [prod_short](includes/prod_short.md)] kan registrere betalinger automatisk hvis du har en Business Merchant-konto for PayPal Commerce-plattformen. Når kundene bruker PayPal opprette en kobling til å betale en faktura, [!INCLUDE [prod_short](includes/prod_short.md)]  bokfører postene og lukker dokumentet.

Hvis du vil bruke denne funksjonen, **aktiverer** du veksleknappen Registrer betalinger automatisk [!INCLUDE [prod_short](includes/prod_short.md)] på siden **Oppsett** for betalingsregistrering og bekrefter kontoene du vil bruke for betalingene. Hvis du bestemmer deg for at du ikke vil registrere betalinger automatisk, kan du slå den av igjen.

> [!TIP]
> Utviklere kan bruke sandkassekontoer til å teste oppsettet. For å gjøre det, endre PayPal URL til **sandbox.paypal.com**. [!INCLUDE [prod_short](includes/prod_short.md)] bruker PayPals Instant Payment Notification (IPN) gjennom notify_url.

## Se også

[Tilpass [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Sette opp salg](sales-setup-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
