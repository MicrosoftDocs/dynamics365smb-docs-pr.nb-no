---
title: Velge brukeropplevelsen for å vise eller skjule avanserte funksjoner | Microsoft-dokumentasjon
description: Finn ut hva brukeropplevelsesnivåene Essential og Premium betyr for brukergrensesnittet, moduler og selskapet ditt.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 9110ee79e4d1788f41c8f1960f282cb490a3cc8a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251426"
---
# <a name="changing-which-features-are-displayed"></a>Endre hvilke funksjoner som vises
[!INCLUDE[d365fin](includes/d365fin_md.md)] er utformet for å hjelpe deg med å drive bedriften din, uansett hvilken bransje du er i. I kjernen av [!INCLUDE[d365fin](includes/d365fin_md.md)] finner du prosessene for finansrapportering, salg og innkjøp. Du legger til opplevelser i henhold til forretningsbehovene ved å legge til utvidelser fra AppSource eller ved å endre Opplevelse-innstillingen for selskapet. Hvis du vil ha mer informasjon, gå til [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md), eller [Velge en brukeropplevelse for å vise eller skjule funksjoner](ui-experiences.md#choosing-a-user-experience-to-show-or-hide-features).

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Velge en brukeropplevelse for å vise eller skjule funksjoner
Brukeropplevelsen bestemmer hvor mye av kjernefunksjonaliteten som er tilgjengelig, når du og dine kolleger bruker [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan velge brukeropplevelsen for firmaet, på siden **Selskapsopplysninger** i feltet **Opplevelse**.

> [!NOTE]  
> Denne innstillingen gjelder for alle brukerne i firmaet. Brukere kan ytterligere tilpasse sin egen opplevelse ved å endre sideoppsett og innholdet. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet og sider](ui-personalization-user.md).  

Tabellen nedenfor viser opplevelsene som er tilgjengelige for øyeblikket.

| Opplevelse | Innvirkning på brukergrensesnittet |
| --- | --- |
| **Essential** |Viser alle handlinger og felt for alle vanlige forretningsfunksjoner.|
| **Premium** |Viser alle handlingene og felt for alle forretningsfunksjonene, inkludert produksjons- og servicehåndtering.|

> [!NOTE]  
> Opplevelser som du kan velge mellom i [!INCLUDE[d365fin](includes/d365fin_md.md)] avhenger av lisensen for løsningen, som kalles en plan. For informasjon om **Essential** og **Premium**-planer, se [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) på markedsføringssiden for Microsoft Dynamics 365. Se også [[!INCLUDE[d365fin](includes/d365fin_md.md)]-lisensveiledningen](https://go.microsoft.com/fwlink/?linkid=2068931) (krever tilgang til CustomerSource eller PartnerSource).

> [!IMPORTANT]  
> Alle vanlige brukere av en løsning må tilordnes samme plan, Essential eller Premium, før denne opplevelsen kan velges for selskapet. På samme måte får ikke én bruker tilgang til Premium-funksjoner hvis én eller flere brukere bare har tilgang til Essential-funksjoner. Dette gjelder ikke for ikke-vanlige brukere av typen teammedlem, intern administrasjon, ekstern regnskapsfører og delegert administrator, som hver kan tilordnes en annen plan enn andre brukere av løsningen.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Aktivere Premium-funksjoner etter oppgradering av en plan
Brukere tilordnes til planer i Office 365-administrasjonssenteret i forbindelse med det generelle arbeidet med å opprette Business Central-brukere. For mer informasjon, se [Legge til brukere i Office 365 for bedrifter](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Du kan deretter definere hvilke bestemte funksjoner og sider i opplevelsen disse brukerne skal ha tilgang til, ved å tilordne tillatelsessett. Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Slik oppdaterer du planendringer i brukergrupper
Når du har endret brukerplaner i Office 365-administrasjonssenteret, for eksempel tilordnet flere brukere til Premium-planen, må du gjenspeile endringen i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Logg på som administrator.
2. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
3. På siden **Brukere** velger du handlingen **Oppdater alle brukergrupper**.

Alle nye opplysninger om brukernes planer og deres tilordnede brukergrupper oppdateres nå i henhold til planendringene.

### <a name="to-select-the-premium-experience"></a>Slik velger du Premium-opplevelsen
Du kan nå fortsette med å velge den nye opplevelsen.
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Selskapsopplysninger**, og velg deretter den relaterte koblingen.
2. På siden **Selskapsopplysninger** i hurtigfanen **Brukeropplevelse** velger du Premium i **Opplevelse**-feltet.

## <a name="help-assumes-premium-experience"></a>Hjelpen tar utgangspunkt i Premium-opplevelsen
Alle funksjonsbeskrivelser i brukerdokumentasjonen for [!INCLUDE[d365fin](includes/d365fin_md.md)] forutsetter **Premium**-opplevelsen, det vil si at beskrivelsene dekker hele omfanget av grensesnittelementer. En tekstmerknad er satt inn i hjelpeemner på høyt nivå for funksjonsområdene Produksjon og Servicehåndtering, om at de krever **Premium**-opplevelsen.

## <a name="see-also"></a>Se også
[Opprette nye selskaper](about-new-company.md)  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)    
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Lisensveiledning for [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
