---
title: Velge brukeropplevelsen for å vise eller skjule avanserte funksjoner | Microsoft-dokumentasjon
description: Finn ut hva brukeropplevelsesnivåene Essential og Premium betyr for brukergrensesnittet, moduler og selskapet ditt.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 10/08/2019
ms.author: sgroespe
ms.openlocfilehash: 8c9223176968d048d167b3b8509cab26343ee9f1
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775334"
---
# <a name="change-which-features-are-displayed"></a>Endre hvilke funksjoner som vises
[!INCLUDE[d365fin](includes/d365fin_md.md)] er utformet for å hjelpe deg med å drive bedriften din uavhengig av størrelse og kompleksitet. I kjernen av produktet finner du viktige funksjoner, for eksempel regnskapsrapporter, salg, kjøp og lagerstyring. Etter hvert som bedriftskompleksiteten øker, kan du f.eks. aktivere funksjonaliteten for produksjons- og servicestyring.

Du kan definere vanskelighetsgraden for produktet, og dermed hvilke funksjoner selskapets brukere får tilgang til, ved å endre **Opplevelse**-innstillingen på siden **Selskapsopplysninger**. Merk at du også kan endre opplevelsesinnstillingen ved å legge til bestemte utvidelser fra AppSource. Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md).

Tabellen nedenfor viser opplevelsene som er tilgjengelige for øyeblikket.

| Opplevelse | Innvirkning på brukergrensesnittet |
| --- | --- |
| **Essential** |Viser alle handlinger og felt for alle vanlige forretningsfunksjoner.|
| **Premium** |Viser alle handlingene og felt for alle forretningsfunksjonene, inkludert produksjons- og servicehåndtering.|

Opplevelser som kan velges i [!INCLUDE[d365fin](includes/d365fin_md.md)], gjenspeiler løsningslisensene, kalt planer, som er definert for produktet. For informasjon om Essential- og Premium-planer, se [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) på markedsføringssiden for Microsoft Dynamics 365. Se også [[!INCLUDE[d365fin](includes/d365fin_md.md)]-lisensveiledningen](https://go.microsoft.com/fwlink/?linkid=2068931) (krever tilgang til CustomerSource eller PartnerSource).

> [!IMPORTANT]  
> Alle vanlige brukere av en løsning må tilordnes samme plan, Essential eller Premium, før denne opplevelsen kan velges for selskapet. På samme måte får ikke én bruker tilgang til Premium-funksjoner hvis én eller flere brukere bare har tilgang til Essential-funksjoner. Dette gjelder ikke for ikke-vanlige brukere av typen teammedlem, intern administrasjon, ekstern regnskapsfører og delegert administrator, som hver kan tilordnes en annen plan enn andre brukere av løsningen.<br /><br /> Bare brukere av typen Evaluering eller Premium kan endre verdien i **Opplevelse**-feltet fra Essential til Premium.

Før du definerer et selskapets opplevelsesinnstilling, definerer du brukernes tilgang til bestemte funksjoner og sider ved å tilordne tillatelsessett. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).

**Opplevelse**-innstillingen gjelder for alle brukerne i et selskap, men hver bruker kan tilpasse sin egen opplevelse ved å endre sideoppsett og innhold. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Aktivere Premium-funksjoner etter oppgradering av en plan
Brukere tilordnes til planer i Office 365-administrasjonssenteret i forbindelse med det generelle arbeidet med å opprette Business Central-brukere. For mer informasjon, se [Legge til brukere i Office 365 for bedrifter](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

### <a name="to-update-plan-changes-in-users-groups"></a>Slik oppdaterer du planendringer i brukergrupper
Når du har endret brukerplaner i Office 365-administrasjonssenteret, for eksempel tilordnet flere brukere til Premium-planen, må du gjenspeile endringen i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Logg på som administrator.
2. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
3. På siden **Brukere** velger du handlingen **Oppdater alle brukergrupper**.

Alle nye opplysninger om brukernes planer og deres tilordnede brukergrupper oppdateres nå i henhold til planendringene.

### <a name="to-select-the-premium-experience"></a>Slik velger du Premium-opplevelsen
Du kan nå fortsette med å velge den nye opplevelsen.
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Selskapsopplysninger**, og velg deretter den relaterte koblingen.
2. På siden **Selskapsopplysninger** i hurtigfanen **Brukeropplevelse** velger du Premium i **Opplevelse**-feltet.

## <a name="help-assumes-premium-experience"></a>Hjelpen tar utgangspunkt i Premium-opplevelsen
Alle funksjonsbeskrivelser i brukerdokumentasjonen for [!INCLUDE[d365fin](includes/d365fin_md.md)] forutsetter **Premium**-opplevelsen, det vil si at beskrivelsene dekker hele omfanget av grensesnittelementer.

## <a name="see-also"></a>Se også
[Tilpasse arbeidsområdet](ui-personalization-user.md)  
[Tilpasse Business Central](ui-customizing-overview.md)  
[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Opprette nye seleskaper](about-new-company.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Lisensveiledning for [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
