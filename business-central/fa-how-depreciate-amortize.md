---
title: Avskrive eller amortisere aktiva | Microsoft-dokumentasjon
description: Du må definere hvordan du vil foreta nedskrivning, avskrivning eller amortisering av hvert aktivum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d113277e72dbc7e367fe39e6af7f4e3e2a2bb18d
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184487"
---
# <a name="depreciate-or-amortize-fixed-assets"></a>Avskrive eller amortisere aktiva
Avskrivning brukes til å fordele aktivakostnader, for eksempel maskiner og utstyr, over den avskrivningsberettigede levetiden til aktivaet. Du må definere hvordan du vil at hvert enkelt aktiva skal avskrives.  

 Det finnes to måter å bokføre avskrivninger på:  

* Automatisk, ved å utføre kjørselen **Beregn avskrivning**.  
* Manuelt, ved hjelp av aktivafinanskladden.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] kan beregne daglig avskrivning slik at du kan beregne avskrivninger for en hvilken som helst periode. Du kan derfor analysere gjeldende operasjonsresultater på for eksempel månedlig, kvartalsvis eller årlig basis. Beregningen bruker et standardår på 360 dager og en standardmåned på 30 dager. Hvis du vil ha mer informasjon, kan du se [Avskrivningsmetoder](fa-depreciation-methods.md).  

Hvis flere avdelinger bruker det samme aktivaet, kan periodisk avskrivning automatisk fordeles til disse avdelingene, etter en brukerdefinert fordelingstabell.  

Du kan kansellere ukorrekte avskrivningsposter fra et avskrivningstablå ved hjelp av kjørselen **Kanseller aktivaposter**. Deretter kan du bokføre det riktige beløpet ved å utføre kjørselen **Beregn avskrivning** på nytt. Feilene du retter, bokføres feilene som aktivafeilposter.  

Indeksregulering brukes til å justere verdier for generelle endringer i prisnivået. Du kan bruke kjørselen **Indeksreg. aktiva** til å beregne avskrivningsbeløpene på nytt.  

## <a name="to-calculate-depreciation-automatically"></a>Slik beregner du avskrivninger automatisk
Du kan utføre kjørselen **Beregn avskrivninger** én gang i måneden, eller etter behov. Kjørselen ingorerer aktiva som er solgt, aktiva som er sperret eller inaktive, eller som bruker den manuelle avskrivningsmetoden.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Beregn avskrivning**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velg **OK**.  

    Kjørselen beregner avskrivningen og oppretter linjer i aktivafinanskladden.

4. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.  

    På siden **Aktiva finanskladd** i **Antall avskrivningsdager**-feltet kan du se hvor mange avskrivningsdager det er beregnet.  
