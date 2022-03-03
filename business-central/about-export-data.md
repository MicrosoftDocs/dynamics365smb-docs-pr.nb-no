---
title: Eksporter Business Central-dataene til Excel
description: Du kan eksportere finansrapporter og forretningsintelligensdata fra Business Central til Excel, eller du kan åpne Business Central-dataene i Excel.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.search.form: 9901, 9018, 9020, 9022, 9027
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3161c51160790b2fcc4e702866025e501167b644
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335607"
---
# <a name="exporting-your-business-data-to-excel"></a>Eksportere forretningsdataene til Excel
Hvis du vil arbeide med dataene fra [!INCLUDE[prod_short](includes/prod_short.md)] i Excel, kan du åpne alle lister i Excel og arbeide med dem der. På samme måte, hvis du vil avbryte abonnementet på [!INCLUDE[prod_short](includes/prod_short.md)], kan du eksportere dataene til Excel, slik at du kan ta dem med deg.

## <a name="opening-lists-in-excel"></a>Åpne lister i Excel
Du kan åpne data i Excel fra alle alle journaler, lister eller forslag. Du bare åpner siden som du ønsker, og deretter velger du **Åpne i Excel**. Åpne for eksempel en oversikt over kunder (Søk etter **kunder**), og velg deretter **Åpne i Excel**. Nettleseren ber deg om å åpne eller lagre Microsoft Excel-arbeidsboken som er generert.  

> [!NOTE]
> Bruk dette alternativet hvis du ikke vil endre og publisere disse endringene til [!INCLUDE[prod_short](includes/prod_short.md)].  

Hver liste inneholder flere kolonner, og eksport til Excel vil inkludere alle kolonner som er i den gjeldende visningen. Hvis du vil legge til eller fjerne kolonner før du åpner listen i Excel, kan du ganske enkelt åpne hurtigmenyen for en kolonne og deretter angir du hvilke kolonner du vil vise. Denne listen over kolonner er forskjellig for de fleste lister, og den reflekterer strukturen i databasen der dataene er lagret. Hvis du ikke er sikker på hvilken type data som inneholder en bestemt kolonne, kan du legge den til din visning og deretter bestemmer deg for om du vil fjerne den på nytt.  

### <a name="edit-data-in-excel"></a>Rediger data i Excel
[!INCLUDE[prod_short](includes/prod_short.md)]-opplevelsen inneholder et tillegg til Excel, slik at du kan redigere data i Excel. Hvis du vil ha mer informasjon, se [Analyser årsregnskap i Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Eksportere data til andre økonomisystemer
Hvis du vil avbryte abonnementet på [!INCLUDE[prod_short](includes/prod_short.md)], kan du eksportere dataene til Excel, slik at du kan ta dem med deg til det neste økonomisystemet.  

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
> Hvis du har definert mer enn ett selskap i [!INCLUDE[prod_short](includes/prod_short.md)], må du eksportere de relevante dataene fra hvert selskap.

> [!NOTE]
> Du må ha minst én av følgende tillatelser for å åpne eller redigere data i Excel:
>    - Tillatelsessett *D365 Excel-eksporthandling*  
>    - Systemtillatelse 6110 *Tillat handlingseksport til Excel*.  

Hvis du vil ha mer informasjon, kan du se [For å få en oversikt over en brukers tillatelser](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Avbryte abonnementet på [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Analysere årsregnskap i Microsoft Excel](finance-analyze-excel.md)  
[Finans](finance.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]