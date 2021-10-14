---
title: Skrive inn data i Business Central
description: Det finnes flere generelle funksjoner som hjelper deg å registrere data raskere, enklere og mer nøyaktig. De grunnleggende prinsippene og de avanserte funksjonene beskrives her.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: decimal separator, data entry, focus
ms.date: 10/01/2021
ms.author: jswymer
ms.openlocfilehash: 1e6dbdd5880902c7b649464ad967f01cc599f37f
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588960"
---
# <a name="entering-data"></a>Skrive inn data

Det finnes flere generelle funksjoner som hjelper deg å registrere data raskere, enklere og mer nøyaktig. Grunnprinsippene og de avanserte funksjonene for å registrere data beskrives i denne artikkelen.  

Eksemplene i denne artikkelen bruker demonstrasjonsdataene.

## <a name="working-with-editable-fields"></a>Arbeide med felter som kan redigeres
Felter [!INCLUDE[prod_short](includes/prod_short.md)] kan inneholde ulike data som kan redigeres, som tekst eller valutabeløp. Redigerbare felter viser vanligvis en inndataboks der du kan skrive eller velge en verdi. Felter som ikke kan redigeres, vises vanligvis med en grå bakgrunn.   

Enkelte redigerbare felter har en velger som hjelper deg med å angi en verdi.  

<!-- TODO: Add illustrations or images of each picker -->
|**Plukker**        |**Slik hjelper den deg å angi en verdi**|
|------------------|------------------------------------|
|Datovelger       |Denne velgeren viser en kalender basert på gjeldende områdeinnstillinger. Den hjelper deg med å velge én dato.|
|Rullegardinliste          |Rullegardinlister gir et valg med faste verdier eller referanseoppføringer fra en annen tabell|
|Bryter eller avmerkingsboks|Enkelte felter gir en et enkelt valg med *Ja*- eller *Nei*-verdier. Bryteren brukes til å angi denne verdien og vises alltid som en avmerkingsboks i lister|
|Redigeringshjelp       |Enkelte felter gir egendefinerte velgere som er egnet til å slå opp og velge den beste verdien for det feltet, som et popup-vindu|

### <a name="modifying-a-field-value"></a>Endre en feltverdi

For å endre verdien i et felt må du først sette fokus på feltet. Du setter fokus ved å gjøre følgende handling:

- Bruk **Tab**-tasten. Handlingen velger hele verdien.
- Venstreklikk med musen eller en lignende inndataenhet. Denne handlingen vil bare velge hele feltverdien hvis feltet er i en liste.  

Når du samhandler med felt i brukergrensesnitt, velger [!INCLUDE[prod_short](includes/prod_short.md)] ofte hele feltverdien for å gjøre det enklere for deg å erstatte verdien.

Når hele feltverdien velges:
- Erstatt verdien ved å bare skrive for å angi en ny verdi. Hvis felter har en velger, kan du aktivere den ved å bruke **Alt + pil ned**-tastatursnarveien.
- Bruk **Delete**- eller **Tilbake**-tasten for å fjerne verdien.

Trykk på **F2**-tasten for å veksle mellom å velge hele feltverdien eller å sette markøren etter feltets verdi. Hvis du setter markøren på slutten av verdien, er det enklere for deg å tilføye til den eksisterende verdien.

Når markøren vises på slutten av feltverdien:
- Legg til verdien ved å skrive.
- Bruk tastene **Home**, **End**, **pil venstre** og **pil høyre** til å flytte markøren innenfor verdien. Hvis du redigerer et felt i en liste, settes fokuset på forrige felt hvis du trykker på **pil venstre**-tasten igjen når markøren er på begynnelsen av verdien. På samme måte settes fokuset på neste felt hvis du trykker på **pil høyre**-tasten igjen når markøren er på slutten av verdien.

> [!NOTE]
> Når du angir en verdi, vil Business Central bare kontrollere at den er gyldig etter at du klikker utenfor feltet eller setter fokus til et annet element, som det neste feltet.  

## <a name="keyboard-shortcuts"></a>Hurtigtaster

Det finnes en rekke hurtigtaster som du kan bruke til å utføre dataregistreringen raskere og uten mus. Disse hurtigtastene er spesielt nyttige med mange registreringer og repeterende skriveoppgaver.

