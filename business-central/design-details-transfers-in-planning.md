---
title: Utformingsdetaljer – Overføringer i planlegging
description: Finn ut hvordan du bruker overføringsordrer som en kilde for forsyning når du planlegger lagernivåer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.keywords: 'design, transfer, sku, locations, warehouse'
---
# <a name="design-details-transfers-in-planning"></a>Designdetaljer: Overføringer i planlegging

Overføringsordrer er også en kilde til forsyning når du arbeider på LFE-nivået. Når flere lokasjoner (lagre) brukes, kan Overfør angis for LFE-etterfyllingssystemet, som betyr at lokasjonen etterfylles ved å overføre varer fra en annen lokasjon. I en situasjon med flere lagre kan du ha en kjede med overføringer. Forsyning til GRØNN-lokasjon overføres fra GULT, forsyning til GULT overføres fra RØD og så videre. I begynnelsen av kjeden finnes etterfyllingssystemet **Prod.ordre.** eller **Kjøp**.  

![Eksempel på overføringsflyt.](media/nav_app_supply_planning_7_transfers1.png "Eksempel på overføringsflyt")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Hvis du sammenligner følgende situasjoner, er det tydelig at planleggingsoppgaven i sistnevnte kan bli komplisert:

* En forsyningsordre er direkte rettet mot en behovsordre
* En ordre angis gjennom en kjede av overføringer for lagerføringsenhet

Hvis behov endres, kan det føre til en bølgeeffekt gjennom kjeden. Alle overføringsordrer, pluss bestillingen og produksjonsordren i den motsatte enden av kjeden, må oppdateres for å balansere behov og forsyning på nytt.  

![Eksempel på balanse mellom tilbud og etterspørsel i overføringer.](media/nav_app_supply_planning_7_transfers2.png "Eksempel på balanse mellom tilbud og etterspørsel i overføringer")  

## <a name="why-is-a-transfer-a-special-case"></a>Hvorfor er overføring et spesialtilfelle?

Overføringsordrer ligner andre ordrer, som bestillinger og produksjonsordrer. I bakgrunnen er de imidlertid svært forskjellige.  

En forskjell er at en overføringslinje representerer både behov og forsyning. Den utgående delen som leveres, er etterspørsel. Den inngående delen, som skal mottas på den nye lokasjonen, er forsyning på denne lokasjonen.  

![Innholdet på siden Overføringsordre.](media/nav_app_supply_planning_7_transfers3.png "Innholdet på siden Overføringsordre")  

Når [!INCLUDE [prod_short](includes/prod_short.md)] endrer forsyningssiden av overføringen, må det gjøre en lignende endring på behovssiden.  

## <a name="transfers-are-dependent-demand"></a>Overføringer er avhengig av behov

Behovs- og forsyningsrelasjoner ligner komponentene på produksjonsordrelinjer. Forskjellen er at komponenter på produksjonsordrelinjer er på det neste planleggingsnivået og har en annen vare. De to delene av overføringen er på samme nivå for den samme varen.  

En viktig likheten er at komponentene og overføringer er avhengig av behov. Behov fra en overføringslinje bestemmes av forsyningssiden til overføringen. Hvis forsyningen endres, påvirkes behovet direkte.

Med mindre planleggingsfleksibiliteten er Ingen, må ikke en overføringslinje behandles som uavhengig behov i planleggingen.  

I fremgangsmåten for planlegging skal overføringsbehovet bare tas hensyn til når planleggingssystemet har behandlet forsyningssiden. Før behandlingen skjer, er ikke det faktiske behovet kjent. Rekkefølgen på endringer er viktig for overføringsordrer.  

## <a name="planning-sequence"></a>Planleggingsrekkefølge

Det følgende bildet viser et eksempel på en streng med overføringer.  

![Eksempel på enkel overføringsflyt.](media/nav_app_supply_planning_7_transfers4.png "Eksempel på enkel overføringsflyt")  

I dette eksemplet bestiller en kunde varen på GRØNN lokasjon. GRØNN lokasjon forsynes ved hjelp av overføring fra det sentrale lageret på RØD lokasjon. Det sentrale lageret i RØD lokasjon forsynes ved hjelp av overføring fra produksjon i BLÅ lokasjon.  

I dette eksemplet starter planleggingssystemet på kundebehovet og arbeide seg bakover gjennom kjeden. Behovene og forsyningene behandles for én lokasjon om gangen.  

![Forsyningsplanlegging med overføringer.](media/nav_app_supply_planning_7_transfers5.png "Forsyningsplanlegging med overføringer")  

## <a name="transfer-level-code"></a>Overføringsnivåkode

Overføringsnivåkoden for lagerføringsenhet bestemmer rekkefølgen som der planleggingssystemet behandler lokasjoner.  

