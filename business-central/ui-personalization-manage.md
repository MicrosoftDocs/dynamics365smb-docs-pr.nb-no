---
title: Administrere tilpasnings om administrator i Business Central | Microsoft-dokumentasjon
description: Finn ut hvordan du kan tilpasse brukergrensesnittet slik at det passer til din arbeidsmåte.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: ad3b4cf3be7031ab1c7c4699bed6020fe09bd2d1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803140"
---
# <a name="managing-personalization-as-an-administrator"></a>Administrere tilpasning som Administrator
<!--NAV in the Web client--> Brukere kan tilpasse arbeidsområdet etter egne behov. Som administrator kan du kontrollere og håndtere tilpasning ved å deaktivere muligheten for brukerne til å tilpasse sider og fjerne en hvilken som helst sidetilpasning som brukere har utført.

## <a name="disable-personalization-for-a-profile"></a>Deaktivere tilpasning for en profil
Du kan hindre alle brukere som tilhører en bestemt profil, fra å tilpasse sine sider.
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Profilliste**, og velg deretter den relaterte koblingen.
2.  Velg profilen i listen som du vil endre.
3. Merk av for **Deaktiver tilpasning**, og velg deretter **OK**.

## <a name="clear-user-personalizations"></a>Fjerne brukertilpasninger

Hvis du fjerner sidetilpasninger, endres siden tilbake til det opprinnelige oppsettet før eventuelle tilpasninger ble utført. Du kan slette tilpasninger brukere har gjort med sider, på to måter: ved hjelp av siden **Slett brukertilpasning** og ved hjelp av siden **Brukertilpasningskort**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Slette brukertilpasninger ved hjelp av siden Slett brukertilpasning

Siden **Slett brukertilpasning** lar deg slette tilpasninger for hver enkelt side og bruker.

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slett brukertilpasning**, og velg deretter den relaterte koblingen.

    Siden viser alle sidene som er tilpasset, og brukerne de tilhører.

    >[!NOTE]
    > Hvis det er merket av for **Gammel tilpassing**-kolonnene, angir dett at tilpassingen ble utført i en eldre versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)], som håndterte tilpassing annerledes enn nå. Brukere som prøver å tilpasse disse sidene, er låst fra å gjøre dette med mindre de ønsker å låse opp siden. Hvis du vil ha mer informasjon, kan du se [Hvorfor en side er låst fra tilpassing](ui-personalization-locked.md).

2. Velg posten du vil slette, og velg deretter handlingen **Slett**.

    Brukeren vil se endringene neste gang vedkommende logger på.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Slette brukertilpasninger ved hjelp av siden Brukertilpasningskort

Siden **Brukertilpasningskort** gir deg muligheten til å slette tilpasningen på alle sider for en bestemt bruker. Dette krever skrivetilgang til tabellen 2000000072 **profil**.

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukertilpasning**, og velg deretter den relaterte koblingen.

    Siden **Brukertilpasning** viser alle brukerne som kan ha tilpassede sider. Hvis du ikke finner en bruker i listen, betyr det at de ikke har tilpassede sider.

2. Velg brukeren fra listen, og velg deretter handlingen **Rediger**.

3.  I kategorien **Handlinger** velger du **Fjern tilpassede sider**.

    Brukeren vil se endringene neste gang vedkommende logger på.

## <a name="see-also"></a>Se også
[Tilpasse arbeidsområdet](ui-personalization-user.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
