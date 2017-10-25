---
title: Forsikre aktiva | Microsoft-dokumentasjon
Description: Du tilordne et aktivum til en forsikringspolise, som representeres av et forsikringskort.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 421d45e7f35ffdc46801fea85221ba453d52c516
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-insure-fixed-assets"></a>Forsikre aktiva
En forsikringspolise for et aktiva representeres av et forsikringskort. Du kan tilordne ett aktiva til én forsikringspolise eller flere aktiva til én forsikringspolise.

Du kan tilordne et aktiva til en forsikringspolise ved å bokføre i forsikringsdekningsposten fra **Forsikringskladd**-vinduet.

I tillegg kan du tilordne et aktiva til en forsikringspolise og opprette forsikringsdekningsposter når du bokfører anskaffelseskostnaden. Du gjør dette ved å bokføre en anskaffelseskost fra aktivakladden med **Forsikringsnr.**-feltet fylt ut. **Autom. forsikringsbokføring** må være avmerket i **Aktivaoppsett**-vinduet. Hvis du vil ha mer informasjon, kan du se avsnittet "Slik bokfører du en aktivaanskaffelse manuelt med aktivafinanskladden" i [Anskaffe aktiva](fa-how-acquire.md).

Hvis **Autom. forsikringsbokføring** i **Aktivaoppsett**-vinduet ikke er valgt, vil bokføring av anskaffelser fra aktivakladden opprette linjer i **Forsikringskladd**-vinduet, som du deretter må bokføre manuelt.

> [!WARNING]  
>   Hvis du ikke merker av for **Autom. forsikringsbokføring** i **Aktivaoppsett**-vinduet, må forsikringskladden være basert på en kladdemal uten en nummerserie. Dette er fordi de innsatte bilagsnumrene fra aktivakladdelinjen ellers vil være i konflikt med nummerserien for forsikringskladden. Se [Definere generell aktivainformasjon](fa-how-setup-general.md) for mer informasjon om kladdemaler og kladder.

Når du har tilordnet et aktiva til en forsikringspolise, er **Forsikret** avmerket på aktivakortet. Når du selger aktivaet, fjernes avmerkingen automatisk.

## <a name="to-create-or-modify-an-insurance-card"></a>Slik oppetter eller endrer du et forsikringskort:
En forsikringspolise for et aktiva må representeres av et forsikringskort.

Når du mottar opplysninger om endringer i dekningsbeløpet, må du angi de nye opplysningene i **Forsikringskort**-vinduet for å sikre at du foretar riktig analyse av forsikringspolisedekningen.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forsikring**, og velg deretter den relaterte koblingen.
2. Velg **Ny** for å opprette et nytt kort for en forsikringspolise. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velg eventuelt forsikringspolisen du vil endre, og velg deretter **Rediger**.

## <a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a>Slik tilordner du et aktiva til en forsikringspolise ved å bokføre fra forsikringskladden:
Du tilordner et aktiva til en forsikringspolise ved å bokføre i forsikringsdekningsposten.  

Fremgangsmåten nedenfor forklarer hvordan du oppretter en forsikringskladdelinje manuelt. Hvis **Autom. forsikringsbokføring** er avmerket i **Aktivaoppsett**-vinduet, opprettes forsikringskladdelinjene automatisk når du bokfører anskaffelseskostnader. I så fall trenger du bare å bokføre kladden.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forsikringskladder**, og velg deretter den relaterte koblingen.  
2. Åpne den relevante kladden, og fyll ut kladdelinjene etter behov.  
3. Hvis du vil tilordne flere aktiva til én forsikringspolise, oppretter du kladdelinjer med samme verdi i **Forsikringsnr.-feltet** og forskjellige verdier i **Aktivane.**-feltet.  
4. Velg handlingen **Bokfør**.  

    > [!NOTE]  
>   Postene i forsikringskladden bokføres bare i forsikringsdekningsposten.  

## <a name="to-update-the-insurance-value-of-a-fixed-asset"></a>Slik oppdaterer du forsikringsverdien for et aktiva:
Du kan bruke kjørselen **Indeksreg. forsikring** til å oppdatere verdien av de dekkede aktivaene.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Indeksreg. forsikring**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov.

    > [!NOTE]  
