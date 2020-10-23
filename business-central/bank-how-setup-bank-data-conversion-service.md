---
title: Konfigurere bankdatakonvertering | Microsoft-dokumentasjon
description: Du kan definere bankkonti for å holde rede på transaksjoner og importere eller eksportere bankfeeder, for eksempel Yodlee.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: af42c1b65480a1ae28387b7207eca09a79bfe75d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924456"
---
# <a name="set-up-the-amc-banking-365-fundamentals-extension"></a>Konfigurere utvidelsen AMC Banking 365 Fundamentals
En global tjenesteleverandør for å konvertere betalingsinformasjon til hvilket som helst dataformat banken krever, er koblet til og klar til å aktiveres i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Denne omtales i [!INCLUDE[d365fin](includes/d365fin_md.md)] som utvidelsen AMC Banking 365 Fundamentals.

Du kan eksportere betalingslinjer fra siden **Betalingskladd** til en fil eller datastrøm som du deretter laster opp til banken for automatisk behandling, slik at du ikke trenger å foreta elektroniske betalinger individuelt. Hvis du vil ha mer informasjon, kan du se [Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Du kan importere filer med bankkontoutdrag til siden **Betalingsavstemmingskladd** ved å bruke utvidelsen AMC Banking 365 Fundamentals til å konvertere en fil som du mottar fra banken din, til en datastrøm som [!INCLUDE[d365fin](includes/d365fin_md.md)] kan importere. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Som et alternativ til å importere bankkontoutdrag med utvidelsen AMC Banking 365 Fundamentals kan du bruke tjenesten Envestnet Yodlee Bank Feeds. Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).

Hvis du vil importere eller eksportere bankfiler, må du definere din egen bankkonto og leverandørenes bankkonti. Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> Utvidelsen AMC Banking 365 Fundamentals kan sette en grense for hvor mange linjer som kan eksporteres i én fil. Du får en feilmelding hvis grensen er overskredet. Det anbefales at bankkontoutdragsfiler ikke overstiger 1 000 linjer, siden behandlingstiden i utvidelsen AMC Banking 365 Fundamentals kan øke betraktelig.

## <a name="to-sign-your-company-up-for-the-amc-banking-365-fundamentals-extension"></a>Registrere selskapet ditt for utvidelsen AMC Banking 365 Fundamentals
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tjenesteoppsett for bankdatakonvertering**, og velg deretter den relaterte koblingen.  
2. Siden **Tjenesteoppsett for bankdatakonvertering** åpnes med tre felt som er forhåndsutfylt med de aktuelle URL-adressene til utvidelsen AMC Banking 365 Fundamentals.

    > [!NOTE]  
    >   I CRONUS International Ltd.-demonstrasjonsdatabasen blir feltene Brukernavn og Passord forhåndsutfylt med påloggingsinformasjon for demonstrasjon som du erstatter med selskapets faktiske informasjon når du registrerer deg for utvidelsen AMC Banking 365 Fundamentals.
3. I feltet **Nettadresse for registrering** velger du nettleserknappen for å åpne registreringssiden for tjenesteleverandøren.  
4. På registreringssiden for tjenesteleverandøren av bankdata, skriver du inn brukernavn og passord for firmaets tjenesteabonnement, og deretter fullfører du registreringsprosessen som beskrevet av tjenesteleverandøren.

    Selskapet er nå registrert for utvidelsen AMC Banking 365 Fundamentals. Fortsett med å skrive inn brukernavnet og passordet som du angav for tjenesten i de tilknyttede oppsettfeltene i [!INCLUDE[d365fin](includes/d365fin_md.md)].

5. På siden **Tjenesteoppsett for bankdatakonvertering**, i **Brukernavn**-feltet, angir du den samme verdien du angav som påloggingsnavn på tjenesteleverandørens side i trinn 4.
6. I **Passord**-feltet angir du den samme verdien du angav i **Passord**-feltet på tjenesteleverandørens side i trinn 4.

> [!NOTE]  
> Påloggingsdataene krypteres automatisk.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Vise eller oppdatere listen over gjeldende bankdataformater som støttes
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tjenesteoppsett for bankdatakonvertering**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Banknavn – datakonverteringsliste** på siden **Tjenesteoppsett for bankdatakonvertering** for å åpne oversikten over banknavn som representerer bankdataformater som støttes av konverteringstjenesten.
3. På siden **Banknavn – datakonverteringsliste** velger du handlingen **Oppdater banknavnliste**.

Listen over bankdataformater som støttes av utvidelsen AMC Banking 365 Fundamentals, er nå oppdatert. Dette er listen over banknavn, filtrert etter land/område, som du kan velge blant i feltet **Banknavn – datakonvertering** på siden **Bankkort**.

> [!NOTE]  
>   Oppdateringen av bankdataformater som støttes, oppstår også når du velger eller angir en verdi i feltet **Banknavn – datakonvertering** i bankkontoen.

Du har nå registrert deg for utvidelsen AMC Banking 365 Fundamentals. Fortsette med å gjenspeile informasjonen for hver bankkonto skal bruke tjenesten.

## <a name="see-also"></a>Se også
[Konfigurere banktjenester](bank-setup-banking.md)  
[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
