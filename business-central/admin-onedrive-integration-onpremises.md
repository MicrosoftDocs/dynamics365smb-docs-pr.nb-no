---
title: Konfigurere OneDrive-integrasjon med Business Central On-premises
description: Lær mer om hvordan du konfigurerer Business Central on-premises for integrasjon med OneDrive for arbeid eller skole (tidligere kjent som OneDrive for Business).
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 06/13/2024
ms.author: jswymer
ms.service: dynamics-365-op
ms.reviewer: jswymer
---
# Konfigurere OneDrive-integrasjon med Business Central On-premises

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Denne artikkelen forklarer hvordan du konfigurerer integrasjon av OneDrive for arbeid eller skole (tidligere kjent som OneDrive for Business) sammen med Business Central lokalt. I motsetning [!INCLUDE[prod_short](includes/prod_short.md)] på Internett er ikke tilkoblingen mellom Business Central og OneDrive konfigurert automatisk. Hvis tilkoblingen ikke er konfigurert, kan ikke brukerne bruke funksjonene i OneDrive.

Det er to oppgaver som må gjøres for å konfigurere OneDrive-integrasjonen.

- Den første oppgaven innebærer at du registrerer en applikasjon (App) på Microsoft Entra-leieren for Microsoft 365-planen. Den registrerte appen brukes til godkjenningsformål. Denne oppgaven gjøres vanligvis i Azure Portal og Business Central-nettklienten.
- Den andre oppgaven innebærer at du konfigurerer OneDrive-URL-adressen og slår på OneDrive-funksjonene i Business Central. Oppgaven er fullført i Business Central-nettklienten. Den er gjort annerledes for versjon 21 enn for versjon 19 og 20. Versjon 21 introduserer et nytt **OneDrive-oppsett** som erstatter **SharePoint-tilkoblingsoppsettet**.  

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] on-premises kan bare kobles til OneDrive driftet av Microsoft i skyen. Tilkobling av [!INCLUDE[prod_short](includes/prod_short.md)] lokalt til Mine områder-repositoriet til SharePoint Server støttes ikke.

## <a name="registerapp"></a>Registrere en app i Microsoft Entra ID for OneDrive-integrasjon

I denne oppgaven legger du til en registrert app for Business Central i Microsoft Entra-leieren i Microsoft 365-planen. På samme måte som andre Azure-tjenester som arbeider med Business Central, krever OneDrive en appregistrering i Microsoft Entra ID. Appregistreringen tilbyr godkjennings- og autorisasjonstjenester mellom Business Central og SharePoint, som brukes av OneDrive.

Hvis du vil ha detaljerte trinn for å fullføre dette trinnet, kan du se [Registrere et app i Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) i hjelpen for utviklere og IT-eksperter.

Når du registrerer applikasjonen, vurder følgende punkt:

- Hvis du allerede har registrert et program som en del av en integrering med et annet Microsoft-produkt, for eksempel Power BI, kan du bruke denne appregistreringen på nytt. I dette tilfellet må du bare angi SharePoint-tillatelser for den eksisterende registrerte appen.

- Sørg for å konfigurere den registrerte appen med følgende delegerte tillatelser til SharePoint-API-en:

    - AllSites.FullControl
    - User.ReadWrite.All
    
    For Business Central 2021 lanseringsbølge 2 (versjon 19) angir du disse tillatelsene i stedet:
    
    - AllSites.Write
    - MyFiles.Write
    - User.Read.All 

- Hvis du bruker Business Central versjon 19 eller 20, kopierer du **App-ID (klient)** og **klienthemmelighet** som brukes av den registrerte appen. Du må ha denne informasjonen i neste oppgave.

## <a name="url"></a>Hente OneDrive-URL-adressen

[!INCLUDE[onedrive-url](includes/onedrive-url.md)]

## Konfigurere OneDrive-tilkoblingen i versjon 21 og senere

Bruk denne fremgangsmåten hvis du bruker Business Central lanseringsbølge 2 i 2022 (versjon 21) eller senere.

### Forutsetninger

- Indirekte, endre og slette tillatelse (IMD) i tabell **Dokumenttjenestescenario** som et minimum

### Kjør OneDrive-oppsett

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **OneDrive-oppsett** og velger den relaterte koblingen.
2. Første gang du kjører assistert oppsett, ser du **Personvern**. Les informasjonen psiden, og hvis du samtykker velger du **Godta** for å fortsette.
3. På siden **Konfigurer filbehandling** kan du velge mellom følgende alternativer:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

