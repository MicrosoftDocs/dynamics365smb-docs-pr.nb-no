---
title: Avstemme betalinger ved hjelp av automatisk utligning
description: Beskriver hvordan du bruker funksjonen for automatisk utligning til å utligne betalinger eller innbetalinger mot de relaterte åpne postene, og avstemme betalinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3b90cb523449367672be71abe0a7cf02effcde5a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748546"
---
# <a name="reconcile-payments-using-automatic-application"></a>Avstemme betalinger ved hjelp av automatisk utligning

Siden **Betalingsavstemmingskladd** angir inngående eller utgående betalinger som er registrert som transaksjoner på nettbankkontoen, og som du kan utligne mot de relaterte åpne kunde-, leverandør og bankkontopostene. Linjene i kladden fylles ut ved å importere et bankkontoutdrag som bankfeed eller fil.

> [!NOTE]
> Siden inneholder automatisk samsvarsfunksjonalitet som gjelder betalinger til de relaterte åpne postene, basert på samsvar av tekst på en bankkontoutdragslinje (kladdelinje) med tekst på én eller flere åpne poster. Merk at du kan overskrive foreslått automatisk bruk, og du kan velge ikke å bruke automatisk bruk i det hele tatt. Hvis du vil ha mer informasjon, kan du se trinn 7.

En betalingsavstemmingskladd er knyttet til én bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] som gjenspeiler nettbankkontoen der betalingstransaksjonene registreres. Alle åpne bankposter relatert til den utlignede kunden- eller leverandørposter lukkes når du velger handlingen **Bokfør betalinger og avstem bankkonto**. Dette betyr at bankkontoen automatisk avstemmes for betalinger du bokfører med kladden.

Hvis du vil importere bankkontoutdrag som bankfeeder, må du først aktivere Envestnet Yodlee Bank Feeds-tjenesten og deretter knytte bankkontoen til den relaterte nettbankkontoen. Betalingsavstemmingskladden oppdager deretter automatisk bankfeeder når du velger handlingen **Importer banktransaksjoner**. I tillegg kan du konfigurere en bankkonto til automatisk å importere nye bankkontoutdragsfeeder hver time. Transaksjoner for betalinger som allerede er bokført som utlignet og/eller avstemt vil ikke bli importert. Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).

Med handlingen **Tilordne tekst til konto** kan du definere tilordninger mellom tekst på betalinger og bestemte debet-, kredit- og motkonti, slik at slike betalinger bokføres på de angitte kontiene når du bokfører kladden for betalingsavstemming. Se trinn 8. Hvis du vil ha mer informasjon, kan du se [Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

Det finnes liknende funksjon hvis du vil avstemme overskytende beløp på linjene for betalingsavstemmingskladd på ad hoc-basis. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger som ikke kan utlignes.](receivables-how-reconcile-payments-cannot-apply-auto.md)

Du bruker **Utlign automatisk**-funksjonen enten automatisk når du importerer en bankfil eller feed med betalingstransaksjoner eller aktiverer den, for å utligne betalinger mot tilknyttede åpne poster basert på samsvar av tekst på en bankkontoutdragslinje (kladdelinje) med tekst på én eller flere åpne poster. Hvis du vil ha mer informasjon, kan du se [Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md).

På kladdelinjer der en betaling er utlignet automatisk mot én eller flere åpne poster, har **Konfidensintervall**-feltet en verdi mellom Lav og Høy for å angi kvaliteten på datasamsvaret som den foreslåtte betalingsutligningen er basert på. Feltene **Kontotype** og **Kontonr.** fylles i tillegg med informasjon om kunden eller leverandøren som betalingen utlignes mot. Hvis du har definert en tekst-til-kontotilordning, kan den automatiske utligningen føre til verdien **Høy – tekst-til-kontotilordning** for samsvarskonfidens.

