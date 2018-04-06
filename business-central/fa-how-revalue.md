---
title: Revaluere aktiva| Microsoft-dokumentasjon
description: "Finn ut hvordan du justerer verdien av aktiva, registrerer nye beløp som en nedskrivning eller oppskrivning, og bokfører flere anskaffelseskostnader."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5dd885d32c0ca08bdf51770669ee569c3a7a98ed
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="revalue-fixed-assets"></a>Revaluere aktiva
Revaluering av aktiva kan bestå av oppskrivinger, nedskrivninger eller generelle verdijusteringer.

Når verdien for et aktiva har økt, kan du bokføre en kladdelinje med et høyere beløp, en oppskriving, i avskrivningstablået. Det nye beløpet registreres som en oppskriving i henhold til bokføringsoppsettet for aktivaet.

Når verdien for et aktiva har sunket, kan du bokføre en kladdelinje med et lavere beløp, en nedskriving, i avskrivningstablået. Det nye beløpet registreres som en nedskriving i henhold til bokføringsoppsettet for aktivaet.

Indeksregulering brukes til å justere flere aktivaverdier, for eksempel i henhold til generelle prisendringer. Du bruker kjørselen **Indeksreg. aktiva** til å endre forskjellige beløp, for eksempel nedskrivingsbeløp og oppskrivningsbeløp.

## <a name="to-post-an-appreciation-from-the-fixed-asset-gl-journal"></a>Slik bokfører du en oppskrivning fra aktivafinanskladden:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.  
2. Opprett en innledende kladdelinje, og fyll ut feltene etter behov.
3. I feltet **Aktivabokf.type** velger du **Revaluering**.
4. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for oppskrivingsbokføring.

    > [!NOTE]  
>   Trinn 4 fungerer bare hvis du har definert følgende: I vinduet **Kort for bokf.grp.- aktiva** for bokføringsgruppen for aktivumet, inneholder **Oppskrivingskonto**-feltet finansdebetkontoen og feltet **Motkonto for oppskriving** inneholder finanskontoen du vil bokføre motposter for oppskrivning til. Hvis du vil ha mer informasjon, kan du se Definere bokføringsgrupper for aktiva i [Definere generell aktivainformasjon](fa-how-setup-general.md).  
5. Velg handlingen **Bokfør**.

## <a name="to-post-a-write-down-from-the-fixed-asset-gl-journal"></a>Slik bokfører du en nedskrivning fra aktivafinanskladden:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.  
2. Opprett en innledende kladdelinje, og fyll ut feltene etter behov.
3. I feltet **Aktivabokf.type** velger du **Nedskriving**.
4. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for nedskrivingsbokføring.

    > [!NOTE]  
>   Trinn 4 fungerer bare hvis du har definert følgende: I vinduet **Kort for bokf.grp.- aktiva** for bokføringsgruppen for aktivumet, inneholder **Nedskrivingskonto**-feltet finanskreditkontoen og feltet **Konto for nedskrivningskostn.** inneholder finansdebetkontoen du vil bokføre motposter for nedskrivning til. Hvis du vil ha mer informasjon, kan du se Definere bokføringsgrupper for aktiva i [Definere generell aktivainformasjon](fa-how-setup-general.md).
5. Velg handlingen **Bokfør**.

## <a name="to-perform-general-revaluation-of-fixed-assets"></a>Slik utfører du generell revaluering av aktiva:
Indeksregulering brukes til å justere flere aktivaverdier, for eksempel i henhold til generelle prisendringer. Du bruker kjørselen **Indeksreg. aktiva** til å endre forskjellige beløp, for eksempel nedskrivingsbeløp og oppskrivningsbeløp. **Tillat indeksreg.** i **Avskrivningstablå**-vinduet må merkes av.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Indeksreg. aktiva**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.
3. Velg **OK**.

    Revalueringslinjer opprettes i henhold til innstillingene i trinn 2. Linjene opprettes i aktivakladden eller aktivafinanskladden, avhengig av malen og kladdeoppsettet i **Aktivakladdoppsett**-vinduet. Hvis du vil ha mer informasjon, kan du se [Definere generell aktivainformasjon](fa-how-setup-general.md).
4. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.  
5. Velg kladden med aktivaene du vil revaluere, og velg deretter **Poster**.  
6. Kontroller postene som er opprettet, og velg deretter **Bokfør** for å bokføre kladden.

    > [!TIP]  
