---
title: Forsikre aktiva | Microsoft-dokumentasjon
Description: Du tilordne et aktivum til en forsikringspolise, som representeres av et forsikringskort.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 3e26786d1568cdae30be0bcb17de7a5ed824c364
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184463"
---
# <a name="insure-fixed-assets"></a>Forsikre aktiva
En forsikringspolise for et aktiva representeres av et forsikringskort. Du kan tilordne ett aktiva til én forsikringspolise eller flere aktiva til én forsikringspolise.

Du kan tilordne et aktiva til en forsikringspolise ved å bokføre i forsikringsdekningsposten fra **Forsikringskladd**-siden.

I tillegg kan du tilordne et aktiva til en forsikringspolise og opprette forsikringsdekningsposter når du bokfører anskaffelseskostnaden. Du gjør dette ved å bokføre en anskaffelseskost fra aktivakladden med **Forsikringsnr.**-feltet fylt ut. **Autom. forsikringsbokføring** må være avmerket på **Aktivaoppsett**-siden. Hvis du vil ha mer informasjon, se [Slik bokfører du en aktivaanskaffelse manuelt med aktivafinanskladden](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

Hvis **Autom. forsikringsbokføring** på **Aktivaoppsett**-siden ikke er valgt, vil bokføring av anskaffelser fra aktivakladden opprette linjer på **Forsikringskladd**-siden, som du deretter må bokføre manuelt.

> [!WARNING]  
>   Hvis du ikke merker av for **Autom. forsikringsbokføring** på **Aktivaoppsett**-siden, må forsikringskladden være basert på en kladdemal uten en nummerserie. Dette er fordi de innsatte bilagsnumrene fra aktivakladdelinjen ellers vil være i konflikt med nummerserien for forsikringskladden. Hvis du vil ha mer informasjon om kladdemaler og kladder, kan du se [Definere generell aktivainformasjon](fa-how-setup-general.md).

Når du har tilordnet et aktiva til en forsikringspolise, er **Forsikret** avmerket på aktivakortet. Når du selger aktivaet, fjernes avmerkingen automatisk.

## <a name="to-create-or-modify-an-insurance-card"></a>Slik oppetter eller endrer du et forsikringskort:
En forsikringspolise for et aktiva må representeres av et forsikringskort.

Når du mottar opplysninger om endringer i dekningsbeløpet, må du angi de nye opplysningene på **Forsikringskort**-siden for å sikre at du foretar riktig analyse av forsikringspolisedekningen.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikring**, og velg deretter den relaterte koblingen.
2. Velg **Ny** for å opprette et nytt kort for en forsikringspolise. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velg eventuelt forsikringspolisen du vil endre, og velg deretter **Rediger**.

## <a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a>Slik tilordner du et aktiva til en forsikringspolise ved å bokføre fra forsikringskladden:
Du tilordner et aktiva til en forsikringspolise ved å bokføre i forsikringsdekningsposten.  

Fremgangsmåten nedenfor forklarer hvordan du oppretter en forsikringskladdelinje manuelt. Hvis **Autom. forsikringsbokføring** er avmerket på **Aktivaoppsett**-siden, opprettes forsikringskladdelinjene automatisk når du bokfører anskaffelseskostnader. I så fall trenger du bare å bokføre kladden.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikringskladder**, og velg deretter den relaterte koblingen.  
2. Åpne den relevante kladden, og fyll ut kladdelinjene etter behov.  
3. Hvis du vil tilordne flere aktiva til én forsikringspolise, oppretter du kladdelinjer med samme verdi i **Forsikringsnr.-feltet** og forskjellige verdier i **Aktivane.**-feltet.  
4. Velg handlingen **Bokfør**.  

    > [!NOTE]  
    >   Postene i forsikringskladden bokføres bare i forsikringsdekningsposten.  

## <a name="to-update-the-insurance-value-of-a-fixed-asset"></a>Slik oppdaterer du forsikringsverdien for et aktiva:
Du kan bruke kjørselen **Indeksreg. forsikring** til å oppdatere verdien av de dekkede aktivaene.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Indeksreg. forsikring**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov.

    > [!NOTE]  
    >   I feltet **Indeksreg.tall** angir du en nedgang på for eksempel 5 % som 95, mens du angir en økning på 2 % som 102.  
3. Velg **OK**.  

   Kjørselen beregner det nye beløpet som en prosentverdi av den totale forsikringsverdien, slik det er oppgitt på siden **Forsikringsstatistikk**, og oppretter deretter en linje i forsikringskladden.  
4. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikringskladder**, og velg deretter den relaterte koblingen.  
5. Åpne den aktuelle forsikringskladden, gå gjennom verdiene som er opprettet, og bokfør dem deretter i forsikringsdekningsposten.  

## <a name="to-monitor-insurance-coverage"></a>Slik kontrollerer du forsikringsdekningen:
[!INCLUDE[d365fin](includes/d365fin_md.md)] tilbyr dedikerte rapporter og statistikksider for bruk i analyse av forsikringspoliser og om aktiva er over- eller underforsikret.  

### <a name="overview-of-insurance-policies"></a>Oversikt over forsikringspoliser
For å få en oversikt over forsikringspolisene, forhåndsvis eller skriv ut rapporten **Forsikring - oversikt**. Rapporten viser alle policyene og de viktigste feltene fra forsikringskortene.  

### <a name="insurance-coverage"></a>Forsikringsdekning
Hvis du vil se hvilke forsikringspoliser som dekker hvert aktiva og med hvilket beløp, kan du forhåndsvise eller skrive ut rapporten **Forsikring – tot.verdi forsik.**.  

### <a name="overunder-coverage"></a>Over-/underdekning
Du kan kontrollere om aktiva er over- eller underforsikret på følgende måter:  

* Siden **Forsikringsstatistikk**. Et positivt beløp i feltet **Over-/underforsikret** betyr at aktivaet er overforsikret. Et negativt beløp betyr at det er underforsikret.  
* **Aktivastatistikk**-siden. Velg **Total forsikringsverdi**-feltet for å vise **Fors.dekningsposter**-siden.  
* **Over-/underdekning**-rapporten.  
* **Forsikring - analyse**-rapporten.  

### <a name="uninsured-fixed-assets"></a>Aktiva ikke forsikret
Hvis du vil sjekke om du har glemt å tilordne et aktiva til en forsikringspolise, kan du skrive ut eller forhåndsvise rapporten **Forsikring - aktiva ikke fors.**. Denne rapporten viser aktiva som det ikke er bokført noen beløp for i forsikringsdekningsposten.  

## <a name="to-view-insurance-coverage-ledger-entries"></a>Slik viser du forsikringsdekningsposter
Du kan vise postene du har opprettet i forsikringsdekningsposten.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikring**, og velg deretter den relaterte koblingen.  
2. Velg den relevante forsikringspolisen, og velg deretter handlingen **Fors.dekningsposter**.  

## <a name="to-view-the-total-insurance-value-of-fixed-assets"></a>Slik viser du den totale forsikringsverdien for aktiva:
En dedikert matriseside viser forsikringsverdiene som er registrert for hver forsikringspolise for hvert aktiva som resultat av forsikringsrelaterte beløp du har bokført.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikring**, og velg deretter den relaterte koblingen.  
2. Velg den relevante forsikringspolisen, og velg deretter handlingen **Total forsikr.verdi per aktiva**.  
3. Fyll ut feltene etter behov.  
4. Velg handlingen **Vis matrise**.  
5. Hvis du vil se de underliggende forsikringsdekningspostene, velger du en verdi i matrisen.  

## <a name="to-correct-insurance-coverage-entries"></a>Slik korrigerer du forsikringsdekningsposter
Hvis et aktiva er knyttet til feil forsikringspolise, kan du korrigere den ved å opprette to reklassifiseringsposter fra forsikringskladden.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikringskladder**, og velg deretter den relaterte koblingen.  
2. Opprett én kladdelinje for aktivaet og den riktige forsikringspolisen der verdien i **Beløp**-feltet er positivt.  
3. Opprett en ny kladdelinje for aktivaet og den gale forsikringspolisen der verdien i **Beløp**-feltet er negativt.  
4. Velg handlingen **Bokfør**.  

Aktivaet frigjøres fra den gale forsikringspolisen på den andre linjen, og knyttes til den riktige forsikringspolisen på den første linjen.  

## <a name="see-also"></a>Se også
[Aktiva](fa-manage.md)  
[Definere aktiva](fa-setup.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
