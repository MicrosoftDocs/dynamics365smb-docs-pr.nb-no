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
ms.date: 10/24/2019
ms.author: jswymer
ms.openlocfilehash: 99fe339426b755b70983d8ec9345858357043347
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808748"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Vise og redigere i Excel fra Business Central

Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også vise poster ved hjelp av Microsoft Excel. Du har to alternative måter å gjøre dette på. Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden. Forskjellene mellom de to handlingen er følgende:  

## <a name="open-in-excel"></a>Åpne i Excel

- Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises. Dette betyr at Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prodshort](includes/prodshort.md)].

- Du kan gjøre endringer i postene i Excel, men du kan ikke publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)]. Du kan bare lagre endringene til Excel-filen på datamaskinen din. 

- Denne handlingen fungerer både i Windows- og macOS. 

> [!NOTE]
> For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt er handlingen **Åpne i Excel** tilgjengelig som standard. Hvis du konfigurerer [!INCLUDE [prodshort](includes/prodshort.md)] lokalt for redigering av data i Excel, erstattes handlingen **Åpne i Excel** med handlingen **Rediger i Excel**.

## <a name="edit-in-excel"></a>Rediger i Excel

- Med denne handlingen respekterer Excel de fleste filtre på siden som avgrenser postene som vises. Dette betyr at Excel-arbeidsboken inneholder nesten de samme postene og kolonnene.

- Fordelen med **Rediger i Excel**-handlingen er at den lar deg gjøre endringer i poster i Excel og deretter publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].

- Den fungerer bare i Windows, ikke i macOS.

Dette ble forbedret i 2019 Release Wave 2. Hvis du vil ha mer informasjon, se [Forbedringer i Excel-integrasjon](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).

> [!NOTE]
> For lokal [!INCLUDE[prodshort](includes/prodshort.md)] er **Rediger i Excel**-handlingen bare tilgjengelig hvis Excel-tillegget er konfigurert av systemansvarlig. For administratorer, hvis du vil vite hvordan du installerer Excel-tilleggskomponenten, se [Definere Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt er denne funksjonen bare tilgjengelig for webklienten.

### <a name="see-the-differences-between-the-options"></a>Se forskjellene mellom alternativene 
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a>Se også
[Arbeide med Business Central](ui-work-product.md)  
