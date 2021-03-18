---
title: Opprett en salgsfaktura eller ordre
description: Beskriver hvordan du oppretter en sluttseddel, eller en salgsfaktura eller ordre, for å registrere avtalen med en kunde om å selge produkter i samsvar med bestemte betingelser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 625259457528ed79b863604e65a55ff63a879ec3
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470415"
---
# <a name="invoice-sales"></a>Fakturere salg

Du kan opprette en salgsfaktura eller ordre for å registrere avtalen med en kunde om å selge bestemte produkter på bestemte leverings- og betalingsbetingelser.  

Det er et par scenarier der du må bruke en ordre i stedet for en salgsfaktura:  

* Hvis du trenger å levere bare en del av en bestillingsantall, for eksempel fordi det fullstendige antallet ikke er på lager.  
* Hvis du leverer varer etter at du har bokført de tilhørende salgsfakturaene.
* Hvis du selger varer som leverandøren gir deg direkte til kunden, kjent som direkte levering. Hvis du vil ha mer informasjon, kan du se [Foreta direkte leveringer](sales-how-drop-shipment.md).  

I alle andre henseender fungerer ordrer og salgsfakturaer på samme måte. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).

Du kan forhandle med kunden ved først å opprette et tilbud, som du kan konvertere til en salgsfaktura når dere blir enige om salget. Hvis du vil ha mer informasjon, kan du se [Gi salgstilbud](sales-how-make-offers.md).

Hvis kunden bestemmer seg for å kjøpe, kan du bokføre salgsfaktura for å lage relaterte antall og verdiposter. Når du bokfører salgsfakturaen, kan du også sende dokumentet som et PDF-vedlegg i e-post. Du kan få brødteksten i e-posten forhåndsutfylt med et sammendrag av fakturaen og betalingsinformasjonen, for eksempel en kobling til PayPal. Hvis du vil ha mer informasjon, kan du se [Sende dokumenter i e-post](ui-how-send-documents-email.md). Når kunden deretter betaler fakturaen, kan du registrere betalingen på ulike måter, avhengig av størrelsen og foretrukne arbeidsflyter i organisasjonen. Hvis du vil ha mer informasjon, kan du se delen [Registrere betalinger](#registering-payments).  


Du kan enkelt korrigere eller annullere en bokført salgsfaktura før den er betalt. Dette er for eksempel praktisk hvis du vil rette en skrivefeil, eller hvis kunden ber om en endring tidlig i ordreprosessen. Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md). Hvis den bokførte salgsfakturaen er betalt, må du opprette en salgskreditnota for å reversere salget. Hvis du vil ha mer informasjon, kan du se [Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md).

Varekortet kan være av typen **Lager**, **Service** eller **Ikke-lagervarer** for å angi om varen er en fysisk lagerenhet, en arbeidstidsenhet eller en fysisk enhet som ikke beholdes i lagerbeholdningen. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md). Salgsfakturaprosessen er den samme for alle de tre varetypene.

Du kan fylle kundefelt i salgsfakturaen på to måter, avhengig av om kunden allerede er registrert. Se trinn 2 i fremgangsmåten nedenfor.

## <a name="to-create-a-sales-invoice"></a>Slik oppretter du en salgsfaktura

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. I feltet **Kunde** angir du navnet på en eksisterende kunde.

    Andre felt på siden **Salgsfaktura** inneholder nå standardinformasjon for den valgte kunden.  

    Hvis kunden ikke er registrert, følger du denne fremgangsmåten:

    1. I feltet **Kunde** angir du navnet på den nye kunden.
    2. Klikk **Ja**-knappen i dialogboksen for å registrere den nye kunden.
    3. På siden **Velg en mal for en ny kunde** velger du en mal som du vil basere det nye kundekortet på, og deretter velger du **OK**-knappen.
    4. Det åpnes et nytt kundekort som viser informasjon om den valgte kundemalen. Fyll ut feltene som gjenstår. Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).  
    5. Når du har fullført kundekortet, velger du **OK**-knappen for å gå tilbake til siden **Salgsfaktura**.

   Flere felt i salgsfakturen er nå fylt ut med informasjon du har angitt på det nye kundekortet.  
3. Fyll ut resten av feltene på siden **Salgsfaktura** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hvis du vil at kunden betaler umiddelbart, for eksempel ved kontant eller PayPal, fyller du ut feltet **Betalingsmåte - kode**. Betalingen registreres deretter når du bokfører salgsfakturaen. Hvis du velger KONTANT, registreres betalingen på en bestemt motkonto.

    Du er nå klar til å fylle ut linjene salgsfaktura for produktene du selger til kunden eller for noen transaksjon med kunden som du vil registrere i en finanskonto.  

    Hvis du har definert gjentakende salgslinjer for kunden, for eksempel en månedlig etterfyllingsordre, kan du sette inn disse linjene på ordren ved å velge handlingen **Hent gjentakende salgslinjer**.  
4. På **Linjer**-hurtigfanen i **Type**-feltet velger du typen produkt, tillegg eller transaksjon som du vil legge til for kunden med salgslinjen.
5. I **Nr.** velger du en post skal bokføres, i henhold til verdien i **Type**-feltet.

    La feltet **Nr.** stå tomt i følgende tilfeller:

    * Hvis linjen er for en kommentar. Skriv inn kommentaren i **Beskrivelse**-feltet.
    * Hvis linjen er for en katalogvare. Velg handlingen **Velg katalogvarer**. Hvis du vil ha mer informasjon, kan du se [Arbeide med katalogvarer](inventory-how-work-nonstock-items.md).

