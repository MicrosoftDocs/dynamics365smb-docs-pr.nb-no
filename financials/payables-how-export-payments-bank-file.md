---
title: Eksportere betalinger til en fil for elektronisk betaling | Microsoft dokumenter
description: "Du foretar leverandørbetalinger ved å aktivere en konverteringstjeneste for bankdata, eksportere en bankfil og laste opp filen til den elektroniske banken for å overføre midlene."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bb79c8df5b353239802f63fc3c268c83b6eb7859
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-export-payments-to-a-bank-file"></a>Eksportere betalinger til en bankfil
Når du er klar til å utføre betalinger til leverandører ved hjelp av vinduet **Betalingskladd**, kan du eksportere en fil med betalingsinformasjonen for kladdelinjene. Du kan deretter laste opp filen til nettbanken for å behandle de relaterte pengeoverføringene.

I den generelle versjonen av [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] er det konfigurert og koblet til en global tjenesteleverandør for å konvertere bankdata til hvilket som helst format banken krever. I Nord-Amerika versjoner, den samme tjenesten som kan brukes til å sende betalinger som elektronisk pengeoverføring (EFT), men med en litt annen prosess. Se trinn 6 i den "for eksport av betalinger til en bankfil".    

> [!NOTE]  
>   Før du kan eksportere betalingsfiler fra betalingsjournalen, må du angi det elektroniske formatet for bankkontoen som er involvert, og du må aktivere konverteringstjenesten for bankdata. Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-how-setup-bank-accounts.md) og [Konfigurere Envestnet Yodlee Bank Feeds](bank-how-setup-bank-data-conversion-service.md). I tillegg må du merke av for **Tillat betalingseksport** i vinduet **Finanskladder**. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  

Du bruker vinduet **Kredittoverføringsregistre** til å vise betalingsfilene som er eksportert fra betalingskladden. Fra dette vinduet kan du også eksportere betalingsfiler på nytt ved tekniske feil eller endringer. Vær oppmerksom på at eksporterte EFT-filer vises ikke i dette vinduet, og kan ikke være eksportert på nytt.  

## <a name="to-export-payments-to-a-bank-file"></a>Slik eksporterer du betalinger til en bankfil:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Betalingskladder**, og velg deretter den relaterte koblingen.
2. Fyll ut utbetalingskladdelinjer, for eksempel ved hjelp av funksjonen **Betalingsforslag - leverandør**. Hvis du vil ha mer informasjon, kan du se [Betalingsforslag - leverandør](payables-how-suggest-vendor-payments.md).
3. Fyll ut feltene på betalingskladdelinjene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   Hvis du bruker EFT, må du velge enten **Elektronisk betaling** eller **Elektronisk betaling-IAT** i feltet **Bankbetalingstype**.

    Andre fileksporttjenester og formater krever ulike oppsettsverdier i vinduet **Bankkort** og **Leverandørs bankkort**. Du blir informert om feil eller manglende oppsettsverdier når du prøver å eksportere filen.

4. Når du har fullført alle betalingskladdlinjene, velger du **Eksporter**.
5. I vinduet **Eksporter elektroniske betalinger** fyller du ut feltene etter behov.

    Eventuelle feilmeldinger vises i faktaboksen **Feil i betalingsfil**, der du også kan velge en feilmelding hvis du vil ha mer informasjon. Du må løse alle feil før betalingsfilen kan eksporteres.

    > [!TIP]  
>   Når du bruker konverteringstjenesten for bankdata, kan du få en vanlig feilmelding om at bankkontonummeret ikke har lengden som banken krever. Hvis du vil unngå eller løse feilen, må du fjerne verdien i **IBAN**-feltet i vinduet **Bankkort**, og i **Bankkontonr.** -feltet angir du deretter et bankkontonummer i formatet som banken krever.

6. I vinduet **Lagre som** angir du plasseringen som filen som blir eksportert til, og deretter velger du **Lagre**.

    > [!NOTE]  
>   Hvis du bruker EFT, lagrer du det resulterende remitteringsskjemaet for leverandører som et Word-dokument, eller du velger at det skal sendes direkte til leverandøren via e-post. Betalingene er nå lagt til i vinduet **Generer EFT-fil**, og derfra kan du generere flere betalingsordrer sammen for å spare overføringskostnader. Hvis du vil ha mer informasjon, kan du se følgende trinn.
7. I vinduet **Utbetalingskladd** velger du **GenerereEFT-fil**.

    I vinduet **Generer EFT-fil** vises alle betalinger som er definert for EFT som du har eksportert fra utbetalingskladden for en bestemt bankkonto, men som ennå ikke er generert på hurtigfanen **Linjer**.
