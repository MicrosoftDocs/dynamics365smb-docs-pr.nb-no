---
title: Opprette samhandlinger på kontakter og segmenter | Microsoft-dokumentasjon
description: Beskriver hvordan du kan opprette samhandlinger for kommunikasjon du har med kontaktene og segmentene i Business Central, for eksempel direktereklame.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: c4726fa1550687a768b7340bba202617a052586d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "918658"
---
# <a name="create-interactions-on-contacts-and-segments"></a>Opprette samhandlinger på kontakter og segmenter
Du kan opprette samhandlinger hvis du vil registrere all samhandling og kommunikasjon med kontaktene og segmentene, for eksempel utsendinger.

Før du kan opprette samhandlinger, må du definere samhandlingsmaler. Hvis du vil ha mer informasjon, kan du se [Definere samhandlingsmaler](marketing-interactions.md).

## <a name="to-create-an-interaction"></a>Slik oppretter du en samhandling
1. Åpne kontakt-, selger- eller samhandlingsposten.
2. Velg handlingen **Opprett samhandling**.
3. Fyll ut feltene, og klikk deretter **OK**.

> [!NOTE]  
>   Hvis du må utføre en annen oppgave før du fullfører samhandlingen, kan du velge **Avbryt** og deretter velge å fullføre samhandlingen på et senere tidspunkt. Dette utsetter samhandlingen.

## <a name="to-finish-and-delete-postponed-interactions"></a>Fullføre og slette utsatte samhandlinger
1. Åpne kontakt-, selger- eller samhandlingsposten.
2. Velg **Utsatte samhandlinger**.
3. Velg samhandlingen du vil fullføre, og velg deretter handlingen **Fortsett**.

## <a name="to-create-an-interaction-on-a-segment"></a>Opprette en samhandling på et segment
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Segmenter**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene i inndelingen **Samhandling** på **Segment**-siden for å angi hvilken samhandling du vil tilordne segmentet.

    Etter at du har tilordnet en samhandling til segmentet, kan du tilpasse samhandlingen for hver enkelt kontakt i segmentet, for eksempel ved å velge en annen samhandlingsmal på linjene på siden **Segment**.  
3. Hvis du vil loggføre segmentet og samhandlinger, velger du handlingen **Logg**. **Loggfør segment**-siden åpnes.
4. Hvis du vil opprette et nytt segment som inneholder de samme kontaktene, merker du av for **Opprett oppfølgingssegment**. Du må ha angitt nummerserier for segmenter på siden **Markedsføringsoppsett** for å opprette et oppfølgingssegment.

En samhandling registreres for hver kontakt i segmentet i tabellen **Samhandlingspost**, og segmentet loggføres. Du finner loggførte segmenter på siden **Loggførte segmenter**.

Hvis du har merket av for **Opprett oppfølgingssegment**, opprettes et nytt segment som inneholder de samme kontaktene som segmentet du nettopp loggførte.

## <a name="see-also"></a>Se også
[Registrere samhandlinger](marketing-interactions.md)  
[Administrere kontakter](marketing-contacts.md)  
[Håndtere salgsmuligheter](marketing-manage-sales-opportunities.md)  
[Arbeide med Business Central](ui-work-product.md)
