---
title: Definere en VIA-metode og overvåke prosjektfremdrift | Microsoft Docs
description: Beskriver hvordan du oppretter en varer i arbeid (via)-metode og beregner VIA for å beregne den økonomiske verdien av prosjekter mens de er fortløpende.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 052a0ecbe3b5435a2d73f377bb4ac0f4c4373f58
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443821"
---
# <a name="monitor-job-progress-and-performance"></a>Overvåke prosjektfremdrift og -ytelse
Under fremdriften av et prosjekt forbrukes materialer, ressurser og andre utgifter som må bokføres til prosjektet. Med funksjonen Varer i arbeid (VIA) kan du beregne den økonomiske verdien av prosjekter i Finans mens prosjektene pågår. I mange tilfeller vil du kanskje bokføre utgifter for et prosjekt før du fakturerer et prosjekt. Når bare utgifter er bokført, vil årsregnskapet bli unøyaktig. Hvis du vil ha mer informasjon, kan du se [Forstå VIA-metoder](projects-understanding-wip.md).

Hvis du vil spore verdien i Finans, kan du beregne VIA og bokføre verdien i Finans.

Du kan beregne VIA basert på følgende:

* Kostverdi
* Salgsverdi
* Gjenkjennelig kost
* Løpende
* Ved avslutning

Hvis du vil vise resultatet ved å bruke en annen metode, kan du endre metoden og beregne VIA på nytt. Det er ingen begrensning på antall ganger du kan beregne VIA. VIA beregnes bare, det bokføres ikke i Finans. Når du har beregnet VIA, kan du bokføre i Finans.

## <a name="to-create-a-job-wip-method"></a>Slik oppretter du en VIA-metode for prosjekt
Du kan opprette en VIA-metode for prosjekt som gjenspeiler behovene i organisasjonen. Når du har opprettet den, kan du angi den som standardmetoden for beregning av prosjekt-VIA som skal brukes i organisasjonen.  

> [!NOTE]
> Når du har brukt den nye metoden til å opprette VIA-poster, kan ikke du slette metoden eller endre den.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **VIA-metoder for prosjekt**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Lukk siden.   
4. Hvis du bruke den nye metoden som standardmetode, velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektoppsett** og velg den relaterte koblingen.  
5. Velg metoden fra listen i feltet **Standard VIA-metode**.

## <a name="to-define-a-wip-method-for-a-job"></a>Slik definerer du en VIA-metode for et prosjekt:
Når du oppretter en nytt prosjekt, må du angi hvilken VIA-metode for prosjekt som gjelder. I enkelte tilfeller er VIA-metoden for prosjekt som du kan bruke, definert for deg som en standard.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.
2. Velg handlingen **Ny**. Hvis du vil ha mer informasjon, kan du se [Opprette prosjekter](projects-how-create-jobs.md).  
3. På siden **Prosjektkort** i feltet **VIA-metode** velger du en VIA-metode fra listen. Hvis en standardmetode er definert, kan du velge et annet alternativ etter behov.  

## <a name="to-calculate-wip"></a>Slik beregner du VIA:
Du kan fastsette VIA-beløpet som skal bokføres på balansekonti for rapportering ved periodeslutt. Du bruker kjørselen **Beregn VIA for prosjekt** til å gjøre dette.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Beregn VIA for prosjekt**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Beregn VIA**.
3. På siden **Beregn VIA for prosjekt** fyller du ut feltene etter behov.
4. Velg **OK**.  

> [!NOTE]  
>   Kjørselen beregner bare VIA. De bokføres ikke i finans. Hvis du vil gjøre det, må du kjøre kjørselen **Bokfør VIA i Finans** når du har beregnet VIA. Hvis du vil ha mer informasjon, kan du se følgende fremgangsmåte:

## <a name="to-post-wip"></a>Slik bokfører du VIA
Når du har beregnet VIA, kan du bokføre VIA i balansekonti for rapporteringen ved periodens slutt. Du bruker kjørselen **Bokfør VIA i Finans for prosjekt** til å gjøre dette.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokfør VIA i Finans for prosjekt**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov på siden **Bokfør VIA i Finans for prosjekt**.  
3. Velg **OK**-knappen.

## <a name="to-calculate-and-post-job-completion-entries"></a>Slik beregner og bokfører du prosjektferdiggjørelsesposter
Når du har fullført alle aktiviteter for et prosjekt, inkludert bokføring og fakturering, må du oppdatere prosjektet for å sette **Status** til **Ferdig**. Deretter må du reversere alle VIA-er som er bokført i finans.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.  
2. Merk et åpent prosjekt, og velg handlingen **Rediger**.
3. I feltet **Status** velger du **Fullført**.
4. Følg hjelpetrinnene for å beregne og bokføre VIA. Alternativt følger du trinn 5 og 6 hvis du vil gjøre dette manuelt.  
5. Velg handlingen **Beregn VIA**.
6. På siden **Beregn VIA for prosjekt** fyller du ut feltene etter behov.  

     VIA-postene for prosjekt du oppretter ved å kjøre kjørselen, vil ha en avmerking i **Prosjekt ferdig**-boksen for å angi at de er ferdiggjørelsesposter.  
7. Velg handlingen **Bokfør VIA i Finans for prosjekt**.
8. Fyll ut feltene etter behov på siden **Bokfør VIA i Finans for prosjekt**.  

     VIA-finanspostene for prosjekt som du oppretter ved å kjøre kjørselen, vil ha en avmerking i **Prosjekt ferdig**-boksen for å angi at de er ferdiggjørelsesposter.

## <a name="to-view-job-ledger-entries"></a>Slik viser du prosjektposter
Alle prosjektrelaterte poster registreres i prosjektjournaler og nummereres fortløpende og starter med 1. I prosjektjournalen kan du få en oversikt over alle prosjektpostene.    

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektjournaler**, og velg deretter den relaterte koblingen.
2. Velg den relevante journalen, og velg deretter handlingen **Prosjektposter**.

På siden **Prosjektposter** kan du gå gjennom postene som er knyttet til et prosjekt.  

## <a name="see-also"></a>Se også
[Administrere prosjekter](projects-manage-projects.md)
[Administrere lagerkostnader](finance-manage-inventory-costs.md)   
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
