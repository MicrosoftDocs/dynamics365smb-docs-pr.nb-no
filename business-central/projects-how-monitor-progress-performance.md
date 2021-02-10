---
title: Definere en VIA-metode og overvåke prosjektfremdrift | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en varer i arbeid (via)-metode og beregner VIA for å beregne den økonomiske verdien av prosjekter mens de er fortløpende.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 059df4f082e1e5a7dfee1f3dda8005e5e3099651
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758695"
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

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **VIA-metoder for prosjekt**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Lukk siden.   
4. Hvis du vil at denne nye metoden skal være standard, velger du ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Prosjektoppsett**, og velger deretter den relaterte koblingen.  
5. Velg metoden fra listen i feltet **Standard VIA-metode**.

## <a name="to-define-a-wip-method-for-a-job"></a>Slik definerer du en VIA-metode for et prosjekt:
Når du oppretter en nytt prosjekt, må du angi hvilken VIA-metode for prosjekt som gjelder. I enkelte tilfeller er VIA-metoden for prosjekt som du kan bruke, definert for deg som en standard.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjekter**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**. Hvis du vil ha mer informasjon, kan du se [Opprette prosjekter](projects-how-create-jobs.md).  
3. På siden **Prosjektkort** i feltet **VIA-metode** velger du en VIA-metode fra listen. Hvis en standardmetode er definert, kan du velge et annet alternativ etter behov.  

## <a name="to-calculate-wip"></a>Slik beregner du VIA:
Du kan fastsette VIA-beløpet som skal bokføres på balansekonti for rapportering ved periodeslutt. Du bruker kjørselen **Beregn VIA for prosjekt** til å gjøre dette.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Beregn VIA for prosjekt**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Beregn VIA**.
3. På siden **Beregn VIA for prosjekt** fyller du ut feltene etter behov.
4. Velg **OK**.  

> [!NOTE]  
>   Kjørselen beregner bare VIA. De bokføres ikke i finans. Hvis du vil gjøre det, må du kjøre kjørselen **Bokfør VIA i Finans** når du har beregnet VIA. Hvis du vil ha mer informasjon, kan du se følgende fremgangsmåte:

## <a name="to-post-wip"></a>Slik bokfører du VIA
Når du har beregnet VIA, kan du bokføre VIA i balansekonti for rapporteringen ved periodens slutt. Du bruker kjørselen **Bokfør VIA i Finans for prosjekt** til å gjøre dette.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokfør VIA i Finans for prosjekt**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov på siden **Bokfør VIA i Finans for prosjekt**.  
3. Velg **OK**.

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Slik viser du prosjektforbruksestimater og bokfører oppdateringer
Du kan vise prosjektforbruk i ett trinn helt frem til et prosjekt er fullført. Det gjør du ved å bruke kjørselen **Beregn gjenstående forbruk for prosjekt** for alle oppgavene til og med avslutningen av prosjektet.  

Dermed kan du spore og sammenligne opprinnelige estimater med faktiske resultater og om nødvendig gjøre endringer eller opprette nye poster. Tenk deg at du har estimert at et prosjekt tar 10 timer, men frem til nå har det tatt 15 timer. Du kan da legge til de fem ekstra timene på den eksisterende kladdelinjen, eller du kan opprette en ny kladdelinje for å rapportere disse fem timene som overtid, som er en annen arbeidstype. Riktig kost og pris beregnes, og du kan deretter bokføre i kladden.  

> [!NOTE]  
>   Vareposter oppretter vareposter og reduserer lagerantallet. Kjørselen **Bokfør lagerkost i Finans** overfører kosten fra lager til Finans. For ressurser opprettes ressursposter.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjektkladder**, og velg deretter den relaterte koblingen.  
2. Velg en journal for det aktuelle prosjektet, og velg deretter handlingen **Beregn gjenstående forbruk**.  
3. På siden **Beregn gjenstående forbruk for prosjekt** skriver du inn dokumentnummeret og bokføringsdatoen som skal settes inn i kladden, og deretter velger du **OK**-knappen.  
4. Oppdater journalen med eventuelle endringer som kreves.  
5. Velg **Bokfør**.

## <a name="to-view-job-ledger-entries"></a>Slik viser du prosjektposter
Alle prosjektrelaterte poster registreres i prosjektjournaler og nummereres fortløpende og starter med 1. I prosjektjournalen kan du få en oversikt over alle prosjektpostene.    

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjektjournaler**, og velg deretter den relaterte koblingen.
2. Velg den relevante journalen, og velg deretter handlingen **Prosjektposter**.

På siden **Prosjektposter** kan du gå gjennom postene som er knyttet til et prosjekt.  

## <a name="see-also"></a>Se også
[Administrere prosjekter](projects-manage-projects.md)
[Administrere lagerkostnader](finance-manage-inventory-costs.md)   
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
