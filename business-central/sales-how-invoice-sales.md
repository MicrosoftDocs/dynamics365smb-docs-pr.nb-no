---
title: Fakturer salg
description: 'Beskriver hvordan du oppretter en sluttseddel, eller en salgsfaktura eller ordre, for å registrere avtalen med en kunde om å selge produkter i samsvar med bestemte betingelser.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bill, sale, invoice, order'
ms.search.form: '43, 48, 9301'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="invoice-sales"></a>Fakturer salg

Du kan vanligvis opprette en ordre eller salgsfaktura for å registrere avtalen med en kunde om å selge bestemte produkter på bestemte leverings- og betalingsbetingelser.  

Du må imidlertid bruke en ordre i stedet for en salgsfaktura hvis du:  

* Trenger å levere bare en del av en bestillingsantall, for eksempel fordi det fullstendige antallet ikke er på lager.  
* Leverer varer etter at du har bokført de tilhørende salgsfakturaene.
* Selger varer som leverandøren gir deg direkte til kunden, kjent som direkte levering. Finn ut mer under [Lag direkte leveringer](sales-how-drop-shipment.md).  

I alle andre situasjoner fungerer ordrer og salgsfakturaer på samme måte. Finn ut mer om hvordan du bruker ordrer under [Selg produkter](sales-how-sell-products.md).

Du kan forhandle med kunden ved først å opprette et tilbud, som du kan konvertere til en salgsfaktura når dere blir enige om salget. Finn ut mer under [Gi salgstilbud](sales-how-make-offers.md).

## <a name="create-sales-invoices"></a>Opprette salgsfakturaer

