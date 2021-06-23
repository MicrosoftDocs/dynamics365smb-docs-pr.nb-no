---
title: 'Gjennomgang: konfigurere og fakturere salgsforskudd'
description: Forskuddsbetalinger er betalinger som faktureres og bokføres i en salgs- eller kjøpsforskuddsordre før endelig fakturering. Du krever kanskje et depositum før du produserer varer på bestilling, eller kanskje du krever betaling før du leverer varer til en kunde. Du bruker funksjonene for forskuddsbetaling i Business Central til å fakturere og kreve inn innskudd som kreves fra kunder, eller remittere innskudd til leverandører. Dermed kan du sørge for at alle betalinger bokføres mot en faktura.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/25/2021
ms.author: edupont
ms.openlocfilehash: dacf9e5492f583513e69f2316a0440fce2597269
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216183"
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Gjennomgang: konfigurere og fakturere salgsforskudd

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Forskuddsbetalinger er betalinger som faktureres og bokføres i en salgs- eller kjøpsforskuddsordre før endelig fakturering. Du krever kanskje et depositum før du produserer varer på bestilling, eller kanskje du krever betaling før du leverer varer til en kunde. Du bruker funksjonene for forskuddsbetaling i [!INCLUDE[prod_short](includes/prod_short.md)] til å fakturere og kreve inn innskudd som kreves fra kunder, eller remittere innskudd til leverandører. Dermed kan du sørge for at alle betalinger bokføres mot en faktura.  

Krav til forskuddsbetaling kan defineres for en kunde eller leverandør for alle varer eller utvalgte varer. Når du har fullført det nødvendige oppsettet, kan du generere forskuddsfakturaer fra ordrer og bestillinger for det beregnede forskuddsbeløpet. Du kan endre standardbeløpene på fakturaen etter behov. Du kan for eksempel sende flere forskuddsfakturaer hvis flere varer blir lagt til i ordren.  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen  

Denne gjennomgangen leder deg gjennom følgende scenarier:  

-  Konfigurere forskuddsbetalinger  
-  Opprette en ordre der det kreves et forskudd  
-  Opprette en forskuddsfaktura  
-  Korrigere forskuddskravene i en ordre  
-  Utligne forskuddsbetalinger mot en ordre  
-  Fakturere det endelige beløpet i en ordre med forskudd  

### <a name="roles"></a>Roller

Denne gjennomgangen omfatter oppgaver for følgende roller:  

-  Regnskapssjef (Jenny)  
-  Ordrebehandler (Heidi)  
-  Kundeansvarlig (Magnus)  

## <a name="story"></a>Hovedscenario

 Jenny er regnskapssjef. Hun gjør beslutninger om hvilke kunder som må betale depositum før varer produseres eller leveres. Jenny konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] til å beregne forskuddsbetalinger automatisk.  

 Heidi er en ordrebehandler. Når en kunde ringer for å bestille, registrerer hun ordren i systemet mens er kunden på telefonen. På denne måten kan hun kontrollere priser og betalingsbetingelser med kunden umiddelbart, og hun kan foreta justeringer i ordren mens hun forhandler med kunden.  

 Magnus arbeider i regnskapsavdelingen, der han bokfører fakturaer og betalinger.  

 I dette scenariet definerer Jenny forskuddskrav for kunden Møbelhandleren A/S basert på kreditthistorikken deres, og hun gir Heidi instruksjoner om hvordan ordrene deres skal håndteres.  

 Når kunden ringer, forhandler Heidi med kunden til de kommer frem til en avtale. Hun kan deretter velge å beregne forskuddsbetalingen på flere forskjellige måter.  

 Etter at Heidi har sendt forskuddsfakturaen, bestiller kunden en ekstra vare. Heidi oppdaterer ordren og oppretter en ekstra forskuddsfaktura.  

 Magnus registrerer kundens betaling og utligner den mot fakturaene, og deretter sender han den endelige fakturaen.  