>   Hvis indeksreguleringstallene bare er til simuleringsformål, kan du lagre dem i et spesielt avskrivningstablå som du oppretter. Disse postene har ingen innvirkning på de andre avskrivningstablåene.

   ## <a name="to-post-additional-acquisition-costs"></a>Slik bokfører du flere anskaffelseskostnader:
   Du kan bokføre tilleggsanskaffelseskostnader for aktiva på samme måte som når du bokfører den opprinnelige anskaffelseskosten: fra en kjøpsfaktura eller fra en aktivakladd. Hvis du vil ha mer informasjon, kan du se [Anskaffe aktiva](fa-how-acquire.md).  

Hvis det allerede er beregnet avskrivning for et aktiva, merker du av for **Avskr.anskaffelseskost** slik at skrapverdien som er avskrevet proporsjonalt med beløpet som det tidligere anskaffede aktivaet allerede er avskrevet med, trekkes fra tilleggsanskaffelseskosten. Dette sikrer at avskrivningsperioden ikke endres.  

Prosentsatsen for avskrivningen beregnes som:  

*P = (fullstendig avskrivning x 100) / avskrivningsgrunnlag*

*Avskrivningsbeløp = (P/100) x (tilleggsanskaffelseskost - skrapverdi)*  

Husk å merke av for **Avskr. frem til aktivabokf.dato** på fakturaen, i aktivafinanskladden eller på aktivakladdelinjene, slik at avskrivning beregnes fra siste aktivabokføringsdato til bokføringsdatoen for tilleggsanskaffelseskosten.

### <a name="example---posting-additional-acquisition-costs"></a>Eksempel – bokføre tilleggsanskaffelseskostnader
Det kjøpes en maskin den 1. august 2000. Anskaffelseskosten er 4 800. Det skal foretas lineær avskrivning over fire år.

Kjørselen **Beregn avskrivning** kjøres den 31. august 2000. Avskrivningen beregnes som:

*bokført verdi x antall avskrivningsdager / totalt antall avskrivningsdager = 4800 x 30 / 1440 = 100*  

Den 15. september 2000 bokføres en faktura for malingsarbeid på maskinen. Fakturabeløpet er på 480.

Hvis du merket av for **Avskr. frem til aktivabokf.dato** i fakturaen før bokføring, foretas følgende beregning:  

15 avskrivningsdager (fra 01.09.00 til 15.09.00) beregnes som :

*bokført verdi x antall avskrivningsdager / resterende antall avskrivningsdager = (4800 - 100) x 15 / 1410 = 50*

Hvis du merket av for **Avskr.anskaffelseskost** i fakturaen før bokføring, foretas følgende beregning:  

*Tilleggsanskaffelseskosten avskrives med ((150 x 100) / 4800) / 100 x 480 = 15*

Avskrivningsgrunnlaget er nå *5280 = (4800 + 480)*, og akkumulert avskrivning er *165 = (100 + 50 + 15)* og tilsvarer 45 dagers avskrivning av total anskaffelseskost. Dette betyr at aktivaet er ferdig avskrevet innen den anslåtte levetiden på fire år.  

Når kjørselen **Beregn avskrivning** kjøres den 30.09.00, gjøres følgende beregning:  

*Resterende avskrivningslevetid er 3 år, 10 måneder og 15 dager = 1395 dager*  

*Bokført verdi er (5280 - 165) = 5115*  

*Avskrivningsbeløp for september 2000: 5115 x 15 / 1395 = 55,00*  

*Samlet avskrivning = 165 + 55 = 220*  

Hvis du ikke merket av for **Avskr. frem til aktivabokf.dato**, går aktivaet glipp av 15 dagers avskrivning, ettersom kjørselen **Beregn avskrivning** som ble kjørt den 30.09.00, beregner avskrivning fra 15.09.00 til 30.09.00. Dette betyr at når kjørselen **Beregn avskrivning** kjøres den 30.09.00, ser beregningen slik ut:  

*Restlevetid er 3 år, 10 måneder og 15 dager = 1395 dager*  

*Bokført verdi er (4800 + 480 - 100 - 15) = 5165*

*Avskrivningsbeløp for september 2000: 5165 x 15 / 1395 = 55,54*  

*Samlet avskrivning = 100 + 15 + 55,54 = 170,54*

## <a name="see-also"></a>Se også
[Aktiva](fa-manage.md)  
[Definere aktiva](fa-setup.md)  
[Finans](finance.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

