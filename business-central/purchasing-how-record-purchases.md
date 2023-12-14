---
title: Registrere kjøp med kjøpsfakturaer (inneholder video)
description: 'Beskriver hvordan du kan kjøpe beholdning, ikke-lagervarer eller ressurser ved å opprette og bokføre kjøpsfakturaer eller ordrer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.search.form: '50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310'
ms.date: 11/01/2023
ms.author: bholtorf
---
# <a name="record-purchases-with-purchase-invoices-and-orders"></a>Registrere kjøp med kjøpsfakturaer og ordrer

Du kan opprette en kjøpsfaktura eller bestilling for å registrere kjøpskostnader og spore leverandørgjeld. Kjøpsfakturaer og bestillinger brukes også til å oppdatere lagernivåer dynamisk, noe som betyr at du kan redusere lagerkostnadene og gi bedre kundeservice. Kjøpskostnadene, inkludert tjenesteutgifter samt lagerverdier som er resultat av bokføring av kjøpsfakturaer eller ordrer, bidrar til fortjenestetall og andre økonomiske ytelsesindikatorer i rollesenteret.

## <a name="record-purchases-with-purchase-invoices"></a>Registrere kjøp med kjøpsfakturaer

Når du mottar lagervarene eller den kjøpte tjenesten er fullført, kan du bokføre kjøpsfakturaen for å oppdatere lager- og økonomiposter og aktivere betaling til leverandøren i samsvar med betalingsbetingelsene. [Utføre betalinger](payables-make-payments.md).

> [!CAUTION]  
> Ikke bokfør fysiske varer for en kjøpsfaktura før du mottar varene og kjenner de endelige kostnadene for kjøpet, herunder eventuelle tilleggskostnader. Hvis ikke, kan det hende at lagerverdien og fortjenestebeløpet er skjevt.

### <a name="create-and-post-a-purchase-invoice"></a>Opprett og bokfør en kjøpsfaktura

Nedenfor ser du en beskrivelse av hvordan du oppretter en kjøpsfaktura. Trinnene for å opprette en bestilling ligner. Hovedforskjellen er at bestillinger har noen ekstra felter og handlinger for fysisk håndtering av varer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. I feltet **Leverandør** angir du navnet på en eksisterende leverandør.

    Andre felt på siden **Kjøpsfaktura** fylles nå med standardinformasjon for den valgte leverandøren. Hvis leverandøren ikke er registrert, følger du denne fremgangsmåten:

    1. I feltet **Leverandør** angir du navnet på den nye leverandøren.
    2. Velg **Ja** i dialogboksen for å registrere den nye leverandøren.
    3. Hvis du vil vite mer om hvordan du fyller ut leverandørkortet, kan du gå til [Registrer nye leverandører](purchasing-how-register-new-vendors.md).  
    4. Når du har fullført leverandørkortet, velger du **OK** for å gå tilbake til **Kjøpsfaktura**-siden.

3. Fyll ut resten av feltene på siden **Kjøpsfaktura** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du kan nå begynn å fylle ut kjøpsfakturalinjene med varer eller ressurser kjøpt fra leverandøren.

    > [!NOTE]  
    > Hvis du har definert gjentakende bestillingslinjer for leverandøren, for eksempel en månedlig etterfyllingsordre, kan du sette inn disse linjene på fakturaen ved å velge handlingen **Hent gjentakende bestillingslinjer**.
4. Angi nummeret på en vare eller en tjeneste i **Varenr.**-feltet i hurtigfanen **Linjer**.
5. I feltet **Antall** angir du hvor mange varer som skal kjøpes.

    Feltet **Linjebeløp** oppdateres for å vise verdien i feltet **Direkte enhetskost** multiplisert med verdien i feltet **Antall**.

    Prisen og linjebeløpet vises med eller uten mva, avhengig av hva du velger i feltet **Priser inkludert merverdiavgift** på leverandørkortet.

    Totaler-feltene under linjene oppdateres automatisk når du oppretter eller endrer linjer for å vise beløpene bokført postene.

6. I feltet **Fakturarabattbeløp** angir du et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.** nederst på fakturaen.

    > [!NOTE]  
    > Hvis du har definert fakturarabatter for leverandøren, settes den angitte prosentverdien automatisk inn i feltet **Leverandørfakturarabatt-%** hvis kriteriene er oppfylt. Det relaterte beløpet settes inn i feltet **Fakturarabattbeløp**.
