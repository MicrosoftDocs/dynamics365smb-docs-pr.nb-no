---
title: Opprett en kundeordre og selg varer
description: Beskriver hvordan du oppretter en ordre for å registrere avtalen med en kunde om å selge eller handle med produkter i samsvar med bestemte betingelser.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, partial deliveries, customer sales order, shipping advice, partial shipments,'
ms.search.form: '42, 48, 9305'
ms.date: 09/02/2022
ms.author: bholtorf
---
# <a name="sell-products-with-a-customer-sales-order"></a>Selg produkter ed en kundeordre

Denne artikkelen gir veiledning om når du skal bruke en kundeordre i tillegg til en faktura. Hvis salgsprosessen krever at du bare sende deler av et ordre, kanskje fordi det fullstendige antallet ikke er tilgjengelig samtidig, må du behandle salget ved å lage en ordre.

Du må også bruke ordrer hvis du selger varer som leveres direkte fra leverandøren til kunden, som kalles en direkte levering. Finn ut mer under [Lag direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer ordrer på samme måte som salgsfakturaer. Finn ut mer under [Fakturer salg](sales-how-invoice-sales.md).

Når du leverer produkter, helt eller delvis, kan du bokføre ordren som levert eller som levert og fakturert for å opprette de beslektede vare- og kundepostene i systemet. Når du bokfører ordren, kan du også sende den som et PDF-vedlegg i e-post. Du kan få brødteksten i e-posten forhåndsutfylt med et sammendrag av ordren og betalingsinformasjonen, for eksempel en kobling til PayPal. Finn ut mer under [Lever varer](warehouse-how-ship-items.md) og [Send dokumenter i e-post](ui-how-send-documents-email.md).

I forretningsmiljøer der kunden betaler umiddelbart, for eksempel ved PayPal eller kontant, registreres betalingen umiddelbart når du bokfører salgsfakturaen som fakturert, det vil si at den bokførte salgsfakturaen lukkes som fullstendig utlignet. Du velger den relevante metoden i **Betalingsmåte – kode**-feltet i ordren. Se trinn 5 nedenfor. For elektroniske betalinger, for eksempel PayPal, må du også fylle ut feltet **Betalingstjeneste**. Finn ut mer under [Aktiver kundebetalinger gjennom betalingstjenester](sales-how-enable-payment-service-extensions.md).

Du kan opprette direkte betalte ordrer for kunder som ikke er registrert ved å definere et kontant kundekort, som du velger på ordren. Finn ut mer under [Definer kontantkunder](finance-how-to-set-up-cash-customers.md).

## <a name="create-a-sales-order"></a>Opprett en ordre

> [!NOTE]  
> Følgende fremgangsmåte forutsetter at kunden allerede er konfigurert. Hvis du vil ha instruksjoner om hvordan du gjør dette, kan du se [Registrer nye kunder](sales-how-register-new-customers.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Velg **Ny** for å opprette en ny post.
3. I feltet **Kunde** angir du navnet på en eksisterende kunde.

    Andre felter på siden **Ordre** fylles nå med standardinformasjon om den valgte kunden.  

4. Fyll ut resten av feltene på siden **Ordre** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hvis du vil at kunden betaler umiddelbart, for eksempel ved kredittkort eller PayPal, fyller du ut feltet **Betalingsmåte - kode**. Betalingen registreres deretter når du bokfører ordren som fakturert. Hvis du velger *kontant*, registreres betalingen på en bestemt motkonto.

    Du kan nå begynne å fylle ut ordrelinjene med lagervarer eller tjenester du vil at kunden skal kjøpe.

    Hvis du har definert gjentakende salgslinjer for kunden, for eksempel en månedlig etterfyllingsordre, kan du sette inn disse linjene på ordren ved å velge handlingen **Hent gjentakende salgslinjer**.
5. På **Linjer**-hurtigfanen i **Type**-feltet velger du typen produkt, tillegg eller transaksjon som du vil legge til for kunden på salgslinjen.

6. I **Nr.** -feltet, angir du nummeret for en lagervare eller service.

    La feltet **Nr.** stå tomt hvis linjen er for en:

    * Merknad. Skriv inn kommentaren i **Beskrivelse**-feltet.
    * Katalogvare. Velg handlingen **Velg katalogvarer**. Finn ut mer under [Arbeid med katalogvarer](inventory-how-work-nonstock-items.md).
7. I feltet **Antall** angir du hvor mange varer som skal selges.

    > [!NOTE]  
    > For varer av typen *Ressurs* eller *Tjeneste* er antallet en tidsenhet, for eksempel timer, som angitt i feltet **Enhetskode** på linjen. Finn ut mer under [Definer vareenheter](inventory-how-setup-units-of-measure.md).

    Feltet **Linjebeløp** oppdateres for å vise verdien i feltet **Salgspris** multiplisert med tallet i feltet **Antall**.

    Prisen og linjebeløpene vises med eller uten mva, avhengig av hva du valgte i feltet **Priser inkludert merverdiavgift** på kundekortet.
8. I feltet **Linjerabatt-%** angir du en prosent hvis du vil gi kunden en rabatt på produktet. Verdien i feltet **Linjebeløp** oppdateres tilsvarende.

    Hvis du har konfigurert varepriser i hurtigfanen **Salgspriser og salgslinjerabatter** i kunde- eller varekortet, oppdateres prisen og beløpet på tilbudslinjen automatisk hvis de avtalte priskriteriene er oppfylt. Finn ut mer under [Registrer avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).
9. Hvis du vil legge til en kommentar om ordrelinjen som kunden kan se på ordreutskriften, skriver du en kommentar på en tom linje i **Beskrivelse**-feltet.  
10. Gjenta trinn 5 til 9 for hver vare som du vil at kunden skal kjøpe.

    Totaler-feltene under linjene oppdateres automatisk når du oppretter eller endrer linjer for å vise beløpene som skal bokføres i postene.

    > [!NOTE]
    > I svært sjeldne tilfeller kan de bokførte beløpene avvike fra det som vises i totalfeltene. Dette skyldes vanligvis avrundingsberegninger i forbindelse med mva. eller salgsmva.
    >
    > Når du skal kontrollere beløpene som faktisk skal bokføres, kan du bruke siden **Statistikk**, som tar hensyn til avrundingsberegningene. Hvis du velger **Frigi**-handlingen, oppdateres totaler-feltene slik at de omfatter avrundingsberegninger.  

11. I feltet **Fakturarabattbeløp** angir du eventuelt beløpet som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.**.

    Hvis du har definert fakturarabatter for kunden, settes den angitte prosentverdien automatisk inn i feltet **Fakturarabatt %** hvis kriteriene er oppfylt, og det relaterte beløpet settes inn i feltet **Fakturarabattbeløp før mva.**. Finn ut mer under [Registrer avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).
12. Hvis du bare vil sende en del av ordreantallet, kan du angi antallet i den feltet **Levere (antall)**. Verdien kopieres automatisk til feltet **Fakturer (antall)**.

    > [!NOTE]
    > Hvis feltet **Leveringsønske** er definert som **Komplett** på hurtigfanen **Levering og fakturering**, kan du ikke bokføre delleveranser. Finn ut mer under [Behandle delvise leveringer](sales-how-send-partial-shipments.md).
13. Hvis du bare vil fakturere en del av det sendte antallet, kan du angi antallet i den feltet **Fakturer (antall)**. Antallet må være lavere enn verdien i feltet **Levere (antall)**.  
14. Når ordrelinjene er fullført, kan du velge handlingen **Bokfør og send**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Dialogboksen **Bokfør og send bekreftelse** viser kundens foretrukne metode for mottak av dokumenter. Du kan endre sendemetoden ved å velge oppslagsknappen for feltet **Send dokument til**. Finn ut mer under [Definer en profil for dokumentsending](sales-how-setup-document-send-profiles.md).

Beslektet element og kundeposter opprettes nå i systemet, og ordren skrives ut som et PDF-dokument. Når ordren er fullstendig bokført, fjernes fra listen over ordrer og erstattes med nye dokumenter i listen over bokførte salgsfakturaer og oversikten over bokførte følgesedler.  

## <a name="external-document-number"></a>Eksternt dokumentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Se også

[Fakturer salg](sales-how-invoice-sales.md)  
[Bokføre salg](ui-post-sales.md)  
[Lever varer](warehouse-how-ship-items.md)  
[Lag direkte levering](sales-how-drop-shipment.md)  
[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Skriv ut plukklisten](sales-how-print-picking-list.md)  
[Behandle delleveringer](sales-how-send-partial-shipments.md)  
[Lager](inventory-manage-inventory.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
