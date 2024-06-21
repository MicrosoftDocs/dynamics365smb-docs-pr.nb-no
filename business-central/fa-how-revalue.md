---
title: Revaluere aktiva
description: 'Finn ut hvordan du justerer verdien av aktiva, registrerer nye beløp som en nedskrivning eller oppskrivning, og bokfører andre anskaffelseskostnader.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '5628, 5629, 5633'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="revalue-fixed-assets"></a>Revaluer aktiva

Revaluering av aktiva kan bestå av oppskrivinger, nedskrivninger eller generelle verdijusteringer.

Når verdien for et aktiva øker, kan du bokføre en kladdelinje med en oppskriving, i avskrivningstablået. Det nye beløpet registreres som oppskriving i henhold til bokføringsoppsettet for aktivumet.

Når verdien for et aktiva reduseres, kan du bokføre en kladdelinje med et lavere beløp, en nedskriving, i avskrivningstablået. Det nye beløpet registreres som en nedskriving i henhold til bokføringsoppsettet for aktivaet.

Indeksregulering brukes til å justere flere aktivaverdier, for eksempel i henhold til generelle prisendringer. Du bruker kjørselen **Indeksreg. aktiva** til å endre forskjellige beløp, for eksempel nedskrivingsbeløp og oppskrivningsbeløp.

