---
title: Periodiser inntekter og utgifter
description: 'Finn ut hvordan du automatisk periodiserer eller utsetter inntekter og utgifter i perioder da transaksjonen ikke ble bokført i, eller utsetter dem etter en angitt tidsplan.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: postpone
ms.search.form: '1700, 1701, 1702, 1703, 1704, 1705, 1706, 1707'
ms.date: 08/08/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="defer-revenues-and-expenses"></a>Periodiser inntekter og utgifter

Hvis du føre inn en inntekt eller en utgift i en annen periode enn perioden som transaksjonen ble bokført, kan du periodisere inntekter og utgifter automatisk etter en angitt tidsplan.

Hvis du vil fordele inntekter eller utgifter på de aktuelle regnskapsperiodene, konfigurerer du en periodiseringsmal for ressursen, varen eller finanskontoen, som det vil bli bokført inntekt eller utgift for. Når du bokfører det aktuelle salgs- eller kjøpsdokumentet, periodiseres inntekter eller utgifter til de aktuelle regnskapsperiodene i henhold til en tidsplan for periodisering som styres av innstillingene i malen for periodisering og bokføringsdatoen.

> [!NOTE]
> Salgs- og kjøpskladder validerer kildesporet. Valideringen krever at kildekoden for henholdsvis salgs- og salgskladder og kjøps- og kjøpskladder ikke er identiske når du bruker utsettelser. Hvis den er konfigurert til å være identisk, kan du omgå denne begrensningen ved å opprette en mal og sats som bruker en annen kildekode.

## <a name="to-set-up-a-gl-account-for-deferral"></a>Slik definerer du finanskonti for periodisering

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene som er nødvendige for å opprette en finanskonto for periodiserte inntekter. Hvis du vil ha mer informasjon, kan du se [Finans og kontoplanen](finance-general-ledger.md).
4. Gjenta trinn 2 og 3 for å opprette en ny finanskonto for periodiserte utgifter.

For begge typer periodisering velger du **Balanse** i **Type**-feltet og gir navn til kontoene, for eksempel "Ikke tjent inntekt" for periodisert inntekt og "Ubetalte utgifter" for periodiserte utgifter.

## <a name="to-set-up-a-deferral-template"></a>Slik definerer du mal for periodisering

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Maler for periodisering**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov.
4. I **Beregningsmetode**-feltet angi du hvordan **Beløp**-feltet beregnes for hver periode på siden **Tidsplan for periodisering**. Du kan velge mellom følgende alternativer:

   * **Lineær**: De periodiske periodiseringsbeløpene beregnes etter antall perioder, distribuert i henhold til periodelengde.
   * **Lik per periode**: De periodiske utsettelsesbeløpene beregnes i henhold til antall perioder, fordelt jevnt på perioder.
   * **Dager per periode**: De periodiske utsettelsesbeløpene beregnes etter antall dager i perioden.
   * **Brukerdefinert**: De periodiske utsettelsesbeløpene beregnes ikke. Du må manuelt fylle ut **Beløp**-feltet for hver periode på siden Tidsplan for periodisering. Hvis du vil ha mer informasjon, kan du se avsnittet Slik endrer du en tidsplan for periodisering fra en salgsfaktura.
5. I **Periodebeskr.** -feltet angir du en beskrivelse som vises i poster for periodiseringsbokføringen. Du kan angi plassholderkodene nedenfor en for vanlige verdier som skal settes inn automatisk når periodebeskrivelsen vises.

   * %1 = Dagnummeret for periodebokføringsdatoen
   * %2 = Ukenummeret for periodebokføringsdatoen
   * %3 = Månedsnummeret for periodebokføringsdatoen
   * %4 = Månedsnavnet for periodebokføringsdatoen
   * %5 = Regnskapsperiodenavnet for periodebokføringsdatoen
   * %6 = Regnskapsåret for periodebokføringsdatoen

Eksempel: Bokføringsdatoen er 06.02.2016. Hvis du angir "Utgifter periodisert for %4 %6", blir beskrivelsen som vises "Utgifter periodisert for februar 2016".

