---
title: Gjennomgang – Lage kontantstrømprognoser ved å bruke kontoskjemaer
description: Lær hvordan du kan bruke kontoskjemaer til å lage kontantstrømprognoser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/16/2021
ms.author: edupont
ms.openlocfilehash: d7a1cfd2a1612d3f593d1635643b2917987d7bea
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470390"
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

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Forslagslinjene for kontantstrøm registreres  

## <a name="roles"></a>Roller

Denne gjennomgangen viser oppgaver som utføres av følgende brukerrolle:  

- Kontrollør  

## <a name="story"></a>Hovedscenario

Ken er kontrollør på CRONUS og utarbeider månedlige kontantstrømprognoser. Han tar med finans, salg, kjøp og aktiva i prognosen, og deretter viser han den til ØKDIR Sara.  

## <a name="setting-up-a-new-account-schedule-name"></a>Definere et nytt kontoskjemanavn

Et kontoskjema består av et navn på kontoskjemaet for kontantstrøm med en rekke linjer og et kolonneoppsett.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Slik definerer du et nytt kontoskjemanavn  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.  
2. Velg **Ny** på siden **Kontoskjemanavn** for å opprette et nytt navn for kontantstrømkontoskjema.  
3. I **Navn**-feltet angir du **Prognose**.  
4. I **Beskrivelse**-feltet angir du **Kontantstrømprognose**.  
5. La feltene **Standard kolonneoppsett** og **Analysevisningsnavn** være tomme.  

## <a name="setting-up-account-schedule-lines"></a>Definere kontoskjemalinjer

Etter at et kontoskjemanavn er angitt, definerer Ken hver linje som vises i kontoskjemaet for kontantstrøm. Ken definerer linjer som kan vises i rapporter, i tillegg til linjer som bare er til beregningsformål.  

### <a name="to-set-up-account-schedule-lines"></a>Definere kontoskjemalinjer  

1. På siden **Kontoskjemanavn** velger du det nye **Prognose**-kontoskjemanavnet du opprettet, og deretter velger du handlingen **Rediger kontoskjema**.  
2. På siden **Kontoskjema** angir du hver linje som vist i tabellen nedenfor.  

    > [!TIP]  
    >  Du kan bruke funksjonen **Sett inn kontantstrømkonti** til raskt å merke kontantstrømkontoene i kontantstrømkontoplanen og kopiere dem til kontoskjemalinjer.  

    | Radnr. | Beskrivelse              | Sammentellingstype            | Sammentelling | Radtype   | Beløpstype | Vis |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Åpne ordrer        | Konti for kontantstrømoppføring | 20       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Leie                  | Konti for kontantstrømoppføring | 30       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Økonomiske aktiva         | Konti for kontantstrømoppføring | 40       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Aktivasalg    | Konti for kontantstrømoppføring | 50       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Private investeringer      | Konti for kontantstrømoppføring | 60       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Diverse mottak   | Konti for kontantstrømoppføring | 70       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Åpne serviceordrer      | Konti for kontantstrømoppføring | 80       |Bevegelse | Nettobeløp  | Ja  |
    | R20     | Kontantmottak totalt      | Formel                  | R10      |Bevegelse | Nettobeløp  | Ja  |
    | R20     | Kontantmottak totalt      | Formel                  | R10      |Bevegelse | Nettobeløp  | Ja  |
    | R30     | Kjøp                 | Konti for kontantstrømoppføring | 1010     |Bevegelse | Nettobeløp  | Ja  |
    | R30     | Åpne bestillinger     | Konti for kontantstrømoppføring | 1020     |Bevegelse | Nettobeløp  | Ja  |
    | R30     | Personalkost          | Konti for kontantstrømoppføring | 1030     |Bevegelse | Nettobeløp  | Ja  |
    | R30     | Løpende kostnader            | Konti for kontantstrømoppføring | 1040     |Bevegelse | Nettobeløp  | Ja  |
    | R30     | Finanskostnader            | Konti for kontantstrømoppføring | 1050     |Bevegelse | Nettobeløp  | Ja  |
    | R30     | Investeringer              | Konti for kontantstrømoppføring | 1070     |Bevegelse | Nettobeløp  | Ja  |
    | R30     | Privat forbruk     | Konti for kontantstrømoppføring | 1090     |Bevegelse | Nettobeløp  | Ja  |
    | R30     | Forfalt mva.                  | Konti for kontantstrømoppføring | 1100     |Bevegelse | Nettobeløp  | Ja  |
    | R30     | Andre utgifter           | Konti for kontantstrømoppføring | 1110     |Bevegelse | Nettobeløp  | Ja  |
    | R40     | Total for kontantutbetalinger | Formel                  | R30      |Bevegelse | Nettobeløp  | Ja  |
    | R50     | Overskudd                  | Formel                  | R20+R40  |Bevegelse | Nettobeløp  | Ja  |
    | R60     | Kontantstrømmidler          | Konti for kontantstrømoppføring | 2100     |Bevegelse | Nettobeløp  | Ja  |
    | R70     | Total kontantstrøm          | Formel                  | R50+R60  |Bevegelse | Nettobeløp  | Ja  |

    > [!NOTE]
    > Radnummeret R10 brukes til å registrere kontosummene for salg. Radnummeret R20 brukes til å beregne summen av alle innbetalinger. Radnummeret R30 brukes til å registrere kontosummene for kjøp. Radnummeret R40 brukes til å beregne summen av alle kontantutbetalinger. Radnummeret R50 brukes til å registrere summen av kontantoverskudd. Radnummeret R60 brukes til å registrere de likvide midlene. Radnummeret R70 brukes til å beregne den prognostiserte kontantstrømmen.

