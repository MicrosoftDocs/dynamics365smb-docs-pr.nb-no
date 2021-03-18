---
title: Vanlige spørsmål om mobilapper
description: Se svar på vanlige spørsmål om bruk av Business Central på telefonen eller nettbrettet.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: phone, tablet
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: 3b00eb417f2e51d87a58885a50e1262150837d93
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385452"
---
# <a name="mobile-apps-faq"></a>Vanlige spørsmål om mobilapper

Denne artikkelen gir svar på spørsmål som våre avanserte brukere ofte stiller om mobilappene for [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="is-there-an-app-for-my-device"></a>Finnes det en app for enheten min?

Sannsynligvis! Installer [!INCLUDE[prod_short](includes/prod_short.md)]-appen på mobilenheten ved å laste ned appen fra Windows Store, App Store eller Google Play.

- [Windows Store](https://go.microsoft.com/fwlink/?LinkId=734848) (bare PC)
- [App Store](https://go.microsoft.com/fwlink/?LinkId=734847)
- [Google Play](https://go.microsoft.com/fwlink/?LinkId=734849)

## <a name="is-it-the-same-experience-in-the-apps-as-in-the-browser"></a>Er det samme funksjoner i appene som i nettleseren?

Nei, ikke helt. Vi viser for eksempel bare **Hjem**-aktivitetsgruppen på grunn av den begrensede skjermstørrelsen på mobile enheter. Hurtigtastene er heller ikke tilgjengelige fordi du hovedsakelig bruker berøring i stedet for et tastatur til å navigere på mobile enheter.

Tabellen nedenfor beskriver noen av de vanligste forskjellene og begrensningene som kan oppstå når du bruker [!INCLUDE [prod_short](includes/prod_short.md)] på mobile enheter, sammenlignet med i nettleseren.

| Begrep | På nettbrett | På telefoner | Eksempel fra nettleseren |
|--|--|--|--|
| Aktivitetsgrupper | Bare **Hjem**-aktivitetsgruppen vises. | Bare **Hjem**-aktivitetsgruppen vises. | **Hjem** og **Bokførte dokumenter** i `Sales Order Processor`-rollesenteret. |  |
| Velge flere poster i lister | Ikke tilgjengelig. | Ikke tilgjengelig. | `Ctrl+A` eller `Ctrl+Click` på rader i en liste i nettleseren. |
| Handlinger på handlingslinjen | Bare forfremmede handlinger vises. | Bare forfremmede handlinger vises. |  |
| Faktabokser | Vises ikke på listesider eller forslagssider. | Vises ikke på listesider eller forslagssider. | `Customer`-listen i `Small Business`-rollesenteret. |
| Avanserte filtre | Ingen kolonnespesifikk filtrering er tilgjengelig. | Ingen kolonnespesifikk filtrering er tilgjengelig. | På `Customer`-listesiden. |
| Fortell meg | Ikke tilgjengelig ennå. | Ikke tilgjengelig ennå. | Se [Finne sider og informasjon med Fortell meg](ui-search.md). |  |
| Rolleutforsker | Ikke tilgjengelig ennå. | Ikke tilgjengelig ennå. | Se [Finne sider med rolleutforskeren](ui-role-explorer.md). |
| Felter i hurtigfaner | Felter i hurtigfaner på listesider vises ikke. Bare repeater-kontrollen vises på innholdsområdet til siden. | Ikke tilgjengelig. |  |
| Velg fra hele listen | Ikke tilgjengelig for oppslag. Brukere kan ikke kjøre handlinger på en oppslagsside, og de får ikke tilgang til hele settet med poster. | Ikke tilgjengelig for oppslag. Brukere kan ikke kjøre handlinger på en oppslagsside, og de får ikke tilgang til hele settet med poster. | På `Item Card` når du velger **Lagerenheter**. |
| Søke på tvers av listekolonner | Støttes delvis. Søket vil ikke inkludere FlowFields. | Støttes delvis. Søket vil ikke inkludere FlowFields. | Se eksempler på `Customers`-listesiden. |
| Oppslag | Tilgjengelig. | Tilgjengelig, med den forskjellen at avanserte og enkle oppslag har samme virkemåte på telefonen. Oppslaget vil ikke hente kortet, vise faktabokser eller feltgrupper. | Se eksempler på `Customer Card`-siden. |
| Matrisekontroller | Ikke tilgjengelig. | Ikke tilgjengelig. | Se eksempel i `G/L Budget`. |
| Filnedlasting | Tilgjengelig. Kan ikke laste ned flere filer samtidig. | Tilgjengelig. Kan ikke laste ned flere filer samtidig. | `Trial Balance`-rapporten i avmerkingsboksen **Skriv ut til Excel**. |
| Forslagssider | Tilgjengelig. | Ikke tilgjengelig. Det vises en feilmelding. | `Sales Price`-forslaget eller `Cash Flow`-forslaget. |
| Oversikter | Tilgjengelig. | Tilgjengelig, med den forskjellen at de vises i et mursteinsoppsett. | Sidene Kunder eller Ordrer. |
| Innrykk i repeater-kontroller | Tilgjengelig. | Ikke tilgjengelig. Repeater-kontrollen blir gjengitt som et vanlig, flatt mursteinsoppsett. | Sidene Kontoplan og Kontaktlister. |
| Automatisk inndatafokus på første redigerbare felt på en side | Ikke tilgjengelig. | Ikke tilgjengelig. | `Customer Card`-side.<BR /><BR />I nettleseren plasseres fokus automatisk på det første redigerbare feltet (for eksempel `Name`-feltet), slik at du kan endre verdien med en gang.<BR /><BR />I nettbrett- og telefonappene vil ikke dette feltet være i fokus. I stedet må du merke av i feltet manuelt for å gjøre endringer.|

## <a name="is-it-the-same-experience-on-tables-and-phones"></a>Er det samme funksjoner på nettbrett og telefoner?

Nesten, men ikke helt. Ser listen i delen [Er det samme funksjoner i appene som i nettleseren?](#is-it-the-same-experience-in-the-apps-as-in-the-browser).  

## <a name="can-i-connect-the-app-to-our-on-premises-solution"></a>Kan jeg koble appen til vår lokale løsning?

Ja, det kan du! Det er en litt annen måte å logge seg på, det er alt. Hvis du vil ha mer informasjon, kan du se [Bruker du Business Central lokalt?](install-mobile-app.md#using-business-central-on-premises).  

## <a name="see-also"></a>Se også

[Få Business Central på mobilenheten din](install-mobile-app.md)  
[Installer Business Central-appen for Microsoft Teams](across-install-app-for-teams.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]