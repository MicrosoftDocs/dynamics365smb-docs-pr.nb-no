---
title: Avstemme betalinger ved hjelp av automatisk utligning
description: Beskriver hvordan du avstemmer betalinger med funksjonen for automatisk utligning til å utligne betalinger eller innbetalinger mot de relaterte åpne postene.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '389, 1290, 1294, 1287'
ms.date: 06/22/2022
ms.author: bholtorf
---
# <a name="reconcile-payments-using-automatic-application" />Avstemme betalinger ved hjelp av automatisk utligning

Siden **Betalingsavstemmingskladd** angir betalinger, enten innkommende eller utgående, som er registrert som transaksjoner på den elektroniske bankkontoen eller betalingstjenesten. Du kan utligne betalingene mot relaterte åpne kunde-, leverandør- og bankkontoposter. Fyll ut linjene i kladden ved å importere et bankkontoutdrag som en bankfeed eller fil, eller ved å registrere transaksjoner manuelt som foretas via betalingstjenesten.

> [!NOTE]
> Siden inneholder automatisk samsvarsfunksjonalitet som gjelder betalinger til de relaterte åpne postene, basert på samsvar av data på en bankkontoutdragslinje (kladdelinje) med data på én eller flere åpne poster. Merk at du kan overskrive foreslått automatisk bruk, og du kan velge ikke å bruke automatisk bruk i det hele tatt. Hvis du vil ha mer informasjon, kan du se trinn 7.

En betalingsavstemmingskladd er knyttet til én bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)]. Bankkontoen representerer den elektroniske bankkontoen der betalingstransaksjonene registreres. Alle åpne bankposter relatert til den utlignede kunden- eller leverandørposter lukkes når du velger handlingen **Bokfør betalinger og avstem bankkonto**. Bankkontoen blir automatisk avstemt for betalinger du bokfører med kladden.

Hvis du bruker siden **Betalingsavstemmingskladd** til å registrere og utligne kundebetalinger, kan du definere kladden slik at den bruker en bestemt nummerserie. Etterpå kan du angi nummerseriene i feltet **Nummerserie for betalingsavstemming** på en bankkonto. Ved å bruke en egen nummerserie kan det være enklere å identifisere eventuelle poster som ble bokført gjennom kladden.

På samme måte som andre kladder, når du korrigerer bokførte poster, kan du tilbakeføre poster som ble bokført via betalingsavstemmingskladden, fra **Finansjournal**-siden. Det kan for eksempel være at du vil tilbakeføre poster for betalinger du har utlignet mot feil kunde. Du må først oppheve utligningen av bokførte kundeposter. Deretter kan du bruke handlingen **Tilbakefør journal** på siden **Finansjournal** til å tilbakeføre kladden som bokførte betalingene. På siden **Bokførte finanskladder** kan du eventuelt bruke handlingen **Kopier valgte linjer til kladd** til å tilbakeføre bestemte linjer fra den bokførte journalen for betalingsavstemming. 

Når du bruker automatisk utligning, gjenkjenner [!INCLUDE[prod_short](includes/prod_short.md)] bankposter som allerede er bokført, som bidrar til å forhindre dobbelt bokføring.

Du kan importere banktransaksjoner som CSV-bankfiler eller et annet format som banken tilbyr. Hvis du vil importere bankkontoutdrag som bankfeeder, må du først aktivere en dedikert bankintegreringstjeneste og deretter knytte bankkontoen til den relaterte nettbankkontoen. Betalingsavstemmingskladden oppdager deretter automatisk bankfeeder når du velger handlingen **Importer banktransaksjoner**. I tillegg kan du konfigurere en bankkonto til automatisk å importere nye bankkontoutdragsfeeder hver time. Transaksjoner for betalinger som allerede er bokført som utlignet og/eller avstemt vil ikke bli importert. Du kan bruke Envestnet Yodlee Bank Feeds-tjenesten til disse transaksjonene, som er forhåndsinstallert i enkelte lands versjoner av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md). Du kan også få en Microsoft-partner til å hjelpe deg med å oppfylle firmaets eller nasjonale krav.

