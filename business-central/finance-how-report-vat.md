---
title: Sende mva-rapporter til skattemyndighetene
description: 'Lær hvordan du klargjør rapporter som viser mva fra salg i en periode, eller fra salg og kjøp, og sender rapporten til en skattemyndighet.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, tax, report, EC sales list, statement'
ms.search.form: '321, 322, 323, 474, 475, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 9401'
ms.date: 08/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="report-vat-to-tax-authorities"></a>Rapportere mva til skattemyndighetene

Denne artikkelen beskriver rapportene [!INCLUDE[prod_short](includes/prod_short.md)] du kan bruke til å sende inn informasjon om merverdiavgiftsbeløp (mva.) for salg og kjøp til skattemyndighetene i din region. Avhengig av landet/regionen kan rapportene inneholde spesifikk informasjon, eller Der kan være flere rapporter du må sende inn. Se artiklene for ditt land/område i delen [Lokal funksjonalitet](about-localization.md).  

Du kan bruke følgende innebygde rapporter:

* Rapporten **EU-salg – oversikt**  

    Rapporten over salg i EU viser verdien som er lagt til mva-beløp som du har samlet for salg til mva-registrerte kunder i EU-land/-områder.  
* Rapporten **Omsetningsoppgave**  

    Rapporten Omsetningsoppgave inkluderer mva for salg og kjøp for kunder og leverandører i alle land/områder som bruker mva.  

I begge tilfeller (som i andre mva-relaterte rapporter) beregnes mva. på grunnlag av mva-bokføringsoppsettet og mva-bokføringsgruppene du har definert. [!INCLUDE[prod_short](includes/prod_short.md)] viser mva-poster som alltid er basert på **mva-datoen** som en primær rapporteringsdato.  

> [!NOTE]
> Alle mva-relaterte rapporter kan nå kjøres ved hjelp av **mva-datoen** for å filtrere relevante poster. Selv om du setter opp **mva-datobruk** som **Ikke bruk funksjonalitet for mva-dato** skjuler [!INCLUDE[prod_short](includes/prod_short.md)] alle forekomster av **mva-datoen** på tvers av programmet. **Mva-datoen** brukes imidlertid fortsatt i alle rapporter og fylles automatisk ut med **bokføringsdatoen**.

Hvis du vil vise en fullstendig historikk over mva-poster, for hver bokføring som gjelder mva, opprettes en post på siden **mva-poster**. Disse postene brukes til å beregne mva-oppgjørsbeløp, for eksempel betaling eller refusjon, for en bestemt periode. Hvis du vil se mva-poster, velger du ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Mva-poster** og velger deretter den relaterte koblingen.

> [!NOTE]
> Hvert [!INCLUDE[prod_short](includes/prod_short.md)]-miljø er ment å håndtere samsvarsrapporter i ett enkelt land/område. Den nederlandske versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] håndterer for eksempel mva-rapportering i Nederland, men ikke i andre land/områder. På samme måte håndterer USA-versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] 1099-rapportering i USA og støtter ikke mva-rapportering i andre land/områder, med mindre via en utvidelse som leveres av partnerøkosystemet eller en kundespesifikk kodeendring.

## <a name="about-the-ec-sales-list-report"></a><a name="ecsaleslist"></a>Om rapporten EU-salg – oversikt

I EU og Storbritannia må alle selskapene som selger varer og tjenester til mva-registrerte kunder, inkludert kunder i andre EU-land/-områder, sende en elektronisk versjon av rapporten til kundene og skattemyndighetene. **Rapporten EU-salg – oversikt** fungerer bare for land/områder i EU.

Rapporten inneholder én linje for hver type transaksjon med kunden og viser det totale beløpet for hver type transaksjon. Det finnes tre typer transaksjoner som rapporten kan inneholde:  

* B2B-varer (bedrift-til-bedrift)  
* B2B-tjenester  
* Triangulerte B2B-varer  

