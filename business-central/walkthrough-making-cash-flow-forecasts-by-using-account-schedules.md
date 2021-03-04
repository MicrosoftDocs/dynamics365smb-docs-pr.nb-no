---
title: Gjennomgang – Lage kontantstrømprognoser ved å bruke kontoskjemaer | Microsoft-dokumentasjon
description: Denne gjennomgangen beskriver hvordan du kan bruke kontoskjemaer til å lage kontantstrømprognoser. Kontoskjemaer utfører beregninger som ikke kan utføres direkte i diagrammet over kontantstrømkontoer. I kontoskjemaer kan du definere delsummer for kontantstrømmottak og -utbetalinger. Disse delsummene kan inkluderes i nye totalsummer som deretter kan brukes til å lage kontantstrømprognoser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a210792a187bde0217917659f118c58a6a135df2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756544"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Gjennomgang: Lage kontantstrømprognoser ved å bruke kontoskjemaer
Denne gjennomgangen beskriver hvordan du kan bruke kontoskjemaer til å lage kontantstrømprognoser. Kontoskjemaer utfører beregninger som ikke kan utføres direkte i diagrammet over kontantstrømkontoer. I kontoskjemaer kan du definere delsummer for kontantstrømmottak og -utbetalinger. Disse delsummene kan inkluderes i nye totalsummer som deretter kan brukes til å lage kontantstrømprognoser.  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen  
Denne gjennomgangen beskriver følgende oppgaver:  

- Definere et nytt navn for kontantstrømkontoskjema.  
- Definere kontoskjemalinjer.  
- Definere et nytt kolonneoppsett.  
- Tilordne et kolonneoppsett til et kontoskjema.  
- Vise og skrive ut kontantstrømprognosen.  

### <a name="prerequisites"></a>Forutsetninger  
For å fullføre denne gjennomgangen må du gjøre følgende:  

- [!INCLUDE[prod_short](includes/prod_short.md)] installert.  
- Forslagslinjene for kontantstrøm registreres.  

## <a name="roles"></a>Roller  
Denne gjennomgangen viser oppgaver som utføres av følgende brukerrolle:  

- Kontrollør  

## <a name="story"></a>Hovedscenario  
Ken er kontrollør på CRONUS og utarbeider månedlige kontantstrømprognoser. Han tar med finans, salg, kjøp og aktiva i prognosen, og deretter viser han den til ØKDIR Sara.  

## <a name="setting-up-a-new-account-schedule-name"></a>Definere et nytt kontoskjemanavn  
Et kontoskjema består av et navn på kontoskjemaet for kontantstrøm med en rekke linjer og et kolonneoppsett.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Slik definerer du et nytt kontoskjemanavn  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.  
2.  Velg **Ny** på siden **Kontoskjemanavn** for å opprette et nytt navn for kontantstrømkontoskjema.  
3.  I **Navn**-feltet angir du **Prognose**.  
4.  I **Beskrivelse**-feltet angir du **Kontantstrømprognose**.  
5.  La feltene **Standard kolonneoppsett** og **Analysevisningsnavn** være tomme.  

## <a name="setting-up-account-schedule-lines"></a>Definere kontoskjemalinjer  
Etter at et kontoskjemanavn er angitt, definerer Ken hver linje som vises i kontoskjemaet for kontantstrøm. Ken definerer linjer som kan vises i rapporter, i tillegg til linjer som bare er til beregningsformål.  

### <a name="to-set-up-account-schedule-lines"></a>Definere kontoskjemalinjer  

1.  På siden **Kontoskjemanavn** velger du det nye **Prognose**-kontoskjemanavnet du opprettet, og deretter velger du handlingen **Rediger kontoskjema**.  
2.  På siden **Kontoskjema** angir du hver linje nøyaktig, som vist i tabellen nedenfor.  

    > [!NOTE]  
    >  Du kan bruke funksjonen **Sett inn kontantstrømkonti** til raskt å merke kontantstrømkontoene i kontantstrømkontoplanen og kopiere dem til kontoskjemalinjer.  

    |Radnr.|Beskrivelse|Sammentellingstype|Sammentelling|Radtype|Beløpstype|Vis|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |C10|Beløp|Bevegelse|Poster|Nettobeløp|Alltid|  
    |C20|Beløp til dato|Saldo til dato|Poster|Nettobeløp|Alltid|  
    |C30|Hele regnskapsåret|Hele regnskapsåret|Poster|Nettobeløp|Alltid|  

4.  Velg **OK**-knappen.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Tilordne kolonneoppsettet til kontoskjemanavnet  
Ken er nå klar til å tilordne kolonneoppsettet til kontoskjemanavnet.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Slik tilordner du kolonneoppsettet til kontoskjemanavnet:  

1.  På siden **Kontoskjemanavn** velger du **Prognose** i **Navn**-feltet.  
2.  Velg kolonneoppsettet **Kontantstrøm** i feltet **Standard kolonneoppsett** for å bruke det som standard kolonneoppsett.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Slik viser og skriver du ut kontantstrømprognosen:  
1.  Velg **Oversikt**-handlingen på siden **Kontoskjemanavn** for å vise kontantstrømprognosen.  
2.  På siden **Kto.skjemaoversikt** kan du velge et beløp og deretter vise kontantstrømprognosepostene som utgjør beløpet. I tillegg kan du vise formelen som brukes til å beregne beløpet. Du kan også filtrere beløpene etter dato og dimensjon.  
3.  Velg **Skriv ut**-handlingen for å skrive ut kontantstrømprognosen.  

## <a name="see-also"></a>Se også  
 [Arbeide med kontoskjemaer](bi-how-work-account-schedule.md)   
 [Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)  
 [Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]