5. Velg handlingen **Bokfør**.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Slik bokfører du avskrivning manuelt fra aktivafinanskladden:
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktiva finanskladd**, og velg deretter den relaterte koblingen.  
2. Opprett en innledende kladdelinje, og fyll ut feltene etter behov.  
3. I feltet **Aktivabokf.type** velger du **Avskrivning**.  
4. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for bokføring av avskrivning. Hvis du vil ha mer informasjon, kan du se [Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Velg handlingen **Bokfør** for å bokføre kladden.  

Feltet **Bokført verdi** på siden **Aktivakort** blir oppdatert i henhold til dette.

Hvis du har definert aktivafordelingsnøkler for å fordele beløp på ulike avdelinger eller prosjekter, vil beløpene fordeles under bokføringen. Hvis du vil ha mer informasjon, kan du se [Definere generell aktivainformasjon](fa-how-setup-general.md).  

## <a name="to-manage-the-ending-book-value"></a>Slik håndterer du siste bokførte verdi
I feltet **Slutt bokført verdi** på siden **Aktivaavskrivningstablå** kan du angi den bokførte verdien du vil at aktivaet skal ha i gjeldende avskrivningstablå når det er fullstendig avskrevet. Du kan gjøre dette manuelt, eller du kan fylle ut feltet **Standard sluttverdi** på den relaterte siden **Avskrivningstablå**, som deretter brukes til å fylle ut feltet automatisk.

> [!NOTE]
> Hvis siste avskrivning innebærer at feltet **Bokført verdi** på siden **Aktivakort** er null, blir den siste avskrivningen automatisk redusert med dette beløpet.<br /><br />
> Hvis verdien i feltet **Bokført verdi** er større enn null etter siste avskrivning, for eksempel på grunn av et avrundingsproblem eller fordi det finnes en skrapverdi, ignoreres verdien i feltet **Slutt bokført verdi** på siden **Aktivaavskrivningstablå**. Hvis du vil ha mer informasjon, se [Slik bokfører du skrapverdien sammen med anskaffelseskosten](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Slik beregner du fordelinger i aktivafinanskladden:
Hvis flere avdelinger bruker det samme aktivaet, kan periodisk avskrivning automatisk fordeles til disse avdelingene, etter en brukerdefinert fordelingstabell.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktiva finanskladd**, og velg deretter den relaterte koblingen.  
2. Opprett en innledende linje, og fyll ut feltene etter behov.
3. I feltet **Aktivabokf.type** velger du **Fordeling**.  
4. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for fordelingsbokføring.  
5. Velg handlingen **Bokfør** for å bokføre kladden.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Bruke duplikatoversikter til å forberede bokføring av flere avskrivningstablåer
Når du fyller ut kladdelinjer som skal bokføres i et avskrivningstablå, kan du duplisere linjene i en separat kladd, slik at du kan bokføre dem i et annet avskrivningstablå. Hvis du vil ha mer informasjon, kan du se [Slik bokfører du poster i ulike avskrivningstablåer](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Avskrivningstablåer**, og velg deretter den relaterte koblingen.  
2. Åpne avskrivningstablået, og merk deretter av for **Del av duplikasjonsoversikt**.  

> [!IMPORTANT]  
>   Hvis du har valgt feltet **Bruk duplikatoversikt**, må du ikke bruke nummerserier på kladden. Årsaken er at nummerserien for aktivafinanskladden ikke samsvarer med nummerserien for aktivakladden.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Slik bokfører du poster i ulike avskrivningstablåer
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktiva finanskladd**, og velg deretter den relaterte koblingen.  
2. I kladden du vil bokføre avskrivning med, merker du av for **Bruk duplikatoversikt**.  
3. Fyll ut feltene som gjenstår, etter behov.  
4. Velg handlingen **Bokfør**.  
5. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktivakladder**, og velg deretter den relaterte koblingen.  

    > [!NOTE]  
    >   **Aktivakladd**-siden inneholder nye linjer for ulike avskrivningstablåer i henhold til duplikatoversikten.  
6. Se gjennom eller rediger linjene, og velg deretter **Bokfør**.  

    > [!NOTE]  
    >   Du kan også duplisere en post i et separat tablå ved å angi koden for avskrivningstablået i feltet **Duplikat i avskrivningstablå**, når du fyller ut en kladdelinje.  

Du kan kopiere poster fra ett avskrivningstablå til et annet med kjørselen **Kopier avskrivningstablå**. Kjørselen oppretter kladdelinjer i kladden du har angitt på siden **Aktivakladdoppsett** for avskrivningstablået du vil kopiere til. Hvis du vil ha mer informasjon, kan du se følgende fremgangsmåte:  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Slik kopierer du aktivaposter mellom avskrivningstablåer:
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Avskrivningstablåer**, og velg deretter den relaterte koblingen.  
2. Åpne det aktuelle avskrivningstablåkortet, og velg deretter **Kopier avskrivningstablå**.  
3. På siden **Kopier avskrivningstablå** fyller du ut feltene etter behov.  
4. Velg **OK**.  

De kopierte linjene opprettes enten i aktivafinanskladden eller i aktivakladden, avhengig av om avskrivningstablået du kopierer, er integrert med Finans.  

## <a name="see-also"></a>Se også
[Aktiva](fa-manage.md)  
[Definere aktiva](fa-setup.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