For hver kladdelinje som representerer en betaling på siden **Betalingsavstemmingskladd**, kan du åpne siden **Betalingsutligning** hvis du vil vise alle åpne kandidatposter for betalingen og detaljert informasjon for hver post om datasamsvaret som en betalingsutligning er basert på. Her kan du manuelt utligne betalinger som ble utlignet automatisk mot feil oppføring, eller utligne betalinger på nytt. Hvis du vil ha mer informasjon, kan du se [Se gjennom eller utligne betalinger etter automatisk utligning](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Du kan starte import av banktransaksjoner samtidig som du åpner siden **Betalingsavstemmingskladd** for en eksisterende kladd for betalingsavstemming på siden **Kladder for betalingsavstemming**. Følgende prosedyre beskriver hvordan du importerer banktransaksjoner til siden **Betalingsavstemmingskladd** etter at du har opprettet en ny kladd.

## <a name="to-reconcile-payments-using-automatic-application"></a>Avstemme betalinger ved hjelp av automatisk utligning
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Betalingsavstemmingskladder**, og velg deretter den relaterte koblingen.
2. Hvis du vil arbeide i en ny kladd for betalingsavstemming, velger du handlingen **Ny kladd**.
3. På siden **Betalingsbankkonto - oversikt** velger du bankkontoen du vil utligne betalinger for, og deretter velger du **OK**-knappen.
   Siden **Betalingsavstemmingskladd** åpnes forberedt for den valgte bankkontoen.
4. Velg handlingen **Importer banktransaksjoner**.
   Hvis bankkontoen for den valgte kladden ikke er konfigurert for import av banktransaksjoner, åpnes en dialogboks som er til hjelp når du skal fylle ut de aktuelle feltene.
5. Velg filen som inneholder banktransaksjoner for betalingene du vil avstemme, på siden **Velg en fil som skal importeres**, og velg deretter **Åpne**-knappen.  
6. Hvis tjenesten for bankkontoutdrag er aktivert, angir du datointervallet for bankkontoutdrag som skal importeres på siden **Filtrering av bankkontoutdrag**, som åpnes automatisk.

    Siden **Betalingsavstemmingskladd** fylles ut med linjer for betalinger som representerer banktransaksjoner i det importerte bankkontoutdraget.

    På linjer for betalinger som er utlignet automatisk mot de tilknyttede åpne postene, har **Konfidensintervall**-feltet en verdi mellom **Lav** og **Høy** for å angi kvaliteten på datasamsvaret som den foreslåtte betalingsutligningen er basert på. Feltene **Kontotype** og **Kontonr.** fylles i tillegg med informasjon om kunden eller leverandøren som betalingen utlignes mot.
7. Velg en kladdelinje, og velg deretter handlingen **Utlign manuelt** for å se gjennom betalingen manuelt på siden **Betalingsutligning**. Hvis du vil ha mer informasjon, kan du se [Se gjennom eller utligne betalinger etter automatisk utligning](receivables-how-review-apply-payments-auto-application.md).

    Når du er ferdig med den manuelle utligningen, inneholder **Konfidensintervall**-feltet på kladdelinjen du har behandlet manuelt, **Godtatt**.
8. Velg en kladdelinje med opphevet utligning for en gjentakende innbetaling eller utgift, for eksempel kjøp av drivstoff til en bil, og velg deretter **Tilordne tekst til konto**. Hvis du vil ha mer informasjon, kan du se [Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
9. Når du er ferdig med å tilordne betalingstekst til kontoer, velger du handlingen **Utlign manuelt**.
10. Når du er sikker på at alle betalinger i kladdelinjene er riktig utlignet eller satt til direkte bokføring, velger du handlingen **Bokfør**, og velger deretter ett av alternativene:

    - **Bokfør betalinger og avstem bankkonto** - Bokfører betalingene som utlignet og lukker de relaterte bankkontopostene som avstemt.
    - **Bokfør bare betalinger** - Bokfører bare betalingene som utlignet, og lar de relaterte bankkontopostene være åpne. Krever at du avstemmer bankkontoen separat, for eksempel: Hvis du vil ha mer informasjon, se [Avstemme bankkontoer](bank-how-reconcile-bank-accounts-separately.md).
    - **Kontrollrapport** - Hvis du vil se resultatet av bokføringen før du bokfører. **Bankkontoutdrag**-rapporten åpnes og viser de samme feltene som nederst i på siden **Betalingsavstemmingskladd**.

Når du bokfører kladden for betalingsavstemming, lukkes de utlignede åpne postene, og de relaterte kunde-, leverandør- eller finanskontiene oppdateres. De angitte kunde-, leverandør- og finanskontiene oppdateres for betalinger på kladdelinjer basert på tekst-til-kontotilordning. Det opprettes bankkontoposter for alle kladdelinjene. Hvis du velger handlingen **Bokfør betalinger og avstem bankkonto**, vil alle åpne bankposter relatert til den utlignede kunden- eller leverandørposter lukkes. Dette betyr at bankkontoen automatisk avstemmes for betalinger du bokfører med kladden.

Du kan sammenligne verdien i feltet **Saldo på bankkonto etter bokføring** med verdien i feltet **Utdrag - sluttsaldo** for å spore når bankkontoen avstemmes basert på betalinger som du bokfører.

> [!NOTE]  
>   Hvis du ikke vil avstemme en bankkonto fra siden **Betalingsavstemmingskladd**, må du bruke siden **Bankkontoavstemming**. Hvis du vil ha mer informasjon, kan du se [Avstemme bankkontoer](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Se også
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
