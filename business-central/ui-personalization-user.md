---
title: Tilpasse sider i Financials | Microsoft-dokumentasjon
description: "Finn ut hvordan du kan tilpasse brukergrensesnittet slik at det passer til din arbeidsmåte."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 246e6fa65de1d638715d16ee76c0c60a88c44cec
ms.contentlocale: nb-no
ms.lasthandoff: 04/18/2018

---
# <a name="personalizing-your-workspace"></a>Tilpasse arbeidsområdet
<!--NAV in the Web client-->
Du kan *tilpasse* arbeidsområdet slik at det passer til arbeidet og preferansene ved å endre sider slik at de bare viser informasjon du trenger, der du trenger den. Tilpasningsendringene som du utfører, påvirker bare hva du ser, ikke hva andre brukere ser.

Avhengig av typen side og hva den inneholder, kan du gjøre følgende:

-   Legge til, flytte og fjerne felt.
-   Legge til, flytte og fjerne kolonner i en liste.
-   Endre den fryste ruten for kolonner i en liste. Den fryste ruten låser én eller flere kolonner til venstre for en liste slik at de alltid er tilgjengelige når du ruller vannrett.
-   Justere bredden til kolonner i en liste.
-   Flytte og fjerne bunker (fliser).
-   Flytte og fjerne deler. Deler er ytterligere inndelinger eller områder på en side som for eksempel inneholder flere felt, en annen side, et diagram eller fliser.  

## <a name="to-personalize-a-page"></a>Slik tilpasser du en side

1. Velg ikonet ![Innstillinger](media/ui-experience/settings_icon_small.png "Innstillinger-ikonet for rollesenteret") øverst til høyre, og klikk deretter **Tilpass**.

    Banneret **Tilpassing** vises øverst, noe som betyr at du kan begynne å gjøre endringer.

    ![Tilpassingsmodus](media/ui_personalize_mode_small.png "Tilpassingsmodus")

2.  Gå til siden som du vil tilpasse.

    Hvis du ser et låseikon i banneret, se [Hvorfor siden er låst](ui-personalization-locked.md) for flere detaljer.

3.  Velg et område som du vil tilpasse, for eksempel et felt eller en kolonneoverskrift i en liste. Alt som du kan tilpasse, blir umiddelbart markert med en pil eller kantlinje.
<!--
    -  If a component can be personalized, an arrow head (![Personalization indicator arrow left](media/ui_personalize_arrow_left.png "Personalization indicator arrow left") or ![Personalization indicator arrow down](media/ui_personalize_arrow_down.png "Personalization indicator arrow down")) appears.
    -   If the component is a part, the extent of the part is indicated by a border.
    -   The freeze pane in a list is indicated by a vertical line along the entire right-side of the last column of the freeze pane.
    -->

4.  Bruk denne tabellen som hjelp til å utføre endringer:     <table>
        <tr><th>Hva vil du gjøre</td><th>Hvordan du gjør det</th></tr>
        <tr><td>Flytte noe, for eksempel et felt, en kolonne i en liste, en flis eller en del</td><td> Pek hvor som helst på det du vil flytte, og dra det til den nye plasseringen. Plasseringen angis enten av en tykk vannrett eller loddrett linje.</td></tr>
        <tr><td>Fjerne noe</td><td>Velg pilspissen, og velg <b>Fjern</b>. </td></tr>
        <tr><td>Legge til et felt eller en kolonne</td><td>I banneret <b>Tilpassing</b> velger du <b>Mer</b>, og velg deretter <b>Felt</b>.<br /></br>Ruten <b>Legg til felt på side</b> åpnes til høyre. Den viser feltene du kan legge til på siden. Feltene som er merket som <b>Plassert</b>, finnes allerede på siden. Feltene som er merket som <b>Klar</b>, finnes ikke på siden for øyeblikket.<br /></br>Hvis du vil legge til et felt, drar du det fra ruten til den ønskede plasseringen. Plasseringen angis enten av en tykk vannrett eller loddrett linje.</td></tr>
        <tr><td>Endre den fryste ruten i en liste til en annen kolonne.</td><td>Velg pilspissen for kolonnen som du vil ha som den siste kolonnen for den fryste ruten, og velg deretter <b>Sett Frys rute</b>.<br /><br/>Hvis du vil sette den fryste ruten tilbake til den opprinnelige utformede plasseringen, velger du pilspissen for den gjeldende kolonnen for fryst rute og velger <b>Fjern Frys rute</b>. Obs!  Du kan ikke fjerne den fryste ruten.</td></tr>
        <tr><td>Endre kolonnebredden</td><td>Dra i kolonnens høyre ramme i raden for tabelloverskriften. <br /><br />Dobbeltklikk høyre rammen for å maksimere kolonnebredden slik at den passer til den lengste tekstlinjen i kolonnen.</td></tr>
      </table>

    > [!IMPORTANT]  
    >   Du kan ikke endre en liste hvis listen vises som fliser. Du må først bytte til listevisning for siden ved å velge ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Vis som liste, pil venstre").

5.  Du kan fortsette å utføre endinger på den samme siden eller flytte til en annen side. Endringene lagres automatisk når du utfører dem. Når du er ferdig, velger du banneret **Tilpassing** og **Ferdig**.

## <a name="clear-personalization-to-change-a-page-back-to-its-original-layout"></a>Fjerne tilpasning for å endre en side tilbake til det opprinnelige oppsettet
Du ønsker kanskje på et gitt tidspunkt å angre tilpasningsendringer du har foretatt på en side over tid, slik at siden ser ut som den var opprinnelig. Du gjør dette ved å velge banneret **Tilpassing**, **Mer** og deretter **Fjern tilpasning**.

## <a name="personalization-in-detail"></a>Tilpasning detaljert
Nedenfor følger noen tips som hjelper deg med å forstå tilpasning bedre.  
-   Når du endrer en kortside som du åpner fra en liste, trer endringene i kraft på alle poster som du åpner fra denne listen. Anta for eksempel at du åpner en bestemt kunde fra kundelistesiden og deretter tilpasser siden ved å legge til et felt. Når du åpner andre kunder fra listen, vises også feltet du har lagt til.
-   Endringer som du utfører, trer i kraft på alle rollesentrene. Hvis du for eksempel gjør en endring i kundelisten når Rollesenter er satt til Forretningsleder, vises også endringen i kundelisten når Rollesenter er angitt som Ordrebehandler.
-   Endringer av en side i en rute trer i kraft på siden der den vises.  
-   Du kan bare legge til felt og kolonner fra en forhåndsdefinert liste, som er basert på siden. Du kan ikke opprette nye.

## <a name="see-also"></a>Se også
[Administrere tilpasning](ui-personalization-manage.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  

