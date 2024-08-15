---
title: Tilpasse sider
description: Finn ut hvordan du kan tilpasse brukergrensesnittet og tilpasse arbeidsområdet slik at det passer til arbeidsmåten og personlige preferanser i Business Central.
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 01/15/2024
ms.author: jswymer
---
# <a name="personalize-your-workspace"></a>Tilpass arbeidsområdet

Du kan tilpasse arbeidsområdet til å passe arbeid og behov. Endre sider slik at de bare viser den informasjonen du trenger, der du trenger den. Personalisering påvirker bare arbeidsområdet. Det endrer ikke måten andre arbeider på. Du kan tilpasse alle typer sider, inkludert [rollesenter](ui-change-basic-settings.md#role-center)-siden.

> [!NOTE]
> På grunn av restriksjoner på utformingsmuligheter i nettklienten er det for øyeblikket ikke mulig å tilpasse kontrollene innenfor syntaksen `grid` og `fixed`.
Det gjelder alle utformingsmoduser, ikke bare tilpassing.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Du kan gjøre ulike endringer, for eksempel flytte eller skjule felt, kolonner, handlinger og hele deler og legge til nye felter. Det meste av tilpasningen må utføres ved først å aktivere **Tilpasning**-banneret. Du kan foreta enkle justeringer, for eksempel kolonnebredden, umiddelbart i alle lister.

> [!NOTE]
> Administratorer kan gjøre samme oppsettendringer som brukerne ved å tilpasse profilen (rollen) som flere brukere er tilordnet. Hvis du vil vite mer om sider for roller, går du til [Tilpass sider for roller](ui-personalization-manage.md)<br /><br />
Administratorer kan også overstyre eller deaktivere brukeres tilpasning, og de kan definere hvilke funksjoner som til og med brukere kan se i alle eller bestemte selskaper. Hvis du vil ha mer informasjon, kan du se [Tilpasse Business Central](ui-customizing-overview.md).

## <a name="video-and-training"></a>Video

Følgende video viser noen av måtene du kan tilpasse rollesenteret på.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## <a name="change-the-width-of-a-column"></a>Endre kolonnebredden

Det er enkelt å endre størrelse på kolonner i en liste. Dra grensen mellom to kolonner til venstre eller høyre.  

1. I toppteksten av en liste velger og drar du grensen mellom to kolonner.
2. Du kan også dobbeltklikke grenselinjen mellom to kolonner for å tilpasse bredden på kolonnen automatisk. Bredden justeres til den optimale størrelsen for lesbarhet.

På samme måte som med andre personlige tilpasninger lagres endringene du gjør i kolonnebredden, på kontoen og følger deg uansett hvilken enhet du logger på.

## <a name="start-personalizing-by-using-the-personalization-mode"></a>Starte tilpasning ved hjelp av tilpassingsmodus

1. Åpne en side som du vil tilpasse.
1. Øverst til høyre velger du ikonet ![Innstillinger.](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter") og deretter **Tilpass**-handlingen.

    Banneret **Tilpassing** vises øverst, noe som betyr at du kan begynne å gjøre endringer.

    > [!NOTE]
    > Hvis du vil navigere under tilpasning, trykker du <kbd>Ctrl</kbd>+<kbd>Klikk</kbd> på en handling hvis den utheves av pilhodet.

    Hvis du ser ![Tilpassingslås](media/personalization-lock-icon.png "Tilpass lås") eller ![Tilpassing sperret](media/personalization-blocked-icon.png "Tilpassing blokkert") i banneret, kan du ikke tilpasse siden. Hvis du vil ha mer informasjon, kan du se [Hvorfor en side er låst fra tilpasning](ui-personalization-locked.md).

1. Hvis du vil endre et grensesnittelement, peker du på elementet, for eksempel en handling, et felt eller en del. Elementet utheves umiddelbart med en pilspiss eller kantlinje. Velg elementet, og velg deretter enten **Flytt**, **Fjern**, **Skjul**, **Vis**, **Vis under Vis mer**, **Vis når skjult**, **Vis alltid**, **Sett/Fjern frys rute** eller **Inkluder/Utelat fra hurtigoppføring**, avhengig av type og tilstand for UI-elementet.
1. Hvis du vil legge til et felt, velger du **Felt**-handlingen. Fra ruten **Legg til felt på side** drar og slupper du et felt på ønsket plassering på siden.
1. Når du er ferdig med å endre oppsettet på én eller flere sider, velger du **Fullført**-knappen på banneret **Tilpasning**.

Hvis du vil ha mer informasjon, kan du se [Hva du kan tilpasse](#What).

## <a name="what-you-can-personalize"></a><a name="What"></a>Hva du kan tilpasse

|Hva vil du gjøre|Hvordan du gjør det|Merknader|
|----|------------|-------|
|Flytte noe, for eksempel et felt, en kolonne i en liste, en flis, en handling eller et annet sted på siden|Pek hvor som helst på det du vil flytte, og dra det til den nye plasseringen. En tykk vannrett eller loddrett linje angir plasseringen.<br /><br />![Kan ikke flytte hit-ikon](media/personalization-cannot-move-here.png "Tilpassingmodus - Kan ikke flytte hit-ikonet") angir at du ikke kan flytte elementet til den valgte lokasjonen.|Deler er ytterligere inndelinger eller områder på en side som for eksempel inneholder flere felt, en annen side, et diagram eller fliser.<br /><br />[Finn ut mer om hvordan du tilpasser handlinger](#Actions)<br>[Finn ut mer om hvordan du tilpasser deler](#Parts)|
|Skjule et element som vises, for eksempel et felt, en kolonne i en liste, flis, handling eller del.|Velg elementet, velg pilhodet, og velg deretter <b>Skjul</b>.|I personaliseringsmodus er skjulte handlinger nedtonet med kursiv tekst, og skjulte deler er skyggelagt med diagonale linjer. Skjulte felter og kolonner vises ikke direkte på siden, men du kan finne dem ved hjelp av ruten <b>Legg til felt på side</b> ([finn ut mer om arbeidsfelter](#fields)).<br><br>Når du avslutter tilpasningsmodus, forsvinner alle elementene fra visningen. Hvis feltet du skjuler, også vises i hurtigfaneoverskriften når hurtigfanen er skjult, vil feltet ikke lenger vises der.|
|Vise en handling eller del som er skjult|For et grått (skjult) element velger du pilspissen og deretter <b>Vis</b>.|Det skjulte elementet er igjen synlig.|
|Legg til et felt som er skjult|I banneret <b>Personalisering</b> velger du handlingen <b>+ Felt</b>.<br /></br>Ruten <b>Legg til felt på side</b> åpnes til høyre på siden. Hvis du velger et felt i ruten, vises den skjulte plasseringen på siden.<br /><br />Hvis du vil legge til et felt, drar du det fra ruten eller fra den skjulte plasseringen til den ønskede plasseringen. Plasseringen angis av en tykk vannrett eller loddrett linje.<br><br> En annen måte er å velge pilspissen på feltets skjulte plassering og velge **Vis**. |Hver side inneholder et forhåndsdefinert sett med felt som du kan vise.<br /><br />[Finn ut mer om å jobbe med felt](#fields) |
|Vise et felt i overskriften i en hurtigfane når den er skjult.|Velg pilspissen, og velg deretter <b>Vis når skjult</b>. <br /> <br />Hvis du ikke ser dette alternativet, er det allerede angitt. I dette tilfellet, hvis du vil slutte å vise feltet i hurtigfaneoverskriften, velger du <b>Vis alltid</b>.|*Hurtigfane* er ordet som brukes for en gruppe med felt som vises under en felles overskrift. Bruk <b>Vis når skjult</b>-alternativet for å vise de viktigste feltene. Hvis du velger et felt i overskriften, åpnes hurtigfanen med fokus på det valgte feltet.<br /><br />Dette alternativet er bare aktuelt hvis en side har mer enn én hurtigfane. Hvis det bare er én hurtigfane, kan den ikke bli skjult, og <b>Vis når skjult</b> er ikke tilgjengelig.|
|Angi at et felt skal vises bare når du velger **Vis mer**.|Velg pilspissen, og velg deretter <b>Vis under Vis mer</b>.|Hvis du ikke ser <b>Vis under Vis mer</b>-alternativet, er feltet allerede angitt. I dette tilfellet, for å vise et felt alltid og ikke bare når du velger **Vis mer**, velger du <b>Vis alltid</b>.|
|Endre om et felt kan redigeres eller ikke.|Velg feltet, velg pilspissen i feltet, og velg deretter <b>Lås redigering</b> for å hindre endring av feltets verdi, eller <b>Lås opp redigering</b> for å tillate endring av feltets verdi.|Du kan bare låse opp felter som du tidligere har låst selv. Noen felt er låst som standard, enten som standard eller av en profiladministrator som har [tilpasset siden](ui-personalization-manage.md). Disse feltene kan ikke låses opp.|
|Endre den fryste ruten i en liste til en annen kolonne. |Velg pilspissen for kolonnen som du vil ha som den siste kolonnen for den fryste ruten, og velg deretter <b>Sett Frys rute</b>.<br /><br/>Hvis du vil sette den fryste ruten tilbake til den opprinnelige utformede plasseringen, velger du pilspissen for den gjeldende kolonnen for fryst rute og velger <b>Fjern Frys rute</b>. Obs! Du kan ikke fjerne den fryste ruten.|Den fryste ruten angir kolonnene som alltid vises til venstre på listen, selv når du ruller vannrett.|  
|Du kan hoppe over et feltet når du trykker Enter.|Velg pilspissen ved siden av feltet, eller kolonneoverskriften i en liste, og velg **Utelat fra hurtigoppføring**.  | Hvis du ikke ser **Utelat fra hurtigoppføring**, er feltet allerede hoppet over. I dette tilfellet, hvis du ikke vil hoppe over i feltet, velger du **Ta med i hurtigoppføring**.<br><br>[Finn ut mer om hurtigoppføring](ui-enter-data.md#QuickEntry)|
|Endre rekkefølge på og fjerne visninger som representerer filtrerte lister.|Velg pilspissen ved siden av en visning, og velg deretter **Flytt**, **Fjern** eller **Skjul**.|[Lære mer om hvordan du lagrer og tilpasser listevisninger](ui-views.md)|  
|Legg til en ny handling på en side eller rapport i rollesenteret.|Velg bokmerkeikonet fra målsiden, rapportforespørselssiden eller Fortell meg-vinduet.|[Finn ut mer om bokmerkesider og rapporter](ui-bookmarks.md)|
|Start alltid en liste som vist eller skjult|Velg knappen **Vis alle** eller **Skjul alle** øverst til venstre i listen. Du kan også velge handlingen **Vis alt** eller **Skjul alt** i menyen for den første kolonnen. |Gjelder for skjuling av hierarkilister|

## <a name="personalize-action-bar-and-menus"></a><a name="Actions"></a>Tilpasse handlingsraden og menyene

Tilpasning lar deg bestemme hvilke handlinger som skal vises i navigasjons- og handlingsrader samt rollesentre, og hvor de skal vises. Du kan vise, skjule eller flytte individuelle handlinger eller handlingsgrupper.

Følgende video viser hvordan du kan tilpasse handlinger på sider og i rollesentre.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

Tilpassing av navigasjons- og handlingsfeltene gjøres mye på samme måte som med andre grensesnittelementer. Hva du kan gjøre med en handling eller gruppe, avhenger imidlertid av hvor handlingen eller gruppen er plassert. Den beste måten å finne det ut på, er å gå inn i tilpasningsmodus og deretter la pilhodene veilede deg.

Det finnes noen begreper du bør være kjent med for å bedre forstå handlingstilpasning: *handlingsgruppe* og *forfremmet kategori*.  

En *handlingsgruppe* er et element som utvides for å vise andre handlinger eller grupper. Eksempelvis, på siden **Salgsordrer**, er én handlingsgruppe **Funksjoner** som vises når du velger handlingen **Handlinger**.

En *forfremmet kategori* er en handlingsgruppe som vises før den loddrette linjen `|` i handlingsfeltet. Disse kategoriene inneholder vanligvis de mest vanlige handlingene, slik at du kan finne dem raskt. Eksempelvis, på **Salgsordrer**-siden, er handlingene **Ordre**, **Frigi** og **Bokføring** forfremmede kategorier.

> [!NOTE]  
> Hvis du vil fjerne personlig tilpasning, merker du av pilhodet rundt delens utformingsmeny og velger **Fjern personlig tilpasning**.

### <a name="remove-hide-and-show-actions-and-action-groups"></a>Fjerne, skjule og vise handlinger og handlingsgrupper

Når du vil vise eller skjule en handling, definerer alternativene under pilspissen hva du kan gjøre, avhengig av handlingens status. 

1. Velg pilspissen for en handling eller handlingsgruppe.
2. Velg blant et av følgende alternativer:

|Alternativ|Hva det gjør|
|------|------------|
|**Fjern**|Dette alternativet vises hvis den valgte handlingen også vises et annet sted i navigasjons- eller handlingsfeltet. Hvis du velger dette alternativet, slettes handlingen fra den valgte lokasjonen, slik at den ikke lenger vises. Handlingen eller handlingsgruppen forblir på de andre lokasjonene. |
|**Skjul**|Dette alternativet vises hvis handlingen eller handlingsgruppen ikke finnes et annet sted i navigasjons- eller handlingsfeltet. Som med **Fjern** forsvinner handlingen eller handlingsgruppen fra navigasjons- eller handlingsfeltet hvis du velger dette alternativet. Med i modusen tilpasning vises handlingen eller handlingsgruppen fremdeles på den aktuelle plasseringen, bortsett fra at den vises nedtonet.|
|**Vis**|Dette alternativet vises hvis handlingen eller handlingsgruppen er skjult (nedtonet). Valg av dette alternativet gjør at handlingen eller handlingsgruppen vises i navigasjons- eller handlingsfeltet.|

### <a name="move-actions-and-action-groups"></a>Flytte handlinger og handlingsgrupper

Hvor du kan dra handlinger eller handlingsgrupper, vises av en vannrett linje mellom to handlinger eller en ramme rundt en handlingsgruppe. Følgende begrensninger finnes:

- Du kan flytte individuelle handlinger til de forfremmede kategoriene, men du kan ikke endre rekkefølgen på handlingene i kategorien.
- Du kan ikke flytte en handlingsgruppe til en forfremmet kategori.

1. For å flytte en handling eller handlingsgruppe dra og slipp den til ønsket plassering, på samme måte som med felt og kolonner.
2. Hvis du vil flytte en handling eller handlingsgruppe til en annen handlingsgruppe som er tom, drar du handlingen eller handlingsgruppen til den nye gruppen og slipper den i boksen **Slipp en handling her**.

### <a name="about-the-automate-menu"></a>Om Automatiser-menyen

- Du kan ikke skjule eller flytte **Automatiser**-menyen eller undermenyen og handlingene på **Power Automate**.
- Du kan flytte flytprosesser som er inkludert under elementet **Automatiser**, men du kan ikke skjule dem ved hjelp av tilpasning. Hvis du flytter flyten, kopierer du flyten til målet, men den fjernes ikke fra elementet **Automatiser**.

> [!TIP]
> Som administrator kan du skjule **Automatiser**-elementet fra brukere. Finn ut mer under [Definer Power Automate-integrering](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="personalize-parts"></a><a name="Parts"></a>Tilpasse deler

Pek på eller velg <kbd>Alt</kbd>+<kbd>Pil opp</kbd>Deler er områder på en side som vanligvis er satt sammen av flere felter, diagrammer eller annet innhold. En del viser en farget ramme når du fokuserer på delen. En startside for rollesenter har for eksempel flere deler. På grunn av sin veldefinerte grense, kan du tilpasse hele delen og innholdet i den.

- Hvis du vil flytte en del, drar og slipper du den til ønsket plassering. En farget linje angir gyldige posisjoner på skjermen. Faktabokser kan for eksempel bare flyttes ved siden av andre faktabokser i faktaboksruten.
- Du kan skjule en del ved å velge alternativet **Skjul** under pilspissen.
- Når du begynner å tilpasse eller navigere til en ny side, vises eventuelle deler som er skjult, på siden med spesielle effekter for å angi at de er skjult. Du kan oppheve skjulingen av den delen ved å velge alternativet **Vis** under pilspissen.

Du kan fjerne alle tilpassingsendringer du har gjort i én del, ved å velge alternativet **Fjern tilpassing** under delens pilspiss. Når du fjerner tilpassingen av en del, påvirkes bare endringer i innholdet i delen, ikke plasseringen eller synligheten for delen på siden.  

## <a name="work-with-fields-and-columns"></a><a name="fields"></a>Arbeide med felter og kolonner

Når du tilpasser en side, bruker du **Legg til felt på side**-ruten for å inkludere felter eller kolonner på siden som for øyeblikket er skjult fra visning. Du åpner denne ruten ved å velge handlingen **+ Felt** nær toppen av siden. I motsetning til andre skjulte elementer angis ikke skjulte felt på selve siden i tilpasningsmodus. Du kan imidlertid identifisere skjulte felt ved hjelp av ruten **Legg til felt på side** .

Her er noen generelle retningslinjer du kan følge når du bruker **Legg til felt på side**-ruten:

- Som standard viser ruten alle skjulte felter. Skjulte felter er merket med ![ikonet Viser det skjulte feltet](media/hidden-icon.png "Viser ikonet for skjult felt").
- Du kan filtrere listen for å vise andre felter, for eksempel de som vises på siden, ved å velge knappen **Anbefalte felter** over listen og velge et filteralternativ. Navnet på knappen endres basert på filteralternativet du velger.
  
   :::image type="content" source="media/personlaization-filter.svg" alt-text="Viser filterknappen i ruten Legg til et felt i tilpasningsmodus.":::
- Når du velger et felt i listen, utheves plasseringen på siden. Hvis feltet for øyeblikket er skjult, vises plasseringen med vilje i en skyggelagt tilstand. 
- Hvis du vil ha flere detaljer om et felt i listen, peker du på det eller velger <kbd>Alt</kbd>+<kbd>Pil opp</kbd> for å vise et verktøytips.
- Feltene som er tilgjengelige i ruten **Legg til felt på side**, bestemmes av utvikleren av siden og kildetabellen, eller av en profiladministrator som har [tilpasset siden](ui-personalization-manage.md). Du kan ikke opprette nye.
- Noen sider har flere sidefelt som tilordnes til samme kildetabell. Ruten viser begge/alle disse sidefeltene uavhengig av hverandre. Å vise/skjule/flytte disse feltene er også uavhengig uten at det ene påvirker det andre.

### <a name="add-a-field-so-its-visible-on-the-page"></a>Legg til et felt slik at det vises på siden

Fra **Legg til felt på side**-ruten er det to måter å inkludere et felt som for øyeblikket er skjult, på siden:

- Dra feltet til ønsket posisjon. En tykk vannrett eller loddrett linje angir målplasseringen.
- Velg feltet i listen, gå deretter til det skyggelagte feltet på siden, og velg **Vis**-alternativet.

> [!NOTE]
> Noen av feltene du legger til, kan ikke redigeres på siden når du er ferdig med tilpasningen. Disse feltene er opprinnelig utformet på denne måten, eller en administrator har [tilpasset](ui-personalization-manage.md) siden for å hindre deg i å redigere dem.

## <a name="clear-personalization"></a>Fjern personlig tilpasning

Du ønsker kanskje på et gitt tidspunkt å angre noen eller alle tilpasningsendringene du har foretatt på en side over tid.

1. På banneret **Tilpasning** velger du handlingen **Fjern tilpassing**.
2. Velg ett av følgende alternativene.  

> [!CAUTION]
> Fjerning av tilpasning ikke kan angres.

|Alternativ|Hva det gjør|
|------|------------
|**Bare navigasjonsmenyen**|Fjerner alle tilpassingsendringer du har gjort på navigasjonsmenyen som deles på tvers av rollesenteret og andre sider. Slike endringer omfatter eventuelle nye handlinger som er lagt til som bokmerker, og endringer i koblinger og grupper på menyen.|  
|**Bare handlinger**|Fjerner alle tilpassingsendringer du har gjort for navigasjons- eller handlingsfeltet på siden.|
|**Bare felter og kolonner**|Fjerner alle tilpassingsendringer du har gjort for handlingfeltet på siden, unntatt endringene i navigasjons- eller handlingsfeltet. Slike endringer inkluderer endringer i felter, kolonner, deler og ruter. |
|**Alle**|Fjerner alle tilpassingsendringene du har gjort på siden, slik at den ser ut slik den gjorde opprinnelig. Slike endringer inkluderer endringer i navigasjons- eller handlingsfelt, kolonner, deler og ruter.|

## <a name="tips-and-other-points-of-interest"></a>Tips og andre interessepunkter

Nedenfor følger noen tips som hjelper deg med å forstå tilpasning bedre.

- Når du endrer en kortside som du åpner fra en liste, trer endringene i kraft på alle poster som du åpner fra denne listen. Anta for eksempel at du åpner en bestemt kunde fra kundelistesiden og deretter tilpasser siden ved å legge til et felt. Når du åpner andre kunder fra listen, vises også feltet du har lagt til.
- Endringer som du utfører, påvirker alle rollesentrene. Hvis du for eksempel gjør en endring i kundelisten når Rollesenter er satt til Forretningsleder, vises også endringen på siden **Kunder** når rollesenteret er angitt til Ordrebehandler.
- Endringer av en side i en rute trer i kraft på siden der den vises.  
- Du kan ikke tilpasse en side som er i [analysemodus](analysis-mode.md). **Analyse**-bryteren er deaktivert. Hvis du bytter til personaliseringsmodus mens siden er i analysemodus, deaktiveres analysemodus automatisk. 
- Noen sider har flere sidefelt som tilordnes til samme kildetabell. Ruten viser begge/alle disse sidefeltene uavhengig av hverandre. Å vise/skjule/flytte disse feltene er også uavhengig uten at det ene påvirker det andre.
- Hvis en del eller gruppe er skjult, vises skyggefelter fortsatt i den, men du kan ikke dra og slippe eller legge til/vise feltet før du har gjort gruppen/delen synlig.

## <a name="see-also"></a>Se også

[Tilpass sider for profiler](ui-personalization-manage.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