4. På siden **Konfigurer Business Central** angir du OneDrive-URL-adressen i **OneDrive URL**-feltet.

   [Hvordan finner jeg OneDrive-nettadressen?](#url)
5. Velg **Test tilkobling**, og vent på resultatet.
   - Hvis testen er vellykket, velger **Fullført**, og deretter velger du klar til bruk.
   - Hvis testen mislykkes, får du en melding som beskriver problemet. Vanligvis har problemet med URL-adressen du angav, å gjøre. Velg **OK** for å gå tilbake til siden **Konfigurer Business Central**, kontroller URL-adressen, og prøv på nytt.
   - Hvis du ikke allerede har opprettet den Microsoft Entra-registrerte appen, åpnes veiviseren for **Konfigurasjon avMicrosoft Entra ID**.
6. Når dette er fullført, er personvernerklæringen for OneDrive-integrasjon avtalt for alle brukere. Hvis du vil endre den slik at brukere må godta eller være uenig for seg selv, kan du gå til siden **Siden Status for personvernerklæringer** og velge **La brukeren bestemme** for OneDrive-integrasjonen. Brukerne vil da bli bedt om å godta eller ikke godta personvernerklæringen første gang de bruker OneDrive-funksjonene. Hvis du vil ha mer informasjon, kan du se [Personvernerklæringer](privacy-notices-status.md).

## Konfigurere tilkobling i [!INCLUDE[prod_short](includes/prod_short.md)]-versjon 19 og 20

Bruk denne fremgangsmåten hvis du bruker Business Central lanseringsbølge 1 for 2022 (versjon 20) eller lanseringsbølge 2 for 2021 (versjon 19).
> [!IMPORTANT]
> Ved å konfigurere denne funksjonen aktiverer du også eldre funksjoner som sender filer til OneDrive.  
>
>* Funksjonen Åpne i Excel kopierer automatisk Excel-filen til OneDrive og åpner den deretter i Excel Online. 
>* Hvis du eksporterer en rapport til en fil, kopieres filen automatisk til OneDrive, og deretter åpnes den i Excel Online, Word Online eller OneDrive. 
>* Andre funksjoner kan også åpnes automatisk i OneDrive.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Microsoft SharePoint-tilkoblingsoppsett** og velger den relaterte koblingen.
2. I feltet **Beskrivelse** angir du en beskrivelse for tilkoblingen, som **OneDrive**.
3. I feltet **Mappe** skriver du inn **Business Central**.
4. I feltet **Plassering** skriver du inn URL-adressen til OneDrive.

   [Hvordan finner jeg OneDrive-nettadressen?](#url)
5. I feltet **Klient-ID** angir du klient-ID-en fra den registrerte appen.
6. I feltet **Klienthemmelighet** angir du hemmeligheten fra den registrerte appen. 

> [!IMPORTANT]
> Siden **Tilkoblingsoppsett for SharePoint** for brukes til å konfigurere flere eldre funksjoner. **Generelt**-delen konfigurerer tilkoblingen til OneDrive, og delen **Delte dokumenter** omadresserer filer til SharePoint i stedet. **Tilkoblingsoppsett for SharePoint** er avskrevet og vil bli fjernet i neste lansering. Vi anbefaler at du ikke konfigurerer delen **Delte dokumenter**. Hvis du vil ha mer informasjon, se [Avskrevne funksjoner i basisprogrammet](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup).

## Etter oppgradering til versjon 21

Når du oppgraderer til versjon 21 eller senere, vil den eksisterende tilkoblingen til OneDrive som er konfigurert på siden **Tilkoblingsoppsett for SharePoint-siden**, fortsatt fungere. Men siden **Tilkoblingsoppsett for SharePoint** vil bli fjernet i versjon 23, anbefaler vi at du bytter til den nye OneDrive-integrasjonen, som beskrevet i neste del. Denne bryteren gjør nå det enklere når **Tilkoblingsoppsett for SharePoint** blir fjernet. I tillegg kan du bruke assistert oppsettsveiledning for **OneDrive-oppsett** til å håndtere OneDrive-funksjonene som er tilgjengelige for brukerne.

## Bytte fra eldre SharePoint til ny OneDrive-integrasjon 

Hvis du vil bytte til den nye OneDrive-integrasjonen, kjører du assistert oppsettsveiledning for **OneDrive-oppsett**, som du kan åpne direkte eller fra siden **Tilkoblingsoppsett for SharePoint**. Assistert oppsett for **OneDrive-oppsett** leder deg gjennom overgangen og gir informasjon om endringene som foretas langs veien.

Før du begynner med byttet eller slik du gjør det, kan du se i neste avsnitt for å lære om prosessens enkelte aspekter og informasjon. 

### <a name="onedrivesetupmigration"></a>Bytte til ny OneDrive-integrering

I tillegg til OneDrive-integrasjon kan Business Central også integrere med andre tjenester, for eksempel Power BI og Universell utskrift. Integrasjon med disse andre tjenestene krever også en registrert Microsoft Entra-app for godkjenning. Microsoft Entra-appen som brukes av disse andre tjenestene, konfigureres i det assisterte oppsettet **Oppsett av Microsoft Entra-kontoer**. Når du bytter fra oppsettet for eldre SharePoint-tilkoblinger, endrer det nye assisterte oppsettet **OneDrive-oppsett** OneDrive-integrasjonen til også å bruke det assisterte oppsettet **Oppsett av Microsoft Entra-kontoen** – slik at alle integreringer bruker samme Microsoft Entra-app.

Denne endringen har noen konsekvenser når det byttes til den nye OneDrive-integrasjonen, avhengig av om det allerede finnes en Microsoft-app som er konfigurert i det assisterte oppsettet **Oppsett av Microsoft Entra-kontoer**. 

> [!IMPORTANT]
> Når du har byttet til et nytt OneDrive-oppsett, kan du ikke lenger bruke siden **Tilkoblingsoppsett for SharePoint** til å konfigurere OneDrive-integreringen.

#### Hvordan endringene påvirker integreringen

Det assisterte oppsettet for **OneDrive-oppsett** bruker alltid appen som er konfigurert i det assisterte oppsettet **Konfigurere Microsoft Entra-kontoene**, hvis det finnes en. Når du kjører assistert oppsett for **OneDrive-oppsett**, sammenligner programmet appen som er konfigurert i **Oppsett av Microsoft Entra-kontoer** med den gjeldende appen konfigurert i **Tilkoblingsoppsett for SharePoint**.

> [!TIP]
> Siden **Tilkoblingsoppsett for SharePoint** og assistert oppsett for **Konfigurere Microsoft Entra-kontoer**, Microsoft Entra-appen identifiseres appen av **Klient-ID**.

- Hvis appen i **Konfigurere Microsoft Entra-kontoer** er forskjellig fra appen i **SharePoint-tilkoblingsoppsett**, endres OneDrive-integrasjonen slik at den bruker appen i **Konfigurere Microsoft Entra-kontoer**.

   I **OneDrive-oppsett**mens byttet foretas, får du en melding som ligner på følgende: 

  `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This means the client id will change to NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN, you may want to test it has the correct permissions.`

  `NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN` representerer klient-IDen til appen i **Konfigurere Microsoft Entra-kontoer** som OneDrive-integrasjonen er byttet til. 

  > [!IMPORTANT]
  > Hvis ny OneDrive-integrering skal fungere etter at du har gjort det, må du gi appen tillatelse til SharePoint-APIen i Azure-portalen. Du kan gjøre dette trinnet før eller etter at du har byttet til det nye OneDrive-oppsettet. Hvis du vil ha mer informasjon, kan du se delen [Registrere en app i Microsoft Entra ID for OneDrive-integrasjon](#registerapp).

- Hvis appen i **Konfigurere Microsoft Entra-kontoene** er den samme som appen i **Tilkoblingsoppsett for SharePoint**, bruker OneDrive-integrasjonen samme app som tidligere, unntatt fra konfigurasjonen i oppsettet **Konfigurere Microsoft Entra-kontoer**.

   I **OneDrive-oppsett**mens byttet foretas, får du en melding som ligner på følgende:

    `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This has already been configured with the same client id (5F78CADE-19C0-49BF-AF84-306D0579B50E).`

- Hvis det ikke finnes noen app konfigurert i oppsettet **Konfigurere Microsoft Entra-kontoer**, bruker OneDrive-integrasjonen samme app som tidligere.

   Det assisterte oppsettet **OneDrive-oppsett** kopierer appkonfigurasjonen til **Konfigurer Microsoft Entra-kontoer**, slik at det blir brukt til andre integreringer som kan konfigureres senere.

   I **OneDrive-oppsett**mens byttet foretas, får du en melding som ligner på følgende:

   `The Microsoft Entra application used for authentication will be configured for all Business Central integrations`.

### Kjør OneDrive-oppsettet for å bytte til den nye OneDrive-integreringen

1. Åpne enten **OneDrive-oppsett**-siden eller siden **Tilkoblingsoppsett for SharePoint**.
2. Hvis du bruker siden **Tilkoblingsoppsett for SharePoint**, velger du **Gå til nytt OneDrive-oppsett** i meldingen øverst på siden.
3. Følg den assisterte veiledningen for **OneDrive-oppsett**.
4. Når du kommer til siden **Konfigurer filbehandling**, velger du ett av følgende alternativer for å slå på funksjoner:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

5. Siden **Konfigurer Business Central** viser samme URL-adresse som brukes av den eksisterende OneDrive-integrasjonen. Du kan URL-adressen ved behov.
6. Velg **Test tilkobling**, og følg instruksjonene.

   Hvis testen er vellykket, velger du **Fullført**, og du er klar. Hvis ikke bruker du meldingene på siden til å løse problemet.

## Se også
[Business Central og OneDrive-integrering](across-onedrive-overview.md)  
[Åpne Business Central-filer i OneDrive](across-share-onedrive.md)  
[Vanlige spørsmål om OneDrive](admin-onedrive-faq.md)

