---
title: Forsikre aktiva
description: Du kan tilordne en eller flere aktiva til én forsikringspolise ved å bokføre i forsikringsdekningsposten fra **Forsikringskladd**-siden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 06/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Forsikre aktiva
En forsikringspolise for et aktiva representeres av et forsikringskort. Du kan tilordne ett aktiva til én forsikringspolise eller flere aktiva til én forsikringspolise.

Du kan tilordne et aktiva til en forsikringspolise ved å bokføre i forsikringsdekningsposten fra **Forsikringskladd**-siden.

I tillegg kan du tilordne et aktiva til en forsikringspolise og opprette forsikringsdekningsposter når du bokfører anskaffelseskostnaden. Du gjør dette ved å bokføre en anskaffelseskost fra aktivakladden med **Forsikringsnr.**-feltet fylt ut. **Autom. forsikringsbokføring** må være avmerket på **Aktivaoppsett**-siden. Hvis du vil ha mer informasjon, se [Slik bokfører du en aktivaanskaffelse manuelt med aktivafinanskladden](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

Hvis **Autom. forsikringsbokføring** på **Aktivaoppsett**-siden ikke er valgt, vil bokføring av anskaffelser fra aktivakladden opprette linjer på **Forsikringskladd**-siden, som du deretter må bokføre manuelt.

> [!WARNING]  
>   Hvis du ikke merker av for **Autom. forsikringsbokføring** på **Aktivaoppsett**-siden, må forsikringskladden være basert på en kladdemal uten en nummerserie. Dette er fordi de innsatte bilagsnumrene fra aktivakladdelinjen ellers vil være i konflikt med nummerserien for forsikringskladden. Hvis du vil ha mer informasjon om kladdemaler og kladder, kan du se [Definere generell aktivainformasjon](fa-how-setup-general.md).

Når du har tilordnet et aktiva til en forsikringspolise, er **Forsikret** avmerket på aktivakortet. Når du selger aktivaet, fjernes avmerkingen automatisk.

## Slik oppetter eller endrer du et forsikringskort:
En forsikringspolise for et aktiva må representeres av et forsikringskort.

Når du mottar opplysninger om endringer i dekningsbeløpet, må du angi de nye opplysningene på **Forsikringskort**-siden for å sikre at du foretar riktig analyse av forsikringspolisedekningen.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Forsikring**, og velg deretter den relaterte koblingen.
2. Velg **Ny** for å opprette et nytt kort for en forsikringspolise. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velg eventuelt forsikringspolisen du vil endre, og velg deretter **Rediger**.

## Slik tilordner du et aktiva til en forsikringspolise ved å bokføre fra forsikringskladden:
Du tilordner et aktiva til en forsikringspolise ved å bokføre i forsikringsdekningsposten.  

Fremgangsmåten nedenfor forklarer hvordan du oppretter en forsikringskladdelinje manuelt. Hvis **Autom. forsikringsbokføring** er avmerket på **Aktivaoppsett**-siden, opprettes forsikringskladdelinjene automatisk når du bokfører anskaffelseskostnader. I så fall trenger du bare å bokføre kladden.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Forsikringskladder**, og velg deretter den relaterte koblingen.  
2. Åpne den relevante kladden, og fyll ut kladdelinjene etter behov.  
3. Hvis du vil tilordne flere aktiva til én forsikringspolise, oppretter du kladdelinjer med samme verdi i **Forsikringsnr.-feltet** og forskjellige verdier i **Aktivane.**-feltet.  
4. Velg handlingen **Bokfør**.  

    > [!NOTE]  
    >   Postene i forsikringskladden bokføres bare i forsikringsdekningsposten.  

## Slik oppdaterer du forsikringsverdien for et aktiva:
Du kan bruke kjørselen **Indeksreg. forsikring** til å oppdatere verdien av de dekkede aktivaene.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Indeksforsikring**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov.

    > [!NOTE]  
    >   I feltet **Indeksreg.tall** angir du en nedgang på for eksempel 5 % som 95, mens du angir en økning på 2 % som 102.  
3. Velg **OK**.  

   Kjørselen beregner det nye beløpet som en prosentverdi av den totale forsikringsverdien, slik det er oppgitt på siden **Forsikringsstatistikk**, og oppretter deretter en linje i forsikringskladden.  
4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Forsikringskladder**, og velg deretter den relaterte koblingen.  
5. Åpne den aktuelle forsikringskladden, gå gjennom verdiene som er opprettet, og bokfør dem deretter i forsikringsdekningsposten.  

## Slik kontrollerer du forsikringsdekningen:
[!INCLUDE[prod_short](includes/prod_short.md)] tilbyr dedikerte rapporter og statistikksider for bruk i analyse av forsikringspoliser og om aktiva er over- eller underforsikret.  

### Oversikt over forsikringspoliser
For å få en oversikt over forsikringspolisene, forhåndsvis eller skriv ut rapporten **Forsikring - oversikt**. Rapporten viser alle policyene og de viktigste feltene fra forsikringskortene.  

### Forsikringsdekning
Hvis du vil se hvilke forsikringspoliser som dekker hvert aktiva og med hvilket beløp, kan du forhåndsvise eller skrive ut rapporten **Forsikring – tot.verdi forsik.**.  

### Over-/underdekning
Du kan kontrollere om aktiva er over- eller underforsikret på følgende måter:  

* Siden **Forsikringsstatistikk**. Et positivt beløp i feltet **Over-/underforsikret** betyr at aktivaet er overforsikret. Et negativt beløp betyr at det er underforsikret.  
* **Aktivastatistikk**-siden. Velg **Total forsikringsverdi**-feltet for å vise **Fors.dekningsposter**-siden.  
* **Over-/underdekning**-rapporten.  
* **Forsikring - analyse**-rapporten.  

### Aktiva ikke forsikret
Hvis du vil sjekke om du har glemt å tilordne et aktiva til en forsikringspolise, kan du skrive ut eller forhåndsvise rapporten **Forsikring - aktiva ikke fors.**. Denne rapporten viser aktiva som det ikke er bokført noen beløp for i forsikringsdekningsposten.  

## Slik viser du forsikringsdekningsposter
Du kan vise postene du har opprettet i forsikringsdekningsposten.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Forsikring**, og velg deretter den relaterte koblingen.  
2. Velg den relevante forsikringspolisen, og velg deretter handlingen **Fors.dekningsposter**.  

## Slik viser du den totale forsikringsverdien for aktiva:
En dedikert matriseside viser forsikringsverdiene som er registrert for hver forsikringspolise for hvert aktiva som resultat av forsikringsrelaterte beløp du har bokført.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Forsikring**, og velg deretter den relaterte koblingen.  
2. Velg den relevante forsikringspolisen, og velg deretter handlingen **Total forsikr.verdi per aktiva**.  
3. Fyll ut feltene etter behov.  
4. Velg handlingen **Vis matrise**.  
5. Hvis du vil se de underliggende forsikringsdekningspostene, velger du en verdi i matrisen.  

## Slik korrigerer du forsikringsdekningsposter
Hvis et aktiva er knyttet til feil forsikringspolise, kan du korrigere den ved å opprette to reklassifiseringsposter fra forsikringskladden.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Forsikringskladder**, og velg deretter den relaterte koblingen.  
2. Opprett én kladdelinje for aktivaet og den riktige forsikringspolisen der verdien i **Beløp**-feltet er positivt.  
3. Opprett en ny kladdelinje for aktivaet og den gale forsikringspolisen der verdien i **Beløp**-feltet er negativt.  
4. Velg handlingen **Bokfør**.  

Aktivaet frigjøres fra den gale forsikringspolisen på den andre linjen, og knyttes til den riktige forsikringspolisen på den første linjen.  

## Se også
[Aktiva](fa-manage.md)  
[Definere aktiva](fa-setup.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]