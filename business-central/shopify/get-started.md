---
title: Kom i gang med kobling for Shopify
description: Første trinn når du konfigurerer tilkobling mellom Business Central og Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: 30100, 30101, 30102, 30103, 30104, 30135,
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: bc3c5769a100909faedbfacce58bb1a2b146f5ad
ms.sourcegitcommit: bb6ecb20cbd82fdb5235e3cb426fc73c29c0a7ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802987"
---
# <a name="get-started-with-the-shopify-connector"></a>Kom i gang med Shopify-koblingen

Koble til Shopify-butikken (eller -butikker) med [!INCLUDE [prod_short](../includes/prod_short.md)] og maksimer produktiviteten i bedriften din. Administrer og vis innsikt fra virksomheten og Shopify-butikken som én enhet.

For å bruke Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)] er det et par ting du må gjøre først. Denne artikkelen fungerer som en veiledning for å integrere Shopify-butikken med [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forutsetninger for Shopify

Du må ha:

- En Shopify-konto
- En Shopify-nettbutikk

Hvis du vil ha mer informasjon om hvordan du oppretter Shopify-prøveversjoner og anbefalte innstillinger, går du til [Oppretting og konfigurering av Shopify-konto](shopify-account.md).

## <a name="prerequisites-for-business-central"></a>Forutsetninger for Business Central

- Kontroller at appen **[Shopify-kobling](https://go.microsoft.com/fwlink/?linkid=2196238)** er installert.

  Appen er forhåndsinstallert for alle nye registreringer og prøveversjoner. Finn ut mer om å installere apper fra AppSource under [Installer og avinstaller utvidelser](../ui-extensions-install-uninstall.md#install). Følg fremgangsmåten nedenfor hvis du ikke har [!INCLUDE[prod_short](../includes/prod_short.md)].

- Kontroller at brukeren har tilstrekkelige tillatelser. Shopify-koblingen er dekket av tillatelsessettet *Shopify – administrator (SHPFY - ADMIN)*. Finn ut mer under [Opprett brukere i henhold til lisenser](../ui-how-users-permissions.md) og [Tildel tillatelser til brukere og grupper](../ui-define-granular-permissions.md)


## <a name="install-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Installer Dynamics 365 Business Central-appen i Shopify-nettbutikken

Dette trinnet er valgfritt for eksisterende [!INCLUDE[prod_short](../includes/prod_short.md)] og kan hoppes over.

1. finn [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-appen i [Shopify AppStore](https://apps.shopify.com/)
2. Velg **Legg til app**-knappen. Logg deg på Shopify-kontoen hvis du blir bedt om det. Velg ønsket nettbutikk hvis du har mer enn én.
3. Når du har gjennomgått personvern og tillatelser, velger du knappen **Installer app**.

   Du kan søke etter og åpne den installerte **Dynamics 365 Business Central**-appen i delen **Apper** på sidepanel for siden **Shopify-administrator**.
4. Velg **Registrer deg nå** for å starte [!INCLUDE[prod_short](../includes/prod_short.md)]-prøveversjonen eller **Logg på** hvis du allerede har [!INCLUDE[prod_short](../includes/prod_short.md)]. Du blir omdirigert til [Business Central](https://businesscentral.dynamics.com)-siden.
5. De neste trinnene må utføres i [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connect-business-central-to-the-shopify-online-store"></a>Koble Business Central til Shopify-nettbutikken

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg handlingen **Ny**.  
3. I feltet **Kode** angir du koden som gjør den enkel å finne i [!INCLUDE[prod_short](../includes/prod_short.md)]. Et navn kan for eksempel gjenspeile hva en butikk selger, for eksempel møbler eller kaffe, eller landet eller området den betjener.
4. Skriv inn nettadressen til nettbutikken som må kobles til, i feltet **Shopify-nettadresse**. Bruk følgende format: `https://{shop}.myshopify.com/`.
5. Aktiver vekslebryteren **Aktivert**, se gjennom og godta vilkårene.
6. Hvis du blir bedt om det, logger du deg på Shopify-kontoen, ser gjennom personvernvilkår og tillatelser, og deretter velger du knappen **Installer app**.

Gjenta trinn 2–6 for alle nettbutikker du vil koble til.

### <a name="known-issues"></a>Kjente problemer

- Nettleseren blokkerer popup-vinduet. Når du aktiverer vekslebryteren **Aktivert**, åpner systemet siden **Venter på svar – ikke lukk denne siden**, som venter på et tilgangstoken fra Shopify, hvis siden er lukket eller blokkert – du kan ikke koble til Shopify. Finn ut mer på [Be om tilgangstokenet](troubleshoot.md#request-the-access-token)
- [Oauth-feilen invalid_request: Finner ikke Shopify API-program med api_key](troubleshoot.md#oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Kan ikke koble til fra sandkasse](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment)


## <a name="next-steps"></a>Neste trinn

Nå er nettbutikken tilkoblet [!INCLUDE[prod_short](../includes/prod_short.md)]. I de neste trinnene skal du definere hvordan og hva som skal synkroniseres.

- [Synkroniser elementer](synchronize-items.md)
- [Synkroniser kunder](synchronize-customers.md)
- [Synkroniser ordrer](synchronize-orders.md)

## <a name="see-also"></a>Se også

[Gjennomgang: Konfigurer og bruk Shopify-koblingen](walkthrough-setting-up-and-using-shopify.md)  

