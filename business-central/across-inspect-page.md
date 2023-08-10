---
title: Kontrollere sider i Business Central
description: Bruk funksjonen for sideinspeksjon til å zoome inn detaljer om sideutformingen og datakilden. Sideinspeksjonsfunksjonen er ideell for feilsøking av problemer med dataene.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
author: jswymer
ms.author: jswymer
ms.date: 04/01/2021
---

# <a name="inspecting-pages-in-business-central"></a>Kontrollere sider i Business Central

Sideinspeksjonsfunksjonen gjør det mulig å få opplysninger om en side ved å gi innsikt i sideutformingen, de ulike elementene som utgjør siden, og kilden bak dataene som vises. Sideninspeksjon er spesielt utviklet for administratorer, avanserte brukere, støttepersonell og utviklere. Den er ideell for å lære datamodellen bak en side og feilsøking. Hvis du har et problem på en side, kan du bruke sideninspeksjon til å få informasjon som kan videresendes til systemansvarlig eller servicepersonell.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]

## <a name="work-with-page-inspection"></a>Arbeid med sideinspeksjon

Startsideinspeksjonen fra **Hjelp og støtte**-siden. Velg spørsmålstegnet øverst til høyre, velg **Hjelp og støtte**, og velg deretter **Undersøk sidene og dataene**. Du kan også bruke hurtigtasten <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>F1</kbd>.

Ruten **Sideninspeksjon** åpnes på siden. Når ruten åpnes for første gang, vises informasjon som gjelder hovedobjektet på siden.

Du kan tastaturet eller pekeenheten til å flytte fokus til forskjellige elementer på siden. Når du velger en faktaboks eller en del på hovedsiden, markeres rammeområdet med en kant, og **Sidenspeksjon**-ruten viser informasjon om det valgte elementet. Den forrige figuren viser opplysninger om listedelen på siden **Ordre**. Når du går til andre sider i programmet, vil ruten **Sideinspeksjon** automatisk oppdateres med sideinformasjon når du flytter.

Hvis du vil ha mer informasjon om hva som vises i sideinspeksjonen, kan du se [Inspisere og feilsøke sider](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) i hjelpen for utviklere og IT-eksperter for Business Central.

Hvis du ikke ser opplysningene du forventer å se i ruten **Sideinspeksjon**, har du trolig ikke den nødvendige tillatelsen, som beskrevet i neste del.

## <a name="controlling-access-to-page-inspection-details"></a>Kontrollere tilgang til sideinspeksjonsinformasjon

Som administrator kan du kontrollere tilgang til alle opplysninger som vises i ruten **Sideinspeksjon**, ved å konfigurere brukernes tillatelser. For å gi en brukertillatelse til alle opplysninger, kan du gi brukere **Kjør**-tilgang for **System**-objekt **5330**. Du kan gi tillatelse ved hjelp av et tillatelsessett (som for eksempel **D365-feilsøking**) eller en brukergruppe (som for eksempel **D365-feilsøking**). Hvis du vil ha mer informasjon om tillatelser, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).

Brukere som ikke har tilgang til **Systemobjekt 5330**, har fremdeles tilgang til **Sideinspeksjon**-ruten, men de ser bare **Side**- og **Tabell**-feltene, som viser grunnleggende informasjon som kan de kan sende videre til støttegruppen.

## <a name="see-also"></a>Se også

[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
