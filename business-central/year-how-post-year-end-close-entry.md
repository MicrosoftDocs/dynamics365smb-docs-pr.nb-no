---
title: Bokføre posten for årsavslutning
description: 'Beskriver hvordan du åpner kladden du angav i kjørselen Lukk resultatregnskapet, og deretter ser gjennom og bokfører avslutningsposten for årsslutt.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: 100
ms.date: 08/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="post-the-year-end-closing-entry"></a>Bokføre posten for årsavslutning

Når du har brukt den satsvise jobben **Lukk resultatregnskapet** til å generere avslutningsposten eller -postene for årsslutt, må du åpne kladden du angav i kjørselen, og deretter se gjennom og bokføre postene.  

> [!TIP]
> Avhengig av arbeidsprosessene i organisasjonen kan du velge å lukke eller ikke lukke regnskapsperioder og regnskapsår i [!INCLUDE [prod_short](includes/prod_short.md)]. Den følgende fremgangsmåten forutsetter at du har lukket regnskapsåret med alternativet *Regnskapsperioder*, generert en avslutningspost ved årsslutt ved hjelp av kjørselen **Lukk resultatregnskap**, og nå er klar til å bokføre årsavslutningsposten sammen med motregningen av poster på egenkapitalkontoen. Organisasjonen din kan velge å arbeide annerledes, for eksempel ved å bokføre avslutningsposten for årsslutt som en del av avslutningen av regnskapsåret.

## <a name="to-post-the-year-end-closing-entry"></a>Bokføre avslutningsposten for årsslutt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. På **siden Finanskladder i** feltet Bunkenavn **Velg** du bunken som inneholder avslutningspostene.
3. Se gjennom postene.
4. Velg handlingen **Bokfør** for å bokføre kladden.

> [!NOTE]  
> Det vises en feilmelding hvis feil blir oppdaget. Hvis bokføringen lykkes, fjernes de bokførte postene fra kladden. Når bokføringen er fullført, posteres en oppføring på hver resultatregnskapskonto, slik at saldoen blir null og årsresultatet overføres til balansen.

## <a name="see-also"></a>Se også

[Lukke regnskapsperioder](year-close-account-periods.md)    
[Avsluttende bøker](year-close-books.md)    
[Lukk resultatregnskapet](year-close-income-statement.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
