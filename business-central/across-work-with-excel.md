---
title: Vise og redigere i Excel fra Business Central | Microsoft-dokumenter
description: Lær om hvordan du åpner sidene i Microsoft Excel fra Business Central for bedre dataanalyser.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 68139f258595bcca2658e394a4251e30dfbe6510
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "925043"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Vise og redigere i Excel fra Business Central 

Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også vise poster ved hjelp av Microsoft Excel. Du har to alternative måter å gjøre dette på. Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden. Forskjellene mellom de to handlingen er følgende:  

## <a name="open-in-excel"></a>Åpne i Excel

-    Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises. Dette betyr at Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prodshort](includes/prodshort.md)].

-    Du kan gjøre endringer i postene i Excel, men du kan ikke publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)]. Du kan bare lagre endringene til Excel-filen på datamaskinen din. 

-    Denne handlingen fungerer både i Windows- og macOS. 

>[!NOTE]
>For lokal [!INCLUDE[prodshort](includes/prodshort.md)] er **Åpne i Excel**-handlingen ikke tilgjengelig hvis **Rediger i Excel**-handlingen er tilgjengelig.

## <a name="edit-in-excel"></a>Rediger i Excel

-    Med denne handlingen respekterer ikke Excel-arbeidsboken filtre på siden som avgrenser postene som vises. Dette betyr at Excel-arbeidsboken inneholder alle tilgjengelige poster og kolonner, uavhengig av hva som vises på siden. 

-    Fordelen med **Rediger i Excel**-handlingen er at den lar deg gjøre endringer i poster i Excel og deretter publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].

-    Den fungerer bare i Windows, ikke i macOS.

>[!NOTE]
>For lokal [!INCLUDE[prodshort](includes/prodshort.md)] er **Rediger i Excel**-handlingen bare tilgjengelig hvis Excel-tillegget er installert av systemansvarlig. For administratorer, hvis du vil vite hvordan du installerer Excel-tilleggskomponenten, se [Definere Excel-tillegget](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Se forskjellene mellom alternativene 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a>Se også
[Arbeide med Business Central](ui-work-product.md)  
