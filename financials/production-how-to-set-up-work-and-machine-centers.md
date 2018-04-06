---
title: Konfigurere arbeidssentre og produksjonsressurser | Microsoft-dokumentasjon
description: "Et **Arbeidssenter**-kort inneholder de faste verdiene og kravene til den aktuelle produksjonsressursen og styrer dermed avgangen for produksjonen som utføres i arbeidssenteret."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 45477104c003d60786961f4329c1543a96be5b0c
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-work-centers-and-machine-centers"></a>Konfigurere arbeidssentre og produksjonsressurser
Programmet skiller mellom tre typer kapasiteter. Disse er rangert hierarkisk. Hvert nivå inneholder underordnede nivåer.  

Det øverste nivået er arbeidssentergruppen. Arbeidssentre er tilordnet arbeidssentergruppene. Hvert arbeidssenter kan bare tilhøre én arbeidssentergruppe.

Du kan tilordne forskjellige produksjonsressurser til hvert arbeidssenter. En produksjonsressurs kan bare tilhøre ett arbeidssenter.  

Planlagt kapasitet i et arbeidssenter består av hvor tilgjengelige tilhørende produksjonsressurser er og annen planlagt tilgjengelighet i arbeidssenteret. Den planlagte tilgjengeligheten i arbeidssentergruppen er derfor summen av all tilhørende tilgjengelighet i produksjonsressursene og arbeidssentrene.  

Tilgjengeligheten lagres i kalenderposter. Før du definerer arbeidssentre eller produksjonsressurser, må du definere produksjonskalendere. Hvis du vil ha mer informasjon, kan du se [Opprette produksjonskalendere](production-how-to-create-work-center-calendars.md).  

## <a name="to-set-up-a-work-center"></a>Slik oppretter du et arbeidssenter:
I det følgende beskrives først og fremst hvordan du definerer et arbeidssenter. Fremgangsmåten for å sette opp en produksjonsressurskalender er lik unntatt hurtigfanen **Ruteoppsett**.  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Arbeidsskift**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Velg eventuelt ressursgruppen på et høyere nivå som arbeidssenteret er organisert under, i feltet **Arbeidssentergruppe**. Velg **Ny**-handlingen i rullegardinlisten.  
5.  Velg **Sperret**-feltet hvis du vil hindre at arbeidssenteret brukes i behandling. Dette betyr at det ikke kan bokføres avgang for en vare som er produsert ved arbeidssenteret. Hvis du vil ha mer informasjon, kan du se [Bokføre produksjonsutgang](production-how-to-post-output-quantity.md).
6.  I feltet **Direkte enhetskost** registrerer du kostnaden av å produsere én enhet ved dette arbeidssenteret, ekskludert andre kostnadselementer. Denne kostnaden kalles ofte *direkte lønnssats*.  
7.  I feltet **Indirekte kost-%** angir du de generelle operasjonskostnadene som løper ved bruk av arbeidssenteret, som en prosentandel av den direkte enhetskostnaden. Denne prosentandelen legges til i direktekostnaden i beregningen av enhetskostnaden.  
8.  I feltet **Sats for indirekte kostnader** registrerer du ikke-operasjonelle kostnader, for eksempel vedlikeholdsutgifter, for arbeidssenteret som et absolutt beløp.  

    **Enhetskost**-feltet inneholder den beregnede enhetskostnaden for å produsere én enhet ved dette arbeidssenteret, inkludert alle kostnadselementer slik:  

    Enhetskostnad = Direkte enhetskostnad + (Direkte enhetskostnad x Indirekte kostnad-%) + Sats for indirekte kostnader.  

9.  I feltet **Beregning av enhetskost** definerer du om beregningen ovenfor skal baseres på medgått tidt:  **Tid**, eller på antall produserte enheter:  **Enheter**.  
10.  Velg feltet **Bestemt enhetskost** hvis du vil definere arbeidssenterets kostnad på rutelinjen der den brukes. Dette kan være relevant for operasjoner med en totalt forskjellig kapasitetskostnad enn det som ville vært normalt ved arbeidssenteret.  
11.  I **Trekkmetode**-feltet velger du om avgangsbokføring ved dette arbeidssenteret skal beregnes og bokføres manuelt eller automatisk ver hjelp av en av de følgende metoder.  

    |Alternativ|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Manuell**|Forbruk bokføres manuelt i ferdigmeldingskladden eller produksjonskladden.|
    |**Fremover**|Forbruk beregnes og bokføres automatisk når produksjonsordren er frigitt.|  
    |**Bakover**|Forbruk beregnes og bokføres automatisk når produksjonsordren er ferdigstilt.|  

    > [!NOTE]  
    >  Om nødvendig kan trekkmetoden som velges her og på **Vare**-kortet, overstyres for individuelle operasjoner ved å endre innstillingen på rutelinjene.

12.  I **Enhetskode**-feltet registrerer du tidsenheten som arbeidssenterets kostnadsberegning og kapasitetsplanlegging beregnes i.
    Du må først definere en enhetsmetode for å kunne kontrollere forbruk konstant. Enhetene du angir, er basisenheter. Behandlingstiden, for eksempel, beregnes i timer og minutter.

    > [!NOTE]  
    > Hvis du velger å bruke Dager, må du huske at én dag = 24 timer, og ikke åtte (arbeidstimer).

