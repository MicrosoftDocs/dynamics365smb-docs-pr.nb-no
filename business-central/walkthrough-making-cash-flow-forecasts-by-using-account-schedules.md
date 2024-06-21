---
title: Lage kontantstrømprognoser ved å bruke finansrapporter
description: Denne gjennomgangen beskriver hvordan du kan bruke finansrapporter til å lage kontantstrømprognoser i Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 08/18/2022
ms.author: bholtorf
ms.search.form: '103, 104, 108, 488, 489, 490'
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="walkthrough-making-cash-flow-forecasts-using-financial-reports"></a>Gjennomgang: Lage kontantstrømprognoser ved å bruke finansrapporter

Denne gjennomgangen beskriver hvordan du kan bruke finansrapportfunksjonen til å lage kontantstrømprognoser. Finansrapporter utfører beregninger som ikke kan utføres direkte i diagrammet over kontantstrømkontoer. I finansrapportene kan du definere delsummer for kontantstrømmottak og -utbetalinger. Disse delsummene kan inkluderes i nye totalsummer som deretter kan brukes til å lage kontantstrømprognoser.  

## <a name="about-this-walkthrough"></a>Om denne gjennomgangen

Denne gjennomgangen beskriver følgende oppgaver:  

- Definere et nytt navn for kontantstrømfinansrapporten.  
- Definer finansrapportlinjer.  
- Definer en ny kolonnedefinisjon.  
- Tildel en kolonnedefinisjon til en finansrapport.  
- Vise og skrive ut kontantstrømprognosen.  

### <a name="prerequisites"></a>Forutsetninger

For å fullføre denne gjennomgangen må du gjøre følgende:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Et kontantstrømforslag med registrerte linjer  

## <a name="roles"></a>Roller

Denne gjennomgangen viser oppgaver som utføres av følgende brukerrolle:  

- Kontrollør  

## <a name="story"></a>Hovedscenario

Ken er kontrollør på CRONUS og utarbeider månedlige kontantstrømprognoser. Ken tar med finans, salg, kjøp og aktiva i prognosene, og presenterer til ØKDIR Sara for forretningsinnsikt.  

## <a name="setting-up-a-new-financial-report-name"></a>Definer et nytt navn for finansrapporten

Navnet på finansrapporten er navnet du gir kontantstrømprognosen som inkluderer en serie med definerte linjer og en kolonnedefinisjon.  

### <a name="set-up-a-new-financial-report-name"></a>Definer et nytt navn for finansrapporten

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny** på siden **Finansrapporter** for å opprette et nytt navn på kontantstrømfinansrapporten.  
3. I **Navn**-feltet angir du **Prognose**.  
4. I **Beskrivelse**-feltet angir du **Kontantstrømprognose**.  
5. La feltene **Raddefinisjon** og **Kolonnedefinisjon** stå tomme.

## <a name="setting-up-row-definition-lines"></a>Definer raddefinisjonslinjer

Når et finansrapportnavn er definert, definerer Ken hver linje i kontantstrømfinansrapport. Ken definerer linjer som skal vises i rapporter, i tillegg til linjer som bare er til beregningsformål.  

### <a name="set-up-row-definition-lines"></a>Definer raddefinisjonslinjer

1. På siden for **Finansrapporter** velger du den nye finansrapporten **Prognose** du opprettet, og deretter velger du handlingen **Rediger raddefinisjon**.  
2. På siden **Raddefinisjon** angir du hver linje som vist i tabellen nedenfor.  

    > [!TIP]  
    > Bruk funksjonen **Sett inn kontantstrømkontoer** til raskt å merke kontantstrømkontoene i kontantstrømkontoene og kopiere dem til raddefinisjonslinjer.  

    | Radnr. | Description              | Sammentellingstype            | Sammentelling | Radtype   | Beløpstype | Visning |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Salg              | Konti for kontantstrømoppføring | 10       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Åpne ordrer        | Kontoer for kontantstrømoppføring | 20       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Leie                  | Konti for kontantstrømoppføring | 30       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Økonomiske aktiva         | Konti for kontantstrømoppføring | 40       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Aktivasalg    | Konti for kontantstrømoppføring | 50       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Private investeringer      | Konti for kontantstrømoppføring | 60       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Diverse mottak   | Konti for kontantstrømoppføring | 70       |Bevegelse | Nettobeløp  | Ja  |
    | R10     | Åpne serviceordrer      | Kontoer for kontantstrømoppføring | 80       |Bevegelse | Nettobeløp  | Ja  |
    | R20     | Kontantmottak totalt      | Formel                  | R10      |Bevegelse | Nettobeløp  | Ja  |
    | R30     | Kjøp                 | Kontoer for kontantstrømoppføring | 1010     |Bevegelse | Nettobeløp  | Ja  |
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
    | R60     | Kontantstrømmidler          | Kontoer for kontantstrømoppføring | 2100     |Bevegelse | Nettobeløp  | Ja  |
    | R70     | Total kontantstrøm          | Formel                  | R50+R60  |Bevegelse | Nettobeløp  | Ja  |

    > [!NOTE]
    > Radnummeret R10 brukes til å registrere kontosummene for salg. Radnummeret R20 brukes til å beregne summen av alle innbetalinger. Radnummeret R30 brukes til å registrere kontosummene for kjøp. Radnummeret R40 brukes til å beregne summen av alle kontantutbetalinger. Radnummeret R50 brukes til å registrere summen av kontantoverskudd. Radnummeret R60 brukes til å registrere de likvide midlene. Radnummeret R70 brukes til å beregne den prognostiserte kontantstrømmen.

