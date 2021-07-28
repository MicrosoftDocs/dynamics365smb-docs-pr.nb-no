---
title: SEPA Direct Debit i Business Central
description: Med kundens samtykke kan du samle inn betaling direkte fra kundens bankkonto i henhold til SEPA-formatet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: d39b30fbe625cd92b85bf8055673fa651242007e
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439513"
---
# <a name="collect-payments-with-sepa-direct-debit"></a>Innkreve betalinger med SEPA direct debit
Med kundens samtykke kan du samle inn betaling direkte fra kundens bankkonto i henhold til SEPA-formatet.  

 Konfigurer først eksportformatet for bankfilen som instruerer banken om å utføre en direct debit. Konfigurer deretter kundens betalingsmåte. Til slutt angir du direct debit-belastningsfullmakten som gjenspeiler avtalen med kunden om å samle sine betalinger i en bestemt avtaleperiode.  

 Hvis du vil instruere banken om å overføre beløpet fra kundens bankkonto til firmaets konto, kan du opprette en post for direct debit-samlingen som inneholder informasjon om bankkonti, berørte salgsfakturaer og direct debit-belastningsfullmakten. Deretter eksporterer du en XML-fil som er basert på samlingsposten, som du sender til banken for behandling. Eventuelle betalinger som ikke kunne behandles blir kommunisert til deg av banken din, og du må deretter manuelt avvise de aktuelle postene for direct debit-samlingen.  

 Du kan konfigurere standard kundesalgskoder med direct debit-betalingsmåten og belastningsfullmaktsinformasjonen. Du kan deretter bruke kjørselen **Opprett standard kundefakturaer** til å generere flere salgsfakturaer med forhåndsutfylt avtalegiroinformasjon. Dette kan gjøres manuelt eller automatisk, i henhold til forfallsdatoen for betalingen.  

 Når betalinger er behandlet, som formidlet av banken din, kan du bokføre kvitteringene direkte fra siden **Poster for Direct Debit-oppkreving** eller ved å flytte betalingslinjene i kladden der du bokfører kvitteringer, for eksempel siden **Innbetalingskladd**. Du kan også, avhengig av kontantstyringsprosessen, vente og bare bruke bare betalinger som en del av bankkontoavstemmingen.  

> [!NOTE]  
>  Hvis du vil innkreve betalinger ved hjelp av SEPA Direct Debit, må valutaen på salgsfakturaen være EURO.  

## <a name="setting-up-sepa-direct-debit"></a>Definere SEPA Direct Debit
Fra siden **Direct Debit-oppkrevinger** kan du eksportere instruksjoner til den elektroniske banken for å utføre en direct debit-oppkreving fra kundens bankkonto til din bankkonto i samsvar med SEPA Direct Debit-formatet.

> [!NOTE]
> Den globale versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] støtter bare SEPA direct debit-formatet. Versjonen for ditt land/område kan støtte andre formater for elektronisk betaling. Se under **Lokal funksjonalitet** i innholdsfortegnelsen.  

Du kan gjøre det mulig å eksportere et bankfilformat som ikke støttes som standard i [!INCLUDE[prod_short](includes/prod_short.md)], ved å definere en datautvekslingsdefinisjon ved hjelp av rammeverket for datautveksling. Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)  

Før du kan behandle kundebetalinger elektronisk ved å eksportere direct debit-instruksjoner i SEPA Direct Debit-formatet, må du utføre følgende konfigureringstrinn:  

* Konfigurer eksportformatet for bankfilen som instruerer banken om å utføre en direct debit-samling fra kundens bankkonto til din bankkonto.  
* Konfigurer kundens betalingsmåte.  
* Konfigurer direct debit-belastningsfullmakten som gjenspeiler avtalen med kunden om å samle sine betalinger i en bestemt avtaleperiode.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Slik konfigurerer du din bankkonto for SEPA direct debit  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkonti**, og velg deretter den relaterte koblingen.  
2. Åpne bankkontoen som du vil bruke til direct debit.  
3. Velg alternativet for SEPA direct debit i feltet **Eksportformat for SEPA Direct Debit** i hurtigfanen **Overfør**.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Slik konfigurerer du kundens betalingsmåte for SEPA direct debit  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsmåter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Konfigurer betalingsmåter. Fyll ut de spesifikke feltene for direct\- debit som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Direct Debit**|Angi om betalingsmåten er for SEPA direct debit-samlinger.|  
    |**Betalingsbet.kode for Direct Debit**|Angi betalingsbetingelsene, for eksempel IKKE BETAL, som vises på salgsfakturaer som betales med SEPA direct debit, for å angi for kunden at betalingen blir innkrevd automatisk. Du kan også la feltet stå tomt.|  

    > [!NOTE]  
    >  Ikke angi en verdi i feltet **Motkontonr.**  

