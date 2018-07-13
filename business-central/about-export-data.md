---
title: Eksportere Business Central-dataene til Excel | Microsoft-dokumentasjon
description: "Du kan eksportere finansrapporter og forretningsintelligensdata fra Business Central til Excel, eller du kan åpne Business Central-dataene i Excel."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 3bd7442582fe13809ea04d1f298b7aecbf9b45ed
ms.contentlocale: nb-no
ms.lasthandoff: 06/01/2018

---
# <a name="exporting-your-business-data-to-excel"></a>Eksportere forretningsdataene til Excel
Hvis du vil arbeide med dataene fra [!INCLUDE[d365fin](includes/d365fin_md.md)] i Excel, kan du åpne alle lister i Excel og arbeide med dem der. På samme måte, hvis du vil avbryte abonnementet på [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du eksportere dataene til Excel, slik at du kan ta dem med deg.

## <a name="opening-lists-in-excel"></a>Åpne lister i Excel
Du kan åpne data i Excel fra alle alle journaler, lister eller forslag. Du bare åpner siden som du ønsker, og deretter velger du **Åpne i Excel**. Åpne for eksempel en oversikt over kunder (Søk etter **kunder**), og velg deretter **Åpne i Excel**. Nettleseren ber deg om å åpne eller lagre Microsoft Excel-arbeidsboken som er generert.  

Hver liste inneholder flere kolonner, og eksport til Excel vil inkludere alle kolonner som er i den gjeldende visningen. Hvis du vil legge til eller fjerne kolonner før du åpner listen i Excel, kan du ganske enkelt åpne hurtigmenyen for en kolonne og deretter angir du hvilke kolonner du vil vise. Denne listen over kolonner er forskjellig for de fleste lister, og den reflekterer strukturen i databasen der dataene er lagret. Hvis du ikke er sikker på hvilken type data som inneholder en bestemt kolonne, kan du legge den til din visning og deretter bestemmer deg for om du vil fjerne den på nytt.  

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
[Finans](finance.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

