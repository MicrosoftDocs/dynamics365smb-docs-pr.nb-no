---
title: Definer tilleggsvalutaer
description: 'Finans er definert til å bruke den lokale valutaen (LV), og en annen valuta blir definert som tilleggsvaluta, med en tilordnet gjeldende valutakurs.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'multiple currencies, foreign exchange rates'
ms.search.form: '5, 16,118, 483, 495'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Konfigurer en tilleggsrapporteringsvaluta

Ettersom selskaper har drift i stadig flere land/områder, blir det også stadig viktigere at de kan vurdere og rapportere finansdata i mer enn én valuta.

> [!NOTE]  
> Hvis du ser etter sanntidsinformasjon om utenlandsk valutakurser (FX) eller historiske kurser i [!INCLUDE[prod_short](includes/prod_short.md)], finner du den referert til som valuta. I tillegg til denne artikkelen kan du også se [Oppdater valutakurser](finance-how-update-currencies.md).

Finans er definert til å bruke den lokale valutaen (LV), men du kan definere at den skal bruke en annen valuta med en gjeldende valutakurs. Hvis du angir en ny valuta som en tilleggsrapporteringsvaluta, registrerer [!INCLUDE[prod_short](includes/prod_short.md)] beløp automatisk i både lokal valuta og tilleggsrapporteringsvalutaen i alle finansposter og andre poster, for eksempel mva-poster.

> [!Warning]
> Du bør ikke bruke ACY-funksjonen som grunnlag for oversettelse av årsregnskap med mindre du forstår begrensningene. Den kan ikke oversette årsregnskap fra utenlandske datterselskaper som en del av en selskapskonsolidering. ACY-funksjonen kan bare brukes til å utarbeide rapporter i en annen valuta, som om denne valutaen var selskapets lokale valuta.
>
> Du har for eksempel et stort antall kunder i britiske pund (GBP), og du har definert ACY til å være GBP. I dette scenariet vil ikke beløp i kundemodulen som bruker GBP, bli justert for valutakursgevinst/-tap i tilleggsvaluta, bare beløp i kundemodulen som finnes i andre valutaer. Det betyr at hvis du bruker tilleggsvaluta til å rapportere regnskapsoppgjør, kan det føre til undervurdert eller overvurderte utestående saldoer for kortsiktige fordringer.

## Vis rapporter og beløp i ACY

Bruk av en ACY kan hjelpe rapporteringsprosessen for et selskap i følgende tilfeller:

- Selskaper som ikke holder til i EU-land/-regioner, men som har transaksjoner som i stor grad foregår med selskaper i EU-land/-regioner. I dette tilfellet ønsker ikke-EU-selskapet kanskje også å rapportere i euro, slik at økonomirapportene gir større mening for handelspartnerne i EU.
- Selskaper som også vil vise rapporter i en valuta som er mer brukt internasjonalt enn den lokale valutaen.

Flere finansrapporter baserer seg på finansposter. Hvis du vil vise rapportdata i ACY, merker du av for **Vis beløp i tilleggsrapp.valuta** på hurtigfanen **Alternativer** for den relevante finansrapporten.

## Justerer valutakurser

Ettersom valutakursene varierer konstant, må ACY-ekvivalenter i systemet justeres jevnlig. Hvis disse justeringene ikke utføres, kan beløp som er regnet om fra utenlandske valutaer (eller tilleggsvalutaer) og bokført i lokal valuta i Finans, være villedende. I tillegg må daglige poster som bokføres før en daglig valutakurs angis i programmet, oppdateres etter at informasjonen om den daglige valutakursen er angitt. Satsjobben **Juster valutakurser** brukes til å justere valutakursene for bokførte kunde-, leverandør- og bankkontoposter. Den kan også oppdatere ACY-beløp i finansposter. Hvis du vil ha mer informasjon, se [Oppdatere valutakurser](finance-how-update-currencies.md).

## Oppsett av en ACY

Du kan sette opp en ACY ved å følge disse trinnene:

- Angi finanskontoer for bokføring av valutakursjusteringer.  
- Angi metoden for valutakursjustering for alle finanskontoer.  
- Angi metoden for valutakursjustering for mva-poster.  
- Aktiver ACY-en.  

### Slik angir du finanskonti for bokføring av valutakursjusteringer  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Valutaer** og velg den relaterte koblingen.  
2. Fyll inn følgende felt for ACY-en på **Valutaer**-siden.  

|Felt|Description|  
|---------------------------------|---------------------------------------|  
|**Kto. for real. agio - t.val.**|Finanskontoen der du vil bokføre agio for kursjusteringer mellom lokal valuta og ACY-en.|  
|**Kto. for real. disagio - t.val**|Finanskontoen der du vil bokføre disagio for kursjusteringer mellom lokal valuta og ACY-en.|  
|**Konto for restagio**|Finanskontoen der du vil bokføre restbeløp som er gevinst hvis du bokfører i finansmodulen i både LV og en ACY.|  
|**Konto for restdisagio**|Finanskontoen der du vil bokføre restbeløp som er tap hvis du bokfører i finansmodulen i både LV og en ACY.|

> [!NOTE]  
> Restbeløp kan forekomme når [!INCLUDE[prod_short](includes/prod_short.md)] avrunder debet- og kreditbeløp som er konvertert fra LV til en ACY.  

For hver finanskonto må du angi hvordan finansbeløp for den aktuelle kontoen skal justeres for valutakursendringer mellom lokal valuta og ACY-en.  

### Slik angir du metoden for valutakursjustering for alle finanskonti:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.  
2. Velg den relevante kontoen på siden **Kontoplan**, og velg deretter handlingen **Rediger**.  
3. På siden **Finanskort** velger du relevant metode i **Valutakursjustering**-feltet.  

    Hvis du bokfører i en ACY, angir du i feltet **Valutakursjustering** hvordan denne finanskontoen skal justeres for valutakurssvingninger mellom lokal valuta og ACY-en. Tabellen nedenfor beskriver alternativene.  

    |Felt|Description|  
    |----------------------------------|---------------------------------------|  
    |**Ingen justering**|Ingen kursjusteringer gjøres til finanskontoen. Denne innstillingen er standardalternativet.<br /><br /> **MERK:** Velg dette alternativet hvis valutakursen mellom lokal valuta og ACY alltid er fast.|  
    |**Juster beløp**|LV-beløpet er justert for eventuell agio og disagio. Agio eller disagio bokføres på finanskontoen i **Beløp**-feltet og på kontoene du har angitt for vinning eller tap i feltene **Kto. for real. agio - t.val.** og **Kto. for real. disagio - t.val** i **Valutaer**-siden.|  
    |**Juster tilleggsvalutabeløp**|ACY-beløpet er justert for eventuell agio og disagio. Agio eller disagio bokføres på finanskontoen i feltet **Tilleggsvalutabeløp** og på kontoene du har angitt for vinning eller tap i feltene **Kto. for real. agio - t.val.** og **Kto. for real. disagio - t.val** på **Valutaer**-siden.|  

    Agio eller disagio bokføres når du kjører kjørselen **Juster valutakurser**. I den kjørselen identifiserer justeringsvalutakursen i vinduet **Valutakurser** og beløpene på siden **Beløp** og **Tilleggsvalutabeløp** i finansposten sammenlignes for å finne ut hvorvidt det er agio eller disagio. Kjørselen bruker alternativet du velger i **Valutakursjustering**-feltet, til å finne ut hvordan agio eller disagio skal beregnes og bokføres for finanskontoer.  

4.  Lukk **Finanskort**-siden.  