Med handlingen **Tilordne tekst til konto** kan du definere tilordninger mellom tekst på betalinger og bestemte debet-, kredit- og motkonti, slik at slike betalinger bokføres på de angitte kontiene når du bokfører kladden for betalingsavstemming. Tildeling er nyttig til for eksempel gjentakende innbetalinger eller utgifter, for eksempel hyppige kjøp av drivstoff til bil eller bankgebyrer og renter, som regelmessig oppstår på bankkontoutdraget og ikke trenger et tilknyttet forretningsdokument. (Se trinn 10) Hvis du vil ha mer informasjon, kan du se [Tildel tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Journallinjer har kanskje ingen foreslått utligning, noe som kan forekomme på ulike årsaker. Dette kan for eksempel være fordi et dokument mangler eller en kunde overbetalte og det finnes et tilleggsbeløp etter at betalingen er utlignet i en annen kladdelinje. I slike tilfeller kan du bruke handlingen **Overfør differanse til konto** for å opprette og bokføre den manglende finansposten, for eksempel for en refusjon, som er nødvendig å utligne betalingen mot. (Se trinn 11) Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger som ikke kan utlignes.](receivables-how-reconcile-payments-cannot-apply-auto.md)

Du bruker **Utlign automatisk**-funksjonen enten automatisk når du importerer en bankfil eller feed med betalingstransaksjoner eller aktiverer den, for å utligne betalinger mot tilknyttede åpne poster basert på samsvar av tekst på en bankkontoutdragslinje (kladdelinje) med tekst på én eller flere åpne poster. Denne automatiseringen er basert på regler som du definerer på siden **Betalingsutligningsregler**, der du også definerer om et avstemmingsforslag krever gjennomgang. Hvis du vil ha mer informasjon, kan du se [Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md).

På kladdelinjer der en betaling er utlignet automatisk mot én eller flere åpne poster, har **Konfidensintervall**-feltet verdien **Lav**, **Middels** eller **Høy** for å angi kvaliteten på datasamsvaret som den foreslåtte betalingsutligningen er basert på.

Enkelte betalingsprogrammer krever gjennomgangen definert av den brukte samsvarsregelen, for eksempel linjer med **lavt** konfidensintervall. Andre linjer krever gjennomgang og manuell endring fordi det finnes en verdi i feltet **Differanse**. Hvis du vil gå gjennom én eller flere betalingsutligninger, velger du feltet **Linjer som skal gjennomgås** eller **Linjer med differanse** nederst. Siden **Se gjennom betalingsutligning** åpnes med alle relevante opplysninger om kunden eller leverandøren som betalingen gjelder, de tilsvarende detaljene og handlingene for å behandle linjen, for eksempel handlingen **Godta utligning**. (Se trinn 7 og 8)