*B2B*-varer og -tjenester angir om du har solgt en vare eller en service, og styres av innstillingen for **EU-tjeneste** i mva-bokføringsoppsettet. *Triangulerte B2B-varer* angir om du handlet med en tredjepart, og styres av innstillingen for **Trekanthandel** i salgsdokumenter, for eksempel ordrer, fakturaer, kreditnotaer og så videre.  

Når skattemyndighetene har gjennomgått rapporten din, sender de en e-post til kontaktpersonen for firmaet ditt. I [!INCLUDE[prod_short](includes/prod_short.md)] er kontaktpersonen angitt på siden **Selskapsopplysninger**. Før du sender inn rapporten, kontrollerer du at du har valgt en kontaktperson.  

### <a name="submit-an-ec-sales-list-report"></a>Send rapporten EU-salg – oversikt

[!INCLUDE [finance-ecsaleslist](includes/finance-ecsaleslist.md)]

## <a name="about-the-vat-return-report"></a><a name="vatreturn"></a>Om rapporten Omsetningsoppgave

Bruk denne rapporten til å sende inn mva for salg og kjøpsdokumenter, for eksempel innkjøp og ordrer, fakturaer og kreditnotaer. Informasjonen i rapporten vises i samme format som i deklarasjonen fra toll- og avgiftsmyndighetene.  

For omsetningsoppgaven kan du angi postene som skal tas med:

* Sende inn bare åpne transaksjoner eller åpne og lukkede. Dette er for eksempel nyttig når du forbereder endelige årlige omsetningsoppgaven.
* Sende inn bare poster fra de angitte periodene, eller også ta med poster fra tidligere perioder. Dette er nyttig hvis du vil oppdatere en omsetningsoppgave du har allerede har sendt, for eksempel hvis en leverandør sender en faktura for sent.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Koble til webtjenesten til skattemyndigheten
[!INCLUDE[prod_short](includes/prod_short.md)] har tjenestetilkoblinger til nettstedene til skattemyndigheten. Hvis du har Storbritannia, kan du aktivere den **GovTalk** service tilkobling sende EU Salgsoversikt og gå tilbake mva-rapporter elektronisk. Hvis du vil sende inn rapporten manuelt, for eksempel ved å skrive inn dataene dine på skattemyndighetenes nettsted, er dette ikke nødvendig.   

For å kunne rapportere mva til skattemyndighetene elektronisk, må du koble [!INCLUDE[prod_short](includes/prod_short.md)]til webtjenesten til skattemyndigheten. Dette krever at du oppretter en konto hos skattemyndigheten. Når du har en konto, kan du aktivere en tjenestetilkobling vi gir i [!INCLUDE[prod_short](includes/prod_short.md)].

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 2.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tjenestetilkoblinger** og velg riktig kobling.
2. Fyll ut de obligatoriske feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Det er lurt å teste tilkoblingen. Du gjør dette ved å merke av for **Testmodus** og deretter forberede og sende mva-rapporten som beskrevet i delen [Forberede og sende inn en omsetningsoppgave](#to-prepare-and-submit-a-vat-report). I testmodus tester tjenesten om skattemyndighetene kan motta rapporten, og statusen for rapporten angir om testinnsendingen var vellykket. Det er viktig å huske at dette ikke er en faktisk innsending. Hvis du vil faktisk sende inn rapporten, må du fjerne merket for **Testmodus** og deretter gjenta innsendingsprosessen.

## <a name="to-set-up-vat-reports-in-"></a>Slik setter du opp omsetningsoppgaver i [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

### <a name="to-set-up-vat-return-periods"></a>Slik definerer du mva-returperioder

Hvis bedriften din ikke er lokalisert i Storbritannia, kan du eventuelt bruke **siden Mva-returperioder** til å definere planlagte mva-meldinger. Hvis bedriften din er lokalisert i Storbritannia, kan du se [Making Tax Digital i Storbritannia](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md).  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Mva-returperioder**, og velg deretter den relaterte koblingen.  
2. På siden **Mva-retur perioder** fyller du ut feltene for å definere den første perioden. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)].  
3. Gjenta trinn 2 for eventuelle andre perioder du vil legge til.  

