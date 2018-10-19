---
title: Definere forskudd | Microsoft-dokumentasjon
description: "Forskuddsbetalinger er betalinger som faktureres og bokføres i en salgs- eller kjøpsforskuddsordre før endelig fakturering. Du må kanskje ha et innskudd før du produserer varer etter ordre, eller du må ha betaling før du sender varer til en kunde. Med funksjonene for forskuddsbetaling kan du fakturere og kreve inn innskudd som kreves fra kunder, eller remittere innskudd til leverandører. Dermed kan du sikre at alle betalinger bokføres mot en faktura."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b4469b91f8bb377e4fef5700063d6085ac700605
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-prepayments"></a>Definerer forskudd
Hvis du krever at kundene skal betale før du leverer en ordre til dem, eller hvis leverandøren krever at du betaler før de leverer en ordre til deg, kan du bruke funksjonaliteten for forskudd. Med funksjonene for forskuddsbetaling kan du fakturere og kreve inn innskudd som kreves fra kunder, eller remittere innskudd til leverandører og sørge for at alle delvise betalinger bokføres mot en faktura. Hvis du vil ha mer informasjon, kan du se [Opprette forskuddsfakturaer](finance-how-to-create-prepayment-invoices.md).

Før du kan bokføre forskuddsfakturaer, må du definere bokføringskontiene i Finans, og du må definere en nummerserie for forskuddsdokumenter.  

Du kan definere hvor stor prosentdel av linjebeløpet som skal faktureres for forskuddsbetaling, for en kunde eller leverandør, for alle varer eller for utvalgte varer. Når du har fullført oppsettet, kan du generere forskuddsfakturaer fra ordrer og bestillinger. Du kan bruke standardprosentsatsene for hver salgs- eller kjøpslinje, eller du kan endre beløpene på fakturaen etter behov. Du kan for eksempel angi et totalbeløp for hele ordren.  

Siden det forhåndsbetalte beløpet tilhører kunden til de har mottatt varene eller tjenestene, må du sette opp finanskontoer for de forhåndsbetalte beløpene frem til den endelige fakturaen er bokført. Utgående forhåndsbetalinger må registreres i en gjeldskonto frem til fakturaen bokføres. Inngående forhåndsbetalinger må registreres i en aktivakonto frem til varene mottas. I tillegg må du definere en separat finanskonto for hver mva-type.

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Slik legger du til forskuddskonti til generelt bokføringsoppsett  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Generelt bokføringsoppsett**, og velg deretter den relaterte koblingen.
2. I vinduet **Generelt bokføringsoppsett** må du fylle ut følgende felt:  

    - **Konto for salgsforskudd**  
    - **Konto for kjøpsforskudd**  

Hvis du ikke allerede har definert finanskonti for forskuddsbetalinger, kan du gjøre det vinduet **Finanskontooversikt**.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Slik setter du opp nummerserie for forskuddsdokumenter  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Salgsoppsett**, og velg deretter den relaterte koblingen.
2. I vinduet **Generelt bokføringsoppsett** må du fylle ut følgende felt:  

   - **Bokførte fakturanumre for forskudd**
   - **Bokførte kreditnotanumre for forskudd**

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsoppsett**, og velg deretter den relaterte koblingen.
2. I vinduet **Generelt bokføringsoppsett** må du fylle ut følgende felt:

    - **Bokførte fakturanumre for forskudd**
    - **Bokførte kreditnotanumre for forskudd**

> [!NOTE]  
>  Du kan bruke samme nummerserie for forskuddsfakturaer og vanlige fakturaer, eller du kan bruke forskjellige nummerserier. Hvis du bruker forskjellige serier, kan de ikke overlappe hverandre fordi ett og samme nummer kan ikke forekomme i begge seriene.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Definere forskuddsprosenter for varer, kunder og leverandører  
For en vare kan du definere en standard forskuddsprosent for alle kunder, en bestemt kunde eller en kundeprisgruppe.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.
2. Velg en vare, og velg deretter handlingen **Forskuddsprosenter**.  
3. Fyll ut feltene etter behov i vinduet **Forskuddsprosenter for salg**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

For en kunde eller leverandør kan du definere en standard forskuddsprosent for alle varer og alle typer salgslinjer. Du angir denne på kortet for kunden eller leverandøren.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kunder**, og velg deretter den relaterte koblingen.
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
[Forstå Finans og kontoplanen](finance-general-ledger.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

