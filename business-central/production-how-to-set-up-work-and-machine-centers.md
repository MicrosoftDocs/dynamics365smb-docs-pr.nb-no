---
title: Konfigurer arbeidssentre og produksjonsressurser
description: Et Arbeidssenter-kort inneholder de faste verdiene og kravene til den aktuelle produksjonsressursen og styrer dermed avgangen for produksjonen som utføres i arbeidssenteret.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000754, 99000755, 99000756, 99000758, 99000760, 99000761, 99000762'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Konfigurer arbeidssentre og produksjonsressurser

[!INCLUDE [prod_short](includes/prod_short.md)] skiller mellom tre typer kapasiteter som er arrangert i et hierarki, der hvert nivå inneholder underordnede nivåer.  

Det øverste nivået er arbeidssentergruppen. Arbeidssentre er tilordnet arbeidssentergrupper. Hvert arbeidssenter kan bare tilhøre én arbeidssentergruppe.

Du kan tilordne forskjellige produksjonsressurser til arbeidssentre. En produksjonsressurs kan bare tilhøre ett arbeidssenter.  

Planlagt kapasitet i et arbeidssenter består av hvor tilgjengelige tilhørende produksjonsressurser er og planlagt tilgjengelighet i arbeidssenteret. Den planlagte tilgjengeligheten i arbeidssentergruppen er derfor summen av all tilhørende tilgjengelighet i produksjonsressursene og arbeidssentrene. Tilgjengeligheten lagres i kalenderposter.  

> [!IMPORTANT]
> Før du definerer arbeidssentre eller produksjonsressurser, må du definere produksjonskalendere. Hvis du vil ha mer informasjon, kan du se [Opprette produksjonskalendere](production-how-to-create-work-center-calendars.md).

## Slik oppretter du et arbeidssenter:

Trinnene nedenfor beskriver hvordan du definerer et arbeidssenter. Fremgangsmåten for å sette opp en produksjonsressurskalender er lik unntatt hurtigfanen **Ruteoppsett**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Arbeidssentre**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg eventuelt ressursgruppen på et høyere nivå som arbeidssenteret er organisert under, i feltet **Arbeidssentergruppekode**. Velg **Ny**-handlingen i rullegardinlisten.  
5. I feltet **Alternativt arbeidssenter** velger du arbeidssenteret som skal brukes hvis dette arbeidssenteret ikke er tilgjengelig, eller når behovet overskrider kapasiteten. Det alternative arbeidssenteret er bare til informasjonsbruk og tas ikke automatisk med i planleggingsprosessene.
6. Velg **Sperret**-feltet hvis du vil hindre at arbeidssenteret brukes i behandling. Dette betyr at det ikke kan bokføres avgang for en vare som er produsert ved arbeidssenteret. Hvis du vil ha mer informasjon, kan du se [Bokføre produksjonsutgang](production-how-to-post-output-quantity.md).
7. I feltet **Direkte enhetskost** registrerer du kostnaden av å produsere én enhet ved dette arbeidssenteret, ekskludert andre kostnadselementer. Denne kostnaden kalles ofte *direkte lønnssats*.  
8. I feltet **Indirekte kost-%** angir du de generelle operasjonskostnadene som løper ved bruk av arbeidssenteret, som en prosentandel av den direkte enhetskostnaden. Denne prosentandelen legges til i direktekostnaden i beregningen av enhetskostnaden.  
9. I feltet **Sats for indirekte kostnader** registrerer du ikke-operasjonelle kostnader, for eksempel vedlikeholdsutgifter, for arbeidssenteret som et absolutt beløp.  

    **Enhetskost**-feltet inneholder den beregnede enhetskostnaden for å produsere én enhet ved dette arbeidssenteret, inkludert alle kostnadselementer slik:  

    Enhetskostnad = Direkte enhetskostnad + (Direkte enhetskostnad x Indirekte kostnad-%) + Sats for indirekte kostnader.  

10. I feltet **Beregning av enhetskost** definerer du om beregningen av enhetskost skal baseres på medgått tid eller på antall produserte enheter.  
11. Velg feltet **Bestemt enhetskost** hvis du vil definere arbeidssenterets kostnad på rutelinjen der den brukes. Denne innstillingen kan være relevant for operasjoner med kapasitetskostnader som er forskjellig fra det du normalt ville ha behandlet ved arbeidssenteret.  
12. I **Trekkmetode**-feltet velger du om du skal beregne og bokføre avganger manuelt eller automatisk ved dette arbeidssenteret ved å bruke én av følgende metoder.

    |Alternativ|Description|
    |------|-----------|
    |**Åpen post**| Bokfør brukt tid, utdata og svinn manuelt i ferdigmeldingskladden eller produksjonskladden.|
    |**Fremover**|Ferdigmeldinger bokføres automatisk når du frigir produksjonsordren.|
    |**Bakover**|Ferdigmeldinger bokføres automatisk når du fullfører produksjonsordren.|

    > [!NOTE]
    > Om nødvendig kan trekkmetoden som velges her, overstyres for individuelle operasjoner ved å endre innstillingen på rutelinjene

