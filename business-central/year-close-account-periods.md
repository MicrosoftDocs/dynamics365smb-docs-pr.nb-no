---
title: Lukk regnskapsperioder for et regnskapsår
description: Denne artikkelen beskriver hvordan du lukker regnskapsperiodene som utgjør regnskapsåret for årsavslutning.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: '100,'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
---
# <a name="close-accounting-periods"></a>Lukk regnskapsperioder

Når et regnskapsår er over, må du lukke periodene som utgjør regnskapsåret.

## <a name="to-close-accounting-periods"></a>Slik lukker du regnskapsperioder

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Regnskapsperioder**, og velg deretter den relaterte koblingen.
2. På siden **Regnskapsperioder** velger du handling **Lukk år**.

    Hvis flere enn ett regnskapsår er åpne, blir det tidligste valg for lukking. En melding viser hvilket år som blir lukket, og resultatet av lukkingen.
3. Hvis du vil lukke året, velger du **Ja**-knappen.

Regnskapsåret er lukket, og det er merket av i feltene **Lukket** og **Dato låst** for alle periodene i året. Regnskapsåret kan ikke åpnes på nytt, og du kan ikke slette haken i feltene **Lukket** eller **Dato låst**.

> [!NOTE]  
> Du kan ikke lukke et regnskapsår før du har opprettet et nytt. Merk at etter at et regnskapsår er lukket, kan du ikke endre startdatoen for det etterfølgende regnskapsåret.

Selv om et regnskapsår er avsluttet, kan du bokføre finansposter i det. Når du gjør dette, blir postene merket som bokført i et avsluttet regnskapsår, og feltet **Etterpost** velges.

Når et regnskapsår er avsluttet, må du lukke resultatkontiene, og overføre årets resultat til resultatkontoen i balansen. Du kan gjenta dette hver gang du bokfører til det lukkede regnskapsåret.

## <a name="see-also"></a>Se også

[Avslutte tablåer](year-close-books.md)  
[Bokfør avslutningsposten for årsslutt](year-how-post-year-end-close-entry.md)  
[Arbeid med regnskapsperioder og regnskapsår](finance-accounting-periods-and-fiscal-years.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
