---
title: Tilpasse sider | Microsoft-dokumentasjon
description: Finn ut hvordan du kan tilpasse brukergrensesnittet slik at det passer til din arbeidsmåte i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 16f334548d9831507970a1b74ba5fa1716611380
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253726"
---
# <a name="personalizing-your-workspace"></a>Tilpasse arbeidsområdet

Du kan *tilpasse* arbeidsområdet slik at det passer til arbeidet og preferansene ved å endre sider slik at de bare viser informasjon du trenger, der du trenger den. Tilpasningsendringene som du utfører, påvirker bare hva du ser, ikke hva andre brukere ser.

Avhengig av sidetypen og hva den omfatter, kan du gjøre ulike ting som å flytte eller skjule feltene, kolonner og handlinger, flytte og skjule hele deler og mer.
<!--
-   Add, move, and remove fields.
-   Add, move, and remove columns in a list.
-   Change the freeze pane of columns in a list. The freeze pane locks one or more columns to the left side of a list so that are always present, even when you scroll horizontally.
-   Adjust the width of columns in a list.
-   Move and remove Cues (tiles).
-   Move and remove parts. Parts are subdivisions or areas on a page that contain things like multiple fields, another page, a chart, or tiles.

-->
> [!NOTE]
> I tillegg til hva brukere kan tilpasse, kan administratorer og superbrukere overstyre brukeres tilpasning og definere funksjonene som er tilgjengelige i alle eller bestemte selskaper. Hvis du vil ha mer informasjon, kan du se [Tilpasse Business Central](ui-customizing-overview.md).

## <a name="to-personalize-a-page"></a>Slik tilpasser du en side

1. Velg ikonet ![Innstillinger](media/ui-experience/settings_icon_small.png "Innstillinger-ikonet for rollesenteret") øverst til høyre, og velg deretter **Tilpass**.

    Banneret **Tilpassing** vises øverst, noe som betyr at du kan begynne å gjøre endringer.

    ![Tilpassingsmodus](media/ui_personalize_mode_small.png "Tilpassingsmodus")

2. Gå til siden som du vil tilpasse.

    Hvis du ser ![Tilpassingslås](media/personalization-lock-icon.png "Tilpassingslås") eller ![Tilpassing sperret](media/personalization-blocked-icon.png "Tilpassing sperret") i banneret, kan du ikke tilpasse siden. Hvis du vil ha mer informasjon, se [Hvorfor kan jeg ikke tilpasse en side?](ui-personalization-locked.md).

