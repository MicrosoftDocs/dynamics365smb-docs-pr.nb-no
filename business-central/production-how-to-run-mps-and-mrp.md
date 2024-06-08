---
title: 'Kjøre full planlegging, MPS eller MRP'
description: 'Planleggingssystemet kan beregne enten MPS (Master Production Schedule) eller MRP (Material Requirements Planning) ved forespørsel, eller begge samtidig.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: '99000852, 99000860'
ms.date: 01/24/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="run-full-planning-mps-or-mrp"></a>Kjøre full planlegging, MPS eller MRP

Uttrykket «kjøre planleggingsforslaget» eller «kjøre MRP» henviser til beregningen av hovedproduksjonsplanen og materialbehovene. Beregningen er basert på faktisk og forutsagt behov. Planleggingssystemet kan beregne enten MPS (Master Production Schedule) eller MRP (Material Requirements Planning) ved forespørsel, eller begge samtidig.  

- MPS er beregningen av en hovedproduksjonsplan basert på faktisk behov og behovsprognosen. MPS-beregningen brukes for sluttvarer som har en prognose- og/eller ordrelinje. Disse varene kalles MPS-varer og identifiseres dynamisk når beregningen starter.  
- MRP er beregningen av materialbehov basert på faktisk behov for komponenter og behovsprognosen på komponentnivå. MRP beregnes bare for varer som ikke er MPS-varer. Formålet med MRP er å lage formelle planer med tidsfaser, etter vare, for å kunne levere det riktige antallet av riktig vare til riktig sted og på rett tidspunkt.  

Planleggingsalgoritmene som brukes til MPS og MRP, er like. Algoritmene gjelder nettoberegning, gjenbruk av eksisterende etterfyllingsordrer samt handlingsmeldinger. Planleggingssystemprosessen undersøker hva som trengs eller kommer til å trengs (behov), og hva som er på lager eller forventet (forsyning). Når du nettoberegner disse antallene mot hverandre, genererer [!INCLUDE[prod_short](includes/prod_short.md)] handlingsmeldinger. Handlingsmeldinger er forslag om å opprette en ny ordre, endre en ordre (antall eller dato) eller annullere en ordre. Betegnelsen "ordre" omfatter bestillinger, monteringsordrer, produksjonsordrer og overføringsordrer.

Du kan spore koblingene som planleggingen oppretter mellom etterspørsel og forsyning på siden **Ordresporing**. Hvis du vil ha mer informasjon, kan du se [Spore relasjoner mellom behov og forsyning](production-how-track-demand-supply.md).

Riktige planleggingsresultater er avhengig av definisjonene i varekort, monteringsstykklister, produksjonsstykklister og ruter.  

## <a name="methods-for-generating-a-plan"></a>Metoder for å generere en plan

- **Beregn replanlegging**: Behandle eller regenerer materialplanen. Denne prosessen starter ved å slette alle planlagte forsyningsordrer som er lastet inn. Alle varer i databasen planlegges på nytt.  
- **Beregn bevegelsesplan**: Behandle en bevegelsesplan. Varer behandles i bevegelsesplanlegging fra to typer endringer:  
   - **Behovs-/forsyningsendringer**: Disse endringene inkluderer endringer av antall i ordrer, behovsprognoser, monteringsordrer, produksjonsordrer eller bestillinger. En endring i beholdningsnivået som ikke er planlagt, regnes også for å være en endring av antall.  
   - **Endringer av planleggingsparameter:** Disse endringene inkluderer endringer av sikkerhetslager, gjenbestillingspunkt, rute og stykkliste og endringer av tidsperioden eller beregningen av leveringstid.  
- **Hent handlingsmeldinger:** Fungerer som et verktøy for planlegging på kort sikt ved å sende handlingsmeldinger for å varsle brukeren om eventuelle endringer som er gjort siden siste gang du beregnet en regenerering eller bevegelsesplan.  

Med hver planlagte metode genererer [!INCLUDE[prod_short](includes/prod_short.md)] forslagsposter som forutsetter ubegrenset kapasitet. Det tas ikke hensyn til arbeidssenter- og produksjonsressurskapasitet når du utvikler tidsplaner.  

> [!IMPORTANT]  
> Beregn replanlegging er den vanligste prosessen. Beregning av planer og utførelse av handlingsmeldinger kan imidlertid brukes til å kjøre prosessen Beregn bevegelsesplan.  
>
> Du kan kjøre planen Hent handlingsmeldinger mellom regenerative kjøringer og nettoendringsplanleggingskjøringer for å få en umiddelbar oversikt over effekten av planendringer. Det er imidlertid ikke ment å erstatte de fullstendige regenerative eller nettoendringsplanleggingsprosessene.  

## <a name="to-calculate-the-planning-worksheet"></a>Slik beregner du planleggingsforslaget
  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Planleggingsforslag**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Beregn replanlegging** for å åpne siden **Beregn Plan**.  
