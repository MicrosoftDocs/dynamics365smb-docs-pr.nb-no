---
title: "Velge brukeropplevelsen for å vise eller skjule avanserte funksjoner | Microsoft-dokumentasjon"
description: "Finn ut hva brukeropplevelsesnivåene Basic og Essential betyr for brukergrensesnittet, moduler og selskapet ditt."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 07/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d0ef9148b082b05a46283f89c3cb98bb1cd0c6d0
ms.openlocfilehash: f8dd92a5a7398ddce64dd4fce0ce9323014a29a0
ms.contentlocale: nb-no
ms.lasthandoff: 08/06/2018

---
# <a name="changing-which-features-are-displayed"></a>Endre hvilke funksjoner som vises
[!INCLUDE[d365fin](includes/d365fin_md.md)] er utformet for å hjelpe deg med å drive bedriften din, uansett hvilken bransje du er i. I kjernen av [!INCLUDE[d365fin](includes/d365fin_md.md)] finner du prosessene for finansrapportering, salg og innkjøp. Du legger til opplevelser i henhold til forretningsbehovene, ved å legge til utvidelser fra AppSource eller ved å endre Opplevelse-innstillingen for selskapet. Hvis du vil ha mer informasjon, gå til [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md), eller delen "Velge en brukeropplevelse for å vise eller skjule funksjoner".

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Velge en brukeropplevelse for å vise eller skjule funksjoner
Brukeropplevelsen bestemmer hvor mye av kjernefunksjonaliteten som er tilgjengelig, når du og dine kolleger bruker [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan velge brukeropplevelsen for firmaet, i vinduet **Selskapsopplysninger** vinduet i feltet **Opplevelse**.

> [!NOTE]  
> Denne innstillingen gjelder for alle brukerne i firmaet. Brukere kan ytterligere tilpasse sin egen opplevelse ved å endre sideoppsett og innholdet. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet og sider](ui-personalization-user.md).  

Tabellen nedenfor viser opplevelsene som er tilgjengelige for øyeblikket.

| Opplevelse | Innvirkning på brukergrensesnittet |
| --- | --- |
| **Grunnleggende** |Viser bare kjernehandlinger og felt i de vanligste forretningsfunksjonene, for eksempel salg, kjøp, lager og finans. |
| **Viktig** |Viser alle handlinger og felt for alle vanlige forretningsfunksjoner.|
| **Premium** |Viser alle handlingene og felt for alle forretningsfunksjonene, inkludert produksjons- og servicehåndtering.|

> [!NOTE]  
> Opplevelser som du kan velge mellom i [!INCLUDE[d365fin](includes/d365fin_md.md)] avhenger av lisensen for løsningen, som kalles en plan. Informasjon om **Essential** og **Premium**-planer, kan du se [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) på markedsføringssiden for Microsoft Dynamics 365. Se også [[!INCLUDE[d365fin](includes/d365fin_md.md)] lisensveiledningen for](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409).

> [!IMPORTANT]  
> Alle vanlige brukere av en løsning må tilordnes samme plan, Essential eller Premium, før denne opplevelsen kan velges for selskapet. På samme måte får ikke én bruker tilgang til Premium-funksjoner hvis én eller flere brukere bare har tilgang til Essential-funksjoner. Dette gjelder ikke for ikke-vanlige brukere av typen teammedlem, intern administrasjon, ekstern regnskapsfører og delegert administrator, som hver kan tilordnes en annen plan enn andre brukere av løsningen.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Aktivere Premium-funksjoner etter oppgradering av en plan
Brukere tilordnes til planer i Office 365-administrasjonssenteret i forbindelse med det generelle arbeidet med å opprette Business Central-brukere. For mer informasjon, se [Legge til brukere i Office 365 for bedrifter](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Du kan deretter definere hvilke bestemte funksjoner og vinduer i opplevelsen disse brukere skal ha tilgang til, ved å tilordne tillatelsessett. Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Slik oppdaterer du planendringer i brukergrupper
Når du har endret brukerplaner i Office 365-administrasjonssenteret, for eksempel tilordnet flere brukere til Premium-planen, må du gjenspeile endringen i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Logg på som administrator.
2. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Brukere**, og velg deretter den relaterte koblingen.
3. I **Brukere**-vinduet velger du **Oppdater alle brukergrupper**-handlingen.

Alle nye opplysninger om brukernes planer og deres tilordnede brukergrupper oppdateres nå i henhold til planendringene.

### <a name="to-select-the-premium-experience"></a>Slik velger du Premium-opplevelsen
Du kan nå fortsette med å velge den nye opplevelsen.
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Selskapsopplysninger**, og velg deretter den relaterte koblingen.
2. I **Selskapsopplysninger**-vinduet i hurtigfanen **Brukeropplevelse** velger du Premium i **Opplevelse**-feltet.

## <a name="see-also"></a>Se også
[Opprette nye seleskaper](about-new-company.md)  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)    
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Lisensveiledning for [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

