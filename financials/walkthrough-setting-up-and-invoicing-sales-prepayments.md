---
title: "Gjennomgang – konfigurere og fakturere salgsforskudd | Microsoft-dokumentasjon"
description: "Forskuddsbetalinger er betalinger som faktureres og bokføres i en salgs- eller kjøpsforskuddsordre før endelig fakturering. Du krever kanskje et depositum før du produserer varer på bestilling, eller kanskje du krever betaling før du leverer varer til en kunde. Du bruker funksjonene for forskuddsbetaling i Finance and Operations, Business edition til å fakturere og kreve inn innskudd som kreves fra kunder, eller remittere innskudd til leverandører. Dermed kan du sørge for at alle betalinger bokføres mot en faktura."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cd74d543168f1f96f55141aace571d6d701e3de1
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Gjennomgang: konfigurere og fakturere salgsforskudd
Forskuddsbetalinger er betalinger som faktureres og bokføres i en salgs- eller kjøpsforskuddsordre før endelig fakturering. Du krever kanskje et depositum før du produserer varer på bestilling, eller kanskje du krever betaling før du leverer varer til en kunde. Du bruker funksjonene for forskuddsbetaling i [!INCLUDE[d365fin](includes/d365fin_md.md)] til å fakturere og kreve inn innskudd som kreves fra kunder, eller remittere innskudd til leverandører. Dermed kan du sørge for at alle betalinger bokføres mot en faktura.  

 Krav til forskuddsbetaling kan defineres for en kunde eller leverandør for alle varer eller utvalgte varer. Når du har fullført det nødvendige oppsettet, kan du generere forskuddsfakturaer fra ordrer og bestillinger for det beregnede forskuddsbeløpet. Du kan endre standardbeløpene på fakturaen etter behov. Du kan for eksempel sende flere forskuddsfakturaer hvis flere varer blir lagt til i ordren.  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen  
 Denne gjennomgangen leder deg gjennom følgende scenarier:  

-   Konfigurere forskuddsbetalinger  
-   Opprette en ordre der det kreves et forskudd  
-   Opprette en forskuddsfaktura  
-   Korrigere forskuddskravene i en ordre  
-   Utligne forskuddsbetalinger mot en ordre  
-   Fakturere det endelige beløpet i en ordre med forskudd  

### <a name="roles"></a>Roller  
 Denne gjennomgangen omfatter oppgaver for følgende roller:  

-   Regnskapssjef (Jenny)  
-   Ordrebehandler (Heidi)  
-   Kundeansvarlig (Magnus)  

## <a name="story"></a>Hovedscenario  
 Jenny er regnskapssjef. Hun gjør beslutninger om hvilke kunder som må betale depositum før varer produseres eller leveres. Jenny konfigurerer [!INCLUDE[d365fin](includes/d365fin_md.md)] til å beregne forskuddsbetalinger automatisk.  

 Heidi er en ordrebehandler. Når en kunde ringer for å bestille, registrerer hun ordren i systemet mens er kunden på telefonen. På denne måten kan hun kontrollere priser og betalingsbetingelser med kunden umiddelbart, og hun kan foreta justeringer i ordren mens hun forhandler med kunden.  

 Magnus arbeider i regnskapsavdelingen, der han bokfører fakturaer og betalinger.  

 I dette scenariet definerer Jenny forskuddskrav for kunden Møbelhandleren A/S basert på kreditthistorikken deres, og hun gir Heidi instruksjoner om hvordan ordrene deres skal håndteres.  

 Når kunden ringer, forhandler Heidi med kunden til de kommer frem til en avtale. Hun kan deretter velge å beregne forskuddsbetalingen på flere forskjellige måter.  

 Etter at Heidi har sendt forskuddsfakturaen, bestiller kunden en ekstra vare. Heidi oppdaterer ordren og oppretter en ekstra forskuddsfaktura.  

 Magnus registrerer kundens betaling og utligner den mot fakturaene, og deretter sender han den endelige fakturaen.  

## <a name="setting-up-prepayments"></a>Konfigurere forskuddsbetalinger  
 Jenny konfigurerer systemet slik at det kan håndtere forskuddsbetalinger for kunder.  

-   Jenny bestemmer seg for å bruke samme nummerserie for forskuddsbetalinger som den som brukes for salgsfakturering.  
-   Jenny angir at programmet skal kontrollere om forskuddsbetalinger kreves før endelig fakturering i en ordre.  
-   Jenny definerer standardverdier for en obligatorisk forskuddsprosent for bestemte varer og kunder.  

Følgende fremgangsmåte beskriver hvordan du fullfører oppgavene til Jenny:  

