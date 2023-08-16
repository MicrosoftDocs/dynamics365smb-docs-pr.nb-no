---
title: 'Telle, justere og reklassifisere lagerbeholdning'
description: Lær hvordan du foretar fysisk opptelling og lager justeringer og reklassifiseringer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
---
# Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder

Tell fysisk alle varene på lager for å sikre at antallet er riktig. Noen bedrifter utfører en årlig fysisk opptelling, og andre teller alle eller bare noen varer oftere. Når du har talt varene, bruker du kladder til å bokføre de faktiske antallene til finans. Når du for eksempel valuterer lageret på slutten av en periode.

Når du skal telle noen varer oftere enn andre, kanskje på grunn av verdien, bruker du syklustellinger. For syklustellinger tildeler du spesielle opptellingsperioder til varene. Finn ut mer under [Utfør syklustelling](inventory-how-count-adjust-reclassify.md#to-do-cycle-counting).

Hvis du vil justere antall etter en opptelling eller andre formål, kan du bruke en varekladd til å endre lagerpostene uten å bokføre transaksjoner. Du kan også justere antallet for én vare på et varekort.

For å endre attributter på vareposter bruker du en varereklassifiseringskladd. Vanlige attributter som skal reklassifiseres, inkluderer dimensjoner og salgskampanjekoder. Reklassifiseringskladder kan også brukes til overføringer ved å reklassifisere hylle og lokasjonskoder. Spesielle trinn brukes når du vil reklassifisere serie- eller partinumre og utløpsdatoene deres. Hvis du vil ha mer informasjon, kan du se [Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md).

> [!NOTE]
> I flertrinnsprosesser er varene registrert i hyller som lagerposter, ikke vareposter. Derfor kan utføre du telle, justere og reklassifisere i lagerkladdene som støtter hyller. Deretter du synkroniserer du nye eller endrede lagerposter med de relaterte varepostene å utføre endringene i antall og verdier.

## Vareopptelling

Tell varene, altså tell den faktiske varebeholdningen, for å se om det antallet som er registrert i programmet er identisk med det fysiske antallet som er på lager. Vanligvis skjer opptelling på slutten av et regnskaps år, men av og til utføres det ofte oftere. Hvis det er differanser, bokfører du de faktiske antallene til varekontoene <!--accounts, or ledger?--> før du utfører lagervaluteringen.

> [!NOTE]
> Denne fremgangsmåten beskriver hvordan du utfører en vareopptelling ved hjelp av en kladd, på siden **Vareopptellingskladd**. Du kan bruke dokumenter på sidene **Vareopptellingsordre** og **Registrering av vareopptelling**. Disse dokumentene gir mer kontroll og støtte for distribusjon av opptellingsarbeidet til flere ansatte. Finn ut mer under [Telle og justere lagerbeholdning ved hjelp av dokumenter](inventory-how-count-inventory-with-documents.md).<br /><br />
> Merk at du ikke kan bruke den dokumentbaserte funksjonaliteten til å telle varer i hyller eller lagerposter.

Opptellingsprosessen omfatter også følgende oppgaver:

- Beregn forventet beholdning.
- Skriv ut rapporten som skal brukes ved telling.
- Angir og bokfør faktisk antall.

Avhengig av lageroppsettet gjøres vareopptelling på en av følgende måter. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).  

- Hvis lokasjonen ikke bruker lagerstyring, bruker du siden **Vareopptellingskladd**. Fremgangsmåten ligner på vareopptelling uten syklustelling.  
- Hvis lokasjonen bruker lagerstyring, bruker du siden **Lagervareopptellingskladd**. Deretter bruker du siden **Varekladder** siden til å kjøre handlingen **Beregn lagerjustering**. <!--We should say what to do on each of these pages.-->

### Slik beregner du den forventede beholdningen i enkle lagerkonfigurasjoner

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareopptellingskladder** og velg den relaterte koblingen.
2. Velg handlingen **Beregn beholdning**.
3. Angi betingelsene som skal brukes ved opprettelse av kladdelinjene, for eksempel om varer uten registrert beholdning skal tas med, på siden **Beregn beholdning**.
4. Angi filtre hvis du bare vil beregne lager for bestemte varer, hyller, lokasjoner eller dimensjoner.
5. Velg **OK**-knappen.

