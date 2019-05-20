---
title: Hvorfor kan jeg ikke tilpasse en side? | Microsoft-dokumentasjon
description: Forklarer hvorfor du kan ikke tilpasse en side og hva du kan gjøre for å låse den opp slik at du kan tilpasse den.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 64995372f68ed2804bc165823dacc34ad6a3194d
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251288"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Hvorfor en side er låst fra tilpasning

Det finnes to betingelser som hindrer deg i å tilpasse en side. Enten hvis siden er låst (som angis av ![Tilpassingslås](media/personalization-lock-icon.png "Tilpassingslås")), eller den er sperret (som angis av ![Tilpassing sperret](media/personalization-blocked-icon.png "Tilpassing sperret")).

## <a name="locked-from-personalizing"></a>Låst for tilpasning

Hvis det er et ![Tilpassingslås](media/personalization-lock-icon.png "Tilpassingslås")-ikon i **Tilpassing**-banneret når du åpner en side (som vist), betyr dette at du er hindret fra å foreta flere tilpasningsendringer av siden.

![Tilpassingslås](media/personalization-locked.png "Tilpassingslås")


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Det kan være to årsaker til dette:

1. Du har brukt tilpasning på siden før, men det ble gjort ved hjelp av tidligere versjon av produktet. Vi endret hvordan tilpasningen fungerer i bakgrunnen siden forrige gang du tilpasset siden. Dessverre fungerer ikke den gamle og nye måten å gjøre ting på.

2. Hittil har du bare brukt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til å tilpasse siden.

### <a name="unlocking-the-page"></a>Låse opp siden

Hvis du vil frigi en side og fortsette med å tilpasse den, velger du ![Tilpassingslås](media/personalization-lock-icon.png "Tilpassingslås") og deretter **Lås opp**.  

Før du låser opp siden må du være oppmerksom på følgende:

- Gjeldende tilpasning av siden slettes. Siden vil gå tilbake til det opprinnelige oppsettet, og du må begynne fra begynnelsen.

- I [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] vil siden forbli som den er, og vil ikke bli påvirket av de nye tilpasningsendringene i Business Central-klienten. I fremtiden vil tilpasningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central-klienten være helt atskilte fra hverandre.

## <a name="blocked-from-personalizing"></a>Blokkert for tilpasning

Hvis det er et ![Tilpassing sperret](media/personalization-blocked-icon.png "Tilpassing sperret")-ikon i tilpasningsbanneret, betyr det at du er sperret for å gjøre eventuelle tilpasninger på siden.

![Tilpassing sperret](media/personalization-blocked.png "Tilpassing sperret")

Dette er fordi rollesenteret eller profilen som er knyttet til brukerkontoen, endrer denne siden spesielt for din rolle. Kontakt systemansvarlig for å få hjelp eller, hvis det er hensiktsmessig, prøv å bytte til et rollesenter (fra [**Mine innstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med brukerinnstillinger i Business Central")) som inkluderer skreddersydde roller for denne siden.

## <a name="see-also"></a>Se også
[Tilpasse arbeidsområdet](ui-personalization-manage.md)  
[Administrere tilpasning](ui-personalization-manage.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
