---
title: Definere bokføring av konserninterne transaksjoner
description: Lær hvordan du oppretter et konserninternt partnerskap.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 09/27/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621, 653_Primary'
ms.service: dynamics-365-business-central
---
# Sett opp konserninterne transaksjoner

Konserninternt partnerskap gjør det enklere å håndtere regnskapsprosesser når to eller flere datterselskaper i et selskap ofte gjør forretninger med hverandre. Partnere kan utveksle transaksjoner, for eksempel salg og kjøp, og håndter dem manuelt eller automatisk. Når en partner for eksempel sender en salgskladdelinje til en annen partner, opprettes det en kjøpskladdelinje for mottakspartneren.

Den konserninterne kontoplanen kan for eksempel være en versjon av synkroniseringspartnerens kontoplan. Hver partner tildeler kontoene sine til den konserninterne kontoplanen. Hver partner tildeler også dimensjoner og dimensjonsverdier til de konserninterne dimensjonene.

> [!NOTE]
> I lanseringsbølge 1 i 2023 vi har innført en forbedret **Konserninternt oppsett**-side. Den nye siden gjør det enklere å definere et konserninternt partnerskap ved å konsolidere alle oppgavene som er definert, på én side. Hvis du er ny til [!INCLUDE [prod_short](includes/prod_short.md)], bruker du allerede den nye opplevelsen. Hvis du er en eksisterende kunde, kan administratoren aktivere funksjonen **Godta automatisk konserninterne finanskladdtransaksjoner** på siden **Funksjonsstyring**.
>
> Oppgavene i denne artikkelen tar utgangspunkt i at funksjonsbryteren er aktivert. Hvis du allerede har definert et konserninternt partnerskap, kan du fortsette å bruke det.

## Før du begynner

Før du begynner å konfigurere det konserninterne partnerskapet, må du ta noen avgjørelser.