Hvis du vil ha mer informasjon om snarveier, kan du se [Hurtigtaster](keyboard-shortcuts.md). Noen hurtigsnarveier beskrives i denne artikkelen.

## <a name="accelerating-data-entry-using-quick-entry"></a><a name="QuickEntry"></a>Raskere dataregistrering ved hjelp av hurtigoppføring

Hurtigoppføring er en funksjon som er beregnet på dataregistrering når du bruker tastaturet. Hurtigoppføring fungerer på felt (som på kortsider) og i lister (rader og kolonner). Det er en fordel når du gjør gjentakende skriveoppgaver som krever oppretting av flere poster i sekvens. Eksempler omfatter en bunke med ordre eller registrering av nye elementer.

Du kan bruke Tab-tasten til å gå fra ett felt på en side til det neste redigerbare feltet. En ulempe ved bruk av tabulatoren er at den alltid går fortløpende til neste felt. <!-- even if the field is non-editable or seldom filled it in.-->Med Hurtigoppføring kan du endre denne banen. Med Hurtigoppføring bruker du Enter-tasten til å navigere til bare de feltene du er interessert i. Hurtigoppføring hopper og felter som ikke kan redigeres, og felt du vanligvis ikke fyller ut. Du kan allerede ha oppdaget denne atferden på noen sider. Denne virkemåten er fordi feltene som skal inkluderes når du trykker på Enter, og de som skal hoppes over, er forhåndsangitt. Du kan tilpasse Hurtigoppføring ved å tilpasse arbeidsområdet og optimalisere hvordan du registrerer data på hver side.

### <a name="how-quick-entry-works"></a>Hvordan Hurtigoppføring fungerer

Hvert felt kan merkes som enten *inkludert i Hurtigoppføring* eller *ekskludert fra Hurtigoppføring*. Felter som inkluderes i Hurtigoppføring, er inkludert i banen når du trykker på Enter. Felter som er ekskludert fra Hurtigoppføring, er ikke det.

