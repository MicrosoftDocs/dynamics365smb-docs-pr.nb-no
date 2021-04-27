---
title: Opprette en forespørsel for å be om et tilbud | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter et tilbud eller et tilbudsforespørselsdokument for å registrere tilbudet til en kunde og selge produkter under visse betingelser.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 416c5a4e4376932c16a1496f2db2b0c79307d22b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772622"
---
# <a name="request-quotes"></a>Be om tilbud
En forespørsel kan brukes som et foreløpig utkast til en bestilling, og bestillingen kan deretter konverteres til en bestilling eller ordre.


## <a name="to-create-a-purchase-quote"></a>Slik oppretter du en forespørsel
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forespørsler**, og velg deretter den relaterte koblingen.
2. Opprett et nytt dokument, på samme måte som du oppretter en bestilling. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Slik konverterer du en forespørsel til en bestilling
Når du har godtatt leverandørtilbudet, kan du konvertere det til en kjøpsfaktura eller ordre for å behandle kjøpet.

1. Åpne en forespørsel som er klar til å konverteres, og velg handlingen **Lag ordre**.

Forespørselen er fjernet fra databasen. Det opprettes en kjøpsfaktura eller bestilling basert på informasjonen i forespørselen der du kan behandle kjøpet. I feltet **Tilbudsnr.** på kjøpsfakturaen eller bestillingen kan du se nummeret på forespørselen den ble laget fra.

## <a name="see-also"></a>Se også
[Innkjøp](purchasing-manage-purchasing.md)  
[Definere kjøp](purchasing-setup-purchasing.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]