---
title: Telle, justere og reklassifisere lagerbeholdning | Microsoft-dokumentasjon
description: Beskriver hvordan du utfører fysisk telling og foretar negative eller positive justeringer, og hvordan du endrer informasjon, for eksempel lokasjons- eller partinummer, i vareposter eller lagerposter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 04/20/2020
ms.author: edupont
ms.openlocfilehash: 63d7157bc25aa97e1963efdfeb75364db04a0c95
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782146"
---
# <a name="count-adjust-and-reclassify-inventory-using-journals"></a>Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder
Minst én gang hvert regnskapsår må du utføre en vareopptelling, det vil si telle alle varer på lager, for å se om antallet som er registrert i databasen, er det samme som det faktiske antallet i lageret. Når det faktiske antallet er funnet, må det bokføres i Finans som en del av verdifastsettelsen av lageret ved periodens avslutning.

Selv om du teller alle varene i beholdningen minst én gang i året, kan du ha bestemt deg for å telle noen varer oftere, kanskje fordi de er mer verdifulle eller fordi de har rask omløpstid og utgjør en stor del av forretningene. Hvis du vil gjøre dette, kan du tilordne spesielle opptellingsperioder til disse varene. Hvis du vil ha mer informasjon, kan du se [Slik utfører du syklustelling](inventory-how-count-adjust-reclassify.md#to-perform-cycle-counting).

Hvis du har bruk for å justere registrerte lagerantall, i forbindelse med opptellinger eller til andre formål, kan du bruke en varekladd til å endre lagerpostene direkte, uten å bokføre forretningstransaksjoner. Du kan også justere for én vare på varekortet.

Hvis du har bruk for å endre lagerpostattributter, kan du bruke varereklassifiseringskladden. Attributter som ofte reklassifiseres, er dimensjoner og salgskampanjekoder, men du også utføre systemoverføringer ved å reklassifisere hylle- og lokasjonskoder. Spesielle trinn brukes når du vil reklassifisere serie- eller partinumre og utløpsdatoene deres. Hvis du vil ha mer informasjon, kan du se [Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md).

> [!NOTE]
> Varene er registrert i hyller som lagerposter, ikke vareposter, i et avansert lageroppsett. Derfor kan utføre du telle, justere og reklassifisere i spesielle lagerkladdene som støtter hyller. Deretter bruke du spesielle for å synkronisere nye eller endrede lagerposter med de relaterte varepostene å utføre endringene i antall og verdier. Dette beskrives i en bestemt fremgangsmåtene nedenfor der det er relevant.

## <a name="to-perform-a-physical-inventory"></a>Utføre en vareopptelling
Ved slutten av et regnskapsår, eller oftere, må du foreta en vareopptelling, altså telle den faktiske varebeholdningen, for å se om det antallet som er registrert i programmet er identisk med det fysiske antallet som er på lager. Hvis det er en differanse, må denne bokføres til varekontiene før du kan fastsette verdien av lageret.

> [!NOTE]
> Denne fremgangsmåten beskriver hvordan du utfører en vareopptelling ved hjelp av en kladd, siden **Vareopptellingskladd**. Du kan også utføre oppgaven med dokumenter, sidene **Vareopptellingsordre** og **Registrering for vareopptelling**, som gir mer kontroll og støtter distribusjon av opptellingen til flere ansatte. Hvis du vil ha mer informasjon, se [Telle lagerbeholdning ved hjelp av dokumenter](inventory-how-count-inventory-with-documents.md).<br /><br />
> Merk at den dokumentbaserte funksjonaliteten ikke kan brukes til å telle varer i hyller, lagerposter.

Bortsett fra den fysiske opptellingsaktiviteten omfatter hele prosessen følgende tre oppgaver:

- Beregn forventet beholdning.
- Skriv ut rapporten som skal brukes ved telling.
- Angir og bokfør faktisk opptalt lagerbeholdning.

Du kan utføre det fysiske lageret på én av følgende måter, avhengig av lageroppsettet. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).  

-   Hvis lokasjonen ikke bruker dirigert plassering og plukk (enkel lagerkonfigurasjon), bruker du siden **Vareopptellingskladd**på **Lager**-menyen. Prosedyren er stort sett den samme som når du utfører en vareopptelling uten syklustelling.  
-   Hvis lokasjonen bruker lagerstyring (avansert lagerkonfigurasjon), bruker du først siden **Lageropptellingskladd** og deretter **Varekladd**-siden for å kjøre funksjonen **Beregn lagerjustering**.