13. I **Enhetskode**-feltet registrerer du tidsenheten som arbeidssenterets kostnadsberegning og kapasitetsplanlegging beregnes i.
    Du må først definere en enhetsmetode for å kunne kontrollere forbruk konstant. Enhetene du angir, er basisenheter. Behandlingstiden, for eksempel, beregnes i timer og minutter.

    > [!NOTE]  
    > Hvis du bruker dager, må du huske at én dag er 24 timer, og ikke en åtte timers arbeidsdag.

14. I **Kapasitet**-feltet definerer du om arbeidssenteret har mer enn én maskin eller person som arbeider samtidig. Hvis Produksjonsressurs-funksjonaliteten ikke inngår i din installasjon av [!INCLUDE[prod_short](includes/prod_short.md)], må verdien i dette feltet være **1**.  
15. I **Effektivitet**-feltet registrerer du prosentandelen for den forventede standardavgangen som dette arbeidssenteret faktisk produserer. Hvis du skriver inn **100**, betyr det at arbeidssenteret har en faktisk avgang som er den samme som standardavgangen.  
16. Merk av for **Konsolidert kalender** hvis du også bruker produksjonsressurser. Denne innstillingen sikrer at kalenderposter blir opprullert på bakgrunn av produksjonsressurskalendere.  
17. Velg en produksjonskalender i feltet **Produksjonskalenderkode**. Hvis du vil ha mer informasjon, kan du se [Opprette produksjonskalendere](production-how-to-create-work-center-calendars.md).  
18. I **Køtid**-feltet angir du en fast tidsrom som må forløpe før tilordnet arbeid kan begynne ved dette arbeidssenteret. 

> [!NOTE]
> Bruk køtid til å angi en buffer mellom tiden som en komponent ankommer ved en produksjonsressurs eller arbeidssenter, og når operasjonen faktisk starter. En del leveres for eksempel til en produksjonsressurs på 10:00, men det tar en time å montere den på maskinen, slik at operasjonen ikke starter før 11,00. For å ta med denne timen vil køtiden være én time. Verdien i feltet **Køtid** på et produksjonsressurskort eller arbeidssenterkortet, pluss summen av verdiene i feltene **Oppstillingstid**, **Operasjonstid**, **Ventetid** og **Transporttid** på varerutelinjen slås sammen for å få leveringstiden for varen. Dette bidrar til å gi nøyaktig total produksjonstid.  

## Hensyn til kapasiteten

Kapasiteten og effektiviteten for et arbeidssenter og en produksjonsressurs, påvirker mer enn bare tilgjengelig kapasitet. Verdiene påvirker også den generelle produksjonstiden som består av oppstillingstid og operasjonstid, som begge er definert på rutelinjen.  

Når du tildeler en rutelinje til et arbeidssenter eller en produksjonsressurs, beregner [!INCLUDE [prod_short](includes/prod_short.md)] følgende:

- Hvor mye kapasitet som trengs.
- Hvor lang tid det tar å fullføre operasjonen.  

### Operasjonstid

For å beregne operasjonstiden tildeler systemet nøyaktig den tiden som er definert i feltet **Operasjonstid** for rutelinjen. Effektivitet og kapasitet virker ikke inn på den tildelte tiden. Hvis for eksempel operasjonstiden er definert som to timer, vil den tildelte tiden være to timer, uavhengig av verdiene i feltene effektivitet og kapasitet i arbeidssenteret.  

> [!NOTE]
> Kapasiteten som brukes i beregningene, er definert som minimumsverdi mellom kapasiteten som er definert i arbeidssenteret eller produksjonsressursen, og samtidig kapasitet som er definert for rutelinjen. Hvis et arbeidssenter har en kapasitet på 100, men samtidig kapasitet for rutelinjen er to, brukes *2* i beregningene.

*Varigheten* av en operasjon tar derimot hensyn til både effektivitet og kapasitet. Varighet beregnes som *operasjonstid/effektivitet/kapasitet*. Følgende oversikt viser noen eksempler på beregning av varighet for samme operasjonstid, som er definert som to timer for rutelinjen:

