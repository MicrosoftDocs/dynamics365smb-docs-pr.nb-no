---
title: Avskrive eller amortisere aktiva
description: 'Du må definere hvordan du vil skrive ned, avskrive eller amortisering hvert aktiva, for eksempel maskiner og utstyr, over avskrivningstiden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: write down
ms.search.form: '5610, 5611, 5629, 5633, 5659, 5660, 5663, 5619, 5666'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Avskrive eller amortisere aktiva

Avskrivning brukes til å fordele aktivakostnader, for eksempel maskiner og utstyr, over den avskrivningsberettigede levetiden til aktivaet. Du må definere hvordan du vil at hvert enkelt aktiva skal avskrives.  

 Det finnes to måter å bokføre avskrivninger på:  

* Automatisk, ved å utføre kjørselen **Beregn avskrivning**.  
* Manuelt, ved hjelp av aktivafinanskladden.  

[!INCLUDE[prod_short](includes/prod_short.md)] kan beregne daglig avskrivning slik at du kan beregne avskrivninger for en hvilken som helst periode. Du kan derfor analysere gjeldende operasjonsresultater på for eksempel månedlig, kvartalsvis eller årlig basis. Beregningen bruker et standardår på 360 dager og en standardmåned på 30 dager. Hvis du vil ha mer informasjon, kan du se [Avskrivningsmetoder](fa-depreciation-methods.md).  

Hvis flere avdelinger bruker det samme aktivaet, kan periodisk avskrivning automatisk fordeles til disse avdelingene, etter en brukerdefinert fordelingstabell.  

Du kan kansellere ukorrekte avskrivningsposter fra et avskrivningstablå ved hjelp av kjørselen **Kanseller aktivaposter**. Deretter kan du bokføre det riktige beløpet ved å utføre kjørselen **Beregn avskrivning** på nytt. Feilene du retter, bokføres feilene som aktivafeilposter.  

Indeksregulering brukes til å justere verdier for generelle endringer i prisnivået. Du kan bruke kjørselen **Indeksreg. aktiva** til å beregne avskrivningsbeløpene på nytt.  

## Slik beregner du avskrivninger automatisk

Du kan utføre kjørselen **Beregn avskrivninger** én gang i måneden, eller etter behov. Kjørselen ingorerer aktiva som er solgt, aktiva som er sperret eller inaktive, eller som bruker den manuelle avskrivningsmetoden.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Beregn avskriving**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velg **OK**.  

    Kjørselen beregner avskrivningen og oppretter linjer i aktivafinanskladden.

4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.  

    På siden **Aktiva finanskladd** i **Antall avskrivningsdager**-feltet kan du se hvor mange avskrivningsdager det er beregnet.  
5. Velg handlingen **Bokfør**.  