### <a name="to-calculate-the-expected-inventory-in-basic-warehouse-configurations"></a>Slik beregner du den forventede beholdningen i enkle lagerkonfigurasjoner
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Vareopptellingskladder**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Beregn beholdning**.
3. Angi betingelsene som skal brukes ved opprettelse av kladdelinjene, for eksempel om varer uten registrert beholdning skal tas med, på siden **Beregn beholdning**.
4. Angi filtre hvis du bare vil beregne lager for bestemte varer, hyller, lokasjoner eller dimensjoner.
5. Velg **OK**.

> [!NOTE]  
>   Varepostene behandles på bakgrunn av opplysninger du har angitt, og linjer opprettes i opptellingskladden. Merk deg at feltet **Antall (opptalt)** automatisk fylles ut med samme antall som i feltet **Antall (beregnet)**. Når du bruker denne funksjonen, er det ikke nødvendig å angi den opptalte lagerbeholdningen for varer som er lik beregnet antall. Hvis imidlertid det opptalte antallet er forskjellig fra det som er angitt i feltet **Antall (beregnet)**, må du overskrive det med det faktisk opptalte antallet.

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>Slik beregner du den forventede beholdningen i avanserte lagerkonfigurasjoner
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varekladd**, og velg deretter den relaterte koblingen.  
2.  Velg **Beregn lagerjust.**-handlingen.  
3.  Fyll ut forespørselssiden for kjørselen med numrene på varene du vil telle, og med lokasjonen.
4. Velg **OK**-knappen, og bokfør de eventuelle justeringene.

    Hvis du ikke gjør dette før du utfører vareopptellingen, blir resultatet du bokfører i vareopptellingskladden og vareposten i andre del av prosessen, vareopptellingsresultatet kombinert med andre lagerjusteringer for varene som ble opptalt.  
5.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageropptellingskladd**, og velg deretter den relaterte koblingen.  
6. Velg handlingen **Beregn beholdning**. Forespørselssiden for kjørselen **Beregn beholdning - lager** åpnes.  
7.  Definer filtrene for å begrense varene som skal telles i kladden, og klikk deretter på **OK**-knappen.

    Programmet oppretter en linje for hver hylle som oppfyller filterkravene. På dette punktet kan du fremdeles slette noen av linjene, men hvis du vil bokføre resultatene som en vareopptelling, må du telle varen i alle hyller som inneholder den.  

     Hvis du bare har tid til å telle varen i noen hyller og ikke i andre, kan du oppdage avvik. Registrer dem og bokfør dem senere i varekladden ved hjelp av funksjonen **Beregn lagerjustering**.  
8.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageropptelling – oversikt**, og velg deretter den relaterte koblingen.  
9.  Åpne rapportforespørselssiden, og skriv ut oversiktene der du vil at de ansatte skal registrere antall varer de teller i hver hylle.  
10. Når tellingen er utført, angir du de opptalte antallene i feltet **Antall (opptalt)** i lageropptellingskladden.  

    > [!NOTE]  
    >  I lageropptellingskladden fyller programmet automatisk ut feltet **Antall (beregnet)** på bakgrunn av lagerhyllepostene og kopierer disse antallene til feltet **Antall (fysisk)** på hver linje. Hvis antallet som er opptalt av den lageransatte, er forskjellig fra det programmet har angitt i feltet Antall (opptalt), må du angi det faktisk opptalte antallet.  

11. Når du har angitt alle de opptalte antallene, velger du **Registrer**-handlingen.  

    Når du har registrert kladden, oppretter programmet to lagerposter i lagerjournalen for hver linje som ble talt og registrert:  

    -   Hvis det beregnede og det opptalte antallet er forskjellig, blir det registrert et negativt eller positivt antall for hyllen, og en motpostering blir bokført for justeringshyllen for lokasjonen.  
    -   Hvis det beregnede antallet er likt det opptalte antallet, registrerer programmet en post på 0 for både hyllen og justeringshyllen. Postene er registreringen av at det på registreringsdatoen ble utført en vareopptelling, og av at det ikke var avvik i beholdningen for varen.  

