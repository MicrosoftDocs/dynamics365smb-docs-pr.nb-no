---
title: Kjøre full planlegging, MPS og MRP
description: Planleggingssystemet kan beregne enten MPS (Master Planning Schedule) eller MRP (Material Requirements Planning) ved forespørsel, eller begge samtidig.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 73b40d3174497c05446d5b6ae6465f23a420f308
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6440331"
---
# <a name="run-full-planning-mps-or-mrp"></a>Kjøre full planlegging, MPS eller MRP
Uttrykket "kjøre planleggingsforslaget" eller "kjøre MRP" henviser til beregningen av hovedproduksjonsplanen og materialbehovene basert på faktisk og prognostisert behov. Planleggingssystemet kan beregne enten MPS (Master Planning Schedule) eller MRP (Material Requirements Planning) ved forespørsel, eller det kan beregne begge samtidig.  

-   MPS er beregningen av en hovedproduksjonsplan basert på faktisk behov og behovsprognosen. MPS-beregningen brukes for sluttvarer som har en prognose- og/eller ordrelinje. Disse varene kalles MPS-varer og identifiseres dynamisk når beregningen starter.  
-   MRP er beregningen av materialbehov basert på faktisk behov for komponenter og behovsprognosen på komponentnivå. MRP beregnes bare for varer som ikke er MPS-varer. Formålet med MRP er å lage formelle planer med tidsfaser, etter vare, for å kunne levere det riktige antallet av riktig vare til riktig sted på rett tidspunkt.  

Planleggingsalgoritmene som brukes til MPS og MRP, er identiske. Planleggingsalgoritmene gjelder nettoberegning, gjenbruk av eksisterende etterfyllingsordrer samt handlingsmeldinger. Planleggingssystemprosessen undersøker hva som trengs eller kommer til å trengs (behov), og hva som er på lager eller forventet (forsyning). Når disse antallene nettoberegnes mot hverandre, genererer [!INCLUDE[prod_short](includes/prod_short.md)] handlingsmeldinger. Handlingsmeldinger er forslag om å opprette en ny ordre, endre en ordre (antall eller dato) eller annullere en ordre som er bestilt. Betegnelsen "ordre" omfatter bestillinger, monteringsordrer, produksjonsordrer og overføringsordrer.

Koblinger som opprettes av planleggingsmotoren mellom etterspørsel og relatert forsyning, kan spores På siden **Sporing**. Hvis du vil ha mer informasjon, kan du se [Spore relasjoner mellom behov og forsyning](production-how-track-demand-supply.md).   

Riktige planleggingsresultater er avhengig av definisjonene i varekort, monteringsstykklister, produksjonsstykklister og ruter.  

## <a name="methods-for-generating-a-plan"></a>Metoder for å generere en plan  

-   **Beregn replanlegging**: Denne funksjonen behandler eller regenererer materialplanen. Denne prosessen starter ved å slette alle planlagte forsyningsordrer som er lastet inn. Alle varer i databasen planlegges på nytt.  
-   **Beregn bevegelsesplan**: Denne funksjonen behandler en bevegelsesplan. Varer behandles i bevegelsesplanlegging fra to typer endringer:  
    - **Behovs-/forsyningsendringer**: Dette inkluderer endringer av antall i ordrer, behovsprognoser, monteringsordrer, produksjonsordrer eller bestillinger. En endring i beholdningsnivået som ikke er planlagt, regnes også for å være en endring av antall.  
    - **Endringer av planleggingsparameter:** Dette inkluderer endringer av sikkerhetslager, gjenbestillingspunkt, rute og stykkliste og endringer av tidsperioden eller beregningen av leveringstid.  
-   **Hent handlingsmeldinger:** Denne funksjonen fungerer som et verktøy for planlegging på kort sikt ved å sende handlingsmeldinger for å varsle brukeren om eventuelle endringer som er gjort siden siste replanlegging eller bevegelsesplan ble beregnet.  

Med hver planlagte metode genererer [!INCLUDE[prod_short](includes/prod_short.md)] forslagsposter som forutsetter ubegrenset kapasitet. Det tas ikke hensyn til arbeidssenter- og produksjonsressurskapasitet når du utvikler tidsplaner.  

> [!IMPORTANT]  
>  Funksjonen Beregn replanlegging er den vanligste prosessen. Funksjonene for beregning av planer og utførelse av handlingsmeldinger, kan imidlertid brukes til å kjøre prosessen Beregn bevegelsesplan.  
>   
>  Funksjonen for planen Hent handlingsmeldinger kan kjøres mellom kjøringer av bevegelsesplanlegging og replanlegging for å få en oversikt over virkningen av planendringer, men er ikke ment å være en erstatning for fullstendige prosesser for bevegelsesplanlegging eller replanlegging.  

