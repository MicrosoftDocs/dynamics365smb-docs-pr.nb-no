---
title: Arbeide med økonomiske oversikter i Excel
description: Lær om hvordan du åpner regnskapene i Microsoft Excel fra Business Central for bedre analyser.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 53221cbacb35e7e82077295a6f7098f07c2b02e6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913474"
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Analysere årsregnskap i Microsoft Excel

I [!INCLUDE [prodshort](includes/prodshort.md)] kan du se ytelsesindikatorer og få en oversikt over selskapets økonomiske tilstand. Du kan også åpne lister i Excel og analysere dataene der. Men du kan også eksportere tunge årsregnskap, for eksempel balansen eller resultatregnskapet til Excel, analysere data og skrive ut rapportene.  

I rollesentrene for forretningsleder og regnskapsfører kan du velge hvilke årsregnskap som skal vises i Excel, fra en rullegardinmeny i Rapporter-delen på båndet. Når du velger et regnskap, åpnes det i Excel eller Excel Online. Et tillegg kobler dataene til [!INCLUDE [prodshort](includes/prodshort.md)]. Du må imidlertid logge på med den samme kontoen som du bruker med [!INCLUDE [prodshort](includes/prodshort.md)].  

## <a name="getting-the-overview-and-the-details-in-excel"></a>Få oversikten og detaljene i Excel

Velg den aktuelle Excel-rapporten på båndet, og la den åpne slik at du får oversikten du søker etter. I denne versjonen av [!INCLUDE [prodshort](includes/prodshort.md)] tilbyr vi følgende Excel-rapporter:

- Balanse  
- Resultatregnskap  
- Kontantstrømutdrag  
- Kontoutdrag for fri egenkapital  
- Aldersfordelt saldoliste - leverandør  
- Aldersford. saldoliste - kunde  

La oss si at du vil se nærmere på kontantstrømmen din. Du kan åpne **Kontantstrømutdrag**-rapporten i Excel fra firma lederen eller regnskapsføreren rollesenter, men hva som skjer faktisk er vi eksportere dataene relevante for deg, og oppretter en Excel-arbeidsbok basert på en forhåndsdefinert mal. Avhengig av webleseren må du kanskje skal åpnes eller lagres arbeidsboken.  

I Excel ser du en fane der dataene er ordnet du første forslaget. Data som ble eksportert finnes også i andre forslagene, i tilfelle du trenger den. Du kan skrive ut rapporten én gang, eller du kan endre den til du har oversikten, og du vil ha detaljer. Bruk [!INCLUDE [prodshort](includes/prodshort.md)] Excel-tillegget til å filtrere og analysere dataene.  

### <a name="understanding-the-excel-templates"></a>Forstå Excel-malene

De forhåndsdefinerte Excel-rapportene er basert på dataene i det gjeldende firmaet. Demonstrasjonsselskapet har for eksempel definert kontoplanen til å vise tre kontantkontoer under *Omløpsmidler*: 10100 **sjekkonto**, 10200 **sparekonto** og 10300 **håndkasse**. Kontoene har feltet **Kontounderkategori** satt til *Kontanter*, og det er det kombinerte beløpet som vises som *Kontanter* i Excel-rapporten **Balanse**.  

Flere ark i Excel-arbeidsboken viser dataene bak rapporten. Hvis du vil finne ut hva som skjules bak grupperingene i Excel-rapportene, kan det for eksempel hende du må gå tilbake til [!INCLUDE [prodshort](includes/prodshort.md)] og bruke filtre på listene.  

## <a name="the-prodshort-excel-add-in"></a>[!INCLUDE [prodshort](includes/prodshort.md)] Excel-tillegget

Din [!INCLUDE [prodshort](includes/prodshort.md)]-opplevelse inneholder et tillegg til Excel. Avhengig av abonnementet er du logget på automatisk, eller du må angi samme pålogging som du bruker for [!INCLUDE [prodshort](includes/prodshort.md)]. Hvis du vil ha mer informasjon, kan du se [Vise og redigere i Excel fra Business Central](across-work-with-excel.md).  

Med tillegget kan du få ferske data fra [!INCLUDE [prodshort](includes/prodshort.md)], og du kan overføre endringer i [!INCLUDE [prodshort](includes/prodshort.md)]. Muligheten til å legge inn data tilbake til databasen deaktiveres imidlertid for Excel-årsregnskap i listen ovenfor.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Vise og redigere i Excel fra Business Central](across-work-with-excel.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med Business Central](ui-work-product.md)  