13.  I **Kapasitet**-feltet definerer du om arbeidssenteret har mer enn én maskin eller person som arbeider samtidig. Hvis Produksjonsressurs-funksjonaliteten ikke inngår i din installasjon av  [!INCLUDE[d365fin](includes/d365fin_md.md)], må verdien i dette feltet være **1**.  
14.  I **Effektivitet**-feltet registrerer du prosentandelen for den forventede standardavgangen som dette arbeidssenteret faktisk produserer. Hvis du skriver inn **100**, betyr det at arbeidssenteret har en faktisk avgang som er den samme som standardavgangen.  
15. Merk av for **Konsolidert kalender** hvis du også bruker produksjonsressurser. Dette sikrer at kalenderposter blir opprullert på bakgrunn av produksjonsressurskalendere.  
16.  Velg en produksjonskalender i feltet **Produksjonskalenderkode**. Hvis du vil ha mer informasjon, kan du se [Opprette produksjonskalendere](production-how-to-create-work-center-calendars.md).  
17.  I **Køtid**-feltet angir du en fast tidsrom som må forløpe før tilordnet arbeid kan begynne ved dette arbeidssenteret. Vær oppmerksom på at Køtid legges til i andre ikke-produktive tidselementer, for eksempel Ventetid og Transporttid, som du kan definere på rutelinjene ved hjelp av dette arbeidssenteret.  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Eksempel – forskjellige produksjonsressurser tilordnet til et arbeidssenter
Det er viktig å planlegge hvilke kapasiteter som skal utgjøre den totale kapasiteten når produksjonsressurser og arbeidssentre opprettes.

Hvis forskjellige produksjonsressurser (for eksempel 210 Pakkebord 1, 310 Malekabinett ...) er tilordnet et arbeidssenter, er hensynet til de enkelte kapasitetene i produksjonsressursen viktig, fordi feil i én produksjonsressurs kan avbryte hele prosessen. Maskingruppene kan angis i henhold til kapasiteten, men kan ikke inkluderes i planleggingen. Hvis feltet **Konsolidert kalender** deaktiveres, tilordnes bare kapasiteten i arbeidssenteret og ikke i produksjonsressursen, i planleggingen.

Hvis imidlertid like produksjonsressurser (for eksempel 210 Pakkebord 1 og 220 Pakkebord 2) kombineres i et arbeidssenter, er hensynet til arbeidssenteret som en sum av tilordnede produksjonsressurser, interessant. Derfor listes arbeidssenteret opp med null kapasitet. Den felles kapasiteten tilordnes arbeidssenteret hvis feltet **Konsolidert kalender** aktiveres.

Hvis kapasiteter i arbeidssentre ikke skal bidra i den totale kapasiteten, kan du oppnå dette ved effektivitet = 0.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Slik definerer du kapasitetsbegrensede maskiner eller arbeidssentre:
Du må sette opp produksjonsressurser som du anser som kritiske og utpeke dem som i stand til å håndtere en begrenset belastning i stedet for den ubegrensede belastningen som andre produksjonsressurser godtar. En kapasitetsbegrenset ressurs være et arbeidssenter eller en produksjonsressurs som er identifisert som flaskehals, og som du derfor vil tildele en begrenset belastning for.

[!INCLUDE[d365fin](includes/d365fin_md.md)] støtter ikke detaljert Shop Floor Control. Det planlegger for en gjennomførbar utnyttelse av ressurser ved å tilby en grov tidsplan, men det blir ikke automatisk opprettet og vedlikeholdt detaljerte tidsplaner basert på prioriteringer eller regler for optimalisering.

I vinduet **Kapasitetsbegrensede ressurser** kan du gjøre oppsett som unngår overbelastning av bestemte ressurser og sikre at all kapasitet fordeles hvis den kan øke gjennomløpstiden til en produksjonsordre. I feltet **Avdemping (% av total kap.)** kan du legge til avdempningstid i ressurser for å minimere oppdeling av operasjonen. Dette gjør at systemet kan planlegge belastning på den aller siste dagen ved å overskride den kritiske belastningsprosenten litt hvis dette kan redusere antall delte operasjoner.

Når du planlegger med kapasitetsbegrensede ressurser, sikrer systemet at ingen ressurser lastes over den angitte kapasiteten (kritisk belastning). Dette gjøres ved å tilordne hver operasjon til nærmeste tilgjengelige tidsluke. Hvis tidsperioden ikke er stor nok til å fullføre hele operasjonen, vil operasjonen bli delt inn i to eller flere deler som plasseres i de nærmeste tilgjengelige tidsrommene.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kapasitetsbegrensede ressurser**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov.

> [!NOTE]
> Operasjoner på arbeidssentre eller produksjonsressurser som er konfigurert som begrensede ressurser vil alltid bli planlagt serielt. Dette betyr at selv om en begrenset ressurs har flere kapasiteter, kan disse kapasitetene bare bli planlagt i sekvens, ikke parallelt, som de ville blitt hvis arbeidssenteret eller produksjonsressursen ikke ble konfigurert som en begrenset ressurs. I en begrenset ressurs er Kapasitet-feltet på arbeidssenteret eller i produksjonsressursen større enn 1.

> I tilfeller med oppdeling av operasjon blir oppstillingstiden bare tilordnet én gang fordi det antas at noe manuell justering er gjort for å optimalisere tidsplanen.

## <a name="see-also"></a>Se også  
[Opprette produksjonskalendere](production-how-to-create-work-center-calendars.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Planlegging](production-planning.md)   
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