6. I **Antall**-feltet angir du hvor mange enheter av produktet, gebyret eller transaksjonen som linjen skal registrere for kunden.  

    > [!NOTE]  
    > Hvis varen er av typen **Service** eller **Type**-feltet inneholder **Ressurs**, er antallet en tidsenhet, for eksempel timer, som angitt i feltet **Enhetskode** på linjen. Hvis du vil ha mer informasjon, kan du se [Definere vareenheter](inventory-how-setup-units-of-measure.md)

    Verdien i **Linjebeløp**-feltet beregnes som *salgspris* x *antall*.  

    Prisen og linjebeløpene er med eller uten mva, avhengig av hva du valgte i feltet **Priser inkludert merverdiavgift** på kundekortet.  
7. Hvis du vil gi en rabatt på salgslinjen, skriver du inn en prosentandel i feltet **Linjerabatt-%**. Verdien i feltet **Linjebeløp** oppdateres tilsvarende.  

    Hvis du har konfigurert varepriser på kunde- eller varekortet, oppdateres prisen og beløpet på salgslinjen automatisk hvis de avtalte priskriteriene er oppfylt. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Gjenta trinn 9 til 12 for hver hvert produkt eller gebyr som du vil fakturere kunden for.  

    Totaler-feltene under linjene oppdateres automatisk når du oppretter eller endrer linjer for å vise beløpene som skal bokføres i postene.

    > [!NOTE]
    > I svært sjeldne tilfeller kan de bokførte beløpene avvike fra det som vises i totalfeltene. Dette skyldes vanligvis avrundingsberegninger i forbindelse med mva eller salgsmva.
    >
    > Når du skal kontrollere beløpene som faktisk skal bokføres, kan du bruke siden **Statistikk**, som tar hensyn til avrundingsberegningene. Hvis du velger **Frigi**-handlingen, oppdateres totaler-feltene slik at de omfatter avrundingsberegninger.
9. I feltet **Fakturarabattbeløp** angir du eventuelt et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.**.

    Hvis du har definert fakturarabatter for kunden, settes den angitte prosentverdien automatisk inn i feltet **Fakturarabatt %** hvis kriteriene er oppfylt, og det relaterte beløpet settes inn i feltet **Fakturarabattbeløp før mva.**. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).  
10. Når salgsfakturalinjene er fullført, kan du velge handlingen **Bokfør og send**.  

Dialogboksen **Bokfør og send bekreftelse** viser kundens foretrukne metode for mottak av dokumenter. Du kan endre sendemetoden ved å velge oppslagsknappen for feltet **Send dokument til**. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).

Beslektet element og kundeposter opprettes nå i systemet, og salgsfakturaen skrives ut som et PDF-dokument. Salgsfakturaen fjernes fra listen over salgsfakturaer og erstattes med et nytt dokument i listen over bokførte salgsfakturaer.  

### <a name="calculating-invoice-discounts-on-sales"></a>Beregning av fakturarabatter på salg

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="registering-payments"></a>Registrering av betalinger

Avhengig av forretningsbehovene kan du få betalt og registrere betalingen på ulike måter: manuelt, automatisk og via betalingstjenester.  

Du kan behandle betalingene rett fra kundekortet. Bruk handlingen **Registrer kundebetalinger** for å få en oversikt over ubetalte fakturaer for denne kunden. Merk deretter fakturaen som betalt delvis eller fullstendig. Denne betalingsavstemmingen behandler kundens betalinger ved å avstemme beløp som er mottatt på bankkontoen med de relaterte ubetalte salgsfakturaene og deretter bokføre betalingene. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger automatisk](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

I forretningsmiljøer der kunden betaler en stund etter levering, i henhold til betalingsbetingelsene, blir en bokført salgsfaktura værende åpen (ubetalt) til regnskapsavdelingen bekrefter at betalingen er mottatt, og utligner betalingen mot den bokførte salgsfakturaen, Dette kan gjøres manuelt eller automatisk. Hvis du vil ha mer informasjon, se [Avstem kundebetalinger med innbetalingskladden eller fra kundeposter](receivables-how-apply-sales-transactions-manually.md) og [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).  

I forretningsmiljøer der kunden betaler umiddelbart, for eksempel ved PayPal eller kontant, registreres betalingen umiddelbart når du bokfører salgsfakturaen, det vil si at den bokførte salgsfakturaen lukkes som fullstendig utlignet. Du velger den relevante metoden i **Betalingsmåte - kode**-feltet i ordren. Se under trinn 8. For elektroniske betalinger, for eksempel PayPal, må du også fylle ut feltet **Betalingstjeneste**. Hvis du vil ha mer informasjon, kan du se [Aktivere kundebetalinger gjennom betalingstjenester](sales-how-enable-payment-service-extensions.md).  

Du kan opprette direkte betalte fakturaer for kunder som ikke er registrert ved å definere et kontant kundekort, som du velger på salgsfakturaen. Du finner mer informasjon under [Definere kontantkunder](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Hvis du vil sende kundene purringer om forfalte betalinger, må du definere purregrader og betingelser. Hvis du vil ha mer informasjon, kan du se [Definer betingelser og grader for purringer](finance-setup-reminders.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/invoicing-customers-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Skrive ut plukklisten](sales-how-print-picking-list.md)  
[Lager](inventory-manage-inventory.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Innkreve utestående saldi](receivables-collect-outstanding-balances.md)  
[Massefakturering fra Microsoft Bookings i Business Central ](finance-bookings.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]