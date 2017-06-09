---
title: Arbeide med finanskladder | Microsoft-dokumentasjon
description: "Lær hvordan finanskladder fungerer."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/03/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 13257a5d82d742d92fb22da9da7ff7f773d7d2f8
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="working-with-general-journals"></a>Arbeide med finanskladder
DU bruker finanskladder til å bokføre finanstransaksjoner til finanskonti og andre konti, for eksempel bank-, kunde- og leverandørkonti. Bokføring med en finanskladd oppretter alltid poster på finanskonti. Dette gjelder selv om en kladdelinje for eksempel bokføres på en kundekonto, ettersom en post bokføres til en finanssamlekonto via en bokføringsgruppe.

[!INCLUDE[d365fin](includes/d365fin_md.md)] har også ikke-finanskladder, for eksempel varekladden og vareopptellingskladden, men disse kladdene vises ikke i brukergrensesnittet.

Opplysningene du angir i en kladd, er midlertidige og kan endres mens de fortsatt befinner seg i kladden. Når du bokfører kladden, overføres opplysningene til poster i individuelle konti, der de ikke kan endres. Du kan imidlertid oppheve utligningen av bokførte poster, og du kan bokføre tilbakeførings- eller korrigeringsposter.

## <a name="journal-templates-and-batches"></a>Kladdemaler og kladder
Det finnes flere finanskladdemaler. Hver kladdemal er representert av et eget vindu med bestemte funksjoner og feltene som er nødvendige for å støtte disse funksjonene, for eksempel vinduet **Betalingsavstemmingskladd** for å behandle betalinger og **Betalingskladd** for å betale leverandører.

**Merk**: Hvis du eksporterer betalingsfiler til banken fra utbetalingskladden, må du merke av for **Tillat betalingseksport** for den aktuelle i kladdebunken i vinduet **Finanskladder**. Hvis du vil ha mer informasjon, kan du se [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

Du kan definere dine egne personlige kladder som en kladd for hver enkelt kladdemal. Du kan for eksempel definere din egen kladd for betalingskladden som har personlig oppsett og innstillinger.

Et eksempel på en personlig innstilling som du kan definere i finanskladden, er å få systemet til å hjelpe deg med å fylle ut beløpsfelt. Hvis du merker av for **Foreslå motkontobeløp** på linjen for den kladden i vinduet **Finanskladder**, vil deretter for eksempel **Beløp**-feltet på finanskladdelinjer for samme dokumentnummer, automatisk forhåndsutfylles med verdien som kreves for balansere dokumentet. Hvis du vil ha mer informasjon, se [La [!INCLUDE[d365fin](includes/d365fin_md.md)] foreslå verdier](ui-let-system-suggest-values.md).

## <a name="main-accounts-and-balancing-accounts"></a>Hovedkontoer og motkontoer
Hvis du har definert standard motkonti for kladdene, vil motkontoen bli fylt ut automatisk når du fyller ut **Kontonr.**-fetet. . Hvis ikke, fyller du ut **Kontonr.** -feltet og **Motkontonr.** -feltet manuelt. Et positivt beløp i **Beløp**-feltet debiteres hovedkontoen og krediteres motkontoen. Et negativt beløp krediteres hovedkontoen og debiteres motkontoen.

**Merk**: Mva beregnes separat for hovedkontoen og motkontoen, så de kan bruke ulike mva-prosentsatser.

## <a name="recurring-journals"></a>Gjentakelseskladder
En gjentakende kladd er en finanskladd med bestemte felt for håndtering av transaksjoner du bokfører ofte, med få eller ingen endringer. Hvis du bruker disse feltene for gjentatte transaksjoner, kan du bokføre både faste og variable beløp. Du kan også angi automatiske tilbakeføringsposter for dagen etter bokføringsdatoen, og bruke fordelingsnøkler med de gjentakende postene.

## <a name="see-also"></a>Se også
[Bruke fordelingsnøkler i finanskladder](ui-how-use-allocation-keys-general-journals.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