3. Velg et område som du vil tilpasse, for eksempel et felt eller en kolonneoverskrift i en liste. Alt som du kan tilpasse, blir umiddelbart markert med et pilhode eller en kantlinje. Se feltet [neste del](#What) for opplysninger om hva du kan gjøre.

4. Du kan fortsette å utføre endinger på den samme siden eller åpne en annen side. Endringene lagres automatisk når du utfører dem. Når du er ferdig, velger du banneret **Tilpassing** og **Ferdig**.

## <a name="What"></a>Hva du kan tilpasse

|Hva vil du gjøre|Hvordan du gjør det|Merknader|
|----|------------|-------|
|Flytte noe, for eksempel et felt, en kolonne i en liste, en flis, en handling eller en del|Pek hvor som helst på det du vil flytte, og dra det til den nye plasseringen. Plasseringen angis enten av en tykk vannrett eller loddrett linje.<br /><br />![Kan ikke flytte hit-ikon](media/personalization-cannot-move-here.png "Tilpassingsmodus – Kan ikke flytte hit-ikon") angir at du ikke kan flytte elementet til den valgte lokasjonen.|Deler er ytterligere inndelinger eller områder på en side som for eksempel inneholder flere felt, en annen side, et diagram eller fliser.<br /><br />Hvis du vil ha mer informasjon om handlingstilpassing, se [neste del](ui-personalization-user.md#Actions). |
|Skjule noe, for eksempel et felt, en kolonne i en liste, en flis eller en del.|Velg pilspissen, og velg <b>Skjul</b>.|Hvis feltet du skjuler, også vises i hurtigfaneoverskriften når hurtigfanen er skjult, vil feltet ikke lenger vises der.|
|Legge til et felt eller en kolonne.|I banneret <b>Tilpassing</b> velger du <b>Mer</b>, og velg deretter <b>Felt</b>.<br /></br>Ruten <b>Legg til felt på side</b> åpnes til høyre. Den viser feltene du kan legge til på siden.<br /><br />Hvis du vil legge til et felt, drar du det fra ruten til den ønskede plasseringen. Plasseringen angis enten av en tykk vannrett eller loddrett linje.|Hver side inneholder et forhåndsdefinert sett med felt som du kan vise. Bruk denne fremgangsmåten for å legge til felt og kolonner som ikke er vist tidligere, eller for å vise feltene du har skjult.|
|Vise et felt i overskriften i en hurtigfane når hurtigfanen er skjult.|Velg pilspissen, og velg <b>Vis når skjult</b>. <br /> <br />Hvis du ikke ser dette alternativet, er det allerede angitt. I dette tilfellet, hvis du slutte å vise feltet i hurtigfaneoverskriften, velger du <b>Vis alltid</b>.|*Hurtigfane* er ordet som brukes for en gruppe med felt som vises under en felles overskrift. Bruk <b>Vis når skjult</b>-alternativet for å vise de viktigste feltene. Hvis du velger et felt i overskriften, åpnes hurtigfanen med fokus på det valgte feltet.<br /><br />Dette alternativet er bare aktuelt hvis en side har mer enn én hurtigfane. Hvis det bare er én hurtigfane, kan den ikke bli skjult, og <b>Vis når skjult</b> er ikke tilgjengelig.|
|Angi at et felt skal vises bare når du velger **Vis mer**.|Velg pilspissen, og velg <b>Vis under Vis mer</b>. <br /> <br />Hvis du ikke ser <b>Vis under Vis mer</b>-alternativet, er det allerede angitt. I dette tilfellet, for å vise et felt alltid og ikke bare når du velger **Vis mer**, velger du <b>Vis alltid</b>.||
|Endre den fryste ruten i en liste til en annen kolonne. |Velg pilspissen for kolonnen som du vil ha som den siste kolonnen for den fryste ruten, og velg deretter <b>Sett Frys rute</b>.<br /><br/>Hvis du vil sette den fryste ruten tilbake til den opprinnelige utformede plasseringen, velger du pilspissen for den gjeldende kolonnen for fryst rute og velger <b>Fjern Frys rute</b>. Obs!  Du kan ikke fjerne den fryste ruten.|Den fryste ruten angir kolonnene som alltid vises til venstre, selv når du ruller vannrett.|  
|Endre kolonnebredden.|Dra i kolonnens høyre ramme i raden for tabelloverskriften. <br /><br />Dobbeltklikk høyre rammen for å maksimere kolonnebredden slik at den passer til den lengste tekstlinjen i kolonnen.||
|Du kan hoppe over et feltet når du trykker Enter.|Velg pilspissen ved siden av feltet eller kolonneoverskriften i en liste, og velg **Utelat fra hurtigoppføring**. <br /><br /> Hvis du ikke se dette alternativet, er feltet allerede definert til å hoppes over. I dette tilfellet, hvis du ikke vil hoppe over i feltet, velger du **Ta med i hurtigoppføring**. |Se [Raskere dataregistrering ved hjelp av hurtigoppføring](ui-enter-data.md#QuickEntry)|

## <a name="Actions"></a>Tilpasse handlinger

Du kan tilpasse handlingsfeltet som er plassert øverst på siden, som indikert av det uthevede området i illustrasjonen nedenfor.

![Tilpasse handlingsfeltet](media/personalize-action-bar.png "Tilpasse handlingsfeltet")

Tilpasning lar deg bestemme hvilke handlinger som skal vises i handlingsfeltet, og hvor de skal vises. Du kan vise, skjule eller flytte individuelle handlinger eller handlingsgrupper. Tilpassing av handlingsfeltet gjøres mye på samme måte som med andre arbeidsområdeelementer. Nøyaktig hva du kan gjøre med en handling eller gruppe, avhenger imidlertid av hvor handlingen eller gruppen er plassert i handlingsfeltet. Den beste måten å finne det ut på, er bare å prøve ut ting og la skjermbildet veilede deg. De følgende delene forklarer noen av nyansene i tilpassing av handlingsfeltet.

### <a name="action-bar-overview"></a>Oversikt over handlingsfeltet

Det finnes noen begreper du bør være kjent med for å bedre forstå handlingstilpasning: *handlingsgruppe* og *forfremmet kategori*.  

En *handlingsgruppe* er et element som utvides for å vise andre handlinger eller grupper. I eksemplet nedenfor er **Bokføring** en handlingsgruppe.

En *forfremmet kategori* er en handlingsgruppe som vises mellom de to loddrette linjene `|` i handlingsfeltet. Disse kategoriene inneholder vanligvis de mest vanlige handlingene, slik at du kan finne dem raskt. I eksemplet nedenfor er **Frigi**, **Bokføring**, **Faktura** og **Naviger** forfremmede kategorier.

![Tilpasse handlingsfeltgruppe](media/personalize-action-bar-group-clip.png "Tilpasse handlingsfeltgruppe ")

### <a name="to-remove-hide-and-show-actions-and-groups"></a>Fjerne, skjule og vise handlinger og grupper

For å vise eller skjule en handling eller handlingsgruppe, velger du den og velger fra en av følgende alternativer:

|Alternativ|Hva det gjør|
|------|------------
|**Fjern**|Dette alternativet vises hvis den valgte handlingen også vises et annet sted i handlingsfeltet. Hvis du velger dette alternativet, slettes handlingen fra den valgte lokasjonen, slik at den ikke lenger vises. Handlingen eller handlingsgruppen forblir på de andre lokasjonene. |
|**Skjul**|Dette alternativet vises hvis handlingen eller handlingsgruppen ikke finnes et annet sted i handlingsfeltet. Som med **Fjern** forsvinner handlingen eller handlingsgruppen fra handlingsfeltet hvis du velger dette alternativet. Med i modusen tilpasning vises handlingen eller handlingsgruppen fremdeles på den aktuelle plasseringen, bortsett fra at den vises nedtonet.|
|**Vis**|Dette alternativet vises hvis handlingen eller handlingsgruppen har vært skjult tidligere (nedtonet). Valg av dette alternativet gjør at handlingen eller handlingsgruppen vises i handlingsfeltet.|

### <a name="to-move-actions-and-action-groups"></a>Flytte handlinger og handlingsgrupper

For å flytte en handling eller handlingsgruppe dra og slipp den til ønsket plassering, på samme måte som felt og kolonner.

Hvor du kan dra handlinger eller handlingsgrupper, vises av en vannrett linje mellom to handlinger eller en ramme rundt en handlingsgruppe.

- Du kan flytte individuelle handlinger til de forfremmede kategoriene, men du kan ikke endre rekkefølgen på handlingene i kategorien.
- Du kan ikke flytte en handlingsgruppe til en forfremmet kategori.
- Hvis du vil flytte en handling eller handlingsgruppe til en annen handlingsgruppe som er tom, drar du handlingen eller handlingsgruppen til den nye gruppen og slipper den i boksen **Slipp en handling her**.

## <a name="additional-points-of-interest"></a>Flere interessepunkter

Nedenfor følger noen tips som hjelper deg med å forstå tilpasning bedre.

- Når du endrer en kortside som du åpner fra en liste, trer endringene i kraft på alle poster som du åpner fra denne listen. Anta for eksempel at du åpner en bestemt kunde fra kundelistesiden og deretter tilpasser siden ved å legge til et felt. Når du åpner andre kunder fra listen, vises også feltet du har lagt til.
- Endringer som du utfører, trer i kraft på alle rollesentrene. Hvis du for eksempel gjør en endring i kundelisten når Rollesenter er satt til Forretningsleder, vises også endringen i kundelisten når Rollesenter er angitt som Ordrebehandler.
- Endringer av en side i en rute trer i kraft på siden der den vises.  
- Du kan bare legge til felt og kolonner fra en forhåndsdefinert liste, som er basert på siden. Du kan ikke opprette nye.

## <a name="to-clear-personalization"></a>Fjerne tilpassing

Du ønsker kanskje på et gitt tidspunkt å angre noen eller alle tilpasningsendringene du har foretatt på en side over tid. Du gjør dette ved å velge banneret **Tilpassing**, **Mer**, **Fjern tilpasning**, og deretter velger du et av alternativene nedenfor. Vær oppmerksom på at fjerning av tilpasning ikke kan angres.

|Alternativ|Hva det gjør|
|------|------------
|Bare handlinger|Fjerner alle tilpasningsendringer du har gjort for handlingfeltet på siden.|
|Alle unntatt handlinger|Fjerner alle tilpasningsendringer du har gjort for handlingfeltet på siden, unntatt de i handlingsfeltet. Dette inkluderer endringer i felt, kolonner, deler og ruter. |
|Alle|Fjerner alle tilpassingsendringene du har gjort på siden, slik at den ser ut slik den gjorde opprinnelig. Dette inkluderer endringer i handlingsfelt, kolonner, deler og ruter.|

## <a name="see-also"></a>Se også

[Administrere tilpasning](ui-personalization-manage.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