For hver kladdelinje som representerer en betaling på siden **Betalingsavstemmingskladd**, kan du åpne siden **Betalingsutligning** hvis du vil vise alle åpne kandidatposter for betalingen og detaljert informasjon for hver post om datasamsvaret som en betalingsutligning er basert på. Her kan du manuelt utligne betalinger som ble utlignet automatisk mot feil oppføring, eller utligne betalinger på nytt. (Se trinn 10) Hvis du vil ha mer informasjon, kan du se [Se gjennom eller utligne betalinger etter automatisk utligning](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Du kan starte import av banktransaksjoner samtidig som du åpner siden **Betalingsavstemmingskladd** for en eksisterende kladd. Følgende prosedyre beskriver hvordan du importerer banktransaksjoner til siden **Betalingsavstemmingskladd** etter at du har opprettet en ny kladd.

## <a name="to-reconcile-payments-using-automatic-application" />Avstemme betalinger ved hjelp av automatisk utligning
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsavstemmingskladder** og velg den relaterte koblingen.
2. Hvis du vil arbeide i en ny kladd for betalingsavstemming, velger du handlingen **Ny kladd**.
3. På siden **Betalingsbankkonto - oversikt** velger du bankkontoen du vil utligne betalinger for, og deretter velger du **OK**-knappen.
   Siden **Betalingsavstemmingskladd** åpnes forberedt for den valgte bankkontoen.
4. Velg handlingen **Importer banktransaksjoner**.
   Hvis bankkontoen for den valgte journalen ikke er definert for import av banktransaksjoner, hjelper [!INCLUDE[d365fin](includes/d365fin_md.md)] deg med dette.
5. Velg filen som inneholder banktransaksjoner for betalingene du vil avstemme, på siden **Velg en fil som skal importeres**, og velg deretter **Åpne**-knappen.  
6. Hvis Envestnet Yodlee Bank Feeds-tjenesten er aktivert, angir du datointervallet for bankkontoutdrag som skal importeres på siden **Filtrering av bankkontoutdrag**, som åpnes automatisk.

    Siden **Betalingsavstemmingskladd** fylles ut med linjer for betalinger som representerer banktransaksjoner i det importerte bankkontoutdraget.

     På linjer for betalinger som er utlignet automatisk mot tilknyttede åpne poster, angir **Konfidensintervall**-feltet kvaliteten på datasamsvaret som den foreslåtte betalingsutligningen er basert på. Feltene **Kontonavn**, **Kontotype** og **Kontonr.** og fylles i tillegg ut med informasjon om kunden eller leverandøren som betalingen utlignes mot.

    De automatiske utligningene, de tilhørende kvalitetene og om linjer må gjennomgås, kontrolleres av regler. Du kan redigere reglene for å justere resultatene. Hvis du vil ha mer informasjon, kan du se [Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md).

7. Hvis du vil se gjennom, godkjenne/fjerne eller manuelt endre flere betalingsutligninger som har en verdi i feltet **Differanse**, velger du handlingen **Linjer med differanse** nederst.

    Siden **Se gjennom betalingsutligning** åpnes og viser den første utligningen som skal gjennomgås. Den neste utligningen som skal gjennomgås, vises på siden mens du behandler den forrige. Gjennomgangen omfatter opplysninger om kunden eller leverandøren som betalingen gjelder, de tilsvarende detaljene og handlingene for å behandle linjen, for eksempel handlingene **Godta utligning** og **Utlign manualt**.

8. Hvis du vil se gjennom, godkjenne eller fjerne eller manuelt endre flere betalingsutligninger som regelen er satt til å gjennomgå, velger du handlingene **Linjer som skal gjennomgås**. 

9. Hvis du vil endre en automatisk utligning, velger du en kladdelinje og velger deretter handlingen **Utlign manuelt** for å se gjennom betalingen manuelt på siden **Betalingsutligning**. Hvis du vil ha mer informasjon, kan du se [Se gjennom eller utligne betalinger etter automatisk utligning](receivables-how-review-apply-payments-auto-application.md).

10. Velg en kladdelinje med opphevet utligning for en gjentakende innbetaling eller utgift, for eksempel kjøp av drivstoff til en bil, og velg deretter **Tilordne tekst til konto**. Hvis du vil ha mer informasjon, kan du se [Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

    Når du er ferdig med å tilordne betalingstekst til kontoer, velger du handlingen **Utlign manuelt**.

    Når det er definert en tildeling av typen tekst-til-konto, vil den resulterende automatiske betalingsutligningen inneholde **Høy – tekst-til-konto-tilordning** i feltet **Konfidensintervall**.

11. For en kladdelinje som har ingen foreslått utligning fordi det ikke finnes noen finanskonto den kan utlignes mot, velger du handlingen **Overfør differanse til konto** for å opprette og bokføre den manglende finansposten som kreves for å utligne betalingen mot. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger som ikke kan utlignes.](receivables-how-reconcile-payments-cannot-apply-auto.md)

12. Hvis ingen flere linjer krever gjennomgang, og feltet **Differanse** er tomt på alle linjer, velger du **Bokfør**-handlingen og velger deretter ett av følgende alternativer:

    - **Bokfør betalinger og avstem bankkonto** - Bokfører betalingene som utlignet og lukker de relaterte bankkontopostene som avstemt.
    - **Bokfør bare betalinger** - Bokfører bare betalingene som utlignet, og lar de relaterte bankkontopostene være åpne. Krever at du avstemmer bankkontoen separat, for eksempel: Hvis du vil ha mer informasjon, se [Avstemme bankkontoer](bank-how-reconcile-bank-accounts-separately.md).
    - **Kontrollrapport** - Hvis du vil se resultatet av bokføringen før du bokfører. **Bankkontoutdrag**-rapporten åpnes og viser de samme feltene som nederst i på siden **Betalingsavstemmingskladd**.

Når du bokfører betalingsavstemmingskladden, lukkes de åpne utlignede postene. Kontoene for kunder, leverandører eller finans oppdateres. De angitte kunde-, leverandør- og finanskontiene oppdateres for betalinger på kladdelinjer basert på tekst-til-kontotilordning. Det opprettes bankkontoposter for alle kladdelinjene. Hvis du velger handlingen **Bokfør betalinger og avstem bankkonto**, vil alle åpne bankposter relatert til den utlignede kunden- eller leverandørposter lukkes. Dette betyr at bankkontoen automatisk avstemmes for betalinger du bokfører med kladden.

Du kan sammenligne verdien i feltet **Saldo på bankkonto etter bokføring** med verdien i feltet **Utdrag - sluttsaldo** for å spore når bankkontoen avstemmes basert på betalinger som du bokfører.

> [!NOTE]  
>   Hvis du ikke vil avstemme en bankkonto fra siden **Betalingsavstemmingskladd**, må du bruke siden **Bankkontoavstemming**. Hvis du vil ha mer informasjon, kan du se [Avstemme bankkontoer](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-related-microsoft-trainingtrainingmodulesuse-journals-dynamics-365-business-central" />Se relatert [Microsoft-opplæring](/training/modules/use-journals-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