Når du registrerer lageropptellingen, bokfører du ikke til vareposten, vareopptellingsposten eller verdiposten, men registreringene finnes for umiddelbar avstemming når det er nødvendig. Hvis du ønsker å ha nøyaktige registreringer av hva som skjer på lageret, og du har talt alle hyllene der varene var registrert, må du imidlertid umiddelbart bokføre lagerresultatene som en lagervareopptelling. Hvis du vil ha mer informasjon, kan du se [Slik angir og bokfører du den faktiske opptalte beholdningen i et avansert lageroppsett](inventory-how-count-adjust-reclassify.md#to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations).

### <a name="to-print-the-report-to-be-used-when-counting"></a>Slik skriver du ut rapporten som skal brukes ved telling
1. Velg handlingen **Skriv ut** på siden **Vareopptellingskladd** som inneholder den beregnede forventede beholdningen.
2. Angi om rapporten skal vise det beregnede antallet og om rapporten skal vise lagervarer etter serie-/partinumre, på siden **Opptellingsoversikt**.
3. Angi filtre hvis du bare vil skrive ut rapporten for bestemte varer, hyller, lokasjoner eller dimensjoner.
4. Velg **Skriv ut**.

Ansatte kan nå fortsette med å telle lagerbeholdningen og registrere eventuelle avvik på den utskrevne rapporten.

> [!NOTE]
> Det kan ta flere dager før utskrevne rapporter kommer tilbake for endelig behandling og bokføring. Når du angir og bokfører faktisk opptalt lager, justerer systemet lager for å gjenspeile differansen mellom forventet og faktisk opptalt beholdning. Du må beholde de opprinnelig beregnede kladdelinjene, og ikke beregne forventet beholdning på nytt, fordi det forventede lageret kan endres og føres til feil lagernivåer. Hvis du har behov for å utstede flere rapporter, for eksempel for ulike lokasjoner eller gruppe varer, må du opprette og holde separate kladder.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>Slik angir og bokfører du den faktiske opptalte beholdningen i et enkelt lageroppsett
1. Angi den faktiske beholdningen i feltet **Antall (opptalt)** for hver linje på siden **Vareopptellingskladd** der den faktiske lagerbeholdningen, som fastsatt ved fysisk opptelling, avviker fra det beregnede antallet.

    De relaterte feltene oppdateres tilsvarende.

    > [!NOTE]  
    >   Hvis opptellingen avdekker avvik som skyldes at varer er bokført med feilaktige lokasjonskoder, må du ikke angi avviket i opptellingskladden. Bruk i stedet reklassifiseringskladden eller en overføringsordre til å omadressere varene til de riktige lokasjonene. Hvis du vil ha mer informasjon, kan du se Varereklassif.kladd eller Opprette overføringsordrer.

2. Hvis du vil justere beregnet antall til faktisk opptalt antall, velger du handlingen **Bokfør**.

    Både vareposter og fysiske vareopptellingsposter opprettes. Åpne varekortet for å vise de resulterende vareopptellingspostende.

3. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.
4. Du kan kontrollere vareopptellingen ved å åpne det aktuelle varekortet og deretter velge handlingen **Vareopptellingsposter**.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>Slik angir og bokfører du den faktiske opptalte beholdningen i et avansert lageroppsett

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varekladd**, og velg deretter den relaterte koblingen.  
2.  Velg **Beregn lagerjust.**-handlingen.  
3.  Velg de samme varene som du talte i syklustellingen eller vareopptellingen du nettopp har utført, og alle andre varer som krever justering, og velg deretter **OK**.  

     Siden **Lagerkladd** åpnes, og linjer opprettes for disse varene. Merk at nettoantallene du nettopp har telt og registrert hyllevis nå kan konsolideres og synkroniseres som vareposter.  

4.  Bokfør kladden uten å endre noen antall.  

Antallene i varepostene og antallene i lageret (lagerpostene) er nå på nytt like for disse varene, og programmet har oppdatert den siste opptellingsdatoen for varen eller lagerføringsenheten.  

## <a name="to-perform-cycle-counting"></a>Utføre syklustelling
Selv om du teller alle varene i beholdningen minst én gang i året, kan du ha bestemt deg for å telle noen varer oftere, kanskje fordi de er mer verdifulle eller fordi de har rask omløpstid og utgjør en stor del av forretningene. Hvis du vil gjøre dette, kan du tilordne spesielle opptellingsperioder til disse varene.

Du kan utføre syklustellingen på én av følgende måter, avhengig av lageroppsettet. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).  

-   Hvis lokasjonen ikke bruker dirigert plassering og plukk (enkel lagerkonfigurasjon), bruker du siden **Vareopptellingskladd**på **Lager**-menyen. Prosedyren er stort sett den samme som når du utfører en vareopptelling uten syklustelling.  
-   Hvis lokasjonen bruker lagerstyring (avansert lagerkonfigurasjon), bruker du først siden **Lageropptellingskladd** og deretter **Varekladd**-siden for å kjøre funksjonen **Beregn lagerjustering**.  