8. Velg **Generer EFT-fil** for å eksportere en fil for alle EFT-betalinger.
9. I vinduet **Lagre som** angir du plasseringen som filen som blir eksportert til, og deretter velger du **Lagre**.

Bankbetalingsfilen eksporteres til plasseringen du angir, og du kan deretter laste den opp til nettbankkontoen og foreta de faktiske betalingene. Deretter kan du bokføre den eksporterte betalingen journallinjer.

## <a name="to-export-payments-that-represent-customer-refunds"></a>Eksportere betalinger som representerer kunden refusjoner
Følgende beskriver en arbeid-rundt for eksport av betalinger elektronisk refusjon.

> [!CAUTION]  
>   Linjene i den resulterende betalingskladden kan ikke posteres, slettes eller annulleres.
1. Konfigurer kunden som en leverandør. Gi den navnet "Kunde X for refusjoner", for eksempel. Hvis du vil ha mer informasjon, kan du se [Registrere nye leverandører](purchasing-how-register-new-vendors.md).
2. På utbetalingskladdelinjen for kunden kan du angi **Kkontotype**-feltet til **Kunde** og **Dokumenttype**-feltet til **Refusjon**.
3. Utfør den vanlige fremgangsmåten for betaling for eksport som beskrevet i delen "Slik eksporterer du betalinger til en bankfil".

## <a name="to-plan-when-to-post-exported-payments"></a>Planlegge når du bokfører eksporterte betalinger
Hvis du ikke vil bokføre en utbetalingskladdelinje for en eksportert betaling, for eksempel fordi du venter på bekreftelse på at transaksjonen er behandlet av banken, kan du bare slette kladdelinjen. Når du senere oppretter en utbetalingskladdelinje for å betale restbeløpet på fakturaen, viser feltet **Totalt eksportert beløp** hvor mye av betalingsbeløpet som allerede er eksportert. Du kan også finne detaljert informasjon om det eksporterte totalbeløpet ved å velge knappen **Poster i kredittoverføringsreg.** for å vise mer informasjon om eksporterte betalingsfiler.

Hvis du følger en prosess der du ikke bokfører betalinger før du har fått bekreftelse på at de har blitt behandlet i banken, kan du kontrollere dette på to måter.

* I en betalingskladd med foreslåtte betalingslinjer kan du sortere etter kolonnen **Lest ut til betalingsfil** eller **Totalt eksportert beløp**, og deretter slette betalingsforslag for åpne fakturaer som allerede er betalt og du ikke ønsker å betale.
* Du kan merke av for **Hopp over eksporterte betalinger** i vinduet **Betalingsforslag - leverandør**, der du angir hvilke betalinger som skal settes inn i utbetalingskladden, hvis du ikke vil sette inn kladdelinjer for betalinger som allerede er eksportert.

Du kan vise informasjon om eksporterte betalinger ved å velge handlingen **Historikk for betalingseksport**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Eksportere betalinger til en bankfil på nytt
Du kan eksportere betalingsfiler på nytt fra vinduet **Kredittoverføringsregistre**. Før du sletter eller bokfører utbetalingskladdelinjer, kan du også eksportere betalingsfilen på nytt fra vinduet **Betalingskladd**. Hvis du har slettet eller bokført utbetalingskladdelinjer etter at du har eksportert dem, kan du eksportere samme betalingsfil på nytt fra vinduet **Kredittoverføringsregistre**. Velg linjen for bunken med kredittoverføringer du vil eksportere på nytt, og bruk handlingen **Eksporter betalinger til fil på nytt**.

> [!NOTE]  
>   Eksporterte EFT-filer vises ikke i vinduet **Kredittoverføringsregistre** og kan ikke eksporteres på nytt.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kredittoverføringsregistre**, og velg deretter den relaterte koblingen.
2. Velg en betalingseksport som du vil eksportere på nytt, og velg deretter **Eksporter betaling til fil på nytt**.

## <a name="see-also"></a>Se også
[Kjøp](payables-manage-payables.md)  
[Definere kjøp](purchasing-setup-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
