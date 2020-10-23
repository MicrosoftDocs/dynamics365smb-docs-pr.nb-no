---
title: Hvorfor kan jeg ikke tilpasse en side? | Microsoft-dokumentasjon
description: Forklarer hvorfor du kan ikke tilpasse en side og hva du kan gjøre for å låse den opp slik at du kan tilpasse den.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0bd24833f37fe70f8e642685be4d28dbb593a16d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923398"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Hvorfor en side er låst fra tilpasning

Det finnes to betingelser som hindrer deg i å tilpasse en side. Siden er låst (som angitt av ikonet ![Tilpassingslås](media/personalization-lock-icon.png "Tilpass lås")), eller den er blokkert (angitt av ikonet ![Tilpassing blokkert](media/personalization-blocked-icon.png "Tilpassing blokkert")).

## <a name="locked-from-personalizing"></a>Låst for tilpasning

Hvis ikonet ![Tilpassingslås](media/personalization-lock-icon.png "Tilpass lås") vises på **Tilpasse**-banneret når du åpner en side, betyr dette at du ikke kan foreta flere tilpassingsendringer av siden.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Det kan være to årsaker til dette:

1. Du har brukt tilpasning på siden før, men det ble gjort ved hjelp av tidligere versjon av produktet. Vi endret hvordan tilpasningen fungerer i bakgrunnen siden forrige gang du tilpasset siden. Dessverre fungerer ikke den gamle og nye måten å gjøre ting på.

2. Hittil har du bare brukt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til å tilpasse siden.

### <a name="unlocking-the-page"></a>Låse opp siden

Hvis du vil låse opp en side og fortsette med å tilpasse den, velger du ikonet ![Tilpassingslås](media/personalization-lock-icon.png "Tilpass lås") og deretter handlingen **Lås opp**.  

Før du låser opp siden må du være oppmerksom på følgende:

- Gjeldende tilpasning av siden slettes. Siden vil gå tilbake til det opprinnelige oppsettet, og du må begynne fra begynnelsen.

- I [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] vil siden forbli som den er, og vil ikke bli påvirket av de nye tilpasningsendringene i Business Central-klienten. I fremtiden vil tilpasningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central-klienten være helt atskilte fra hverandre.

## <a name="blocked-from-personalizing"></a>Blokkert for tilpasning

Hvis ikonet ![Tilpassing blokkert](media/personalization-blocked-icon.png "Tilpassing blokkert") vises på **Tilpasse**-banneret, betyr det at du ikke kan gjøre eventuelle tilpassinger på siden.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

Dette er fordi rollesenteret eller rollen som er knyttet til brukerkontoen, endrer denne siden spesielt for din rolle. Kontakt systemansvarlig for å få hjelp. Du kan eventuelt prøve å bytte til et rollesenter som inkluderer rolleskreddersying for denne siden. Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).

## <a name="see-also"></a>Se også
[Tilpasse arbeidsområdet](ui-personalization-user.md)  
[Tilpasse sider for profiler](ui-personalization-manage.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
