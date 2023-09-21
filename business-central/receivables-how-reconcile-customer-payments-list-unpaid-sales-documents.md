---
title: Utlign betalinger mot ubetalte salgsdokumenter
description: 'Du utligner beløp betalt av kunder mot relaterte salgsdokumenter og bokfører betalingen for å oppdatere kunde-, finans- og bankposter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipts, customer payment'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Avstemme kundebetalinger fra en liste over ubetalte salgsdokumenter

Når kundene har gjort elektroniske betalinger til bankkontoen, må du gjøre følgende:

* Utlign hver betalt beløp til det relaterte salgsdokumentet
* Bokfør betalingen for å oppdatere kunde-, finans- og bankpostene. 

Avhengig av forretningsbehovene kan du få betalt og registrere betalingen på ulike måter: manuelt, automatisk og via betalingstjenester.  

> [!NOTE]  
> Du kan utføre de samme oppgavene, inkludert leverandørbetalinger, på siden **Betalingsavstemmingskladd** ved hjelp av funksjoner for import av bankkontoutdrag, automatisk utligning og bankkontoavstemming. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).

Bruk siden **Registrer kundebetalinger** til å balansere interne kontoer ved å bruke faktiske kontanttall for å sikre at betalinger samles inn. Du kan raskt kontrollere og bokføre enkeltbetalinger eller engangsbetalinger, behandle rabatter og finne de ubetalte dokumentene.

Betalinger for ulike kunder som har ulike betalingsdatoer, må bokføres som individuelle betalinger. Betalinger for den samme kunden, som har samme betalingsdato, kan bokføres som en engangsbetaling. Engangsbetalinger er nyttig, for eksempel når en kunde har foretatt en enkeltbetaling som dekker flere salgsfakturaer.

## Slik definerer du betalingsregistreringsjournalen:
Fordi du kan bokføre forskjellige betalingstyper til forskjellige motkonti, må du velge en motkonto på siden **Betalingsregistreringsoppsett** før du starter behandlingen av kundebetalinger. Hvis du alltid bokfører til den samme motkontoen, kan du angi denne kontoen som standard og unngå dette trinnet hver gang du åpner siden **Registrer kundebetalinger**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsregistreringsoppsett** og velge den relaterte koblingen. Du kan også velge handlingen **Konfigurer** på siden **Registrer kundebetalinger**.
2. Fyll ut feltene på siden **Betalingsregistreringsoppsett**. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)] Velg et felt som skal inneholde en kort beskrivelse av feltet eller kobling til relatert informasjon.  

> [!TIP]
> For å gjøre det enklere å identifisere poster som ble bokført gjennom kladden, kan du tildele en bestemt nummerserie til kladden. Dette er nyttig hvis du bruker betalingsavstemmingskladder til å registrere og utligne betalinger.

## Slik registrerer du kundenes betalinger individuelt:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Registrer kundebetalinger**, og velg deretter den relaterte koblingen.  

    Siden **Registrer kundebetalinger** viser alle bokførte dokumenter som en betaling kan registreres for. Siden er også tilgjengelig fra sidene **Kunder** og **Kundekort**, der det automatisk er filtrert for den angitte kunden.  
2. Merk av for **Betaling utført** på linjen som representerer det bokførte dokumentet som en betaling er utført for.

    Hvis det er merket av for **Fyll ut mottaksdato automatisk** på siden **Betalingsregistreringsoppsett**, angis arbeidsdatoen i feltet **Mottatt den**.  
3. I feltet **Mottatt den** angir du datoen da betalingen ble mottatt. Denne datoen kan være forskjellig fra arbeidsdatoen.  
4. I feltet **Beløp mottatt** angir du beløpet som er betalt.

    For fullstendige betalinger er dette beløpet det samme som beløpet i **Restbeløp** på linjen. For delbetalinger er dette beløpet lavere enn beløpet i **Restbeløp** på linjen.
5. Gjenta trinn 2 til 4 for andre linjer som representerer bokførte dokumenter som betalinger er utført for.  
6. Velg handlingen **Bokfør betalinger**.  

Betalingsinformasjonen bokføres for dokumenter som vises som linjer der det er merket av for **Betaling utført** .  

