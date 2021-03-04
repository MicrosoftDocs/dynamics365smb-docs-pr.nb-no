---
title: Kontrollere sider i Business Central
description: Bruk funksjonen for sideinspeksjon til å zoome inn detaljer om sideutformingen og datakilden. Sideinspeksjonsfunksjonen er ideell for feilsøking av problemer med dataene.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
author: jswymer
ms.author: jswymer
ms.date: 10/01/2020
ms.openlocfilehash: d80baed51b646b389f9dd86540cc993c212be09b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754395"
---
# <a name="inspecting-pages-in-business-central"></a>Kontrollere sider i Business Central

Sideinspeksjonsfunksjonen gjør det mulig å få opplysninger om en side ved å gi innsikt i sideutformingen, de ulike elementene som utgjør siden, og kilden bak dataene som vises. Sideninspeksjon er spesielt utviklet for administratorer, avanserte brukere, støttepersonell og utviklere. Den er ideell for å lære datamodellen bak en side og feilsøking. Hvis du har et problem på en side, kan du bruke sideninspeksjon til å få informasjon som kan videresendes til systemansvarlig eller servicepersonell.

## <a name="working-with-page-inspection"></a>Arbeide med sideinspeksjon

Startsideinspeksjonen fra **Hjelp og støtte**-siden. Velg spørsmålstegnet øverst til høyre, velg **Hjelp og støtte**, og velg deretter **Undersøk sidene og dataene**. Du kan også bruke hurtigtasten **Ctrl+Alt+F1**.

Ruten **Sideninspeksjon** åpnes på siden. Følgende figur viser ruten **Sideninspeksjon** på siden **Ordre**.

![Sideinspeksjon](media/page-inspection-example.png)

Når ruten **Sideinspeksjon** åpnes for første gang, vises informasjon som gjelder hovedobjektet på siden.

Du kan tastaturet eller pekeenheten til å flytte fokus til forskjellige elementer på siden. Når du velger en faktaboks eller en del på hovedsiden, markeres rammeområdet med en kant, og **Sidenspeksjon**-ruten viser informasjon om det valgte elementet. Den forrige figuren viser opplysninger om listedelen på siden **Ordre**. Når du går til andre sider i programmet, vil ruten **Sideinspeksjon** automatisk oppdateres med sideinformasjon når du flytter.

Hvis du vil ha mer informasjon om hva som vises i sideinspeksjonen, kan du se [Inspisere og feilsøke sider](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) i hjelpen for utviklere og IT-eksperter for Business Central.

Hvis du ikke ser opplysningene du forventer å se i ruten **Sideinspeksjon**, har du trolig ikke den nødvendige tillatelsen, som beskrevet i neste del.

## <a name="controlling-access-to-page-inspection-details"></a>Kontrollere tilgang til sideinspeksjonsinformasjon

Som administrator kan du kontrollere tilgang til alle opplysninger som vises i ruten **Sideinspeksjon**, ved å konfigurere brukernes tillatelser. For å gi en brukertillatelse til alle opplysninger, kan du gi brukere **Kjør**-tilgang for **System**-objekt **5330**. Du kan gi tillatelse ved hjelp av et tillatelsessett (som for eksempel **D365-feilsøking**) eller en brukergruppe (som for eksempel **D365-feilsøking**). Hvis du vil ha mer informasjon om tillatelser, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).

Brukere som ikke har tilgang til **Systemobjekt 5330**, har fremdeles tilgang til **Sideinspeksjon**-ruten, men de ser bare **Side**- og **Tabell**-feltene, som viser grunnleggende informasjon som kan de kan sende videre til støttegruppen.

## <a name="see-also"></a>Se også

[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]