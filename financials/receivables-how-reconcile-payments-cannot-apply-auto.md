---
title: "Bruke funksjonen Overfør differanse til konto til å avstemme betalinger | Microsoft-dokumentasjon"
description: "Beskriver hvordan du behandler betalinger som ikke kan utlignes mot et dokument, for eksempel når en valutakurs fører til at beløp blir forskjellige."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 37d2d8af5086a9f633cb90abb380578b4ca73136
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-reconcile-payments-that-cannot-be-applied-automatically"></a>Avstemme betalinger som ikke kan utlignes automatisk
Noen ganger må du å håndtere betalinger til din bankkonto som ikke kan utlignes mot en relatert åpen kunde-, leverandør- eller bankkontopost. Årsakene kan være at det ikke finnes dokumenter i [!INCLUDE[d365fin](includes/d365fin_md.md)] som betalingen kan utlignes mot, eller at det tilknyttede dokumentet i [!INCLUDE[d365fin](includes/d365fin_md.md)] har et annet beløp enn transaksjonsbeløpet, for eksempel på grunn av valutaveksling. I vinduet **Betalingsavstemmingskladd** vises alle transaksjonsbeløp for betalinger som ennå ikke er utlignet i **Differanse** -feltet, inkludert beløp som ikke kan brukes på grunn av årsaker som nevnt ovenfor.

Betalinger som ikke kan brukes, kan vises på linjer for betalingsavstemmingskladd på følgende forskjellige måter:

* Verdien i **Differanse**-feltet er lik verdien i **Transaksjonsbeløp** -feltet, som angir at ingen del av betalingen kan utlignes mot en relatert åpne kunde-, leverandør- eller bankkontopost.
* Verdien i **Differanse**-feltet er lavere enn verdien i **Transaksjonsbeløp** -feltet, som angir at ingen del av betalingen kan utlignes mot en relatert åpne kunde-, leverandør- eller bankkontopost. Den gjenværende delen av betalingen kan ikke utlignes og må avstemmes manuelt eller ved å bokføre den direkte til en konto.

Hvis du vil avstemme slike betalinger, kan du velge Overfør differanse til konto-knappen, og deretter angir du hvilken konto beløpet i Differanse-feltet bokføres til når du bokfører betalingsavstemmingskladd.

> [!NOTE]  
>   Det finnes lignende funksjonalitet for å konfigurere automatisk avstemming av regelmessige betalinger som ikke kan utlignes mot relaterte åpne kunde-, leverandør- eller bankkontoposter. Hvis du vil ha mer informasjon, kan du se [Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

## <a name="to-reconcile-payments-that-cannot-be-applied"></a>Avstemme betalinger som ikke kan utlignes
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Betalingsavstemmingskladder**, og velg deretter den relaterte koblingen.
2. Åpne en kladd for betalingsavstemming. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).
3. Velg **Overfør differanse til konto**. Vinduet **Overfør differanse til konto** åpnes.
4. I **Kontotype**-feltet angir du om kontotypen som betalingsbeløpet blir bokført til.
5. I **Kontonummer** -feltet angir du kontotypen som betalingsbeløpet blir bokført til.
6. I **Beskrivelse**-feltet angir du en tekst som beskriver denne direktebetalingsbokføringen. Som standard blir teksten i **Transaksjonstekst**-feltet på linjen for betalingsavstemmingskladd, satt inn.
7. Velg **OK**.

Hvis verdien i **Differanse**-feltet er lik verdien i **Transaksjonsbeløp**-feltet når du bokfører betalingsavstemmingskladden, bokføres hele betalingen på kladdelinjen direkte til den angitte motkontoen.

Hvis verdien i **Differanse**-feltet var lavere enn verdien i **Transaksjonsbeløpet**-feltet, opprettes det en ekstra kladdelinje med samme tekst og dato og med differansen som er satt inn i **Transaksjonsbeløp**-feltet. I den opprinnelige kladdelinjen blir differansen trukket fra verdien i **Transaksjonsbeløp**-feltet, og betalingen blir brukt til den relaterte kunde-, leverandør- eller bankkontoposten. Når du bokfører betalingsavstemmingskladden, bokføres en del av betalingen som utlignet betaling. Den andre delen av betalingen posteres direkte til den angitte kontoen.

## <a name="see-also"></a>Se også
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