Betalingsposter bokføres til finans-, bank- og kundekonti. Hver betaling brukes på det relaterte bokførte salgsdokumentet.  

## Avstemme engangsbetalinger
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsregistrering** og velg den relaterte koblingen.
2. Merk av for **Betaling utført** på linjene som representerer bokførte dokumenter for den samme kunden som en engangsbetaling er utført for.  

    > [!NOTE]  
    >   Kunden **Navn**-feltet må være det samme på alle linjer som bokføres som en engangsbetaling.  

    Hvis det er merket av for **Fyll ut mottaksdato automatisk** på siden **Betalingsregistreringsoppsett**, fylles arbeidsdatoen ut i feltet **Mottatt den**.  
3. I feltet **Mottatt den** angir du datoen da betalingen ble mottatt. Denne datoen kan være forskjellig fra arbeidsdatoen.  

    > [!NOTE]  
    >   Denne datoen må være den samme på alle linjene som skal bokføres som en engangsbetaling.  
4. I feltet **Beløp mottatt** angir du beløpene på flere linjer som summerer opp engangsbetalingsbeløpet.  

    > [!TIP]  
    > Prøv å bokføre så mange fullstendige betalinger som mulig med engangsbeløpet. Angi beløp som er det samme som beløpet i feltet **Restbeløp**, på så mange linjer som mulig.  
5. Gjenta trinn 2 til 4 for andre linjer som representerer bokførte dokumenter for samme kunde som det er utført en engangsbetaling for.  
6. Velg handlingen **Bokfør som engangsbetaling**. Den angitte betalingsinformasjonen bokføres for dokumenter som vises som linjer der det er merket av for **Betaling utført** .  

Betalingsposter bokføres til finans-, bank- og kundekonti. Hver betaling brukes på det relaterte bokførte salgsdokumentet.  

