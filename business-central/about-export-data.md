---
title: Eksporter Business Central-dataene til Excel
description: 'Du kan eksportere finansrapporter og forretningsintelligensdata fra Business Central til Excel, eller du kan åpne dataene i Excel.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'analysis, reporting, financial report, business intelligence, BI, Excel'
ms.search.form: 9901
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="export-your-business-data-to-excel"></a>Eksporter forretningsdataene til Excel

Excel er et kraftig verktøy når du skal arbeide med data. I [!INCLUDE[prod_short](includes/prod_short.md)] kan du åpne alle lister i Excel. Du kan til og med endre data i Excel og deretter sende dem tilbake til [!INCLUDE [prod_short](includes/prod_short.md)]. Samme funksjon gjør det enkelt for deg å ta med deg dataene hvis du bestemmer deg for å avslutte abonnementet.

## <a name="opening-lists-in-excel"></a>Åpne lister i Excel

Du kan åpne data i Excel fra alle alle journaler, lister eller forslag. Du bare åpner siden som du ønsker, og deretter velger du **Åpne i Excel**. Åpne for eksempel en oversikt over kunder (Søk etter **kunder**), og velg deretter **Åpne i Excel**. Nettleseren ber deg om å åpne eller lagre Microsoft Excel-arbeidsboken som er generert.  

> [!NOTE]
> Bruk dette alternativet hvis du ikke vil endre og publisere disse endringene til [!INCLUDE[prod_short](includes/prod_short.md)].  

Hver liste inneholder noen kolonner. Eksporten til Excel inkluderer alle kolonner i nåværende visning. Endre kolonnene ved å åpne hurtigmenyen for en kolonne, og angi deretter hvilke kolonner du vil vise. Listen med kolonner er forskjellig for de fleste lister. Kolonnene gjenspeiler strukturen i databasen som lagrer dataene. Hvis du ikke er sikker på hvilken datatype en bestemt kolonne inneholder, legger du den til i visningen. Du kan alltids fjerne den igjen.  

### <a name="edit-data-in-excel"></a>Rediger data i Excel

[!INCLUDE[prod_short](includes/prod_short.md)]-opplevelsen inneholder et tillegg til Excel, slik at du kan redigere data i Excel. Hvis du vil ha mer informasjon, se [Analyser årsregnskap i Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Eksportere data til andre økonomisystemer

Hvis du vil avbryte abonnementet på [!INCLUDE[prod_short](includes/prod_short.md)], kan du eksportere dataene til Excel, slik at du kan ta dem med deg til det neste økonomisystemet.  

Du kan eksportere alle sider, men det kan være mer enn det du virkelig trenger. Derfor bør du vurdere å eksportere følgende viktige sider, og husk å legge til alle kolonner som beskrevet tidligere:  

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
>
> * Tillatelsessett *D365 Excel-eksporthandling*  
> * Systemtillatelse 6110 *Tillat handlingseksport til Excel*.  

Hvis du vil ha mer informasjon, kan du se [For å få en oversikt over en brukers tillatelser](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-also"></a>Se også
[Avbryte abonnementet på [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Importer forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Analyser årsregnskap i Microsoft Excel](finance-analyze-excel.md)  
[Finans](finance.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