## <a name="to-calculate-the-planning-worksheet"></a>Slik beregner du planleggingsforslaget  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Planleggingsforslag**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Beregn replanlegging** for å åpne siden **Beregn Plan**.  
3.  I hurtigfanen **Alternativer** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**MPS**|Velg dette alternativet for å starte beregningen av hovedproduksjonsplan. Varer med åpne ordrer eller behovsprognoser behandles i denne kjøringen.|  
    |**MRP**|Velg dette alternativet for å starte beregningen av materialbehovsplanlegging. Varer med avhengige behov behandles i denne kjøringen. Vanligvis kjøres MPS og MRP samtidig. Hvis du vil kjøre MPS og MRP samtidig, merker du av for feltet **Kombinert MPS/MRP-beregning** på hurtigfanen **Planlegging** på **Produksjonsoppsett**-siden.|  
    |**Startdato**|Denne datoen brukes til å evaluere lagerbeholdningen. Hvis antallet på lager av en vare er under gjenbestillingspunktet, planlegger systemet en etterfyllingsordre fremover fra denne datoen. Hvis en vare er under sikkerhetslageret (per startdatoen), planlegger systemet en etterfyllingsordre bakover som forfaller på den planlagte startdatoen.|  
    |**Sluttdato**|Dette er sluttdatoen for planleggingshorisonten. Det tas hensyn til verken behov eller forsyning etter denne datoen. Hvis gjenbestillingssyklusen for en vare overskrider sluttdatoen, er den effektive planleggingshorisonten for denne varen lik ordredato + gjenbestillingssyklus.<br /><br /> Planleggingshorisonten er varigheten til planen. Hvis horisonten er for kort, bestilles ikke varer med en lengre leveringstid i tide. Hvis horisonten er for lang, brukes det for lang tid på gjennomgang og behandling av informasjon som sannsynligvis endres før det er behov for den. Det er mulig å angi én planleggingshorisont for produksjonen og en lengre for kjøp, men det er ikke nødvendig. En planleggingshorisont for kjøp og produksjon bør angis slik at den dekker samlet leveringstid for komponenter.|  
    |**Stopp og vis første feil**|Velg dette alternativet hvis du vil at planleggingskjøringen skal stoppe når det oppstår en feil. Samtidig vises en melding med informasjon om den første feilen. Hvis det oppstår en feil, vises bare feilfrie planleggingslinjer som ble behandlet før feilen oppstod, i planleggingsforslaget. Hvis du ikke velger dette feltet, fortsetter kjørselen **Beregn plan** til den er ferdig, det vil si at eventuelle feil ikke avbryter kjørselen. Hvis det oppstår feil, vises en melding når kjørselen er fullført, med informasjon om hvor mange varer som er berørt. Deretter åpnes siden **Feillogg planlegging** med ytterligere informasjon om feilen samt koblinger til berørte varekort.|  
    |**Bruk prognose**|Velg en prognose som skal tas med som behov når du utfører Planlegging-kjørselen. Standardprognosen defineres på hurtigfanen **Planlegging** på **Produksjonsoppsett**-siden.|  
    |**Utelat prognose før**|Angi hvor mye av den valgte prognosen som skal inkluderes i planleggingskjøringen, ved å angi en dato som prognosebehov ikke skal inkluderes før, slik at du dermed kan utelate gammel informasjon.|  
    |**Respekter planleggingsparametre for unntaksadvarsler**|Feltet er merket som standard.<br /><br /> Forsyning på planleggingslinjer med advarsler endres vanligvis ikke i henhold til planleggingsparametere. I stedet foreslår planleggingssystemet bare en forsyning for å dekke den nøyaktige behovsmengden. Du kan imidlertid definere visse planleggingsparametere for planleggingslinjer som det må ta hensyn til, med visse advarsler.<br /><br />|  

4.  På hurtigfanen **Vare** angir du filtre for å kjøre planleggingen basert på vare, varebeskrivelse eller lokasjon.  
5.  Velg **OK**-knappen. Kjørselen utføres, og deretter fylles planleggingsforslaget ut med planleggingslinjene  

## <a name="to-perform-action-messages"></a>Utføre handlingsmeldinger  
1.  På siden **Planleggingsforslag** velger du handlingen **Utfør handlingsmelding**.  
2.  På hurtigfanen **Alternativer** angir du hvordan forsyningene skal opprettes. Fyll ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Produksjonsordre**|Angi hvordan du vil opprette produksjonsordrer. Dette kan du gjøre direkte fra planleggingslinjeforslagene. Du kan opprette enten planlagte eller fast planlagte produksjonsordrer.|  
    |**Monteringsordre**|Angi hvordan du vil opprette monteringsordrer. Dette kan du gjøre direkte fra planleggingslinjeforslagene.|  
    |**Bestilling**|Angi hvordan du vil opprette bestillinger. Dette kan du gjøre direkte fra planleggingslinjeforslagene.<br /><br /> Hvis du velger å kopiere planleggingslinjeforslagene for bestillinger til bestillingsforslaget, velger du malen og forslagsnavnet.|  
    |**Overføringsordre**|Angi hvordan du vil opprette overføringsordrer. Dette kan du gjøre direkte fra planleggingslinjeforslagene.<br /><br /> Hvis du velger å kopiere planleggingslinjeforslagene for overføringsordrer til bestillingsforslaget, velger du malen og forslagsnavnet.|  
    |**Kombiner overføringsordrer**|Velg dette alternativet hvis du vil kombinere overføringsordrer.|  
    |**Stopp og vis første feil**|Velg dette alternativet hvis du vil at kjørselen **Utfør handlingsmelding - plan.** skal slutte når det oppstår en feil. Samtidig vises en melding med informasjon om den første feilen. Hvis det oppstår en feil, er det bare planleggingslinjer som ble behandlet før feilen oppstod, som genererer forsyningsordrer.|  