|Avgjørelse  |Beskrivelse  |
|---------|---------|
|Hvilken kontoplan skal være grunnlaget for den konserninterne kontoplanen?     | Alle selskaper i partnerskapet må bruke den samme konserninterne kontoplanen. Du kan basere den konserninterne kontoplanen på kontoplanen fra et av selskapene i partnerskapet, eller opprette en ny konsernintern kontoplan. Du tildeler kontoene til bruk i partnerskapet på begge måter, slik at både partneren sender og mottar transaksjoner i de riktige kontoene. Lær mer om hvordan du definerer den konserninterne kontoplanen under [Definer den konserninterne kontoplanen](#set-up-the-intercompany-charts-of-accounts).         |
|Hvilke dimensjoner skal være grunnlaget for de konserninterne dimensjonene?     | Hvis du bruker konserninterne dimensjoner, må de være like for alle selskapene i partnerskapet. Når du har angitt de konserninterne dimensjonene, tildeler du dimensjonsverdiene. Lær mer om tildeling av dimensjonsverdier under [Definer konserninterne dimensjoner](#set-up-intercompany-dimensions).        |
|Hvilke partnere er kunder eller leverandører, eller begge deler?     |  Lær mer om oppsett av kunde- og leverandørselskaper i et konserninternt partnerskap under [Definer konserninterne partnere som kunder og leverandører](#set-up-intercompany-partners-as-customers-and-vendors).       |
|Vil du angi bankkontoene som skal brukes i partnerskapet?| Du kan gjøre prosessen med å registrere betalingstransaksjoner raskere ved å angi bankkontoen som skal brukes for hvert partnerselskap. Lær mer under [Angi hvilke bankkontoer som skal brukes for konserninterne partnere](#specify-the-bank-accounts-to-use-for-intercompany-partners). |
|Hvordan vil du identifisere selskapene i partnerskapet?     | Alle parter må være enige om en unik identifikasjonskode for konsernintern partner for hvert firma. Du tildeler koden til kunde- og leverandørkortene for å identifisere relaterte transaksjoner. Lær mer om identifikatorer under [Opprett nummerserier](ui-create-number-series.md).        |
|Hvordan vil du behandle varenumre?     | Hvis konserninterne linjer inneholder varer, kan du bruke dine egne varenumre eller definere partnerens varenumre for hver vare, enten i feltet **Leverandørs varenr.** eller i feltet **Felles varenr.** på varekortet. Du kan også bruke handlingen **Varereferanse** til å tildele varenes numre til de konserninterne partnerbeskrivelsene for varene. Hvis du vil lære mer om varereferanser, går du til [Bruk varereferanser](inventory-how-use-item-cross-refs.md).        |
|Er ressurser involvert?     | Hvis konserninterne salgstransaksjoner inkluderer ressurser, fyller du ut feltet **Finanskontonr. for KI-partnerkjøp** på ressurskortet for hver ressurs. Feltet inneholder nummeret til den konserninterne finanskontoen der beløpet for denne ressursen skal bokføres i partnerselskapet. Hvis du vil ha mer informasjon om ressurser, går du til [Definer ressurser](projects-how-setup-resources.md).<br><br>**Obs!**<br>Konserninterne kjøpstransaksjoner som omfatter ressurser, aktiva og varegebyrer, støttes ikke fullstendig. I partnerselskapet er **Linjetype**-feltet tomt på kjøpsdokumentlinjene som inneholder disse enhetene. Du må oppdatere feltet manuelt.        |

## Oversikt over trinnene for å komme i gang

Bruk siden **Konserninternt oppsett** til å definere følgende komponenter for konserninterne transaksjoner:

* Selskapets konserninterne innstillinger.
* Selskapet som skal være synkroniseringspartneren.
* Den konserninterne kontoplanen som alle partnere bruker til å utveksle transaksjoner.
* Tildelingene mellom kontoer i kontoplanen og konsernintern kontoplan for inngående og utgående transaksjoner for hver partner.
* Konserninterne dimensjoner og dimensjonsverdier som skal brukes, og hvordan de tildeles til dimensjoner for hver partner.
* Selskapene som er de konserninterne partnerne.
* Selskapene som er leverandører eller kunder, eller begge deler.

## Konfigurer en synkroniseringspartner

Alle partnere må bruke den samme konserninterne kontoplanen og, om nødvendig, de samme konserninterne dimensjonene. Du kan spare tid når du definerer partnerskapet ved hjelp av kontoplanen og dimensjonene for en av partnerne som en opprinnelig plan for den konserninterne kontoplanen og dimensjonene. Selskapet du bruker som opprinnelig plan, kalles *synkroniseringspartneren*. Synkroniseringspartneren er vanligvis det hovedkontorselskapet, men den trenger ikke være det.

På siden **Konserninternt oppsett** angir hver partner synkroniseringspartneren i feltet **Synkroniseringspartner** . Etterpå angis den konserninterne kontoplanen og konserninterne dimensjonene automatisk for dem, basert på oppsettet for synkroniseringspartneren. Partnerne bruker deretter sidene **Konsernintern kontoplantildeling** og **Konsernintern dimensjonstildeling** til å tildele kontoplanen og dimensjonene til den konserninterne kontoplanen og dimensjonene og omvendt. 

> [!NOTE]
> Det er viktig å tildele kontoer og dimensjoner i begge retninger. Det vil si både til den konserninterne kontoplanen og dimensjonene, og fra disse til dine egne kontoer og dimensjoner.

### Få kontakt med partnere i en annen leier eller et annet miljø

Hvis én eller flere partnere [!INCLUDE [prod_short](includes/prod_short.md)] er i en annen leier eller et annet miljø, er det noen ekstra trinn for å opprette tilkoblingen. Fremgangsmåten gjelder for alle partnere i en annen leier eller et annet miljø.

* Konfigurer [!INCLUDE [prod_short](includes/prod_short.md)] som en registrert app i Azure Portal.
* Legg til og aktiver appregistreringen i [!INCLUDE [prod_short](includes/prod_short.md)].
* Utveksle informasjon om deres konserninterne oppsett. Hver partner kan få denne informasjonen fra den assisterte oppsettsveiledningen **Oppsett av kryssmiljø for KI-partner**.

   |Kopiere fra partnerens oppsett  |Kopiere til oppsettet  |
   |---------|---------|
   |Nåværende tilkoblingsnettadresse     |KI-partnerens tilkoblingsnettadresse         |
   |Nåværende selskaps-ID     |KI-partnerens selskaps-ID         |
   |Konsernintern ID     |KI-partnerens konserninterne ID         |
   |Selskapsnavn     |KI-partnerens selskapsnavn         |

* Bytt følgende godkjenningsinnstillinger slik at [!INCLUDE [prod_short](includes/prod_short.md)] kan godkjennes når den kobles til. Hver partner kan få denne informasjonen fra sin registrerte app. Hvis du vil finne ut mer om hvordan du oppretter en registrert app, kan du gå til [Opprette en registrert app i Azure-portalen](#create-a-registered-app-in-azure-portal).  

  * Klient-ID
  * Klienthemmelighet
  * Tokenendepunkt
  * Nettadresse for omdirigering

Kjør den assisterte oppsettsveiledningen for **Oppsett av kryssmiljø for KI-partner** i alle firmaer for å angi informasjonen. Du starter veiledningen på siden **Konsernintern partner** ved å bruke handlingen **Koble til eksternt oppsett**.

#### Opprette en registrert app i Azure Portal

Denne prosessen er bare nødvendig hvis du vil få kontakt med en partner med [!INCLUDE [prod_short](includes/prod_short.md)] i en annen leier eller et annet miljø.

> [!TIP]
> Det er lurt å ha et tekstredigeringsprogram åpent, for eksempel Notisblokk, mens du oppretter den registrerte appen din. Du trenger noe av informasjonen når du kjører den assisterte oppsettsveiledningen **Oppsett av kryssmiljø for KI-partner**, så det er fint å ha informasjonen tilgjengelig.

1. Gå til [Azure-portalen](https://portal.azure.com/#home).
2. Velg **Microsoft Entra-ID**-tjenesten.
3. Velg **Appregistreringer** i navigasjonsruten.
4. På siden **Appregistreringer** velger du **ny registrering**.
5. Gi programmet et navn.
6. Velg kontotypen **Kontoer i en hvilken som helst organisasjonskatalog (enhver Microsoft Entra-katalog – flere leietakere)**.
7. Velg **Web** i feltet **Velg en plattform** for omadresserings-URIen, og angi deretter URI-en. Eksempel \**https://businesscentral.dynamics.com/OAuthLanding.htm**.

  Hvis du arbeider med en innebygd ISV, trenger du kanskje en annen URI.

8. Registrer appen.
9. På siden **Konsernintern app**, i navigasjonsruten, velger du **API-tillatelser**.
10. Velg handlingen **Legg til en tillatelse**.
11. I fanen **Microsoft API-er** velger du **Dynamics 365 Business Central**.
12. I ruten **Be om API-tillatelser** velger du **Apptillatelser**, og deretter velger du tillatelsen **API.ReadWrite.All**.
13. På siden **Konsernintern app | API-tillatelse** velger du handlingen **Gi administratorsamtykke for Contoso** , og gi deretter samtykke.
14. I navigasjonsruten velger du **Sertifikater og hemmeligheter**.
15. Velg kategorien **Klienthemmeligheter**, og velg deretter **Ny klienthemmelighet**.
16. Skriv inn et navn på hemmeligheten i ruten **Legg til en klienthemmelighet**, og angi når den skal utløpe.

  > [!NOTE]
  > Alle partnere som er i forskjellige miljøer, må fornye hemmeligheten før den utløper.

  > [!IMPORTANT]
  > Kopiere IDen i **Verdi-feltet** før du forlater siden for **Konsernintern app | Sertifikater og hemmeligheter**. Du trenger den i et senere trinn, og den vil ikke være tilgjengelig etter at du har forlatt siden. Du kan for eksempel lime inn verdien i et tekstredigeringsprogram.

17. I navigasjonsruten velger du  **Oversikt**.
18. Kopier verdien i feltet **Program (klient)-ID**. Du kan for eksempel lime inn verdien i et tekstredigeringsprogram.
19. Velg handlingen **Endepunkter**, og kopier deretter verdien i feltet **OAuth 2.0-tokenendepunkt (v2)**. Du kan for eksempel lime inn verdien i et tekstredigeringsprogram.
20. Kopier verdien i feltet **Katalog (klient)-ID**. Du kan for eksempel lime inn verdien i et tekstredigeringsprogram.
21. I tokenverdien du kopierte, erstatter du **organisasjoner** med verdien du kopierte fra feltet **Katalog-ID (leier)** i det forrige trinnet.

#### Legge til og aktivere den registrerte appen i Business Central

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Microsoft Entra-programkort**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. I feltet **Status** velger du **Aktivert**. 
4. Velg handlingen **programkort**. 
5. I **Tillatelsessett**-feltet velger du tillatelsessettet **API – konserninternt kryssmiljø**.

## Definer den konserninterne kontoplanen

Alle partnere må bruke den samme konserninterne kontoplanen og tildele kontoene i sin egen kontoplan til det. Hvis kontoplanen for selskapet definerer den konserninterne kontoplanen for partnerselskapene, følger du fremgangsmåten i denne delen.

Hvis du bruker en XML-fil som inneholder den konserninterne kontoplanen, følger du fremgangsmåten under [Importer eller eksporter en konsernintern kontoplan](intercompany-how-setup.md#import-or-export-an-intercompany-chart-of-accounts).  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninternt oppsett**, og velg deretter den relaterte koblingen.
2. Velg handlingen **KI-kontoplan**.
3. For å legge til kontoer gjør du et av følgende på siden **Konsernintern kontoplan**:
    * Velg **Opprett** og angi deretter hver konto på en linje på siden.  
    * Hvis den konserninterne kontoplanen vil være identisk med eller vil ligne på den vanlige kontoplanen, kan du fylle ut siden automatisk ved å velge handlingen **Kopier fra kontoplan**. Du kan redigere de nye linjene etter behov.
    * Hvis du har definert en konsernintern kontoplan for en synkroniseringspartner, bruker du handlingen **Synkroniseringsoppsett** til å kopiere disse kontoene.

    > [!TIP]
    > Hvis du kopierer den konserninterne kontoplanen fra en synkroniseringspartner, kan du bruke handlingen **Synkroniseringsoppsett** til å oppdatere de konserninterne kontoene med eventuelle endringer partneren gjør i sine.

Det neste trinnet er å tildele kontoplanen i den konserninterne kontoplanen. Finn ut mer under [Tildel den konserninterne kontoplanen til selskapets kontoplan](#map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts).

### Importer eller eksporter en konsernintern kontoplan

Synkroniseringsselskapet kan dele kontoplanen med partnere ved å eksportere den til en fil. Partnere kan importere filen for å få kontoplanen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninternt oppsett**, og velg deretter den relaterte koblingen.
2. Velg handlingen **KI-kontoplan**.
3. På siden **Konsernintern kontoplan** velger du **Importer/eksporter**-handlingen og velger deretter **Importer** eller **Eksporter**.
4. Velg filen som skal importeres eller eksporteres.  

Siden **Konsernintern kontoplan** fylles ut med nye eller redigerte finanskontolinjer i henhold til den konserninterne kontoplanen i filen. Eventuelle eksisterende urelaterte linjer på siden forblir uendret.

## Tildel den konserninterne kontoplanen til selskapets kontoplan  

Når du har definert eller importert den konserninterne kontoplanen, tildeler du hver konserninterne konto til en av kontoene dine. På siden **Konsernintern kontoplan** angir du hvordan konserninterne finanskontoer i innkommende transaksjoner tildeles til finanskontoer fra selskapets kontoplan.

Hvis de konserninterne kontoene og kontoene har samme numre, kan du tildele kontoene automatisk.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninternt oppsett**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **KI-kontoplan**.

    > [!TIP]
    > Du må kanskje utvide siden til bred oppsettvisningen for å få tilgang til handlingene på siden.

3. På siden **Konsernintern kontoplan** velger du handlingen **Kontoplantildeling**.
4. Du kan tildele kontoer manuelt eller automatisk.

    * Hvis du vil opprette tildelingen manuelt i rutene **Konsernintern kontoplan** og **Finanskontoplan**, velger du en konto, og deretter velger du en konto i **Finansnr.** og **KI-nr.** -feltene.
    * Hvis du automatisk vil tildele kontoer som har samme numre, merker du linjene du vil tildele, velger du **Tildel til konto med samme nr.**-handlingen, og deretter velger du kontoplanen du vil oppdatere.

    > [!TIP]
    > Hvis du vil tildele mange eller kanskje alle kontoer, velger du en linje, velger :::image type="icon" source="media/show-more-options-icon.png" border="false"::: og velger deretter **Velg flere**.

## Definer konserninterne dimensjoner

Hvis partnerne vil utveksle transaksjoner med tilknyttede dimensjoner, må dere bli enige om dimensjonene som alle skal bruke. Synkroniseringsselskapet kan for eksempel opprette en forenklet versjon av dimensjonene sone, eksportere dem til en XML-fil og deretter distribuere filen til hver partner. Hver partner kan importere XML-filen på siden **Konserninterne dimensjoner** og deretter tildele de konserninterne dimensjonene til dimensjonene sine. Finn ut mer under [Tildel konserninterne dimensjoner til selskapets dimensjoner](#map-intercompany-dimensions-to-your-companys-dimensions).

> [!NOTE]
> Hvert selskap må tildele dimensjonene til de konserninterne dimensjonene for utgående dokumenter og innkommende dokumenter. Tildeling av kontoer i begge retninger er viktig og bidrar til å opprettholde konsekvensen på tvers av selskapene.

Hvis partnerne skal bruke synkroniseringspartnerens konserninterne dimensjoner, følger du fremgangsmåten i denne delen. Hvis du vil dele ved å bruke en XML-fil som inneholder de konserninterne dimensjonene, følger du fremgangsmåten under [Importer eller eksporter konserninterne dimensjoner](#import-or-export-intercompany-dimensions).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninternt oppsett**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **KI-dimensjoner**.
3. For å legge til dimensjoner gjør du et av følgende på siden **Konserninterne dimensjoner**:
    * Velg **Opprett** og angi deretter hver dimensjon på en linje.  
    * Hvis de konserninterne dimensjonene vil være identisk med eller vil ligne på de vanlige dimensjonene, kan du fylle ut siden automatisk ved å velge handlingen **Kopier fra dimensjoner**. Etterpå kan du redigere de nye linjene etter behov.
    * Hvis du har angitt konserninterne dimensjoner for en synkroniseringspartner, bruker du handlingen **Synkroniseringsoppsett** til å kopiere disse dimensjonene.

    > [!TIP]
    > Hvis du kopierer de konserninterne dimensjonene fra en synkroniseringspartner, kan du bruke handlingen **Synkroniseringsoppsett** til å oppdatere de konserninterne dimensjonene med eventuelle endringer partneren gjør i sine.  

### Importer eller eksporter konserninterne dimensjoner  

Synkroniseringsselskapet kan dele dimensjonene med partnere ved å eksportere dem til en fil. Partnere kan importere filen for å få dimensjonene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninternt oppsett**, og velg deretter den relaterte koblingen.
2. Velg handlingen **KI-dimensjoner**.  
3. På siden **Konserninterne dimensjoner** velger du **Importer/eksporter**-handlingen og velger deretter **Importer** eller **Eksporter**.
4. Velg filen som skal importeres eller eksporteres.

Det neste trinnet er å tildele dimensjonene med de konserninterne dimensjonene. Finn ut mer under [Tildel konserninterne dimensjoner til selskapets dimensjoner](#map-intercompany-dimensions-to-your-companys-dimensions).

### Tildel konserninterne dimensjoner til selskapets dimensjoner

Etter at du angir dimensjonene du bruker, tildeler du hver konserninterne dimensjonen til en av selskapets dimensjoner, og omvendt. Bruk siden **Konsernintern dimensjonstildeling** til å angi tildelingen. Etterpå gjentar du prosessen for dimensjonsverdiene.

* Angi hvordan konserninterne dimensjoner på inngående transaksjoner tildeles til dimensjoner fra selskapets oversikt over dimensjoner.
* Angi hvordan dimensjonene skal oversettes til konserninterne dimensjoner i *utgående transaksjoner*.

Hvis noen av de konserninterne dimensjonene har samme kode som de tilsvarende dimensjonene i selskapet, kan du tildele dimensjonene automatisk.  

I fremgangsmåten nedenfor tilordner du først konserninterne dimensjoner til dimensjoner for inngående dokumenter i ruten **Konserninterne dimensjoner**. Deretter tilordner du dimensjoner til konserninterne dimensjoner for utgående dokumenter i ruten **Nåværende selskapsdimensjoner**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninternt oppsett**, og velg deretter den relaterte koblingen.
2. Velg handlingen **KI-dimensjoner**.
3. På siden **Konserninterne dimensjoner** velger du handlingen **Dimensjonstildeling**.
4. Du kan tildele dimensjonene manuelt eller automatisk.

    * Hvis du vil opprette tildelingen manuelt i rutene **Konserninterne dimensjoner** og **Nåværende selskapsdimensjoner**, velger du en dimensjon, og deretter velger du en dimensjon i feltene **Dimensjonskode** og **KI-dimensjonskode**.
    * Hvis du automatisk vil tildele dimensjoner som har samme kode, merker du linjene du vil tildele, velger du **Tildel dimensjoner med samme kode**-handlingen, og deretter velger du dimensjonene du vil oppdatere. 

    > [!TIP]
    > Hvis du vil tildele mange eller kanskje alle dimensjoner, velger du en linje, velger :::image type="icon" source="media/show-more-options-icon.png" border="false"::: og velger deretter **Velg flere**.

5. Velg handlingen **Dimensjonsverditildeling**.
6. På siden **Tildeling av konserninterne dimensjonsverdier** ligner fremgangsmåten for oppretting av tildelingen på det du nettopp gjorde for dimensjoner.

## Definer konserninterne finanskladdemaler og -bunker

Du må definere en finanskladdemal og en finanskladd som skal brukes som standard for konserninterne transaksjoner. Malen og bunken er spesielt viktig hvis du automatisk godtar konserninterne transaksjoner fra partnerne. Hvis du vil lære mer om automatisk godkjenning av transaksjoner, går du til [Automatisk godkjenning av transaksjoner fra konserninterne partnere](#auto-accept-transactions-from-intercompany-partners).   

* Finanskladder brukes til å bokføre til finanskonti og andre konti, for eksempel bank-, kunde-, leverandørkontoer. Bokføring med en finanskladd oppretter alltid poster på finanskonti.  Bruk siden **Konsernintern finanskladd** til å definere finanskladdebunken som skal brukes. Innstillingene som gjelder spesielt for konserninterne transaksjoner, er de kontoene du angir i feltene **KI-kontotype** og **KI-kontonr.**.
* Kladdemaler gir deg en kladdeside som er tilpasset et bestemt formål. Det vil si at feltene i kladdemalene er nøyaktig de som trengs i den delen av programmet. Bruk siden **Finanskladdemaler** til å definere en mal som skal brukes for konserninterne transaksjoner.

Hvis du vil vite mer om finanskladdemaler og bunker, går du til [Bruk kladdemaler og bunker](ui-work-general-journals.md#use-journal-templates-and-batches).

## Definer et selskap for konserninterne transaksjoner

De følgende trinnene forutsetter at en synkroniseringspartner defineres med kontoplanen og dimensjonene du vil basere den konserninterne kontoplanen og dimensjonene på. Du kan konfigurere dem selv, men det er vanligvis raskere å komme i gang, og vedlikehold er enklere, for å bruke en synkroniseringspartner. Lær mer om synkroniseringspartneren, gå til [Definer en synkroniseringspartner](#set-up-a-synchronization-partner).

> [!TIP]
> Det er lurt å fylle ut feltene på hurtigfanen **Generelt** på siden **Konserninternt oppsett** for hver partner før du legger til partnerne. Når du legger til partnerselskaper som er i samme leier, får [!INCLUDE [prod_short](includes/prod_short.md)] KI-koden og selskapsnavnet fra oppsettet i hurtigfanen Generelt. Feltet **Selskapsnavn** kontrollerer at KI-koden er unik.

> [!NOTE]
> Hvis du skal bruke en synkroniseringspartner, lar du feltet **Synkroniseringspartner** stå tomt når du setter opp dette selskapet for partnerskapet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninternt oppsett**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene på hurtigfanen **Generelt** på siden **Konserninternt oppsett**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> I [!INCLUDE[prod_short](includes/prod_short.md)] Online kan du ikke bruke filplasseringer til å overføre transaksjoner til partnerne fordi [!INCLUDE[prod_short](includes/prod_short.md)] ikke har tilgang til det lokale nettverket. Hvis du velger **Filplassering** i **Overføringstype**-feltet, er derfor ikke **Mappebane**-feltet tilgjengelig. Filen lastes i stedet ned til **Nedlastinger**-mappen på datamaskinen. Du sender deretter filen til noen i partnerselskapet, for eksempel via e-post. Vi anbefaler at du velger **E-post** for å bruke en mer direkte fremgangsmåte.

Det neste trinnet er å konfigurere partnerselskapene.

## Konfigurer konserninterne partnere

Hver partner må legge til alle andre selskaper i partnerskapet som partner.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninternt oppsett**, og velg deretter den relaterte koblingen.
2. Velg **Legg til** i hurtigfanen **Konserninterne partnere**.
3. På siden **Konsernintern partner** må du fylle ut feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gjenta trinn 2 og 3 for alle selskapene i partnerskapet.

> [!NOTE]
> Hvis du aktiverer **Godta transaksjoner automatisk** for den konserninterne bokføringen på siden **Konsernintern partner** undertrykker [!INCLUDE[prod_short](includes/prod_short.md)] meldinger som varsler om kjøpsfakturaer som kopiere den opprinnelige bestillingen. Det er viktig å ha en forretningsprosess for å behandle duplikater. Ved å slette slike bestillinger når for eksempel kjøpsfakturaen mottas fra den konserninterne partneren.

### Definer konserninterne partnere som leverandører og kunder

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninternt oppsett**, og velg deretter den relaterte koblingen.
2. Åpne kortsiden for partneren på hurtigfanen **Konserninterne partnere**.
3. Avhengig av hva du vil gjøre, velger du kunden eller partneren i **Kundenr.**- eller **Leverandørnr.**-feltene.

    > [!NOTE]
    > Hvis kunden eller leverandøren ikke er opprettet, kan du velge **+Opprett** i rullegardinmenyen for å konfigurere dem. Hvis du vil vite mer om hvordan du oppretter kunder og leverandører, går du til [Registrer nye kunder](sales-how-register-new-customers.md) og [Registrer nye leverandører](purchasing-how-register-new-vendors.md).

    > [!TIP]
    > Du kan også angi en kunde eller leverandør som konsernintern partnern ved å fylle ut feltet **KI-partnerkode** på sidene **Kundekort** og **Leverandørkort**.

### Sett opp standard finanskontoer for konsernintern partner  

Når du oppretter en konsernintern salgs- eller kjøpslinje som skal sendes som en utgående transaksjon, angir du en konto fra den konserninterne kontoplanen som standard for hvilken konto i partnerens selskap som beløpet skal bokføres på. På **Finanskontokort**-siden kan du angi en standard finanskonto for konsernintern partner for konti du bruker ofte i utgående konserninterne salgslinjer eller kjøpslinjer. For samlekontoen for kunder kan du for eksempel angi tilsvarende samlekonto for leverandører fra den konserninterne kontoplanen. Kontoene for kortsiktige fordringer og kjøp brukes som motkonto for den konserninterne partneren når du bokfører transaksjoner i konserninterne finanskladder.  

Når du nå angir en finanskonto i feltet **Motkontonr.** i en konsernintern linje med **Konsernintern partner** i feltet **Kontotype**, blir feltet **Finanskonto for KI-partner** automatisk fylt ut.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.  
2. Åpne finanskontoen som brukes for konserninterne transaksjoner og i feltet **Standard finanskonto for KI-Partner** angir du den konserninterne finanskontoen partneren skal bokføre til når du bokfører i finanskontoen på linjen.
3. Gjenta trinn 2 for hver konto du ofte angir, i feltet **Motkontonr.** på en linje i en konsernintern kladd eller et konserninternt dokument.

### Godta transaksjoner automatisk fra konserninterne partnere

For å gjøre det raskere å behandle konserninterne transaksjoner kan du angi at du vil opprette kladdelinjer automatisk på en konsernintern partners oppføringer fra siden **KI-finanskladd**. Hvis du vil opprette inngående og utgående transaksjoner automatisk, må du aktivere følgende vekselbryter for hver partner:

* På siden **Konserninternt oppsett** slår du på **Send transaksjoner automatisk**-vekslebryteren for synkroniseringspartneren. Deretter angir du hvor du vil opprette mottatte konserninterne kladdetransaksjoner ved å fylle ut feltene **Standard KI-finanskladdemal** og **Standard KI-finanskladd**.

    > [!TIP]
    > Hvis feltet **Standard finanskladdemal** er tomt, må du definere en finanskladdemal som skal brukes for de konserninterne finanskladdene. Hvis du vil vite mer om maler og bunker, går du til [Definer konserninterne finanskladdemaler og bunker](#set-up-intercompany-general-journal-templates-and-batches)    

* På siden **Konsernintern partner** slår du på **Godta transaksjoner automatisk**-vekslebryteren.

Kladdelinjene opprettes for deg, men bokføres ikke.

> [!NOTE]
> Hvis organisasjonen brukte konserninterne funksjoner i [!INCLUDE [prod_short](includes/prod_short.md)] før lanseringsbølge 1 i 2022 til å godta transaksjoner automatisk, må administratoren aktivere funksjonen **Godta automatisk konserninterne finanskladdtransaksjoner** på siden **Funksjonsstyring**.

### Angi hvilke bankkontoer som skal brukes for konserninterne partnere

For å forenkle raske betalinger må du angi en eller flere bankkontoer som skal brukes for konserninterne partnere. Når en partner bruker en konsernintern finanskladd til å foreta en betaling, kan de angi bankkontoen på linjen. Bankkontoen brukes som motkonto i mottaksselskapet, noe som reduserer behovet for å registrere transaksjoner manuelt.

* Du angir bankkontoen som skal brukes ved å velge **Bankkonto**-handlingen på siden **Konserninterne partnere**. Skriv inn kontoopplysningene på **Konserninternt bankkontokort**.

## Feilsøk det konserninterne oppsettet

På siden **Konserninternt oppsett** inneholder ruten **Diagnostikk for konserninternt oppsett** fliser som angir om du har satt opp alle komponentene som trengs for å utveksle konserninterne transaksjoner. Flisene er også tilgjengelige i rollesenteret for forretningsleder. Velg flisene for å finne ut hva som mangler. Hvis du vil ha en oversikt over de nødvendige komponentene, går du til [Oversikt over trinnene for å komme i gang](#overview-of-the-steps-to-get-started).

## Se også

[Behandle konserninterne transaksjoner](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