## <a name="to-post-appreciation-from-the-fixed-asset-gl-journal"></a>Slik bokfører du oppskrivning fra aktivafinanskladden

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.  
2. Opprett en innledende kladdelinje, og fyll ut feltene etter behov.
3. I feltet **Aktivabokf.type** velger du **Revaluering**.
4. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for oppskrivingsbokføring.

    > [!NOTE]  
    >   Trinn 4 fungerer bare hvis du har definert følgende: På siden **Kort for bokf.grp.- aktiva** for bokføringsgruppen for aktivumet, inneholder **Konto for oppskrivning**-feltet finansdebetkontoen og feltet **Motkonto for oppskrivning** inneholder finanskontoen du vil bokføre motposter for oppskrivning til. Hvis du vil ha mer informasjon, kan du se [Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Velg handlingen **Bokfør**.

## <a name="to-post-a-write-down-from-the-fixed-asset-gl-journal"></a>Slik bokfører du en nedskrivning fra aktivafinanskladden:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.  
2. Opprett en innledende kladdelinje, og fyll ut feltene etter behov.
3. I feltet **Aktivabokf.type** velger du **Nedskriving**.
4. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for nedskrivingsbokføring.

    > [!NOTE]  
    >   Trinn 4 fungerer bare hvis du har definert følgende: På siden **Kort for bokf.grp.- aktiva** for bokføringsgruppen for aktivumet, inneholder **Nedskrivingskonto**-feltet finanskreditkontoen og feltet **Konto for nedskrivningskostn.** inneholder finansdebetkontoen du vil bokføre motposter for nedskrivning til. Hvis du vil ha mer informasjon, kan du se [Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Velg handlingen **Bokfør**.

## <a name="to-perform-general-revaluation-of-fixed-assets"></a>Slik utfører du generell revaluering av aktiva:

Indeksregulering brukes til å justere flere aktivaverdier, for eksempel i henhold til generelle prisendringer. Du bruker kjørselen **Indeksreg. aktiva** til å endre forskjellige beløp, for eksempel nedskrivingsbeløp og oppskrivningsbeløp. **Tillat indeksreg.** på **Avskrivningstablå**-siden må merkes av.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Indeksreg. aktiva**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.
3. Velg **OK**.

    Revalueringslinjer opprettes i henhold til innstillingene i trinn 2. Linjene opprettes i aktivakladden eller aktivafinanskladden, avhengig av malen og kladdeoppsettet på **Aktivakladdoppsett**-siden. Hvis du vil ha mer informasjon, kan du se [Definere generell aktivainformasjon](fa-how-setup-general.md).
4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.  
5. Velg kladden med aktivaene du vil revaluere, og velg deretter **Poster**.  
6. Kontroller postene som er opprettet, og velg deretter **Bokfør** for å bokføre kladden.

    > [!TIP]  
    >   Hvis indeksreguleringstallene bare er til simuleringsformål, kan du lagre dem i et spesielt avskrivningstablå som du oppretter. Disse postene har ingen innvirkning på de andre avskrivningstablåene.

## <a name="to-post-other-acquisition-costs"></a>Slik bokfører du andre anskaffelseskostnader

Du kan bokføre andre anskaffelseskostnader for aktiva fra en bestilling eller fra en aktivakladd på samme måte som når du bokfører den opprinnelige anskaffelseskosten. Hvis du vil ha mer informasjon, kan du se [Anskaffe aktiva](fa-how-acquire.md).  

Hvis det allerede er beregnet avskrivning for et aktiva, merker du av for **Avskr.anskaffelseskost** slik at skrapverdien som er avskrevet proporsjonalt med beløpet som det tidligere anskaffede aktivaet, trekkes fra den andre anskaffelseskosten. Denne metoden sikrer at avskrivningsperioden ikke endres.  

Prosentsatsen for avskrivningen beregnes som:  

*P = (fullstendig avskrivning x 100) / avskrivningsgrunnlag*

*Avskrivningsbeløp = (P/100) x (tilleggsanskaffelseskost - skrapverdi)*  

Husk å merke av for **Avskr. frem til aktivabokf.dato** på fakturaen, i aktivafinanskladden eller på aktivakladdelinjene, slik at avskrivning beregnes fra siste aktivabokføringsdato til bokføringsdatoen for den andre anskaffelseskosten.

### <a name="example---posting-other-acquisition-costs"></a>Eksempel – bokfør andre anskaffelseskostnader

Det kjøpes en maskin den 1. august 2000. Anskaffelseskosten er 4 800. Det skal foretas lineær avskrivning over fire år.

Kjørselen **Beregn avskrivning** kjøres den 31. august 2000. Avskrivningen beregnes som:

*bokført verdi x antall avskrivningsdager / totalt antall avskrivningsdager = 4800 x 30 / 1440 = 100*  

Den 15. september 2000 bokføres en faktura for malingsarbeid på maskinen. Fakturabeløpet er på 480.

Hvis du merket av for **Avskr. frem til aktivabokf.dato** i fakturaen før bokføring, foretas følgende beregning:  

15 avskrivningsdager (fra 01.09.00 til 15.09.00) beregnes som :

*bokført verdi x antall avskrivningsdager / resterende antall avskrivningsdager = (4800 - 100) x 15 / 1410 = 50*

Hvis du merket av for **Avskr.anskaffelseskost** i fakturaen før bokføring, foretas følgende beregning:  

*Den andre anskaffelseskosten avskrives som ((150 x 100) / 4800) / 100 x 480 = 15*

Avskrivningsgrunnlaget er nå *5280 = (4800 + 480)*, og akkumulert avskrivning er *165 = (100 + 50 + 15)* og tilsvarer 45 dagers avskrivning av total anskaffelseskost. Denne beregningen betyr at aktivaet er ferdig avskrevet innen den anslåtte levetiden på fire år.  

Når kjørselen **Beregn avskrivning** kjøres den 30.09.00, gjøres følgende beregning:  

*Resterende avskrivningslevetid er 3 år, 10 måneder og 15 dager = 1395 dager*  

*Bokført verdi er (5280 - 165) = 5115*  

*Avskrivningsbeløp for september 2000: 5115 x 15 / 1395 = 55,00*  

*Samlet avskrivning = 165 + 55 = 220*  

Hvis du ikke merket av for **Avskr. frem til aktivabokf.dato**, går aktivumet glipp av 15 dagers avskrivning, ettersom kjørselen **Beregn avskrivning** som ble kjørt den 30.09.00, beregner avskrivning fra 15.09.00 til 30.09.00. Dette betyr at når kjørselen **Beregn avskrivning** kjøres den 30.09.00, ser beregningen slik ut:  

*Restlevetid er 3 år, 10 måneder og 15 dager = 1395 dager*  

*Bokført verdi er (4800 + 480 - 100 - 15) = 5165*

*Avskrivningsbeløp for september 2000: 5165 x 15 / 1395 = 55,54*  

*Samlet avskrivning = 100 + 15 + 55,54 = 170,54*

## <a name="see-also"></a>Se også

[Aktiva](fa-manage.md)  
[Definer aktiva](fa-setup.md)  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
