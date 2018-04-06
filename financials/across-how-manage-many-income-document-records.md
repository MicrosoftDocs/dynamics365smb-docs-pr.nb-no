---
title: "Definere hvilke inngående dokumenter som skal vises | Microsoft-dokumentasjon"
description: "Du kan justere standardvisningen for inngående dokumenter, for eksempel e-fakturaer, for å få bedre oversikt over behandlede og ubehandlede poster."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2016
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 65f3c14b29a5fcf7f855d7ea183445cf2fc1bd95
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="manage-many-incoming-document-records"></a>Håndtere mange inngående dokumentposter
Når du oppretter eller behandle inngående dokumentposter, kan antall linjer i vinduet **Inngående dokumenter** øke så mye at du mister oversikten. Derfor kan du sette inngående dokumentposter til Behandlet for å fjerne dem fra standardvisningen. Når du velger handlingen **Vis alle**, kan du vise både behandlede og ubehandlede poster.

> [!NOTE]  
>   Du kan ikke redigere informasjon, legge ved filer eller utføre andre prosesser på inngående dokumentposter som er satt til Behandlet. Først må du sette det til Ubehandlet.

Det merkes automatisk av for **Behandlet** på inngående dokumentposter som har blitt behandlet, men du kan også merke av for eller fjerne merket manuelt. Avhengig av forretningsprosessen, kan en inngående dokumentpost behandles når et relatert dokument er opprettet for det eller en fil er tilknyttet.

> [!NOTE]  
>   Når du åpner vinduet **Inngående dokumenter** med handlingen **Mine inngående dokumenter** i rollesenteret, vises bare ubehandlede inngående dokumentposter som standard. I dette emnet kalles dette "standardvisningen".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Fjerne inngående dokumentposter fra standardvisningen
1. I vinduet **Inngående dokumenter** velger du én eller flere linjer for inngående dokumentposter som du vil fjerne fra standardvisning.
2. Velg handlingen **Satt til Behandlet**.

    Inngående dokumentposter fjernes fra standardvisningen, og det merkes av for **Behandlet** på linjene.

> [!NOTE]  
>   Du kan også utføre denne handlingen for hver enkelt post i vinduet **Kort for inngående dokument**.

## <a name="to-view-all-incoming-document-records"></a>Vise alle inngående dokumentposter
1. I vinduet **Inngående dokumenter** velger du handlingen **Vis alle**.

Alle inngående dokumentposter vises, inkludert dem som det ikke er merket av for **Behandlet**.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Legge til inngående dokumentposter i standardvisningen
1. I vinduet **Inngående dokumenter** velger du handlingen **Vis alle**.
2. Velg én eller flere linjer for inngående dokumentposter som du vil skal vises i standardvisningen.
3. Velg handlingen **Satt til Ubehandlet**.  

> [!NOTE]  
>   Du kan også utføre denne handlingen for hver enkelt post i vinduet **Kort for inngående dokument**.

## <a name="see-also"></a>Se også
[Behandle inngående dokumenter](across-process-income-documents.md)  
[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

