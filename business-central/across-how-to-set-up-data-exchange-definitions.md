---
title: Definere hvordan data utveksles elektronisk
description: 'Definer hvordan Business Central utveksler data med eksterne filer, for eksempel elektroniske dokumenter, bankdata, varekataloger og så videre.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.search.form: '1210, 1211, 1213, 1214, 1215, 1216, 1217'
ms.date: 11/03/2022
ms.author: bholtorf
---
# Definere datautvekslingsdefinisjoner

Du kan opprette [!INCLUDE[prod_short](includes/prod_short.md)] for å utveksle data i bestemte tabeller med data i eksterne filer. Du kan for eksempel sende og motta elektroniske dokumenter, importere og eksportere bankdata eller andre data, for eksempel lønn, og varekataloger. Lær mer på [Utveksle data elektronisk](across-data-exchange.md).  

For å opprette en datautvekslingsdefinisjon for en datafil eller -strøm, kan du bruke det tilknyttede XML-skjemaet til å definere hvilke dataelementer skal tas med i hurtigfanen **Kolonnedefinisjoner**. Se trinn 6 under [Slik beskriver du formateringen av linjer og kolonner i filen](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Lær mer på [Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Vanligvis setter du opp datautvekslingsdefinisjoner på siden **Datautvekslingsdefinisjon**. Når det gjelder oppdatering av valutakurser, er det imidlertid raskere å bruke en valutakurstjeneste. Lær mer på [Oppdatere valutakurser](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service)

> [!NOTE]  
> Hvis filen som konverteres, er i XML-format, skal begrepet *"kolonne"* i denne artikkelen tolkes som et *XML-element som inneholder data*.  

Denne artikkelen inneholder følgende fremgangsmåter:  

* Opprett en datautvekslingsdefinisjon.
* Eksporter en datautvekslingsdefinisjon som en XML-fil som andre kan bruke.
* Importer en XML-fil for en eksisterende datautvekslingsdefinisjon.

## Opprette en datautvekslingsdefinisjon

Oppretting av en datautvekslingsdefinisjon omfatter to oppgaver:  

1. På siden **Datautvekslingsdefinisjon** beskriver du formateringen for linjer og kolonner i filen. Lær mer i delen [Slik beskriver du formateringen av linjer og kolonner i filen](#formatlinescolumns).  
2. På siden **Tilordning for datautveksling** tilordner du kolonner i datafilen til felt i [!INCLUDE[prod_short](includes/prod_short.md)]. Lær mer i delen [Slik tilordner du kolonner i datafilen til felt i [!INCLUDE[prod_short](includes/prod_short.md)]](#mapfields).  

### <a name=formatlinescolumns></a>Slik beskriver du formateringen av linjer og kolonner i filen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Datautvekslingsdefinisjoner**, og velg deretter den tilknyttede koblingen.  
2. Velg handlingen **Ny**.  
3. I hurtigfanen **Generelt** beskriver du datautvekslingsdefinisjonen og datafiltypen ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Definisjon|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Skriv inn en kode for å identifisere datautvekslingsdefinisjonen.|  
    |**Navn**|Angi et navn for datautvekslingsdefinisjonen.|  
    |**Filtype**|Angi hvilken type fil datautvekslingsdefinisjonen brukes til. Du kan velge mellom fire filtyper:<br /><br /> -   **XML**: lagdelte strenger med innhold og kode omgitt av koder som angir funksjon.<br />-   **Variabel tekst**: Poster har variabel lengde og er atskilt med et tegn, for eksempel komma eller semikolon\-, også kjent som en *kommadelt fil*.<br />-   **Fast tekst**: Poster har samme lengde ved hjelp av utfyllingstegn, og hver post er på en separat linje, også kjent som en *fil med fast bredde*.<br />- **Json**: Lagvise strenger med innhold i JavaScript.|  
    |**Type**|Angi hvilken type forretningsvirksomhet datautvekslingsdefinisjonen brukes til, for eksempel **betalingseksport**.|  
    |**Kodeenhet for datahåndtering**|Angi kodeenheten som overfører data inn i og ut av tabeller i [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Kodeenhet for validering**|Angi kodeenheten som brukes til å validere data mot forhåndsdefinerte forretningsregler.|  
    |**Kodeenhet for lesing/skriving**|Angi kodeenheten som behandler importerte data før tilordning og eksporterte data etter tilordning.|  
    |**XMLport for lesing/skriving**|Angir XMLport som en importert datafil eller tjeneste overføres via før tilordning, og som eksporterte data overføres via når de skrives til en datafil eller tjeneste etter tilordning.|  
    |**Kodeenhet for ekstern datahåndtering**|Angi kodeenheten som overfører eksterne data inn i og ut av rammeverket for datautveksling.|  
    |**Kodeenhet for brukertilbakemelding**|Angi kodeenheten som inneholder ulike oppryddinger etter tilordning, for eksempel markerer linjene som eksporteres og sletter midlertidige poster.|  
    |**Filkoding**|Angi kodingen for filen. **Obs!** Dette feltet er bare relevant for import.|  
    |**Kolonneskilletegn**|Angi hvordan kolonner skilles i datafilen, hvis filen er av typen **Variabel tekst**.|  
    |**Topptekstlinjer**|Angi hvor mange topptekstlinjer det er i filen.<br /><br /> Denne innstillingen sikrer at topptekstdataene ikke importeres. **Obs!** Dette feltet er bare relevant for import.|  
    |**Topptekstkode**|Hvis det finnes en topptekst på flere steder i filen, kan du angi teksten i den første kolonnen på topptekstlinjen.<br /><br /> Dette alternativet sikrer at topptekstdataene ikke importeres. **Obs!** Dette feltet er bare relevant for import.|  
    |**Bunntekstkode**|Hvis det finnes en bunntekst på flere steder i filen, kan du angi teksten i den første kolonnen på bunntekstlinjen.<br /><br /> Dette alternativet sikrer at bunntekstdataene ikke importeres. **Obs!** Dette feltet er bare relevant for import.|  

   > [!TIP]
   > Hvis du vil se hvilke codeuniter Microsoft bruker i eksisterende definisjoner i standardproduktet, kan du se de tre **Codeunit**-feltene i hodet på **Felttilordning**-siden for hver definisjon under hurtigfanen **Generelt** for hver definisjon.  

4. I hurtigfanen **Linjedefinisjoner** beskriver du formateringen av linjer i datafilen ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

    > [!NOTE]  
    > For import av bankkontoutdrag kan du bare opprette én linje for enkeltformatet til bankkontoutdragsfilen som du vil importere.  
    >
    > For eksport av betalinger kan du opprette en linje for hver betaling du vil eksportere. I slike tilfeller viser hurtigfanen **Kolonnedefinisjoner** forskjellige kolonner for hver betalingstype.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Linjetype**|Angir linjetypen i filen.|  
    |**Kode**|Angi en kode som identifiserer linjen i filen.|  
    |**Navn**|Angi et navn som beskriver linjen i filen.|  
    |**Antall kolonner**|Angi hvor mange kolonner det er på linjen i datafilen. **Obs!** Dette feltet er bare relevant for import.|  
    |**Datalinjemerke**|Angi posisjonen til elementet som representerer hovedposten i datafilen, i det tilknyttede XML-skjemaet. **Obs!** Dette feltet er bare relevant for import.|  
    |**Navneområde**|Angi navneområdet som forventes i filen, for å aktivere validering av navneområde. Du kan la dette feltet stå tomt hvis du ikke vil aktivere validering av navneområde.|  
    |**Overordnet kode**|Angi linjens overordnede, som vise i feltet **Kode**, i tilfeller der datautvekslingsoppsettet gjelder for filer med overordnede og underordnede poster, for eksempel dokumenttopptekst og -linjer.

5. Gjenta trinn 4 for å opprette en linje for hver fildatatype du vil eksportere.  

     Fortsett med å beskrive formateringen av kolonner i datafilen ved å fylle ut feltene i hurtigfanen **Kolonnedefinisjoner** som beskrevet i tabellen nedenfor. Du kan bruke filstrukturen, for eksempel en XSD-fil, for datafilen til å forhåndsutfylle hurtigfanen med de aktuelle elementene. Lær mer på [Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

6. I hurtigfanen **Kolonnedefinisjoner** velger du handlingen **Hent filstruktur**.  
7. På siden **Hent filstruktur** velger du den relaterte strukturfilen og velger deretter **OK**. Linjene i hurtigfanen **Kolonnedefinisjoner** fylles ut i henhold til strukturen til datafilen.  
8. I hurtigfanen **Kolonnedefinisjoner** redigerer eller fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Kolonnenr.**|Angi tallet som gjenspeiler kolonneposisjonen på linjen i filen.<br /><br /> For XML-filer angir du tallet som gjenspeiler elementtype i filen som inneholder dataene.|  
    |**Navn**|Angi navnet på kolonnen.<br /><br /> For XML-filer kan du angi markeringen som merker dataene som skal utveksles.|  
    |**Datatype**|Angi om dataene som skal utveksles, er av typen **Tekst**, **Dato** eller **Desimal**.|  
    |**Dataformat**|Angi det eventuelle dataformatet. Eksempel: **dd.MM.åååå** hvis datatypen er **Dato**. **Obs!** For eksport angir du dataformatet i henhold til [!INCLUDE[prod_short](includes/prod_short.md)]. For import angir du dataformatet i henhold til .NET Framework. Finn ut mer på [Standard formatstrenger for dato og klokkeslett](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Dataformateringskultur**|Angi det eventuelle regionale dataformatet. For eksempel **en-US** hvis datatypen er **Desimal**, for å sikre at komma brukes som skilletegn for .000, i henhold til formatet for USA. Finn ut mer på [Standard formatstrenger for dato og klokkeslett](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Obs!** Dette feltet er bare relevant for import.|  
    |**Lengde**|Angi lengden på linjen med fast bredde som inneholder kolonnen, hvis datafilen er av typen **Fast tekst**.|  
    |**Beskrivelse**|Angir en beskrivelse av kolonnen for informasjonsformål.|  
    |**Bane**|Angi posisjonen til elementet i det tilknyttede XML-skjemaet.|  
    |**Identifikator for minustegn**|Angi verdien som brukes i datafilen til å identifisere negative beløp i datafiler som ikke kan inneholde negative fortegn. Denne identifikatoren brukes deretter til å gi de identifiserte beløpene negative fortegn under import. **Obs!** Dette feltet er bare relevant for import.|  
    |**Konstant**|Angi data du vil eksportere i denne kolonnen, for eksempel tilleggsinformasjon om betalingstypen. **Obs!** Dette feltet er bare relevant for eksport.|  
    |**Tekstutfylling kreves**|Angir at dataene må inkludere tekstutfylling.|  
    |**Utfyllingstegn**|Angi tekstens utfyllingstegn.|  
    |**Justering**|Angi om kolonnejusteringen er mot høyre eller venstre.|  

9. Gjenta trinn 8 for hvert kolonne- eller XML-element i datafilen som har data du vil utveksle med [!INCLUDE[prod_short](includes/prod_short.md)].  

Det neste trinnet i å opprette en datautvekslingsdefinisjon er å bestemme hvilke felt i [!INCLUDE[prod_short](includes/prod_short.md)]som kolonner eller XML-elementer i datafilen skal tilordnes til.  

> [!NOTE]  
> Den bestemte tilordningen avhenger av forretningsformålet med datafilen som skal utveksles, og av lokale variasjoner. Selv SEPA-bankstandarden har lokale variasjoner. [!INCLUDE[prod_short](includes/prod_short.md)] støtter import av SEPA CAMT-bankkontoutdragsfiler \-\-\-. Dette er angitt med **SEPA CAMT**-postkoden for datautvekslingsdefinisjon på siden **Datautvekslingsdefinisjoner**. For informasjon om spesifikk felttilordning av SEPA CAMT-støtten kan du se [Felttilordning ved import av SEPA CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md).  

### <a name=mapfields></a>Slik tilordner du kolonner i datafilen til felt i [!INCLUDE[prod_short](includes/prod_short.md)]

> [!TIP]
> Noen ganger er verdiene i feltene du vil tilordne, forskjellige. For eksempel, i én virksomhetapp er språkkoden for USA "U.S.", men i en annen er det "US". Det betyr at du må transformere verdien når du utveksler data. Dette skjer gjennom transformeringsregler som du definerer for feltene. Lær mer om [Transformasjonsregler](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

Fra lanseringsbølge 2 i 2022 kan du også gruppere etter et hvilket som helst felt, bruke nøkkelindeksen til å sortere resultatene og de nye transformeringstypene **Avrunding** og **Feltoppslag**.

1. I hurtigfanen **Linjedefinisjoner** velger du linjen for tilordning av kolonner til felt, og deretter velger du **Felttilordning**. Siden **Tilordning for datautveksling** åpnes.  
2. I hurtigfanen **Generelt** angir du tilordningsoppsettet ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Tabell-ID**|Angi tabellen som inneholder feltene som data utveksles til eller fra i samsvar med tilordningen.|  
    |**Bruk som foreløpig tabell**|Angi om tabellen du velger i feltet **Tabell-ID**, er en foreløpig tabell der de importerte dataene lagres før de tilordnes til måltabellen.<br /><br /> Du bruker vanligvis en midlertidig tabell når datautvekslingsdefinisjonen brukes til å importere og konvertere elektroniske dokumenter, for eksempel leverandørfakturaer til kjøpsfakturaer i [!INCLUDE[prod_short](includes/prod_short.md)]. Lær mer på [Utveksle data elektronisk](across-data-exchange.md).|  
    |**Navn**|Angi et navn for tilordningsoppsettet.|  
    |**Nøkkelindeks**|Angir nøkkelindeksen for å sortere kildeoppføringene før eksport.|
    |**Kodeenhet for forhåndstilordning**|Angi kodeenheten som klargjør tilordningen mellom felt i [!INCLUDE[prod_short](includes/prod_short.md)] og eksterne data.|  
    |**Kodeenhet for tilordning**|Angi kodeenheten som brukes til å tilordne de angitte kolonnene eller XML-dataelementene til felt i [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Kodeenhet for ettertilordning**|Angi kodeenheten som fullfører tilordningen mellom felt i [!INCLUDE[prod_short](includes/prod_short.md)] og eksterne data. **Obs!** Når utvidelsesfunksjonen for AMC Banking 365 Fundamentals brukes, konverterer kodeenheten eksporterte data fra [!INCLUDE[prod_short](includes/prod_short.md)] til et generelt format som er klart til eksport. For import konverterer kodeenheten eksterne data til et format som er klar for import til [!INCLUDE[prod_short](includes/prod_short.md)].|
3. På hurtigfanen **Felttilordning** angir du hvilke kolonner som skal tilordnes felt i [!INCLUDE[prod_short](includes/prod_short.md)] ved å fylle ut feltene som beskrevet i tabellene nedenfor, avhengig av om feltet **Bruk som midlertidig tabell** var aktivert eller ikke.  
   * Når **Bruk som foreløpig tabell** er deaktivert:

     |Felt|Description|  
     |--------------------------------- |---------------------------------------|  
     |**Kolonnenr.**|Angi hvilken kolonne i datafilen du vil definere en tilordning for.<br /><br /> Du kan bare velge kolonner som vises som linjer i hurtigfanen **Kolonnedefinisjoner** på siden **Datautvekslingsdefinisjon**.|
     |**Kolonneoverskrift**|Angi overskriften for kolonnen i den eksterne filen som er tilordnet til feltet i feltet **Måltabell-ID**, når du bruker en midlertidig tabell for dataimport.|
     |**Felt-ID**|Angi hvilket felt kolonnen i feltet **Kolonnenr.** er tilordnet.<br /><br /> Du kan bare velge blant felt som finnes i tabellen du har angitt i **Tabell-ID**-feltet i hurtigfanen **Generelt**.|
     |**Felttittel**|Angi overskriften for feltet i den eksterne filen som er tilordnet til feltet i feltet **Måltabell-ID**, når du bruker en foreløpig tabell for dataimport.|
     |**Valgfritt**|Angi om tilordningen skal hoppes over hvis feltet er tomt. Hvis du ikke merker av for dette alternativet, vil det oppstå en eksportfeil hvis feltet er tomt.|  
     |**Transformasjonsregel**|Angi regelen som omdanner importert tekst til en verdi som støttes, før den kan tilordnes til et angitt felt. Når du velger en verdi i dette feltet, blir den samme verdien angitt i feltet for **Transformeringsregel** i **Buffer for felttilordning for datautveksl.** -abellen, og vice versa. Se neste del hvis du vil ha mer informasjon om tilgjengelige transformeringsregler som kan brukes.|
     |**Overskriv verdi**|Angi at den gjeldende verdien blir overskrevet av en ny verdi.|
     |**Prioritet**|Angi rekkefølgen som felttilordningene må behandles i. Felttilordningen med det høyeste prioritetsnummeret, behandles først.|
     |**Multiplikator**|Angi en multiplikator som skal brukes på numeriske data, inkludert negative verdier.|

   * Når **Bruk som foreløpig tabell** er aktivert:

     |Felt|Description|  
     |---------------------------------|---------------------------------------|  
     |**Kolonnenr.**|Angi hvilken kolonne i datafilen du vil definere en tilordning for.<br /><br /> Du kan bare velge kolonner som vises som linjer i hurtigfanen **Kolonnedefinisjoner** på siden **Datautvekslingsdefinisjon**.|
     |**Kolonneoverskrift**|Angi overskriften for kolonnen i den eksterne filen som er tilordnet til feltet i feltet **Måltabell-ID**, når du bruker en midlertidig tabell for dataimport.|
     |**Måltabell-ID**|Angirtabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|
     |**Tabelltittel**|Angi navnet på tabellen i feltet **Måltabell-ID**, som er tabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|
     |**Målfelt-ID**|Angi feltet i måltabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|
     |**Felttittel**|Angi navnet på feltet i måltabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|
     |**Bare valider**|Angi at element-til-felt-tilordningen ikke brukes til å konvertere data, men bare til å validere data.|
     |**Transformasjonsregel**|Angi regelen som omdanner importert tekst til en verdi som støttes, før den kan tilordnes til et angitt felt. Når du velger en verdi i dette feltet, blir den samme verdien angitt i feltet for **Transformeringsregel** i **Buffer for felttilordning for datautveksl.** -abellen, og vice versa. Se neste del hvis du vil ha mer informasjon om tilgjengelige transformeringsregler som kan brukes.|
     |**Prioritet**|Angi rekkefølgen som felttilordningene må behandles i. Felttilordningen med det høyeste prioritetsnummeret, behandles først.|

4. På hurtigfanen **Feltgruppering** angir du regler du vil bruke til å gruppere feltene når du oppretter filen, ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

     |Felt|Description|  
     |--------------------------------- |---------------------------------------|  
     |**Felt-ID**|Angir nummeret for feltet i den eksterne filen som brukes til gruppering, og dette feltet må angis av brukeren.|
     |**Felttittel**|Angir tittelen for feltet i den eksterne filen som brukes til gruppering.|

## Transformasjonsregler

Hvis verdiene i feltene du tilordner, er forskjellige, må du bruke transformeringsregler for datautvekslingsdefinisjoner for å gjøre dem like. Du definerer transformeringsregler for datautvekslingsdefinisjoner ved å åpne en eksisterende definisjon eller opprette en ny definisjon, og deretter, på hurtigfanen **Linjedefinisjoner**, velger du **Administrer**og deretter **Felttilordning**. Forhåndsdefinerte regler er angitt, men du kan også opprette dine egne. Tabellen nedenfor beskriver hvilke typer transformasjoner du kan utføre.

|Alternativ|Beskrivelse|
|---------|---------|
|**Store bokstaver**|Gjør alle bokstaver til store bokstaver.|
|**Små bokstaver**|Gjør alle bokstaver til små bokstaver.|
|**Store forbokstaver**|Den første bokstaven i hvert ord er en stor bokstav.|
|**Trim**|Fjern tomme mellomrom før og etter verdien.|
|**Delstreng**|Transformer en bestemt del av en verdi. Hvis du vil angi hvor transformasjonen skal starte, velger du enten **Startposisjon** eller **Starttekst**. Startposisjonen er et tall som representerer det første tegnet som skal transformeres. Startteksten er bokstaven rett foran bokstaven som skal erstattes. Hvis du vil begynne med den første bokstaven i verdien, bruker du en startposisjon i stedet. Hvis du vil angi hvor du vil stoppe transformeringen, velger du **Lengde**, som er antall tegn som skal erstattes, eller **Sluttekst**, som er tegnet som er rett etter det siste tegnet som skal transformeres.|
|**Erstatt**|Finn en verdi, og erstatt den med en annen. Denne transformasjonen er nyttig når du skal erstatte enkle verdier, for eksempel et bestemt ord.|
|**Regulært uttrykk - Erstatt**|Bruk et regulært uttrykk som en del av en søk-og-erstatt-operasjon. Denne transformasjonen er nyttig for å erstatte flere, eller mer komplekse, verdier.|
|**Fjern ikke-alfanumeriske tegn**|Slett tegn som ikke er bokstaver eller tall, for eksempel symboler eller spesialtegn.|
|**Datoformatering**|Angi hvordan datoer skal vises. Du kan for eksempel transformere DD-MM-ÅÅÅÅ til ÅÅÅÅ-MM-DD.|
|**Desimalformatering**|Definer regler for desimalplassering og avrundingspresisjon.|
|**Regulært uttrykk - Samsvar**|Bruk et regulært uttrykk for å finne én eller flere verdier. Denne regelen ligner på alternativene **Delstreng** og **Vanlig uttrykk - Erstatt**.|
|**Egendefinert**|Denne transformasjonsregelen er et avansert alternativ som krever assistanse fra en utvikler. Det muliggjør en integreringshendelse som du kan abonnere på, hvis du vil bruke din egen transformeringskode. Hvis du er utvikler og vil bruke dette alternativet, kan du se delen nedenfor.|
|**Dato- og klokkeslettformatering**|Definer hvordan gjeldende dato og tidspunktet på dagen skal vises.|
|**Feltoppslag**|Bruk felter fra forskjellige tabeller. Du må følge noen regler for å kunne bruke den. Først bruker du **Tabell-ID** til å angi ID-en for tabellen som inneholder posten for feltoppslaget. Deretter angir du ID-en til feltet som inneholder posten for feltoppslaget, i feltet **Kildefelt-ID**. Til slutt angir du ID-en til feltet for å finne posten for feltoppslaget, i feltet **Målfelt-ID**. Hvis du vil, kan du bruke feltet **Feltoppslagsregel** til å angi typen feltoppslag. Verdien fra **Målfelt-ID** brukes for **målfeltet**, selv om det er tomt. For feltet **Original hvis målet er tomt** brukes den opprinnelige verdien hvis målet er tomt.|
|**Avrund**|Avrund verdien i dette feltet ved hjelp av noen tilleggsregler. I feltet **Presisjon** angir du en avrundingspresisjon. Deretter angir du avrundingsretningen i **Retning**-feltet.|

> [!NOTE]  
> Lær mer om dato-og klokkeslettformatering på [Standard formatstrenger for dato og klokkeslett](/dotnet/standard/base-types/standard-date-and-time-format-strings).

### Tips for utviklere: eksempel på det egendefinerte alternativet

Følgende eksempel viser hvordan du implementerer din egen transformeringskode.

```AL
codeunit 60100 "Hello World"
{
    [EventSubscriber(ObjectType::Table, Database::"Transformation Rule", 'OnTransformation', '', false, false)]
    procedure OnTransformation(TransformationCode: Code[20]; InputText: Text; var OutputText: Text)
    begin
        if TransformationCode = 'CUST' then
            OutputText := InputText + ' testing';
    end;
}
```

Når du har definert reglene, kan du teste dem. I hurtigfanen **Test** skriver du inn et eksempel på en verdi du vil transformere, og deretter kontrollerer du resultatene ved å velge **Oppdater**.

## Eksporter en datautvekslingsdefinisjon som en XML-fil som andre kan bruke

Når du har opprettet datautvekslingsdefinisjonen for en bestemt datafil, kan du eksportere datautvekslingsdefinisjonen som en XML-fil som du kan importere. Denne oppgaven er beskrevet i følgende fremgangsmåte.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Datautvekslingsdefinisjoner**, og velg deretter den tilknyttede koblingen.  
2. Velg datautvekslingsdefinisjonen du vil eksportere.  
3. Velg **Eksporter datautvekslingsdefinisjon**.  
4. Lagre XML-filen som representerer datautvekslingsdefinisjonen, på en passende plassering.  

    Hvis en datautvekslingsdefinisjon allerede er opprettet, trenger du bare å importere XML-filen til rammeverket for datautveksling. Denne oppgaven er beskrevet i følgende fremgangsmåte.  

## Importere en eksisterende datautvekslingsdefinisjon

1. Lagre XML-filen som representerer datautvekslingsdefinisjonen, på en passende plassering.  
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Datautvekslingsdefinisjoner**, og velg deretter den tilknyttede koblingen.  
3. Velg **Importer datautvekslingsdefinisjon**.  
4. Velg filen du lagret i trinn 1.  

## Se også

[Definere datautveksling](across-set-up-data-exchange.md)  
[Konfigurer sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Innkreve betalinger med SEPA direct debit](finance-collect-payments-with-sepa-direct-debit.md)  
[Betale med utvidelsen AMC Banking 365 Fundamentals eller SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Inngående dokumenter](across-income-documents.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