4. Velg **OK**-knappen for å lukke siden **Betalingsmåter**.  
5. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.  
6. Åpne kundekortet for kunden som du vil konfigurere SEPA direct debit-samling for.  
7. Velg feltet **Betalingsmåte - kode**, og velg deretter koden for betalingsmåte som du angav i trinn 3.  
8. Gjenta trinn 6 og 7 for alle kundene du vil konfigurere SEPA direct debit-samling for.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Slik konfigurerer du direct debit-belastningsfullmakten som representerer kundeavtalen  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.  
2. Åpne kortet for kunden som du vil konfigurere SEPA direct debit for.  
3. Velg **Bankkonti**-handlingen.  
4. På siden **Kundebankkonto - oversikt** velger du kundebankkonto som skal bruke direct debit, og deretter velger du handlingen **Direct Debit-belastningsfullmakter**.  
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
    |**Sperret**|Angi om direct debit-samlinger ikke kan opprettes ved hjelp av denne direct debit\-belastningsfullmakten.|  

6.  Gjenta trinn 1 til 5 for alle kundene du vil konfigurere SEPA direct debit for.  

 Direct debitbelastningsfullmakten fylles automatisk ut i feltet **ID for Direct Debit-belastningsfullmakt** når du oppretter en salgsfaktura for kunden som du valgte i trinn 2. Hvis du vil ha mer informasjon, kan du se [Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md).

## <a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Opprette poster for SEPA Direct Debit-oppkreving og eksportere til en bankfil
 Hvis du vil instruere banken om å overføre beløpet fra kundens bankkonto til firmaets konto, kan du opprette en post for direct debit-samlingen som inneholder informasjon om kundens bankkonto, berørte salgsfakturaer og direct debit-belastningsfullmakten. Fra den resulterende posten for avtalegirosamlingen eksporterer du deretter en XML-fil som du sender eller laste opp til nettbanken for behandling. Eventuelle betalinger som ikke kunne behandles av banken blir kommunisert til deg av banken din, og du må deretter manuelt avvise de aktuelle postene for direct debit-samlingen.  

 > [!NOTE]  
 >  Hvis du vil innkreve betalinger ved hjelp av SEPA Direct Debit, må valutaen på salgsfakturaen være EURO.  

### <a name="to-create-a-direct-debit-collection"></a>Slik oppretter du en avtalegirooppkreving  

 1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Direct Debit-samlinger**, og velg deretter den relaterte koblingen.  
 2. På siden **Direct Debit-oppkrevinger** velger du handlingen **Opprett Direct Debit-oppkreving**.  
 3. På siden **Opprett Direct Debit-oppkreving** fyller du ut feltene som beskrevet i tabellen nedenfor.  

     |Felt|Beskrivelse|  
     |---------------------------------|---------------------------------------|  
     |**Fra forfallsdato**|Angi den tidligste betalingsforfallsdatoen på salgsfakturaer som du vil opprette en avtalegirosamling for.|  
     |**Til forfallsdato**|Angi den siste betalingsforfallsdatoen på salgsfakturaer som du vil opprette en avtalegirosamling for.|  
     |**Partnertype**|Angi om avtalegirosamlingen opprettes for kundetypen **Firma** eller **Person**.|  
     |**Bare kunder med gyldig belastningsfullmakt**|Angi om en direct debit-samling opprettes for kunder som har en gyldig direct debit-belastningsfullmakt. **Obs!:**  Det blir opprettet en avtalegirosamling selv om feltet **ID for Direct Debit-belastningsfullmakt** ikke er fylt ut på salgsfakturaen.|  
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

 Hvis den eksporterte filen ikke kan behandles, for eksempel fordi kunden er insolvent, kan du avvise posten for avtalegirosamlingen. Hvis den eksporterte filen er behandlet av banken, samles automatisk utestående betalinger for de aktuelle salgsfakturaene fra de aktuelle kundene. I slike tilfeller kan du lukke samlingen.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Slik avviser du poster for avtalegirosamlinger  

 * På siden **Poster for Direct Debit-oppkreving** merker du av for posten som ikke ble behandlet, og deretter velger du handlingen **Avvis post**.  

      Verdien i **Status**-feltet på siden **Poster for Direct Debit-oppkreving** endres til **Avvist**.  

### <a name="to-close-a-direct-debit-collection"></a>Slik lukker du en avtalegirosamling  
 *  På siden **Poster for Direct Debit-oppkreving** merker du av for posten som ble behandlet, og deretter velger du handlingen **Lukk oppkreving**.  

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
     |**Opprett bare kladd**|Merk av for dette alternativet hvis du ikke vil bokføre kvitteringen når du velger **OK**. Kvitteringen blir klargjort i den angitte kladden, og blir ikke bokført før noen bokfører de aktuelle kladdelinjene.|  

 5. Velg **OK**-knappen.

## <a name="see-also"></a>Se også  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Servicebehandling](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]