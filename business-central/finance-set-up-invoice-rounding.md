---
title: Definere fakturaavrunding | Microsoft-dokumentasjon
description: Du kan runde av fakturabeløp når du oppretter fakturaer. I tillegg kan lokale forskrifter eller lokale regler kreve at fakturaen rundes av på en bestemt måte, for eksempel til et beløp som kan deles på 0,05.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 0f32fd85c475e2950ae7bc5c6e2fcdc8b08a184e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783700"
---
# <a name="set-up-invoice-rounding"></a>Definere fakturaavrunding
Hvis du må runde av fakturabeløp når du oppretter fakturaer, kan du bruke funksjonen for automatisk avrunding. Når en faktura rundes av, legges det til en ekstra linje med avrundingsbeløpet, og denne linjen bokføres sammen med de andre fakturalinjene.

> [!NOTE]  
>  Lokale forskrifter eller lokale regler kan kreve at fakturaen rundes av på en bestemt måte, for eksempel til et beløp som kan deles på 0,05.  

Hvis du vil bruke automatisk fakturaavrunding, må du gjøre følgende:  

* Angi finanskontiene der avrundingsdifferanser skal bokføres.  
* Definere regler for avrunding av fakturaer i lokal valuta og utenlandsk valuta.  
* Aktivere funksjonen.  

> [!NOTE]  
>  I tillegg til funksjonene for fakturaavrunding kan beløp på fakturaer rundes av med prisavrundingsfunksjonen og beløpsavrundingsfunksjonen.  

## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Definere finanskonti i for avrundingsdifferanser på fakturaer
Hvis du vil bruke funksjonen for automatisk fakturaavrunding, må du opprette finanskontoen(e) der avrundingsdifferansen skal bokføres. Før du kan gjøre dette, må du opprette mva-bokføringsgrupper for varer. Hvis du vil ha mer informasjon, kan du se [Konfigurere mva](finance-setup-vat.md).  

### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Slik setter du opp finanskonti for avrundingsdifferanser på fakturaer  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoplan**, og velg deretter den relaterte koblingen.  
2. Sett opp kontoen på siden **Kontoplan**, og gi den navnet **Fakturaavrunding** eller noe lignende. [!INCLUDE[prod_short](includes/prod_short.md)] bruker kontonavnet som tekst for fakturaer som er avrundet.  
3. Avhengig av om du bruker mva eller salgsmva, i feltene **Mva-bokføringsgruppe - vare** eller **Mva-bokf.gruppe - vare** velger du en bokføringsgruppe for avrundede beløp. Du kan også definere en ny gruppekode som skal brukes til fakturaavrunding.
4. La feltet **Bokføringstype** og ett av feltene **Mva-bokføringsgruppe - firma** eller **Mva-bokf.gruppe - firma** stå tomt. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

Du kan nå tilordne fakturaavrundingskontoen til bokføringsgrupper på siden **Bokføringsgrupper - leverandør**.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a>Definere avrunding for fremmed og lokal valuta
Før du kan bruke funksjonen for automatisk fakturaavrunding for fakturaer, må du definere avrundingsregler for fremmed og lokal valuta.

### <a name="to-set-up-rounding-for-foreign-currencies"></a>Slik oppretter du avrundingsregler for fremmed valuta  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Valutaer**, og velg deretter den relaterte koblingen.  
2. På **Valutaer**-siden velger du den fremmede valutaen for å åpne **valutakortet**, og deretter fyller du ut feltet **Avrundingspresisjon, beløp**, **Avrundingspresisjon, pris**, **Avrundingspresisjon, faktura** og **Fakturaavrundingstype**.

### <a name="to-set-up-rounding-for-your-local-currency"></a>Slik oppretter du avrunding for den lokale valutaen
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finansoppsett**, og velg deretter den relaterte koblingen.  
2. På siden **Finansoppsett** på hurtigfanen **Generelt** fyller du ut feltene **Avrund.presisjon faktura** og **Fakturaavrundingstype**.  

## <a name="activate-the-invoice-rounding-function"></a>Aktivere funksjonen for fakturaavrunding  
For å sørge for at salgs- og kjøpsfakturaer avrundes automatisk, må du aktivere fakturaavrundingsfunksjonen. Du aktiverer fakturaavrunding separat for salgs- og kjøpsfakturaer.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsoppsett** eller **Kjøpsoppsett**, og velg deretter den relaterte koblingen.  
2. På hurtigfanen **Generelt** velger du **Fakturaavrunding**.  

## <a name="see-also"></a>Se også  
[Fakturere salg](sales-how-invoice-sales.md)  
[Registrere kjøp](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]