- Effektivitet 80 % betyr at du trenger 2,5 timer i stedet for to timer  
- Effektivitet 200 % betyr at du kan fullføre arbeidet på en time. Du kan grave hullet dobbelt så raskt hvis du har en gravemaskin som er dobbelt så stor som den minste  

    Du kan få samme resultat hvis du bruker to mindre gravemaskiner i stedet for en stor. Bruk *2* som kapasitet og *100 %* som effektivitet  

Fraksjonskapasitet er vanskelig. Vi skal diskutere det senere i denne artikkelen. 

### Oppstillingstid

Tidstilordning for oppstillingstiden avhenger av kapasiteten og beregnes som *oppstillingstid * kapasitet*. Hvis for eksempel kapasiteten er satt til *2*, fordobles den tilordnede oppstillingstiden fordi du må definere to maskiner for operasjonen.  

*Varigheten* av oppstillingstiden avhenger av effektivitet og beregnes som *tid/effektivitet for oppsettet*. 

- Effektivitet 80 % betyr at du trenger 2,5 timer i stedet for to timer 2 oppsettet.  
- Effektivitet 200 % betyr at du kan fullføre oppsettet på 1 time i stedet for 2 timer definert på rutelinjen  

Fraktalkapasiteten brukes kun i spesielle tilfeller.

### Arbeidssenter behandler flere ordrer samtidig

La oss bruke et maleappart som eksempel. Det har samme oppsett og operasjonstider for hvert behandlede parti. Men hvert parti kan inneholde flere individuelle bestillinger som kan males samtidig.  

I dette tilfellet håndterer oppstillingstiden og samtidig kapasitet kostnadene som tildeles ordrer. Vi anbefaler at du ikke bruker operasjonstiden på rutelinjer.  

Den tilordnede oppstillingstiden for hver enkelt ordre blir i motsatt rekkefølge av antall ordrer (mengder) som utføres samtidig. Her er noen eksempler på beregning av oppstillingstid når det er definert som to timer for rutelinjen:

- Hvis det finnes to ordrer, bør samtidig kapasitet på rutelinjen settes til 0,5.

    Som et resultat av dette er den tildelte kapasiteten for hver enkelt én time, men varigheten for hver ordre forblir to timer.
- Hvis det finnes to ordrer med et antall på én og fire, vil den samtidige kapasiteten for rutelinjen for den første ordren være 0,2 og 0,8 for den andre.  

    Som et resultat av dette vil den tildelte kapasiteten for den første ordren være 24 min og 96 for den andre. Varigheten for begge ordrene forblir to timer.  

I begge tilfeller er den totale tildelte tiden for alle ordrer to timer.


### Effektiv ressurs kan bare dedikere en del av arbeidsdatoen til produktivarbeid

> [!NOTE]
> Dette scenarioet anbefales ikke. Vi anbefaler at du bruker effektiviteten i stedet. 

Et av arbeidssentrene representerer en erfaren arbeidsenhet som arbeider med 100 % effektivitet på aktiviteter. De kan imidlertid bare bruke 50 % av arbeidstiden på oppgaver, fordi resten av tiden de løser administrative oppgaver. Selv om denne arbeideren kan fullføre en totimers aktivitet på nøyaktig to timer, må du i gjennomsnitt vente to timer til mens personen håndterer andre tildelinger.  

Tildelt operasjonstid er to timer, og varigheten er fire timer.  

Ikke bruk oppstillingstid for slike scenarioer, ettersom [!INCLUDE [prod_short](includes/prod_short.md)] bare tildeler 50 % av tiden. Hvis oppstillingstiden er satt til *2*, er den tildelte oppstillingstiden én time, og varigheten er to timer.

### Konsolidert kalender

Når feltet **Konsolidert kalender** er valgt, har arbeidssenteret ingen kapasitet. I stedet er kapasiteten lik summen av kapasiteten for alle produksjonsressursene som er tilordnet arbeidssenteret.  

> [!NOTE]
> Produksjonsressursens effektivitet blir konvertert til kapasiteten i arbeidssenteret.

Hvis du for eksempel har to produksjonsressurser med en effektivitet på henholdsvis 80 og 70, har den konsoliderte kalenderposten:

- En effektivitet på 100
- En kapasitet på 1,5
- En total kapasitet på 12 timer (åtte timers skift * 1,5 kapasitet).