3. I hurtigfanen **Alternativer** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**MPS**|Beregn en hovedproduksjonsplan. Varer med åpne ordrer eller behovsprognoser behandles i denne kjøringen. <br/>Hvis det også finnes andre behov, for eksempel sikkerhetslager, gjenbestillingspunkt eller åpne produksjonskomponentlinjer for slike varer, tas disse behovene med i MPS-beregningen for å sikre at planleggingssystemet håndterer hele lagerprofilen.  |  
    |**MRP**|Beregn materialplanleggingsbehov Varer med avhengige behov behandles i denne kjøringen. Vanligvis kjøres MPS og MRP samtidig. Hvis du vil kjøre MPS og MRP samtidig, merker du av for feltet **Kombinert MPS/MRP-beregning** på hurtigfanen **Planlegging** på **Produksjonsoppsett**-siden.|  
    |**Startdato**|Evaluer lagertilgjengelighet. Hvis antallet på lager av en vare er under gjenbestillingspunktet, planlegger systemet en etterfyllingsordre fremover fra denne datoen. Hvis en vare er under sikkerhetslageret (per startdatoen), planlegger systemet en etterfyllingsordre bakover som forfaller på den planlagte startdatoen.|  
    |**Sluttdato**|Sluttdatoen for planleggingshorisonten. Det tas hensyn til verken behov eller forsyning etter denne datoen. Hvis gjenbestillingssyklusen for en vare overskrider sluttdatoen, er den effektive planleggingshorisonten for denne varen lik ordredato pluss gjenbestillingssyklus.<br/><br/> Planleggingshorisonten er varigheten til planen. Hvis horisonten er for kort, bestilles ikke varer med en lengre leveringstid i tide. Hvis horisonten er for lang, brukes det for lang tid på gjennomgang og behandling av informasjon som sannsynligvis endres før det er behov for den. Du kan angi en planleggingshorisont for produksjonen og en lengre for kjøp, men det er ikke nødvendig. En planleggingshorisont for kjøp og produksjon bør angis slik at den dekker total leveringstid for komponenter.|  
    |**Stopp og vis første feil**|Velg dette alternativet hvis du vil at planleggingskjøringen skal stoppe når det oppstår en feil. En melding vises med informasjon om feilen. Hvis det oppstår en feil, vises bare feilfrie planleggingslinjer som ble behandlet før feilen oppstod, i planleggingsforslaget. Hvis du ikke velger dette feltet, fortsetter satsjobben **Beregn plan** til den er fullført. Feil avbryter ikke den satsvise jobben. Hvis det oppstår feil, vises en melding når satsjobben er fullført, med informasjon om hvor mange varer som er berørt. Deretter åpnes siden **Feillogg planlegging** med ytterligere informasjon om feilen samt koblinger til berørte varekort.|  
    |**Bruk prognose**|Velg en prognose som skal tas med som behov når du utfører Planlegging-kjørselen. Standardprognosen defineres på hurtigfanen **Planlegging** på **Produksjonsoppsett**-siden.|  
    |**Utelat prognose før**|Definer hvor mye av den valgte prognosen som skal inkluderes i planleggingskjøringen, ved å angi en dato som prognosebehovet ikke er inkludert før.|  
    |**Respekter planleggingsparametre for unntaksadvarsler**|Feltet er merket som standard.<br/><br/> Forsyning på planleggingslinjer med advarsler endres vanligvis ikke i henhold til planleggingsparametere. I stedet foreslår planleggingssystemet bare en forsyning for å dekke den nøyaktige behovsmengden. Du kan imidlertid definere visse planleggingsparametere for planleggingslinjer som det må ta hensyn til, med visse advarsler.<br/><br/>|  

4. På hurtigfanen **Vare** angir du filtre for å kjøre planleggingen basert på varen, varebeskrivelsen eller lokasjonen.  
5. Velg **OK**-knappen. Satsjobben kjøres og planleggingslinjene legges til i planleggingsforslaget.  

## <a name="to-perform-action-messages"></a>Utføre handlingsmeldinger
  
1. På siden **Planleggingsforslag** velger du handlingen **Utfør handlingsmelding**.  
2. På hurtigfanen **Alternativer** angir du hvordan forsyningene skal opprettes. Fyll ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Produksjonsordre**|Angi hvordan produksjonsordrer skal opprettes. Dette kan du gjøre direkte fra planleggingslinjeforslagene. Du kan opprette enten planlagte eller fast planlagte produksjonsordrer.|  
    |**Monteringsordre**|Angi hvordan du oppretter monteringsordrer. Dette kan du gjøre direkte fra planleggingslinjeforslagene.|  
    |**Bestilling**|Angi hvordan du oppretter bestillinger. Dette kan du gjøre direkte fra planleggingslinjeforslagene.<br/><br/> Hvis du velger å kopiere planleggingslinjeforslagene for bestillinger til bestillingsforslaget, velger du malen og forslagsnavnet.|  
    |**Overføringsordre**|Angi hvordan du oppretter overføringsordrer. Dette kan du gjøre direkte fra planleggingslinjeforslagene.<br/><br/> Hvis du velger å kopiere planleggingslinjeforslagene for overføringsordrer til bestillingsforslaget, velger du malen og forslagsnavnet.|  
    |**Kombiner overføringsordrer**|Velg om du vil kombinere overføringsordrer.|  
    |**Stopp og vis første feil**|Velg dette alternativet hvis du vil at satsjobben **Utfør handlingsmelding - plan.** skal slutte når den finner en feil. En melding viser informasjon om feilen. Hvis det oppstår en feil, er det bare planleggingslinjer som ble behandlet før feilen ble funnet, som genererer forsyningsordrer.|  