### <a name="to-set-up-counting-periods"></a>Slik definerer du opptellingsperioder
En vareopptelling blir vanligvis foretatt regelmessig, for eksempel hver måned, hvert kvartal eller hvert år. Du kan definere de opptellingsperiodene som kreves.

Definer opptellingsperiodene du vil bruke, og tilordne deretter én til hver vare. Når du utfører en vareopptelling og bruker **Beregn opptellingsperiode** i vareopptellingskladden, opprette linjer for varene automatisk.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Vareopptellingsperioder**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Tilordne en opptellingsperiode til en vare  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.  
2. Velg varen du vil tilordne en opptellingsperiode til.  
3. Velg den aktuelle opptellingsperioden i vinduet **Vareopptell.periode - kode**.  
4. Velg **Ja**-knappen for å endre koden og beregne den første opptellingsperioden for varen. Neste gang du velger å beregne en opptellingsperiode i vareopptellingskladden, vises varen som en linje på siden **Vareutvalg for vareopptelling**. Du kan deretter begynne å telle varen periodisk.

### <a name="to-initiate-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Slik starter du en opptelling basert på opptellingsperioder i enkle lageroppsett
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Vareopptellingskladd**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Beregn opptellingsperiode**.

    Siden **Vareutvalg for vareopptelling** åpnes og viser varene som har opptellingsperioder tilordnet, og som må telles, i samsvar med opptellingsperiodene.
3. Utfør vareopptellingen. Hvis du vil ha mer informasjon, kan du se [Utføre en vareopptelling](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).

### <a name="to-initiate-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Slik starter du en opptelling basert på opptellingsperioder i avanserte lageroppsett
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageropptellingskladd**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Beregn opptellingsperiode**.

    Siden **Vareutvalg for vareopptelling** åpnes og viser varene som har opptellingsperioder tilordnet, og som må telles, i samsvar med opptellingsperiodene.
3. Utfør vareopptellingen. Hvis du vil ha mer informasjon, kan du se [Utføre en vareopptelling](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).  

    > [!NOTE]  
    >  Du må telle varen i alle hyllene som inneholder den bestemte varen. Hvis du sletter noen av hyllelinjene som er hentet for telling på **Lageropptelling**-siden, kommer du ikke til å telle alle varene på lageret. Hvis du senere bokfører slike ufullstendige resultater i Vareopptellingskladd, vil de bokførte antallene være feilaktige.  

## <a name="to-adjust-the-inventory-of-one-item"></a>Justere lagerbeholdningen for én vare
Når du har utført en fysisk opptelling av en vare i lagerområdet, kan du bruke funksjonen **Juster lagerbeholdning** til å registrere det faktiske lagerantallet.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.
2. Velg varen du vil justere lagerbeholdning for, og velg deretter handlingen **Justere lagerbeholdning**.
3. I feltet **Ny beholdning** angir du lagerantallet som du vil registrere for varen.
4. Velg **OK**.

Beholdningen for varen er nå justert. Det nye antallet vises i feltet **Gjeldende beholdning** på siden **Juster lagerbeholdning** og i feltet **Lagerbeholdning** på siden **Varekort**.

Du kan også bruke funksjonen **Juster lagerbeholdning** til enkel plassering av kjøpte varer på lager, hvis du ikke bruker kjøpsfakturaer eller ordrer til å registrere kjøpene. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Når du har justert lagerbeholdningen, må du oppdatere den med den gjeldende, beregnede verdien. Hvis du vil ha mer informasjon, kan du se [Revaluere beholdning](inventory-how-revalue-inventory.md).

### <a name="to-adjust-the-inventory-quantity-of-multiple-items-in-basic-warehouse-configurations"></a>Slik justerer du lagerantall for flere varer i enkle lageroppsett
På siden **Varekladd** kan du bokføre varetransaksjoner direkte for å justere lagerbeholdningen i forbindelse med kjøp, salg og positive eller negative justeringer, uten å bruke dokumenter.

