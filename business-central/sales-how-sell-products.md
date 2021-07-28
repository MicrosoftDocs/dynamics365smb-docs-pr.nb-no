---
title: Opprette en ordre og selge varer | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en ordre for å registrere avtalen med en kunde om å selge eller handle med produkter i samsvar med bestemte betingelser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 67d7ad0d10ddc5c6065df482c7ceb4b98058d504
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436729"
---
# <a name="sell-products"></a>Selge produkter

Du kan opprette en ordre eller salgsfaktura for å registrere avtalen med en kunde om å selge bestemte produkter på bestemte leverings- og betalingsbetingelser.

> [!NOTE]  
> Bruk ordrer hvis salgsprosessen krever at du kan sende deler av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke er tilgjengelig samtidig. Hvis du bruker salgsfakturaer, antar [!INCLUDE [prod_short](includes/prod_short.md)] at du leverer hele antallet når du bokfører fakturaen. Hvis du selger varer ved å levere direkte fra leverandøren til kunden, som en direkte levering, må du også å bruke ordrer. Hvis du vil ha mer informasjon, kan du se [Foreta direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer ordrer på samme måte som salgsfakturaer. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md).

Du kan forhandle med kunden ved først å opprette et tilbud, som du kan konvertere til en ordre når dere blir enige om salget. Hvis du vil ha mer informasjon, kan du se [Gi salgstilbud](sales-how-make-offers.md).

Etter at kunden har bekreftet avtalen, for eksempel etter en tilbudsprosess, kan du sende en ordrebekreftelse for å registrere din forpliktelse til å levere produktene som avtalt.

Når du leverer produkter, helt eller delvis, kan du bokføre ordren som levert eller som levert og fakturert for å opprette de beslektede vare- og kundepostene i systemet. Når du bokfører ordren, kan du også sende dokumentet som et PDF-vedlegg i e-post. Du kan få brødteksten i e-posten forhåndsutfylt med et sammendrag av ordren og betalingsinformasjonen, for eksempel en kobling til PayPal. Hvis du vil ha mer informasjon, kan du se [Sende dokumenter i e-post](ui-how-send-documents-email.md).

I forretningsmiljøer der kunden betaler en stund etter levering, i henhold til betalingsbetingelsene, blir en bokført salgsfaktura værende åpen (ubetalt) til regnskapsavdelingen bekrefter at betalingen er mottatt, og utligner betalingen mot den bokførte salgsfakturaen, Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).

I forretningsmiljøer der kunden betaler umiddelbart, for eksempel ved PayPal eller kontant, registreres betalingen umiddelbart når du bokfører salgsfakturaen som fakturert, det vil si at den bokførte salgsfakturaen lukkes som fullstendig utlignet. Du velger den relevante metoden i **Betalingsmåte - kode**-feltet i ordren. Se under trinn 8. For elektroniske betalinger, for eksempel PayPal, må du også fylle ut feltet **Betalingstjeneste**. Hvis du vil ha mer informasjon, kan du se [Aktivere kundebetalinger gjennom betalingstjenester](sales-how-enable-payment-service-extensions.md).

Du kan opprette direkte betalte ordrer for kunder som ikke er registrert ved å definere et kontant kundekort, som du velger på ordren. Du finner mer informasjon under [Definere kontantkunder](finance-how-to-set-up-cash-customers.md).

Du kan enkelt å løse eller annullere en bokført salgsfaktura som resultat av en ordre før den er betalt. Dette er praktisk hvis du vil rette en skrivefeil, eller hvis kunden ber om en endring tidlig i ordreprosessen. Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md). Hvis den bokførte salgsfakturaen er betalt, må du opprette en salgskreditnota for å reversere salget. Hvis du vil ha mer informasjon, kan du se [Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md).

Varekortet kan være av typen **Lager**, **Service** eller **Ikke-lagervarer** for å angi om varen er en fysisk lagerenhet, en arbeidstidsenhet eller en fysisk enhet som ikke beholdes i lagerbeholdningen. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md). Ordreprosessen er den samme for alle de tre varetypene.

Du kan fylle kundefelt i ordren på to måter, avhengig av om kunden allerede er registrert. Se trinn 2 i fremgangsmåten nedenfor.

## <a name="to-create-a-sales-order"></a>Opprette en ordre

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. I feltet **Kunde** angir du navnet på en eksisterende kunde.

    Andre felt på siden **Ordre** fylles nå med standardinformasjon for den valgte kunden.  

    [!INCLUDE [sales-create-customer](includes/sales-create-customer.md)]  

    Flere felt i ordren er nå fylt ut med informasjon du har angitt på det nye kundekortet.
