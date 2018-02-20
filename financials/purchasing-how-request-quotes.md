---
title: "Opprette en forespørsel for å be om et tilbud fra leverandøren | Microsoft-dokumentasjon"
description: "Beskriver hvordan du oppretter et tilbud eller et tilbudsforespørselsdokument for å registrere tilbudet til en kunde og selge produkter under visse betingelser."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3fe5eca9c26380248471facbd945838b1bf47a1d
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="request-quotes"></a>Be om tilbud
En forespørsel kan brukes som et foreløpig utkast til en bestilling, og bestillingen kan deretter konverteres til en bestilling eller ordre.


## <a name="to-create-a-purchase-quote"></a>Slik oppretter du en forespørsel
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Forespørsler**, og velg deretter den relaterte koblingen.
2. Opprett et nytt dokument, på samme måte som du oppretter en bestilling. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Slik konverterer du en forespørsel til en bestilling
Når du har godtatt leverandørtilbudet, kan du konvertere det til en kjøpsfaktura eller ordre for å behandle kjøpet.

1. Åpne en forespørsel som er klar til å konverteres, og velg handlingen **Lag ordre**.

Forespørselen er fjernet fra databasen. Det opprettes en kjøpsfaktura eller bestilling basert på informasjonen i forespørselen der du kan behandle kjøpet. I feltet **Tilbudsnr.** på kjøpsfakturaen eller bestillingen kan du se nummeret på forespørselen den ble laget fra.

## <a name="see-also"></a>Se også
[Innkjøp](purchasing-manage-purchasing.md)  
[Definere kjøp](purchasing-setup-purchasing.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