Når tiden da har kommet til å sende en mva-rapport for en mva-returperiode, velger du perioden på siden **Mva-returperioder**, og deretter velger du handlingen **Opprett VAR-retur**. Deretter velger du handlingen **Foreslå linjer** på kortet **Mva-retur** som beskrevet i trinn 3 i fremgangsmåten nedenfor.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Slik forbereder du og sender inn en omsetningsoppgave

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **EC Sales List** eller **Mva-meldinger**, og velg deretter den relaterte opprette en kobling.  
2. Velg **Ny**, og fyll deretter ut de obligatoriske feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Du genererer innholdet i rapporten ved å velge handlingen **Foreslå linjer**.  

    > [!NOTE]  
    >  For rapporten EU-salg - oversikt kan du gå gjennom transaksjonene som er inkludert i rapportlinjene, før du sender rapporten. Velg linjen for å gjøre dette, og velg deretter handlingen **Vis mva-poster**.  

4. Du validerer og klargjør rapporten for innsending ved å velge handlingen **Frigi**.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] validerer om rapporten er riktig definert. Hvis valideringen mislykkes, vises feilene under **Feil og advarsler**, slik at du vet hva du må løse. Vanligvis, hvis meldingen er om en manglende innstilling i [!INCLUDE[prod_short](includes/prod_short.md)], kan du klikke meldingen for å åpne siden som inneholder informasjon for å korrigere.  
5. Du sender inn rapporten ved å velge handlingen **Send**.  

Når du har sendt inn rapporten, overvåker [!INCLUDE[prod_short](includes/prod_short.md)] tjenesten og holder en oversikt over kommunikasjonen din. **Status**-feltet angir hvor rapporten er i prosessen. Når myndighetene behandler rapporten, endres for eksempel statusen til **Vellykket**. Hvis skattemyndigheten finner feil i rapporten du har sendt inn, blir statusen for rapporten **Mislyktes**. Du kan vise feilene under **Feil og advarsler**, rette dem og deretter sende inn rapporten på nytt. Hvis du vil se en oversikt over alle rapportene for EU-salg - oversikt, går du til siden **Rapporter for EU-salg - oversikt**.  

### <a name="vat-return-statuses"></a>Mva-returstatuser

Mva-returer kan ha forskjellige statuser, som beskrevet i tabellen nedenfor.

| Status | Beskrivelse |
|------------|-------------------------|
| Åpne | Når du oppretter en ny mva-retur. Du kan kjøre handlingen **Foreslå linjer**. Hvis du må korrigere verdier, kan du kjøre handlingen **Foreslå linjer** på nytt. Du kan ikke sende en mva-retur med denne statusen. |
| Frigitt | Statusen blir endret når du bruker handlingen **Frigi**. [!INCLUDE[prod_short](includes/prod_short.md)] viser hurtigfanen **Feil og advarsler**. Du kan ikke gjøre endringer eller bruke handlingen **Foreslå linjer**. Hvis du vil foreta endringer, må du åpne mva-returen på nytt. |
| Avvist | Hvis innsendingen ikke lyktes (for eksempel hvis godkjenningen mislyktes), endres statusen til **Avvist**. Du kan ikke åpne en mva-retur med denne statusen på nytt. |
| Sendt | Mva-returen sendes ved hjelp av handlingen **Send**, eller den er merket som sendt inn med **Merk som sendt**-handlingen. |
| Godtatt | Mva-meldingen har denne statusen hvis rapporten er merket som godkjent ved hjelp av handlingen **Merk som godkjent** . Hvis **mva-returrapporten** er merket som **Godkjent**, kan du kjøre handlingen **Beregn og bokfør mva-oppgjør**. |