#### <a name="to-set-up-number-series-for-prepayments"></a>Slik definerer du en nummerserie for forskuddsbetalinger:  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.  
2.  Vis hurtigfanen **Nummerering** i **Salgsoppsett**-vinduet.  
3.  Kontroller at nummerserien for bokførte forskuddsfakturaer i feltet **Bokførte fakturanumre for forskudd** er den samme som for bokførte salgsfakturaer (**Bokførte fakturanr.**), og at nummerserien for bokførte kreditnotaer for forskudd (**Bokførte kreditnotanumre for forskudd**) er den samme som for bokførte kreditnotaer (**Bokførte kreditnotanr.**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Slik sperrer du leveringer ved ubetalt forskudd  
1.  Merk av for **Kontroller forskudd ved bokføring** på hurtigfanen **Generelt** i **Salgsoppsett**-vinduet.

    Nå kan du ikke levere eller fakturere en ordre som har ubetalte forskuddsbeløp.  

Jenny krever at kunde 20000 som standard faktureres for et avdrag på 30 % i alle ordrer. Derfor angir hun en standard forskuddsprosent på kundekortet.  

Jenny krever at alle kunder faktureres for et depositum på 20&#160;% for vare 1100. Kunde 20000 har en dårlig betalingshistorikk. Derfor krever hun en 40 % forskuddsbetaling fra kunde 20000 for vare 1100. Fremgangsmåten nedenfor viser hvordan du konfigurerer standard forskuddsprosent.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Slik tilordner du standard forskuddsprosenter til kunder og varer:  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kunder**, og velg deretter den relaterte koblingen.  
2.  Åpne kortet for kunde 20000 (Møbelhandleren).
3.  Skriv inn **30** i feltet **Forskuddsprosent**.  
4.  Velg **OK**-knappen for å lukke kundekortet.  
5.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.  
6.  Åpne kortet for kunde 1100.
7.  Velg handlingen **Forskuddsprosenter for salg**.  
8.  Fyll ut to linjer i vinduet **Forskuddsprosenter for salg** på følgende måte.  

    |**Salgstype**|**Salgskode**|**Varenr.**|**Forskuddsprosent**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Kunde**|**20000**|**1100**|**40**|  
    |**Alle kunder**||**1100**|**20**|  

    > [!IMPORTANT]  
    >  Alt etter land/område må du også angi en mva-gruppekode på hurtigfanen **Fakturering** for varene 1000 og 1100.  

9. Lukk alle vinduer.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Slik angir du en konto for salgsforskudd i generelt bokføringsoppsett:  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Generelt bokføringsoppsett**, og velg deretter den relaterte koblingen.  
2.  Velg linjen hvor feltet **Bokføringsgruppe - firma** er satt til **EKSPORT**, og feltet **Bokføringsgruppe - vare** er satt til **DETALJ**, og velg deretter **Rediger**-handlingen.  
3.  Angi den relevante kontoen i feltet **Konto for salgsforskudd** i vinduet **Generelt bokføringsoppsettskort**.  
4.  Velg **OK**-knappen.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Opprette en ordre der det kreves et forskudd  
 I det følgende scenariet oppretter ordrebehandleren Heidi en ordre mens hun snakker med en kunde. Varene som kunden bestiller, krever et forskudd, og kunden har tidligere vært sen med betalingen enkelte ganger. Heidi har derfor blitt bedt om å kreve et fast beløp på 2000 som en forskuddsbetaling på ordren.  

Kunden ber om å kunne få betale 35 %, og Susanne samtykker. Derfor endrer hun rekkefølgen.  

Heidi oppretter forskuddsfakturaen og sender den til kunden.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Slik oppretter du en ordre med et forskudd:  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  I feltet **Salg til-kundenr.** -feltet, velger du **20000**.  
5.  Godta advarselen om forfalt saldo som vises.  
6.  Fyll ut to salgslinjer med følgende informasjon.  

    |**Type**|**Nr.**|**Antall**|  
    |--------------|-------------|------------------|  
    |**Vare**|**1000**|**1**|  
    |**Vare**|**1100**|**1**|

    Som standard er forskuddsfeltene på salgslinjen skjult, så du må vise dem.  

7. Kontroller at feltet **Forskuddsprosent** på linjen med vare **1000** inneholder **30**. Standardverdien ble tatt fra salgshodet, som ble fylt ut fra kundekortet.  

    Feltet **Forskuddsprosent** på linjen med vare **1100** inneholder **40**. Dette er prosentsatsen du registrerte i vinduet **Forskuddsprosenter for salg** for vare **1100** og kunde **20000**.  

    Hvis du vil ha mer informasjon, kan du se [Definere forskudd](finance-set-up-prepayments.md).  
8. Velg handlingen **Statistikk**.  
9. På hurtigfanen **Forskuddsbetaling** inneholder feltet **Linjebeløp for forskudd eks. mva.** **1,560**. Hvis du oppretter en forskuddsfaktura for ordren nå, er dette beløpet som vises på fakturaen.  

    I dette scenariet har Heidi fått beskjed om å foreslå et totalt forskudd på 2&#160;000 for ordren.  

    > [!IMPORTANT]  
    >  Følgende trinn gjelder kanskje ikke avhengig av land/område.  
10. Endre beløpet i feltet **Linjebeløp for forskudd eks. mva** til **2000**, og lukk deretter vinduet.  
11. Når du kontroller feltet **Forskuddsprosent** på salgslinjene, ser du at den har blitt beregnet på nytt til **40,81625**.  

    Den nye beregningen tar med alle linjene med en forskuddsprosent som er større enn 0.  

    Nå spør kunden om forskuddsprosenten kan settes til 35 %. Heidis arbeidsleder godkjenner endringen.  

12. Angi **35** i **Forskuddsprosent**-feltet i **Ordre**-vinduet.  
13. Klikk **Ja** i advarselen som vises. En sats på 35 % vil bli brukt som betalingsprosent for hele ordren.  
14. Kontroller at linjene har blitt oppdatert i samsvar med dette.  

## <a name="creating-a-prepayment-invoice"></a>Opprette en forskuddsfaktura  
Etter at Heidi har registrert de riktige forskuddsverdiene i ordren, oppretter hun forskuddsfakturaen og sender den til kunden.  

#### <a name="to-create-a-prepayment-invoice"></a>Slik oppretter du en forskuddsfaktura:  

1.  I vinduet **Ordre** velger du handlingen **Bokfør forskuddsfaktura**.  

> [!NOTE]  
>  Heidi ville ha valgt **Bokfør og skriv ut forskuddsfaktura** og sendt fakturaen til kunden via e-post.  

## <a name="creating-an-additional-prepayment-invoice"></a>Opprette en ekstra forskuddsfaktura  
Neste dag ringer kunden Heidi og endrer ordren. Kunden vil ha to av vare 1100. Heidi åpner ordren på nytt og oppdaterer den, og deretter oppretter hun en ekstra forskuddsfaktura i ordren og sender den til kunden.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Slik oppretter du en ekstra forskuddsfaktura:  

1.  I vinduet **Ordre** velger du handlingen **Åpne på nytt**.  
2.  Angi **2** i **Antall**-feltet på linjen for vare **1100**.  

    Rull for å se forskuddsfeltene. Feltet **Linjebeløp for forskudd eks. mva** inneholder nå **630**, og feltet **Fakturert forskuddsbeløp eks. mva.** inneholder **315**. Dette viser at det er et ytterligere forskuddsbetalingsbeløp som ennå ikke er fakturert.  
3.  Hvis du vil bokføre en faktura for det ekstra forskuddsbetalingsbeløpet, velger du **Forskuddsbetaling** under **Bokføring** i fanebladet **Handlinger** og velger deretter **Bokfør forskuddsfaktura**.  

## <a name="applying-the-prepayments"></a>Utligne forskuddsbetalingene  
Kunden betaler forskuddsbeløpet, og Magnus, som arbeider i regnskapsavdelingen, registrerer betalingen og utligner den mot forskuddsfakturaene.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Slik utligner du en betaling mot forskuddsfakturaene:  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Innbetalingskladder**, og velg deretter den relaterte koblingen.  
2.  Fyll ut en kladdelinje med følgende informasjon.  

    |Feltnavn|Angi|  
    |----------------|-----------|  
    |**Bilagstype**|**Betaling**|  
    |**Kontotype**|**Kunde**|  
    |**Kontonr.**|**20000**|  
3. Velg handlingen **Utlign poster**.  
4.  Velg den første forskuddsfakturaen i vinduet **Utlign kundeposter**, og velg deretter handlingen **Angi utlignings-ID**.  
5.  Gjenta forrige trinn for den andre forskuddsbetalingen.  
6.  Velg **OK**.  

    Beløpsfeltet er nå fylt ut med summen av de to forskuddsfakturaene.  

7.  Bokfør kladden.  

## <a name="invoicing-the-remaining-amount"></a>Fakturere restbeløpet  
Magnus har nå fått beskjed om at varene i ordren er levert, og at ordren er klar til fakturering. Magnus oppretter en faktura for ordren.  

#### <a name="to-invoice-the-remaining-amount"></a>Slik fakturerer du restbeløpet:  
1. Åpne ordren.  
2. Velg **Levere og fakturere**-handlingen, og velg deretter **OK**-knappen.  

> [!NOTE]  
>  Vanligvis ville transportavdelingen allerede ha bokført leveringen.  

Arnie kan vise historikken for å bekrefte at salgsfakturaen ble opprettet som tiltenkt.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  

## <a name="next-steps"></a>Neste trinn  
Denne gjennomgangen har ledet deg gjennom trinnene for å konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)] slik at du kan håndtere forskuddsbetalinger i det. Du har konfigurert standard forskuddsprosenter for kunder og varer, og du har også brukt flere ulike metoder til å beregne forskuddsbetalingene i en ordre. Du har prøvd å tilordne ett totalt forskuddsbeløp i ordren, og du har fått beregnet forskuddsbeløpet som en prosentsats for hele ordren.  

Du har også bokført en forskuddsfaktura, opprettet en ekstra forskuddsfaktura når ordren har blitt endret, og bokført den endelige fakturaen for restbeløpet.  

Med funksjonene for forskuddsbetaling i [!INCLUDE[d365fin](includes/d365fin_md.md)] blir det enkelt å konfigurere og håndheve forskuddsregler for kunder og varer, og du kan bokføre hver betaling mot en faktura.  

## <a name="see-also"></a>Se også  
[Fakturere forskuddsbetalinger](finance-invoice-prepayments.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)