Hvis du ofte bruker varekladden til å bokføre identiske eller lignende kladdelinjer, for eksempel i forbindelse med materialforbruk, kan du bruke siden **standardvarekladden** til å forenkle dette gjentakende arbeidet. Hvis du vil ha mer informasjon, kan du se [Arbeide med standardkladder](ui-work-general-journals.md#working-with-standard-journals).

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varekladder**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velg handlingen **Bokfør** for å foreta lagerjusteringene.

> [!NOTE]  
>   Når du har justert lagerbeholdningen, må du oppdatere den med den gjeldende, beregnede verdien. Hvis du vil ha mer informasjon, kan du se [Revaluere beholdning](inventory-how-revalue-inventory.md).

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Slik justerer du hylleantall i avanserte lageroppsett.  
Hvis lokasjonen bruker lagerstyring, bruker du **lagervarekladden** til å bokføre, utenom konteksten av beholdningen, alle positive og negative justeringer i vareantall som du vet er virkelige vinninger, for eksempel varer som tidligere var bokført som manglende som uventet dukker opp, eller virkelige tap, for eksempel knusing.  

Til forskjell fra justeringer i varekladden, gir bruk av lagervarekladden deg et ekstra nivå for justering, som gjør at det registrerte antallet er mer nøyaktig til enhver tid. Lageret vil dermed alltid ha en fullstendig registrering av hvor mange varer som er på lager, og hvor de er lagret, men hver registrering av justeringer blir ikke umiddelbart bokført i vareposten. I registreringsprosessen krediteres og debiteres den virkelige hyllen med antallsjusteringen, og korrigeringspost angis i en justeringshylle, som er en virtuell hylle uten virkelige varer. Denne hyllen defineres i **Hyllekode for lagerjustering** på lokasjonskortet.

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagervarekladd**, og velg deretter den relaterte koblingen.  
2.  Fyll ut informasjonen i hodet.  
3.  Fyll ut feltet **Varenr.** på linjen.  
4.  Angi hyllen der du legger de ekstra varene, eller der du har funnet ut at det mangler varer.  
5.  Fyll ut det antallet du observerer som et avvik, i feltet **Antall**. Hvis du har funnet ekstra varer, angir du et positivt antall. Hvis det mangler varer, angir du et negativt antall.  
6.  Velg handlingen **Registrer**.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>Slik synkroniserer du de justerte lagerpostene med de tilhørende varepostene
Med passende mellomrom, som defineres av selskapets prinsipper, må du bokføre postene for lagerjusteringshyllen i varepostene. Enkelte selskaper bokfører justeringer i vareposten hver dag, mens andre finner det tilstrekkelig å avstemme sjeldnere.

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varekladd**, og velg deretter den relaterte koblingen.  
2.  Fyll ut feltene på hver kladdelinje.  
3.  Velg **Beregn lagerjustering**, og definer de aktuelle filtrene på forespørselssiden for kjørselen. Justeringene er beregnet bare for postene i justeringshyllen som oppfyller filterkravene.  
4.  På hurtigfanen **Alternativer** angir du et nummer i feltet **Bilagsnummer**. Siden det ikke er definert noen nummerserie for denne kjørselen, bruker du den nummereringsplanen som er definert av lageret, eller du angir datoen fulgt av dine egne initialer.  
5.  Velg **OK**. De positive og negative justeringene summeres for hver vare, og linjer opprettes i varekladden for eventuelle varer der summen er et positivt eller negativt antall.  
6.  Bokfør kladdelinjene for å angi antallsavviket i vareposten. Beholdningen i lagerhyllene samsvarer nå nøyaktig med beholdningen i vareposten.  

## <a name="to-reclassify-an-items-lot-number"></a>Reklassifisere partinummeret for en vare
Hvis du har bruk for å endre lagerpostattributter, kan du bruke varereklassifiseringskladden. Attributter som ofte reklassifiseres, er dimensjoner og salgskampanjekoder, men du også utføre systemoverføringer ved å reklassifisere hylle- og lokasjonskoder.

Spesielle trinn brukes når du vil reklassifisere serie- eller partinumre og utløpsdatoene deres. Hvis du vil ha mer informasjon, kan du se [Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md).

Eksempelet nedenfor er basert på en lokasjonskode. Fremgangsmåten er den samme som for andre typer vareattributter.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Vareoverføringskladder**, og velg deretter den relaterte koblingen.
2. På siden **Vareoverføringskladder** fyller du ut feltene etter behov.
3. I **Lokasjonskode**-feltet angir du varens gjeldende lokasjonskode.
4. I **Ny lokasjonskode**-feltet angir du varens nye lokasjonskode.
5. Velg handlingen **Bokfør**.

Hvis du vil ha informasjon om overføring av varer med full kontroll over antall levert og mottatt, kan du se [Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md).

## <a name="see-also"></a>Se også
[Telle lagerbeholdning ved hjelp av dokumenter](inventory-how-count-inventory-with-documents.md)  
[Lager](inventory-manage-inventory.md)
[Lagerstyring](warehouse-manage-warehouse.md)    
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
