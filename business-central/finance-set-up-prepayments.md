---
title: Definere forskudd | Microsoft-dokumentasjon
description: Forskuddsbetalinger er betalinger som faktureres og bokføres i en salgs- eller kjøpsforskuddsordre før endelig fakturering. Du må kanskje ha et innskudd før du produserer varer etter ordre, eller du må ha betaling før du sender varer til en kunde. Med funksjonene for forskuddsbetaling kan du fakturere og kreve inn innskudd som kreves fra kunder, eller remittere innskudd til leverandører. Dermed kan du sikre at alle betalinger bokføres mot en faktura.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: prepayment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 34e5d1e0f424097de259d01e438158f6a92390ae
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750433"
---
# <a name="set-up-prepayments"></a>Definerer forskudd
Hvis du krever at kundene skal betale før du leverer en ordre til dem, eller hvis leverandøren krever at du betaler før de leverer en ordre til deg, kan du bruke funksjonaliteten for forskudd. Med funksjonene for forskuddsbetaling kan du fakturere og kreve inn innskudd som kreves fra kunder, eller remittere innskudd til leverandører og sørge for at alle delvise betalinger bokføres mot en faktura. Hvis du vil ha mer informasjon, kan du se [Opprette forskuddsfakturaer](finance-how-to-create-prepayment-invoices.md).

Før du kan bokføre forskuddsfakturaer, må du definere bokføringskontiene i Finans, og du må definere en nummerserie for forskuddsdokumenter. Du må angi en konto for forskuddsbetalinger som er knyttet til salg, og en konto for forskuddsbetalinger som er knyttet til innkjøp. Du kan angi at de samme bokføringskontoene skal brukes for alle forskuddsbetalinger knyttet til alle generelle bedriftsrelaterte bokføringsgrupper og generelle produktrelaterte bokføringsgrupper, eller du kan angi bestemte kontoer for bestemte bokføringsgrupper for henholdsvis salg og kjøp. Dette avhenger av selskapets krav for sporing av forskuddsbetalinger.  

Du kan definere hvor stor prosentdel av linjebeløpet som skal faktureres for forskuddsbetaling, for en kunde eller leverandør, for alle varer eller for utvalgte varer. Når du har fullført oppsettet, kan du generere forskuddsfakturaer fra ordrer og bestillinger. Du kan bruke standardprosentsatsene for hver salgs- eller kjøpslinje, eller du kan endre beløpene på fakturaen etter behov. Du kan for eksempel angi et totalbeløp for hele ordren.  

> [!NOTE]
> Vi anbefaler at du ikke bruker en forskuddsprosent på 100 % i følgende tilfeller:
> * Hvis du befinner deg i Nord-Amerika. En forskuddsprosent på 100 % kan føre til problemer med forskuddsfakturaer på grunn av måten avgifter beregnes på.
> * I noen regioner hvis du trekker en kontantrabatt fra fakturaen manuelt. En forskuddsprosent på 100 % etterlater ikke automatisk et beløp som rabatten kan trekkes fra. 

Siden det forhåndsbetalte beløpet tilhører kunden til de har mottatt varene eller tjenestene, må du sette opp finanskontoer for de forhåndsbetalte beløpene frem til den endelige fakturaen er bokført. Utgående forhåndsbetalinger må registreres i en gjeldskonto frem til fakturaen bokføres. Inngående forhåndsbetalinger må registreres i en aktivakonto frem til varene mottas. I tillegg må du definere en separat finanskonto for hver mva-type.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Slik legger du til forskuddskonti til generelt bokføringsoppsett  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Generelt bokføringsoppsett**, og velg deretter den relaterte koblingen.
2. På siden **Generelt bokføringsoppsett** må du fylle ut følgende felt:  

    - **Konto for salgsforskudd**  
    - **Konto for kjøpsforskudd**  

> [!TIP]
> Hvis du ikke kan se feltene på siden **Generelt bokføringsoppsett**, bruker du det vannrette rullefeltet nederst på siden til å bla til høyre.  

Hvis du ikke allerede har definert finanskontoer for forskuddsbetalinger, kan du åpne siden **Finanskontooversikt** fra det relevante kontofeltet.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Slik setter du opp nummerserie for forskuddsdokumenter  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.
2. På siden **Generelt bokføringsoppsett** må du fylle ut følgende felt:  

   - **Bokførte fakturanumre for forskudd**
   - **Bokførte kreditnotanumre for forskudd**

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsoppsett**, og velg deretter den relaterte koblingen.
2. På siden **Generelt bokføringsoppsett** må du fylle ut følgende felt:

    - **Bokførte fakturanumre for forskudd**
    - **Bokførte kreditnotanumre for forskudd**

> [!NOTE]  
> Du kan bruke samme nummerserie for forskuddsfakturaer og vanlige fakturaer, eller du kan bruke forskjellige nummerserier. Hvis du bruker forskjellige serier, kan de ikke overlappe hverandre fordi ett og samme nummer kan ikke forekomme i begge seriene.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Definere forskuddsprosenter for varer, kunder og leverandører  
For en vare kan du definere en standard forskuddsprosent for alle kunder, en bestemt kunde eller en kundeprisgruppe.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.
2. Velg en vare, og velg deretter handlingen **Forskuddsprosenter**.  
3. Fyll ut feltene etter behov på siden **Forskuddsprosenter for salg**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

For en kunde eller leverandør kan du definere en standard forskuddsprosent for alle varer og alle typer salgslinjer. Du angir denne på kortet for kunden eller leverandøren.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne kortet for en kunde.
3. Fyll ut feltet **Forskuddsprosent**.
4. Gjenta fremgangsmåten for andre kunder eller leverandører.  

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Slik bestemmes hvilken forskuddsprosent som har førsteprioritet  

En ordre kan ha en forskuddsprosent på salgshodet og en annen prosent for varene på linjene. For å bestemme hvilken forskuddsprosent som gjelder for hver salgslinje, leter systemet etter forskuddsprosenten i den følgende ordren. Den første standardverdien som blir funnet, blir tatt i bruk:  

1. En forskuddsprosent for varen på linjen og kunden som ordren er for.  
2. En forskuddsprosent for varen på linjen og kundeprisgruppen som kunden tilhører.  
3. En forskuddsprosent for varen på linjen for alle kunder.  
4. Forskuddsprosenten i salgs- eller bestillingshodet.  

Forskuddsprosenten på kundekortet gjelder med andre ord bare hvis det ikke er satt opp noen forskuddsprosent for varen. Hvis du imidlertid endrer innholdet i feltet **Forskuddsprosent** i salgs- eller bestillingshodet etter at du har opprettet linjene, oppdateres forskuddsprosenten på alle linjene. Dette gjør det enkelt å opprette en ordre med en fast forskuddsprosent uavhengig av prosenten som er satt opp for varene.

## <a name="see-also"></a>Se også  

[Fakturere forskuddsbetalinger](finance-invoice-prepayments.md)  
[Gjennomgang: konfigurere og fakturere salgsforskudd](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Beregne mva på varer og tjenester på forskuddsbetalinger i Australia](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Beregne mva på varer og tjenester på forskuddsbetalinger i New Zealand](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Forstå Finans og kontoplanen](finance-general-ledger.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
