---
title: Konfigurer og bruk Shopify-koblingen
description: Ulike integreringsscenarioer for å vise arbeidsflyt mellom Shopify og Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 713a5bd748c76fa6bc7917460a0c47d7cbaf2f77
ms.sourcegitcommit: bb6ecb20cbd82fdb5235e3cb426fc73c29c0a7ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803045"
---
# <a name="walkthrough-set-up-and-use-the-shopify-connector"></a>Gjennomgang: Konfigurer og bruk Shopify-koblingen

Denne delen viser noen vanlige scenarioer og leder deg gjennom fremgangsmåten for å teste eller lære opp brukere i arbeidsflyten for den integrerte [!INCLUDE[prod_short](../includes/prod_short.md)] og Shopify-butikken.

## <a name="prerequisites"></a>Forutsetninger 

### <a name="shopify"></a>Shopify

Du må ha:

- En Shopify-konto
- En Shopify-nettbutikk

Finn ut mer om hvordan du oppretter Shopify-prøveversjoner og anbefalte innstillinger under [Oppretting og konfigurering av Shopify-konto](shopify-account.md).

### <a name="business-central"></a>Business Central

Du må ha en [!INCLUDE[prod_short](../includes/prod_short.md)]-konto. 

Du kan for eksempel opprette en demokonto eller starte en prøveversjon. Finn ut mer under [Klargjøring av [!INCLUDE[prod_short](../includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/administration/demo-environment.md) og [Registrer deg for prøveversjonen](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop"></a>Koble Business Central til Shopify-butikken

Gjør følgende trinn i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikk** og velger den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Skriv inn `DEMO1` i **Kode**-feltet.
4. I feltet **Shopify-nettadresse** angir du nettadressen til nettbutikken du vil koble deg til.
5. Aktiver vekslebryteren **Aktivert**, se gjennom og godta vilkårene.

Konfigurer Shopify-butikken slik det er beskrevet i fremgangsmåten nedenfor:

1. Slå på vekslebryteren **Logg aktivert**.
2. Slå av vekslebryteren **Tillat bakgrunnssynkroniseringer**.
3. Velg **Til Shopify** velger du **Synkroniser vare**-feltet.
4. Velg **Til Shopify** velger du **Synkroniser varebilder**-feltet.
5. Slå på vekslebryteren **Synkroniser vareattributter**.
6. Slå på vekslebryteren **Lager sporet**.
7. Velg **Avslå** i feltet **Standard lagerpolicy**.
8. Slå på vekslebryteren **Opprett ukjente kunder automatisk**.
9. Fyll ut feltet **Kundemalkode** med riktig mal.
10. Fyll ut **fraktkostnadskontoen**, **tipskontoen** med inntektskontoen. Bruk for eksempel `40100` i USA.
11. Slå på vekslebryteren **Opprett ordrer automatisk**.

Konfigurer lokasjonstildeling:

1. Velg handlingen **Lokasjoner** for å åpne **Shopify-butikklokasjoner**.
2. Velg handlingen **Hent Shopify-lokasjoner** hvis du vil importere alle lokasjonene som er definert i Shopify.
3. Angi `''|EAST|MAIN` i **lokasjonsfilteret**.
4. Slå av vekslebryteren **Deaktivert** for å aktivere lagersynkronisering for valgt Shopify-lokasjon.

## <a name="walkthrough-start-selling-products-online"></a>Gjennomgang: Begynn å selge produkter på nettet

### <a name="scenario"></a>Scenario

La oss si at du vil prøve Shopify som en nettbutikk uten å bruke tid på å konfigurere ting, spesielt fordi du allerede opprettholder varene i [!INCLUDE[prod_short](../includes/prod_short.md)] på riktig måte. Når du har startet Shopify-nettbutikken, får du umiddelbart nye kunder som er fornøyde med butikken din og kjøpsopplevelsen. De ønsker derfor å legge igjen tips ved betaling.

### <a name="steps"></a>Trinn

Gå gjennom følgende trinn i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-produkter**. Velg den relaterte koblingen.
2. Velg handlingen **Legg til varer**.
3. Skriv inn *DEMO1* i **Butikkode**-feltet.
4. Angi filter `CHAIR` i feltet **Varekategorikode** (legg til Filter-feltet hvis nødvendig).
5. Velg **OK** og vent til den første synkroniseringen av varer og priser er fullført.
6. Velg handlingen **Synkroniser produktbilder**.
7. Velg handlingen **Synkroniser lager**.

Åpne produktkatalogen i **Shopify-nettbutikken**. Merknad:

* Produkttitler, bilder og priser.
* Tilgjengelighetsindikator (utsolgt for produkter ikke på lager).

Velg et hvilket som helst produkt som kan selges, for eksempel `BERLIN Swivel Chair, yellow`. Legg merke til at beskrivelsen inneholder vareattributter.

Velg knappen **Kjøp nå**, og fortsett betaling.

1. I feltet **E-postadresse eller mobiltelefonnummer** angir du `cl@contoso.com` (eller e-postadressen der du vil motta ordre- og forsendelsesbekreftelser).
2. Skriv inn `Claudia Lawson` i **Fornavn** og **Etternavn**.
3. Angi den lokale adressen.
4. Merk av for **Lagre denne informasjonen til neste gang**.
5. Velg **Fortsett til levering**-knappen.
6. Behold `Standard` som leveringsmåte, og deretter velger du **Fortsett til betaling**-knappen.
7. Velg `10%` tips.
8. I **Kredittkort**-feltet angir du `1` hvis du bruker *(for testing) falsk gateway*, hvis du bruker *Shopify Payments* i testmodus, angir du `5555 5555 5555 4444` i **Kredittkort**-feltet.
9. Fyll ut **Navn på kort**-feltet.
10. I **Utløpsdato**-feltet angir du inneværende måned/år.
11. Skriv inn `111` i **Sikkerhetskode**-feltet.
12. Velg **Betal nå**-knappen.

Gjør følgende trinn i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Shopify-ordrer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Synkroniser ordrer fra Shopify**.
3. Velg **OK**.

Den importerte ordren er klar til behandling.

1. Velg den importerte ordren for å åpne vinduet **Shopify-ordre**.
2. Legg merke til at den nye kunden og ordren er opprettet.
3. Utforsk handlingene **Risiko** og **Leveringskostnader**.
4. Velg **Ordre**-handlingen for å åpen **Ordre**-vinduet. Ordre er en etterspørsel som om nødvendig kan dekkes av montering, produksjon eller ved kjøp ved hjelp av planleggingsmotoren. Den støtter også forskjellige lagerhåndteringsprosesser med fullstendig separasjon av oppgaver.
5. Velg handlingen **Åpne på nytt**.
6. I feltet **Agent** angir du `DHL`.
7. I feltet **Pakkesporingsnr.** angir du `123456789`.
8. Velg **Bokfør**-handlingen, behold **Lever og fakturer**-alternativet, og velg deretter **OK**-knappen.

Nå er fysiske og økonomiske data registrert i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det er på tide å varsle Shopify om endringene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Synkroniser leveringer til Shopify**, og velg deretter den relaterte koblingen.
2. Velg **OK**.

I **Shopify-administrator** legger du merke til at ordren nå er merket som *Oppfylt*. Du kan også se gjennom leveringsinformasjon og se sporingsnettadressen. Hvis du kjører **Synkroniser ordrer fra Shopify** på nytt, arkiveres ordren i begge systemene.

## <a name="walkthrough-invite-your-customers-to-your-new-online-store"></a>Gjennomgang: Inviter kunder til den nye nettbutikken

### <a name="scenario"></a>Scenario

Etter en vellykket hurtigstart av den nye nettbutikken, vil du at de nå værende kundene skal besøke den og begynne å legge inn bestillinger.

### <a name="steps"></a>Trinn

Gjør følgende trinn i [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg **DEMO1**-butikken du vil synkronisere kunder med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Synkroniser kunder**.

I **Shopify-administrator** legger du merket til at kundene ble importert. Åpne en av kundene, og legg merke til at for- og etternavnene til kunden kommer fra **Kontaktnavn**-feltet på **kundekortet**. Firmanavnet finnes i standardadressen, koblet til kunden. Velg **Send kontoinvitasjon** for å invitere kunden.

## <a name="walkthrough-fine-tuning-of-item-management"></a>Gjennomgang: Finjustering av varestyring

### <a name="scenario"></a>Scenario 

Du vil legge til mer fleksibelt og kontroll i prosessene rundt varestyring. Du ønsker å forbedre produktbeskrivelsen og vil legge til flere gjennomgangstrinn før produkter blir tilgjengelig for sluttkunden.

### <a name="steps"></a>Trinn

Gjør følgende trinn i [!INCLUDE[prod_short](../includes/prod_short.md)]:

Klargjør data.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kundeprisgruppe**, og velg den relaterte koblingen.
2. Legg til ny prisgruppe. Skriv inn `SHOPIFY` i **Kode**-feltet.
3. Lukk vinduet **Kundeprisgruppe**.
4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
5. Velg varen **1896-S, Athens Desk**.
6. Velg handlingen **Varianter**, og legg deretter til to varianter `PREMIUM, Athens Desk, Premium edition` og `ESSENTIAL, Athens Desk, Essential edition`.
7. Velg **Utvidet tekst** og opprett en ny utvidet tekst som gjelder alle språkkoder. Angi `Shopify` i **Beskrivelse**-feltet. 
8. Legg til følgende beskrivelse i HTML-koder: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`.
9. Velg **Salgspriser**, og legg til nye priser som vist i følgende tabell:

  |Linje|**Salgstype**|**Salgskode**|Type| - kode|Variantkode<br>(legg til feltet via tilpasning)|Enhetspris|
  |------|------------|------------|------------|------------|------------|------------|
  |1|Kundeprisgruppe|SHOPIFY|Element|1896-S|ESSENTIAL|700|
  |2|Kundeprisgruppe|SHOPIFY|Element|1896-S|PREMIUM|1 000|

10. Velg **Salgsrabatter** og legg til en ny rabatt:

* **Salgstype** *Kunderabattgruppe*
* **Salgskode** *DETALJHANDEL*
* **Type** *Vare*
* **Kode** *1896-S*
* **Enhetskode** *STK*
* **Linjerabatt-%** *10*

11. Velg **Varereferanser** og følgende tilleggslinjer:

  |Linje|**Referansetype**|**Referansenr.**|Variantkode|
  |------|------------|------------|------------|
  |1|Strekkode|77777777|ESSENTIAL|
  |2|Strekkode|11111111|PREMIUM|

12. Lukk **varekortet**.
13. Velg varen **1920-S, ANTWERP Conference Table**.
14. Velg **Juster lager** og skriv inn `100` for lokasjonene **ØST** og *VEST* i feltet *Ny beholdning*. 
1. Velg **OK**.
1. Lukk **varekortet**.

Juster synkroniseringsinnstillingene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg *DEMO1*-butikken du vil synkronisere varer med for å åpne siden Shopify-butikkort.
3. Velg *SHOPIFY* i feltet **Kundeprisgruppe**.
4. Velg *DETALJHANDEL* i feltet **Kunderabattgruppe**.
5. Aktiver feltet **Synkroniser utvidet tekst for vare**.
6. Velg *varenr. + variantkode* i feltet **Tildeling for lagerføringsenhet**.
7. Velg *Utkast* i feltet **Status for opprettede produkter**.
8. Velg *Status som skal arkiveres* i feltet **Handling for fjernet produkt**.

Kjør synkroniseringen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg *DEMO1*-butikken du vil synkronisere varer med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Produkter** for å åpne vinduet **Shopify-produkter**.
4. Velg handlingen **Legg til varer**.
5. Sett filteret *TABELL* på feltet **Varekategorikode**.
6. Velg handlingen **Synkroniser produktbilder**.
7. Velg handlingen **Synkroniser lager**.

Produkter legges til. Legg merke til at statusen er satt til *Utkast*, og derfor er ikke varene synlige i Shopify-nettbutikken.

1. Velg linjen med varen *1920-S, ANTWERP Conference Table*. Angi `Rectangular meeting table Antwerp, 10 seats, black` i **SEO-tittelen**.
2. Velg *Aktiv* i feltet **Status**.
3. Velg linjen med varen *1906-S, ATHENS, Mobile Pedestal*, og velg deretter handlingen **Slett**.

I **Shopify-administrator** legger du merke til at alle produkter har forskjellige statuser.

* *ANTWERP Conference Table* er *Aktiv* fordi vi endret statusen i vinduet **Shopify-produkt**.
* *ATHENS Desk* er *Utkast* fordi vi konfigurerte standardstatusen for alle tillagte produkter som *Utkast*.
* *ATHENS Mobile Pedestal* *arkiveres* fordi vi har konfigurert butikken slik at den automatisk tildeler statusen *Arkivert* for slettede produkter.

Legg merke til at lageret for ANTWERP Conference Table er 100, fordi vi konfigurerte systemet til å bruke lager bare fra to lokasjoner HOVED og ØST. Lageret på andre lokasjoner (VEST) ignoreres.

* Åpne *ANTWERP Conference Table*, legg merke til feltene **Egendefinert type**, **Leverandør**, **Vekt**, **Kostnad per vare** og delen **Forhåndsvisning av søkemotor**.
* Åpne *Athens Desk*, rull nedover til **Varianter**-delen, og legg merke til hvordan **Lagerføringsenhet** er fylt ut.
* Velg **Rediger** for å gå gjennom strekkode og priser.
* Endre status for *Athens Desk* til *Aktiv*, og velg **Forhåndsvis**-handlingen.

I **Shopify-nettbutikken** åpner du produktkatalogen og finner produktet *Athens Desk*. Legg merke til at andre alternativer er tilgjengelige. For ulike alternativer er prisene forskjellige. Vær oppmerksom på rabattinformasjon.

## <a name="walkthrough-import-items-from-shopify"></a>Gjennomgang: Importer varer fra Shopify

### <a name="scenario"></a>Scenario 

Du har allerede en vellykket nettbutikk og ønsker å begynne å bruke [!INCLUDE[prod_short](../includes/prod_short.md)] som programvare for forretningsstyring. Du ønsker å importere så mye data fra Shopify som mulig. 

### <a name="steps"></a>Trinn

Dette er en fortsettelse av [Gjennomgang: Begynn å selge produkter på nettet](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Du kan også prøve med dine egne data, for eksempel Shopify-butikken eller -sandkassen.

Gjør følgende trinn i [!INCLUDE[prod_short](../includes/prod_short.md)]:

#### <a name="prepare-data"></a>Klargjør data

1. Bytt til en 30-dagers prøveversjon uten eksempeldata. Hvis du vil ha mer informasjon, kan du se [Legg til dine egne data i en tom prøveversjon](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions.md#add-your-own-data-to-an-empty-trial-company).
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikk** og velger den relaterte koblingen.
3. Velg handlingen **Ny**.
4. Skriv inn `DEMO2` i **Kode**-feltet.
5. I feltet **Shopify-nettadresse** angir du nettadressen til nettbutikken du vil koble deg til.
6. Aktiver vekslebryteren **Aktivert**, se gjennom og godta vilkårene.

Konfigurer Shopify-butikken slik det er beskrevet i fremgangsmåten nedenfor:

7. Aktiver vekslebryteren **Logg aktivert**.
8. Deaktiver vekslebryteren **Tillat bakgrunnssynkroniseringer**.
9. Velg **Fra Shopify** velger du **Synkroniser vare**-feltet.
5. Aktiver vekslebryteren **Opprett ukjente varer automatisk**.
11. Fyll ut feltet **Varemalkode** med riktig mal.
12. Velg **Fra Shopify** velger du **Synkroniser varebilder**-feltet.
13. Velg **Alle kunder** i **Kundeimport fra Shopify**.
14. Aktiver vekslebryteren **Opprett ukjente kunder automatisk**.
15. Fyll ut feltet **Kundemalkode** med riktig mal.
16. Fyll ut **fraktkostnadskontoen**, **tipskontoen** med inntektskontoen. Bruk for eksempel `40100` i USA.
17. Aktiver vekslebryteren **Opprett ordrer automatisk**.

#### <a name="run-the-synchronization"></a>Kjør synkroniseringen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg *DEMO2*-butikken du vil synkronisere data med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Synkroniser produkter**.
4. Velg handlingen **Synkroniser produktbilder**.
5. Velg handlingen **Synkroniser kunder**.

### <a name="results"></a>Resultater

* Shopify-produkter importeres. For å bekrefte velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-produkter**. Velg den relaterte koblingen.
* Varer med bilder opprettes. For å bekrefte velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Vare** og velg den relaterte koblingen.
* Shopify-kunder importeres. For å bekrefte velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-kunder**. Velg den relaterte koblingen.
* Kunder opprettes. For å bekrefte velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder**. Velg den relaterte koblingen.


## <a name="see-also"></a>Se også

[Kom i gang med Shopify-koblingen](get-started.md)  