> [!NOTE]
> Kjent begrensning: Hvis du angir feltet **Bruk tvunget antall dager** til Ja og feltet **Tvunget antall dager** er satt til en verdi der **bokføringsdatoen** minus **Antall dager** resulterer i en dato i forrige kalenderår, tillater ikke systemet at du bokfører avskrivningen.
> Du kan unngå det ved å redusere feltet **Tvunget antall dager** til ikke høyere enn de beregnede dagene frem til bokføringsdato med 30 dager i måneden, ELLER angi flagget **Regnskapsår 365 dager** i avskrivningstablået.
> Vi anbefaler det første alternativet fordi du kanskje ikke vil endre bruken av 30 dager/måneder for avskrivning. Hvis du vil ha mer informasjon, se [Regnskapsår 365 dager-feltavskriving](fa-how-setup-depreciation.md#fiscal-year-365-days-field-depreciation).


## Slik bokfører du avskrivning manuelt fra aktivafinanskladden:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Aktivafinanskladd** og velger den relaterte koblingen.  
2. Opprett en innledende kladdelinje, og fyll ut feltene etter behov.  
3. I feltet **Aktivabokf.type** velger du **Avskrivning**.  
4. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for bokføring av avskrivning. Hvis du vil ha mer informasjon, kan du se [Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Velg handlingen **Bokfør** for å bokføre kladden.  

Feltet **Bokført verdi** på siden **Aktivakort** blir oppdatert i henhold til dette.

Hvis du har definert aktivafordelingsnøkler for å fordele beløp på ulike avdelinger eller prosjekter, vil beløpene fordeles under bokføringen. Hvis du vil ha mer informasjon, kan du se [Definere generell aktivainformasjon](fa-how-setup-general.md).  

## Slik håndterer du siste bokførte verdi

I feltet **Slutt bokført verdi** på siden **Aktivaavskrivningstablå** kan du angi den bokførte verdien du vil at aktivaet skal ha i gjeldende avskrivningstablå når det er fullstendig avskrevet. Du kan gjøre dette manuelt, eller du kan fylle ut feltet **Standard sluttverdi** på den relaterte siden **Avskrivningstablå**, som deretter brukes til å fylle ut feltet automatisk.

> [!NOTE]
> Hvis siste avskrivning innebærer at feltet **Bokført verdi** på siden **Aktivakort** er null, blir den siste avskrivningen automatisk redusert med dette beløpet.<br /><br />
> Hvis verdien i feltet **Bokført verdi** er større enn null etter siste avskrivning, for eksempel på grunn av et avrundingsproblem eller fordi det finnes en skrapverdi, ignoreres verdien i feltet **Slutt bokført verdi** på siden **Aktivaavskrivningstablå**. Hvis du vil ha mer informasjon, se [Slik bokfører du skrapverdien sammen med anskaffelseskosten](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## Slik beregner du fordelinger i aktivafinanskladden:

Hvis flere avdelinger bruker det samme aktivaet, kan periodisk avskrivning automatisk fordeles til disse avdelingene, etter en brukerdefinert fordelingstabell.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Aktivafinanskladd** og velger den relaterte koblingen.  
2. Opprett en innledende linje, og fyll ut feltene etter behov.
3. I feltet **Aktivabokf.type** velger du **Fordeling**.  
4. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for fordelingsbokføring.  
5. Velg handlingen **Bokfør** for å bokføre kladden.  

## Bruke duplikatoversikter til å forberede bokføring av flere avskrivningstablåer

Når du fyller ut kladdelinjer som skal bokføres i et avskrivningstablå, kan du duplisere linjene i en separat kladd, slik at du kan bokføre dem i et annet avskrivningstablå. Hvis du vil ha mer informasjon, kan du se [Slik bokfører du poster i ulike avskrivningstablåer](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Avskrivningstablåer**, og velg deretter den relaterte koblingen.  
2. Åpne avskrivningstablået, og merk deretter av for **Del av duplikasjonsoversikt**.  

> [!IMPORTANT]  
>   Hvis du har valgt feltet **Bruk duplikatoversikt**, må du ikke bruke nummerserier på kladden. Årsaken er at nummerserien for aktivafinanskladden ikke samsvarer med nummerserien for aktivakladden.  

## Slik bokfører du poster i ulike avskrivningstablåer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Aktivafinanskladd** og velger den relaterte koblingen.  
2. I kladden du vil bokføre avskrivning med, merker du av for **Bruk duplikatoversikt**.  
3. Fyll ut feltene som gjenstår, etter behov.  
4. Velg handlingen **Bokfør**.  
5. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivakladder**, og velg deretter den relaterte koblingen.  

    > [!NOTE]  
    >   **Aktivakladd**-siden inneholder nye linjer for ulike avskrivningstablåer i henhold til duplikatoversikten.  
6. Se gjennom eller rediger linjene, og velg deretter **Bokfør**.  

    > [!NOTE]  
    >   Du kan også duplisere en post i et separat tablå ved å angi koden for avskrivningstablået i feltet **Duplikat i avskrivningstablå**, når du fyller ut en kladdelinje.  

Du kan kopiere poster fra ett avskrivningstablå til et annet med kjørselen **Kopier avskrivningstablå**. Kjørselen oppretter kladdelinjer i kladden du har angitt på siden **Aktivakladdoppsett** for avskrivningstablået du vil kopiere til. Hvis du vil ha mer informasjon, kan du se følgende fremgangsmåte:  

## Slik kopierer du aktivaposter mellom avskrivningstablåer:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Avskrivningstablåer**, og velg deretter den relaterte koblingen.  
2. Åpne det aktuelle avskrivningstablåkortet, og velg deretter **Kopier avskrivningstablå**.  
3. På siden **Kopier avskrivningstablå** fyller du ut feltene etter behov.  
4. Velg **OK**.  

De kopierte linjene opprettes enten i aktivafinanskladden eller i aktivakladden, avhengig av om avskrivningstablået du kopierer, er integrert med Finans.  

## Se også

[Aktiva](fa-manage.md)  
[Definer aktiva](fa-setup.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
