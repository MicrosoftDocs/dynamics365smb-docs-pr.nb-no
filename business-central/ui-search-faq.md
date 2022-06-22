---
title: Vanlige spørsmål om Fortell meg
description: Denne artikkelen gir svar på spørsmål som våre kunder og partnere ofte stiller om Fortell meg-funksjonen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: TellMe
ms.date: 05/23/2022
ms.author: bholtorf
ms.openlocfilehash: 6217fa0bd800f90bffce85e272f2ee99576c6a2d
ms.sourcegitcommit: 93f30ce3349233cbcd03f300e74b654b49fa5518
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/24/2022
ms.locfileid: "8799447"
---
# <a name="tell-me-faq"></a>Vanlige spørsmål om Fortell meg
Denne artikkelen gir svar på spørsmål som våre avanserte brukere ofte stiller om Fortell meg-funksjonen.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Kan alle handlinger fra den gjeldende siden oppdages i Fortell meg?

Nei. Handlinger i deler, for eksempel salgslinjer eller faktabokser, vises ikke i Fortell meg.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Er resultatene i Fortell meg filtrert etter tillatelser?

Hvis brukeren ikke har AccessByPermissions, vises ikke handlinger. Sider og rapporter vises i resultatet, men krever at brukeren har tillatelse til å få tilgang til dem. En melding vises hvis brukeren ikke har tillatelse til å vise objektet.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Viser Fortell meg innhold fra tilpasninger eller installerte tredjeparts utvidelser?

Handlinger, sider og rapporter som kommer fra utvidelser, hentes av Fortell meg. For teknisk informasjon om hvordan du gjør det mulig å oppdage egendefinerte sider og rapporter, kan du se [Legge til sider og rapporter i Søk](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Hva gjør dette forskjellig fra det som tidligere ble kalt for Sidesøk?

Sidesøk har utviklet seg til Fortell meg for å hjelpe deg med å arbeide raskt. Sidesøk kunne bare hjelpe deg med å navigere til sider eller rapporter. På et teknisk nivå er Fortell meg ikke lenger basert på det eldre MenuSuite-konseptet.

### <a name="i-use-on-premises-prod_short-does-that-include-tell-me"></a>Jeg bruker lokal [!INCLUDE[prod_short](includes/prod_short.md)]. Inkluderer dette Fortell meg?

Du kan bruke Fortell meg i den lokale webklienten til å finne handlinger, sider og rapporter, men ikke apper og konsulenttjenester på AppSource.

### <a name="is-tell-me-available-for-all-form-factors"></a>Er Fortell meg tilgjengelig for alle skjemafaktorer?

Fortell meg er bare tilgjengelig i webklienten eller Windows-apper for stasjonær datamaskin.

<!-- removed in v20 because of Help pane
### Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

### <a name="does-tell-me-give-me-help-on-how-to-use-pages-reports-and-other-things"></a>Gir Fortell meg hjelp om hvordan jeg bruker sider, rapporter og andre ting?

Nei, men du kan lett hente denne informasjonen fra hjelperuten. Velg **Hjelp**-menyelementet (spørsmålstegnet i øvre høyre hjørne), eller trykk på Ctrl + F1 på tastaturet. Hvis du vil ha mer informasjon, kan du se [Hjelperute](product-help-and-support.md#help-pane).

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Hvorfor ser jeg ikke et bokmerkeikon i søkeresultatene?

Bokmerkeikonet vises ikke i Fortell meg-vinduet når tilpasning er deaktivert for en brukerrolle.


## <a name="see-also"></a>Se også  
[Lagre og tilpasse listevisninger](ui-views.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Finne sider med rolleutforskeren](ui-role-explorer.md)  
[Bokmerke en side eller rapport i rollesenteret](ui-bookmarks.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]