> [!NOTE]
> Bruk feltet **Konsolidert kalender** når du strukturerer rutene til å planlegge produksjonsoperasjoner på produksjonsressursnivå, ikke arbeidssenternivå. Når du konsoliderer kalenderen, blir siden og rapportene **Arbeidssenterbelastning** en oversikt over samlebelastningen i alle produksjonsressurser som er tilordnet arbeidssenteret.

### Eksempel – forskjellige produksjonsressurser tilordnet til et arbeidssenter

Det er viktig å planlegge hvilke kapasiteter som skal utgjøre den totale kapasiteten når du oppretter produksjonsressurser og arbeidssentre.

Hvis forskjellige produksjonsressurser (for eksempel 210 Pakkebord 1, 310 Malekabinett ...) er tilordnet et arbeidssenter, er hensynet til de enkelte kapasitetene i produksjonsressursen viktig, fordi en feil i én produksjonsressurs kan avbryte hele prosessen. Maskingruppene kan angis i henhold til kapasiteten, men de inkluderes ikke i planlegging. Hvis du deaktiverer **Konsolidert kalender**, tilordnes bare kapasiteten i arbeidssenteret i planleggingen. Kapasiteten i produksjonsressursen blir utelatt.

Hvis du imidlertid kombinerer like produksjonsressurser (for eksempel 210 Pakkebord 1 og 220 Pakkebord 2) i et arbeidssenter, kan du se på arbeidssenteret som en sum av tilordnede produksjonsressurser. Derfor listes arbeidssenteret opp med null kapasitet. Den felles kapasiteten tilordnes arbeidssenteret hvis du aktiverer **Konsolidert kalender**.

Hvis du ikke vil at kapasiteter i arbeidssentre skal bidra i den totale kapasiteten, angir du **0** i **Effektivitet**-feltet.

## Slik definerer du kapasitetsbegrensede maskiner eller arbeidssentre:

Du må sette opp produksjonsressurser som du anser som kritiske og utpeke dem som i stand til å håndtere en begrenset belastning i stedet for den ubegrensede belastningen som andre produksjonsressurser godtar. En kapasitetsbegrenset ressurs kan være et arbeidssenter eller en produksjonsressurs som er en flaskehals, og som du derfor vil tildele en begrenset belastning for.

[!INCLUDE[prod_short](includes/prod_short.md)] støtter ikke detaljert Shop Floor Control. Det planlegger for en gjennomførbar utnyttelse av ressurser ved å tilby en grov tidsplan, men det blir ikke automatisk opprettet og vedlikeholdt detaljerte tidsplaner basert på prioriteringer eller regler for optimalisering.

På siden **Kapasitetsbegrensede ressurser** kan du opprette et oppsett for å hindre at ressurser blir overbelastet. Oppsettet kan også sikre at kapasiteten ikke forblir tildelt, hvis den kan øke gjennomløpstiden for en produksjonsordre I feltet **Avdemping (% av total kap.)** kan du legge til avdempningstid i ressurser for å minimere oppdeling av operasjonen. Denne innstillingen gjør at systemet kan planlegge belastningen på den siste mulige dagen ved å delvis overstige den kritiske belastningsprosenten. Hvis du overskrider belastningsprosenten, kan dette redusere antall operasjoner som deles.

Når du planlegger med kapasitetsbegrensede ressurser, sikrer [!INCLUDE [prod_short](includes/prod_short.md)] at ingen ressurser lastes over den angitte kapasiteten (kritisk belastning). Det tildeler hver operasjon til nærmeste tilgjengelige tidsluke. Hvis tidsperioden ikke er stor nok til å fullføre hele operasjonen, deler den operasjonen inn i to eller flere deler som plasseres i de nærmeste tilgjengelige tidsrommene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kapasitetsbegrensede ressurser** og velg den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov.

> [!NOTE]
> Operasjoner på arbeidssentre eller produksjonsressurser som er konfigurert som begrensede ressurser vil alltid bli planlagt serielt. Denne planleggingen betyr at hvis en begrenset ressurs har flere kapasiteter, må disse kapasitetene planlegges i rekkefølge. Du kan ikke planlegge dem parallelt som ville blitt gjort hvis arbeidssenteret eller produksjonsressursen ikke var definert som en begrenset ressurs. For en begrenset ressurs er **Kapasitet**-feltet på arbeidssenteret eller i produksjonsressursen større enn **1**.

> I tilfeller med oppdeling av operasjon blir oppstillingstiden bare tildelt én gang fordi det antas at noe manuell justering er gjort for å optimalisere tidsplanen.

## Se også

[Opprette produksjonskalendere](production-how-to-create-work-center-calendars.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)  
[Planlegging](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