Hvis kunden bestemmer seg for å kjøpe, kan du bokføre salgsfaktura for å lage relaterte antall og verdiposter. Når du bokfører salgsfakturaen, kan du også sende den som et PDF-vedlegg i e-post. Du kan få brødteksten i e-posten forhåndsutfylt med et sammendrag av fakturaen og betalingsinformasjonen, for eksempel en kobling til PayPal. Finn ut mer under [Send dokumenter i e-post](ui-how-send-documents-email.md#to-send-documents-by-email). Når kunden deretter betaler fakturaen, kan du registrere betalingen på ulike måter, avhengig av størrelsen og foretrukne arbeidsflyter i organisasjonen. Finn ut mer i delen [Registrering av betalinger](#register-payments).  

Varekort kan være av typen **Lager**, **Service** eller **Ikke-lagervarer** for å angi om varen er henholdsvis en fysisk lagerenhet, en arbeidstidsenhet eller en fysisk enhet som ikke beholdes i lagerbeholdningen. Finn ut mer under [Registrer nye varer](inventory-how-register-new-items.md). Salgsfakturaprosessen er den samme for alle de tre varetypene.

Du kan fylle kundefelter i salgsfakturaen på en av to måter, avhengig av om kunden allerede er registrert. Se trinn 2 i fremgangsmåten nedenfor.

### <a name="to-create-a-sales-invoice"></a>Slik oppretter du en salgsfaktura

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. I feltet **Kundenavn** angir du navnet på en eksisterende kunde. Hvis kunden imidlertid er ny og derfor ikke er registrert, følger du denne fremgangsmåten for å fylle ut standard kundeopplysninger på siden **Salgsfaktura**:

    1. I feltet **Kundenavn** angir du navnet på den nye kunden.
    2. Velg **OK** i dialogboksen for å registrere den nye kunden.
    3. På siden **Velg en mal for en ny kunde** velger du en mal som du vil basere det nye kundekortet på, og deretter velger du **OK**.
    4. Det åpnes et nytt kundekort som viser informasjon om den valgte kundemalen. Fyll ut feltene som gjenstår. Finn ut mer under [Registrer nye kunder](sales-how-register-new-customers.md).  
    5. Når du fullfører kundekortet, velger du **Lukk** for å gå tilbake til siden **Salgsfaktura**.

   Flere felt i salgsfakturen er nå fylt ut med informasjon du har angitt på det nye kundekortet.  
3. Fyll ut resten av feltene på siden **Salgsfaktura** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hvis du vil at kunden betaler umiddelbart, for eksempel ved kontant eller PayPal, fyller du ut feltet **Betalingsmåte – kode**. Betalingen registreres deretter når du bokfører salgsfakturaen. Hvis du velger *Kontant*, registreres betalingen på en bestemt motkonto.

    Du er nå klar til å fylle ut hurtigfanen **Linjer** med produktene du selger til kunden eller for noen transaksjon med kunden som du vil registrere i en finanskonto.

4. På **Linjer**-hurtigfanen i **Type**-feltet velger du typen produkt, tillegg eller transaksjon som du vil legge til for kunden på salgslinjen.
   > [!TIP]
   > Hvis du har definert gjentakende salgslinjer for kunden, for eksempel en månedlig etterfyllingsordre, kan du gjenspeile dette på ordren ved å velge handlingen **Hent gjentakende salgslinjer**.
5. I **Nr.** velger du en post skal bokføres, i henhold til verdien i **Type**-feltet.

    La feltet **Nr.** stå tomt i følgende tilfeller:

    * Hvis linjen er for en kommentar. Skriv inn kommentaren i **Beskrivelse**-feltet.
    * Hvis linjen er for en katalogvare. Velg handlingen **Velg katalogvarer**. Finn ut mer under [Arbeid med katalogvarer](inventory-how-work-nonstock-items.md).

6. I **Antall**-feltet angir du hvor mange enheter av produktet, gebyret eller transaksjonen linjen skal registrere for kunden.  

    > [!NOTE]  
    > Hvis varen er av typen **Service** eller **Type**-feltet inneholder **Ressurs**, er antallet en tidsenhet, for eksempel timer, som angitt i feltet **Enhetskode** på linjen. Finn ut mer under [Definer vareenheter](inventory-how-setup-units-of-measure.md)

    Verdien i **Linjebeløp**-feltet beregnes som *salgspris* × *antall*.  

    Prisen og linjebeløpene er med eller uten mva, avhengig av hva du valgte i feltet **Priser inkludert merverdiavgift** på kundekortet.  
7. Hvis du vil gi en rabatt, skriver du inn en prosentandel i feltet **Linjerabatt-%**. Verdien i feltet **Linjebeløp** oppdateres tilsvarende.  

    Hvis spesialvarepriser er konfigurert i hurtigfanen **Salgspriser og salgslinjerabatter** i kunde- eller varekortet, og når du oppfyller priskriteriene, oppdateres prisen og beløpet på salgslinjen automatisk. Finn ut mer under [Registrer avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Gjenta trinn 4 til 7 for hver hvert produkt eller gebyr som du vil fakturere kunden for.

    Totaler-feltene under linjene oppdateres automatisk når du oppretter eller endrer linjer for å vise beløpene bokført postene.

    > [!NOTE]
    > I svært sjeldne tilfeller kan de bokførte beløpene avvike fra det som vises i totalfeltene. Dette skyldes vanligvis avrundingsberegninger i forbindelse med mva eller salgsmva.<br /><br />Hvis du vil kontrollere beløpene du vil bokføre, bruker du faktaboksen **Kundestatistikk** . Når du velger **Frigi**-handlingen, oppdateres verdiene i totaler-feltene slik at de omfatter avrundingsberegninger.

9. I feltet **Fakturarabattbeløp før mva.** angir du et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.**.

    Hvis du definerte fakturarabatter for kunden, settes den angitte prosentverdien automatisk inn i feltet **Fakturarabatt %** hvis rabattkriteriene er oppfylt, og det relaterte beløpet settes inn i feltet **Fakturarabattbeløp før mva.**. Finn ut mer under [Registrer avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).

10. Når salgsfakturalinjene er fullført, kan du velge handlingen **Bokfør og send**.  

Dialogboksen **Bokfør og send bekreftelse** viser kundens foretrukne metode for mottak av dokumenter. Du kan endre sendemetoden ved å velge oppslagsknappen for feltet **Send dokument til**. Finn ut mer under [Definer en profil for dokumentsending](sales-how-setup-document-send-profiles.md).

Beslektet element og kundeposter opprettes nå i systemet, og salgsfakturaen skrives ut som et PDF-dokument. Salgsfakturaen fjernes fra listen over salgsfakturaer og erstattes med et nytt dokument i listen over bokførte salgsfakturaer.  

### <a name="calculate-invoice-discounts-on-sales"></a>Beregning av fakturarabatter på salg

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="posted-invoices"></a>Bokførte fakturaer

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Du kan enkelt korrigere eller annullere en bokført salgsfaktura før den endelige betalingen. Dette er praktisk hvis du vil rette en skrivefeil, eller hvis kunden ber om en endring tidlig i ordreprosessen. Finn ut mer under [Korriger eller annuller ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md). Hvis den bokførte salgsfakturaen er betalt, må du opprette en salgskreditnota for å reversere salget. Finn ut mer under [Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md).  

[Åpne listen **Bokførte salgsfakturaer**](https://businesscentral.dynamics.com/?page=143) i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="register-payments"></a>Registrer betalinger

Avhengig av forretningsbehovene kan du få betalt og registrere en betaling på ulike måter: manuelt, automatisk og via betalingstjenester.  

Du kan behandle betalingene rett fra kundekortet. Bruk handlingen **Registrer kundebetalinger** for å få en oversikt over ubetalte fakturaer for denne kunden. Merk deretter fakturaen som betalt delvis eller fullstendig. Denne betalingsavstemmingen behandler kundens betalinger ved å avstemme beløp som er mottatt på bankkontoen med de relaterte ubetalte salgsfakturaene og deretter bokføre betalingene. Finn ut mer i delen [Avstem betalinger automatisk](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

I forretningsmiljøer hvor kunden betaler en stund etter levering. I henhold til betalingsbetingelsene, blir en bokført salgsfaktura værende åpen (ubetalt) til regnskapsavdelingen bekrefter betalingen, og utligner den mot den bokførte salgsfakturaen, Dette kan gjøres manuelt eller automatisk. Finn ut mer under [Avstem kundebetalinger med innbetalingskladden eller fra kundeposter](receivables-how-apply-sales-transactions-manually.md) og [Avstem betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).  

I forretningsmiljøer der kunden betaler umiddelbart, for eksempel via PayPal eller kontant, registreres betalingen umiddelbart når du bokfører salgsfakturaen, som si at den bokførte salgsfakturaen lukkes som fullstendig utlignet. Du velger den relevante metoden i **Betalingsmåte – kode**-feltet i ordren. For elektroniske betalinger, for eksempel PayPal, må du også fylle ut feltet **Betalingstjeneste**. Finn ut mer under [Aktiver kundebetalinger gjennom betalingstjenester](sales-how-enable-payment-service-extensions.md).

Du kan opprette direkte betalte fakturaer for kunder som ikke er registrert ved å definere et kontant kundekort for dem, som du velger på salgsfakturaen. Finn ut mer under [Definer kontantkunder](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Hvis du vil sende kundene purringer om forfalte betalinger, må du først definere purregrader og betingelser. Finn ut mer under [Definer betingelser og nivåer for leveringspåminnelser](finance-setup-reminders.md).  

## <a name="external-document-numbers"></a>Eksterne dokumentnumre

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Skriv ut plukklisten](sales-how-print-picking-list.md)  
[Lager](inventory-manage-inventory.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md#to-send-documents-by-email)  
[Innkreve utestående saldi](receivables-collect-outstanding-balances.md)  
[Massefakturering fra Microsoft Bookings i Business Central ](finance-bookings.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
