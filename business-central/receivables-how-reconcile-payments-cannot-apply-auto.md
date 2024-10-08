---
title: Bruke funksjonen for overføringsdifferanse til konto til å avstemme betalinger
description: 'Beskriver hvordan du behandler betalinger som ikke kan brukes på et dokument, for eksempel når en valutakurs fører til at beløp avviker.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 07/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="reconcile-payments-that-cant-be-applied-automatically"></a>Avstemme betalinger som ikke kan utlignes automatisk
Noen ganger må du kanskje håndtere betalinger til bankkontoen din som ikke kan brukes på en relatert åpen kunde-, leverandør- eller bankkontopost. Årsakene kan være at det ikke finnes noe bilag som [!INCLUDE[prod_short](includes/prod_short.md)] betalingen kan utlignes mot, eller at det tilknyttede dokumentet i [!INCLUDE[prod_short](includes/prod_short.md)] har et annet beløp enn transaksjonsbeløpet, for eksempel på grunn av valutaveksling. På **siden Betalingsavstemmingskladd** vises alle transaksjonsbeløp for betalinger som ikke er utlignet ennå, i Differanse-feltet **·**, inkludert beløp som ikke kan utlignes på grunn av årsaker som ovenfor.

Metodene for å løse disse typene betalinger som ikke er utlignet:
* Utlign manuelt
* Bruk tekst-til-konto-tilordning
* Overfør et ekstra beløp til en kladdelinje for å opprette og bokføre den nødvendige posten, for eksempel refusjon av en overbetaling.

Betalinger som ikke kan utlignes, kan vises på linjer i betalingsavstemmingskladdelinjer på følgende forskjellige måter:

* Verdien i **Differanse**-feltet er lik verdien i **Transaksjonsbeløp** -feltet, som angir at ingen del av betalingen kan utlignes mot en relatert åpne kunde-, leverandør- eller bankkontopost.
* Verdien i **Differanse**-feltet er lavere enn verdien i **Transaksjonsbeløp** -feltet, som angir at ingen del av betalingen kan utlignes mot en relatert åpne kunde-, leverandør- eller bankkontopost. Den gjenværende delen av betalingen kan ikke utlignes, og må avstemmes manuelt eller ved å bokføre den direkte til en konto.

Hvis du vil avstemme slike betalinger, kan du velge **Overfør differanse til konto**-handlingen, og deretter angir du hvilken konto beløpet i **Differanse**-feltet bokføres til når du bokfører betalingsavstemmingskladd. Du kan gjøre dette enten fra siden **Betalingsavstemmingskladd** eller **Se gjennom betalingsutligning** som du åpner, ved å velge verdien i feltet **Konfidensintervall** eller ved å velge feltet **Forskjell**.

> [!TIP]  
>   Det finnes lignende funksjonalitet for å konfigurere automatisk avstemming av regelmessige betalinger som ikke kan utlignes mot relaterte åpne kunde-, leverandør- eller bankkontoposter. Hvis du vil ha mer informasjon, kan du se [Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

## <a name="to-reconcile-payments-that-cant-be-applied-automatically"></a>Slik avstemmer du betalinger som ikke kan utlignes automatisk:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsavstemmingskladder** og velg den relaterte koblingen.
2. Åpne en kladd for betalingsavstemming. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).
3. Velg **Overfør differanse til konto**. Siden **Overfør differanse til konto** åpnes.
4. I **Kontotype**-feltet angir du om kontotypen som betalingsbeløpet blir bokført til.
5. I **Kontonr.**-feltet angir du kontoen som betalingsbeløpet blir bokført til.
6. I **Beskrivelse**-feltet angir du en tekst som beskriver denne direktebetalingsbokføringen. Som standard blir teksten i **Transaksjonstekst**-feltet på linjen for betalingsavstemmingskladd, satt inn.
7. Velg **OK**.

Hvis verdien i **Differanse**-feltet er lik verdien i **Transaksjonsbeløp**-feltet når du bokfører betalingsavstemmingskladden, bokføres hele betalingen på kladdelinjen direkte til den angitte motkontoen.

Hvis verdien i **Differanse**-feltet var lavere enn verdien i **Transaksjonsbeløpet**-feltet, opprettes det en ekstra kladdelinje med samme tekst og dato og med differansen som er satt inn i **Transaksjonsbeløp**-feltet. I den opprinnelige kladdelinjen blir differansen trukket fra verdien i **Transaksjonsbeløp**-feltet, og betalingen blir brukt til den relaterte kunde-, leverandør- eller bankkontoposten. Når du bokfører betalingsavstemmingskladden, bokføres en del av betalingen som utlignet betaling. Den andre delen av betalingen posteres direkte til den angitte kontoen.

## <a name="see-also"></a>Se også
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
