---
title: Definere hvordan data utveksles elektronisk | Microsoft-dokumentasjon
description: Du kan bruke en ekstern leverandør av OCR-tjenester for å konvertere PDF- eller bildefiler til elektroniske dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 44069b903df5426ae2aa3e851404c2b9e01f3979
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188183"
---
# <a name="set-up-data-exchange-definitions"></a>Definere datautvekslingsdefinisjoner
Du kan konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)] til å utveksle data i bestemte tabeller med data i eksterne filer, for eksempel for å sende og motta elektroniske dokumenter, importere og eksportere bankdata eller andre data, for eksempel lønn, valutakurser og elementkataloger. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).  

Som forberedelse til å opprette en datautvekslingsdefinisjon for en datafil eller -strøm, kan du bruke det tilknyttede XML-skjemaet til å definere hvilke dataelementer skal tas med i hurtigfanen **Kolonnedefinisjoner**. Se trinn 6 under [Slik beskriver du formateringen av linjer og kolonner i filen](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Hvis du vil ha mer informasjon, kan du se [Bruke XML-skjemaer til å forberede datautvekslingsdefinisjoner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Vanligvis setter du opp datautvekslingsdefinisjoner på siden **Datautvekslingsdefinisjon**. Men når du setter opp en datautvekslingsdefinisjon for å oppdatere valutakurser, starter du prosessen på den forenklede siden **Kort for oppsett for val.kursoppdatering**.  

> [!NOTE]  
>  Hvis filen som konverteres, er i XML-format, skal begrepet *kolonne* i dette emnet tolkes som *et XML-element som inneholder data*.  

Dette emnet inneholder følgende fremgangsmåter:  

* Slik oppretter du en datautvekslingsdefinisjon:  
* Slik eksporterer en datautvekslingsdefinisjon som en XML-fil som andre kan bruke:  
* Slik importerer du en XML-fil for en eksisterende datautvekslingsdefinisjon:  

## <a name="to-create-a-data-exchange-definition"></a>Slik oppretter du en datautvekslingsdefinisjon:  
Oppretting av en datautvekslingsdefinisjon omfatter to oppgaver:  

1. På siden **Datautvekslingsdefinisjon** beskriver du formateringen for linjer og kolonner i filen.  
2. På siden **Tilordning for datautveksling** tilordner du kolonner i datafilen til felt i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Dette er beskrevet i følgende fremgangsmåter.  

> [!TIP]
> Hvis du vil se hvilke codeunits Microsoft bruker i eksisterende definisjoner i standardproduktet, kan du se de tre **codeunit**-feltene i hodet på **Felttilordning**-siden for hver definisjon.

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>Slik beskriver du formateringen av linjer og kolonner i filen:  
1. Skriv inn **Datautvekslingsdefinisjoner** i **Søk**-boksen, og velg deretter den tilknyttede koblingen.  
2. Velg handlingen **Ny**.  
3. I hurtigfanen **Generelt** beskriver du datautvekslingsdefinisjonen og datafiltypen ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Definisjon|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Skriv inn en kode for å identifisere datautvekslingsdefinisjonen.|  
    |**Navn**|Angi et navn for datautvekslingsdefinisjonen.|  
    |**Filtype**|Angi hvilken type fil datautvekslingsdefinisjonen brukes til. Du kan velge mellom fire filtyper:<br /><br /> -   **XML**: lagdelte strenger med innhold og kode omgitt av koder som angir funksjon.<br />-   **Variabel tekst**: Poster har variabel lengde og er atskilt med et tegn, for eksempel komma eller semi\-kolon. Kalles også *kommadelt fil*.<br />-   **Fast tekst**: Poster har samme lengde ved hjelp av utfyllingstegn, og hver post er på en separat linje. Kalles også *fil med fast bredde*.<br />- **Json**: Lagvise strenger med innhold i JavaScript.|  
    |**Type**|Angi hvilken type forretningsvirksomhet datautvekslingsdefinisjonen brukes til, for eksempel **betalingseksport**.|  
    |**Kodeenhet for datahåndtering**|Angi kodeenheten som overfører data inn i og ut av tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Kodeenhet for validering**|Angi kodeenheten som brukes til å validere data mot forhåndsdefinerte forretningsregler.|  
    |**Kodeenhet for lesing/skriving**|Angi kodeenheten som behandler importerte data før tilordning og eksporterte data etter tilordning.|  
    |**XMLport for lesing/skriving**|Angir XMLport som en importert datafil eller tjeneste overføres via før tilordning, og som eksporterte data overføres via når de skrives til en datafil eller tjeneste etter tilordning.|  
    |**Kodeenhet for ekstern datahåndtering**|Angi kodeenheten som overfører eksterne data inn i og ut av rammeverket for datautveksling.|  
    |**Kodeenhet for brukertilbakemelding**|Angi kodeenheten som inneholder ulike oppryddinger etter tilordning, for eksempel markerer linjene som eksporteres og sletter midlertidige poster.|  
    |**Filkoding**|Angi kodingen for filen. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Kolonneskilletegn**|Angi hvordan kolonner skilles i datafilen, hvis filen er av typen **Variabel tekst**.|  
    |**Topptekstlinjer**|Angi hvor mange topptekstlinjer det er i filen.<br /><br /> Dette sikrer at topptekstdataene ikke importeres. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Topptekstkode**|Hvis det finnes en topptekst på flere steder i filen, kan du angi teksten i den første kolonnen på topptekstlinjen.<br /><br /> Dette sikrer at topptekstdataene ikke importeres. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Bunntekstkode**|Hvis det finnes en bunntekst på flere steder i filen, kan du angi teksten i den første kolonnen på bunntekstlinjen.<br /><br /> Dette sikrer at bunntekstdataene ikke importeres. **Obs!**  Dette feltet er bare relevant for import.|  

4. I hurtigfanen **Linjedefinisjoner** beskriver du formateringen av linjer i datafilen ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

    > [!NOTE]  
    >  For import av bankkontoutdrag kan du bare opprette én linje for enkeltformatet til bankkontoutdragsfilen som du vil importere.  
    >   
    >  For eksport av betalinger kan du opprette en linje for hver betaling du vil eksportere. I slike tilfeller viser hurtigfanen **Kolonnedefinisjoner** forskjellige kolonner for hver betalingstype.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Angi en kode som identifiserer linjen i filen.|  
    |**Navn**|Angi et navn som beskriver linjen i filen.|  
    |**Antall kolonner**|Angi hvor mange kolonner det er på linjen i datafilen. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Datalinjemerke**|Angi posisjonen til elementet som representerer hovedposten i datafilen, i det tilknyttede XML-skjemaet. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Navneområde**|Angi navneområdet som forventes i filen, for å aktivere validering av navneområde. Du kan la dette feltet stå tomt hvis du ikke vil aktivere validering av navneområde.|  

5. Gjenta trinn 4 for å opprette en linje for hver fildatatype du vil eksportere.  

     Fortsett med å beskrive formateringen av kolonner i datafilen ved å fylle ut feltene i hurtigfanen **Kolonnedefinisjoner** som beskrevet i tabellen nedenfor. Du kan bruke filstrukturen, for eksempel en XSD-fil, for datafilen til å forhåndsutfylle hurtigfanen med de aktuelle elementene. Hvis du vil ha mer informasjon, kan du se [Bruke XML-skjemaer til å forberede datautvekslingsdefinisjoner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

6. I hurtigfanen **Kolonnedefinisjoner** velger du **Hent filstruktur**.  
7. På siden **Hent filstruktur** velger du den relaterte strukturfilen og velger deretter **OK**-knappen. Linjene i hurtigfanen **Kolonnedefinisjoner** fylles ut i henhold til strukturen til datafilen.  
8. I hurtigfanen **Kolonnedefinisjoner** redigerer eller fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kolonnenr.**|Angi tallet som gjenspeiler kolonneposisjonen på linjen i filen.<br /><br /> For XML-filer angir du tallet som gjenspeiler elementtype i filen som inneholder dataene.|  
    |**Navn**|Angi navnet på kolonnen.<br /><br /> For XML-filer kan du angi markeringen som merker dataene som skal utveksles.|  
    |**Datatype**|Angi om dataene som skal utveksles, er av typen **Tekst**, **Dato** eller **Desimal**.|  
    |**Dataformat**|Angi det eventuelle dataformatet. Eksempel: **dd.MM.åååå** hvis datatypen er **Dato**. **Obs!**  For eksport angir du dataformatet i henhold til [!INCLUDE[d365fin](includes/d365fin_md.md)]. For import angir du dataformatet i henhold til .NET Framework. Hvis du vil ha mer informasjon, kan du se [Standard formatstrenger for dato og klokkeslett](https://go.microsoft.com/fwlink/?LinkID=323466).|  
    |**Dataformateringskultur**|Angi den eventuelle kulturen for dataformatet. For eksempel **en-US** hvis datatypen er **Desimal**, for å sikre at komma brukes som skilletegn for .000, i henhold til formatet for USA. Hvis du vil ha mer informasjon, kan du se [Standard formatstrenger for dato og klokkeslett](https://go.microsoft.com/fwlink/?LinkID=323466). **Obs!**  Dette feltet er bare relevant for import.|  
    |**Lengde**|Angi lengden på linjen med fast bredde som inneholder kolonnen, hvis datafilen er av typen **Fast tekst**.|  
    |**Beskrivelse**|Angi en beskrivelse for kolonnen for informasjon.|  
    |**Bane**|Angi posisjonen til elementet i det tilknyttede XML-skjemaet.|  
    |**Identifikator for minustegn**|Angi verdien som brukes i datafilen til å identifisere negative beløp i datafiler som ikke kan inneholde negative fortegn. Denne identifikatoren brukes deretter til å gi de identifiserte beløpene negative fortegn under import. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Konstant**|Angi data du vil eksportere i denne kolonnen, for eksempel tilleggsinformasjon om betalingstypen. **Obs!**  Dette feltet er bare relevant for eksport.|  

9. Gjenta trinn 8 for hvert kolonne- eller XML-element i datafilen som har data du vil utveksle med [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Det neste trinnet i å opprette en datautvekslingsdefinisjon er å bestemme hvilke felt i [!INCLUDE[d365fin](includes/d365fin_md.md)]som kolonner eller XML-elementer i datafilen skal tilordnes til.  

> [!NOTE]  
>  Den bestemte tilordningen avhenger av forretningsformålet med datafilen som skal utveksles, og av lokale variasjoner. Selv SEPA-bankstandarden har lokale variasjoner. [!INCLUDE[d365fin](includes/d365fin_md.md)] støtter import av SEPA CAMT-bankkontoutdragsfiler \-\-\-. Dette er angitt med **SEPA CAMT**-postkoden for datautvekslingsdefinisjon på siden **Datautvekslingsdefinisjoner**. For informasjon om spesifikk felttilordning av SEPA CAMT-støtten kan du se [Felttilordning ved import av SEPA CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md).  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-d365fin"></a>Slik tilordner du kolonner i datafilen til felt i [!INCLUDE[d365fin](includes/d365fin_md.md)]  
> [!TIP]
> Noen ganger er verdiene i feltene du vil tilordne, forskjellige. For eksempel, i én virksomhetapp er språkkoden for USA "U.S.", men i den andre er det "US". Det betyr at du må transformere verdien når du utveksler data. Dette skjer gjennom transformeringsregler som du definerer for feltene. Hvis du vil ha mer informasjon, kan du se [Transformeringsregler](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

1. I hurtigfanen **Linjedefinisjoner** velger du linjen for tilordning av kolonner til felt, og deretter velger du **Felttilordning**. Siden **Tilordning for datautveksling** åpnes.  
2. I hurtigfanen **Generelt** angir du tilordningsoppsettet ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Tabell-ID**|Angi tabellen som inneholder feltene som data utveksles til eller fra i samsvar med tilordningen.|  
    |**Bruk som foreløpig tabell**|Angi om tabellen du velger i feltet **Tabell-ID**, er en foreløpig tabell der de importerte dataene lagres før de tilordnes til måltabellen.<br /><br /> Du bruker vanligvis en midlertidig tabell når datautvekslingsdefinisjonen brukes til å importere og konvertere elektroniske dokumenter, for eksempel leverandørfakturaer til kjøpsfakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).|  
    |**Navn**|Angi et navn for tilordningsoppsettet.|  
    |**Kodeenhet for forhåndstilordning**|Angi kodeenheten som klargjør tilordningen mellom felt i [!INCLUDE[d365fin](includes/d365fin_md.md)] og eksterne data.|  
    |**Kodeenhet for tilordning**|Angi kodeenheten som brukes til å tilordne de angitte kolonnene eller XML-dataelementene til felt i [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Kodeenhet for ettertilordning**|Angi kodeenheten som fullfører tilordningen mellom felt i [!INCLUDE[d365fin](includes/d365fin_md.md)] og eksterne data. **Obs!**  Når utvidelsesfunksjonen for AMC Banking 365 Fundamentals brukes, konverterer kodeenheten eksporterte data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til et generelt format som er klart til eksport. For import konverterer kodeenheten eksterne data til et format som er klar for import til [!INCLUDE[d365fin](includes/d365fin_md.md)].|  

3.  I hurtigfanen **Felttilordning** angir du hvilke kolonner som er tilordnet hvilke felt i [!INCLUDE[d365fin](includes/d365fin_md.md)], ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kolonnenr.**|Angi hvilken kolonne i datafilen du vil definere en tilordning for.<br /><br /> Du kan bare velge kolonner som vises som linjer i hurtigfanen **Kolonnedefinisjoner** på siden **Datautvekslingsdefinisjon**.|  
    |**Felt-ID**|Angi hvilket felt kolonnen i feltet **Kolonnenr.** er tilordnet.<br /><br /> Du kan bare velge blant felt som finnes i tabellen du har angitt i **Tabell**-feltet i hurtigfanen **Generelt**.|  
    |**Valgfritt**|Angi at tilordningen hoppes over hvis feltet er tomt. **Obs!**  Hvis du ikke merker av for alternativet, vil det oppstå en eksportfeil hvis feltet er tomt. **Obs!**  Dette feltet er bare relevant for eksport.|  
    |**Måltabell-ID**|Synlig bare når det er merket av for **Bruk som foreløpig tabell**.<br /><br /> Angirtabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|  
    |**Måltabelloverskrift**|Synlig bare når det er merket av for **Bruk som foreløpig tabell**.<br /><br /> Angi navnet på tabellen i feltet **Måltabell-ID**, som er tabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|  
    |**Målfelt-ID**|Synlig bare når det er merket av for **Bruk som foreløpig tabell**.<br /><br /> Angi feltet i måltabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|  
    |**Målfelttekst**|Synlig bare når det er merket av for **Bruk som foreløpig tabell**.<br /><br /> Angi navnet på feltet i måltabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|  
    |**Valgfritt**|Synlig bare når det er merket av for **Bruk som foreløpig tabell**.<br /><br /> Angi om tilordningen skal hoppes over hvis feltet er tomt. Hvis du ikke merker av for alternativet, vil det oppstå en eksportfeil hvis feltet er tomt.|  

Datautvekslingsdefinisjonen er nå klar til å aktiveres for brukere. Hvis du vil ha mer informasjon, kan du se [Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md), [Definere SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer), [Innkreve betalinger med SEPA direct debit](finance-collect-payments-with-sepa-direct-debit.md) og [Betale med utvidelsen AMC Banking 365 Fundamentals eller SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

### <a name="transformation-rules"></a>Transformasjonsregler
Hvis verdiene i feltene du tilordner, er forskjellige, må du bruke transformeringsregler for datautvekslingsdefinisjoner for å gjøre dem like. Du definerer transformeringsregler for datautvekslingsdefinisjoner ved å åpne en eksisterende definisjon eller opprette en ny definisjon, og deretter, på hurtigfanen **Linjedefinisjoner**, velger du **Administrer** og deretter **Felttilordning**. Forhåndsdefinerte regler er angitt, men du kan også opprette dine egne. Tabellen nedenfor beskriver hvilke typer transformasjoner du kan utføre.

|Alternativ|Beskrivelse|
|---------|---------|
|**Store bokstaver**|Gjør alle bokstaver til store bokstaver.|
|**Små bokstaver**|Gjør alle bokstaver til små bokstaver.|
|**Store forbokstaver**|Den første bokstaven i hvert ord er en stor bokstav.|
|**Trim**|Fjern tomme mellomrom før og etter verdien.|
|**Delstreng**|Transformer en bestemt del av en verdi. Hvis du vil angi hvor transformasjonen skal starte, velger du enten **Startposisjon** eller **Starttekst**. Startposisjonen er et tall som representerer det første tegnet som skal transformeres. Startteksten er bokstaven rett foran bokstaven som skal erstattes. Hvis du vil begynne med den første bokstaven i verdien, bruker du en startposisjon i stedet. Hvis du vil angi hvor du vil stoppe transformeringen, velger du **Lengde**, som er antall tegn som skal erstattes, eller **Sluttekst**, som er tegnet som er rett etter det siste tegnet som skal transformeres.|
|**Erstatt**|Finn en verdi, og erstatt den med en annen. Dette er nyttig når du skal erstatte enkle verdier, for eksempel et bestemt ord.|
|**Regulært uttrykk - Erstatt**|Bruk et regulært uttrykk som en del av en søk-og-erstatt-operasjon. Dette er nyttig for å erstatte flere, eller kanskje mer komplekse, verdier.|
|**Fjern ikke-alfanumeriske tegn**|Slett tegn som ikke er bokstaver eller tall, for eksempel symboler eller spesialtegn.|
|**Datoformatering**|Angi hvordan datoer skal vises. Du kan for eksempel transformere DD-MM-ÅÅÅÅ til ÅÅÅÅ-MM-DD.|
|**Desimalformatering**|Definer regler for desimalplassering og avrundingspresisjon.|
|**Regulært uttrykk - Samsvar**|Bruk et regulært uttrykk for å finne én eller flere verdier. Dette ligner på alternativene **Delstreng** og **Vanlig uttrykk - Erstatt**.|
|**Egendefinert**|Dette er et avansert alternativ som krever assistanse fra en utvikler. Det muliggjør en integreringshendelse som du kan abonnere på, hvis du vil bruke din egen transformeringskode. Hvis du er utvikler og vil bruke dette alternativet, kan du se avsnittet "Tips for utviklere: eksempel på alternativet Egendefinert" nedenfor.|
|**Dato- og klokkeslettformatering**|Definer hvordan gjeldende dato skal vises i tillegg til tidspunktet på dagen.|

#### <a name="tip-for-developers-example-of-the-custom-option"></a>Tips for utviklere: eksempel på alternativet Egendefinert
Følgende eksempel viser hvordan du implementerer din egen transformeringskode.

```
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
Når du har definert reglene, kan du teste dem. I **Test**-delen skriver du inn et eksempel på en verdi du vil transformere, og deretter kontrollerer du resultatene.

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Slik eksporterer en datautvekslingsdefinisjon som en XML-fil som andre kan bruke:
Når du har opprettet datautvekslingsdefinisjonen for en bestemt datafil, kan du eksportere datautvekslingsdefinisjonen som en XML-fil som du kan importere. Dette er beskrevet i følgende fremgangsmåte.  

1. Skriv inn **Datautvekslingsdefinisjoner** i **Søk**-boksen, og velg deretter den tilknyttede koblingen.  
2. Velg datautvekslingsdefinisjonen du vil eksportere.  
3. Velg **Eksporter datautvekslingsdefinisjon**.  
4. Lagre XML-filen som representerer datautvekslingsdefinisjonen, på en passende plassering.  

    Hvis en datautvekslingsdefinisjon allerede er opprettet, trenger du bare å importere XML-filen til rammeverket for datautveksling. Dette er beskrevet i følgende fremgangsmåte.  

### <a name="to-import-an-existing-data-exchange-definition"></a>Slik importerer du en eksisterende datautvekslingsdefinisjon:  
1. Lagre XML-filen som representerer datautvekslingsdefinisjonen, på en passende plassering.  
2. Skriv inn **Datautvekslingsdefinisjoner** i **Søk**-boksen, og velg deretter den tilknyttede koblingen.  
3. Velg handlingen **Ny**. Siden **Datautvekslingdefinisjon** åpnes.  
4. Velg **Importer datautvekslingsdefinisjon**.  
5. Velg filen du lagret i trinn 1.  

## <a name="see-also"></a>Se også  
[Definere datautveksling](across-set-up-data-exchange.md)  
[Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Innkreve betalinger med SEPA direct debit](finance-collect-payments-with-sepa-direct-debit.md)  
[Betale med utvidelsen AMC Banking 365 Fundamentals eller SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Inngående dokumenter](across-income-documents.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
