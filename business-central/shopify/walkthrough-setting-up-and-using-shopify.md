---
title: Konfigurer og bruk Shopify-koblingen
description: Ulike integreringsscenarioer for å vise arbeidsflyt mellom Shopify og Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector"></a>Gjennomgang: Konfigurer og bruk Shopify-koblingen

Denne delen viser noen vanlige scenarioer og leder deg gjennom fremgangsmåten for å teste eller lære opp brukere i arbeidsflyten for den integrerte [!INCLUDE[prod_short](../includes/prod_short.md)] og Shopify-butikken.

## <a name="prerequisites"></a>Forutsetninger

### <a name="shopify"></a>Shopify

Du må ha:

- En Shopify-konto
- En Shopify-nettbutikk

Finn ut mer om hvordan du oppretter Shopify-prøveversjoner og anbefalte innstillinger under [Opprett og konfigurer Shopify-konto](shopify-account.md).

### <a name="business-central"></a>Business Central

Du må ha en [!INCLUDE[prod_short](../includes/prod_short.md)]-konto. 

Du kan for eksempel opprette en demokonto eller starte en prøveversjon. Finn ut mer under [Klargjør demonstrasjonsmiljøer av Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) og [Registrer deg for prøveversjonen](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop"></a>Koble Business Central til Shopify-butikken

I [!INCLUDE[prod_short](../includes/prod_short.md)] gjør du følgende:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg handlingen **Opprett**.
3. Skriv inn `DEMO1` i **Kode**-feltet.
4. I feltet **Shopify-nettadresse** angir du nettadressen for nettbutikken du vil koble deg til.
5. Aktiver vekslebryteren **Aktivert** og se gjennom og godta vilkårene.

Følg denne fremgangsmåten for å konfigurere Shopify-butikken:

1. Deaktiver vekslebryteren **Tillat bakgrunnssynkroniseringer**.
2. Velg *Til Shopify* velger du **Synkroniser vare**-feltet.
3. Velg *Til Shopify* velger du **Synkroniser varebilder**-feltet.
4. Slå på vekslebryteren **Synkroniser vareattributter**.
5. Slå på vekslebryteren **Lager sporet**.
6. Velg *Avslå* i feltet **Standard lagerpolicy**.
7. Slå på vekslebryteren **Opprett ukjente kunder automatisk**.
8. Fyll ut feltet **Kunde-/selskapsmalkode** med riktig mal.
9. Fyll ut **fraktkostnadskontoen**, **tipskontoen** med inntektskontoen. Bruk for eksempel `40210` i USA.
10. Slå på vekslebryteren **Opprett ordrer automatisk**.
11. Deaktiver veksleknappen **Frigi ordrer automatisk**.

Konfigurer lokasjonstildeling:

1. Velg handlingen **Lokasjoner** for å åpne **Shopify-butikklokasjoner**.
2. Velg handlingen **Hent Shopify-lokasjoner** hvis du vil importere alle lokasjonene som er definert i Shopify. Velg oppføring med veksleknappen **Er primær** valgt.
3. Angi `''|EAST|MAIN` i **lokasjonsfilteret**.
4. Velg *Beregnet disponibel saldo i dag* i feltet **Lagerberegning** for å aktivere en lagersynkronisering for en valgt Shopify-lokasjon.

## <a name="walkthrough-start-selling-products-online"></a>Gjennomgang: Begynn å selge produkter på nettet

### <a name="scenario"></a>Scenario

La oss si at du vil prøve Shopify som en nettbutikk uten å bruke tid på å konfigurere, spesielt fordi du allerede opprettholder varene i [!INCLUDE[prod_short](../includes/prod_short.md)] på riktig måte. Når du har startet Shopify-nettbutikken, får du umiddelbart nye kunder som er fornøyde med butikken din og kjøpsopplevelsen. De ønsker derfor å legge igjen tips ved betaling.

### <a name="steps"></a>Trinn

Følg denne fremgangsmåten i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-produkter**. Velg den relaterte koblingen.
2. Velg **Legg til varer**.
3. Skriv inn `DEMO1` i **Butikkode**-feltet.
4. Sett filteret `CHAIR` på feltet **Varekategorikode**.
5. Slå på vekslebryteren **Synkroniser produktbilder**.
6. Slå på vekslebryteren **Synkroniser lager**.
7. Velg **OK** og vent til den første synkroniseringen av varer, priser, bilder og lager er fullført.

I **Shopify-nettbutikken**:
> [!Tip]  
> Åpne **Shopify -administrator** ved å navigere til nettadressen som er angitt i **Nettadresse**-feltet på siden for **Shopify-butikkort**. Velg øyeikonet ved siden av **Nettbutikk**-salgskanalen, som du finner på sidepanelet for **Shopify -administrator**. 

Åpne produktkatalogen. Merknad:

* Produkttitler, bilder og priser.
* Tilgjengelighetsindikator (utsolgt for produkter ikke på lager).

Velg et hvilket som helst produkt som kan selges, for eksempel `BERLIN Swivel Chair, yellow`. Legg merke til at beskrivelsen inneholder vareattributter.

Velg **Kjøp nå** og fortsett til betaling.

1. I feltet **E-postadresse eller mobiltelefonnummer** angir du `cl@contoso.com` (eller e-postadressen der du vil motta ordre- og forsendelsesbekreftelser).
2. Skriv inn `Claudia Lawson` i feltene **Fornavn** og **Etternavn**.
3. Angi den lokale adressen.
4. Merk av for **Lagre denne informasjonen til neste gang**.
6. Behold *Standard* som leveringsmetode.
8. I **Kredittkortnummer**-feltet angir du `1` hvis du bruker *(for testing) falsk gateway*, eller angir `5555 5555 5555 4444` hvis du bruker *Shopify Payments* i testmodus.
9. Fyll ut **Navn på kort**-feltet.
10. I **Utløpsdato**-feltet angir du inneværende måned/år.
11. Skriv inn `111` i **Sikkerhetskode**-feltet.
7. Valgfritt: Velg `10%` tips.
8. 12. Velg **Betal nå**.

Gjør følgende trinn i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Shopify-ordrer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Synkroniser ordrer fra Shopify**.
3. Velg **OK**.

Den importerte ordren er klar til behandling.

1. Velg den importerte ordren for å åpne vinduet **Shopify-ordre**.
2. Legg merke til at den nye kunden og ordrene er opprettet.
3. Utforsk handlingene **Risiko** og **Leveringskostnader**.
4. Velg **Ordre** for å åpne vinduet **Ordre**. Ordre er en etterspørsel som om nødvendig kan dekkes av montering, produksjon eller ved kjøp ved hjelp av planleggingsmotoren. Den støtter også forskjellige lagerhåndteringsprosesser med fullstendig separasjon av oppgaver.
6. I feltet **Agent** angir du `DHL`. Åpne ordren på nytt om nødvendig ved å velge handlingen **Åpne på nytt**.
7. I feltet **Pakkesporingsnr.** angir du `123456789`.
8. Velg **Bokfør**, behold **Lever og fakturer**-alternativet, og velg deretter **OK**.

Nå er fysiske og økonomiske data registrert i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det er på tide å varsle Shopify om endringene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Synkroniser leveringer til Shopify**, og velg deretter den relaterte koblingen.
2. Velg **OK**.

I **Shopify-administrator** legger du merke til at ordren nå er merket som *Oppfylt*. Du kan også se gjennom leveringsinformasjon og se sporingsnettadressen. Hvis du kjører **Synkroniser ordrer fra Shopify** på nytt, arkiveres ordren i begge systemene.

## <a name="walkthrough-add-your-customers-to-your-new-online-store"></a>Gjennomgang: Legg til kunder i den nye nettbutikken

### <a name="scenario-1"></a>Scenario

Etter en vellykket hurtigstart av den nye nettbutikken, vil du at de nå værende kundene skal besøke den og begynne å legge inn bestillinger. Avhengig av Shopify-planen og -prosessen kan du prøve B2B- og DTC-flyter.

### <a name="dtc-steps"></a>DTC-trinn

I [!INCLUDE[prod_short](../includes/prod_short.md)] gjør du følgende:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-kunder** og velger den relaterte koblingen.
2. Velg **Legg til kunder**.
3. Skriv inn `DEMO1` i **Butikkode**-feltet.
4. Angi filteret `20000` til **Nr.** .
5. Velg **OK** og vent til den første synkroniseringen av kunder er fullført.

I **Shopify-administrator** legger du merket til at kunden ble importert. Åpne kundene, og legg merke til at for- og etternavnene til kunden kommer fra **Kontaktnavn**-feltet på **kundekortet**. Firmanavnet finnes i standardadressen, koblet til kunden. Hvis du bruker *klassiske kundekontoer*, kan du velge **Send kontoinvitasjon** for å invitere kunden. Med *nye kundekontoer* er det ikke nødvendig med et passord for at kundene skal logge seg på, i stedet lar Shopify kundene dine logge seg på ved hjelp av en engangs sekssifret bekreftelseskode sendt via e-post. 

### <a name="b2b-steps"></a>B2B-trinn

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

I [!INCLUDE[prod_short](../includes/prod_short.md)] gjør du følgende:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-selskaper** og velger den relaterte koblingen.
2. Velg **Legg til selskap**.
3. Skriv inn `DEMO1` i **Butikkode**-feltet.
4. Angi filteret `30000` til **Nr.** .
5. Velg **OK** og vent til den første synkroniseringen av kunder er fullført.

Legg merke til at både selskapet og kunden ble importert i **Shopify-administrator**. Åpne kundene, og legg merke til faktaboksen Selskap med kobling til Selskap, lokasjon og tildelte tillatelser. Velg **[...]** i faktaboksen **Selskap**, og velg deretter **Send e-post med B2B-tilgang** for å invitere kunden.

## <a name="walkthrough-fine-tuning-of-item-management"></a>Gjennomgang: Finjustering av varestyring

### <a name="scenario-2"></a>Scenario

Du vil legge til mer fleksibelt og kontroll i prosessene rundt varestyring. Du ønsker å forbedre produktbeskrivelsene og vil legge til flere gjennomgangstrinn før produkter blir tilgjengelig for alle kundene.

### <a name="steps-1"></a>Trinn

I [!INCLUDE[prod_short](../includes/prod_short.md)] gjør du følgende:

Klargjør data.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kundeprisgruppe**, og velg den relaterte koblingen.
2. Legg til en ny prisgruppe. Skriv inn `SHOPIFY` i **Kode**-feltet.
3. Lukk vinduet **Kundeprisgruppe**.
4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
5. Velg vare *1896-S, Athens Desk* og følg denne fremgangsmåten:

6. Velg handlingen **Varianter**, og legg deretter til to varianter: `PREMIUM, Athens Desk, Premium edition` og `ESSENTIAL, Athens Desk, Essential edition`.
7. Velg handlingen **Markedsføringstekst**, og bruk **Lag utkast med Copilot** til å få kreativ og engasjerende tekst. Hvis forslag til markedsføringstekst ikke er aktivert, skriver du bare: **Enkel, stilig utforming** passer sammen med et hvilket som helst ensemble. *Tilgjengelig i to utgaver.*'. 
8. Velg handlingen **Salgspriser**, og legg til nye priser som vist i følgende tabell:

   |Linje|Salgstype|Salgskode|Type| - kode|Variantkode<br>(legg til feltet via tilpasning)|Enhetspris|
   |------|------------|------------|------------|----------------|------------|------------|
   |1|Kundeprisgruppe|SHOPIFY|Element|1896-S|ESSENTIAL|700|
   |2|Kundeprisgruppe|SHOPIFY|Element|1896-S|PREMIUM|1 000|

9. Velg handlingen **Salgsrabatter** og legg til en ny rabatt:

   * **Salgstype** *Kunderabattgruppe*
   * **Salgskode** *DETALJHANDEL*
   * **Type** *Vare*
   * **Kode** *1896-S*
   * **Enhetskode** *STK*
   * **Linjerabatt-%** *10*

10. Velg handlingen **Varereferanser** og følgende tilleggslinjer:

   |Linje|Referansetype|Referansenr.|Variantkode|
   |------|------------|------------|------------|
   |1|Strekkode|77777777|ESSENTIAL|
   |2|Strekkode|11111111|PREMIUM|

11. Velg varen *1920-S, ANTWERP Conference Table* og følg denne fremgangsmåten:
12. Velg **Juster lager** og skriv inn `100` for lokasjonene **ØST** og *VEST* i feltet *Ny beholdning*. 
13. Velg **OK**.

Juster synkroniseringsinnstillingene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikker**. Velg den relaterte koblingen.
2. Velg `DEMO1`-butikken du vil synkronisere varer med for å åpne siden **Shopify-butikkort**.
3. Aktiver feltet **Synkroniser markedsføringstekst**.
4. Velg *varenr. + variantkode* i feltet **Tildeling for lagerføringsenhet**.
5. Velg *Fortsett* i feltet **Standard lagerpolicy**.
6. Velg *Utkast* i feltet **Status for opprettede produkter**.
7. Velg *Status som skal arkiveres* i feltet **Handling for fjernet produkt**.
8. Velg *SHOPIFY* i feltet **Kundeprisgruppe**.
9. Velg *DETALJHANDEL* i feltet **Kunderabattgruppe**.
 
Kjør synkroniseringen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikker**. Velg den relaterte koblingen.
2. Velg `DEMO1`-butikken du vil synkronisere varer med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Produkter** for å åpne vinduet **Shopify-produkter**.
4. Velg handlingen **Legg til varer**.
5. Sett filteret *TABLE|DESK* på feltet **Varekategorikode**.
6. Slå på vekslebryteren **Synkroniser produktbilder**.
7. Slå på vekslebryteren **Synkroniser lager**.
8. Velg **OK** og vent til den første synkroniseringen av varer, priser, bilder og lager er fullført.

Produkter legges til. Legg merke til at statusen er satt til *Utkast*, og derfor er ikke varene synlige i Shopify-nettbutikken.

1. Velg linjen med varen *1920-S, ANTWERP Conference Table*. Angi `Rectangular meeting table Antwerp, 10 seats, black` i **SEO-tittelen**.
2. Velg *Aktiv* i feltet **Status**.
3. Velg linjen med varen *1906-S, ATHENS, Mobile Pedestal*, og velg deretter **Slett**.

I **Shopify-administrator** legger du merke til at alle produkter har forskjellige statuser.

* *ANTWERP Conference Table* er *Aktiv* fordi vi endret statusen i vinduet **Shopify-produkt**.
* *ATHENS Desk* er *Utkast* fordi vi konfigurerte standardstatusen for alle tillagte produkter som *Utkast*.
* *ATHENS Mobile Pedestal* *arkiveres* fordi vi har konfigurert butikken slik at den automatisk tildeler statusen *Arkivert* for slettede produkter.

Legg merke til at lageret for ANTWERP Conference Table er 100, fordi vi konfigurerte systemet til å bruke lager bare fra to lokasjoner HOVED og ØST. Lageret på annen lokasjon (VEST) ignoreres.

* Åpne *ANTWERP Conference Table*, legg merke til feltene **Egendefinert type**, **Leverandør**, **Vekt**, **Kostnad per vare** og delen **Forhåndsvisning av søkemotor**.
* Åpne *Athens Desk*, rull nedover til **Varianter**-delen, og legg merke til hvordan **Lagerføringsenhet** er fylt ut.
* Velg **Rediger** for å gå gjennom strekkode og priser.
* Endre status for *Athens Desk* til *Aktiv*, og velg **Forhåndsvis**.

I **Shopify-nettbutikken** åpner du produktkatalogen og finner produktet *Athens Desk*. Legg merke til at andre alternativer er tilgjengelige. For ulike alternativer er prisene forskjellige. Vær oppmerksom på rabattinformasjon.

### <a name="additional-steps-for-b2b"></a>Ytterligere trinn for B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Du kan konfigurere koblingen for å opprette og tildele katalog for eksporterte selskaper automatisk. Trinnene nedenfor er nyttige hvis du vil ha mer nøyaktig kontroll over hva som er tilgjengelig for B2B-kunder.

I **Shopify-administrator**cOpprett og tildelt katalog.

1. Velg **Produkter** og deretter **Kataloger** i sidefeltet **Shopify-administrator**.
2. Opprett katalog for bestemte produkter. Gi den navnet B2B. 
3. Velg **Administrer** og deretter **Administrer produkter og priser**.
4. Velg *Ekskludert*-filter, finn *ATHERN Desk* og velg **Inkluder i katalog**.
5. Velg **Kunder** og deretter **Selskaper** i sidefeltet **Shopify-administrator**.
6. Velg *School of Fine Art*, velg **[...]** og deretter **Legg til kataloger** og legg til *B2B*-katalogen opprettet tidligere.

I [!INCLUDE[prod_short](../includes/prod_short.md)] gjør du følgende:

Klargjør data.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.

2. Velg vare **1896-S, Athens Desk** og følg denne fremgangsmåten:

3. Velg handlingen **Salgsrabatter** og legg til en ny rabatt:

   * **Salgstype** *Kunderabattgruppe*
   * **Salgskode** *STOR AKK*
   * **Type** *Vare*
   * **Kode** *1896-S*
   * **Enhetskode** *STK*
   * **Linjerabatt-%** *25*

4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-kataloger**. Velg den relaterte koblingen.
5. Velg **Hent kataloger**.
6. Skriv inn `DEMO1` i **Butikkode**-feltet.
7. Velg oppføring med navnet *B2B*-katalog du vil synkronisere priser for.
8. Aktiver veksleknappen **Synkroniser priser**.
9. Velg *SHOPIFY* i feltet **Kundeprisgruppe**.
10. Velg *STOR AKK* i feltet **Kunderabattgruppe**.
11. Velg **Synkroniser priser** og vent til synkroniseringen av priser er fullført.

I **Shopify-administrator** utforsker du prisene for *B2B*-katalogen.

I **Shopify-nettbutikken** åpner du produktkatalogen og finner produktet *Athens Desk*. Merk at priser er rabattinformasjon.

## <a name="walkthrough-check-out-and-order-synchronization-for-individual-buyer-and-company-representative"></a>Gjennomgang: Betaling og ordresynkronisering for individuell kjøper og selskapsrepresentant
Dette er en fortsettelse av [Gjennomgang: Begynn å selge produkter på nettet](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Du kan også prøve med dine egne data, for eksempel Shopify-butikken eller -sandkassen.

Individuell kjøper

1. I **Shopify-nettbutikken**. Velg **Konto**-ikon. Angi e-posten du har tilgang til.
2. Logg på med en engangs sekssifret bekreftelseskode sendt via e-post du skrev inn.
3. Utforsk produktkatalogen, du skal kunne se alle produkter med utsalgspriser.
4. Velg Essential-variant og velg **Kjøp den nå** og fortsett til kassen.
5. Fyll ut feltene **Fornavn** og **Etternavn**.
6. Angi den lokale adressen.
7. Behold *Standard* som leveringsmetode.
8. I **Kredittkortnummer**-feltet angir du `1` hvis du bruker *(for testing) falsk gateway*, eller angir `5555 5555 5555 4444` hvis du bruker *Shopify Payments* i testmodus.
9. I **Utløpsdato**-feltet angir du inneværende måned/år.
10. Skriv inn `111` i **Sikkerhetskode**-feltet.
11. Fyll ut **Navn på kort**-feltet.
12. Velg **Betal nå**.
 
Selskapsrepresentant

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. I **Shopify-administrator**.
2. Velg **Kunder** og deretter **Selskaper** i sidefeltet **Shopify-administrator**.
3. Åpne posten *School of Fine Art*.
4. Velg **[...]** i faksboksen **School of Fine Art** og deretter **Rediger betalingsbetingelser** og velg *Forfall ved oppfyllelse*.
5. Velg **[...]** i faktaboksen **Kunder** og deretter **Legg til kunde** og legg til en med e-postadresse du brukte til å logge deg på butikken tidligere.
6. I **Shopify-nettbutikken**. Velg **Konto**-ikon. Angi e-posten du har tilgang til.
7. Logg på med en engangs sekssifret bekreftelseskode sendt via e-post du skrev inn.
8. Utforsk produktkatalogen, du skal bare kunne se produkt som er lagt til i *B2B*-katalogen med spesialpriser.
9. Velg Essential-variant og velg **Kjøp den nå** og fortsett til kassen.
10. Legg merke til at kontoen, Send til, betalingsmåten er fylt ut.
11. Fyll ut **Bestillingsnummer**-feltet med `PO-12345`.
12. Velg **Send bestilling**.
 
Gjør følgende trinn i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Shopify-ordrer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Synkroniser ordrer fra Shopify**.
3. Velg **OK**.

Den importerte ordren er klar til behandling.

1. Velg den importerte ordren for å åpne vinduet **Shopify-ordre**.
2. Legg merke til at selv om begge bestillingene ble sendt inn av samme person, er de knyttet til to forskjellige kunder. 
3. I ordren som sendes på vegne av selskapet, vises verdien i feltet **Bestillingsnummer**, som også overføres til **Eksternt dokumentnr**-feltet i det opprettede salgsdokumentet.
4. Fordi vi konfigurerte B2B-selskap til å håndtere betalinger utenfor Shopify er **Finansstatus** satt til *Venter*. Når du har mottatt betaling, velger du handlingen **Merk som betalt**. Finansstatus blir oppdatert i Shopify. 

## <a name="walkthrough-import-items-customers-companies-from-shopify"></a>Gjennomgang: Importer varer, kunder, selskaper fra Shopify

### <a name="scenario-3"></a>Scenario

Du har allerede en vellykket nettbutikk og ønsker å begynne å bruke [!INCLUDE[prod_short](../includes/prod_short.md)] som programvare for forretningsstyring. Du ønsker å importere så mye data fra Shopify som mulig. 

### <a name="steps-2"></a>Trinn

Dette er en fortsettelse av [Gjennomgang: Begynn å selge produkter på nettet](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) og [Gjennomgang: Legg til kundene i den nye nettbutikken](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). Du kan også prøve med dine egne data, for eksempel Shopify-butikken eller -sandkassen.

Følg fremgangsmåten nedenfor i [!INCLUDE[prod_short](../includes/prod_short.md)].

#### <a name="prepare-data"></a>Klargjør data

1. Bytt til en 30-dagers prøveversjon uten eksempeldata. Hvis du vil ha mer informasjon, kan du se [Legg til dine egne data i en tom prøveversjon](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
3. Velg **Ny**.
4. Skriv inn `DEMO2` i **Kode**-feltet.
5. I feltet **Shopify-nettadresse** angir du nettadressen til nettbutikken du vil koble deg til.
6. Aktiver vekslebryteren **Aktivert** og se gjennom og godta vilkårene.

Konfigurer Shopify-butikken som beskrevet her:

1. Deaktiver vekslebryteren **Tillat bakgrunnssynkroniseringer**.
2. Velg *Fra Shopify* velger du **Synkroniser vare**-feltet.
3. Aktiver vekslebryteren **Opprett ukjente varer automatisk**.
4. Fyll ut feltet **Varemalkode** med riktig mal.
5. Velg *Fra Shopify* velger du **Synkroniser varebilder**-feltet.
6. Velg *varenr. + variantkode* i feltet **Tildeling for lagerføringsenhet**.
7. Velg *Alle kunder* i **Kundeimport fra Shopify**.
8. Aktiver vekslebryteren **Opprett ukjent kunde automatisk**.
9. Fyll ut feltet **Kunde-/selskapsmalkode** med riktig mal.
10. Velg *Alle kunder* i **Selskapsimport fra Shopify**.
11. Aktiver vekslebryteren **Opprett ukjent selskap automatisk**.

#### <a name="run-the-synchronization"></a>Kjør synkroniseringen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikker**. Velg den relaterte koblingen.
2. Velg *DEMO2*-butikken du vil synkronisere data med for å åpne siden **Shopify-butikkort**.
3. Velg **Synkroniser produkter**.
4. Velg **Synkroniser produktbilder**.
5. Velg **Synkroniser kunder**.
6. Velg **Synkroniser selskaper**

### <a name="results"></a>Resultater

* Shopify-produkter importeres. For å bekrefte velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-produkter**. Velg den relaterte koblingen.
* Varer med bilder opprettes. For å bekrefte velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Vare** og velger den relaterte koblingen.
* Shopify-kunder importeres. For å bekrefte velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-kunder** og velger den relaterte koblingen.
* Shopify-selskaper importeres. For å bekrefte velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-selskaper** og velger den relaterte koblingen.
* Kunder opprettes. For å bekrefte velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.


## <a name="see-also"></a>Se også

[Kom i gang med Shopify-koblingen](get-started.md)  