>   I feltet **Indeksreg.tall** angir du en nedgang på for eksempel 5 % som 95, mens du angir en økning på 2 % som 102.  
3. Velg **OK**.  

   Kjørselen beregner det nye beløpet som en prosentverdi av den totale forsikringsverdien, slik det er oppgitt i vinduet **Forsikringsstatistikk**, og oppretter deretter en linje i forsikringskladden.  
4. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forsikringskladder**, og velg deretter den relaterte koblingen.  
5. Åpne den aktuelle forsikringskladden, gå gjennom verdiene som er opprettet, og bokfør dem deretter i forsikringsdekningsposten.  

## <a name="to-monitor-insurance-coverage"></a>Slik kontrollerer du forsikringsdekningen:
[!INCLUDE[d365fin](includes/d365fin_md.md)] tilbyr dedikerte rapporter og statistikkvinduer for bruk i analyse av forsikringspoliser og om aktiva er over- eller underforsikret.  

### <a name="overview-of-insurance-policies"></a>Oversikt over forsikringspoliser
For å få en oversikt over forsikringspolisene, forhåndsvis eller skriv ut rapporten **Forsikring - oversikt**. Rapporten viser alle policyene og de viktigste feltene fra forsikringskortene.  

### <a name="insurance-coverage"></a>Forsikringsdekning
Hvis du vil se hvilke forsikringspoliser som dekker hvert aktiva og med hvilket beløp, kan du forhåndsvise eller skrive ut rapporten **Forsikring – tot.verdi forsik.**.  

### <a name="overunder-coverage"></a>Over-/underdekning
Du kan kontrollere om aktiva er over- eller underforsikret på følgende måter:  

* Vinduet **Forsikringsstatistikk**. Et positivt beløp i feltet **Over-/underforsikret** betyr at aktivaet er overforsikret. Et negativt beløp betyr at det er underforsikret.  
* **Aktivastatistikk**-vinduet. Velg **Total forsikringsverdi**-feltet for å vise **Fors.dekningsposter**-vinduet.  
* **Over-/underdekning**-rapporten.  
* **Forsikring - analyse**-rapporten.  

### <a name="uninsured-fixed-assets"></a>Aktiva ikke forsikret
Hvis du vil sjekke om du har glemt å tilordne et aktiva til en forsikringspolise, kan du skrive ut eller forhåndsvise rapporten **Forsikring - aktiva ikke fors.**. Denne rapporten viser aktiva som det ikke er bokført noen beløp for i forsikringsdekningsposten.  

## <a name="to-view-insurance-coverage-ledger-entries"></a>Slik viser du forsikringsdekningsposter
Du kan vise postene du har opprettet i forsikringsdekningsposten.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forsikring**, og velg deretter den relaterte koblingen.  
2. Velg den relevante forsikringspolisen, og velg deretter handlingen **Fors.dekningsposter**.  

## <a name="to-view-the-total-insurance-value-of-fixed-assets"></a>Slik viser du den totale forsikringsverdien for aktiva:
Et dedikert matrisevindu viser forsikringsverdiene som er registrert for hver forsikringspolise for hvert aktiva som resultat av forsikringsrelaterte beløp du har bokført.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forsikring**, og velg deretter den relaterte koblingen.  
2. Velg den relevante forsikringspolisen, og velg deretter handlingen **Total forsikr.verdi per aktiva**.  
3. Fyll ut feltene etter behov.  
4. Velg handlingen **Vis matrise**.  
5. Hvis du vil se de underliggende forsikringsdekningspostene, velger du en verdi i matrisen.  

## <a name="to-correct-insurance-coverage-entries"></a>Slik korrigerer du forsikringsdekningsposter
Hvis et aktiva er knyttet til feil forsikringspolise, kan du korrigere den ved å opprette to reklassifiseringsposter fra forsikringskladden.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forsikringskladder**, og velg deretter den relaterte koblingen.  
2. Opprett én kladdelinje for aktivaet og den riktige forsikringspolisen der verdien i **Beløp**-feltet er positivt.  
3. Opprett en ny kladdelinje for aktivaet og den gale forsikringspolisen der verdien i **Beløp**-feltet er negativt.  
4. Velg handlingen **Bokfør**.  

Aktivaet frigjøres fra den gale forsikringspolisen på den andre linjen, og knyttes til den riktige forsikringspolisen på den første linjen.  

## <a name="see-also"></a>Se også
[Aktiva](fa-manage.md)  
[Definere aktiva](fa-setup.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

