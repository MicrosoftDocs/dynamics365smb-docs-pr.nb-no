---
title: Overvåk prosjektfremdrift og -ytelse
description: Beskriver hvordan du kan opprette en VIA-metode (arbeid i arbeid) og beregne VIA for å beregne den økonomiske verdien av prosjekter mens de pågår.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 07/31/2024
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
ms.service: dynamics-365-business-central
---

# <a name="monitor-project-progress-and-performance"></a>Overvåk prosjektfremdrift og -ytelse

Med varer i arbeid (VIA) kan du beregne den økonomiske verdien av pågående prosjekter i finans.

Under fremdriften av et prosjekt forbrukes materialer og ressurser og utgifter som påløper, må bokføres til prosjektet. I mange tilfeller vil du kanskje bokføre utgifter for et prosjekt før du fakturerer. Men hvis bare utgifter er bokført, er årsregnskapet unøyaktig. Du kan spore den faktiske verdien av prosjektet ved å beregne VIA og bokføre det i finans. Finn ut mer under [Forstå VIA-metoder](projects-understanding-wip.md).

Du kan beregne VIA basert på følgende:

* Kostverdi
* Salgsverdi
* Gjenkjennelig kost
* Løpende
* Ved avslutning

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## <a name="create-a-project-wip-method"></a>Opprett en VIA-metode for prosjekt

Opprett en VIA-metode for prosjekt som oppfyller behovene i organisasjonen, og angi den som standardverdi.  

> [!NOTE]
> Når du har brukt den nye metoden til å opprette VIA-poster, kan ikke du endre eller slette metoden.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **VIA-metoder** for prosjekt, og velg deretter det relaterte opprette en kobling.  
2. Velg handlingen **Ny**, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Lukk siden.   
4. Hvis du bruke den nye metoden som standardmetode, velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Prosjektoppsett**, og velg deretter den relaterte opprette en kobling.  
5. Velg metoden fra listen i feltet **Standard VIA-metode**.

## <a name="define-a-wip-method-for-a-project"></a>Definer en VIA-metode for et prosjekt

Når du oppretter en nytt prosjekt, må du angi hvilken VIA-metode for prosjekt som gjelder. I noen tilfeller er VIA-metoden for prosjektet du bruker, allerede angitt som standard.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.
2. Velg handlingen **Ny**. Finn ut mer under [Opprett prosjekter](projects-how-create-jobs.md).  
3. På **siden Prosjekt kort**  i **feltet VIA-metode** på **hurtigfanen Bokføring** Velg du en VIA-metode fra listen. Hvis en standardmetode er definert, kan du velge et annet alternativ etter behov.  

### <a name="define-a-wip-method-for-a-project-task"></a>Definer en VIA-metode for en prosjektoppgave

Du kan definere en VIA-metode for en prosjektoppgave, utelate noen prosjektoppgaver fra VIA-beregning eller gruppere aktiviteter som skal beregnes sammen. 

Hvis du vil beregne VIA for hver prosjektoppgave individuelt, inneholder VIA-bokføring definerte dimensjoner for de bestemte oppgavene.

**VIA-sum** angir prosjektoppgavene du vil gruppere sammen under beregning av VIA og føring. I en gruppe med oppgaver må det alltid finnes én oppgave som oppfyller to betingelser:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Har **VIA-sum** satt til *Sum*. (Hvis det ikke finnes prosjektoppgaver der **Sum** er angitt for *VIA-sum*, angis *Sum* automatisk på siste prosjektoppgavelinje når VIA beregnes for første gang.)

* Har et **prosjektoppgavenr.** som er det siste i gruppen eller området med prosjektoppgaver.

Tabellen nedenfor beskriver de tre alternativene:

| Felt | Description |
|--|--|
| **\<blank\>** | La stå tomt hvis prosjektoppgaven er en del av en gruppe med oppgaver. |
| **I alt** | Definerer området eller gruppen med aktiviteter som er inkludert i beregningen av VIA og føringer. Alle prosjektoppgaver med **Prosjektoppgavetype** satt til **Bokføring** i gruppen, tas med i VIA-summen, med mindre oppgavens **VIA-sum**-felt er satt til **Utelatt**. |
| **Utelatt** | Gjelder bare en oppgave med **prosjektoppgavetypen** **bokføring**, og da blir ikke oppgaven tatt med når VIA og føring beregnes. |

I følgende eksempel er prosjektoppgaver delt inn i to VIA-sumgrupperinger, som viser hvordan feltet **VIA-sum** fungerer:

|Prosjektoppgavenr.|Beskrivelse|Prosjektoppgavetype|Feltet **VIA-sum**|  
|------------------|----------------------|----------------------|----------------------|  
|1 000|Forberedelse|Fra-sum|\<blank\>|
|1010|.    Rengjøring|Bokføring|**Utelatt**|
|1099|Forberedelse totalt|Til-sum|\<blank\>|
|1100|Teppelegging|Fra-sum|\<blank\>|
|1110|.    Lime gulv|Bokføring|**Utelatt**|
|1120|.    Legge på teppe|Bokføring|\<blank\>|
|1199|Teppelegging totalt|Til-sum|\<blank\>|
|1200|Ferdig|Fra-sum|\<blank\>|
|1210|.    Støvsuge teppe|Bokføring|\<blank\>|
|1299|Etterbehandling totalt|Til-sum|**I alt**|
|1300|Feilkorrigering|Fra-sum|\<blank\>|
|1310|.    Feilkorrigering|Bokføring|\<blank\>|
|1399|Feilkorrigering totalt|Til-sum|**I alt**|

Du vil se at:

* *1000* til *og med 1299*: VIA beregnes separat for denne gruppen med prosjektaktiviteter. Merk deg imidlertid at to av oppgavene, 1010 og 1110, er utelatt fra VIA-beregningen, fordi prosjektoppgavetypen er **Bokføring**.

* *1300* til og med *1399*: VIA beregnes separat for denne gruppen med prosjektaktiviteter.

## <a name="calculate-wip"></a>Beregn VIA

Du kan fastsette VIA-beløpet som skal bokføres på balansekontoer for rapportering ved periodeslutt. Bruk kjørselen **Beregn VIA for prosjekt** til å gjøre dette.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Prosjektberegn VIA**, og velg deretter det relaterte opprette en kobling.  
2. Velg handlingen **Beregn VIA**.
3. På siden **Beregn VIA for prosjekt** fyller du ut feltene etter behov.
4. Velg **OK**-knappen.  

> [!NOTE]  
> Kjørselen beregner bare VIA, den bokfører den ikke i finans. Hvis du vil bokføre den, må du kjøre kjørselen **Bokfør VIA i Finans** etter at du har beregnet VIA. Finn ut mer i fremgangsmåten nedenfor.

## <a name="post-wip"></a>Bokfør VIA

Når du har beregnet VIA, kan du bokføre VIA i balansekontoer for rapporteringen ved periodens slutt. Du bruker kjørselen **Bokfør VIA i Finans for prosjekt** til å gjøre dette.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokfør VIA i Finans for prosjekt**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov på siden **Bokfør VIA i Finans for prosjekt**.  
3. Velg **OK**-knappen.

## <a name="calculate-and-post-project-completion-entries"></a>Beregn og bokfør prosjektferdiggjørelsesposter

Når du har fullført alle aktiviteter for et prosjekt, inkludert bokføring og fakturering, må du oppdatere prosjektet for å sette statusen til **Ferdig**. Deretter må du reversere alle VIA-er som er bokført i finans.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.  
2. Merk et åpent prosjekt, og velg handlingen **Rediger**.
3. På **hurtigfanen Bokføring** i Status-feltet **Velg** **Fullført**.
4. Følg hjelpetrinnene for å beregne og bokføre VIA, eller følg trinn 5 og 6 for å gjøre dette manuelt.  
5. Velg handlingen **Beregn VIA**.
6. På siden **Beregn VIA for prosjekt** fyller du ut feltene etter behov.  

     VIA-postene for prosjekt som opprettes ved å kjøre kjørselen, har merket av for **Prosjekt fullført** for å vise at de er ferdiggjørelsesposter.  
7. Velg handlingen **Bokfør VIA i Finans for prosjekt**.
8. Fyll ut feltene etter behov på siden **Bokfør VIA i Finans for prosjekt**.  

     VIA-finanspostene for prosjekt som opprettes ved å kjøre kjørselsprosjektet, har merket av for **Prosjekt fullført** for å vise at de er ferdiggjørelsesposter.

## <a name="view-project-ledger-entries"></a>Vis prosjektposter

Alle prosjektrelaterte poster registreres i prosjektjournaler og nummereres fortløpende og starter med 1. I prosjektjournalen kan du få en oversikt over alle prosjektpostene.    

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektjournaler**, og velg deretter den relaterte koblingen.
2. Velg den relevante journalen, og velg deretter handlingen **Prosjektposter**.

På siden **Prosjektposter** kan du gå gjennom postene som er knyttet til et prosjekt.  

## <a name="see-also"></a>Se også

[Gjennomgang - beregne pågående arbeid for et prosjekt](walkthrough-calculating-work-in-process-for-a-job.md)    
[Administrere prosjekter](projects-manage-projects.md)    
[Administrere lagerkostnader](finance-manage-inventory-costs.md)    
[Finans](finance.md)    
[Innkjøp](purchasing-manage-purchasing.md)    
[Salg](sales-manage-sales.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