Når du er ferdig med å registrere data i et felt, trykker du på Enter for å bekrefte endringene og gå til neste felt. Hvis du vil reversere retningen og gå til forrige felt, trykker du på Skift+Enter. Hvis du vil ha mer informasjon om snarveier, kan du se [Hurtigtaster for hurtigoppføring for felt](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Tips og triks

Listen nedenfor inneholder litt informasjon om å bruke Hurtigoppføring.

- Det er tilgjengelig for alle redigerbare felt.
- Den fungerer også i kolonner og rader.
- Det hindrer ikke tilgang til andre elementer på en side, som handlinger. Disse elementene kan fremdeles nås ved å bruke Tab og Skift + Tab.  
- Det er ikke nødvendig at FastTabs er utvidet for at Hurtigoppføring skal fungere. Hvis det neste Hurtigoppføring-feltet er plasser i en skjult FastTab, utvides den FastTab-en automatisk og fokuserer på det valgte feltet. [!INCLUDE[prod_short](includes/prod_short.md)] husker at FastTab skal ekskluderes neste gang du besøker siden.  
- Hurtigoppføring fungerer uansett om felter er obligatoriske. Det kan derfor være lurt å sørge for at obligatoriske felt er inkludert i Hurtigoppføring.
- Som standard inkluderes de fleste feltene automatisk i Hurtigoppføring. Så i starten vil oppgaven din sannsynligvis eksludere felt fra Hurtigoppføring.

### <a name="to-change-quick-entry-fields"></a>Endre Hurtigoppføring-felt

Du bruker tilpasning til å konfigurere Hurtigoppføring på felt.

1. Start tilpasning ved å velge ikonet ![Innstillinger.](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter") og deretter **Tilpass**-handlingen.
2. Velg et felt du vil endre. I lister velger du tilsvarende kolonneoverskrift. Velg deretter enten **Inkludert i Hurtigoppføring** eller **Ekskludert fra Hurtigoppføring**.

Hvis du vil ha mer informasjon om tilpasning, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Obligatoriske felt

Når du angir data på sider, merkes bestemte felt med en rød stjerne. Det røde stjernetegnet betyr at feltet må fylles ut for å fullføre en bestemt prosess. Et eksempel er når du poster en transaksjon som bruker verdien i feltet.  

Selv om et felt er obligatorisk, må du ikke fylle ut feltet før du fortsetter til andre felt eller lukker siden. Den røde stjernen er bare en påminnelse om at du blir blokkert fra å fullføre en bestemt prosess.  

## <a name="finding-data-as-you-type"></a>Finne data mens du skriver

 Når du begynner å skrive inn tegn i et felt, åpnes en rullegardinliste med mulige feltverdier. Listen endres mens du skriver flere tegn, og du kan velge riktig verdi når den vises.  

 Mange felt har en pil-ned-knapp som du kan velge. Du velger pilen for å få frem en liste over data som kan settes inn i feltet. Knappen har to funksjoner, avhengig av felttype:  

-   Oppslag - viser informasjon fra en annen tabell som du kan sette inn i feltet. Du kan velge én datadel om gangen.  

-   Rullegardin - viser settet med alternativer som finnes for feltet. Du kan bare velge ett av alternativene.  

## <a name="copying-and-pasting-faq-fields-and-lines"></a>Vanlige spørsmål om kopiere og lime inn felt og linjer

Du kan kopiere én eller flere rader fra en liste eller fra ett felt på en side. Deretter limer du inne det du kopierte, på samme side, en annen side eller et eksternt dokument. Du kan for eksempel lime inn i Microsoft Excel eller Outlook-e-post. Kort fortalt for å kopiere trykker du CTRL + C (kommando + C i macOS) på tastaturet. Du limer inn ved å trykke på CTRL + V eller kommando + V i macOS.

Trykk på F8 i listen for å kopiere feltet i den samme kolonnen i raden over, og lim det inn i den gjeldende raden.

Hvis du vil ha mer informasjon, kan du se [Vanlige spørsmål om kopiere og lime inn](faq-copy-paste.yml).

## <a name="filtering-line-items"></a>Filtrere linjeelementer

For å starte filtreringen kan du velge ![Filtreringsruteikon](media/open-filter-pane-icon.png "Filtreringsruteikon") øverst i oversikten eller trykke på Skift+F3 for å åpne filtreringsruten. Du arbeider med filtreringsruten som i andre oversikter. Hvis du vil ha mer informasjon, kan du se [Filtrering](ui-enter-criteria-filters.md#filtering).

Filtrering er spesielt nyttig når du viser og analyserer lengre dokumenter. Du åpner for eksempel en postert salgsfaktura. Deretter filtrerer du linjeelementene til å vise alle linjeelementene som har en individuell rabatt over 5 %. Eller du kan filtrere for å vise bare sykkeltilbehør med «pro» i navnet.

## <a name="focusing-on-line-items"></a><a name="Focus"></a>Fokusere på linjeelementer

Når du arbeider i dokumenter som inkluderer en del for linjeelementer, kan du bytte visning til å fokusere bare på linjeelementene. Eksempeldokumenter er ordre eller fakturaside. Delen for linjeelementer utvides slik at den bruker nesten hele arbeidsområdet. Den skjuler andre deler på siden unntatt handlingsområdet øverst. Dette oppsettet gir deg bedre oversikt over linjeelementene og gir deg mer plass til å arbeide med dem.

Det er særlig nyttig når du arbeider med store linjeelementlister og du vil registrere data raskt. Denne funksjoner inneholder også filtreringsegenskaper. Som i andre lister blir blaing og søking gjennom linjeelementer enda enklere.

### <a name="switching-the-focus-on-and-off"></a>Bytte fokus på og av

Hvis du vil fokusere på linjeelementer, velger du hvor som helst i linjeelementdelen, og deretter velger du ![Fokusmodusikon.](media/focus-mode.png "Fokusmodusikon") øverst i høyre hjørne, eller trykk på CTRL + SKIFT + F12.

Hvis du vil gå tilbake til normal visning, velger du ![Fokusmodusikon.](media/focus-mode.png "Fokusmodusikon") eller trykker på CTRL + SKIFT + F12 på nytt.

## <a name="multitasking-across-multiple-pages"></a>Multitaske på tvers av flere sider

Du kan åpne et kort eller en dokumentside i et nytt vindu. Ved å åpne i et nytt vindu kan du:

- arbeide på flere oppgaver samtidig
- administrere avbrudd for gjeldende oppgave, som å besvare et innkommende anrop
- holde et vindu åpent for en pågående oppgave mens du starter eller fullfører en annen oppgave i vinduer

Hvis du vil åpne det gjeldende kortet eller dokumentet i et nytt vindu, velger du ![Åpne nytt vindu.](media/open-new-window-icon.png "Åpne i nytt vindu-ikon") øverst i høyre hjørne, eller trykk på ALT + SKIFT + W.

<!--
When working on multiple tasks at a time or when managing interruptions to the current task, such as taking an incoming call, you can open a card or document page in a new window. This allows you to keep a window open for an ongoing task while you start or complete another task in one or more other windows.
-->
Hvis du vil åpne det gjeldende kortet eller dokumentet i et nytt vindu, velger du ![Åpne nytt vindu.](media/open-new-window-icon.png "Åpne i nytt vindu-ikon") øverst i høyre hjørne, eller trykk på ALT + SKIFT + W.

> [!NOTE]
> Når du åpner andre sider fra et kort eller dokument som er åpnet i et nytt vindu, åpnes disse sidene i et nytt vindu selv om du ikke velger ![Åpne i nytt vindu.](media/open-new-window-icon.png "Åpne i nytt vindu-ikon").

> [!NOTE]
> Hvis du arbeider i Safari-leseren, kan en popup-blokkering føre til at det nye vinduet ikke åpnes. Hvis dette er tilfellet, angir du produkt-URL-adressen som et tillatt webområde. Hvis du vil ha mer informasjon, kan du se [Endre innstillinger i Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Det samme kan skje i andre nettlesere, for eksempel Firefox. Se [Innstillinger for popup-blokkering i Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400) hvis du vil ha mer informasjon.  

En annen måte å kjøre gjøremål på, er å åpne [!INCLUDE[prod_short](includes/prod_short.md)] i to eller flere webleserkategorier. Når du gjør det på denne måten, bør du opprette en ny fane og kopiere / lime inn URL-adressen til den opprinnelige fanen i den nye fanen. Dette oppretter en ny økt.   

> [!NOTE]
> Ikke bruk **Dupliser**-funksjonen i nettleseren til å opprette den nye fanen, siden dette kan forårsake at handlinger på én fane blokkerer handlinger på andre faner fordi de er en del av den samme økten.

## <a name="entering-quantities-by-calculation"></a>Angi antall ved beregning

Når du setter inn tall i antallfelt, for eksempel **Antall**-feltet på en varekladdlinje, kan du angi formelen i stedet for summen.  

### <a name="examples"></a>Eksempler  

-   Hvis du skriver inn 19+19, beregnes feltet til 38.  

-   Hvis du skriver inn 41-9, beregnes feltet til 32.  

-   Hvis du skriver inn 12*4, beregnes feltet til 48.  

-   Hvis du skriver inn 12/4, beregnes feltet til 3.  

## <a name="entering-negative-numbers"></a>Skrive inn negative tall

Du kan angi negative tall på to måter. Tallet -20,5 kan angis som:  

-   -20,5  

    eller
-   20,5-  

 I begge tilfeller registreres beløpet som -20,5.  

 Hvis det siste tegnet i uttrykket er en **++** eller en **--**, blir hele uttrykket registrert med dette tegnet. Eksempel: **10-20+** resulterer i 10 og ikke -10.  

## <a name="entering-dates-and-times"></a>Angi datoer og klokkeslett

Du kan angi datoer og klokkeslett i alle feltene som er tilordnet datoer (datofelt). Datoene kan skrives inn med eller uten skilletegn.

> [!NOTE]  
> Hvordan du angir dato og klokkeslett på, avhenger av dine **Område**-innstillinger. Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Sette inn datoer

Du kan enten bruke datovelgeren til å velge en dato fra en kalender, eller du kan angi datoer manuelt. Denne delen inneholder en kort oversikt over hvordan du angir datoer. Se [Arbeider med kalenderdatoer og klokkeslett](ui-enter-date-ranges.md) hvis du vil ha mer informasjon.

For manuell datoregistrering kan du angi to, fire, seks eller åtte tall:  

-   To sifre tolkes som dagen. Det legger til måneden og året i arbeidsdatoen.  

-   Fire sifre tolkes som dagen og måneden. Det legger til året i arbeidsdatoen.  

-   Hvis datoen du ønsker, er i området 01.01.1930 til 31.12.2029, angir du året med to tall. Hvis ikke angir du året med fire tall.  

Du kan også angi en dato som en ukedag etterfulgt av et ukenummer. Eller du kan angi et år. For eksempel Man25 eller man25 betyr mandag i uke 25.  

I stedet for å skrive inn en bestemt dato kan du skrive inn én av disse kodene.  

| - kode|Resultat|  
|--------------|----------------|  
|i|Angir dagens dato (systemdatoen til datamaskinen).|  
|P|Angir en regnskapsperiode der p betyr den første regnskapsperioden, p2 betyr den andre regnskapsperioden og så videre. |
|a|Angir arbeidsdatoen som er konfigurert i programmet. Du kan endre arbeidsdatoen ved å se [Endre grunnleggende innstillinger](ui-change-basic-settings.md). Hvis du har mange transaksjoner å utføre på en dato som ikke er dagens dato, er det en fordel å bruke arbeidsdatoen.|
|a|Angir at datoen etter a er for en lukkingsdato, for eksempel C123101.|  

## <a name="entering-times"></a>Angi klokkeslett

Når du angir klokkeslett, kan du sette i et skilletegn du ønsker mellom enhetene, men det er ikke nødvendig. Du trenger ikke å skrive minutter eller sekunder.  

Tabellen nedenfor viser forskjellige måter som klokkeslett kan angis på, og hvordan de tolkes.  

|Angivelse|Tolkning|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5,50|05:30:05.5|  
|053005050|05:30:05.05|  

 Du angir to tall for hver tidsenhet hvis du ikke angir et skilletegn.  

## <a name="entering-combined-datetimes"></a>Angi kombinerte datoer og klokkeslett

[!INCLUDE [datetimes](includes/datetimes.md)]

## <a name="entering-duration"></a>Angi varighet

Du angir en varighet som et tall etterfulgt av enheten.  

Her er noen eksempler.  

|Varighet|Enhtet**|  
|------------------|-------------------------|  
|2t|2 timer|  
|6t 30 m|6 timer 30 min|  
|6,5t|6 timer 30 min|  
|90m|1 t 30 min|  
|2d 6t 30m|2 dager 6 timer 30 min|  
|2d 6t 30m 56s 600ms|2 dager 6 timer 30 min 56 sek 600 msek|  

 Du kan også angi et tall, og det konverteres automatisk til en varighet. Tallet du angir, konverteres i henhold til standardenheten som er angitt for feltet Varighet.  

 Hvis du vil se hvilken enhet som brukes i et varighetsfelt, kan du angi et tall og se hvilken enhet programmet er konvertert det til.  

 Tallet 5 konverteres til 5 timer hvis enheten er timer.  

## <a name="setting-the-decimal-separator-used-by-numeric-keyboards"></a><a name="decimal"></a>Angi desimalskilletegnet som brukes av numeriske tastaturer

Når du bruker desimalskilletegn for numerisk tastatur til å skrive inn data, bestemmes det faktiske desimalskilletegnet som er angitt i feltet, av områdeinnstillingen for Business Central. Du angir området i Business Central på siden **Mine innstillinger**.

La oss for eksempel anta at du bruker et numerisk tastatur som bruker et punktum (.) som desimalskilletegn. Du registrerer imidlertid data for et regionalt språk som bruker komma (**,**) som desimalskilletegn, for eksempel dansk (Danmark) eller fransk (Frankrike). Du vil derfor at desimaler skal settes til 1.23 angis som 1,23. I dette tilfellet kan du gå til siden **Mine innstillinger** og angir **Område** på det regionale språket, for eksempel **dansk (Danmark)** eller **fransk (Frankrike)**. Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md#region).

## <a name="see-also"></a>Se også

[Sortere, søke etter og filtrere oversikter](ui-enter-criteria-filters.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]