---
title: Definere vareenheter | Microsoft-dokumentasjon
description: Du kan definere flere enheter for en vare slik at du kan tilordne enheter til varen for følgende formål.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 04/01/2019
ms.author: SorenGP
ms.openlocfilehash: 47d59af91af7c043c98a4db2a5c103b0052e32e2
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239432"
---
# <a name="set-up-item-units-of-measure"></a>Definere vareenheter
Du kan definere flere enheter for en vare slik at du kan tilordne enheter til varen for følgende formål:

- Tilordne en lagerenhet på varekortet for varen for å definere hvordan den lagres på lageret, og for å bruke den som grunnlaget for konvertering for alternative enheter.
- Tilordne alternative enheter til kjøps-, produksjons- eller salgsdokumenter for å angi hvor mange enheter av lagerenheter du håndterer samtidig i disse prosessene. Du kan for eksempel kjøpe varen på paller, og bare bruke enkeltdeler i produksjonen.

Hvis en vare lagerføres i én enhet, men produseres i en annen, opprettes en produksjonsordre som bruker en produksjonsbunkeenhet til å beregne riktig antall komponenter mens kjørselen **Forny produksjonsordre** kjøres. Ett eksempel på beregning med produksjonsbunkeenhet er når en produsert vare lagerføres i stykker, men produseres i tonn. Hvis du vil ha mer informasjon, kan du se [Arbeide med produksjonsbunkeenhet](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).

## <a name="to-set-up-a-unit-of-measure"></a>Slik definerer du en enhet:
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.
2. Åpne varekortet som du vil definere alternative enheter for.
3. Velg handlingen **Enheter**. Siden **Vareenheter** åpnes.
4. Hvis feltet **Lagerenhet** på varekortet er fylt ut, er denne enheten allerede konfigurert.
5. Velg handlingen **Ny**. Det settes inn en ny, tom linje.
6. I feltet **Kode** angir du navnet på enheten. Du kan også velge feltet for å velge fra enhetskodene som finnes i databasen.
7. I feltet **Antall per enhet** angir du hvor mange enheter av lagerenheten den nye enheten inneholder.
8. Gjenta trinn 5 til 7 for å definere alle alternative enheter som du vil bruke i ulike prosesser for denne varen.

Du kan nå bruke de alternative enhetene på kjøps-, produksjons- og salgsdokumenter. Hvis du vil ha mer informasjon, kan du se Angi standardenhetskoder for kjøpstransaksjoner og salgstransaksjoner eller Bruke produksjonsbunkeenheten.

## <a name="to-set-up-unit-of-measure-translations"></a>Slik definerer du enhetsoversettelser
Når du selger varer til kunder i utlandet, kan du angi enheten på kundens språk. Dette gjør du etter at du har definert de enhetsoversettelsene du trenger.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Enheter**, og velg deretter den relaterte koblingen.
2. Velg koden du vil definere oversettelser for, og velg deretter handlingen **Oversettelser**.
3. I **Språkkode**-feltet velger du rullegardinpilen for å vise en oversikt over tilgjengelige språkkoder. Velg språkkoden du vil opprette en oversettelse for, og klikk deretter OK-knappen for å kopiere koden til feltet.
4. Angi den teksten i feltet **Beskrivelse**.
5. Gjenta trinn 2 til 4 for enhetskodene og språkene du vil angi oversettelser for.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Angi en standardenhetskode for kjøpstransaksjoner
Hvis du vanligvis kjøper eller selger i andre enheter enn lagerenhetene, kan du angi en separat enhet for innkjøp og salg. Hvis du vil gjøre dette, må du definere enheter på siden **Vareenheter**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.
2. Åpne det aktuelle varekortet du vil angi en standardkode for salgs- eller kjøpsenhet for.
3. For salg åpner du siden **Vareenheter** i feltet **Salgsenhet** på hurtigfanen **Fakturering**.
4. For kjøp åpner du siden **Vareenheter** under **Kjøpsenhet** på hurtigfanen **Etterfylling**.
5. Velg koden du vil definere som standardenhet for salg eller kjøp, og velg deretter **OK**-knappen.

## <a name="see-also"></a>Se også
[Arbeide med produksjonsbunkeenhet](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Håndtere lager](inventory-manage-inventory.md)  
[Håndtere kjøp](purchasing-manage-purchasing.md)  
[Håndtere salg](sales-manage-sales.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
