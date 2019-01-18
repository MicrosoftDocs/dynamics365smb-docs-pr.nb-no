---
title: Eksportere betalinger til en fil for elektronisk betaling | Microsoft dokumenter
description: "Du foretar leverandørbetalinger ved å aktivere en konverteringstjeneste for bankdata, eksportere en bankfil og laste opp filen til den elektroniske banken for å overføre midlene."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 14015c089e3cd6db19a12fe4eed72d523f3aefc5
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="export-payments-to-a-bank-file"></a>Eksportere betalinger til en bankfil
Når du er klar til å utføre betalinger til leverandører eller refusjoner til de ansatte, kan du eksportere en fil med betalingsinformasjonen for linjene på siden **Betalingskladd**. Du kan deretter laste opp filen til banken for å behandle de relaterte pengeoverføringene.

I den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] er det konfigurert og koblet til en global tjenesteleverandør for å konvertere bankdata til hvilket som helst format banken krever. I Nord-Amerika versjoner, den samme tjenesten som kan brukes til å sende betalinger som elektronisk pengeoverføring (EFT), men med en litt annen prosess. Se trinn 6 i den "for eksport av betalinger til en bankfil".    

> [!NOTE]  
>   Før du kan eksportere betalingsfiler fra betalingsjournalen, må du angi det elektroniske formatet for bankkontoen som er involvert, og du må aktivere konverteringstjenesten for bankdata. Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-how-setup-bank-accounts.md) og [Konfigurere Envestnet Yodlee Bank Feeds](bank-how-setup-bank-data-conversion-service.md). I tillegg må du merke av for **Tillat betalingseksport** på siden **Finanskladder**. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  

Du bruker siden **Kredittoverføringsregistre** til å vise betalingsfilene som er eksportert fra betalingskladden. Fra denne siden kan du også eksportere betalingsfiler på nytt ved tekniske feil eller endringer. Vær oppmerksom på at eksporterte EFT-filer vises ikke på denne siden, og kan ikke være eksportert på nytt.  

## <a name="to-export-payments-to-a-bank-file"></a>Slik eksporterer du betalinger til en bankfil:
Nedenfor beskrives hvordan du betaler en leverandør med sjekk. Fremgangsmåten er lik refusjon til kunde med sjekk.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.
2. Fyll ut utbetalingskladdelinjene. Hvis du vil ha mer informasjon, kan du se [Registrere betalinger og refusjoner](payables-how-post-payments-refunds.md).

> [!NOTE]  
>   Hvis du bruker EFT, må du velge enten **Elektronisk betaling** eller **Elektronisk betaling-IAT** i feltet **Bankbetalingstype**. Andre fileksporttjenester og formater krever ulike oppsettsverdier på siden **Bankkort** og **Leverandørs bankkort**. Du blir informert om feil eller manglende oppsettsverdier når du prøver å eksportere filen.

3. Når du har fullført alle betalingskladdlinjene, velger du **Eksporter**.
4. På siden **Eksporter elektroniske betalinger** fyller du ut feltene etter behov.

    Eventuelle feilmeldinger vises i faktaboksen **Feil i betalingsfil**, der du også kan velge en feilmelding hvis du vil ha mer informasjon. Du må løse alle feil før betalingsfilen kan eksporteres.

    > [!TIP]  
    >   Når du bruker konverteringstjenesten for bankdata, kan du få en vanlig feilmelding om at bankkontonummeret ikke har lengden som banken krever. Du kan unngå eller løse feilen ved å fjerne verdien i **IBAN**-feltet på siden **Bankkort** og deretter angi et bankkontonummer i formatet som banken krever, i feltet **Bankkontonr.**

5. På siden **Lagre som** angir du plasseringen som filen som blir eksportert til, og deretter velger du **Lagre**.

    > [!NOTE]  
    >   Hvis du bruker EFT, lagrer du det resulterende remitteringsskjemaet for leverandører som et Word-dokument, eller du velger at det skal sendes direkte til leverandøren via e-post. Betalingene er nå lagt til på siden **Generer EFT-fil**, og derfra kan du generere flere betalingsordrer sammen for å spare overføringskostnader. Hvis du vil ha mer informasjon, kan du se følgende trinn.
6. På siden **Utbetalingskladd** velger du **GenerereEFT-fil**.

    På siden **Generer EFT-fil** vises alle betalinger som er definert for EFT som du har eksportert fra utbetalingskladden for en bestemt bankkonto, men som ennå ikke er generert på hurtigfanen **Linjer**.
7. Velg **Generer EFT-fil** for å eksportere en fil for alle EFT-betalinger.
8. På siden **Lagre som** angir du plasseringen som filen som blir eksportert til, og deretter velger du **Lagre**.

Bankbetalingsfilen eksporteres til plasseringen du angir, og du kan deretter laste den opp til nettbankkontoen og foreta de faktiske betalingene. Deretter kan du bokføre den eksporterte betalingen journallinjer.

## <a name="to-plan-when-to-post-exported-payments"></a>Planlegge når du bokfører eksporterte betalinger
Hvis du ikke vil bokføre en utbetalingskladdelinje for en eksportert betaling, for eksempel fordi du venter på bekreftelse på at transaksjonen er behandlet av banken, kan du bare slette kladdelinjen. Når du senere oppretter en utbetalingskladdelinje for å betale restbeløpet på fakturaen, viser feltet **Totalt eksportert beløp** hvor mye av betalingsbeløpet som allerede er eksportert. Du kan også finne detaljert informasjon om det eksporterte totalbeløpet ved å velge knappen **Poster i kredittoverføringsreg.** for å vise mer informasjon om eksporterte betalingsfiler.

Hvis du følger en prosess der du ikke bokfører betalinger før du har fått bekreftelse på at de har blitt behandlet i banken, kan du kontrollere dette på to måter.

* I en betalingskladd med foreslåtte betalingslinjer kan du sortere etter kolonnen **Lest ut til betalingsfil** eller **Totalt eksportert beløp**, og deretter slette betalingsforslag for åpne fakturaer som allerede er betalt og du ikke ønsker å betale.
* Du kan merke av for **Hopp over eksporterte betalinger** på siden **Betalingsforslag - leverandør**, der du angir hvilke betalinger som skal settes inn i utbetalingskladden, hvis du ikke vil sette inn kladdelinjer for betalinger som allerede er eksportert.

Du kan vise informasjon om eksporterte betalinger ved å velge handlingen **Historikk for betalingseksport**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Eksportere betalinger til en bankfil på nytt
Du kan eksportere betalingsfiler på nytt fra siden **Kredittoverføringsregistre**. Før du sletter eller bokfører utbetalingskladdelinjer, kan du også eksportere betalingsfilen på nytt fra siden **Betalingskladd**. Hvis du har slettet eller bokført utbetalingskladdelinjer etter at du har eksportert dem, kan du eksportere samme betalingsfil på nytt fra siden **Kredittoverføringsregistre**. Velg linjen for bunken med kredittoverføringer du vil eksportere på nytt, og bruk handlingen **Eksporter betalinger til fil på nytt**.

> [!NOTE]  
>   Eksporterte EFT-filer vises ikke på siden **Kredittoverføringsregistre** og kan ikke eksporteres på nytt.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kredittoverføringsregistre**, og velg deretter den relaterte koblingen.
2. Velg en betalingseksport som du vil eksportere på nytt, og velg deretter **Eksporter betaling til fil på nytt**.

## <a name="see-also"></a>Se også
[Utføre betalinger](payables-make-payments.md)  
[Kjøp](payables-manage-payables.md)  
[Definere kjøp](purchasing-setup-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

