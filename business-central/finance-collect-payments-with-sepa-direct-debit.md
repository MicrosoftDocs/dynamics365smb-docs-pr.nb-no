---
title: SEPA Direct Debit i Business Central
description: Med kundens samtykke kan du samle inn betaling direkte fra kundens bankkonto i henhold til SEPA-formatet.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.form: '371, 423, 424, 427, 1208, 1207, 1230'
ms.date: 07/17/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="collect-payments-with-sepa-direct-debit"></a>Innkreve betalinger med SEPA Direct Debit

Med kundens samtykke kan du samle inn betaling direkte fra kundens bankkonto i henhold til SEPA-formatet.  

Konfigurer først eksportformatet for bankfilen som instruerer banken om å utføre en direct debit. Konfigurer deretter kundens betalingsmåte. Til slutt angir du direct debit-belastningsfullmakten som gjenspeiler avtalen med kunden om å samle sine betalinger i en bestemt avtaleperiode.  

Hvis du vil instruere banken om å overføre beløpet fra kundens bankkonto til firmaets konto, kan du opprette en post for direct debit-samlingen som inneholder informasjon om bankkonti, berørte salgsfakturaer og direct debit-belastningsfullmakten. Deretter eksporterer du en XML-fil som er basert på samlingsposten, som du sender til banken for behandling. Betalinger som ikke kunne behandles, vil bli kommunisert til deg av banken din, og du må deretter manuelt avvise de aktuelle postene for direkte belastning.  

Du kan konfigurere standard kundesalgskoder med direct debit-betalingsmåten og belastningsfullmaktsinformasjonen. Du kan deretter bruke kjørselen **Opprett standard kundefakturaer** til å generere flere salgsfakturaer med forhåndsutfylt avtalegiroinformasjon. Dette kan gjøres manuelt eller automatisk, i henhold til forfallsdatoen for betalingen.  

Når betalingene er behandlet, som kommunisert av banken din, kan du bokføre betalingskvitteringene enten direkte fra **Direct Debit Collect. Poster-siden** eller ved å flytte betalingslinjene til kladden der du bokfører innbetalingen, for eksempel **siden Innbetalingskladder** . Du kan også, avhengig av kontantstyringsprosessen, vente og bare bruke bare betalinger som en del av bankkontoavstemmingen.  

> [!NOTE]  
> Hvis du vil innkreve betalinger ved hjelp av SEPA Direct Debit, må valutaen på salgsfakturaen være EURO.  

## <a name="how-to-set-up-sepa-direct-debit"></a>Slik konfigurerer du SEPA Direct Debit

Fra siden **Direct Debit-oppkrevinger** kan du eksportere instruksjoner til den elektroniske banken for å utføre en direct debit-oppkreving fra kundens bankkonto til din bankkonto i samsvar med SEPA Direct Debit-formatet.

> [!NOTE]
> Den globale versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] støtter bare SEPA direct debit-formatet. Versjonen for ditt land/område kan støtte andre formater for elektronisk betaling. Se under **Lokal funksjonalitet** i innholdsfortegnelsen.  

Hvis du vil aktivere eksport av et bankfilformat som ikke støttes som standard [!INCLUDE[prod_short](includes/prod_short.md)], kan du konfigurere en datautvekslingsdefinisjon ved hjelp av rammeverket for datautveksling. Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)  

Før du kan behandle kundebetalinger elektronisk ved å eksportere direct debit-instruksjoner i SEPA Direct Debit-formatet, må du utføre følgende konfigureringstrinn:  

* Konfigurer eksportformatet for bankfilen som instruerer banken om å utføre en direct debit-samling fra kundens bankkonto til din bankkonto.  
* Konfigurer kundens betalingsmåte.  
* Konfigurer direct debit-belastningsfullmakten som gjenspeiler avtalen med kunden om å samle sine betalinger i en bestemt avtaleperiode.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Slik konfigurerer du bankkontoen din for SEPA Direct Debit:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkontoer**, og velg deretter den relaterte koblingen.  
2. Åpne bankkontoen som du vil bruke til direct debit.  
3. Velg **alternativet for** SEPA Direct Debet Exp. Format i hurtigfanen **Generelt**, i feltet SEPA Direct Debit Exp..  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Slik definerer du kundens betalingsmåte for SEPA Direct Debit:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsmåter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Konfigurer betalingsmåter. Fyll ut de spesifikke feltene for direct\- debit som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Direct Debit**|Angi om betalingsmåten er for innsamling av SEPA Direct Debit.|  
    |**Betalingsbet.kode for Direct Debit**|Angi betalingsbetingelsene, for eksempel IKKE BETAL, som vises på salgsfakturaer som betales med SEPA Direct Debit, for å angi for kunden at betalingen vil bli samlet inn automatisk. Du kan også la feltet stå tomt.|  

    > [!NOTE]  
    >  Ikke angi en verdi i feltet **Motkontonr.**  