7. Velg **Bokfør** når du mottar innkjøpte varer eller tjenester.

Kjøpet gjenspeiles nå i beholdningen, ressursposter og økonomiposter, og leverandørbetalingen aktiveres. Kjøpsfakturaen fjernes fra listen over kjøpsfakturaer og erstattes med et nytt dokument i listen over bokførte kjøpsfakturaer.  Hvis du vil ha mer informasjon om hva som skjer når du bokfører kjøpsdokumenter, kan du se [Bokfør kjøp](purchasing-how-record-purchases.md#posting-purchases).

> [!NOTE]
> I sjeldne tilfeller kan de bokførte beløpene avvike fra det som vises i totalfeltene. Dette skyldes vanligvis avrundingsberegninger i forbindelse med mva. eller salgsmva.
>
> Når du skal kontrollere beløpene som faktisk skal bokføres, kan du gå til siden **Statistikk**, som tar hensyn til avrundingsberegningene. Hvis du velger **Frigi**-handlingen, oppdateres totaler-feltene slik at de omfatter avrundingsberegninger.

## <a name="posted-invoices"></a>Bokførte fakturaer

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Du kan enkelt korrigere eller annullere en bokført kjøpsfaktura før du betaler leverandøren. Dette er praktisk hvis du må rette en skrivefeil eller endre kjøpet tidlig i bestillingsprosessen. Finn ut mer under [Korriger eller annuller ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Hvis du vil tilbakeføre et kjøp for varer eller tjenester oppført i den bokførte kjøpsfakturaen som betalingen behandles for, må du opprette en kjøpskreditnota. Finn ut mer under [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

[Åpne listen **Bokførte kjøpsfakturaer**](https://businesscentral.dynamics.com/?page=146) i [!INCLUDE [prod_short](includes/prod_short.md)].


## <a name="purchasing-non-inventory-items"></a>Kjøp av ikke-lagervarer

Linjene på en kjøpsfaktura kan være av typen **Ressurs** eller **Vare**. Varekort kan også klassifiseres av typen **Lager**, **Service** eller **Ikke-lagervarer** som angir om varen er en fysisk lagerenhet, en arbeidstidsenhet (gjelder også ressurser) eller en fysisk enhet som ikke holdes i lagerbeholdningen. Finn ut mer under [Registrer nye varer](inventory-how-register-new-items.md). Kjøpsfakturaprosessen er den samme for alle typene nevnt ovenfor.

> [!NOTE]
> Med kjøpslinjetypen **Ressurs** kan du også kjøpe eksterne ressurser, for eksempel for å fakturere en leverandør for arbeid som er levert. Finn ut mer under [Definer ressurser](projects-how-setup-resources.md).
>
> Hvis du vil bruke en kjøpt ressurs, må du kanskje angi ressursens kapasitet og tilordne den manuelt til et prosjekt. Kjøp av en ressurs oppretter en ressurspost, men ressursposter spores imidlertid ikke for antall og verdi, for eksempel varer. Hvis antalls- og verdisporing er nødvendig, kan du vurdere å bruke andre linjeelementtyper.

## <a name="when-to-use-purchase-orders"></a>Når du bør bruke bestillinger

Du må bruke bestillinger hvis kjøpsprosessen krever at du registrerer delvise mottak av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke er tilgjengelig hos leverandøren. Hvis du leverer solgte varer direkte fra leverandøren til kunden, som en direkte levering, må du også å bruke bestillinger. Finn ut mer under [Lag direkte leveringer](sales-how-drop-shipment.md).

I alle andre henseender fungerer bestillinger på samme måte som kjøpsfakturaer. Følgende fremgangsmåte er basert på en kjøpsfaktura. Trinnene er de samme for en bestilling.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="receive-items-with-a-purchase-order"></a>Motta varer med bestilling

Følgende beskriver hvordan du mottar varer med en bestilling. 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Åpne en eksisterende bestilling eller opprett en ny.
3. I feltet **Motta (antall)** angir du det mottatte antallet.

   > [!NOTE]
   > Hvis det mottatte antallet er mer enn antallet i bestillingen, og leverandøren er definert til å tillate overmottak, bruker du feltet **Overmottak** til å håndtere det overflødige antallet. Finn ut mer i delen [Slik mottar du flere varer enn bestilt](purchasing-how-record-purchases.md#receive-more-items-than-ordered).
4. Velg handlingen **Bokfør**.

  Verdien i feltet **Mottatt ant.** oppdateres. Hvis dette er et delvis mottak, vil verdien være mindre enn verdien i feltet **Antall**.

> [!NOTE]
> Hvis du bruker en lagerstyring, kan du ikke bruke handlingen **Bokfør** på bestillingen til å registrere mottaket. Det er fordi en lagerarbeider allerede bokført bestillingsantallet som mottatt. Finn ut mer under [Designdetaljer – Inngående lagerflyt](design-details-inbound-warehouse-flow.md).

## <a name="receive-more-items-than-ordered"></a>Motta flere varer enn bestilt

Når det kommer flere varer enn bestilt, kan det være lurt å motta dem i stedet for å annullere mottaket. Det kan for eksempel være billigere å beholde de overskytende varene i beholdningen enn å returnere dem, eller leverandøren kan tilby deg en rabatt for å beholde leveransen.

<!--move the over-receipt setup info to an article about purchasing. Keep the concept info here and link to the steps-->
### <a name="set-up-over-receipts"></a>Sett opp overmottak

Opprett overmottakskoder for å definere en prosentverdi som et mottatt antall kan overskride det bestilte antallet for. Angi prosenten i feltet **Toleranseprosent for overmottak**. Deretter tildeler du koden på sidene Varekort eller Leverandørkort for varer og leverandører.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Overmottakskoder**, velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="assign-the-over-receipt-code-to-an-item"></a>Tildel overmottakskoden til en vare

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Åpne siden **Varekort** for den relaterte varen.
3. I feltet **Overmottakskode** velger du koden som inneholder prosenten du vil tillate for overmottak.

Overmottakskoden tilordnes til varen. Bestillinger eller lagermottak for varen tillater nå at du mottar mer enn det bestilte antallet innenfor toleranseprosenten for overmottak.

> [!NOTE]
> Du kan definere en godkjenningsarbeidsflyt som krever at overmottak må godkjennes før de kan håndteres. Merk av for **Krever godkjenning** på siden **Overmottakskoder**. Finn ut mer under [Opprett arbeidsflyter](across-how-to-create-workflows.md).

### <a name="over-receive-an-order"></a>Overmottak av en ordre

På kjøpslinjer og lagermottakslinjer brukes feltet **Antall overmottak** til å registrere overmottatt antall, noe som betyr et antall som overskred verdien for bestilt antall i feltet **Antall**.

Når du håndterer et overmottak, kan du øke verdien i feltet **Motta (antall)** til det faktisk mottatte antallet. Feltet **Antall overmottak** oppdateres for å vise det overflødige antallet. Du kan eventuelt angi det ekstra antallet i feltet **Antall overmottak**. Feltet **Motta (antall)** oppdateres for å vise det bestilte antallet pluss det overflødige antallet. Følgende fremgangsmåte beskrev hvordan du fyller ut feltet **Motta (antall)**.  

1. I en bestilling eller et lagermottaksdokument der det mottatte antallet er høyere enn bestilt, angir du det faktiske mottatte antallet i feltet **Motta (antall)**.

    Hvis økningen er innenfor toleransen som er angitt av en tildelt overmottakskode, oppdateres feltet **Antall overmottak** til å vise antallet som verdien i feltet **Aantall** er overskredet med.

    Hvis økningen er over toleransen, er ikke overmottak tillatt. Undersøk om en annen overmottakskode tillater det. Ellers kan bare det bestilte antallet mottas, og det overflødige antallet må håndteres på en annen måte, for eksempel ved å returnere det til leverandøren.

2. Bokfør mottaket på samme måte som for andre mottak.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] håndterer ikke automatisk økonomiske aspekter ved overmottak. Du må håndtere dette manuelt og være enig med leverandøren, for eksempel leverandøren som videresender en ny eller oppdatert faktura.

## <a name="external-document-number"></a>Eksternt dokumentnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="posting-purchases"></a>Bokføre kjøp

I et kjøpsdokument kan du velge mellom følgende bokføringshandlinger:

* **Bokfør**
* **Forhåndsvis bokføring**
* **Bokfør og skriv ut**
<!--* **Test Report**-->
* **Massebokfør**

Når en et kjøpsdokument bokføres, oppdateres leverandørens konto, finans og vareposter, og ressurspostene blir oppdatert.

For hvert kjøpsdokument opprettes det en kjøpspost i tabellen **Finanspost**. Det opprettes også en post på leverandørens konto i **Leverandørpost**-tabellen, og en finanspost opprettes i den relevante samlekontoen. I tillegg kan bokføring av kjøpet resultere i en mva-post og en finanspost for rabattbeløpet. Om en rabattpost skal bokføres, avhenger av innholdet i feltet  **Rabattbokføring** på siden **Kjøpsoppsett**.

Følgende poster blir opprettet for hver kjøpslinje, etter behov, i:

* **Varepost**-tabellen hvis kjøpslinjen er av typen **Vare**.
* **Finanspost**-tabellen hvis kjøpslinjen er av typen **Finanskonto**.
* **Ressurspost**-tabellen hvis kjøpslinjen er av typen **Ressurs**.

I tillegg registreres alltid kjøpsdokumenter i tabellene **Mottakshode** og **Kjøpsfakturahode**.

Du kan alltid se gjennom forskjellige poster som blir opprettet som et resultat av bokføringer. Velg **Forhåndsvis bokføring** for å validere dokument og kontrollere forventede poster.


> [!IMPORTANT]  
> Når du bokfører en bestilling for varer, kan du opprette både et mottak og en faktura. Dette kan gjøres samtidig, eller hver for seg. Du kan også opprette et delvis mottak og en delfaktura ved å fylle ut feltene **Motta (antall)** og **Fakturer (antall)** på de enkelte bestillingsordrelinjene før du bokfører. Legg merke til at du ikke kan opprette en kjøpsfaktura fra en bestilling for produkter eller tjenester som ikke er mottatt. Det vil si at for å kunne fakturere, må du på forhånd ha registrert et mottak, eller du må velge å motta og fakturere samtidig.

Du kan enten bokføre eller bokføre og skrive ut. Hvis du velger å bokføre og skrive ut, skrives det ut en rapport når ordren bokføres. Du kan også velge handlingen **Massebokfør** for å bokføre flere bestillinger samtidig. Finn ut mer under [Bokfør flere dokumenter samtidig](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Vis poster

Når bokføringen er utført, fjernes de bokførte kjøpslinjene fra bestillingen. En melding viser når bokføringen er gjennomført. Etter dette kan du se de bokførte postene på de forskjellige sidene, inkludert sidene **Leverandørposter**, **Finansposter**, **Vareposter**, **Ressursposter**, **Kjøpsmottak** og **Bokførte kjøpsfakturaer**.

I de fleste tilfeller kan du åpne poster fra det berørte kortet eller dokumentet. På siden **Leverandørkort** velger du for eksempel handlingen **Poster**.

## <a name="editing-ledger-entries"></a>Rediger poster

Du kan redigere bestemte felt på bokførte kjøpsdokumenter, for eksempel feltet **Betalingsreferanse**. Finn ut mer under [Rediger bokførte dokumenter](across-edit-posted-document.md). Hvis du vil ha mer kritiske felt som påvirker revisjonssporingen, må du tilbakeføre eller angre bokføringen. Finn ut mer under [Tilbakefør kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md).

## <a name="see-also"></a>Se også

[Be om tilbud](purchasing-how-request-quotes.md)  
[Kjøpvarer for et salg](purchasing-how-purchase-products-sale.md)  
[Klargjøre direkte leveringer](sales-how-drop-shipment.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Definere kjøp](purchasing-setup-purchasing.md)  
[Definere ressurser](projects-how-setup-resources.md)  
[Registrere nye leverandører](purchasing-how-register-new-vendors.md)  
[Redigere bokførte dokumenter](across-edit-posted-document.md)  
[Bokfør flere dokumenter samtidig](ui-batch-posting.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Bokføre dokumenter og kladder](ui-post-documents-journals.md)  
[Korriger eller annuller ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