## <a name="setting-up-a-new-column-layout"></a>Definere et nytt kolonneoppsett

Før Ken kan skrive ut kontantstrømprognosen, må han opprette kolonneoppsettet for den numeriske informasjonen. Han definerer informasjon han vil bruke fra linjene, i kolonnene.

- Den første kolonnen viser tallet *C10* med tittelen **Beløp**, og inneholder bevegelsen.  
- Den andre kolonnen viser tallet *C20* med tittelen **Saldo per dato**, og inneholder transaksjoner for perioden.  
- Den tredje kolonnen har tallet *C30* med tittelen **Hele året**, og viser bevegelsen i saldoene for hele regnskapsåret.  
- Til slutt tilordner han kolonneoppsettet som standard kolonneoppsett for kontoskjemaet **Prognose**.  

## <a name="to-set-up-a-new-column-layout"></a>Definere et nytt kolonneoppsett

1. Velg det nye kontoskjemanavnet for **Prognose** du har opprettet, i vinduet **Kontoskjemanavn**. I fanebladet **Hjem** under **Prosess** velger du **Rediger oppsett for kolonneutforming**.

    > [!TIP]
    > Du kan finne den samme handlingen på siden **Kontoskjema** hvis du fremdeles redigerer kontoskjemaet **Prognose** der.

2. Opprett et nytt kolonneoppsett med navnet **Kontantstrøm**.

3. Velg OK-knappen.

4. Angi hver linje nøyaktig som vist i tabellen nedenfor.

    |Kolonnenr.|Kolonneoverskrift|Kolonnetype|Postoppføringstype|Beløpstype|Vis|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Beløp|Bevegelse|Poster|Nettobeløp|Alltid|  
    |C20|Beløp til dato|Saldo til dato|Poster|Nettobeløp|Alltid|  
    |C30|Hele regnskapsåret|Hele regnskapsåret|Poster|Nettobeløp|Alltid|

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Tilordne kolonneoppsettet til kontoskjemanavnet

Ken er nå klar til å tilordne kolonneoppsettet til kontoskjemanavnet.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Slik tilordner du kolonneoppsettet til kontoskjemanavnet:  

1. På siden **Kontoskjema**, der du arbeider med kontoskjemaet **Prognose**, velger du handlingen **Rediger oppsett for kolonneutforming**.  
2. Velg kolonneoppsettet **Kontantstrøm** i feltet **Navn på kolonneoppsett** for å bruke det som standard kolonneoppsett.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Slik viser og skriver du ut kontantstrømprognosen:

1. Velg **Oversikt**-handlingen på siden **Kontoskjemanavn** for å vise kontantstrømprognosen.  
2. På siden **Kto.skjemaoversikt** kan du velge et beløp og deretter vise kontantstrømprognosepostene som utgjør beløpet. I tillegg kan du vise formelen som brukes til å beregne beløpet. Du kan også filtrere beløpene etter dato og dimensjon.  
3. Velg **Skriv ut**-handlingen for å skrive ut kontantstrømprognosen.  

## <a name="see-also"></a>Se også

[Arbeide med kontoskjemaer](bi-how-work-account-schedule.md)  
[Analysere kontantstrømmen i firmaet](finance-analyze-cash-flow.md)  
[Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]