> [!NOTE]  
> Varepostene behandles på bakgrunn av opplysninger du har angitt, og linjer opprettes i opptellingskladden. Merk deg at feltet **Antall (opptalt)** har samme antall som i feltet **Antall (beregnet)**. Du trenger ikke å angi det opptalte antallet for varer der disse verdiene samsvarer. Men hvis det talte antallet er forskjellige, angir du antallet som ble talt.

### Slik skriver du ut rapporten som skal brukes ved telling

1. Velg handlingen **Skriv ut** på siden **Vareopptellingskladd** som inneholder den beregnede forventede beholdningen.
2. Angi om rapporten skal vise det beregnede antallet og om rapporten skal vise lagervarer etter serie- og partinumre, på siden **Vareopptellingsoversikt for lager**.
3. Angi filtre hvis du bare vil skrive ut rapporten for bestemte varer, hyller, lokasjoner eller dimensjoner.
4. Velg **Skriv ut**.

Lagermedarbeidere kan nå telle lagerbeholdningen og registrere differansene på den utskrevne rapporten.

> [!NOTE]
> Det kan ta flere dager før utskrevne rapporter kommer tilbake for endelig behandling og bokføring. Når du angir og bokfører faktisk opptalt lager, justerer systemet lager for å gjenspeile differansen mellom forventet og faktisk opptalt beholdning. Du må beholde de opprinnelig beregnede kladdelinjene, og ikke beregne forventet beholdning på nytt, fordi det forventede lageret kan endres og føres til feil lagernivåer. Hvis du har behov for å utstede flere rapporter, for eksempel for ulike lokasjoner eller gruppe varer, må du opprette og holde separate kladder.

### Slik angir og bokfører du den faktiske opptalte beholdningen i et enkelt lageroppsett

1. Angi den faktiske beholdningen i feltet **Antall (opptalt)** for hver linje på siden **Vareopptellingskladd** der den faktiske lagerbeholdningen, som fastsatt ved fysisk opptelling, avviker fra det beregnede antallet.
  
  > [!NOTE]  
  > Hvis opptellingen avdekker avvik skyldes at varer er bokført med feil lokasjoner, må du ikke angi avviket i opptellingskladden. Bruk i stedet en reklassifiseringskladd eller en overføringsordre til å omadressere varene til de riktige lokasjonene. 

2. Hvis du vil justere beregnet antall til faktisk opptalt antall, velger du handlingen **Bokfør**.

    Bokføring oppretter vareposter og fysiske vareopptellingsposter. Åpne siden Varekort for å vise varen for å finne vareopptellingspostene for varen. <!--Where are they shown on an item?-->

3. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
4. Du kan kontrollere tellingen ved å åpne siden Varekort for varen og deretter velge handlingen **Vareopptellingsposter**. <!--I don't see this action -->

### Slik beregner du den forventede beholdningen i avanserte lagerkonfigurasjoner

