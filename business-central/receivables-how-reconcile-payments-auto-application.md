---
title: Avstemme betalinger ved hjelp av automatisk utligning
description: Beskriver hvordan du bruker funksjonen for automatisk utligning til å utligne betalinger eller innbetalinger mot de relaterte åpne postene, og avstemme betalinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5c13e41d102e2a7ff2ca80275571a1a05eea225e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779050"
---
# <a name="reconcile-payments-using-automatic-application"></a>Avstemme betalinger ved hjelp av automatisk utligning

Siden **Betalingsavstemmingskladd** angir inngående eller utgående betalinger som er registrert som transaksjoner på nettbankkontoen eller en betalingstjeneste, og som du kan utligne mot de relaterte åpne kunde-, leverandør og bankkontopostene. Linjene i kladden kan fylles ut ved å importere et bankkontoutdrag som en bankfeed eller fil, eller ved å registrere transaksjoner manuelt som foretas i betalingstjenesten.

> [!NOTE]
> Siden inneholder automatisk samsvarsfunksjonalitet som gjelder betalinger til de relaterte åpne postene, basert på samsvar av data på en bankkontoutdragslinje (kladdelinje) med data på én eller flere åpne poster. Merk at du kan overskrive foreslått automatisk bruk, og du kan velge ikke å bruke automatisk bruk i det hele tatt. Hvis du vil ha mer informasjon, kan du se trinn 7.

En betalingsavstemmingskladd er knyttet til én bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] som gjenspeiler nettbankkontoen der betalingstransaksjonene registreres. Alle åpne bankposter relatert til den utlignede kunden- eller leverandørposter lukkes når du velger handlingen **Bokfør betalinger og avstem bankkonto**. Dette betyr at bankkontoen automatisk avstemmes for betalinger du bokfører med kladden.

Du kan importere banktransaksjoner som CSV-bankfiler eller et annet format som banken tilbyr. Hvis du vil importere bankkontoutdrag som bankfeeder, må du først aktivere en dedikert bankintegreringstjeneste og deretter knytte bankkontoen til den relaterte nettbankkontoen. Betalingsavstemmingskladden oppdager deretter automatisk bankfeeder når du velger handlingen **Importer banktransaksjoner**. I tillegg kan du konfigurere en bankkonto til automatisk å importere nye bankkontoutdragsfeeder hver time. Transaksjoner for betalinger som allerede er bokført som utlignet og/eller avstemt vil ikke bli importert. Du kan bruke Envestnet Yodlee Bank Feeds-tjenesten til dette, som er forhåndsinstallert i enkelte lands versjoner av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md). Du kan også kontakte Microsoft-partneren din for å få hjelp til å dekke firmaets eller nasjonale krav.

Med handlingen **Tilordne tekst til konto** kan du definere tilordninger mellom tekst på betalinger og bestemte debet-, kredit- og motkonti, slik at slike betalinger bokføres på de angitte kontiene når du bokfører kladden for betalingsavstemming. Dette er nyttig til for eksempel gjentakende innbetalinger eller utgifter, for eksempel hyppige kjøp av drivstoff til bil eller bankgebyrer og renter, som regelmessig oppstår på bankkontoutdraget og ikke trenger et tilknyttet forretningsdokument. (Se trinn 10 nedenfor.) Hvis du vil ha mer informasjon, kan du se [Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Kladdelinjer kan ikke ha foreslått utligning. Dette kan være av ulike årsaker, for eksempel et manglende dokument, eller fordi en kunde har betalt for mye, slik at det finnes et tilleggsbeløp etter at betalingen er utlignet i en annen kladdelinje. I slike tilfeller kan du bruke handlingen **Overfør differanse til konto** for å opprette og bokføre den manglende finansposten, for eksempel for en refusjon, som er nødvendig å utligne betalingen mot. (Se trinn 11 nedenfor) Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger som ikke kan utlignes.](receivables-how-reconcile-payments-cannot-apply-auto.md)

Du bruker **Utlign automatisk**-funksjonen enten automatisk når du importerer en bankfil eller feed med betalingstransaksjoner eller aktiverer den, for å utligne betalinger mot tilknyttede åpne poster basert på samsvar av tekst på en bankkontoutdragslinje (kladdelinje) med tekst på én eller flere åpne poster. Denne automatiseringen er basert på regler som du definerer på siden **Betalingsutligningsregler**, der du også definerer om et avstemmingsforslag krever gjennomgang. Hvis du vil ha mer informasjon, kan du se [Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md).

På kladdelinjer der en betaling er utlignet automatisk mot én eller flere åpne poster, har **Konfidensintervall**-feltet verdien **Lav**, **Middels** eller **Høy** for å angi kvaliteten på datasamsvaret som den foreslåtte betalingsutligningen er basert på.

Enkelte betalingsprogrammer krever gjennomgangen definert av den brukte samsvarsregelen, for eksempel linjer med **lavt** konfidensintervall. Andre linjer krever gjennomgang og manuell endring fordi det finnes en verdi i feltet **Differanse**. Hvis du vil gå gjennom én eller flere betalingsutligninger, velger du feltet **Linjer som skal gjennomgås** eller **Linjer med differanse** nederst. Siden **Se gjennom betalingsutligning** åpnes med alle relevante opplysninger om kunden eller leverandøren som betalingen gjelder, de tilsvarende detaljene og handlingene for å behandle linjen, for eksempel handlingen **Godta utligning**. (Se trinn 7 og 8 nedenfor.)

