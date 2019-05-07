---
title: Eksportere Business Central-dataene til Excel | Microsoft-dokumentasjon
description: Du kan eksportere finansrapporter og forretningsintelligensdata fra Business Central til Excel, eller du kan åpne Business Central-dataene i Excel.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 382bee236225c1038430bb2243c6c54b56ef772e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "935949"
---
# <a name="exporting-your-business-data-to-excel"></a>Eksportere forretningsdataene til Excel
Hvis du vil arbeide med dataene fra [!INCLUDE[d365fin](includes/d365fin_md.md)] i Excel, kan du åpne alle lister i Excel og arbeide med dem der. På samme måte, hvis du vil avbryte abonnementet på [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du eksportere dataene til Excel, slik at du kan ta dem med deg.

## <a name="opening-lists-in-excel"></a>Åpne lister i Excel
Du kan åpne data i Excel fra alle alle journaler, lister eller forslag. Du bare åpner siden som du ønsker, og deretter velger du **Åpne i Excel**. Åpne for eksempel en oversikt over kunder (Søk etter **kunder**), og velg deretter **Åpne i Excel**. Nettleseren ber deg om å åpne eller lagre Microsoft Excel-arbeidsboken som er generert.  

> [!NOTE]
> Bruk dette alternativet hvis du ikke vil endre og publisere disse endringene til [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Hver liste inneholder flere kolonner, og eksport til Excel vil inkludere alle kolonner som er i den gjeldende visningen. Hvis du vil legge til eller fjerne kolonner før du åpner listen i Excel, kan du ganske enkelt åpne hurtigmenyen for en kolonne og deretter angir du hvilke kolonner du vil vise. Denne listen over kolonner er forskjellig for de fleste lister, og den reflekterer strukturen i databasen der dataene er lagret. Hvis du ikke er sikker på hvilken type data som inneholder en bestemt kolonne, kan du legge den til din visning og deretter bestemmer deg for om du vil fjerne den på nytt.  

### <a name="edit-data-in-excel"></a>Rediger data i Excel
[!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen inneholder et tillegg til Excel, slik at du kan redigere data i Excel. Hvis du vil ha mer informasjon, se [Analyser årsregnskap i Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Eksportere data til andre økonomisystemer
Hvis du vil avbryte abonnementet på [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du eksportere dataene til Excel, slik at du kan ta dem med deg til det neste økonomisystemet.  

Du kan eksportere alle sider, selvsagt, men det kan være mer enn det du virkelig trenger. Derfor bør du vurdere å eksportere følgende viktige sider, og husk å legge til alle kolonner som beskrevet tidligere:  

* Kontoplan  
* Kunder  
* Leverandører  
* Banker  
* Varer  

Hvis du ønsker alle finansielle transaksjoner også, er dette en stor mengde data, slik at eksporten vil ofte ta mer enn et par minutter av tid. Økonomiske transaksjoner vises på siden **Finansposter**.  

Vi anbefaler at du også vurdere å eksportere dataene fra de følgende sidene:  

* Kundeposter  
* Leverandørposter  
* Bankkontoposter  
* Vareposter  
* Generelt bokføringsoppsett  
* Bokføringsgrupper - kunde  
* Bokføringsgrupper - leverandør  
* Bokføringsgrupper - varer  
* Bokføringsgruppe - bank  
* Finansbudsjetter  
* Budsjettposter  
* Tilbud  
* Salgsfakturaer  
* Kjøpsfakturaer  
* Kontakter  
* Selgere  

> [!NOTE]  
>   Hvis du har definert mer enn ett selskap i [!INCLUDE[d365fin](includes/d365fin_md.md)], må du eksportere de relevante dataene fra hvert selskap.

## <a name="see-also"></a>Se også
[Avbryte abonnementet på [!INCLUDE[d365fin](includes/d365fin_md.md)]](admin-cancel.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Analysere årsregnskap i Microsoft Excel](finance-analyze-excel.md)  
[Finans](finance.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
