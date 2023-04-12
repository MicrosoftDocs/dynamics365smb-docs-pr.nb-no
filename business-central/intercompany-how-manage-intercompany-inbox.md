---
title: Administrere den konserninterne innboksen og utboksen
description: 'Konserninterne transaksjoner du mottar fra de partnerne dine, er oppført i den konserninterne innboksen der du behandler dem manuelt eller automatisk.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
---
# Administrere den konserninterne innboksen og utboksen

De konserninterne transaksjonene du mottar elektronisk fra partnerne, er oppført på siden **Konsernintern innboks**. Hvis du vil lære hvordan du behandler inngående konserninterne transaksjoner, går du til [Behandle inngående konserninterne transaksjoner](#process-incoming-intercompany-transactions). De konserninterne transaksjonene du sender til partnerne, er oppført på siden **Konsernintern utboks**. Hvis du vil lære hvordan du behandler utgående konserninterne transaksjoner, går du til [For å behandle utgående konserninterne transaksjoner](#to-process-outgoing-intercompany-transactions).

Enkelte transaksjoner håndteres imidlertid automatisk, avhengig av det konserninterne oppsettet. Du kan definere kildeselskapet og partnerselskapene slik at det automatisk opprettes dokumenter og kladder som tilsvarer transaksjoner som partnere bokfører gjennom den konserninterne finanskladden. Hvis du vil lære mer om bruk av konserninterne kladder, går du til [Fyll ut og bokfør en konsernintern kladd](intercompany-how-work-documents-journals.md#fill-in-and-post-an-intercompany-journal).  

## Ordre innboksen  

Du kan bruke filterfeltene øverst på innbokssiden til å bestemme hvilke transaksjoner som skal vises på siden. Hvis du for eksempel bare vil utforske transaksjoner som en bestemt partner har opprettet, bruker du filtrene for **transaksjonskilde** og **kode for konsernintern partner**.  

### Transaksjonskilde  

Hva du kan gjøre med en transaksjon, avhenger av om den ble:  

* Opprettet av den konserninterne partneren  
* Avvist av den konserninterne partneren og returnert til deg  

Bruk feltet **Vis transaksjonskilde** til å filtrere siden **Konserninterne inngående transaksjoner** slik at det bare viser én av disse transaksjonstypene. Du kan også filtrere etter konsernintern partner eller etter innholdet i **Linjehandling**-feltet.  

#### Opprettet av konsernintern partner  

 Når du mottar en ny transaksjon som ble opprettet av partneren, kan du velge å:

* Godta transaksjonen  
* Avvise transaksjonen (returnere den til partneren)  
* Avbryte transaksjonen (slette transaksjonen og ikke returnere den til partneren)  

#### Returnert fra konsernintern partner  

Hvis den konserninterne partneren avviser en transaksjon, må du avbryte transaksjonen i innboksen og deretter opprette korrigeringslinjer eller reversere kladden eller bilaget.  

## Opprette innboksposter på nytt  

Hvis du godtok en transaksjon i innboksen, men deretter slettet bilaget eller kladden i stedet for å bokføre det/den, kan du opprette innboksposten på nytt og godta den på nytt.  

## Få oversikt over konserninterne transaksjoner for en periode  

Du kan få oversikt over alle de konserninterne transaksjonene du har sendt og mottatt i en periode. Rapporten **Konserninterne transaksjoner** viser alle konserninterne finansposter, kundeposter og leverandørposter.

> [!NOTE]  
> Hvis de konserninterne partnerne er i samme database, kan partnerne automatisk godta transaksjoner. Gå direkte til sidene **Håndterte konserninterne innbokstransaksjoner** og **Håndterte konserninterne utbokstransaksjoner**. Hvis du vil lære mer om automatisk godkjenning av transaksjoner, går du til [Automatisk godkjenning av transaksjoner fra konserninterne partnere](intercompany-how-setup.md#auto-accept-transactions-from-intercompany-partners).  
>
> * For synkroniseringspartneren, på siden **Konserninternt oppsett**, slår du på **Send transaksjoner automatisk**-vekslebryteren.
> * For partnerselskaper, på siden **Konsernintern partner**, slår du på **Godta transaksjoner automatisk**-vekslebryteren.  

## Importer konserninterne transaksjoner fra en fil

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Hvis du har en konsernintern partner som ikke er i samme database som selskapet ditt, kan du motta konserninterne transaksjoner fra partneren i en XML-fil. Deretter må du importere transaksjonene til innboksen.  

1. Lagre filen på lokasjonen du har angitt i feltet **Detaljer om konsernintern innboks** når du konfigurerer konserninternt selskap.  
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninterne inngående transaksjoner**, og velg deretter den relaterte koblingen.
3. På siden **Konserninterne inngående transaksjoner** velger du **Importer transaksjonsfil**.  
4. På siden som vises, velger du XML-filen som inneholder transaksjonene, og deretter velger du **Åpne**-knappen.  

Transaksjonene importeres til innboksen, og du kan nå behandle dem.

## Behandle inngående konserninterne transaksjoner  

Når de konserninterne partnerne sender deg konserninterne transaksjoner, ender transaksjonene opp i den konserninterne innboksen. Du må vurdere hver transaksjon i innboksen og utføre de nødvendige handlingene.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninterne inngående transaksjoner**, og velg deretter den relaterte koblingen.  
2. På siden **Konserninterne inngående transaksjoner** velger du en linje og velger en handling som **Godta**, for å behandle linjen.
3. På siden **Fullfør KI-innbokshandling** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg **OK**-knappen.  

For linjer som du godtar, opprettes dokument eller kladdelinjer i selskapet. Åpne hvert bilag eller hver kladd, gjør de nødvendige endringene, og bokfør dem.  

Linjer du avviser og returnerer til partneren, går til den konserninterne utboksen, der du kan sende dem til partneren din.

For linjer som en partner avviste og returnerte til deg, må du bokføre en korreksjon av den opprinnelige transaksjonen du bokførte i selskapet ditt.

## Slik behandler du utgående konserninterne transaksjoner  

Når du bokfører konserninterne kladder eller bilag eller sender en konsernintern bestillingsbekreftelse, går transaksjonene til den konserninterne utboksen. For å sende dem til de konserninterne partnerne åpner du utboksen og behandler dem.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninterne utgående transaksjoner**, og velg deretter den relaterte koblingen.  
2. På siden **Konserninterne utgående transaksjoner** velger du en linje og velger en handling som **Gå tilbake til innboks**, for å behandle linjen.

Bruk **Send til konsernintern partner**-handlingen til å sende linjer til den relevante partneren.

Bruk **Gå tilbake til innboks**-handlingen til å flytte linjer til innboksen der du kan godta dem til å opprette bilag eller kladdelinjer i selskapet.  

Hvis du bruker **Avbryt**-handlingen, må du nå bokføre en korrigering til transaksjonen du opprinnelig bokførte i selskapet ditt.  

## Opprett konserninterne innbokstransaksjoner på nytt  

Du vil du kanskje opprette en transaksjon på nytt i innboksen eller utboksen. Hvis du for eksempel godtok en transaksjon i innboksen, men deretter slettet bilaget eller kladden i stedet for å bokføre det/den, kan du opprette innboksposten på nytt og godta den på nytt.  

Følgende fremgangsmåte beskriver hvordan du oppretter innbokstransaksjoner på nytt, men de samme trinnene gjelder også for utboksen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Håndterte inngående KI-transaksjoner**, og velg deretter den relaterte koblingen.  
2. På siden **Håndterte inngående KI-transaksjoner** velger du linjen med transaksjonen du vil opprette på nytt i innboksen, og velger deretter **Opprett inngående transaksjon på nytt**.  

## Se også

[Behandle konserninterne transaksjoner](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
