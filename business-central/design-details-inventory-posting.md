---
title: Designdetaljer – Lagerbokføring | Microsoft-dokumentasjon
description: Hver lagertransaksjon, for eksempel et kjøpsmottak eller en følgeseddel, bokfører to postene av forskjellige typer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 71ee3624868f546ec7b45f5177dcc61acc5b7a21
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303402"
---
# <a name="design-details-inventory-posting"></a>Designdetaljer: Lagerbokføring
Hver lagertransaksjon, for eksempel et kjøpsmottak eller en følgeseddel, bokfører to postene av forskjellige typer.  

|Posttype|Beskrivelse|  
|----------------|---------------------------------------|  
|Antall|Gjenspeiler endringen i antallet på lager. Denne informasjonen lagres i vareposter.<br /><br /> Sammen med vareutligningsposter.|  
|Verdi|Gjenspeiler endringen i lagerverdien. Disse opplysningene finnes i verdiposter.<br /><br /> Det kan finnes én eller flere verdiposter for hver varepost eller kapasitetspost.<br /><br /> Hvis du vil ha informasjon om verdiposter for kapasitet som er relatert til bruk av produksjons- eller monteringsressurser, kan du se [Designdetaljer: Bokføre produksjonsordre](design-details-production-order-posting.md).|  

 I forhold til antallsbokføringer finnes det verdiposter for å koble lagerøkning med lagerreduksjon. Dette gjør at kostmotoren kan videresende kostnader fra økninger til tilknyttede reduksjoner, og omvendt. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Vareutligning](design-details-item-application.md).  

 Det opprettes vareposter, verdiposter og vareutligningsposter som et resultat av bokføring av en varekladdelinje, indirekte ved å bokføre en ordrelinje eller direkte på siden Varekladd.  

 Med jevne mellomrom vil verdiposter som opprettes i vareopptellingen, bli bokført til finans for å avstemme de to postene for økonomisk styring. Hvis du vil ha mer informasjon, se [Designdetaljer: Avstemming med konti i Finans](design-details-reconciliation-with-the-general-ledger.md).  

 ![Postflyt ved avstemming av lager med finans](media/design_details_inventory_costing_1_entry_flow.png "Postflyt ved avstemming av lager med finans")  

## <a name="example"></a>Eksempel  
 Følgende eksempel viser hvordan vareposter, verdiposter og vareutligningsposter resulterer i finansposter.  

 Du bokfører en bestilling som mottatt og fakturert for 10 varer med en direkte enhetskost på NOK 7 og en sats for indirekte kostnader på NOK 1. Bokføringsdatoen er 01-01-20. Følgende poster opprettes.  

 **Vareposter**  

|Bokføringsdato|Posttype|Kostbeløp (faktisk)|Antall|Løpenr.|  
|------------------|----------------|----------------------------|--------------|---------------|  
|01.01.20|Kjøp|80,00|10|1|  

 **Verdiposter**  

|Bokføringsdato|Posttype|Kostbeløp (faktisk)|Varepostnr.|Løpenr.|  
|------------------|----------------|----------------------------|---------------------------|---------------|  
|01.01.20|Kjøpspris/prod.kost|70,00|1|1|  
|01.01.20|Indirekte kost|10,00|1|2|  

 **Vareutligningsposter**  

|Løpenr.|Varepostnr.|Inngående vareløpenr.|Utgående vareløpenr.|Antall|  
|---------------|---------------------------|----------------------------|-----------------------------|--------------|  
|1|1|1|0|10|  

 Deretter bokfører du et salg på 10 enheter av varen med posteringsdatoen 15.01.20.  

 **Vareposter**  

|Bokføringsdato|Posttype|Kostbeløp (faktisk)||Antall|Løpenr.|  
|------------------|----------------|----------------------------|-|--------------|---------------|  
|15.01.20|Salg|-80,00||-10|2|  

 **Verdiposter**  

|Bokføringsdato|Posttype|Kostbeløp (faktisk)|Varepostnr.|Løpenr.|  
|------------------|----------------|----------------------------|---------------------------|---------------|  
|15.01.20|Kjøpspris/prod.kost|-80,00|2|3|  

 **Vareutligningsposter**  

|Løpenr.|Varepostnr.|Inngående vareløpenr.|Utgående vareløpenr.|Antall|  
|---------------|---------------------------|----------------------------|-----------------------------|--------------|  
|2|2|1|2|-10|  

 På slutten av en regnskapsperiode, kjører du den satsvise jobben **Bokfør lagerkost i Finans** for å avstemme disse lagertransaksjonene med finans.  

 Hvis du vil ha mer informasjon, se [Designdetaljer: Konti i Finans](design-details-accounts-in-the-general-ledger.md).  

 Tabellene nedenfor viser resultatet av å avstemme lagertransaksjonene med Finans i dette eksemplet.  

 **Verdiposter**  

|Bokføringsdato|Posttype|Kostbeløp (faktisk)|Bokført kost|Varepostnr.|Løpenr.|  
|------------------|----------------|----------------------------|-------------------------|---------------------------|---------------|  
|01.01.20|Kjøpspris/prod.kost|70,00|70,00|1|1|  
|01.01.20|Indirekte kost|10,00|10,00|1|2|  
|15.01.20|Kjøpspris/prod.kost|-80,00|-80,00|2|3|  

 **Finansposter**  

|Bokføringsdato|Finanskonto|Kontonummer (En-US-demo)||Beløp|Løpenr.|  
|------------------|------------------|---------------------------------|-|------------|---------------|  
|01.01.20|[Lagerkonto]|2130||70,00|1|  
|01.01.20|[Konto utl. kj.pris/prod.kost]|7291||-70,00|2|  
|01.01.20|[Lagerkonto]|2130||10,00|3|  
|01.01.07|[Konto for utlign. indir. kost.]|7292||-10,00|4|  
|15.01.20|[Lagerkonto]|2130||-80,00|5|  
|15.01.20|[Vareforbrukskonto]|7290||80,00|6|  

> [!NOTE]  
>  Bokføringsdatoen for finanspostene er den samme som for de tilknyttede verdipostene.  
>   
>  Feltet **Bokført kost** i **Verdipost**-tabellen fylles ut.  

 Relasjonen mellom verdiposter og finansposter lagres i tabellen **Finans - varepostrelasjon**.  

 **Relasjonsposter i tabellen Finans – varepostrelasjon**  

|Finansløpenr.|Verdiløpenummer|Finansjournalnr.|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## <a name="assembly-and-production-posting"></a>Monterings- og produksjonsbokføring  
Kapasitet og ressursposter representerer klokkeslettet som er bokført som forbrukt under produksjon eller montering. Disse prosesskostnadene bokføres som verdiposter i finans sammen med de involverte materialkostnadene i en struktur som ligner på den som er beskrevet for vareposter i dette emnet.  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Bokføre monteringsordre](design-details-assembly-order-posting.md).  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)   
 [Designdetaljer: Konti i Finans](design-details-accounts-in-the-general-ledger.md)   
 [Designdetaljer: Kostkomponenter](design-details-cost-components.md) [Administrere lagerkostnader](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