Overføringsnivåkoden er et internt felt. Feltet beregnes og lagres på lagerføringsenheten når du oppretter eller endrer lagerføringsenheten. Beregningen kjøres på tvers av alle lagerføringsenheter for en gitt kombinasjon av vare og varevariant. Beregningen bruker lokasjonskoden og overfør-fra-koden til å angi hvilken rute som skal brukes for lagerføringsenhetene. Beregningen sikrer at alle behov behandles.  

Overføringsnivåkoden blir 0 for lagerførignsenheter med etterfyllingssystemet Kjøp eller Prod.ordre, og blir -1 for det første overføringsnivået, -2 for det andre og så videre. I eksempelet beskrevet i forrige del, vil nivåene være -1 for RØD og -2 for GRØNN, som vist i illustrasjonen nedenfor.  

![Innholdet på siden LFE-kort.](media/nav_app_supply_planning_7_transfers6.gif "Innholdet på siden LFE-kort")  

Når en lagerføringsenhet oppdateres, registrerer planleggingssystemet om etterfyllingssystemer for lagerføringsenheter har sirkelreferanser.  

## <a name="planning-transfers-without-sku"></a>Planleggingsoverføringer uten lagerføringsenhet

For mindre avanserte lageroppsett kan du bruke lokasjoner og foreta manuelle overføringer mellom lokasjoner, selv om du ikke bruker lagerføringsenheter. Overføringen kan for eksempel dekke en ordre på denne lokasjonen. Planleggingssystemet reagere på behovsendringer.  

For manuelle overføringer analyserer planleggingssystemet overføringsordrer og planlegger deretter rekkefølgen lokasjonene skal behandles i. Internt bruker planleggingssystemet midlertidige lagerføringsenheter som har overføringsnivåkoder.  

![Overføringsnivåkode.](media/nav_app_supply_planning_7_transfers7.png "Overføringsnivåkode")  

Hvis det finnes flere overføringer til en lokasjon, definerer den første overføringsordren planleggingsretningen. Overføringer i motsatt retning, blir avbrutt.  

## <a name="changing-quantity-with-reservations"></a>Endre antall med reservasjoner

Når du endrer antall på en forsyning, tar planleggingssystemet med reservasjoner i betraktning. Det reserverte antallet representerer nedre grense for hvor mye som skal redusere forsyningen.  

Når du endrer antallet på en overføringsordrelinje, må du tenke på den nedre grensen. Den nedre grensen er det høyeste reserverte antallet på de utgående og inngående overføringslinjene.

En overføringsordrelinje på 117 stykker er for eksempel reservert for følgende linjer:

* En ordrelinje på 46
* En kjøpslinje på 24

Selv om den inngående siden kan ha ekstra forsyning, kan du ikke redusere overføringslinjen under 46.  

![Reservasjoner i overføringsplanlegging.](media/nav_app_supply_planning_7_transfers8.png "Reservasjoner i overføringsplanlegging")  

## <a name="changing-quantity-in-a-transfer-chain"></a>Endre antall i en overføringskjede

Her er et eksempel på hva som skjer når du endrer antall i en overføringsendring.

Utgangspunktet er en balansert situasjon med en overføringskjede som gir en ordre på 27 til lokasjon RØD. Det finnes en tilsvarende bestilling på lokasjon BLÅ. Begge overføringene går gjennom lokasjonen ROSA. Det finnes to overføringsordrer, BLÅ-ROSA og ROSA-RØD.  

![Endre antallet i overføringsplanlegging 1.](media/nav_app_supply_planning_7_transfers9.png "Endre antallet i overføringsplanlegging 1")  

Planleggeren på ROSA lokasjon velger nå å reservere for kjøpet.  

![Endre antallet i overføringsplanlegging 2.](media/nav_app_supply_planning_7_transfers10.png "Endre antallet i overføringsplanlegging 2")  

Reservasjonen betyr vanligvis at planleggingssystemet ignorerer bestillingen og overføringsbehovet. Det er ikke et problem så lenge det er balanse. Men hva skjer når RØD lokasjon endrer rekkefølge fra 27 til 22?  

![Endre antallet i overføringsplanlegging 3.](media/nav_app_supply_planning_7_transfers11.png "Endre antallet i overføringsplanlegging 3")  

Når planleggingssystemet kjøres på nytt, skal det kunne bli kvitt overflødig forsyning. Reservasjonen låser imidlertid kjøp og overføring til antallet 27.  

![Endre antallet i overføringsplanlegging 4.](media/nav_app_supply_planning_7_transfers12.png "Endre antallet i overføringsplanlegging 4")  

ROSA-RØD-overføringen er redusert til 22. Den inngående delen av BLÅ-ROSA-overføring blir ikke reservert, men den utgående delen er. Reservasjonen betyr at du ikke kan redusere antallet under 27.  

## <a name="lead-time-calculation"></a>Beregning av leveringstid

Når forfallsdatoen for en overføringsordre beregnes, blir ulike typer leveringstid tatt med i betraktningen.  

Følgende leveringstider er aktive når du planlegger en overføringsordre:  

