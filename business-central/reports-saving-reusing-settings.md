---
title: Bruke og endre lagrede innstillinger i rapporter | Microsoft-dokumentasjon
description: "Beskriver hvordan du bruker forhåndsdefinerte alternativer og filtre til å tilpasse rapporter og generere riktige data."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: f5225d1f6d0d4ac0020fb073d5df6da83b5c0f5b
ms.contentlocale: nb-no
ms.lasthandoff: 06/28/2018

---
# <a name="managing-saved-settings-on-reports"></a>Administrere lagrede innstillinger i rapporter
Avhengig av hvilken rapport som skal kjøres, kan det vises en side som lar deg angi bestemte alternativer og filtre for å endre dataene som er inkludert i den genererte rapporten. Denne siden kalles rapportforespørselssiden. En rapport kan inneholde en eller flere *lagrede innstillinger* som du kan bruke på rapporten fra forespørselssiden. *Lagrede innstillinger* er i hovedsak forhåndsdefinerte alternativer og filtre. Lagrede innstillinger er en rask og pålitelig metode for å generere konsekvent rapporter som inneholder de riktige dataene.

Du kan se de lagrede innstillingene som er tilgjengelige for en rapport i delen **Lagrede innstillinger** i rapportforespørselssiden.  

## <a name="apply-saved-settings-to-a-report"></a>Bruke lagrede innstillinger på en rapport
1. Åpne rapporten.

   Rapportforespørselssiden vises.    
2. I delen **Lagrede innstillinger** på siden, setter du **Navn**-feltet til de lagrede innstillingene du vil bruke.

   Delen **Lagrede innstillinger** vises bare hvis rapporten er kjørt tidligere eller hvis det finnes eksisterende oppføringer for lagrede innstillinger. Oppføringen med lagrede innstillinger, som kalles **Sist brukte alternativer og filtre**, er alltid tilgjengelig. Disse innstillingene er verdiene for alternativet og filteret som ble brukt sist gang du kjørte rapporten.

## <a name="create-and-modify-saved-settings-for-all-users"></a>Opprette og endre lagrede innstillinger for alle brukere
Hvis du har riktige tillatelser, kan du vise, opprette og endre de lagrede innstillingene for alle rapporter for alle brukere i firmaet. Du kan tilordne lagrede innstillingene for en rapport til enkeltbrukere eller alle brukerne i firmaet.

Du kan administrere lagrede innstillinger fra siden 1506 **Rapportinnstillinger**. Du åpner denne siden ved å velge ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Rapportinnstillinger** og deretter velge den relaterte koblingen.

Fra siden **Rapportinnstillinger** kan du opprette en ny innstillinger fra bunnen av eller du kan kopiere og endre eksisterende innstillinger. Hvis du vil endre alternativer og filtre for en innstillingene, velger du **Rediger**-handling.

> [!NOTE]
> Funksjonen for lagrede innstillinger i rapporter gjelder bare når SaveValues-egenskapen for forespørselssiden er satt til Ja. SaveValues-egenskapen angis i utviklingsmiljøet.  

> [!Important]
> Hvis du oppretter et element for lagrede innstillinger for alle brukere, og det har samme navn som eksisterende lagrede innstillinger for en bestemt bruker, kan ikke brukeren bruke de lagrede innstillingene som er tilordnet til alle.  I feltet Lagrede innstillinger på rapportforespørselssiden, vil brukeren se to lagrede innstillingsalternativer med samme navn. Uansett hvilket alternativ som velges, vil imidlertid de brukerspesifikke lagrede innstillingene bli brukt.

## <a name="see-also"></a>Se også
[Arbeide med rapporter](ui-work-report.md)  