For hver kladdelinje som representerer en betaling på siden **Betalingsavstemmingskladd**, kan du åpne siden **Betalingsutligning** hvis du vil vise alle åpne kandidatposter for betalingen og detaljert informasjon for hver post om datasamsvaret som en betalingsutligning er basert på. Her kan du manuelt utligne betalinger som ble utlignet automatisk mot feil oppføring, eller utligne betalinger på nytt. (Se trinn 10 nedenfor.) Hvis du vil ha mer informasjon, kan du se [Se gjennom eller utligne betalinger etter automatisk utligning](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Du kan starte import av banktransaksjoner samtidig som du åpner siden **Betalingsavstemmingskladd** for en eksisterende kladd. Følgende prosedyre beskriver hvordan du importerer banktransaksjoner til siden **Betalingsavstemmingskladd** etter at du har opprettet en ny kladd.

## <a name="to-reconcile-payments-using-automatic-application"></a>Avstemme betalinger ved hjelp av automatisk utligning
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Betalingsavstemmingskladder**, og velg deretter den relaterte koblingen.
2. Hvis du vil arbeide i en ny kladd for betalingsavstemming, velger du handlingen **Ny kladd**.
3. På siden **Betalingsbankkonto - oversikt** velger du bankkontoen du vil utligne betalinger for, og deretter velger du **OK**-knappen.
   Siden **Betalingsavstemmingskladd** åpnes forberedt for den valgte bankkontoen.
4. Velg handlingen **Importer banktransaksjoner**.
   Hvis bankkontoen for den valgte kladden ikke er konfigurert for import av banktransaksjoner, åpnes en dialogboks som er til hjelp når du skal fylle ut de aktuelle feltene.
5. Velg filen som inneholder banktransaksjoner for betalingene du vil avstemme, på siden **Velg en fil som skal importeres**, og velg deretter **Åpne**-knappen.  
6. Hvis Envestnet Yodlee Bank Feeds-tjenesten er aktivert, angir du datointervallet for bankkontoutdrag som skal importeres på siden **Filtrering av bankkontoutdrag**, som åpnes automatisk.

    Siden **Betalingsavstemmingskladd** fylles ut med linjer for betalinger som representerer banktransaksjoner i det importerte bankkontoutdraget.

     På linjer for betalinger som er utlignet automatisk mot de tilknyttede åpne postene, har **Konfidensintervall**-feltet en verdi mellom **Lav** og **Høy** for å angi kvaliteten på datasamsvaret som den foreslåtte betalingsutligningen er basert på. Feltene **Kontonavn**, **Kontotype** og **Kontonr.** og fylles i tillegg ut med informasjon om kunden eller leverandøren som betalingen utlignes mot.

    De automatiske utligningene, de tilhørende kvalitetene og om linjer må gjennomgås, defineres av regler du kan redigere for å justere resultatene. Hvis du vil ha mer informasjon, kan du se [Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md).

7. Hvis du vil se gjennom, godkjenne/fjerne eller manuelt endre flere betalingsutligninger som har en verdi i feltet **Differanse**, velger du handlingen **Linjer med differanse** nederst.

    Siden **Se gjennom betalingsutligning** åpnes og viser den første utligningen som skal gjennomgås. Den neste utligningen som skal gjennomgås, vises på siden mens du behandler den forrige. Alle relevante opplysninger om kunden eller leverandøren som betalingen gjelder, de tilsvarende detaljene og handlingene for å behandle linjen, for eksempel handlingene **Godta utligning** og **Utlign manualt**.

8. Hvis du vil se gjennom, godkjenne/fjerne eller manuelt endre flere betalingsutligninger som er angitt for gjennomgang, i henhold til regelen for betalingsutligning, velger du handlingen **Linjer som skal gjennomgås** nederst. Den samme opplevelsen som beskrevet i trinn 8, vises

9. Hvis du vil endre en automatisk utligning, velger du en kladdelinje og velger deretter handlingen **Utlign manuelt** for å se gjennom betalingen manuelt på siden **Betalingsutligning**. Hvis du vil ha mer informasjon, kan du se [Se gjennom eller utligne betalinger etter automatisk utligning](receivables-how-review-apply-payments-auto-application.md).

10. Velg en kladdelinje med opphevet utligning for en gjentakende innbetaling eller utgift, for eksempel kjøp av drivstoff til en bil, og velg deretter **Tilordne tekst til konto**. Hvis du vil ha mer informasjon, kan du se [Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

    Når du er ferdig med å tilordne betalingstekst til kontoer, velger du handlingen **Utlign manuelt**.

    Når det er definert en tilordning av typen tekst-til-konto, vil den resulterende automatiske betalingsutligningen inneholde **Høy – tekst-til-konto-tilordning** i feltet **Konfidensintervall**.

11. For en kladdelinje som har ingen foreslått utligning fordi det ikke finnes noen finanskonto den kan utlignes mot, velger du handlingen **Overfør differanse til konto** for å opprette og bokføre den manglende finansposten som kreves for å utligne betalingen mot. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger som ikke kan utlignes.](receivables-how-reconcile-payments-cannot-apply-auto.md)

10. Hvis ingen flere linjer krever gjennomgang, og feltet **Differanse** er tomt på alle linjer, velger du **Bokfør**-handlingen og velger deretter ett av følgende alternativer:

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


[!INCLUDE[footer-include](includes/footer-banner.md)]