## <a name="to-assign-a-deferral-template-to-an-item"></a>Slik tilordner du en mal for periodisering til en vare

> [!NOTE]  
> Fremgangsmåten i denne prosedyren er den samme som når du tilordner en mal for periodisering til en finanskonto eller ressurs.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Åpne kortet for varen som inntekter eller utgifter skal periodiseres for til regnskapsperiodene da varen ble solgt eller kjøpt.
3. På **hurtigfanen Kostnader og bokføring** i **feltet Standard utsettelsesmal** Velg du den aktuelle utsettelsesmalen.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>Slik endrer du en tidsplan for periodisering fra en salgsfaktura

> [!NOTE]  
> Trinnene i denne fremgangsmåten er de samme som når du endrer en tidsplan for periodisering, for utgifter, fra en kjøpsfaktura.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsfakturaer**, og velg deretter den relaterte koblingen.
2. Opprett en salgsfaktura for en vare som er tilordnet en mal for periodisering. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md).

    Legg merke til at så snart du angir varen (eller ressursen eller finanskontoen) på fakturalinjen, fylles **Periodiseringskode**-feltet ut med koden til den tildelte malen for periodisering.
3. Velg handlingen **Tidsplan for periodisering**.
4. På siden **Tidsplan for periodisering** endrer du innstillingene på hodet eller verdiene på linjen, for eksempel for å periodisere beløpet til en ekstra regnskapsperiode.
5. Velg handlingen **Beregn tidsplan**.
6. Velg **OK**. Tidsplanen for periodisering oppdateres for salgsfakturaen. Relaterte malen for periodisering forblir uendret.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Slik forhåndsviser du hvordan periodiserte inntekter eller utgifter skal bokføres i finans

> [!NOTE]  
> Trinnene i denne fremgangsmåten er de samme som når du forhåndsviser hvordan periodisering av utgift bokføres.

1. På siden **Salgsfaktura** velger du handlingen **Forhåndsvis bokføring**.
2. På siden **Forhåndsvisning av bokføring** velger du **Finanspost**-handlingen og deretter handlingen **Vis relaterte poster**.

Finansposter som skal posteres til den angitte periodiseringskontoen, for eksempel Ikke tjent inntekt, er merket med beskrivelsen du skrev inn i **Periodebeskr.** -feltet i malen for periodisering, for eksempel "Utgifter periodisert for februar 2016".

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>Slik ser du gjennom bokførte periodiseringer i rapporten Periodiseringssammendrag for Salg

> [!NOTE]  
> Trinnene i denne fremgangsmåten er de samme som når du ser gjennom rapporten Periodiseringssammendrag for Kjøp.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Periodiseringssammendrag for Salg**, og velg deretter den relaterte koblingen.
2. På siden **Periodiseringssammendrag for Salg** i **Saldo per**-feltet, angir du den siste datoen du vil se periodiserte inntekter for.
3. Velg **Forhåndsvisning**-knappen.

## <a name="to-specify-a-period-in-which-to-allow-deferral-posting"></a>Slik angir du en periode der du kan tillate periodiseringsbokføring

Du kan angi en periode der brukere kan bokføre transaksjoner, ved å angi datoer i feltene **Bokf. tillatt fra** og **Bokf. tillatt til** på følgende måte:

* For alle brukere på siden **Finansoppsett**
* For bestemte brukere på siden **Brukeroppsett**

Hvis du har gjort det, må du gjøre et unntak for periodiseringer for at de skal kunne bokføres utenfor perioden. Hvis du vil definere perioden, følger du disse trinnene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansoppsett** eller **Brukeroppsett**, og velg deretter den relaterte koblingen.
2. I feltene **Tillat periodiseringsbokføring fra** og **Tillat periodiseringsbokføring til** angir du en start- og sluttdato for perioden.

### <a name="video-guidance"></a>Videoveiledning

Den følgende videoen viser hvordan du definerer perioden der du lar folk legge inn periodiserte inntekter og utgifter, og hvordan du spesifiserer unntak.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fG6C]

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
