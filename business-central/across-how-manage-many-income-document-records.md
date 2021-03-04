---
title: Definere hvilke inngående dokumenter som skal vises | Microsoft-dokumentasjon
description: Du kan justere standardvisningen for inngående dokumenter, for eksempel e-fakturaer, for å få bedre oversikt over behandlede og ubehandlede poster.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6ff52767bbd0a5661cad2dd80abb20885f3fca6d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754945"
---
# <a name="manage-many-incoming-document-records"></a>Håndtere mange inngående dokumentposter
Når du oppretter eller behandle inngående dokumentposter, kan antall linjer på siden **Inngående dokumenter** øke så mye at du mister oversikten. Derfor kan du sette inngående dokumentposter til Behandlet for å fjerne dem fra standardvisningen. Når du velger handlingen **Vis alle**, kan du vise både behandlede og ubehandlede poster.

> [!NOTE]  
>   Du kan ikke redigere informasjon, legge ved filer eller utføre andre prosesser på inngående dokumentposter som er satt til Behandlet. Først må du sette det til Ubehandlet.

Det merkes automatisk av for **Behandlet** på inngående dokumentposter som har blitt behandlet, men du kan også merke av for eller fjerne merket manuelt. Avhengig av forretningsprosessen, kan en inngående dokumentpost behandles når et relatert dokument er opprettet for det eller en fil er tilknyttet.

> [!NOTE]  
>   Når du åpner siden **Inngående dokumenter** med handlingen **Mine inngående dokumenter** i rollesenteret, vises bare ubehandlede inngående dokumentposter som standard. I dette emnet kalles dette "standardvisningen".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Fjerne inngående dokumentposter fra standardvisningen
1. På siden **Inngående dokumenter** velger du én eller flere linjer for inngående dokumentposter som du vil fjerne fra standardvisning.
2. Velg handlingen **Satt til Behandlet**.

    Inngående dokumentposter fjernes fra standardvisningen, og det merkes av for **Behandlet** på linjene.

> [!NOTE]  
>   Du kan også utføre denne handlingen for hver enkelt post på siden **Kort for inngående dokument**.

## <a name="to-view-all-incoming-document-records"></a>Vise alle inngående dokumentposter
1. På siden **Inngående dokumenter** velger du handlingen **Vis alle**.

Alle inngående dokumentposter vises, inkludert dem som det ikke er merket av for **Behandlet**.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Legge til inngående dokumentposter i standardvisningen
1. På siden **Inngående dokumenter** velger du handlingen **Vis alle**.
2. Velg én eller flere linjer for inngående dokumentposter som du vil skal vises i standardvisningen.
3. Velg handlingen **Satt til Ubehandlet**.  

> [!NOTE]  
>   Du kan også utføre denne handlingen for hver enkelt post på siden **Kort for inngående dokument**.

## <a name="see-also"></a>Se også
[Behandle inngående dokumenter](across-process-income-documents.md)  
[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]