## <a name="setting-up-a-new-column-definition"></a>Definer en ny kolonnedefinisjon

Før Ken skriver ut kontantstrømprognosen, må han opprette kolonnedefinisjonen for den numeriske informasjonen. Ken definerer informasjon som trengs for å bruke fra linjene, i kolonnene.

- Den første kolonnen viser tallet *C10* med tittelen **Beløp**, og inneholder bevegelsen.  
- Den andre kolonnen viser tallet *C20* med tittelen **Saldo per dato**, og inneholder transaksjoner for perioden.  
- Den tredje kolonnen har tallet *C30* med tittelen **Hele året**, og viser bevegelsen i saldoene for hele regnskapsåret.  
- Til slutt tildeler Ken kolonnedefinisjonen som standardalternativ for finansrapporten **Prognose**.  

### <a name="set-up-a-new-column-definition"></a>Definer en ny kolonnedefinisjon

1. Velg det nye finansrapportnavnet for **Prognose** på siden **Finansrapporter**. På fanen **Hjem** under **Prosess** velger du **Rediger oppsett for kolonnedefinisjon**.

2. Opprett en ny kolonnedefinisjon med navnet **Kontantstrøm**.

3. Velg **OK**-knappen.

4. Angi hver linje nøyaktig som vist i tabellen nedenfor.

    |Kolonnenr.|Kolonneoverskrift|Kolonnetype|Postoppføringstype|Beløpstype|Visning|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Beløp|Bevegelse|Oppføringer|Nettobeløp|Alltid|  
    |C20|Beløp til dato|Saldo per dato|Oppføringer|Nettobeløp|Alltid|  
    |C30|Helt regnskapsår|Helt regnskapsår|Oppføringer|Nettobeløp|Alltid|

## <a name="assigning-the-column-definition-to-the-financial-report-name"></a>Tildel kolonnedefinisjonen til finansrapportnavnet

Ken er nå klar til å tildele kolonnedefinisjonen til finansrapportnavnet.  

### <a name="assign-the-column-definition-to-the-financial-report-name"></a>Tildel kolonnedefinisjonen til finansrapportnavnet

1. På siden **Finansrapporter** velger du finansrapporten **Prognose**, og deretter velger du handlingen **Rediger kolonnedefinisjon**.  
2. Velg kolonnedefinisjonen **Kontantstrøm** i feltet **Navn** for å bruke det som standard kolonnedefinisjon.  

## <a name="view-and-print-the-cash-flow-forecast"></a>Vis og skriv ut kontantstrømprognosen

1. Velg handlingen finansrapporten **Prognose** på siden **Finansrapporter** for å vise kontantstrømprognosen.  
2. På siden **Finansrapport** kan du velge et beløp og deretter vise kontantstrømprognosepostene som utgjør beløpet. I tillegg kan du vise formelen som brukes til å beregne beløpet. Du kan også filtrere beløpene etter dato og dimensjon.  
3. Velg **Skriv ut**-handlingen for å skrive ut kontantstrømprognosen.  

## <a name="see-also"></a>Se også

[Arbeid med finansrapporter](bi-how-work-account-schedule.md)  
[Analyser kontantstrømmen i firmaet](finance-analyze-cash-flow.md)  
[Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
