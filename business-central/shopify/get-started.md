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
ms.openlocfilehash: b79691660ca84309057c3abab3d3a3df47271f58
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728414"
---
# <a name="get-started-with-the-shopify-connector"></a>Kom i gang med Shopify-koblingen

Koble til Shopify-butikken (eller -butikker) med [!INCLUDE [prod_short](../includes/prod_short.md)] og maksimer produktiviteten i bedriften din. Administrer og vis innsikt fra virksomheten og Shopify-butikken som én enhet.

Shopify-koblingen inneholder følgende funksjoner:

- Støtte for mer enn én Shopify-butikk
  - Hver butikk har sitt eget oppsett, inkludert en samling produkter, lokasjoner som brukes til å beregne lager og prislister.  
- Toveissynkronisering av varer eller produkter.
  - Koblingen synkroniserer bilder, varevarianter, strekkoder, leverandørvarenumre, utvidede tekster og koder.  
  - Eksporter vareattributter til Shopify.  
  - Bruk valgte kundeprisgrupper og rabatter til å definere priser som er eksportert til Shopify.  
  - Angi om varer kan opprettes automatisk, eller bare tillat oppdateringer av eksisterende produkter.  
- Synkronisering av lagernivåer.
  - Velg noen av eller alle de tilgjengelige lokasjonene i [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Oppdater lagernivåer på flere lokasjoner i Shopify.  
- Toveissynkronisering av kunder.
  - Kartlegg kunder smart per telefon og e-post.  
  - Bruk landspesifikke maler når du oppretter kunder, noe som bidrar til å sikre at avgiftsinnstillingene er riktige.  
- Import av ordrer fra Shopify.
  - Under importen kan du automatisk opprette kunder i [!INCLUDE [prod_short](../includes/prod_short.md)] eller velge å håndtere kundene i Shopify.  
  - Ta med ordrer som er opprettet i andre kanaler, for eksempel Shopify-salgssted eller Amazon.  
  - Leveringskostnader, gavekort, tips, leverings- og betalingsmåter, transaksjoner og risiko for svindel.  
  - Motta utbetalingsopplysninger fra Shopify Payments.  
- Spor oppfyllelsesinformasjon.
  - Du kan eventuelt velge å overføre varesporingsinformasjon fra [!INCLUDE [prod_short](../includes/prod_short.md)] til Shopify.  

For å bruke Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)] er det et par ting du må gjøre først. Denne artikkelen fungerer som en veiledning for å integrere Shopify-butikken med [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forutsetninger for Shopify

Du må ha:

- En Shopify-konto.
- En Shopify-nettbutikk.

Gå til [Shopify.com](https://www.shopify.com/) for å opprette en ny Shopify-konto eller registrere deg for en 14-dagers prøveversjon. Finn ut mer om hvordan du oppretter og tilpasser nettbutikken på [Shopify-hjelpesenteret](https://help.shopify.com/).
  
Andre salgskanaler støttes, for eksempel Shopify-salgssted.

### <a name="recommended-settings"></a>Anbefalte innstillinger

- Deaktiver **Arkiver ordren automatisk** i delen **Ordrebehandling** i innstillingene [**Betaling**](https://www.shopify.com/admin/settings/checkout) i **Shopify-administratoren**.

Finn ut mer om Shopify-innstillinger for demo- og prøveversjonsscenarioer på [Test- og opplæringsscenarioer](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Forutsetninger for Business Central

- Kontroller at appen **[Shopify-kobling](https://go.microsoft.com/fwlink/?linkid=2196238)** er installert.

Appen er forhåndsinstallert for alle nye registreringer og prøveversjoner. Finn ut mer om å installere apper fra AppSource under [Installer og avinstaller utvidelser](../ui-extensions-install-uninstall.md#install). Følg fremgangsmåten nedenfor hvis du ikke har [!INCLUDE[prod_short](../includes/prod_short.md)].

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

> [!NOTE]
> Kontroller at nettleseren ikke blokkerer popup-vinduer. Når du aktiverer vekslebryteren **Aktivert**, åpner systemet siden **Venter på svar – ikke lukk denne siden**, som venter på et tilgangstoken fra Shopify, hvis siden er lukket eller blokkert – du kan ikke koble til Shopify. Finn ut mer på [Be om tilgangstokenet](troubleshoot.md#request-the-access-token)

### <a name="next-steps"></a>Neste trinn

Nå er nettbutikken tilkoblet [!INCLUDE[prod_short](../includes/prod_short.md)]. I de neste trinnene skal du definere hvordan og hva som skal synkroniseres.

- [Synkroniser elementer](synchronize-items.md)
- [Synkroniser kunder](synchronize-customers.md)
- [Synkroniser ordrer](synchronize-orders.md)

## <a name="see-also"></a>Se også

[Test- og opplæringsscenarioer](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).