4. Velg **OK**-knappen for å lukke siden **Betalingsmåter**.  
5. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.  
6. Åpne kunde kort for kunden du vil definere for innsamling av SEPA Direct Debit.  
7. Velg feltet **Betalingsmåte - kode**, og velg deretter koden for betalingsmåte som du angav i trinn 3.  
8. Gjenta trinn 6 og 7 for alle kundene du vil definere for innsamling av SEPA Direct Debit.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Slik konfigurerer du direct debit-belastningsfullmakten som representerer kundeavtalen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.  
2. Åpne kort for kunden du vil definere for SEPA Direct Debit.  
3. Velg **Bankkonti**-handlingen.  
4. På siden Kundebankkontooversikt **Velg** du kundebankkontoen som skal bruke avtalegiro, og deretter velger du handlingen **Avtalegirofullmakter** fra **Ny**.  
5. På siden **SEPA Direct Debit-belastningsfullmakter** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Bankkontokode for kunde**|Angir bankkontoen som avtale\-girobetalinger kreves inn fra. Dette feltet fylles ut automatisk.|  
    |**Gyldig fra**|Angi datoen direct debit\-belastningsfullmakten gjelder fra.|  
    |**Gyldig til**|Angi datoen da direct debit\-belastningsfullmakten utløper.|  
    |**Signeringsdato**|Angi datoen da kunden signert direct debit\-belastningsfullmakten.|  
    |**Type betaling**|Angi om avtalen dekker flere (**Gjentakende**) eller én enkelt (**Engangsforekomst**) direct debit-samlinger.|  
    |**Forventet antall debetbeløp**|Angi hvor mange direct debit-samlinger vil opprette. Dette feltet er bare relevant hvis du valgte **Gjentakende** i feltet **Type betaling**.|  
    |**Debetteller**|Angir hvor mange direct debit-samlinger som er utført ved hjelp av denne direct debit\-belastningsfullmakten. Dette feltet oppdateres automatisk.|  
    |**Sperret**|Angi at avtalegiroinnkrevinger ikke kan utføres ved hjelp av denne avtalegirofullmakten\-.|  

6. Gjenta trinn 1 til og med 5 for alle kundene du vil definere for SEPA Direct Debit.  

 Direct debitbelastningsfullmakten fylles automatisk ut i feltet **ID for Direct Debit-belastningsfullmakt** når du oppretter en salgsfaktura for kunden som du valgte i trinn 2. Hvis du vil ha mer informasjon, kan du se [Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md).

## <a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Opprette poster for SEPA Direct Debit-oppkreving og eksportere til en bankfil

Hvis du vil instruere banken om å overføre beløpet fra kundens bankkonto til firmaets konto, kan du opprette en post for direct debit-samlingen som inneholder informasjon om kundens bankkonto, berørte salgsfakturaer og direct debit-belastningsfullmakten. Fra den resulterende posten for avtalegirosamlingen eksporterer du deretter en XML-fil som du sender eller laste opp til nettbanken for behandling. Eventuelle betalinger som ikke kunne behandles av banken, vil bli kommunisert til deg av banken din, og du må deretter manuelt avvise de aktuelle postene for direkte belastning.  

 > [!NOTE]  
 > Hvis du vil innkreve betalinger ved hjelp av SEPA Direct Debit, må valutaen på salgsfakturaen være EURO.  

### <a name="to-create-a-direct-debit-collection"></a>Slik oppretter du en avtalegirooppkreving

 1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Direct Debit-samlinger**, og velg deretter den relaterte koblingen.  
 2. På siden **Direct Debit-oppkrevinger** velger du handlingen **Opprett Direct Debit-oppkreving**.  
 3. På siden **Opprett Direct Debit-oppkreving** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Fra forfallsdato**|Angi den tidligste betalingsforfallsdatoen på salgsfakturaer som du vil opprette en avtalegirosamling for.|  
    |**Til forfallsdato**|Angi den siste betalingsforfallsdatoen på salgsfakturaer som du vil opprette en avtalegirosamling for.|  
    |**Partnertype**|Angi om avtalegirosamlingen opprettes for kundetypen **Firma** eller **Person**.|  
    |**Bare kunder med gyldig belastningsfullmakt**|Angi om en direct debit-samling opprettes for kunder som har en gyldig direct debit-belastningsfullmakt. **Merk:**  Det opprettes en avtalegirosamling selv om **feltet Avtalegiromandat-ID** ikke er fylt ut på salgsfakturaen.|  
    |**Bare fakturaer med gyldig belastningsfullmakt**|Angi om en Direct Debit-oppkreving bare blir opprettet for salgsfakturaer hvis en gyldig Direct Debit-belastningsfullmakt er valgt i feltet **ID for Direct Debit-belastningsfullmakt** på salgsfakturaen.|  
    |**Bankkontonr.**|Angi hvilke av firmaets bankkontoer som den samlede betalingen blir overført til fra kundens bankkonto.|  
    |**Bankkontonavn**|Angir navnet på bankkontoen som du velger i feltet **Bankkontonr.**. Dette feltet fylles ut automatisk.|  

 4. Velg **OK**.  