3. På hurtigfanen **Planleggingslinje** kan du angi filtre for å begrense handlingsmeldingene som skal utføres.  
4. Velg **OK**-knappen.  

Kjørselen sletter linjene i planleggingsforslaget etter at handlingsmeldingen er utført. De andre linjene beholdes i planleggingsforslaget til de godtas eller slettes. Du kan også slette linjene manuelt.  

## <a name="action-messages"></a>Handlingsmeldinger
  
Handlingsmeldinger utstedes av sporingssystemet når balanse er uoppnåelig i det eksisterende ordrenettverket. Meldingene kan ses på som forslag om å behandle endringer som gjenoppretter balanse mellom forsyning og behov.  

Genereringen av handlingsmeldinger skjer på ett nivå om gangen for lavnivåkoden for hver vare. Dette sikrer at alle varer med forsyning eller behov som endres eller kommer til å bli endret, behandles.  

For å unngå små, unødvendige eller uviktige handlingsmeldinger kan du angi filtre som begrenser genereringen av handlingsmeldinger til bare de endringene som overstiger det angitte antallet eller antallet dager.  

Når du har gått gjennom handlingsmeldingene og avgjort om du vil godta noen av eller alle de foreslåtte endringene, merker du av i feltet **Godta handlingsmelding**. Deretter oppdaterer du tidsplanene tilsvarende.  

> [!NOTE]  
> En handlingsmelding er et forslag om å opprette en ny ordre, kansellere en ordre eller endre antallet eller datoen i en ordre. En ordre er en bestilling, overføringsordre eller produksjonsordre.  

Som følge av at forholdet mellom forsyning og behov ikke er i balanse, genereres følgende handlingsmeldinger.  

|Handlingsmelding|Beskrivelse|  
|--------------------|---------------------------------------|  
|**Ny**|Hvis et behov ikke kan dekkes ved å foreslå handlingsmeldingen **Endre ant.**, **Tidsplanlegg på nytt** eller **Tidsplanl. på nytt og endre ant.** i eksisterende ordrer, genereres handlingsmeldingen **Ny** for å foreslå en ny ordre. Meldingen **Ny** genereres også hvis det ikke er noen forsyningsordrer i den aktuelle varens gjenbestillingssyklus. Dette alternativet fastsetter antallet perioder fremover og bakover i tilgjengelighetsprofilen ved søk etter en ordre som skal tidsplanlegges på nytt.|  
|**Endre antall**|Når antallet endres for et behov som spores til en forsyningsordre, genereres handlingsmeldingen **Endre ant.**. Meldingen angir at den aktuelle forsyningen må endres i forhold endringen i behov. Hvis det oppstår et nytt behov, søker [!INCLUDE[prod_short](includes/prod_short.md)] etter den nærmeste eksisterende forsyningsordren i gjenbestillingssyklusen som ikke er reservert, og utsteder en handlingsmelding om endring for denne ordren.|  
|**Planlegg på nytt**|Når en datoendring for en forsynings- eller behovsordre fører til en ubalanse i ordrenettverket, genereres handlingsmeldingen **Tidsplanlegg på nytt**. Hvis det er et én-til-én-forhold mellom behov og forsyning, genereres en handlingsmelding for å foreslå at du flytter forsyningsordren. Hvis forsyningsordrene dekker behovet for flere enn én ordre, tidsplanlegges forsyningsordren på nytt til datoen for det første behovet.|  
|**Tidsplan. på nytt og endre ant.**|Hvis både datoene og antallene i en ordreendring, må du endre planer med hensyn til begge deler. Handlingsmeldingssystemet samler begge handlingene i én melding, **Tidsplanl. på nytt og endre ant.**, for å sikre at balansen i ordrenettverket gjenopprettes.|  
|**Kanseller**|Hvis et behov som har blitt dekket på en ordre-til-ordre-basis, slettes, genereres en handlingsmelding om å kansellere den aktuelle forsyningsordren. Hvis forholdet ikke er et ordre-til-ordre-forhold, genereres en handlingsmelding om å endre for å redusere forsyningen. Hvis det på grunn av andre faktorer, for eksempel lagerjusteringer, ikke er behov for en forsyningsordre når du genererer handlingsmeldingen, foreslår [!INCLUDE[prod_short](includes/prod_short.md)] handlingsmeldingen **Avbryt** i forslaget.|  

## <a name="see-also"></a>Se også

[Planlegging](production-planning.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
