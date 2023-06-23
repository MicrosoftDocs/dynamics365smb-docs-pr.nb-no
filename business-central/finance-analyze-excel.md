---
title: Arbeide med økonomiske oversikter i Excel
description: Lær om hvordan du åpner regnskapene i Microsoft Excel fra Business Central for bedre analyser.
author: edupont04
ms.topic: overview
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: 9027
ms.date: 08/23/2022
ms.author: edupont
---
# <a name="analyzing-financial-statements-in-microsoft-excel" />Analysere årsregnskap i Microsoft Excel

[!INCLUDE [prod_short](includes/prod_short.md)] gir KPI-er og får oversikt over firmaets økonomi. Følgende er eksempler på hvordan du kan analysere KPI-er og oversikter i Excel:

* Åpne lister i Excel og analyser dataene. 
* Eksporter tunge årsregnskap, for eksempel balansen eller resultatregnskapet til Excel, analysere data og skrive ut rapportene.  

> [!TIP]
> Som standard er rapportene du kan vise i Excel, utformet for å hjelpe deg med å analysere inneværende år. Rapporten Resultatregnskap er imidlertid et unntak. Med denne rapporten kan du filtrere dataene slik at de omfatter tidligere år i analysene.

## <a name="getting-the-overview-and-the-details-in-excel" />Få oversikten og detaljene i Excel

I rollesentrene for forretningsleder og regnskapsfører får kan du velg årsregnskaper du vil vise i Excel, med handlingen **Rapporter**. Når du velger et regnskap, åpnes det i Excel eller Excel Online. Et tillegg kobler dataene til [!INCLUDE [prod_short](includes/prod_short.md)]. Du må imidlertid logge på med den samme kontoen som du bruker med [!INCLUDE [prod_short](includes/prod_short.md)]. Tabellen nedenfor inneholder en oversikt over rapportene og hvor de er tilgjengelige.  


|Rapporter  |Rollesenter  |
|---------|---------|
|Balanse                 | Forretningsleder, revisor |
|Resultatregnskap              | Forretningsleder, revisor |
|Kontantstrømutdrag       | Forretningsleder, revisor |
|Kontoutdrag for fri egenkapital| Forretningsleder, revisor |
|Salgsmva. innkrvd – ikke Norge         | Forretningsleder, revisor |
|Kontoutdrag           | Forretningsleder, revisor |
|Aldersfordelt saldoliste – leverandør         | Revisor |
|Aldersfordelt saldoliste – kunde      | Revisor |

La oss si at du vil se nærmere på kontantstrømmen din. Du kan åpne **Kontantstrømutdrag**-rapporten i Excel fra firma lederen eller regnskapsføreren rollesenter, men hva som skjer faktisk er vi eksportere dataene relevante for deg, og oppretter en Excel-arbeidsbok basert på en forhåndsdefinert mal. Avhengig av webleseren må du kanskje skal åpnes eller lagres arbeidsboken.  

I Excel ser du en fane der dataene er ordnet du første forslaget. Data som ble eksportert finnes også i andre forslagene, i tilfelle du trenger den. Du kan skrive ut rapporten én gang, eller du kan endre den til du har oversikten, og du vil ha detaljer. Bruk [!INCLUDE [prod_short](includes/prod_short.md)] Excel-tillegget til å filtrere og analysere dataene.  

### <a name="understanding-the-excel-templates" />Forstå Excel-malene

De forhåndsdefinerte Excel-rapportene er basert på dataene i det gjeldende firmaet. Demonstrasjonsselskapet har for eksempel definert kontoplanen til å vise tre kontantkontoer under *Omløpsmidler*: 10100 **sjekkonto**, 10200 **sparekonto** og 10300 **håndkasse**. Kontoene har feltet **Kontounderkategori** satt til *Kontanter*, og det er det kombinerte beløpet som vises som *Kontanter* i Excel-rapporten **Balanse**.  

Andre ark i Excel-arbeidsboken viser dataene bak rapporten. Du må kanskje filtrere listene i [!INCLUDE [prod_short](includes/prod_short.md)] for å finne ut hva som er bak grupperingene i Excel-rapportene.  

## <a name="the-include-prodshortincludesprodshortmd-excel-add-in" />[!INCLUDE [prod_short](includes/prod_short.md)] Excel-tillegget

Din [!INCLUDE [prod_short](includes/prod_short.md)]-opplevelse inneholder et tillegg til Excel. Avhengig av abonnementet er du logget på automatisk, eller du må angi samme påloggingsinformasjon for [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Vise og redigere i Excel fra Business Central](across-work-with-excel.md).  

Med tillegget kan du få ferske data fra [!INCLUDE [prod_short](includes/prod_short.md)], og du kan overføre endringer tilbake til [!INCLUDE [prod_short](includes/prod_short.md)]. Muligheten til å legge inn data tilbake til databasen er ikke tilgjengelig for årsregnskap du kan vise i Excel.  

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex" />Se relatert [Microsoft-opplæring](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Se også

[Vise og redigere i Excel fra Business Central](across-work-with-excel.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeid med Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