## <a name="setting-up-prepayments"></a>Konfigurere forskuddsbetalinger

Jenny konfigurerer systemet slik at det kan håndtere forskuddsbetalinger for kunder.  

-  Jenny bestemmer seg for å bruke samme nummerserie for forskuddsbetalinger som den som brukes for salgsfakturering.  
-  Jenny angir at programmet skal kontrollere om forskuddsbetalinger kreves før endelig fakturering i en ordre.  
-  Jenny definerer standardverdier for en obligatorisk forskuddsprosent for bestemte varer og kunder.  

Følgende fremgangsmåte beskriver hvordan du fullfører oppgavene til Jenny:  

#### <a name="to-set-up-number-series-for-prepayments"></a>Slik definerer du en nummerserie for forskuddsbetalinger:

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.  
2.  Vis hurtigfanen **Nummerserier** på **Salgsoppsett**-siden.  
3.  Kontroller at nummerserien for bokførte forskuddsfakturaer i feltet **Bokførte fakturanumre for forskudd** er den samme som for bokførte salgsfakturaer (**Bokførte fakturanr.**), og at nummerserien for bokførte kreditnotaer for forskudd (**Bokførte kreditnotanumre for forskudd**) er den samme som for bokførte kreditnotaer (**Bokførte kreditnotanr.**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Slik sperrer du leveringer ved ubetalt forskudd

1.  Merk av for **Kontroller forskudd ved bokføring** på hurtigfanen **Generelt** på siden **Salgsoppsett**.

Nå kan du ikke levere eller fakturere en ordre som har ubetalte forskuddsbeløp.  

Jenny krever at kunde 20000 som standard faktureres for et avdrag på 30 % i alle ordrer. Derfor angir hun en standard forskuddsprosent på kundekortet.  

Jenny krever at alle kunder faktureres for et depositum på 20 % for vare 1896-S. Kunde 20000 har en dårlig betalingshistorikk. Derfor krever hun en 40 % forskuddsbetaling fra kunde 20000 for vare 1896-S. Fremgangsmåten nedenfor viser hvordan du konfigurerer standard forskuddsprosent.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Slik tilordner du standard forskuddsprosenter til kunder og varer:

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.  
2.  Åpne kortet for kunde 20000 (Trey Research).
3.  Angi **30** i feltet **Forskuddsprosent**.  
4.  Velg **Relatert**, og velg deretter **Salg** og deretter **Forskuddsprosenter**
5.  Fyll ut to linjer på siden **Forskuddsprosenter for salg** på følgende måte:  

    |**Salgstype**|**Salgskode**|**Varenr.**|**Forskuddsprosent**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Kunde**|**20000**|**1896-S**|**40**|  
    |**Alle kunder**| |**1896-S**|**20**|  

    > [!IMPORTANT]  
    >  Alt etter land/område må du også angi en mva-gruppekode på hurtigfanen **Fakturering** for vare 1896-S.  

6.  Lukk alle sider.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Slik angir du en konto for salgsforskudd i generelt bokføringsoppsett:

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Generelt bokføringsoppsett**, og velg deretter den relaterte koblingen.  
2.  Velg linjen hvor feltet **Bokføringsgruppe – firma** er satt til **INNLAND**, og feltet **Bokføringsgruppe – vare** er satt til **DETALJ**.  
3.  Angi den relevante kontoen i feltet **Konto for salgsforskudd**. Valget lagres automatisk.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Opprette en ordre der det kreves et forskudd

 I det følgende scenariet oppretter ordrebehandleren Heidi en ordre mens hun snakker med en kunde. Varene som kunden bestiller, krever et forskudd, og kunden har tidligere vært sen med betalingen enkelte ganger. Heidi har derfor blitt bedt om å kreve et fast beløp på **800** som en forskuddsbetaling på ordren.  

Kunden ber om å kunne få betale 35 %, og Susanne samtykker. Derfor endrer hun rekkefølgen.  

Heidi oppretter forskuddsfakturaen og sender den til kunden.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Slik oppretter du en ordre med et forskudd:

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  For **Kundenr.** -feltet, velger du **20000**.  
4.  Lukk advarselen om forfalt saldo som vises.  
5.  Fyll ut to salgslinjer med følgende informasjon.  

    |**Type**|**Nr.**|**Antall**|  
    |--------------|-------------|------------------|  
    |**Vare**|**1896-S**|**1**|  
    |**Vare**|**1900-S**|**1**|

    Som standard er forskuddsfeltene på salgslinjen skjult, så du må vise dem. Du må tilpasse siden for å gjøre dette. Hvis du vil ha mer informasjon, kan du se [Slik tilpasser du en side med Tilpasse-banneret](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6.  Kontroller at feltet **Forskuddsprosent** på linjen med vare **1900-S** inneholder **30**. Standardverdien ble tatt fra salgshodet, som ble fylt ut fra kundekortet.  

    Feltet **Forskuddsprosent** på linjen med vare **1896-S** inneholder **40**. Dette er prosentsatsen du registrerte på siden **Forskuddsprosenter for salg** for vare **1896-S** og kunde **20000**.  

    Hvis du vil ha mer informasjon, kan du se [Definere forskudd](finance-set-up-prepayments.md).  
7.  Velg **Statistikk** i handlingen **Rekkefølge**.  
8.  På hurtigfanen **Forskuddsbetaling** inneholder feltet **Linjebeløp for forskudd eks. mva.** **458.16**. Hvis du oppretter en forskuddsfaktura for ordren nå, er dette beløpet som vises på fakturaen.  

    I dette scenariet har Heidi fått beskjed om å foreslå et totalt forskudd på **800** for ordren.  

    > [!IMPORTANT]  
    >  Følgende trinn gjelder kanskje ikke avhengig av land/område.  
9.  Endre beløpet i feltet **Linjebeløp for forskudd eks. mva.** til **800**, og lukk deretter siden.  
10.  Når du kontroller feltet **Forskuddsprosent** på salgslinjene, ser du at den har blitt beregnet på nytt til **67,02438** og **67,02282**.  

     Den nye beregningen tar med alle linjene med en forskuddsprosent som er større enn 0.  

     Nå spør kunden om forskuddsprosenten kan settes til 35 %. Heidis arbeidsleder godkjenner endringen.
11.  Angi **35** i **Forskuddsprosent**-feltet på siden **Ordre** på hurtigfanen **Forskudd**.  
12.  Klikk **Ja** i advarselen som vises. En sats på 35 % vil bli brukt som betalingsprosent for hele ordren.  
13.  Kontroller at linjene har blitt oppdatert i samsvar med dette.  

## <a name="creating-a-prepayment-invoice"></a>Opprette en forskuddsfaktura  
Etter at Heidi har registrert de riktige forskuddsverdiene i ordren, oppretter hun forskuddsfakturaen og sender den til kunden.  

#### <a name="to-create-a-prepayment-invoice"></a>Slik oppretter du en forskuddsfaktura:

1.  På siden **Ordre** velger du **Handlinger**, **Bokføring**, **Forskudd** og velger deretter **Bokfør og skriv ut forskuddsfaktura**
2.  Velg **Ja**-knappen for å bokføre fakturaen.  

> [!NOTE]  
>  Heidi ville ha valgt **Bokfør og skriv ut forskuddsfaktura** og sendt fakturaen til kunden via e-post.  

## <a name="creating-an-additional-prepayment-invoice"></a>Opprette en ekstra forskuddsfaktura

Neste dag ringer kunden Heidi og endrer ordren. Kunden vil ha to av vare 1100. Heidi åpner ordren på nytt og oppdaterer den, og deretter oppretter hun en ekstra forskuddsfaktura i ordren og sender den til kunden.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Slik oppretter du en ekstra forskuddsfaktura:

1.  På siden **Ordre** velger du handlingen **Frigi** og deretter **Åpne på nytt**.  
2.  Angi **2** i **Antall**-feltet på linjen for vare **1896-S**.  

    Velg **Statistikk** i handlingen **Rekkefølge**. Feltet **Linjebeløp for forskudd eks. mva** inneholder nå **768.04**, og feltet **Fakturert forskuddsbeløp eks. mva.** inneholder **417.76**. Dette viser at det er et ytterligere forskuddsbetalingsbeløp som ennå ikke er fakturert.  
3.  Hvis du vil bokføre en faktura for det ekstra forskuddsbetalingsbeløpet, velger du **Handlinger**, **Bokføring**, **Forskudd** og velger deretter **Bokfør og skriv ut forskuddsfaktura**
4.  Velg **Ja**-knappen for å bokføre fakturaen.  

## <a name="applying-the-prepayments"></a>Utligne forskuddsbetalingene  
Kunden betaler forskuddsbeløpet, og Magnus, som arbeider i regnskapsavdelingen, registrerer betalingen og utligner den mot forskuddsfakturaene.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Slik utligner du en betaling mot forskuddsfakturaene:

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Innbetalingskladder**, og velg deretter den relaterte koblingen.  
2.  Fyll ut en kladdelinje med følgende informasjon.  

    |Feltnavn|Angi|  
    |----------------|-----------|  
    |**Bilagstype**|**Betaling**|  
    |**Kontotype**|**Kunde**|  
    |**Kontonr.**|**20000**|  
3.  Velg handlingen **Behandle** og deretter **Utlign poster**.  
4.  Velg den første forskuddsfakturaen på siden **Utlign kundeposter**, og velg deretter handlingen **Behandle** og **Angi utlignings-ID**.  
5.  Gjenta forrige trinn for den andre forskuddsbetalingen.  
6.  Velg **OK**-knappen.  

    Beløpsfeltet er nå fylt ut med summen av de to forskuddsfakturaene.  

7.  Hvis du vil bokføre kladden, velger du handlingen **Bokfør / skriv ut** og velger **Bokfør**.
8.  Velg **Ja**-knappen.

## <a name="invoicing-the-remaining-amount"></a>Fakturere restbeløpet

Magnus har nå fått beskjed om at varene i ordren er levert, og at ordren er klar til fakturering. Magnus oppretter en faktura for ordren.  

#### <a name="to-invoice-the-remaining-amount"></a>Slik fakturerer du restbeløpet:

1.  Åpne ordren.
2.  Velg handlingen **Bokføring** og **Bokfør**.
3.  Velg **Lever og fakturer** og deretter **OK**-knappen.
4.  Hvis du vil forhåndsvise fakturaen , velger du **Ja**-knappen.

> [!NOTE]  
>  Vanligvis ville transportavdelingen allerede ha bokført leveringen.  

Arnie kan vise historikken for å bekrefte at salgsfakturaen ble opprettet som tiltenkt.

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  

## <a name="next-steps"></a>Neste trinn

Denne gjennomgangen har ledet deg gjennom trinnene for å konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] slik at du kan håndtere forskuddsbetalinger i det. Du har konfigurert standard forskuddsprosenter for kunder og varer, og du har også brukt flere ulike metoder til å beregne forskuddsbetalingene i en ordre. Du har prøvd å tilordne ett totalt forskuddsbeløp i ordren, og du har fått beregnet forskuddsbeløpet som en prosentsats for hele ordren.  

Du har også bokført en forskuddsfaktura, opprettet en ekstra forskuddsfaktura når ordren har blitt endret, og bokført den endelige fakturaen for restbeløpet.  

Med funksjonene for forskuddsbetaling i [!INCLUDE[prod_short](includes/prod_short.md)] blir det enkelt å konfigurere og håndheve forskuddsregler for kunder og varer, og du kan bokføre hver betaling mot en faktura.  

## <a name="see-also"></a>Se også  
[Fakturere forskuddsbetalinger](finance-invoice-prepayments.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
