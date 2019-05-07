---
title: Konfigurere bankdatakonvertering | Microsoft-dokumentasjon
description: Du kan definere bankkonti for å holde rede på transaksjoner og importere eller eksportere bankfeeder, for eksempel Yodlee.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 38c1ee9b37513b270dcad09238df4f841a961d1a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "927545"
---
# <a name="set-up-the-bank-data-conversion-service"></a>Konfigurere tjeneste for konvertering av bankdata
En global tjenesteleverandør for å konvertere betalingsinformasjon til hvilket som helst dataformat banken krever, er koblet til og klar til å aktiveres i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette er det refereres til i [!INCLUDE[d365fin](includes/d365fin_md.md)] som tjenesten for konvertering av bankdata.

Du kan eksportere betalingslinjer fra siden **Betalingskladd** til en fil eller datastrøm som du deretter laster opp til banken for automatisk behandling, slik at du ikke trenger å foreta elektroniske betalinger individuelt. Hvis du vil ha mer informasjon, kan du se [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

Du kan importere filer med bankkontoutdrag til siden **Betalingsavstemmingskladd** ved hjelp av tjenesten for konvertering av bankdata til å konvertere en fil som du mottar fra banken din til en datastrøm som [!INCLUDE[d365fin](includes/d365fin_md.md)] kan importere. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Som et alternativ til å importere bankkontoutdrag med tjenesten for konvertering av bankdata kan du bruke tjenesten Bankfeeder for Envestnet Yodlee. Hvis du vil ha mer informasjon, kan du se [Konfigurere bankfeedservicen Envestnet Yodlee](bank-how-setup-bank-statement-service.md)

Hvis du vil importere eller eksportere bankfiler, må du definere din egen bankkonto og leverandørenes bankkonti. Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> Konverteringstjenesten for bankdata kan sette en grense for hvor mange linjer som kan eksporteres i én fil. Du får en feilmelding hvis grensen er overskredet. Det anbefales at bankkontoutdragsfiler ikke overstiger 1 000 linjer, siden behandlingstiden i konverteringstjenesten for bankdata kan øke betraktelig.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Slik registrerer du selskapet for tjenesten for bankdatakonvertering:
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tjenesteoppsett for bankdatakonvertering**, og velg deretter den relaterte koblingen.  
2. Siden **Tjenesteoppsett for bankdatakonvertering** åpnes med tre felt som er forhåndsutfylt med de aktuelle URL-adressene til leverandøren av konverteringstjenesten for bankdata.

    > [!NOTE]  
    >   I CRONUS International Ltd.-demonstrasjonsdatabasen blir feltene Brukernavn og Passord forhåndsutfylt med påloggingsinformasjon for demonstrasjon som du erstatter med selskapets faktiske informasjon når du registrerer deg for konverteringstjenesten for bankdata.
3. I feltet **Nettadresse for registrering** velger du nettleserknappen for å åpne registreringssiden for tjenesteleverandøren.  
4. På registreringssiden for tjenesteleverandøren av bankdata, skriver du inn brukernavn og passord for firmaets tjenesteabonnement, og deretter fullfører du registreringsprosessen som beskrevet av tjenesteleverandøren.

    Selskapet er nå registrert for tjenesten for bankdatakonvertering. Fortsett med å skrive inn brukernavnet og passordet som du angav for tjenesten i de tilknyttede oppsettfeltene i [!INCLUDE[d365fin](includes/d365fin_md.md)].

5. På siden **Tjenesteoppsett for bankdatakonvertering**, i **Brukernavn**-feltet, angir du den samme verdien du angav som påloggingsnavn på tjenesteleverandørens side i trinn 4.
6. I **Passord**-feltet angir du den samme verdien du angav i **Passord**-feltet på tjenesteleverandørens side i trinn 4.

> [!NOTE]  
> Påloggingsdataene krypteres automatisk.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Vise eller oppdatere listen over gjeldende bankdataformater som støttes
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tjenesteoppsett for bankdatakonvertering**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Banknavn – datakonverteringsliste** på siden **Tjenesteoppsett for bankdatakonvertering** for å åpne oversikten over banknavn som representerer bankdataformater som støttes av konverteringstjenesten.
3. På siden **Banknavn – datakonverteringsliste** velger du handlingen **Oppdater banknavnliste**.

Listen over bankdataformater som støttes av tjenesten for bankdatakonvertering, er nå oppdatert. Dette er listen over banknavn, filtrert etter land/område, som du kan velge blant i feltet **Banknavn – datakonvertering** på siden **Bankkort**.

> [!NOTE]  
>   Oppdateringen av bankdataformater som støttes, oppstår også når du velger eller angir en verdi i feltet **Banknavn – datakonvertering** i bankkontoen.

Du har nå registrert deg for tjenesten for bankdatakonvertering. Fortsette med å gjenspeile informasjonen for hver bankkonto skal bruke tjenesten.

## <a name="see-also"></a>Se også
[Konfigurere banktjenester](bank-setup-banking.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
