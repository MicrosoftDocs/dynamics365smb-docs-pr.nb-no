---
title: Arbeide med regnskapsperioder og regnskapsår
description: Lær hvordan du arbeider med regnskapsperioder for å definere når bedriften rapporterer økonomiske resultater.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 100
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d1a7121f74cf58289e0bf4ce6a80080c071f64fe
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2022
ms.locfileid: "8383482"
---
# <a name="working-with-accounting-periods-and-fiscal-years"></a>Arbeide med regnskapsperioder og regnskapsår

Regnskapsperioder, som også kalles rapporteringsperioder, er tidsperioder som en bedrift eller organisasjon rapporterer økonomiske resultater for, for eksempel ved å generere resultatregnskapet eller balansen. Vanligvis viser regnskapsperioder til selskapets regnskapsår, som kan inneholde flere regnskapsperioder, for eksempel måneder eller kvartal.

I mange selskaper samsvarer ikke regnskapsåret med kalenderåret. Regnskapsåret kan for eksempel slutte 30. juni i stedet for 31. desember. For nyopprettede selskaper kan regnskapsåret faktisk være lenger enn 12 måneder.  

[!INCLUDE[prod_short](includes/prod_short.md)] krever bare regnskapsperioder hvis du vil lukke et resultatregnskap eller kjøre datakomprimeringsoppgaver. 

Du kan bruke regnskapsperioder i rapportering. For eksempel når du går gjennom bokførte poster på siden **Saldo/Budsjett** der rapporteringsintervallet kan angis. Ett av alternativene du kan angi er å rapportere etter regnskapsperiode. Du kan også lage et kontoskjema som sammenligner resultater for ulike regnskapsperioder.

## <a name="creating-a-new-fiscal-year"></a>Opprette et nytt regnskapsår

Du kan masseopprette regnskapsperioder ved å bruke kjørselen **Opprett regnskapsår** eller gjøre det manuelt.

### <a name="how-to-create-accounting-periods-in-bulk"></a>Slik masseoppretter du regnskapsperioder

Bruk **Opprett regnskapsår**-kjørselen til å dele et regnskapsår inn i like lange perioder.  

1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og angi **Regnskapsperioder**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Opprett år**.  <!--What about the Scheduling option? Should we mention that? There's also the Report Output Type field...-->
3. I **Startdato**-feltet angir du datoen som regnskapsåret starter på.  
4. I **Antall perioder**-feltet angir du antall regnskapsperioder som regnskapsåret skal deles inn i. Det kan være opptil 365 perioder i et år.  
5. I feltet **Periodelengde** angir du en varighet for hver periode. For eksempel 1M for én måned, 1K for ett kvartal og 1Å for ett år.  
6. Velg **OK**.  

### <a name="how-to-create-accounting-periods-manually"></a>Slik oppretter du regnskapsperioder manuelt

Hvis regnskapsperiodene i regnskapsåret har forskjellig varighet, som 4-4-5-kalenderen i detaljhandel, kan du opprette det manuelt.  
  
1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og angi **Regnskapsperioder**, og velg deretter den relaterte koblingen.  
2. I **Startdato**-feltet angir du datoen som regnskapsåret starter på. Feltet **Navn** vil vise navnet på måneden.  
3. Merk av for **Nytt regnskapsår** for å angi at dette er den første perioden i året. [!INCLUDE[prod_short](includes/prod_short.md)] bruker denne perioden for å finne ut hvilke perioder som skal lukkes ved årsslutt.
4. Gjenta trinn 2 og 3 for hver gjenværende periode.  

## <a name="closing-a-fiscal-year"></a>Lukke et regnskapsår

Lukking av regnskapsåret er en av oppgavene for lukking av tablåene. Når du har lukket regnskapsåret, er det merket av for **Lukket** og **Dato låst** for alle periodene i året. Du kan ikke åpne et år på nytt eller fjerne avmerkingene.

> [!NOTE]  
> Du må alltid ha minst ett åpent regnskapsår. Når du lukker et år, må du kontrollere at et nytt år er opprettet. Legg også merke til at etter du lukker ett år, er det ikke mulig å endre startdatoen for det etterfølgende året.

1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og angi **Regnskapsperioder**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Lukk år**.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a>Bokføre poster i et lukket regnskapsår

Selv om et regnskapsår er avsluttet, kan du bokføre finansposter i det. Når du gjør dette, blir postene merket som bokført i et avsluttet regnskapsår, og det merkes av for feltet **Etterpost**. Som standard vises ikke avmerkingsboksen på siden, men du kan legge den til. Neste trinn er å lukke resultatregnskapskontoene og overføre årsresultatene til en konto i balansen. Gjenta disse trinnene hver gang du bokfører poster til et lukket regnskapsår.

## <a name="see-also"></a>Se også

[Lukke tablåene](year-close-books.md)  
[Avslutte år og perioder](year-close-years-periods.md)  
[Arbeide med kontoskjemaer](bi-how-work-account-schedule.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]