3. Fyll ut resten av feltene på siden **Ordre** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hvis du vil at kunden betaler umiddelbart, for eksempel ved kredittkort eller PayPal, fyller du ut feltet **Betalingsmåte - kode**. Betalingen registreres deretter når du bokfører ordren som fakturert. Hvis du velger KONTANT, registreres betalingen på en bestemt motkonto.

    Du kan nå begynne å fylle ut ordrelinjene med lagervarer eller tjenester du vil selge til kunden.

    Hvis du har definert gjentakende salgslinjer for kunden, for eksempel en månedlig etterfyllingsordre, kan du sette inn disse linjene på ordren ved å velge handlingen **Hent gjentakende salgslinjer**.
4. På **Linjer**-hurtigfanen i **Type**-feltet velger du typen produkt, tillegg eller transaksjon som du vil legge til for kunden med salgslinjen.

5. I **Nr.** -feltet, angir du nummeret for en lagervare eller service.

    La feltet **Nr.** stå tomt i følgende tilfeller:

    * Hvis linjen er for en kommentar. Skriv inn kommentaren i **Beskrivelse**-feltet.
    * Hvis linjen er for en katalogvare. Velg handlingen **Velg katalogvarer**. Hvis du vil ha mer informasjon, kan du se [Arbeide med katalogvarer](inventory-how-work-nonstock-items.md).
6. I feltet **Antall** angir du hvor mange varer som skal selges.

    > [!NOTE]  
    > For varer av typen *Ressurs* eller *Tjeneste* er antallet en tidsenhet, for eksempel timer, som angitt i feltet **Enhetskode** på linjen. Hvis du vil ha mer informasjon, kan du se [Definere vareenheter](inventory-how-setup-units-of-measure.md).

    Feltet **Linjebeløp** oppdateres for å vise verdien i feltet **Salgspris** multiplisert med verdien i feltet **Antall**.

    Prisen og linjebeløpene vises med eller uten mva, avhengig av hva du valgte i feltet **Priser inkludert merverdiavgift** på kundekortet.
7. I feltet **Linjerabatt-%** angir du en prosent hvis du vil gi kunden en rabatt på produktet. Verdien i feltet **Linjebeløp** oppdateres tilsvarende.

    Hvis du har konfigurert varepriser i hurtigfanen **Salgspriser og salgslinjerabatter** i kunde- eller varekortet, oppdateres prisen og beløpet på tilbudslinjen automatisk hvis de avtalte priskriteriene er oppfylt. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).
8. Hvis du vil legge til en kommentar om tilbudslinjen som kunden kan se på tilbudsutskriften, skriver du en tekst i **Beskrivelse**-feltet på en tom linje.  
9. Gjenta trinn 4 til 8 for hver vare som du vil selge til kunden.

    Totaler-feltene under linjene oppdateres automatisk når du oppretter eller endrer linjer for å vise beløpene som skal bokføres i postene.

    > [!NOTE]
    > I svært sjeldne tilfeller kan de bokførte beløpene avvike fra det som vises i totalfeltene. Dette skyldes vanligvis avrundingsberegninger i forbindelse med mva eller salgsmva.
    >
    > Når du skal kontrollere beløpene som faktisk skal bokføres, kan du bruke siden **Statistikk**, som tar hensyn til avrundingsberegningene. Hvis du velger **Frigi**-handlingen, oppdateres totaler-feltene slik at de omfatter avrundingsberegninger.  

10. I feltet **Fakturarabattbeløp** angir du eventuelt et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.**.

    Hvis du har definert fakturarabatter for kunden, settes den angitte prosentverdien automatisk inn i feltet **Fakturarabatt %** hvis kriteriene er oppfylt, og det relaterte beløpet settes inn i feltet **Fakturarabattbeløp før mva.**. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).
11. Hvis du vi sende bare en del av ordreantallet, kan du angi antallet i den feltet **Levere (antall)**. Verdien kopieres til feltet **Fakturer (antall)**.
12. Hvis du vi fakturere bare en del av det sendte antallet, kan du angi antallet i den feltet **Fakturer (antall)**. Antallet må være lavere enn verdien i feltet **Levere (antall)**.  
13. Når ordrelinjene er fullført, kan du velge handlingen **Bokfør og send**.

Dialogboksen **Bokfør og send bekreftelse** viser kundens foretrukne metode for mottak av dokumenter. Du kan endre sendemetoden ved å velge oppslagsknappen for feltet **Send dokument til**. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).

Beslektet element og kundeposter opprettes nå i systemet, og ordren skrives ut som et PDF-dokument. Når ordren er fullstendig bokført, fjernes fra listen over ordrer og erstattes med nye dokumenter i listen over bokførte salgsfakturaer og oversikten over bokførte følgesedler.  

## <a name="external-document-number"></a>Eksternt dokumentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Skrive ut plukklisten](sales-how-print-picking-list.md)  
[Lager](inventory-manage-inventory.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]