Hvis en betaling i banken ikke er representert av en linje på siden **Betalingsregistrering**, kan det være fordi det tilknyttede dokumentet ennå ikke er bokført. I det tilfellet kan du bruke en søkefunksjon til raskt å finne dokumentet og bokføre det for å behandle betalingen. Hvis du vil ha mer informasjon, kan du se delen [Slik finner du et bestemt salgsdokument som ikke er fullstendig fakturert](#to-find-a-specific-sales-document-that-isnt-fully-invoiced).  

Hvis en betaling i banken ikke er representert av et dokument i [!INCLUDE[prod_short](includes/prod_short.md)], kan du åpne en forhåndsutfylt finanskladd fra siden **Betalingsregistrering** for å bokføre betalingen direkte til motkontoen uten å bruke betalingen på et dokument. Alternativt kan du registrere betalingen i kladden til opprinnelsen til betalingen er fastsatt. Hvis du vil ha mer informasjon, kan du se delen [Registrere eller bokføre betalinger manuelt uten et relatert dokument](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## Behandle kundebetalinger med rabatter manuelt
Hvis du har avtalt en kontantrabatt med kunden, kan betalingsbeløpene være lavere enn fakturabeløpene hvis betalingen finner sted før den avtalte rabattdatoen.  

De følgende fremgangsmåtene beskriver fire forskjellige måter for bokføring av rabatterte betalinger på siden **Betalingsregistreringer**.  

* Betalingsbeløpet er det samme som det gjenstående rabattbeløpet, og betalingsdatoen er før rabattdatoen. Du bokfører betalingen som den er.  
* Betalingsbeløpet er det samme som det gjenstående rabattbeløpet, men betalingsdatoen er etter rabattdatoen. Du bokfører betalingen som delvis. Dokumentet forblir åpen for å hente/betale det gjenstående beløpet. Du kan også angi rabattdatoen senere for å tillate fullstendig betaling.  
* Betalingsbeløpet er lavere enn det gjenstående rabattbeløpet. Du bokfører betalingen som delvis. Dokumentet forblir åpen for å hente/betale det gjenstående beløpet.  
* Betalingsbeløpet er større enn det gjenstående rabattbeløpet. Du bokfører betalingene som de er. Bare det gjenstående beløpet bokføres. Det ekstra beløpet krediteres til kunden.  

### Slik behandler du et betalingsbeløp som er det samme som rabattbeløpet, og der betalingsdatoen er før rabattdatoen:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsregistrering** og velg den relaterte koblingen.  
2. Angi betalingsbeløpet i feltet **Beløp mottatt**. Beløpet er det samme som beløpet i feltet **Restbeløp etter rabatt**.

    Det merkes automatisk av for **Betaling utført**, og **Mottatt den** fylles ut med arbeidsdatoen.    
3. Angi betalingsdato i feltet **Mottatt den**. Datoen er før datoen i feltet **Kont.rabattdato**.
4. Kontroller at **Restbeløp**-feltet inneholder null (0).  
5. Velg handlingen **Bokfør betalinger** for å bokføre full betaling til finans-, bank- og kundekonti.

### Slik behandler du et betalingsbeløp som er det samme som rabattbeløpet, men der betalingsdatoen er etter rabattdatoen:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsregistrering** og velg den relaterte koblingen.  
2. Angi betalingsbeløpet i feltet **Beløp mottatt**. Beløpet er det samme som beløpet i feltet **Restbeløp etter rabatt**.

    Det merkes automatisk av for **Betaling utført**, og **Mottatt den** fylles ut med arbeidsdatoen.
3. I feltet **Mottatt den** angir du en betalingsdato er etter datoen i feltet **Kont.rabattdato**. Datofelt endres til rød skrift, og en feilmelding vises nederst på siden.

    > [!TIP]  
    >   Hvis du vil gjøre et unntak og gi rabatten selv om betalingen er sen, følger du disse trinnene:
4. Velg handlingen **Detaljer**.  
5. På siden **Betalingsregistreringsdetaljer**, i feltet **Kont.rabattdato** i hurtigfanen **Kontantrabatt**, skriver du inn en dato som er etter datoen i feltet **Mottatt den** på siden **Betalingsregistrering**.  

    Feilmeldingen og rød skrift forsvinner, og du kan fortsette å behandle den rabatterte betalingen.    
6. Kontroller at **Restbeløp**-feltet viser beløpet som gjenstår å betale for det fullstendige fakturabeløpet.  
7. Velg handlingen **Bokfør betalinger** for å bokføre den delvise betalingen til finans-, bank- og kundekonti.  

Det tilknyttede dokumentet forblir åpent.

### Slik behandler du en betaling som er lavere enn det gjenstående rabattbeløpet:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsregistrering** og velg den relaterte koblingen.  
2. Angi betalingsbeløpet i feltet **Beløp mottatt**. Beløpet er lavere enn beløpet i feltet **Restbeløp etter rabatt**.

    Det merkes automatisk av for **Betaling utført**, og **Mottatt den** fylles ut med arbeidsdatoen.  
3. Angi betalingsdato i feltet **Mottatt den**. Datoen er før datoen i feltet **Kont.rabattdato**.
4. Kontroller at **Restbeløp**-feltet viser beløpet som gjenstår å betale for det fullstendige rabattbeløpet.  
5. Velg handlingen **Bokfør betalinger** for å bokføre den delvise betalingen til finans-, bank- og kundekonti.  

Det tilknyttede dokumentet forblir åpent.

### Slik behandler du en betaling som er større enn det gjenstående rabattbeløpet:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsregistrering** og velg den relaterte koblingen.  
2. Angi betalingsbeløpet i feltet **Beløp mottatt**. Beløpet er større enn beløpet i feltet **Restbeløp etter rabatt**.  

    Det merkes automatisk av for **Betaling utført**, og **Mottatt den** fylles ut med arbeidsdatoen.    
3. Angi betalingsdato i feltet **Mottatt den**. Datoen er før datoen i feltet **Kont.rabattdato**.
4. Kontroller at **Restbeløp**-feltet inneholder null (0).  
5. Velg handlingen **Bokfør betalinger** for å bokføre full betaling til finans-, bank- og kundekonti.  

Det tilknyttede dokumentet lukkes, og kunden blir kreditert med det overflødige betalingsbeløpet.  

## Slik finner du et bestemt salgsdokument som ikke er fullstendig fakturert
**Betalingsregistrering**-siden støtter deg i oppgaver som er nødvendige for å balansere interne konti med faktiske kontanttall, for å sikre effektiv innkreving fra kunder og betaling ved forfall til leverandører. Den viser utestående innkommende betalinger som linjer som representerer salgsdokumentene der et beløp er forfalt til betaling.  

Vanligvis når en betaling er gjort i banken eller på annen måte, er relaterte salgs- eller kjøpsdokumenter representert som en linje på siden **Betalingsregistrering**, fordi det aktuelle dokumentet venter på at betalingen skal bokføres mot det utestående beløpet. Noen ganger er imidlertid ikke en utført betaling representert av en linje på siden **Betalingsregistrering**, vanligvis fordi det aktuelle dokumentet ikke er fullstendig fakturabokført.

På siden **Dokumentsøk** kan du søke blant dokumenter som ikke er fullstendig fakturert. Du kan søke basert på ett eller flere av følgende kriterier:  

* Dokumentnummer  
* Beløp eller beløpområde  

Fremgangsmåten nedenfor forklarer hvordan du søker etter et bestemt dokument ved å bruke begge søkevilkårene.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsregistrering** og velg den relaterte koblingen.
2. Med pekeren på en av linjene, velger du handlingen **Søk i dokumenter**.
3. På siden **Dokumentsøk** skriver du inn en søkeverdi i feltet **Bilagsnr.**.  

    > [!NOTE]  
    >   Verdien du angir i dette feltet, er omsluttet med skjulte jokertegn. Dette betyr at funksjonen søker etter alle bilagsnumre som inneholder den angitte verdien.    
4. I feltet **Beløp** angir du det bestemte beløpet som finnes i dokumentet du vil finne.  
5. I feltet **Beløpstoleranse-%** angir du en prosentverdi for å definere området for beløp som du vil søke etter for å finne det åpne dokumentet.  

    Hvis du skriver inn 10, søkes det etter beløp i et område mellom ti prosent lavere og ti prosent høyere enn verdien i feltet **Beløp**.    
6. Velg handlingen **Søk**.  

Søkefunksjonen søker blant dokumenter som ikke er fullstendig fakturert, basert på de angitte kriteriene.  

Hvis ett eller flere dokumenter samsvarer med søkekriteriene, åpnes siden **Dokumentsøkeresultat** for å vise linjer som representerer disse dokumentene. Hver linje inneholder et dokumentnummer, en beskrivelse og et beløp. Denne informasjonen gjør det enklere å finne et bestemt dokument.

Hvis en betaling i banken ikke er representert av noen dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)], kan du åpne en forhåndsutfylt finanskladd fra siden **Betalingsregistrering** for å bokføre betalingen direkte til motkontoen uten å bruke betalingen på et dokument. Alternativt kan du registrere betalingen i kladden til opprinnelsen til betalingen er fastsatt.  

## Slik registrerer eller bokfører du en betaling uten et relatert dokument:
Hvis en betaling i banken ikke er representert av noen dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)], kan du åpne en forhåndsutfylt finanskladdlinje fra siden **Betalingsregistrering** for å bokføre betalingen direkte til motkontoen uten å bruke betalingen på et dokument. Alternativt kan du registrere betalingen i kladden til opprinnelsen til betalingen er klarlagt.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsregistrering** og velg den relaterte koblingen.
2. Velg handlingen **Finanskladd**.  

    Siden **Finanskladd** åpnes med én linje som inneholder motkontoen for kladden som er definert på siden **Betalingsregistreringsoppsett**.  
3. Fyll ut de gjenstående feltene på finanskladden. Angi for eksempel beløpet, kundenummeret eller informasjonen fra bankkontoutdraget. Hvis du vil ha mer informasjon, kan du se [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).  

Du kan bokføre kladdelinjen for å oppdatere totalsummen på motkontoen. Du kan også la kladdelinjen være upostert, og kanskje tilføye den med en merknad om at betalingen trenger mer analyse.  

Hvis du ikke bokfører kladdelinjen, øker verdien i feltet **Ikke-bokført saldo** nederst på siden **Betalingsregistrering**.  

## Se også
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]