### Slik angir du metode for valutakursjustering for mva-poster

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansoppsett**, og velg deretter den relaterte koblingen.  
2. På siden **Finansoppsett** velger du relevant metode i **Mva-valutakursjustering**-feltet.  
3. Hvis du bokfører i en ACY, kan du i **Mva-valutakursjustering**-feltet angi hvordan kontoene som er definert for mva-bokføring på siden **Mva-bokføringsoppsett**, skal justeres for valutakursendringer mellom lokal valuta og ACY-en.  

    Når du kjører kjørselen **Juster valutakurser**, identifiseres justeringsvalutakursen på **Valutakurs**-siden og sammenligner beløpene i feltene **Beløp** og **Tilleggsvalutabeløp** i mva-posten for å finne ut om det er agio eller disagio. Kjørselen bruker alternativet som du velger i dette feltet, til å angi hvordan agio og disagio for mva-konti skal bokføres.  

    Du har de samme alternativene som med finansposter, men i dette tilfellet vil de justerte postene være mva-poster. Tabellen nedenfor beskriver alternativene.

    |Felt|Description|  
    |----------------------------------|---------------------------------------|  
    |**Ingen justering**|Ingen kursjusteringer gjøres til finanskontoen. Denne innstillingen er standardalternativet.|  
    |**Juster beløp**|LV-beløpet er justert for eventuell agio og disagio. Agio eller disagio bokføres på finanskontoen i **Beløp**-feltet og på kontoene du har angitt for vinning eller tap i feltene **Kto. for real. agio - t.val.** og **Kto. for real. disagio - t.val** i **Valutaer**-siden.|  
    |**Juster tilleggsvalutabeløp**|ACY-beløpet er justert for eventuell agio og disagio. Agio eller disagio bokføres på finanskontoen i feltet **Tilleggsvalutabeløp** og på kontoene du har angitt for vinning eller tap i feltene **Kto. for real. agio - t.val.** og **Kto. for real. disagio - t.val** på **Valutaer**-siden.|  

### Slik aktiverer du ACY-en  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansoppsett**, og velg deretter den relaterte koblingen.  
2. Velg feltet **Tilleggsrapporteringsvaluta** på siden **Finansoppsett** for å velge tilleggsvalutaen du vil rapportere i.  
3. Når du forlater feltet, viser [!INCLUDE[prod_short](includes/prod_short.md)] en bekreftelsesmelding som beskriver virkningene av å aktivere ACY-en.  
4. Velg **Ja**-knappen for å bekrefte at du ønsker å aktivere valutaen.  
5. Den satsvise jobben **Justere tilleggsrapporteringsvaluta** åpnes.

    Denne kjørselen konverterer LV-beløp i eksisterende poster til ACY-en. Den satsvise jobben bruker en standard valutakurs som er kopiert fra valutakursen som er gyldig på arbeidsdatoen, på **Valutakurser**-siden. Restbeløp som oppstår ved omregning fra LV til ACY-en, bokføres i agio- og disagiokontoene som er angitt på **Valutaer**-siden. Bokføringsdatoen og bilagsnummeret for disse postene er identiske for den opprinnelige finansposten. Når du har bokført alle restbeløpene, bokfører kjørselen en avrundingspost på avslutningsdatoen for hvert avsluttet år til kontoen for fri egenkapital. Denne bokføringen sikrer at sluttsaldoen for inntektskontoene for hvert avsluttet år er 0 i både lokal valuta og ACY-en.
6. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Velg **OK**-knappen for å kjøre kjørselen.  

Etter at du har kjørt satsjobben, vil beløpene i følgende eksisterende poster være både i lokal valuta og ACY:  

- Finansposter  
- Vareutligningsposter  
- Mva-poster  
- Prosjektposter  
- Verdiposter  
- Produksjonsordrelinjer  
- Produksjonsordreposter  

I tillegg vil alle fremtidige poster av samme type få beløpene registrert i både lokal valuta og ACY.  

> [!NOTE]  
> Feltet **Tilleggsrapporteringsvaluta** vil først bli aktivert når du har valgt **OK** i kjørselen **Juster tilleggsrapp.valuta**.  

## Se også

[Oppdater valutakurser](finance-how-update-currencies.md)  
[Lukk år og perioder](year-close-years-periods.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
