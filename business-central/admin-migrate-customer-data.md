---
title: Flytte kundedata | Microsoft-dokumentasjon
description: Du kan flytte eksisterende kundedata fra et eksisterende ERP-system til Business Central ved å bruke RapidStart Services. Du kan bruke Excel XLSX-filer som databærer. Du kan også flytte dataene manuelt ved å skrive dem inn direkte i selskapet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e25082286f53c5b0458359d5f5c895b03c6f6bcf
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927125"
---
# <a name="migrate-customer-data"></a>Flytte kundedata
Du kan flytte eksisterende kundedata fra et eksisterende ERP-system til [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å bruke verktøyene for dataflytting i RapidStart Services. Du kan bruke Excel-filer som databærer. Du kan også flytte dataene manuelt ved å skrive dem inn direkte i selskapet.

> [!NOTE]
> Felt av typen blob kan ikke eksporteres/importeres i Excel.

Siden **Flytting - oversikt** og **Konfigurer forslag** gir deg tilgang til funksjonene og visningene som lar deg utføre oppgavene som er relatert til overføring av data. Vi anbefaler at du flytter én tabell om gangen, for å håndtere avhengigheter i dataene. Når du flytter, berører du også hoveddatatabellene, som inneholder informasjon om kunder, leverandører, varer, kontakter og finans.  

## <a name="to-import-configuration-packages"></a>Importere konfigurasjonspakker
Når du oppretter et nytt selskap, kan du importere firmainnstillinger for det nye selskapet. Du importerer innstillingene fra en .rapidstart-fil, som leverer innholdet i pakken i et komprimert format. Et tilsvarende sett med standard dataflyttingstabeller er importert. Datasettet inneholder hoveddatatabeller og oppsettsdatatabeller. Den første oppgaven i dataflytting er å evaluere hvorvidt standardoppsettet for flytting dekker behovene til det nye firmaet.

> [!NOTE]  
>  Du kan ikke gi nytt navn til en fil som ikke allerede er en RapidStart Services-konfigurasjonspakke, som en .rapidstart-konfigurasjonspakkefil, og deretter prøve å importere den. Hvis du prøver å gjøre dette, får du en feilmelding.  

Før du begynner, må du kontrollere at du har tillatelse til å kjøre RapidStart Services-objektene. Du kan for eksempel ha SUPER- eller D365 RAPIDSTART-tillatelessett. Vi anbefaler også at du er på et rollesenter med koblinger til RapidStart Services, for eksempel rollesenteret for administrasjon. Hvis du vil ha mer informasjon, kan du se [Endre rollen](ui-change-basic-settings.md#to-change-the-role).  

> [!IMPORTANT]  
> Når du eksportere og importere konfigurasjonspakker mellom to firmadatabaser, må databasene har samme skjema for å sikre at alle dataene overføres. Dette betyr at databasene bør ha den samme tabell- og feltstruktur, der tabellene har samme primærnøkler og felt har samme IDer og datatyper.  
>
>  Du kan importere en konfigurasjonspakke som har blitt eksportert fra en database, som har et annet skjema enn måldatabasen. Tabeller eller felt i konfigurasjonpakken som ikke finnes i måldatabasen, blir imidlertid ikke importert.
>
> Tabeller som har forskjellige primærnøkler og felt med ulike datatyper, blir heller ikke importert. Hvis konfigurasjonspakken inneholder en tabell, for eksempel **50000-kunden**, som har primærnøkkelen **Kode20**, og databasen du importerer pakken til, som inneholder tabellen **Bankkonto for 50000-kunde**, som har primærnøkkelen **Kode20 + Kode20**, importeres ikke dataene.  

1. Åpne det nye selskapet.  
2. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonspakker**, og velg deretter den relaterte koblingen.  
3. Velg handlingen **Importer pakke**. Gå til .rapidstart-pakkefilen du vil importere, og velg deretter den **Åpne**-handlingen. Under import dekomprimeres innholdet i pakken og pakkeposten opprettes.  

    Når importen er fullført, kan du se hvor mange konfigurasjonstabeller som er importert, i feltet **Antall tabeller**.  
4. Hvis du vil se gjennom konfigurasjonstabellene, kan du velge **Vis**-handlingen.  
5. Du kan bruke pakken ved å velge **Bruk pakke**-handlingen.  

    > [!NOTE]  
    >  Dataoverføringsinformasjonen er basert på konfigurasjonsmaler, hvis du angir en. Hvis du vil endre oversikten over felt, må du først oppdatere malen.  

6.  Hvis du vil se gjennom feltvalgene, velger du en tabell og deretter, på fanen **Linje**, velger du **Felt**-handlingen. Sammenligne og se hvor mange felt som er tilgjengelige, med antall felt der dataene er brukt.  

Hvis tabellutvalget ikke oppfyller dine behov, kan du opprette én eller flere nye dataflyttingsfiler. Hvis filene er tilstrekkelige, kan du fortsette med dataflyttingen ved å bruke Excel- eller XML-filer.

## <a name="to-create-a-data-migration-file"></a>Slik oppretter du en dataflyttingsfil:

Du kan opprette nye dataoverføringsfiler og tilpasse dem for å støtte forretningsprosessene.  

> [!TIP]
> En fil kan bare brukes til å flytte et felt der **Normal** er angitt for **FieldClass**-egenskapen.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonspakke**, og velg deretter den relaterte koblingen.  
2. Velg og åpne pakken som du vil bruke til å flytte data, og velger deretter **Hent tabeller**-handlingen. Siden **Hent pakketabeller** åpnes.  
3. Skriv inn et tabellnummer i **Tabell-ID**-feltet, eller velg en tabell fra listen, for eksempel tabell 18, **Kunde**. Feltet **Tabellnavn** fylles ut automatisk.  
4. Velg den nye flyttingsstabellen, og deretter, i fanen **Tabeller**, velger du **Felt**-handlingen. Siden **Flyttingsfelt** åpnes.  
5. Fjern merket for **Inkluder feltet** for alle feltene du ikke vil importere, og velg deretter handlingen **Sett inkludert** eller **Fjern inkludert**.  

> [!IMPORTANT]  
>  Hvis det er merket av for **Inkluder felt** som standard, er dette feltet den del av primærnøkkelen. Valget bør ikke fjernes, ellers kan det oppstå feil og posten kan ikke importeres.  
>
>  Hvis du tar med et felt som har en relasjon til en annen tabell, merkes det automatisk av for **Valider felt**. Validering kan føre til at andre felt i denne og andre tabeller oppdateres, og utføres i rekkefølge etter feltnummeret.  

Det opprettes en ny flyttingstabell.  

## <a name="to-export-data-migration-files"></a>Slik eksporterer du dataflyttingsfiler:
Når du har bestemt hvilke tabeller du vil overføre kundedata til, eksporterer du filene.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonspakker**, og velg deretter den relaterte koblingen.  
2. Velg og åpne pakken du vil bruke til eksport.
3. Velg tabellen eller tabellene som du vil eksportere, og velg deretter den **Eksporter til Excel**-handlingen.
4. Lagre den eksporterte Excel-filen.  
5. Gjenta denne fremgangsmåten for alle relevante dataflyttingstabeller. Hvis du velger flere tabeller samtidig, eksporteres dataene til en vanlig arbeidsbok.  

Hvis tabellen er tom, den resulterende dataflyttingsfilen inneholder tomme celler for feltene du valgte da du valgte eller opprettet flyttingstabeller for det nye selskapet. Hvis den valgte dataflyttingstabellen inneholder data, eksporteres de.  

## <a name="to-map-values-to-be-used-during-import"></a>Tilordne verdiene som skal brukes under import
Når du bruker data som du har importert fra Excel eller fra en RapidStart-pakke, vil [!INCLUDE[d365fin](includes/d365fin_md.md)] behandle og håndtere tilordningen basert på tabellrelasjoner:  

- Hvis du definerer en tilordning direkte for et felt i en tabell, brukes denne tilordningen i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

- Hvis feltet har en relasjon til en annen tabell, søker [!INCLUDE[d365fin](includes/d365fin_md.md)] etter tilordningen som er definert for primærnøkkelfeltet i den relaterte tabellen. Den relaterte tabellen må imidlertid være en del av konfigurasjonspakken.  

- Hvis tilordningsinformasjon er definert begge steder, for feltet direkte og for primærnøkkelen i den relaterte tabellen, søker [!INCLUDE[d365fin](includes/d365fin_md.md)] etter tilordningen begge steder.  

- Hvis de samme tilordningene er definert direkte for et felt og i den relaterte tabellen, men har ulike nye verdier, prioriteres tilordningen som er definert direkte for feltet, fremfor tilordningen som er definert for tabellen som feltet refererer til.  

I fremgangsmåtene nedenfor bør du på forhånd se gjennom hvilke verdier du vil beholde under overføringsprosessen. Hvis du vil utføre følgende fremgangsmåte, trenger du dataflyttingsfiler (XLSX) som du har eksportert fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Se [Slik eksporterer du dataflyttingsfiler](admin-migrate-customer-data.md#to-export-data-migration-files).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonspakker**, og velg deretter den relaterte koblingen.
2. Åpne pakken for det aktuelle selskapet.  
3. Velg tabellen du vil tilordne verdier for, og velg deretter fanen **Tabeller** og **Felt**-handlingen.  
4. For hvert felt du vil tilordne velger du **Tilordning**-handlingen.  
5. Angi verdien du vil endre, i **Gammel verdi**-feltet. Angi verdien du vil endre den gamle verdien til, i **Ny verdi**-feltet. Velg **OK**.  
6. Importer kundedataene. Hvis du vil ha mer informasjon, kan du se [Slik importerer du kundedata](admin-migrate-customer-data.md#to-import-customer-data).
7. Se om det er rapportert noen feil i feltet **Antall pakkefeil**. Hvis det er det, viser du detaljene for å se feilene. Siden **Konfig. pakkeposter** åpnes.
8. Velg handlingen **Vis feil**. Du vil motta følgende feilmelding: **XX er ikke et gyldig alternativ. Gyldige alternativer er XX**. Velg **OK**-knappen.  
9. Hvis du vil bruke tilordningen som du har definert, kan du velge **Bruk Data**-handlingen.  

### <a name="mapping-example"></a>Eksempel på tilordning  
Følgende eksempel illustrerer hvordan [!INCLUDE[d365fin](includes/d365fin_md.md)] implementerer tilordningsdefinisjoner.  

1. Opprett en konfigurasjonstabell som har tabellen **Selger/innkjøper**. Definer en tilordning for **Kode**-feltet.  
2. Legg til flere tabeller i pakken, for eksempel **Kunde** og **Leverandør**. Begge disse tabellene refererer til tabellen **Selger/innkjøper** via henholdsvis feltet **Selgerkode** og **Innkjøperkode**.  
3. Når du bruker data, blir det også tatt hensyn til tilordningen du har angitt for **Kode**-feltet i tabellen **Selger/innkjøper**, under behandlingen av feltene **Selgerkode** og **Innkjøperkode**.

## <a name="to-add-additional-values-to-d365fin"></a>Legge til flere verdier i [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonspakker**, og velg deretter den relaterte koblingen.  
2. Velg tabellen du vil legge til flere verdier for, og velg deretter fanen **Tabeller** og **Felt**-handlingen.  
3. Merk av for **Opprett manglende koder** for feltene som [!INCLUDE[d365fin](includes/d365fin_md.md)] skal tillate ytterligere verdier for under overføringen.  
4. Importer kundedataene. Hvis du vil ha mer informasjon, kan du se [Slik importerer du kundedata](admin-migrate-customer-data.md#to-import-customer-data).

## <a name="to-clean-up-and-process-data-before-applying-data"></a>Rydde og behandle data før du bruker data
I noen tilfeller kan det være aktuelt å rydde kundedata og behandle dem før du bruker dem på databasen. Hvis du vil gjøre dette, kan du bruke kjørselen **Konfigurer pakke - prosess** for å løse problemer, for eksempel:  

- Konvertere datoer og desimaler til formatet som kreves av de regionale innstillingene på datamaskinen til en bruker.  
- Fjerne innledende/etterfølgende mellomrom eller spesialtegn.  

Når du har kjørt kjørselen, kan du bruke fremgangsmåten nedenfor til å behandle dataene.  

1. Åpne konfigurasjonspakken for selskapet.  
2. Velg **Behandle Data**-handlingen.  
3. Hvis du vil bruke tilordningen som du har definert, kan du velge **Bruk Data**-handlingen.

## <a name="to-migrate-customer-data"></a>Flytte kundedata
Når du har eksportert en flyttingstabell, er neste trinn å angi kundens eldre data. Du kan forenkle oppgavene ved å bruke verktøyene for XML-manipulering i Excel. Du kan også bruke innebygde Excel-funksjoner for å få hjelp med dataformatering og plassering av data i riktig celle.

Hvis du trenger hjelp med XML, aktiverer du fanen **Utvikler** på Excel-båndet, og deretter velger du **Kilde**-handlingen for å se XML-skjemaet for overføringstabellen, som vist i Excel.

Følgende fremgangsmåte er basert på et Excel-regneark som du har opprettet for overføring. Se [Slik eksporterer du dataflyttingsfiler](admin-migrate-customer-data.md#to-export-data-migration-files).

> [!IMPORTANT]  
> Ikke endre kolonnene i Excel-regnearkene. Hvis du flytter, endrer eller sletter dem, kan ikke regnearket importeres til [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Åpne den eksporterte datafilen i Excel. Det finnes et forslag med tabellnavnet.
2. Gi nytt navn til Ark1 for å indikere at regnearket skal brukes til å transformere dataene. Kopier overskriftsraden uten formateringen fra den eksporterte tabellen til det nye forslaget.
3. Kopier alle kundedata på et tredje forslag. Gi for eksempel arket det nye navnet Eldre data.
4. Lag en Excel-formel til å tilordne data i transformasjonsregnearket mellom feltene i det eksporterte regnearket og eldre kundedata.
5. Når du har tilordnet alle dataene, kan du kopiere dataområdet til tabellregnearket.
6. Lagre filen og kontroller at du ikke endrer filtypen.

Du er nå klar til å importere dataoverføringsfilene som inneholder eldre kundedata, til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="to-import-customer-data"></a>Slik importerer du kundedata
Når kundedataene er angitt i dataoverføringsfilene i Excel, importerer du filene til [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Åpne siden **Konfigurer pakkekort**.
2. Velg tabellen du vil importere verdier for, og velg deretter fanen **Tabeller** og **Importer fra Excel**-handlingen.
3. Finn og åpne filen som du vil importere data fra.
4. På siden **Forhåndsvis. av konfig.pakkeimport** ser du hva som skal importeres.

    Siden **Forhåndsvis. av konfig.pakkeimport** gir en oversikt over innholdet i Excel-filen som skal importeres. Den angir også om det opprettes en ny konfigurasjonspakke, eller den eksisterende oppdateres, og om nye konfigurasjonspakkelinjer (tabeller) opprettes eller eksisterende oppdateres.    
5. Velg handlingen **Importer**

Data fra filen importeres til konfigurasjonspakketabellene. I feltet **Antall pakkeposter** kan du se hvor mange databaseposter som er importert. I tillegg kan du vise antall feil under flyttingen.

## <a name="to-validate-customer-data"></a>Slik bekrefter du kundedata:
Kundedata må valideres før du utligner postene i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen.  

> [!NOTE]  
>  I de fleste tilfeller opprettes ikke ugyldige data i databasen. Programmet kan imidlertid av og til blokkeres hvis en importert flyttingstabell inneholder feil.  

1. På siden **Flytting - oversikt** ser du gjennom feltet **Antall feil under flytting** for å se om det oppstod feil under importen.  
2. Hvis det oppstår feil, velger du flyttingstabellen, og deretter, i fanen **Tabeller**, velger du **Feil**-handlingen. Det er merket av for **Ugyldig** for hver post som inneholder en feil.  
3. Hvis du vil se gjennom feil, velger du en linje og deretter **Vis feil**-handlingen.  

    Feltet **Feiltekst** inneholder årsaken til feilen. Feltet **Felttekst** inneholder overskriften for feltet med feilen.  
4.  Hvis du vil korrigere en feil eller gjøre andre oppdateringer, går du til siden **Flytting - oversikt**, velger **Flyttepost**-handlingen, og deretter, på siden **Flyttepost**, korrigerer du posten med feil.  

Når du foretar en korrigering, fjernes posten fra listen over poster på siden **Dataoverføringsfeil**.  

Du er nå klar til å bruke kundens data i databasen.  

## <a name="to-apply-customer-data"></a>Slik bruker du kundedata:
Når du har importert alle dataoverføringsposter som er gyldige og ikke inneholder feil, kan du bruke postene i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen.  

1. Åpne siden **Konfigurasjonspakker**.  
2. Velg tabellen for dataoverføringsfilen du vil bruke, og velg deretter handlingen **Bruk data**.

I feltet **Antall databaseposter** kan du se hvor mange databaseposter som er opprettet. Du kan bekrefte at de riktige postene er opprettet ved å velge koblingen i feltet **Antall databaseposter**.  

Kundens firmadatabasen er nå konfigurert, og grunnleggende data er importert. Neste trinn i implementeringsprosessen er å lære opp brukere, definere prosesser, opprette flere data, tilpasse rapporter og så videre.

## <a name="see-also"></a>Se også  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)
