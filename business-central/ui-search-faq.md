---
title: Vanlige spørsmål om Fortell meg | Microsoft-dokumentasjon
description: Denne artikkelen gir svar på spørsmål som våre kunder og partnere ofte stiller om Fortell meg.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 88a1e6cc711888a3cf68744d0ea6bbfdee41aea3
ms.sourcegitcommit: 49309bdff9b680a35032b355fe97c565845dba15
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2695098"
---
# <a name="tell-me-faq"></a>Vanlige spørsmål om Fortell meg
Dette emnet gir svar på spørsmål som våre avanserte brukere ofte stiller om Fortell meg-funksjonen.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Kan alle handlinger fra den gjeldende siden oppdages i Fortell meg?
Nei. Handlinger i deler, for eksempel salgslinjer eller faktabokser, vises ikke i Fortell meg.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Er resultatene i Fortell meg filtrert etter tillatelser?
Hvis brukeren ikke har AccessByPermissions, vises ikke handlinger. Sider og rapporter vises i resultatet, men krever at brukeren har tillatelse til å få tilgang til dem. En melding vises hvis brukeren ikke har tillatelse til å vise objektet.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Viser Fortell meg innhold fra tilpasninger eller installerte tredjeparts utvidelser?
Handlinger, sider og rapporter som kommer fra utvidelser, hentes av Fortell meg, men ikke egendefinert hjelp. For teknisk informasjon om hvordan du gjør det mulig å oppdage egendefinerte sider og rapporter, kan du se [Legge til sider og rapporter i Søk](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Hva gjør dette forskjellig fra det som tidligere ble kalt for Sidesøk?
Sidesøk har utviklet seg til Fortell meg for å hjelpe deg med å arbeide raskt. Sidesøk kunne bare hjelpe deg med å navigere til sider eller rapporter. På et teknisk nivå er Fortell meg ikke lenger basert på det eldre MenuSuite-konseptet.

### <a name="i-use-on-premises-included365finincludesd365fin_mdmd-does-that-include-tell-me"></a>Jeg bruker lokal [!INCLUDE[d365fin](includes/d365fin_md.md)]. Inkluderer dette Fortell meg?
Du kan bruke Fortell meg i den lokale webklienten til å finne handlinger, sider og rapporter, men ikke dokumentasjon, eller apper og konsulenttjenester på AppSource.

### <a name="is-tell-me-available-for-all-form-factors"></a>Er Fortell meg tilgjengelig for alle skjemafaktorer?
Fortell meg er bare tilgjengelig i webklienten eller Windows-apper for stasjonær datamaskin.

### <a name="are-the-documentation-results-available-in-any-language"></a>Er dokumentasjonsresultatene tilgjengelige på alle språk?
Hjelpeartiklene vises på språket du har angitt i **Mine innstillinger** hvis hjelp er tilgjengelig på dette språket.

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Hvorfor ser jeg ikke et bokmerkeikon i søkeresultatene?
Bokmerkeikonet vises ikke i Fortell meg-vinduet når tilpasning er deaktivert for en brukerrolle.

### <a name="is-the-bookmark-icon-available-for-reports"></a>Er bokmerkeikonet tilgjengelig for rapporter?
Nei. Du kan bare lage bokmerker for en kobling til en side eller hvilke som helst søkeresultater som vises i delen **Sider og oppgaver** i Fortell meg-vinduet.


## <a name="see-also"></a>Se også  
[Lagre og tilpasse listevisninger](ui-views.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Finne sider med rolleutforskeren](ui-role-explorer.md)