3.  På hurtigfanen **Planleggingslinje** kan du angi filtre for å begrense handlingsmeldingene som skal utføres.  
4.  Velg **OK**-knappen.  

Kjørselen sletter linjene i planleggingsforslaget etter at handlingsmeldingen er utført. De andre linjene beholdes i planleggingsforslaget til de godtas eller slettes. Du kan også slette linjene manuelt.  

## <a name="action-messages"></a>Handlingsmeldinger  
Handlingsmeldinger utstedes av sporingssystemet når balanse er uoppnåelig i det eksisterende ordrenettverket. De kan ses på som forslag om å behandle endringer som gjenoppretter balanse mellom forsyning og behov.  

Genereringen av handlingsmeldinger skjer på ett nivå om gangen for lavnivåkoden for hver vare. Dette sikrer at alle varer med forsyning eller behov som endres eller kommer til å bli endret, behandles.  

For å unngå små, overflødige eller uviktige handlingsmeldinger kan brukeren opprette filtre som begrenser genereringen av handlingsmeldinger til bare de endringene som overstiger det angitte antallet eller antallet dager.  

Når du har gått gjennom handlingsmeldingene og avgjort om du vil godta noen av eller alle de foreslåtte endringene, merker du av i feltet **Godta handlingsmelding**, og deretter er du klar til å oppdatere tidsplanene.  

> [!NOTE]  
>  En handlingsmelding er et forslag om å opprette en ny ordre, kansellere en ordre eller endre antallet eller datoen i en ordre. En ordre er en bestilling, overføringsordre eller produksjonsordre.  

Som følge av at forholdet mellom forsyning og behov ikke er i balanse, genereres følgende handlingsmeldinger.  

|Handlingsmelding|Beskrivelse|  
|--------------------|---------------------------------------|  
|**Ny**|Hvis et behov ikke kan dekkes ved å foreslå handlingsmeldingen **Endre ant.**, **Tidsplanlegg på nytt** eller **Tidsplanl. på nytt og endre ant.** i eksisterende ordrer, genereres handlingsmeldingen **Ny**, som foreslår en ny ordre. I tillegg utsteder systemet meldingen **Ny** hvis det ikke finnes eksisterende forsyningsordrer i den aktuelle varens gjenbestillingssyklus. Denne parameteren fastsetter antallet perioder fremover og bakover i tilgjengelighetsprofilen ved søk etter en ordre som skal tidsplanlegges på nytt.|  
|**Endre antall**|Når behovet som spores i en forsyningsordre, endres i antall, genereres handlingsmeldingen **Endre ant.**, som angir at den aktuelle forsyningen må endres i forhold endringen i behov. Hvis det oppstår et nytt behov, søker [!INCLUDE[prod_short](includes/prod_short.md)] etter den nærmeste eksisterende forsyningsordren i gjenbestillingssyklusen som ikke er reservert, og utsteder en handlingsmelding om endring for denne ordren.|  
|**Tidsplanlegg på nytt**|Når datoen i en forsynings- eller behovsordre endres slik at det oppstår en ubalanse i ordrenettverket, genereres handlingsmeldingen **Tidsplanlegg på nytt**. Hvis det er et én-til-én-forhold mellom behov og forsyning, genereres en handlingsmelding med forslag om å flytte forsyningsordren tilsvarende. Hvis forsyningsordrene dekker behovet for flere enn én ordre, tidsplanlegges forsyningsordren på nytt til datoen for det første behovet.|  
|**Tidsplan. på nytt og endre ant.**|Hvis både datoene og antallene i en ordre er endret, må du endre planer med hensyn til begge deler. Handlingsmeldingssystemet samler begge handlingene i én melding, **Tidsplanl. på nytt og endre ant.**, for å sikre at balansen i ordrenettverket gjenopprettes.|  
|**Kanseller**|Hvis et behov som har blitt dekket på en ordre-til-ordre-basis, slettes, genereres en handlingsmelding om å kansellere den aktuelle forsyningsordren. Hvis forholdet ikke er et ordre-til-ordre-forhold, genereres en handlingsmelding om å endre for å redusere forsyningen. Hvis det på grunn av andre faktorer, for eksempel lagerjusteringer, ikke er behov for en forsyningsordre når handlingsmeldingen genereres av brukeren, foreslår [!INCLUDE[prod_short](includes/prod_short.md)] handlingsmeldingen **Avbryt** i forslaget.|  

## <a name="see-also"></a>Se også  
[Planlegging](production-planning.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]