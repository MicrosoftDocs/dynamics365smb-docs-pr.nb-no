---
title: Definerer forskudd
description: Finn ut hvordan du konfigurerer Business Central slik at du kan bruke forskuddsbetalinger til å fakturere og kreve inn innskudd fra kunder, og remittere innskudd til leverandører.
author: edupont04
ms.topic: conceptual
ms.search.keyword: prepayment
ms.search.form: 314, 459, 460, 664
ms.date: 10/27/2021
ms.author: edupont
ms.openlocfilehash: a1b771425c2a70f62dcfebeb4619c0f2f5445de3
ms.sourcegitcommit: 93f30ce3349233cbcd03f300e74b654b49fa5518
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/24/2022
ms.locfileid: "8799615"
---
# <a name="set-up-prepayments"></a>Definerer forskudd

Hvis du krever at kundene skal betale før du leverer en ordre til dem, eller hvis leverandøren krever at du betaler før de leverer en ordre til deg, kan du bruke funksjonaliteten for forskudd. Med funksjonene for forskuddsbetaling kan du fakturere og kreve inn innskudd som kreves fra kunder, eller remittere innskudd til leverandører for å sørge for at alle delvise betalinger bokføres mot en faktura. Hvis du vil ha mer informasjon, kan du se [Opprette forskuddsfakturaer](finance-how-to-create-prepayment-invoices.md).

Før du kan bokføre forskuddsfakturaer, må du definere bokføringskontiene i Finans, og du må definere en nummerserie for forskuddsdokumenter. Du må angi en konto for forskuddsbetalinger som er knyttet til salg, og en konto for forskuddsbetalinger som er knyttet til innkjøp. Du kan angi at de samme bokføringskontoene skal brukes for alle forskuddsbetalinger knyttet til alle generelle bedriftsrelaterte bokføringsgrupper og generelle produktrelaterte bokføringsgrupper, eller du kan angi bestemte kontoer for bestemte bokføringsgrupper for henholdsvis salg og kjøp. Dette avhenger av selskapets krav for sporing av forskuddsbetalinger.  

Du kan definere hvor stor prosentdel av linjebeløpet som skal faktureres for forskuddsbetaling, for en kunde eller leverandør, for alle varer eller for utvalgte varer. Når du har fullført oppsettet, kan du generere forskuddsfakturaer fra ordrer og bestillinger. Du kan bruke standardprosentsatsene for hver salgs- eller kjøpslinje, eller du kan endre beløpene på fakturaen etter behov. Du kan for eksempel angi et totalbeløp for hele ordren.  

> [!NOTE]
> Vi anbefaler at du ikke bruker en forskuddsprosent på 100 i følgende tilfeller:
>
> * Hvis du befinner deg i Nord-Amerika. En forskuddsprosent på 100 kan føre til problemer med forskuddsfakturaer på grunn av måten avgifter beregnes på.
> * I noen regioner hvis du trekker en kontantrabatt fra fakturaen manuelt. En forskuddsprosent på 100 etterlater ikke automatisk et beløp som rabatten kan trekkes fra.
>
> Når du bruker forskuddsprosenten 100, kan det hente at [!INCLUDE[prod_short](includes/prod_short.md)] må opprette avrundingsposter. Når dette skjer, må du velge en finanskonto i feltet **Fakturaavrundingskonto** på siden **Kundebokføringsgrupper**. Dette gjelder også når du ikke har aktivert alternativet **Fakturaavrunding** på siden **Salgsoppsett**. Hvis du ikke angir en konto, kan du ikke bokføre forskuddsfakturaer. 

Siden det forhåndsbetalte beløpet tilhører kunden til de har mottatt varene eller tjenestene, må du sette opp finanskontoer for de forhåndsbetalte beløpene frem til den endelige fakturaen er bokført. Utgående forhåndsbetalinger må registreres i en gjeldskonto frem til fakturaen bokføres. Inngående forhåndsbetalinger må registreres i en aktivakonto frem til varene mottas. I tillegg må du definere en separat finanskonto for hver mva-type.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Slik legger du til forskuddskonti til generelt bokføringsoppsett  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Generelt bokføringsoppsett**, og velg deretter den relaterte koblingen.
2. På siden **Generelt bokføringsoppsett** for de relevante linjene må du fylle ut følgende felt:  

    * **Konto for salgsforskudd**  
    * **Konto for kjøpsforskudd**  

> [!TIP]
> Hvis du ikke kan se feltene på siden **Generelt bokføringsoppsett**, bruker du det vannrette rullefeltet nederst på siden til å bla til høyre.  

Hvis du ikke allerede har definert finanskontoer for forskuddsbetalinger, kan du åpne siden **Finanskontooversikt** fra det relevante kontofeltet.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Slik setter du opp nummerserie for forskuddsdokumenter  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgsoppsett**, og velg deretter den relaterte koblingen.
2. På siden **Salgsoppsett** i hurtifanen **Nummerserier** fyller du ut følgende felt:  

   * **Bokførte fakturanumre for forskudd**
   * **Bokførte kreditnotanumre for forskudd**

3. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsoppsett**, og velg deretter den relaterte koblingen.
4. På siden **Kjøpsoppsett** i hurtigfanen **Nummerserier** fyller du ut følgende felt:

    * **Bokførte fakturanumre for forskudd**
    * **Bokførte kreditnotanumre for forskudd**

> [!NOTE]  
> Du kan bruke samme nummerserie for forskuddsfakturaer og vanlige fakturaer, eller du kan bruke forskjellige nummerserier. Hvis du bruker forskjellige serier, kan de ikke overlappe hverandre fordi ett og samme nummer kan ikke forekomme i begge seriene.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Definere forskuddsprosenter for varer, kunder og leverandører

For en vare kan du definere en standard forskuddsprosent for alle kunder, en bestemt kunde eller en kundeprisgruppe. Hvis du ikke vil bruke samme forskuddsprosent på alle kunder, må du angi hvilke kunder eller hvilke kundeprisgrupper forskuddsprosenten skal gjelde.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Velg en vare, og velg deretter handlingen **Forskuddsprosenter**.  
3. Fyll ut feltene etter behov på siden **Forskuddsprosenter for salg**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

For en kunde eller leverandør kan du definere en standard forskuddsprosent for alle varer og alle typer salgslinjer. Du angir denne på kortet for kunden eller leverandøren. Følgende fremgangsmåte viser hvordan du angir en forskuddsprosent for en kunde, men lignende fremgangsmåte gjelder leverandører.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Åpne kortet for en kunde.
3. Fyll ut feltet **Forskuddsprosent**.
4. Gjenta fremgangsmåten for andre kunder eller leverandører.  

> [!TIP]
> Du kan også bruke siden **Forskuddsprosenter for salg** fra kunden eller leverandøren.

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Slik bestemmes hvilken forskuddsprosent som har førsteprioritet  

En ordre kan ha en forskuddsprosent på salgshodet og en annen prosent for varene på linjene. For å bestemme hvilken forskuddsprosent som gjelder for hver salgslinje, leter systemet etter forskuddsprosenten i den følgende ordren. Den første standardverdien som blir funnet, blir tatt i bruk:  

1. En forskuddsprosent for varen på linjen og kunden som ordren er for.  
2. En forskuddsprosent for varen på linjen og kundeprisgruppen som kunden tilhører.  
3. En forskuddsprosent for varen på linjen for alle kunder.  
4. Forskuddsprosenten i salgs- eller bestillingshodet.  

Forskuddsprosenten på kundekortet gjelder med andre ord bare hvis det ikke er satt opp noen forskuddsprosent for varen. Hvis du imidlertid endrer innholdet i feltet **Forskuddsprosent** i salgs- eller bestillingshodet etter at du har opprettet linjene, oppdateres forskuddsprosenten på alle linjene. Dette gjør det enkelt å opprette en ordre med en fast forskuddsprosent uavhengig av prosenten som er satt opp for varene.

## <a name="to-automatically-release-sales-orders-when-prepayments-are-applied"></a>Slik frigir du ordrer automatisk når forskuddsbetalinger brukes

Du kan spare tid ved å opprette en jobbkøpost som automatisk frigir ordrer som krever forskuddsbetaling, etter at betalinger er utlignet. Når du automatiserer prosessen, sparer du trinnet ved å frigi ordren.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgsoppsett**, og velg deretter den relaterte koblingen.
2. I feltet **Hyppighet for automatisk oppdatering av forskudd** angir hvor ofte du vil at jobbkøen skal kjøres.

> [!TIP]
> Mens du er her, kan du vurdere å legge til beskyttelse mot levering eller fakturering av ordrer som har ubetalte forskuddsbeløp. Hvis du aktiverer alternativet **Kontroller forskudd ved bokføring**, hindrer [!INCLUDE[prod_short](includes/prod_short.md)] at personer bokfører ordrer med utestående forskuddsbeløp.

3. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Jobbkøposter**, og velg deretter den relaterte koblingen.
4. Konfigurer jobbkøposten **Oppdater ventende forskuddssalg**, for eksempel ved å bruke innstillingene i hurtigfanen **Regelmessighet** til å planlegge hvor ofte den skal kjøres. Hvis du vil ha mer informasjon, kan du se [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

## <a name="see-also"></a>Se også  

[Fakturere forskuddsbetalinger](finance-invoice-prepayments.md)  
[Gjennomgang: konfigurere og fakturere salgsforskudd](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Beregne mva på varer og tjenester på forskuddsbetalinger i Australia](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Beregne mva på varer og tjenester på forskuddsbetalinger i New Zealand](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Forstå Finans og kontoplanen](finance-general-ledger.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]