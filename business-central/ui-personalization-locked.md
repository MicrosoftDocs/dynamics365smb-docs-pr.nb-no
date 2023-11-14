---
title: Hvorfor en side er låst fra tilpasning
description: 'Du kan være sperret fra å tilpasse en side. Her kan du lese mer om hva du kan gjøre for å låse det opp, slik at du kan tilpasse det.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Hvorfor en side er låst fra tilpasning

Det finnes to betingelser som hindrer deg i å tilpasse en side. Siden er låst (som angitt av ikonet ![Tilpassingslås.](media/personalization-lock-icon.png "Tilpass lås")), eller den er blokkert (angitt av ikonet ![Tilpassing blokkert.](media/personalization-blocked-icon.png "Tilpassing blokkert"). ).

## Låst for tilpasning

Hvis det er et ikon ![Tilpasningslås.](media/personalization-lock-icon.png "Tilpass lås") i banneret **Tilpassing** når du åpner en side, er du hindret fra å foreta flere tilpasningsendringer av siden.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Det kan være to årsaker:

1. Du har brukt tilpasning på siden før, men det ble gjort ved hjelp av tidligere versjon av produktet. Vi endret hvordan tilpasningen fungerer i bakgrunnen siden forrige gang du tilpasset siden. Dessverre fungerer ikke den gamle og nye måten å gjøre ting på.

2. Hittil har du bare brukt buen avskrevet [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til å tilpasse siden.

### Låse opp siden

Hvis du vil låse opp en side og fortsette med å tilpasse den, velger du ikonet ![Tilpassingslås](media/personalization-lock-icon.png "Tilpass lås") og deretter handlingen **Lås opp**.  

> [!CAUTION]
> Gjeldende tilpasning av siden slettes. Siden vil gå tilbake til det opprinnelige oppsettet, og du må begynne fra begynnelsen.  

## Blokkert for tilpasning

Hvis ikonet ![Tilpassing blokkert](media/personalization-blocked-icon.png "Tilpassing blokkert") vises på **Tilpasse**-banneret, kan du kan gjøre eventuelle tilpassinger på siden.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked.](media/personalization-blocked.png "Personalize lock") -->

Dette er fordi rollesenteret eller rollen som er knyttet til brukerkontoen, endrer denne siden spesielt for din rolle. Kontakt systemansvarlig for å få hjelp. Du kan eventuelt prøve å bytte til et rollesenter som inkluderer rolleskreddersying for denne siden. Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).

## Se også

[Tilpasse arbeidsområdet](ui-personalization-user.md)  
[Tilpasse sider for profiler](ui-personalization-manage.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
