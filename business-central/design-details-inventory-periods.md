---
title: Designdetaljer – Lagerperioder | Microsoft-dokumentasjon
description: Tilbakedaterte transaksjoner eller kostnadsjusteringer påvirker ofte saldoer og lagerverdier for regnskapsperioder som kan anses som avsluttet. Dette kan ha en negativ virkning på nøyaktig rapportering, særlig i globale selskaper. Du kan bruke Lagerperioder-funksjonen til å unngå slike problemer, ved å åpne eller lukke lagerperioder for å begrense bokføring i en angitt tidsperiode.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0e58b0711433c656907704d614d90f78b5d57579
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "936439"
---
# <a name="design-details-inventory-periods"></a>Designdetaljer: Beholdningsperioder
Tilbakedaterte transaksjoner eller kostnadsjusteringer påvirker ofte saldoer og lagerverdier for regnskapsperioder som kan anses som avsluttet. Dette kan ha en negativ virkning på nøyaktig rapportering, særlig i globale selskaper. Du kan bruke Lagerperioder-funksjonen til å unngå slike problemer, ved å åpne eller lukke lagerperioder for å begrense bokføring i en angitt tidsperiode.  

 En lagerperiode er en bestemt periode, angitt av en sluttdato, der du bokfører lagertransaksjoner. Når du lukker en lagerperiode, kan ingen verdiendringer bokføres i den lukkede periode. Dette omfatter nye verdibokføringer, forventede eller fakturerte bokføringer, endring av eksisterende verdier og kostjusteringer. Du kan imidlertid framdels bruke på en åpen varepost som er i en lukket periode. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Vareutligning](design-details-item-application.md).  

 For å sikre at alle transaksjonsposter i en lukket periode er endelige, må følgende betingelser oppfylles før en lagerperiode kan lukkes:  

-   Alle utgående vareposter i perioden må avsluttes (ingen negativ beholdning).  
-   Alle varekostnader i perioden må justeres.  
-   Alle frigitte og ferdige produksjonsordrer i perioden må kostnadsjusteres.  

 Når du lukker en lagerperiode, opprettes en lagerperiode ved hjelp av nummeret på den siste varejournalen i lagerperioden. I tillegg registreres klokkeslett, dato og brukerkode i lagerperiodeposten for brukeren som lukker perioden. Ved hjelp av denne informasjonen med siste varejournalen for forrige periode, kan du se hvilke lagertransaksjonene som bokført i lagerperioden. Det er også mulig å åpne lagerperioder på nytt hvis du må bokføre i en lukket periode. Når du åpner en lagerperiode på nytt, blir det opprettet en lagerperiodepost.  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md) [Administrere lagerkostnader](finance-manage-inventory-costs.md) [Finans](finance.md)  
 [Arbeide med Business Central](ui-work-product.md)
