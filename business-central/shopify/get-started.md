---
title: Kom i gang med kobling for Shopify
description: Første trinn når du konfigurerer tilkobling mellom Business Central og Shopify
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: brentholtorf
ms.author: bholtorf
---

# Kom i gang med Shopify-koblingen

Koble til Shopify-butikken (eller -butikker) med [!INCLUDE [prod_short](../includes/prod_short.md)] og maksimer produktiviteten i bedriften din. Administrer og vis innsikt fra virksomheten og Shopify-butikken som én enhet.

For å bruke Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)] er det et par ting du må gjøre først. Denne artikkelen fungerer som en veiledning for å integrere Shopify-butikken med [!INCLUDE [prod_short](../includes/prod_short.md)].

## Forutsetninger for Shopify

Du må ha:

- En Shopify-konto
- En Shopify-nettbutikk

For å finne ut mer om hvordan du oppretter Shopify-prøveversjoner og anbefalte innstillinger går du til [Oppretting og konfigurering av Shopify-konto](shopify-account.md).

## Forutsetninger for Business Central

- Kontroller at appen **[Shopify-kobling](https://go.microsoft.com/fwlink/?linkid=2196238)** er installert.

  Appen er forhåndsinstallert for alle nye registreringer og prøveversjoner. Finn ut mer om å installere apper fra AppSource under [Installer og avinstaller utvidelser](../ui-extensions-install-uninstall.md#install). Følg fremgangsmåten nedenfor hvis du ikke har [!INCLUDE[prod_short](../includes/prod_short.md)].

- Kontroller at brukeren har riktige tillatelser. Shopify-koblingen er dekket av tillatelsessettet **Shopify – administrator (SHPFY - ADMIN)**. Finn ut mer under [Opprett brukere i henhold til lisenser](../ui-how-users-permissions.md) og [Tildel tillatelser til brukere og grupper](../ui-define-granular-permissions.md).

## Installer Dynamics 365 Business Central-appen i Shopify-nettbutikken

Dette trinnet er valgfritt for eksisterende forekomster av [!INCLUDE[prod_short](../includes/prod_short.md)] og kan hoppes over.

1. finn [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-appen i [Shopify AppStore](https://apps.shopify.com/)
2. Velg **Legg til app**-knappen. Logg deg på Shopify-kontoen hvis du blir bedt om det. Velg nettbutikken hvis du har mer enn én.
3. Når du har gjennomgått personvern og tillatelser, velger du knappen **Installer app**.

   Du kan søke etter og åpne den installerte **Dynamics 365 Business Central**-appen i delen **Apper** på sidepanel for siden **Shopify-administrator**.
4. Velg **Registrer deg nå** for å starte [!INCLUDE[prod_short](../includes/prod_short.md)]-prøveversjonen eller **Logg på** hvis du allerede har [!INCLUDE[prod_short](../includes/prod_short.md)]. Du blir omdirigert til [Business Central](https://businesscentral.dynamics.com)-siden.
5. Gjør følgende trinn i [!INCLUDE[prod_short](../includes/prod_short.md)].

## Koble Business Central til Shopify-nettbutikken

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg handlingen **Ny**.  
3. I feltet **Kode** angir du en kode som gjør den enkel å finne i [!INCLUDE[prod_short](../includes/prod_short.md)]. Navnet kan for eksempel gjenspeile hva en butikk selger, for eksempel møbler eller kaffe, eller landet eller området den betjener.
4. I feltet **Shopify-nettadresse** angir du nettadressen til nettbutikken du kobler deg til. Bruk følgende format: `https://{shop}.myshopify.com/`.
5. Aktiver vekslebryteren **Aktivert** og se gjennom og godta vilkårene.
6. Hvis du blir bedt om det, logger du deg på Shopify-kontoen. Gå gjennom personvernvilkårene og velg knappen **Installer app**.

Gjenta trinn 2–6 for alle nettbutikker du vil koble til.

### Kjente problemer

- Nettleseren blokkerer popup-vinduet. Når du slår på **Aktivert**-bryteren, åpner [!INCLUDE [prod_short](../includes/prod_short.md)] siden **Venter på svar – ikke lukk denne siden** mens den venter på et tilgangstoken fra Shopify. Hvis siden er lukket eller blokkert, kan du ikke koble til Shopify. Finn ut mer på [Be om tilgangstokenet](troubleshoot.md#request-the-access-token)
- Det kan være lurt å ha Shopify-administratoren åpen i samme nettleser som [!INCLUDE [prod_short](../includes/prod_short.md)]
- [Feil: Oauth-feilen invalid_request: Finner ikke Shopify API-program med api_key](troubleshoot.md#error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Feil: Oauth-feil invalid_request: Kontoen din har ikke tillatelse til å gi den forespurte tilgangen for denne appen.](troubleshoot.md#error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app)
- [Kan ikke koble til fra sandkasse](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment)

## Neste trinn

Nå er nettbutikken tilkoblet [!INCLUDE[prod_short](../includes/prod_short.md)]. I de neste trinnene skal du definere hvordan og hva som skal synkroniseres.

- [Synkroniser elementer](synchronize-items.md)
- [Synkroniser kunder](synchronize-customers.md)
- [Synkroniser ordrer](synchronize-orders.md)

## Teststrategier

Det finnes forskjellige måter å teste en samhandling på, og hver fremgangsmåte har fordeler og ulemper.

Du kan koble til [!INCLUDE[prod_short](../includes/prod_short.md)]- og Shopify-kontoer så ofte du vil. Shopify-koblingen påvirker bare miljøet, eller mer nøyaktig, firmaet der det er aktivert. Du kan koble til den samme Shopify-nettbutikken fra flere miljøer eller selskaper. Du kan deaktivere og aktivere koblingen på nytt.

Det er enkelt å kjøre synkroniseringstester på nytt. Koblingen gjør det mulig å slette importerte data, for eksempel produkter, kunder og ordrer, og deretter importere dem på nytt. [Tilbakestill synkronisering](troubleshoot.md#reset-sync).

### Shopify-sandkasse og Business Central-sandkasse

Dette er antakelig den sikreste måten å teste integrering på. I stedet for å bruke en Shopify-sandkasse, kan du også bruke et prøveabonnement eller utviklingsbutikk. I [!INCLUDE[prod_short](../includes/prod_short.md)] kan du også bruke et testselskap i et produksjonsmiljø.

Hvis du vil finne ut mer om [!INCLUDE[prod_short](../includes/prod_short.md)]-sandkasser, kan du gå til [Opprett et nytt miljø](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

### Shopify-sandkasse og Business Central-produksjon

Dette er *ikke* en anbefalt konfigurasjon for testing fordi Shopify-koblingen kan opprette eller endre varer og kunder. Det kan også opprette salgsdokumenter, for eksempel bestillinger og fakturaer. Det kan være vanskelig å angre disse dokumentene.
 
Hvis du må bruke denne konfigurasjonen, anbefaler vi at du leser og sannsynligvis deaktiverer følgende innstillinger:

* **Opprett ukjent vare automatisk** uten å opprette varer
* **Shopify kan oppdatere varer** for ikke å oppdatere tildelte varer
* **Opprett ukjent kunde automatisk** for ikke å opprette kunder og kontakter
* **Shopify kan oppdatere kunder** for ikke å oppdatere eksisterende kunder
* **Opprett ordre automatisk** for ikke å opprette ordrer og salgsfakturaer

Hvis du vil ha mer informasjon, kan du se [Gjenoppretting av et miljø](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).

### Shopify-produksjon og Business Central-sandkasse

Det kan være lurt å sikkerhetskopiere dataene. Du kan for eksempel eksportere produkter og kunder. Hvis du vil ha mer informasjon, kan du se [Bruk CSV-filer til å sikkerhetskopiere lagringsinformasjon](https://help.shopify.com/en/manual/shopify-admin/duplicate-store#using-csv-files-to-back-up-store-information).

Deaktiver **Tillat datasynkronisering til Shopify** for å veksle slik at [!INCLUDE[prod_short](../includes/prod_short.md)] ikke skriver til Shopify. I dette tilfellet kan du importere produkter, bilder, kunder og ordrer fra Shopify. Men du kan ikke sende vare, priser, lagernivåer, kunder, oppfyllelsesinformasjon til Shopify.

Hvis du holder vekslebryteren **Tillat datasynkronisering til Shopify** aktiver, er de beskyttende tiltakene:

*   Velg **Utkast** i feltet **Status for Opprett produkt** for å sikre at eksporterte produkter ikke er tilgjengelige for kjøpere. Du kan kontrollere hvordan produkter vises i nettbutikken, synkronisere priser, alternativer og lagernivåer. Bare pass på at du bruker filtre på siden **Legg til vare i Shopify** for å begrense antall eksporterte varer.
* Deaktiver **Eksport kunde til Shopify**-vekslebryteren slik at du ikke sender kunder til Shopify.

## Se også

[Gjennomgang: Konfigurer og bruk Shopify-koblingen](walkthrough-setting-up-and-using-shopify.md)  

