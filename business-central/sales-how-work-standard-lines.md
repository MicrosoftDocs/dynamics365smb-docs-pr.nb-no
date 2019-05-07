---
title: Definere standardlinjer for gjentakende salg og kjøp | Microsoft-dokumentasjon
description: Du kan definere salgslinjer og kjøpslinjer du ofte lager, og deretter sette dem inn i salgs- og kjøpsdokumenter for å fylle ut linjene raskt med standardinformasjon.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 35395ad71dbc0717410ed5a910f5bcd0170b1d8c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "936791"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Opprette gjentakende salgs- og kjøpslinjer
Hvis du ofte må opprette salgs- og kjøpslinjer med lignende informasjon, kan du definere standardlinjer du deretter kan sette inn på gjentakende salgs- og kjøpsdokumenter, for eksempel for gjentakende etterfyllingsordrer.  

Fremgangsmåtene nedenfor viser hvordan du arbeider med standardlinjer på en salgsfaktura. Den fungerer på lignende måte for alle andre salgsdokumenter og alle kjøpsdokumenter.  

## <a name="to-set-up-standard-sales-lines"></a>Definere standard salgslinjer  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Standard salgslinjer**, og velg deretter den relaterte koblingen.  
2. På siden **Standard salgslinjer** velger du handlingen **Ny**.  
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I hurtigfanen **Linjer** angir du informasjon i feltene for å klargjøre salgslinjer som gjenspeiler standardlinjene du forventer å bruke som gjentakende linjer i salgsdokumenter.  

> [!NOTE]
> Du kan ikke definere priser på standardsalgslinjene, fordi priser, rabatter og så videre. beregnes på de faktiske salgsdokumentene etter at du setter inn standardsalgslinjene.

## <a name="to-assign-standard-sales-lines-to-a-customers"></a>Slik tilordner du standard salgslinjer til kunder
Tilordne én eller flere standard salgslinjer til en kunde, slik at de kan settes inn i salgsdokumenter for kunden.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne kortet for den aktuelle kunden.
3. Velg handlingen **Gjentakende salgslinjer**.
4. På siden **Gjentakende salgslinjer** velger du kodene for de gjentakende salgslinjene som du vil sette inn i salgsdokumenter for kunden.
5. Fyll ut de andre feltene for å definere når, hvordan og hvor de gjentakende salgslinjene skal brukes. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Sette inn gjentakende salgslinjer i en salgsfaktura
Hvis det finnes gjentakende salgslinjer for kunden, kan de kan settes inn på alle typer salgsdokumenter, for eksempel en salgsfaktura. Hvis du har aktivert den aktuelle meldingen, blir du informert om det finnes gjentakende salgslinjer.
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Fakturaer**, og velg deretter den relaterte koblingen.
2. Åpne salgsfakturaen du vil sette inn én eller flere standard salgslinjer på.
3. Velg handlingen **Hent gjentakende salgslinjer**.
4. På siden **Gjentakende salgslinjer** velger du oppslagsknappen i **Kode**-feltet, og deretter velger du et sett med standard salgslinjer.

    > [!NOTE]
    > For å bruke settet med gjentakende salgslinjer sammen med kjørselen **Opprett gjentakende salgsfakturaer** må du også fylle ut feltene **Gyldig fra-dato** og **Gyldig til-dato** på siden **Gjentakende salgslinjer**. Hvis du vil ha mer informasjon, kan du se [Opprette flere salgsfakturaer basert på standard salgslinjer](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-standard-sales-lines).

5. Velg **OK** for å sette inn de standard salgslinjene på fakturaen, der du kan bruke informasjonen på nytt som den er eller redigere den.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Opprette flere salgsfakturaer basert på standard salgslinjer
Du kan bruke kjørselen **Opprett gjentakende salgsfakturaer** til å opprette salgsfakturaer i henhold til standard salgslinjer som er tilordnet til kundene, og med bokføringsdatoer innenfor gyldig-fra- og gyldig til-datoer du angir på standardsalgslinjene.

> [!NOTE]
> På siden **Gjentakende salgslinjer** kan du også angi en Direct Debit-betalingsmåte og en Direct Debit-belastningsfullmakt. Salgsfakturaene som er opprettet med den satsvise jobben **Opprett gjentak. salgsfakt.**, vil dermed inneholde informasjon som kreves for å kreve inn betaling for salgsfakturaer med SEPA direct debit. Hvis du vil ha mer informasjon, kan du se [Innkreve betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Opprett gjentakende salgsfakturaer**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene på siden **Opprett gjentakende salgsfakturaer** etter behov.
3. I filterfeltet **Kode** angir du koden for standard salgslinjer som er tilordnet en kunde du vil opprette salgsfakturaer for.
4. Velg **OK**.

Salgsfakturaer blir opprettet for kunder med angitt standard kundesalgskode og eventuell angitt avtalegiroinformasjon, for bokføring på den angitte datoen.

## <a name="see-also"></a>Se også  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