* Utgående lagerhåndteringstid  
* Leveringstid  
* Inngående lagerhåndteringstid  

Følgende felt brukes på planleggingslinjen til å gi informasjon om beregningen:  

* Overføringsforsendelsesdato  
* Startdato  
* Sluttdato  
* Forfallsdato  

Forsendelsesdatoen for overføringslinjen vises i felet **Overføringsforsendelsesdato**. Mottaksdatoen for overføringslinjen vises i felet **Forfallsdato**.  

Start- og sluttdatoene brukes til å beskrive den faktiske transportperioden.  

Følgende bilde viser tolkningen av startdato-tidspunkt og sluttdato-tidspunkt på planleggingslinjer for overføringsordrer.  

![Sentrale datoer og klokkeslett i overføringsplanlegging.](media/nav_app_supply_planning_7_transfers13.png "Sentrale datoer og klokkeslett i overføringsplanlegging")  

Eksempelet viser følgende beregninger:  

* Forsendelsesdato + utgående håndtering = startdato  
* Startdato + leveringstid = sluttdato  
* Sluttdato + inngående håndtering = mottaksdato  

## <a name="safety-lead-time"></a>Sikkerhetsleveringstid

Feltet **Standard sikkerhetstid** på **Produksjonsoppsett**-siden og det tilknyttede feltet **Sikkerhetsleveringstid** på siden **Varekort** er ikke inkludert i overføringsordreberegninger. Sikkerhetsleveringstiden påvirker imidlertid ikke den totale planen. Sikkerhetsleveringstiden påvirker etter fyllingsordren (kjøp eller produksjon) i begynnelsen av overføringskjeden. Det er det punktet der varene ble plassert i lokasjonen de overføres fra.  

![Elementer fra forfallsdato for overføring.](media/nav_app_supply_planning_7_transfers14.png "Elementer fra forfallsdato for overføring")  

På produksjonsordrelinjen er Sluttdato + Sikkerhetsleveringstid + Inngående lagerhåndteringstid = Forfallsdato.  

På bestillingslinjen er Planlagt mottaksdato + sikkerhetsleveringstid + inngående lagerhåndteringstid = forventet mottaksdato.  

## <a name="reschedule"></a>Tidsplanlegg på nytt

Når du planlegger en overføringslinje på nytt, finner planleggingssystemet den utgående delen og endrer dato og klokkeslett for den.

> [!NOTE]
> Hvis leveringstiden er angitt, vil det være et mellomrom mellom levering og mottak. Leveringstiden kan bestå av flere elementer, for eksempel transporttid og lagerhåndteringstid. På en tidslinje går planleggingssystemet tilbake i tid mens elementene balanseres.  

![Endre forfallsdatoen i overføringsplanlegging.](media/nav_app_supply_planning_7_transfers15.png "Endre forfallsdatoen i overføringsplanlegging")  

Når du endrer forfallsdatoen på en overføringslinje, må derfor leveringstiden beregnes for at den utgående siden av overføringen skal oppdateres.  

## <a name="serial-and-lot-numbers-in-transfer-chains"></a>Serie- og partinumrene i overføringskjeder

Hvis behovet bruker serie- eller partinumre og du kjører planleggingsmotoren, oppretter det overføringsordrer. Hvis du vil ha mer informasjon om dette konseptet, kan du se Vareattributter. Hvis imidlertid serie- eller partinumre fjernes fra etterspørselen, bruker overføringsordrene fortsatt serie- eller partinumre og planlegging ignorerer dem (slettes ikke).  

## <a name="order-to-order-links"></a>Odre-til-ordre-koblinger

I dette eksemplet defineres den BLÅ lagerføringsenhet med et **ordregjenbestillingsprinsipp**. De ROSA og RØDE lagerføringsenhetene er **Parti for parti**-gjenbestillingsprinsippet. Oppretting av en ordre på 27 til lokasjon RØD fører til en kjede med overføringer. Den siste overføringen er på lokasjonen BLÅ, og den er reservert med binding. I dette eksemplet er ikke reservasjoner faste reservasjoner som er opprettet av planleggeren på ROSA lokasjon. Planleggingssystemet oppretter bindingene. Den viktige forskjellen er at planleggingssystemet kan endre sistnevnte.  

![Ordre-til-ordre-koblinger i overføringsplanlegging.](media/nav_app_supply_planning_7_transfers16.png "Ordre-til-ordre-koblinger i overføringsplanlegging")  

Hvis behovet endrete fra 27 til 22, vil planleggingssystemet redusere antallet ned gjennom kjeden. Bindingsreservasjonen reduseres også.  

## <a name="see-also"></a>Se også

[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)   
[Designdetaljer: Tabell for planleggingstilordning](design-details-planning-assignment-table.md)   
[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)   
[Utformingsdetaljer: Planlegg med eller uten lokasjoner](production-planning-with-without-locations.md)   
[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