## <a name="viewing-communications-with-your-tax-authority"></a>Vise kommunikasjon med skattemyndigheten

I enkelte land/områder utveksler du meldinger med skattemyndigheten når du sender inn rapporter. Du kan vise den første og siste meldingen du har sendt eller mottatt, ved å velge handlingene **Last ned sendingsmelding** og **Last ned svarmelding**.  

## <a name="submitting-vat-reports-manually"></a>Sende inn mva-rapporter manuelt
Hvis du bruker en annen metode til å sende inn rapporten, for eksempel ved å eksportere XML-filen og laste den opp til nettstedet til en skattemyndighet, kan du etterpå velge **Merk som Sendt** for å lukke rapporteringsperioden. Når du merker rapporten som frigitt, kan den ikke redigeres. Hvis du må endre rapporten etter at du har merket den som frigitt, må du åpne den på nytt.

## <a name="vat-settlement"></a>Mva-oppgjør
Du må jevnlig remittere netto mva til skattemyndighetene. Hvis du må gjøre opp mva ofte, kan du kjøre kjørselen **Beregn og bokfør mva-oppgjør** for å lukke åpne mva-poster og overføre inngående og utgående mva-beløp til kontoen for mva-oppgjør.

Når du overfører mva-beløp til oppgjørskontoen, krediteres kontoen for inngående mva., og kontoen for utgående mva. debiteres med beløpene som er beregnet for den angitte perioden. Nettobeløpet krediteres mva-oppgjørskontoen, eller debiteres hvis det inngående mva-beløpet er størst. Du kan bokføre oppgjøret umiddelbart eller skrive ut en testrapport først.  

> [!Note]
> Når du bruker kjørselen **Beregn og bokfør mva-oppgjør**, hvis du ikke angir en **Mva-bokføringsgruppe - firma** og en **Mva-bokføringsgruppe - vare**, inkluderes poster som har alle firma-og varebokføringsgrupper.

## <a name="configuring-your-own-vat-reports"></a>Konfigurere dine egne mva-rapporter

Du kan bruke standardrapporten **EU-salg – oversikt**. Du kan imidlertid også opprette dine egne rapporter hvis du har en utviklingslisens, slik at du kan opprette codeunit-er. Hvis du vil ha hjelp med dette, kan du kontakte en Microsoft-partner.  

Tabellen nedenfor beskriver kodeenhetene du må lage for rapporten.  

| Kodeenhet | Det den må gjøre |
|----|-----|
|Foreslå linjer| Hente informasjon fra tabellen **Mva-poster** og vise den på linjer i mva-rapporten.|
|Innhold | Styre formatet på rapporten, For eksempel om det er XML eller JSON. Formatet som skal brukes, er avhengig av kravene som gjelder i webtjenesten til skattemyndighetene. |
|Innsending | Styre hvordan og når du sender inn rapporten, basert på kravene til skattemyndigheten. |
|Svarbehandler | Håndtere returer fra skattemyndighetene. Den kan for eksempel sende en e-postmelding til kontaktpersonen i selskapet ditt. |
|Annuller | Sende en annullering av en mva-rapport ble sendt inn til skattemyndigheten tidligere. |  

> [!Note]
> Når du lager kodeenheter for rapporten, må du være oppmerksom på verdien i feltet **Versjon av mva-rapport**. Dette feltet må gjenspeile versjonen av rapporten som skattemyndigheten krever eller krevde. Du kan for eksempel angi **2021** i feltet for å angi at rapporten følger kravene som var gjeldende for dette året. For å finne nåværende versjon kontakter du skattemyndigheten.  

## <a name="see-also"></a>Se også

[Definere beregnings- og bokføringsmetoder for merverdiavgift](finance-setup-vat.md)    
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)    
[Sett opp salg](sales-setup-sales.md)    
[Fakturere salg](sales-how-invoice-sales.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
