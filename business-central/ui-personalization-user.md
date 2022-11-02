---
title: Tilpasse sider (inneholder video)
description: Finn ut hvordan du kan tilpasse brukergrensesnittet og tilpasse arbeidsområdet slik at det passer til arbeidsmåten og personlige preferanser i Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017
ms.date: 10/11/2022
ms.author: bholtorf
ms.openlocfilehash: 436adf8dcfd9d5825530a1a51f5ed0efad7d9b7c
ms.sourcegitcommit: 902834e76460d751a345485c66fd2831066b396b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716574"
---
# <a name="personalize-your-workspace"></a>Tilpasse arbeidsområdet

Du kan tilpasse arbeidsområdet til å passe arbeid og behov. Endre sider slik at de bare viser den informasjonen du trenger, der du trenger den. Tilpasningsendringene påvirker bare hva *du* ser, ikke hva andre brukere ser.

Du kan tilpasse alle typer sider, inkludert Rollesenter-siden. Se [Rollesenter](ui-change-basic-settings.md#role-center) hvis du vil ha mer informasjon om rollesentre.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Du kan gjøre ulike endringer, for eksempel flytte eller skjule felt, kolonner, handlinger og hele deler og legge til nye felter. Det meste av tilpasningen må utføres ved først å aktivere **Tilpasning**-banneret. Du kan foreta enkle justeringer, for eksempel kolonnebredden, umiddelbart i alle lister.

> [!NOTE]
> Administratorer kan utføre samme oppsettendringer som brukerne ved å tilpasse arbeidsområdet for en profil som flere brukere er tilordnet. Hvis du vil ha mer informasjon, kan du se [Tilpasse sider for roller](ui-personalization-manage.md).<br /><br />
Administratorer kan også overstyre eller deaktivere brukeres tilpasning, og de kan definere hvilke funksjoner som til og med brukere kan se i alle eller bestemte selskaper. Hvis du vil ha mer informasjon, kan du se [Tilpasse Business Central](ui-customizing-overview.md).

## <a name="video-overview"></a>Videooversikt
Følgende video viser noen av måtene du kan tilpasse rollesenteret på.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## <a name="to-change-the-width-of-a-column"></a>Endre kolonnebredden

Det er enkelt å endre størrelse på kolonner i en liste. Dra grensen mellom to kolonner til venstre eller høyre.  

1. I toppteksten av en liste velger og drar du grensen mellom to kolonner.
2. Du kan også dobbeltklikke grenselinjen mellom to kolonner for å tilpasse bredden på kolonnen automatisk. Bredden justeres til den optimale størrelsen for lesbarhet.

På samme måte som med andre personlige tilpasninger lagres endringene du gjør i kolonnebredden, på kontoen og følger deg uansett hvilken enhet du logger på.

## <a name="to-start-personalizing-a-page-through-the-personalizing-banner"></a>Slik tilpasser du en side med **Tilpasse**-banneret

1. Åpne en side som du vil tilpasse.
2. Øverst til høyre velger du ikonet ![Innstillinger.](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter") og deretter **Tilpass**-handlingen.

    Banneret **Tilpassing** vises øverst, noe som betyr at du kan begynne å gjøre endringer.

    > [!NOTE]
    > Hvis du vil navigere under tilpasning, trykker du CTRL+klikk på en handling hvis den utheves av pilhodet.

    Hvis du ser ![Tilpassingslås](media/personalization-lock-icon.png "Tilpass lås") eller ![Tilpassing sperret](media/personalization-blocked-icon.png "Tilpassing blokkert") i banneret, kan du ikke tilpasse siden. Hvis du vil ha mer informasjon, kan du se [Hvorfor en side er låst fra tilpasning](ui-personalization-locked.md).

3. Hvis du vil legge til et felt, velger du **Felt**-handlingen.
4. Fra ruten **Legg til felt på side** drar og slupper du et felt på ønsket plassering på siden.
5. Hvis du vil endre et grensesnittelement, peker du på elementet, for eksempel en handling, et felt eller en del. Elementet utheves umiddelbart med en pilspiss eller kantlinje.
6. Velg elementet, og velg deretter enten **Flytt**, **Fjern**, **Skjul**, **Vis**, **Vis under Vis mer**, **Vis når skjult**, **Vis alltid**, **Sett/Fjern frys rute** eller **Inkluder/Utelat fra hurtigoppføring**, avhengig av type og tilstand for UI-elementet. Hvis du vil ha mer informasjon, kan du se [Hva du kan tilpasse](#What).
7. Når du er ferdig med å endre oppsettet på én eller flere sider, velger du **Fullført**-knappen på banneret **Tilpasning**.

## <a name="what-you-can-personalize"></a><a name="What"></a>Hva du kan tilpasse

|Hva vil du gjøre|Hvordan du gjør det|Merknader|
|----|------------|-------|
|Flytte noe, for eksempel et felt, en kolonne i en liste, en flis, en handling eller en del|Pek hvor som helst på det du vil flytte, og dra det til den nye plasseringen. Plasseringen angis av en tykk vannrett eller loddrett linje.<br /><br />![Kan ikke flytte hit-ikon](media/personalization-cannot-move-here.png "Tilpassingmodus - Kan ikke flytte hit-ikonet") angir at du ikke kan flytte elementet til den valgte lokasjonen.|Deler er ytterligere inndelinger eller områder på en side som for eksempel inneholder flere felt, en annen side, et diagram eller fliser.<br /><br />Hvis du vil ha mer informasjon om handlingstilpassing, se [Tilpasse handlinger](ui-personalization-user.md#Actions). |
|Skjul noe, for eksempel et felt, en kolonne i en liste, en flis, en handling eller en del.|Velg pilspissen, og velg <b>Skjul</b>.|Elementet blir nedtonet når du er i tilpasningsmodus. Hvis feltet du skjuler, også vises i hurtigfaneoverskriften når hurtigfanen er skjult, vil feltet ikke lenger vises der.|
|Vis skjulte handlinger og deler.|For et grått (skjult) element velger du pilspissen og deretter <b>Vis</b>.|Det skjulte elementet er igjen synlig.|
|Legge til et felt eller en kolonne.|I banneret <b>Personalisering</b> velger du handlingen <b>+ Felt</b>.<br /></br>Ruten <b>Legg til felt på side</b> åpnes til høyre. Den viser feltene du kan legge til på siden.<br /><br />Hvis du vil legge til et felt, drar du det fra ruten til den ønskede plasseringen. Plasseringen angis av en tykk vannrett eller loddrett linje.|Hver side inneholder et forhåndsdefinert sett med felt som du kan vise. Bruk denne fremgangsmåten for å legge til felt og kolonner som ikke er vist tidligere, eller for å vise feltene du har skjult.|
|Vise et felt i overskriften i en hurtigfane når den er skjult.|Velg pilspissen, og velg deretter <b>Vis når skjult</b>. <br /> <br />Hvis du ikke ser dette alternativet, er det allerede angitt. I dette tilfellet, hvis du vil slutte å vise feltet i hurtigfaneoverskriften, velger du <b>Vis alltid</b>.|*Hurtigfane* er ordet som brukes for en gruppe med felt som vises under en felles overskrift. Bruk <b>Vis når skjult</b>-alternativet for å vise de viktigste feltene. Hvis du velger et felt i overskriften, åpnes hurtigfanen med fokus på det valgte feltet.<br /><br />Dette alternativet er bare aktuelt hvis en side har mer enn én hurtigfane. Hvis det bare er én hurtigfane, kan den ikke bli skjult, og <b>Vis når skjult</b> er ikke tilgjengelig.|
|Angi at et felt skal vises bare når du velger **Vis mer**.|Velg pilspissen, og velg deretter <b>Vis under Vis mer</b>. <br /> <br />Hvis du ikke ser <b>Vis under Vis mer</b>-alternativet, er det allerede angitt. I dette tilfellet, for å vise et felt alltid og ikke bare når du velger **Vis mer**, velger du <b>Vis alltid</b>.||
|Endre den fryste ruten i en liste til en annen kolonne. |Velg pilspissen for kolonnen som du vil ha som den siste kolonnen for den fryste ruten, og velg deretter <b>Sett Frys rute</b>.<br /><br/>Hvis du vil sette den fryste ruten tilbake til den opprinnelige utformede plasseringen, velger du pilspissen for den gjeldende kolonnen for fryst rute og velger <b>Fjern Frys rute</b>. Obs! Du kan ikke fjerne den fryste ruten.|Den fryste ruten angir kolonnene som alltid vises til venstre, selv når du ruller vannrett.|  
|Du kan hoppe over et feltet når du trykker Enter.|Velg pilspissen ved siden av feltet, eller kolonneoverskriften i en liste, og velg **Utelat fra hurtigoppføring**. <br /><br /> Hvis du ikke se dette alternativet, er feltet allerede definert til å hoppes over. I dette tilfellet, hvis du ikke vil hoppe over i feltet, velger du **Ta med i hurtigoppføring**. |Se [Raskere dataregistrering ved hjelp av hurtigoppføring](ui-enter-data.md#QuickEntry)|
|Endre rekkefølge på og fjerne visninger som representerer filtrerte lister.|Velg pilspissen ved siden av en visning, og velg deretter **Flytt**, **Fjern** eller **Skjul**.|Se [Lagre og tilpasse listevisninger](ui-views.md)|  
|Legg til en ny handling på en side eller rapport i rollesenteret.|Velg bokmerkeikonet fra målsiden, rapportforespørselssiden eller Fortell meg-vinduet.|Se [Bokmerke en side eller rapport i rollesenteret](ui-bookmarks.md)|
|Start alltid en liste som vist eller skjult|Velg knappen **Vis alle** eller **Skjul alle** øverst til venstre i listen. Du kan også velge handlingen **Vis alt** eller **Skjul alt** i menyen for den første kolonnen. |Gjelder for skjuling av hierarkilister|

## <a name="personalizing-the-action-bar-and-menus"></a><a name="Actions"></a>Tilpass handlingsraden og menyene

Tilpasning lar deg bestemme hvilke handlinger som skal vises i navigasjons- og handlingsrader samt rollesentre, og hvor de skal vises. Du kan vise, skjule eller flytte individuelle handlinger eller handlingsgrupper.

I lanseringsbølge 2 i 2022 gav deg flere måter å gjøre Business Central til din egen på. Følgende video viser hvordan du kan tilpasse handlinger på sider og i rollesentre.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

Tilpassing av navigasjons- og handlingsfeltene gjøres mye på samme måte som med andre grensesnittelementer. Hva du kan gjøre med en handling eller gruppe, avhenger imidlertid av hvor handlingen eller gruppen er plassert. Den beste måten å finne det ut på, er å gå inn i tilpasningsmodus og deretter la pilhodene veilede deg.

Det finnes noen begreper du bør være kjent med for å bedre forstå handlingstilpasning: *handlingsgruppe* og *forfremmet kategori*.  

En *handlingsgruppe* er et element som utvides for å vise andre handlinger eller grupper. Eksempelvis, på siden **Salgsordrer**, er én handlingsgruppe **Funksjoner** som vises når du velger handlingen **Handlinger**.

En *forfremmet kategori* er en handlingsgruppe som vises før den loddrette linjen `|` i handlingsfeltet. Disse kategoriene inneholder vanligvis de mest vanlige handlingene, slik at du kan finne dem raskt. Eksempelvis, på **Salgsordrer**-siden, er handlingene **Ordre**, **Frigi** og **Bokføring** forfremmede kategorier.

> [!NOTE]
> Du kan ikke tilpasse handlingslinjen som vises i deler på siden (for eksempel delen salgslinjer på **Ordre**-siden).

### <a name="to-remove-hide-and-show-actions-and-action-groups"></a>Fjerne, skjule og vise handlinger og handlingsgrupper

Når du vil vise eller skjule en handling, definerer alternativene under pilspissen hva du kan gjøre, avhengig av handlingens status. 

1. Velg pilspissen for en handling eller handlingsgruppe.
2. Velg blant et av følgende alternativer:

|Alternativ|Hva det gjør|
|------|------------
|**Fjern**|Dette alternativet vises hvis den valgte handlingen også vises et annet sted i navigasjons- eller handlingsfeltet. Hvis du velger dette alternativet, slettes handlingen fra den valgte lokasjonen, slik at den ikke lenger vises. Handlingen eller handlingsgruppen forblir på de andre lokasjonene. |
|**Skjul**|Dette alternativet vises hvis handlingen eller handlingsgruppen ikke finnes et annet sted i navigasjons- eller handlingsfeltet. Som med **Fjern** forsvinner handlingen eller handlingsgruppen fra navigasjons- eller handlingsfeltet hvis du velger dette alternativet. Med i modusen tilpasning vises handlingen eller handlingsgruppen fremdeles på den aktuelle plasseringen, bortsett fra at den vises nedtonet.|
|**Vis**|Dette alternativet vises hvis handlingen eller handlingsgruppen har vært skjult tidligere (nedtonet). Valg av dette alternativet gjør at handlingen eller handlingsgruppen vises i navigasjons- eller handlingsfeltet.|

### <a name="to-move-actions-and-action-groups"></a>Flytte handlinger og handlingsgrupper

Hvor du kan dra handlinger eller handlingsgrupper, vises av en vannrett linje mellom to handlinger eller en ramme rundt en handlingsgruppe. Følgende begrensninger finnes:

- Du kan flytte individuelle handlinger til de forfremmede kategoriene, men du kan ikke endre rekkefølgen på handlingene i kategorien.
- Du kan ikke flytte en handlingsgruppe til en forfremmet kategori.

1. For å flytte en handling eller handlingsgruppe dra og slipp den til ønsket plassering, på samme måte som med felt og kolonner.
2. Hvis du vil flytte en handling eller handlingsgruppe til en annen handlingsgruppe som er tom, drar du handlingen eller handlingsgruppen til den nye gruppen og slipper den i boksen **Slipp en handling her**.

## <a name="personalizing-parts"></a><a name="Parts"></a>Tilpasse deler

Deler er områder på en side som vanligvis er satt sammen av flere felter, diagrammer eller annet innhold. En del viser en farget ramme når du fokuserer på delen. En startside for rollesenter har for eksempel flere deler. På grunn av sin veldefinerte grense, kan du tilpasse hele delen og innholdet i den.

- Hvis du vil flytte en del, drar og slipper du den til ønsket plassering. En farget linje angir gyldige posisjoner på skjermen. Faktabokser kan for eksempel bare flyttes ved siden av andre faktabokser i faktaboksruten.
- Du kan skjule en del ved å velge alternativet **Skjul** under pilspissen.
- Når du begynner å tilpasse eller navigere til en ny side, vises eventuelle deler som er skjult, på siden med spesielle effekter for å angi at de er skjult. Du kan oppheve skjulingen av den delen ved å velge alternativet **Vis** under pilspissen.

Du kan fjerne alle tilpassingsendringer du har gjort i én del, ved å velge alternativet **Fjern tilpassing** under delens pilspiss. Når du fjerner tilpassingen av en del, påvirkes bare endringer i innholdet i delen, ikke plasseringen eller synligheten for delen på siden.  

## <a name="to-clear-personalization"></a>Fjerne tilpassing
Du ønsker kanskje på et gitt tidspunkt å angre noen eller alle tilpasningsendringene du har foretatt på en side over tid.

1. På banneret **Tilpasning** velger du handlingen **Fjern tilpassing**.
2. Velg ett av følgende alternativene.  

> [!CAUTION]
> Fjerning av tilpasning ikke kan angres.

|Alternativ|Hva det gjør|
|------|------------
|**Bare navigasjonsmenyen**|Fjerner alle tilpassingsendringer du har gjort på navigasjonsmenyen som deles på tvers av rollesenteret og andre sider. Slike endringer omfatter eventuelle nye handlinger som er lagt til som bokmerker, og endringer i koblinger og grupper på menyen.|  
|**Bare handlinger**|Fjerner alle tilpassingsendringer du har gjort for navigasjons- eller handlingsfeltet på siden.|
|**Bare felt, kolonner og deler**|Fjerner alle tilpassingsendringer du har gjort for handlingfeltet på siden, unntatt endringene i navigasjons- eller handlingsfeltet. Slike endringer inkluderer endringer i felter, kolonner, deler og ruter. |
|**Alle**|Fjerner alle tilpassingsendringene du har gjort på siden, slik at den ser ut slik den gjorde opprinnelig. Slike endringer inkluderer endringer i navigasjons- eller handlingsfelt, kolonner, deler og ruter.|

## <a name="other-points-of-interest"></a>Andre interessepunkter

Nedenfor følger noen tips som hjelper deg med å forstå tilpasning bedre.

- Når du endrer en kortside som du åpner fra en liste, trer endringene i kraft på alle poster som du åpner fra denne listen. Anta for eksempel at du åpner en bestemt kunde fra kundelistesiden og deretter tilpasser siden ved å legge til et felt. Når du åpner andre kunder fra listen, vises også feltet du har lagt til.
- Endringer som du utfører, trer i kraft på alle rollesentrene. Hvis du for eksempel gjør en endring i kundelisten når Rollesenter er satt til Forretningsleder, vises også endringen på siden **Kunder** når rollesenteret er angitt til Ordrebehandler.
- Endringer av en side i en rute trer i kraft på siden der den vises.  
- Du kan bare legge til felt og kolonner fra en forhåndsdefinert liste, som er basert på siden. Du kan ikke opprette nye.
- Elementet **Power Automate** på handlingsraden
  - Du kan ikke skjule eller flytte **Automatiser**-elementet eller **Power Automate**-underelementet og de tilhørende handlingene **Opprett en flyt** og **Administrer flytprosesser**.
  - Du kan flytte flytprosesser som er inkludert under elementet **Automatiser**, men du kan ikke skjule dem ved hjelp av tilpasning. Hvis du flytter flyten, kopierer du flyten til målet, men den fjernes ikke fra elementet **Automatiser**.

   > [!TIP]
   > Som administrator kan du skjule **Automatiser**-elementet fra brukere. Finn ut mer under [Definer Power Automate-integrering](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Tilpass sider for profiler](ui-personalization-manage.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
