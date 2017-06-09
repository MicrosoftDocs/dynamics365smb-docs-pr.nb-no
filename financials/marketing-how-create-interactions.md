---
title: "Opprette samhandlinger på kontakter og segmenter | Microsoft-dokumentasjon"
description: "Beskriver hvordan du oppretter samhandlinger på kontakter og segmenter i Financials."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b50d332441bee01158559616fff5d5f5ca381a90
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-create-interactions-on-contacts-and-segments"></a>Opprette samhandlinger på kontakter og segmenter
Du kan opprette samhandlinger hvis du vil registrere all samhandling og kommunikasjon med kontaktene og segmentene, for eksempel utsendinger.

Før du kan opprette samhandlinger, må du definere samhandlingsmaler. Hvis du vil ha mer informasjon, kan du se [Definere samhandlingsmaler](marketing-interactions.md#set-up-interaction-templates).

## <a name="to-create-an-interaction"></a>Slik oppretter du en samhandling
1. Åpne kontakt-, selger- eller samhandlingsposten.
2. Velg handlingen **Opprett samhandling**.
3. Fyll ut feltene, og velg **OK**-knappen.

**Merk**: Hvis du må utføre en annen oppgave før du fullfører samhandlingen, kan du velge **Avbryt** og velge å fullføre samhandling på et senere tidspunkt. Dette utsetter samhandlingen.

## <a name="to-finish-and-delete-postponed-interactions"></a>Fullføre og slette utsatte samhandlinger
1. Åpne kontakt-, selger- eller samhandlingsposten.
2. Velg **Utsatte samhandlinger**.
3. Velg samhandlingen du vil fullføre, og velg deretter handlingen **Fortsett**.

## <a name="to-create-an-interaction-on-a-segment"></a>Opprette en samhandling på et segment
1. På hjemmesiden velger du **Aktive segmenter**, eller i øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Segmenter**, og deretter velger du den beslektede koblingen.
2. Fyll ut feltene i inndelingen **Samhandling** i **Segment**-vinduet for å angi hvilken samhandling du vil tilordne segmentet.

    Etter at du har tilordnet en samhandling til segmentet, kan du tilpasse samhandlingen for hver enkelt kontakt i segmentet, for eksempel ved å velge en annen samhandlingsmal på linjene i vinduet **Segment**.  
3. Hvis du vil loggføre segmentet og samhandlinger, velger du handlingen **Logg**. **Loggfør segment**-vinduet åpnes.
4. Hvis du vil opprette et nytt segment som inneholder de samme kontaktene, merker du av for **Opprett oppfølgingssegment**. Du må ha angitt nummerserier for segmenter i vinduet **Markedsføringsoppsett** for å opprette et oppfølgingssegment.

En samhandling registreres for hver kontakt i segmentet i tabellen **Samhandlingspost**, og segmentet loggføres. Du finner loggførte segmenter i vinduet **Loggførte segmenter**.

Hvis du har merket av for **Opprett oppfølgingssegment**, opprettes et nytt segment som inneholder de samme kontaktene som segmentet du nettopp loggførte.

## <a name="see-also"></a>Se også
[Registrere samhandlinger](marketing-interactions.md)  
[Administrere kontakter](marketing-contacts.md)  
[Håndtere salgsmuligheter](marketing-manage-sales-opportunities.md)  
[Sette opp forbindelser](marketing-setup-marketing.md)  
[Arbeide med Financials](ui-work-product.md)