En avtalegirosamling legges til på siden **Direct Debit-oppkrevinger**, og én eller flere poster for avtalegirosamlingen blir opprettet.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Slik oppretter du en post for avtalegirosamling til en bankfil

 1. På siden **Direct Debit-oppkrevinger** velger du handlingen **Poster for Direct Debit-oppkreving**.  
 2. På siden **Poster for Direct Debit-oppkreving** merker du av for posten som du vil eksportere, og deretter velger du handlingen **Opprett direct debit-fil**.  
 3. Lagre den eksporterte filen på plasseringen der du sender eller laste den opp til nettbanken.  

      På siden **Poster for Direct Debit-oppkreving** endres feltet **Status for Direct Debit-oppkreving** til Fil opprettet. På siden **SEPA Direct Debit-belastningsfullmakter** oppdateres feltet **Debetteller** med én.  

 Hvis den eksporterte filen ikke kan behandles, for eksempel fordi kunden er insolvent, kan du avvise posten for direct debit-samlingen. Hvis den eksporterte filen er behandlet av banken, samles automatisk utestående betalinger for de aktuelle salgsfakturaene fra de aktuelle kundene. I slike tilfeller kan du lukke samlingen.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Slik avviser du poster for avtalegirosamlinger

* På **direkte belastning Collect. Poster-siden**, Velg posten som ikke ble behandlet, og velg deretter handlingen **Avvis post** .  

    Verdien i **Status**-feltet på siden **Poster for Direct Debit-oppkreving** endres til **Avvist**.  

### <a name="to-close-a-direct-debit-collection"></a>Slik lukker du en avtalegirosamling

* På siden **Poster for Direct Debit-oppkreving** merker du av for posten som ble behandlet, og deretter velger du handlingen **Lukk oppkreving**.  

    Den relaterte avtalegirosamlingen er lukket.  

 Du kan deretter fortsette å bokføre kvitteringer for betaling for de aktuelle salgsfakturaene. Dette kan du gjøre slik du vanligvis bokfører kvitteringer, for eksempel på siden **Betalingsregistrering**, eller du kan bokføre de relaterte kvitteringene direkte fra siden **Poster for Direct Debit-oppkreving** . Hvis du vil ha mer informasjon, kan du se [Innkreve betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).

## <a name="posting-sepa-direct-debit-payment-receipts"></a>Bokføre kvitteringer for SEPA Direct Debit

Når en direct debit-samling er behandlet av banken din, kan du fortsette med å bokføre mottak av betalingen for de aktuelle salgsfakturaene. Hvis du vil ha mer informasjon, kan du se [Opprette poster for SEPA Direct Debit-oppkreving og eksportere til en bankfil](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)  

Du kan bokføre kvittering direkte fra siden **Direct Debit\-oppkrevinger** eller siden **Poster for Direct Debit-oppkreving**. Du kan også overføre arbeidet til en annen bruker ved klargjøre de relaterte kladdelinjene.  

### <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Slik bokfører du en kvittering for direct debit fra siden Direct Debit-samlinger

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Direct Debit-samlinger**, og velg deretter den relaterte koblingen.  
2. Velg en linje for en direct debit-samling som er eksportert til en bankfil og behandlet av banken.
3. Velg handlingen **Bokfør kvitteringer**.  
4. På siden **Bokfør Direct Debit-oppkreving** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Direct Debit-oppkrevingsnr.**|Angi direct debit-samlingen du vil bokføre kvittering for.|  
    |**Finanskladdemal**|Angi hvilken finanskladdemal som skal brukes til bokføring av kvitteringen, for eksempel malen for innbetalinger.|  
    |**Finanskladdenavn**|Angi hvilken finanskladd som skal brukes til bokføring av kvitteringen.|  
    |**Opprett bare kladd**|Velg denne avmerkingsboksen hvis du ikke vil bokføre kvitteringen når du velger **OK**-knappen. Kvitteringen klargjøres i den angitte kladden og bokføres ikke før noen bokfører de aktuelle kladdelinjene.|  

5. Velg **OK**-knappen.

## <a name="see-also"></a>Se også

[Håndtere fordringer](receivables-manage-receivables.md)  
[Servicebehandling](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