Synkroniser vareposter og lager <!--warehouse what?--> før vareopptellingen. Ellers vil det du bokfører i vareopptellingskladden og i varepostene, være de fysiske lagerresultatene som er kombinert med andre lagerjusteringer for varene. Finn ut mer under [Synkroniser antall i vareposten og på lageret](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagervareopptellingskladd**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Beregn beholdning** for å åpne siden **Beregn beholdning – lager**.  
3. Definer filtrene for å angi varene som skal telles i kladden, og klikk deretter på **OK**.

   [!INCLUDE [prod_short](includes/prod_short.md)] oppretter en linje for hver hylle som oppfyller filterkravene. Du kan slette linjer, men hvis du vil bokføre resultatene som en vareopptelling, må du telle varen i alle hyller som inneholder den.  

   Hvis du bare teller en vare i noen hyller, men ikke i andre, kan du angi differanser og bokfør dem senere i varekladden ved hjelp av handlingen **Beregn lagerjustering**. <!--I don't see this action-->  

### Slik angir og bokfører du den faktiske opptalte beholdningen i et avansert lageroppsett

1. Angi de opptalte antallene i feltet **Antall (opptalt)** på siden **Varelageropptellingskladd**.  

    > [!NOTE]  
    >  Feltet **Antall (beregnet)** fylles ut på bakgrunn av hyllekoder. Antallet kopieres til feltet **Antall (fysisk)** på hver linje. Hvis antallene i disse feltene ikke samsvarer, angir du det faktiske antallet.  

2. Når du har angitt alle de faktiske antallene, velger du **Registrer**-handlingen.  

    Når du har registrert kladden, oppretter [!INCLUDE [prod_short](includes/prod_short.md)] to lagerposter i lagerjournalen for hver linje som ble talt og registrert:  

    - Hvis det beregnede og det faktiske antallet er forskjellig, blir det registrert et negativt eller positivt antall for hyllen, og en motpostering blir bokført for justeringshyllen for lokasjonen.  
    - Hvis det beregnede antallet er likt det opptalte antallet, registrerer [!INCLUDE [prod_short](includes/prod_short.md)] en post på **0** for både hyllen og justeringshyllen. 

Når du registrerer vareopptelling, bokfører du ikke til varen, vareopptellingen eller verdipostene. Postene er imidlertid tilgjengelige for avstemming når det er nødvendig. Hvis du vil beholde antall nøyaktige etter at du har talt varene i alle hyller, bokfører du resultatet som en lageropptelling <!--physical inventory journal-->. Finn ut mer under [Synkroniser antall i vareposten og på lageret](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

## Utfør syklustelling

Du kan telle varer så ofte du vil. For eksempel fordi de er mer verdifulle, eller fordi de er populære og en stor del av virksomheten. Angi opptellingsintervallet ved å tildele spesielle opptellingsperioder til varene.

Du kan utføre syklustellingen på en av følgende måter, avhengig av lageroppsettet. Finn ut mer under [Definer lagerstyring](warehouse-setup-warehouse.md).  

- Hvis lokasjonen ikke bruker lagerstyring, bruker du siden **Vareopptellingskladd**. Fremgangsmåten ligner på vareopptelling uten syklustelling.  
- Hvis lokasjonen bruker lagerstyring, bruker du siden **Lagervareopptellingskladd**. Deretter bruker du siden **Varekladder** siden til å kjøre handlingen **Beregn lagerjustering**. <!--we should say what to do on each of these pages-->  

### Slik definerer du opptellingsperioder

Vareopptelling er vanligvis en regelmessig oppgave, for eksempel hver måned, hvert kvartal eller hvert år. Du kan definere opptellingsperiodene du trenger, og tilordne deretter én til hver vare. Etterpå bruker du handlingen **Beregn opptellingsperiode** på siden **Vareopptellingskladd** til å opprette linjer for varene automatisk.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareopptellingsperioder** og velg den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Tilordne en opptellingsperiode til en vare

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
2. Velg varen du vil tilordne en opptellingsperiode til.  
3. Velg opptellingsperioden i vinduet **Vareopptell.periode - kode**.  

> [!NOTE]
> Hvis du endrer opptellingsperioden, viser en melding informasjon om resultatene av endringen. Velg **Ja** for å endre koden og beregne den første opptellingsperioden for varen. Neste gang du velger å beregne en opptellingsperiode i vareopptellingskladden, vises varen som en linje på siden **Vareutvalg for vareopptelling**. Deretter kan du telle varen regelmessig.

### Slik starter du en opptelling basert på opptellingsperioder i enkle lageroppsett

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareopptellingskladd** og velg den relaterte koblingen.
2. Velg handlingen **Beregn opptellingsperiode**.

    Siden **Vareutvalg for vareopptelling** viser varene som må telles, i samsvar med opptellingsperiodene.
3. Tell det fysiske lageret. Finn ut mer under [Vareopptelling](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).

### Slik starter du en opptelling basert på opptellingsperioder i avanserte lageroppsett

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagervareopptellingskladd**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Beregn opptellingsperiode**.

    Siden **Vareutvalg for vareopptelling** viser varene som må telles, i samsvar med opptellingsperiodene.
3. Tell det fysiske lageret. Finn ut mer under [Vareopptelling](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).  

   > [!NOTE]  
   > Tell varen i alle hyller som inneholder den. Hvis du sletter hyllelinjer som ble hentet for telling på **Lageropptelling**-siden, er tellingen feil når du bokfører den i vareopptellingskladden.  

## Juster antallet for én vare

Når du er ferdig med en fysisk opptelling av en vare, kan du bruke handlingen **Juster lagerbeholdning** til å registrere det faktiske lagerantallet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Velg varen du vil justere lagerbeholdning for, og velg deretter handlingen **Justere lagerbeholdning**.
3. Angi resultatet av tellingen i feltet **Ny beholdning** for lokasjonen.
4. Velg **OK**-knappen.

<!-- I don't see a "Quantity on Hand" field on the Item Card page. Should this point to the options for viewing availability?

The item’s inventory is adjusted. The new quantity is shown in the **Quantity on Hand** field on the **Item Card** page.-->

Du kan også bruke handlingen **Juster lagerbeholdning** som en enkel måte å legge til kjøpte varer i beholdningen på, hvis du ikke bruker kjøpsfakturaer eller ordrer til å registrere kjøpene. Finn ut mer under [Registrer kjøp](purchasing-how-record-purchases.md).

> [!NOTE]  
> Når du har justert lageret, oppdaterer du gjeldende verdi. Hvis du vil ha mer informasjon, kan du se [Revaluere beholdning](inventory-how-revalue-inventory.md).

### Slik justerer du antall for flere varer i enkle lageroppsett

På siden **Varekladd** kan du bokføre varetransaksjoner direkte for å justere lagerbeholdningen for kjøp, salg og positive eller negative endringer, uten å bruke dokumenter.

Hvis du ofte bruker varekladden til å bokføre identiske eller lignende kladdelinjer, for eksempel materialforbruk, kan siden **standardvarekladden** forenkle dette gjentakende arbeidet. Hvis du vil ha mer informasjon, kan du se [Arbeid med standardkladder](ui-work-general-journals.md#work-with-standard-journals).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varekladder** og velg den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velg handlingen **Bokfør** for å justere antallet.

### Slik justerer du hylleantall i avanserte lageroppsett.

Hvis lokasjonen bruker lagerstyring, bruker du siden **Lagervarekladd** til å bokføre ikke-planlagte positive og negative antallsendringer. For eksempel for varer som er bokført som manglende, som vises uventet eller tap på grunn av knusing.  

Lagervarekladder gir deg flere justeringsnivåer for å gjøre antallet mer presise. Lageret vet hvor mange varer som er tilgjengelige, og hvor de er lagret, men at ikke hver justering bokføres i vareposten. Kreditt eller debet opprettes i den reelle hyllen med antallsjusteringen. En motpost lages i en justeringshylle. Justeringshyllen er en virtuell hylle uten virkelige varer. Angi den virtuelle hyllen i feltet **Hyllekode for lagerjustering** på siden **Lokasjonskort**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagervarekladd** og velg den relaterte koblingen.  
2. Fyll ut informasjonen i hodet.  
3. I feltet **Varenr.** på linjen velger du varen.  
4. Angi hyllen der du legger de ekstra varene, eller der du har varer som mangler.  
5. Angi et positivt antall i feltet **Antall** hvis du har funnet positivt antall. Hvis det mangler varer, angir du et negativt antall.  
6. Velg handlingen **Registrer**.

## Slik synkroniserer du de justerte lagerpostene med de tilhørende varepostene

Bokfør justeringshyllepostene i varepostene for periodene du har definert. Enkelte selskaper bokfører daglige justeringer i vareposten, mens andre avstemmer sjeldnere.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varekladd** og velg den relaterte koblingen.  
2. Fyll ut feltene på hver kladdelinje.  
3. Velg handlingen **Beregn lagerjustering**, og legg deretter til filtre på siden **Beregn lagerjustering**. Justeringene er beregnet bare for postene i justeringshyllen som oppfyller filterkravene.  
4. På hurtigfanen **Alternativer** angir du et nummer i feltet **Bilagsnummer**. Siden det ikke er definert noen nummerserie for denne kjørselen, bruker du den nummereringsplanen som er definert av lageret, eller du angir datoen fulgt av dine egne initialer.  
5. Velg **OK**. De positive og negative justeringene summeres for hver vare, og linjer opprettes i varekladden.  
6. Bokfør kladdelinjene for å angi antallsavviket i vareposten. Nå samsvarer beholdningene i hyllene og vareposten.  

## Se relatert [Microsoft-opplæring](/training/modules/adjust-inventory/)

## Se også

[Telle lagerbeholdning ved hjelp av dokumenter](inventory-how-count-inventory-with-documents.md)  
[Lager](inventory-manage-inventory.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
