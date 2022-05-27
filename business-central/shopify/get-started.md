---
title: Kom i gang med kobling for Shopify
description: Første trinn når du konfigurerer tilkobling mellom Business Central og Shopify
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 2b88995cad8cfe0c3688ca062643f2d339fed9bf
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768154"
---
# <a name="get-started-with-the-shopify-connector"></a>Kom i gang med Shopify-koblingen

[!INCLUDE [prod_short](../includes/prod_short.md)] gir deg fleksibilitet til å koble Shopify-butikken (eller butikkene) sammen med den for å maksimere produktiviteten i bedriften din. Du kan administrere og vise innsikt fra virksomheten og Shopify-nettbutikken som én enhet ved å bruke Shopify-koblingen. Du må følge noen trinn for å kunne bruke Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)]. Denne siden fungerer som en veiledning for å fullføre integreringen av Shopify-butikken med [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forutsetninger for Shopify

Du må ha:

- En Shopify-konto
- En Shopify-nettbutikk

Naviger til [Shopify](https://www.shopify.com/) for å opprette en ny Shopify-konto eller registrere deg for en 14-dagers prøveversjon. Se [Shopify-hjelpesenteret](https://help.shopify.com/) hvis du vil ha mer informasjon om hvordan du oppretter og tilpasser nettbutikken.
  
- Andre salgskanaler støttes, for eksempel Shopify-salgssted.

### <a name="recommended-settings"></a>Anbefalte innstillinger

- Deaktiver **Arkiver ordren automatisk** i delen **Ordrebehandling** i innstillingene [**Betaling**](https://www.shopify.com/admin/settings/checkout) i **Shopify-administratoren**.

Se [Test- og opplæringsscenarioer](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation) hvis du vil vite mer om Shopify-innstillinger for demo- og prøveversjonsscenarioer.

## <a name="prerequisites-for-business-central"></a>Forutsetninger for Business Central

- Kontrollerer at utvidelsen **Koble til Shopify for [!INCLUDE[prod_short](../includes/prod_short.md)]** er installert.

Utvidelsen er forhåndsinstallert for alle nye registreringer og prøveversjoner. Hvis du må installere utvidelser fra markedsplassen, går du til [Installer og avinstaller utvidelser](../ui-extensions-install-uninstall.md#install). Følg fremgangsmåten nedenfor hvis du ikke har [!INCLUDE[prod_short](../includes/prod_short.md)].
<!--
## Installing the **Dynamics 365 Business Central** app to your Shopify online store

For existing [!INCLUDE[prod_short](../includes/prod_short.md)], this step is optional and can be skipped.

1. Locate the [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) app on the [Shopify AppStore](https://apps.shopify.com/)
2. Choose the **Add App** button. Sign-in into your Shopify account if prompted. Select the required online shop if you've more than one.
3. After reviewing privacy and permissions, choose the **Install App** button.
  You can find and open the installed **Dynamics 365 Business Central** app in the **Apps** section on the sidebar of **Shopify admin**.
4. Choose **Sign up now** to start [!INCLUDE[prod_short](../includes/prod_short.md)] trial or **Sign in** if you already have [!INCLUDE[prod_short](../includes/prod_short.md)]. You'll be redirected to your [!INCLUDE[prod_short](../includes/prod_short.md)] at [Business Central](https://businesscentral.dynamics.com).
5. The next steps should be done in [!INCLUDE[prod_short](../includes/prod_short.md)].
-->
## <a name="connecting-business-central-to-the-shopify-online-store"></a>Koble Business Central til Shopify-nettbutikken

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg handlingen **Ny**.  
3. I feltet **Kode** angir du det ønsket kode.  
4. Skriv inn nettadressen til nettbutikken som må kobles til, i feltet **Shopify-nettadresse**.
5. Aktiver vekslebryteren **Aktivert**, se gjennom og godta vilkårene.
6. Hvis du blir bedt om det, logger du deg på Shopify-kontoen, ser gjennom personvern og tillatelser, og deretter velger du knappen **Installer app**.

Gjenta trinn 2–6 for alle nettbutikker du vil koble til.

### <a name="next-steps"></a>Neste trinn

Nå er nettbutikken tilkoblet [!INCLUDE[prod_short](../includes/prod_short.md)]. I de neste trinnene skal du definere hvordan og hva som skal synkroniseres.

- [Synkroniser elementer](synchronize-items.md)
- [Synkroniser kunder](synchronize-customers.md)
- [Synkroniser ordrer](synchronize-orders.md)

## <a name="see-also"></a>Se også

[Test- og opplæringsscenarioer](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).

