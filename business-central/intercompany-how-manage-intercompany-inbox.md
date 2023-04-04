---
title: Administrere den konserninterne innboksen og utboksen
description: 'Konserninterne transaksjoner du mottar fra de konserninterne partnerne dine, er oppført i den konserninterne innboksen der du behandler dem manuelt eller automatisk.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.search.form: '600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611'
ms.date: 03/09/2022
ms.author: edupont
---
# Administrere den konserninterne innboksen og utboksen
Alle de konserninterne transaksjonene du mottar elektronisk fra de konserninterne partnerne, er oppført i den konserninterne innboksen.  

Avhengig av hvordan det konserninterne selskapet er definert for selskapet, blir imidlertid enkelte transaksjoner automatisk replikert til de relevante konserninterne partnerne. Fra lanseringsbølge 1 for 2022 kan du definere selskapet for automatisk oppretting av mottatte konserninterne transaksjoner fra konserninterne partnere, bokført gjennom den konserninterne finanskladden. Hvis du vil ha mer informasjon, kan du se [Slik fyller du ut og bokfører en konsernintern kladd](intercompany-how-work-documents-journals.md#to-fill-in-and-post-an-intercompany-journal).  

## Ordre innboksen  
 Du kan bruke filterfeltene øverst på innbokssiden til å bestemme hvilke transaksjoner som skal vises på siden. Hvis du for eksempel bare vil se på transaksjoner som en bestemt partner har opprettet, kan du angi filtre i filtrene for **transaksjonskilde** og **kode for konsernintern partner**.  

### Transaksjonskilde  
Hva du kan gjøre med en transaksjon, avhenger av om den ble:  

- Opprettet av den konserninterne partneren  
- Avvist av den konserninterne partneren og returnert til deg  

Du kan bruke feltet **Vis transaksjonskilde** til å filtrere siden **Konserninterne inngående transaksjoner** slik at det bare viser én av disse transaksjonstypene. (Du kan også filtrere etter konsernintern partner eller etter innholdet i **Linjehandling**-feltet.)  

#### Opprettet av konsernintern partner  
 Når du mottar en ny transaksjon som ble opprettet av partneren, kan du velge å:

- Godta transaksjonen  
- Avvise transaksjonen (returnere den til partneren)  
- Avbryte transaksjonen (slette transaksjonen, men ikke returnere den til partneren)  

#### Returnert fra konsernintern partner  
 Hvis transaksjonen ble avvist av den konserninterne partneren, kan du bare avbryte transaksjonen i innboksen. Deretter må du opprette korrigeringslinjer eller reversere kladden eller bilaget i selskapet.  

## Opprette innboksposter på nytt  
 Hvis du godtok en transaksjon i innboksen, men deretter slettet bilaget eller kladden i stedet for å bokføre det/den, kan du opprette innboksposten på nytt og godta den på nytt.  

## Få oversikt over konserninterne transaksjoner for en periode  
 Du kan få oversikt over alle de konserninterne transaksjonene du har sendt og mottatt i en periode. Rapporten **Konserninterne transaksjoner** viser alle konserninterne finansposter, kundeposter og leverandørposter.

 > [!NOTE]  
 > Hvis de konserninterne partnerne er i samme database, overføres transaksjoner uten å måtte filen eller e-post. Se feltet **Overføringstype** på siden **Konsernintern partner**. <br /><br />
I så fall kan du konfigurere systemet til å hoppe over innboksen og utboksen ved å merke av for henholdsvis **Godta transaksjoner automatisk** på siden **Konsernintern partner** og **Send transaksjoner automatisk** på siden **Konserninternt oppsett**. Inngående konserninterne transaksjoner kan bare godtas automatisk hvis oppgaveplanlegging er aktivert. Hvis du vil ha mer informasjon, kan du se [Konfigurere Business Central Server – Oppgaveplanleggingsinnstillinger](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Task).

## Slik importerer du konserninterne transaksjoner fra en fil

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Hvis du har en konsernintern partner som ikke er i samme database som selskapet ditt, kan du motta konserninterne transaksjoner fra partneren i en XML-fil. Deretter må du importere transaksjonene til innboksen.  

1. Lagre filen på lokasjonen du har angitt i feltet **Detaljer om konsernintern innboks** når du konfigurerer konserninternt selskap.  
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninterne inngående transaksjoner**, og velg deretter den relaterte koblingen.
3. På siden **Konserninterne inngående transaksjoner** velger du **Importer transaksjonsfil**.  
4. På siden som vises, velger du XML-filen som inneholder transaksjonene, og deretter velger du **Åpne**-knappen.  

Transaksjonene importeres til innboksen, og du kan nå behandle dem.

## Slik behandler du inngående konserninterne transaksjoner  
Når de konserninterne partnerne sender deg konserninterne transaksjoner, ender transaksjonene opp i den konserninterne innboksen. Du må vurdere hver transaksjon i innboksen og utføre de nødvendige handlingene.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninterne inngående transaksjoner**, og velg deretter den relaterte koblingen.  
2. På siden **Konserninterne inngående transaksjoner** velger du en linje og velger en handling som **Godta**, for å behandle linjen.
3. På siden **Fullfør KI-innbokshandling** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg **OK**.  

For linjer som du behandlet med **Godta**-handlingen, bilag eller kladdelinjer vil bli opprettet i selskapet. Åpne hvert bilag eller hver kladd, gjør de nødvendige endringene, og bokfør dem.  

Linjene som du behandlet med **Gå tilbake til partner**-handlingen, vil bli flyttet til utboksen fra der du kan deretter sende dem til partneren.

For linjer du behandlet med **Returnert av partner**-handlingen, må du nå bokføre en korreksjon av den opprinnelige transaksjonen du bokførte i selskapet ditt.

## Slik behandler du utgående konserninterne transaksjoner  
Når du bokfører konserninterne kladder eller bilag eller sender en konsernintern bestillingsbekreftelse, sendes transaksjonene til den konserninterne utboksen. Du må åpne utboksen og behandle dem for at de skal bli sendt videre til de konserninterne partnerne.  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninterne utgående transaksjoner**, og velg deretter den relaterte koblingen.  
2. På siden **Konserninterne utgående transaksjoner** velger du en linje og velger en handling som **Gå tilbake til innboks**, for å behandle linjen.

Linjene som du behandlet med **Send til konsernintern partner**-handlingen, vil bli sendt til innboksen til den relevante partneren.

Linjene som du behandlet med **Gå tilbake til innboks**-handlingen, vil bli flyttet til innboksen der du kan godta dem til å opprette bilag eller kladdelinjer i selskapet.  

For linjer du behandlet med **Avbryt**-handlingen, må du nå bokføre en korreksjon av den opprinnelige transaksjonen du bokførte i selskapet ditt.  

## Slik oppretter du konserninterne innbokstransaksjoner på nytt:  
Noen ganger vil du kanskje opprette en transaksjon på nytt i innboksen eller utboksen. Hvis du for eksempel godtok en transaksjon i innboksen, men deretter slettet bilaget eller kladden i stedet for å bokføre det/den, kan du opprette innboksposten på nytt og godta den på nytt.  

Følgende fremgangsmåte beskriver hvordan du oppretter innbokstransaksjoner på nytt, men de samme trinnene gjelder også for utboksen.

  1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Håndterte inngående KI-transaksjoner**, og velg deretter den relaterte koblingen.  

  2.  På siden **Håndterte inngående KI-transaksjoner** velger du linjen med transaksjonen du vil opprette på nytt i innboksen, og velger deretter **Opprett inngående transaksjon på nytt**.  

## Se også
[Behandle konserninterne transaksjoner](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
